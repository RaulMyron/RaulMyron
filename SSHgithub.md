

# Criando uma key SSH no Ubuntu
Entre em ~/.ssh
```bash
cd ~/.ssh
```
Gera um ssh
```bash
ssh-keygen -t ed25519 -C "raul.myron@gmail.com"
ssh-keygen -t rsa -b 4096 -C "example@example.com" //caso voce esteja antes de ssh 6.8
```
Ele vai pedir
* name-file *
* password *
* re-enter-password *

Roda seu SSH
```bash
eval $(ssh-agent -s)
```

Adicione o agente aos truted hosts
```
ssh-add ~/.ssh/name-file
```

Aparecerá o pid do agente, caso queira listar seu ssh-add
```bash
ssh-add -l
ssh-add -l -E md5
ssh-add -l -E sha256
```
```bash
cat name-file.pub
```
Agora pegue tudo que está escrito dentro do name-file.pub e coloque [a ssh key aqui](https://github.com/settings/keys)

voilá. em teoria deu certo. dont call me if it does not work. 
