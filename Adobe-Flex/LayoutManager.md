# Adobe Flex

## LayoutManager


> So far you have used a variety of layout containers, including VBox and HBox, to arrange your component on the screen. For some of these components, you have provided explicit sizes by providing a fixed number for their height or width. For other components, you have provided relative sizes by providing a percentage for the height or width property. Howerver, you have left the decision of sizing the majority of your components and containers to the **Flex Layout Manager**.
> 
> Every *HBox*, *Label*, or *Button* that does not have an explicit or relative size specified must be assigned a size before it can appear on the screen. Flex components must be able to provide a recommendation of an appropriate size in this case. Each component provides this recommendation in unique way. For example, the *HBox* looks at all its children and determines how much space they will require. The *Label* takes the size of its text to account, and the *Button* examines both its text and icon, if present. The method inside each component that provides this recommendation is  called **_measure()_**.
> 
> When the *Layout Manager* needs to determine how to lay out a Flex application, it first asks all the components for their explicit or recommended sizes, starting with the most deeply nested and working toward the *Application* container.
> 
> Once the Layout Manager understands the required sizes, it works from the outermost container, the *Application* container, toward the most deeply nested component, assigning sizes and moving components to the appropriate place on the screen.
> 
> ![mx:Application > mx:ApplicationControlBar + (mx:HBox > (mx:VBox > mx:Label) + mx:Canvas)](_assets/LayoutManager-01.png "mx:Application > mx:ApplicationControlBar + (mx:HBox > (mx:VBox > mx:Label) + mx:Canvas)")
> 
> 
> The following narrative based on this diagram will help illustrate this layout mechanism.
> 
> The *Flex Layout Manager* asks the *Application* how much space it requires on the screen. Before the *Application* can respond, it must first ask the *ApplicationControlBar* and *HBox* how much space the each require. Unfortunately, the *HBox* needs to ask the *VBox* and *Canvas* before it can respond. In turn th *VBox* must ask the *Label*.
> 
> This means that the deepest nested child must determine its size before any of the components that contain it. Once the *Label* provides its size, th *VBox*, *Hbox*, and eventually the *Application* can respond to *Layout Manager*'s request.
> 
> So far we have referred to the sizes provided by each of these components as a recommendation. Ultimately, the sizes recommended by each of these components may add up to more than the total space available on the user's screen, so anoter pass through the components is required to size them appropriately.
> 
> The *Layout Manager* informs the *Application* container of the actual usable width and height. In turn, the *Application* container decides how much of that space to give to the *ApplicationControlBar* and how much to give the *HBox*. When the *HBox* receives its sizing information, it decides how much is provided to the *VBox* and how much to the *Canvas*. Finally, the *VBox* determines how much space to allocate to the *Label*. Immediately after each component determines the size of its children, it also determines where they should be placed whithin the component based on the layout rules implicit in their type (*HBox* lays out its children horizontally; *VBox* vertically.) The method inside each component that is responsible for sizing and positioning children is called **_updateDisplayList()_**.
> 
> The passes up and down the component hierarchy occur every time the application is resized. Based on the amount of work required, it becomes ease to see why a developer shoud limit unnecessary container nesting.

[Adobe Flex 3: Training from the Source - pgs 268,269](https://books.google.com.br/books?id=yFNZGjqJe9IC&pg=PA268&lpg=PA268)

Ou seja:

1. Todo *HBox*, *Label* ou *Button* que não tiver suas dimensões informadas explícitamente ou tamanho relativo especificado precisa definir um tamanho antes de aparecer na tela;
2. O método dentro de cada componente que provém esta recomendação de dimensões é o **_measure()_**;
3. As requisições de dimensão são feitas em um único sentido, do nó container principal para os nós mais internos, p.e.: No exemplo acima, o *LayoutManager* requisita as dimensões do *Application* que por sua vez, requisita as dimensões de seus nós filhos, que recursivamente vão requisitando as dimensões de seus respectivos nós filhos até os últimos nós sem filhos informarem suas dimensões, e assim as dimensões são informadas no caminho inverso até todas as dimensões estarem definidas e o *Application* passar suas dimensões finais para o *LayoutManager*;
4. Após isto, o *LayoutManager* informa ao *Application* a dimensão total da tela disponível, que por sua vez decide quanto de espaço é provido a cada um de seus filhos e assim subsequentemente definindo quanto de espaço está disponível para cada componente.
5. Imediatamente após todos os componentes determinarem o tamanho de seus filhos, estes também definem a posição onde cada subcomponente será colocado, baseado em suas próprias regras implicitas à seu tipo;