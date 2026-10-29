# nvidia

## Atualização

Roteiro de Migração para a Série 550 (nvidia-550xx-dkms)

Passo 1: Instalar os Headers do Kernel e o DKMS

Para que o sistema consiga compilar o driver da NVIDIA sob medida para o seu Kernel atual, os arquivos de cabeçalho e o gerenciador de módulos são obrigatórios:

```bash
sudo pacman -S linux618-headers dkms
```

Passo 2: Remoção do Driver Legado AtualRemova totalmente o perfil 470xx via MHWD antes de puxar os pacotes do AUR:Bashsudo mhwd -r pci video-nvidia-470xx

```bash
sudo mhwd -r pci video-nvidia-470xx
```

Passo 3: Compilação e Instalação via yayInstale o módulo do driver e as bibliotecas de compatibilidade de 32 bits exigidas pela Steam:   Bashyay -S nvidia-550xx-dkms lib32-nvidia-550xx-utils

```bash
yay -S nvidia-550xx-dkms lib32-nvidia-550xx-utils
```

Passo 4: Atualização das Configurações de BootAtualize o menu do GRUB para fixar o carregamento do módulo:Bashsudo update-grub

```bash
sudo update-grub
```

Passo 5: Reinicialização e VerificaçãoReinicie a máquina:Bashsudo reboot

Reinicie a máquina:

```bash
sudo reboot
```

Confirme o funcionamento do driver:

```bash
nvidia-smi
```

A saída deve exibir a GPU GTX 970 e a versão do driver na série 550.xx

## Caso dê errado

Restaurar o snapshot do Timeshift (Mais rápido e garantido)

```bash
sudo timeshift --list
sudo timeshift --restore --snapshot '[ID]'
sudo reboot
```

Ou:

```bash
sudo pacman -Rns nvidia-550xx-dkms lib32-nvidia-550xx-utils
sudo mhwd -i pci video-nvidia-470xx
sudo update-grub
sudo reboot
```

Caso funcione pode remover o mhwd-nvidia-versao que ficou:

```bash
sudo pacman -Rdd mhwd-nvidia-580xx
```
