

# Criando uma key SSH no Ubuntu
Entre em ~/.ssh
```bash
cd ~/.ssh
```
Gera um ssh
```bash
ssh-keygen -t ed25519 -C "raul.myron@gmail.com"
```
Ele vai pedir
* name-file *
* password *
* re-enter-password *

Roda seu SSH
```bash
eval $(ssh-agent)
```

Adicione o agente aos truted hosts
```
ssh-add ~/.ssh/name-file
```

Aparecerá o pid do agente
```bash
ssh-add -l
ssh-add -l -E md5
ssh-add -l -E sha256
```
Agora pegue tudo que está escrito dentro do name-file.pub e coloque [a ssh key aqui](https://github.com/settings/keys)

voilá. em teoria deu certo. dont call me if it does not work. 
