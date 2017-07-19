# Como configurar o acesso ssh no terminal

* OS testado: Mac

### daí vc tá tentando configurar um acesso ssh no terminal, e se depara com esse arquivo perdido aqui pra te salvar. =D
eis a solução:


1. abra o terminal

2. execute: _**\> cd ~/.ssh**_
3. execute: _**\> nano config**_

4. adicione as configurações (exemplo abaixo):

```
Host vaidarjogo 
  HostName 52.67.3.41 
  User ubuntu 
  IdentityFile ~/.ssh/vaidarjogo.pem
```

5. _**ctrl+o**_ para salvar _(enter para confirmar o nome)_
6. _**ctrl+x**_ para sair

7. copie a chave _.pem_ para a pasta _.ssh_
	* comando: _**\> cp vaidarjogo.pem ../.ssh **_

8. adicione permissão na chave
	* comando: chmod 400 ../.ssh/vaidarjogo.pem

9. para executar (usando nome do Host no exemplo): _**\> ssh vaidarjogo **_