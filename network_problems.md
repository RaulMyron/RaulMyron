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

```bash
sudo dkms remove r8168/8.043.02 --all

sudo apt-get purge r8168-dkms
sudo apt-get update
sudo apt-get install r8168-dkms

```
Voilá

