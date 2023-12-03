# Criando uma key SSH no Ubuntu
Liste todos os drivers de rede
```bash
lspci -nnk | grep -iA2 net
```
Pronto, agora dá pra resolver metade dos problemas, no meu caso no ubuntu geralmente é erro de driver, 
```bash
sudo modprobe -r r8168; sudo modprobe r8169
sudo mhwd -r pci network-r8168
ubuntu-drivers autoinstall
```
Voilá

