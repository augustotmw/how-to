# Como fazer um triangulo arredondado com css?

**Autor:** Augusto TMW


### Referências:

* (http://stackoverflow.com/q/14446677/1397351)
* (http://dabblet.com/gist/4592062)


### Rounded triangle

**css**

```css

.triangle {
	position: relative;
	background-color: orange;
	text-align: left;
}
.triangle:before,
.triangle:after {
	content: '';
	position: absolute;
	background-color: inherit;
}
.triangle,
.triangle:before,
.triangle:after {
	width:  10em;
	height: 10em;
	border-top-right-radius: 30%;
}

.triangle {
	transform: rotate(-60deg) skewX(-30deg) scale(1,.866);
}
.triangle:before {
	transform: rotate(-135deg) skewX(-45deg) scale(1.414,.707) translate(0,-50%);
}
.triangle:after {
	transform: rotate(135deg) skewY(-45deg) scale(.707,1.414) translate(50%);
}

```

### Rounded alert

**scss**

```scss

.rounded-triangle {
	display: table;
	font-size: 1.7em;

	.triangle {
		position: relative;
		background-color: orange;
		text-align: left;
		transform: rotate(-60deg) skewX(-30deg) scale(1,.866);
		z-index: 1;

		&:before,
		&:after {
			content: '';
			position: absolute;
			background-color: inherit;
		}

		&,
		&:before,
		&:after {
			width:  1em;
			height: 1em;
			border-top-right-radius: 30%;
		}

		&:before {
			transform: rotate(-135deg) skewX(-45deg) scale(1.414,.707) translate(0,-50%);
		}
		&:after {
			transform: rotate(135deg) skewY(-45deg) scale(.707,1.414) translate(50%);
		}
	}

	&.alert {
		&:before {
			content: '!';
			display: block;
			font-size: 1em;
			color: #fff;
			position: absolute;
			top: 70%;
			left: 50%;
			@include transform(translate(-50%, -50%));
			z-index: 2;
		}
	}
	
			
}


```

**html**

```html

<div class="rounded-triangle alert"><div class="triangle"></div></div>

```
