# Instalação de Custom ROM no Redmi Pad SE

Este guia cobre todas as etapas para desbloquear o bootloader, instalar o TWRP e aplicar uma ROM personalizada no Redmi Pad SE (codinome: xun).

## Etapa 1: Desbloquear o Bootloader

1. Ativar opções de desenvolvedor
- Vá em Configurações > Sobre e verifique se está com a versão MIUI V14.0.2.0.TLYMIXM
- Toque 7 vezes em Versão do MIUI para ativar o modo desenvolvedor
- Acesse Configurações > Configurações adicionais > Opções de desenvolvedor
- Ative Desbloqueio OEM e Depuração USB
- Em Status de desbloqueio do Mi, clique em Concordo

2. Reiniciar em modo Fastboot
- Verifique se o dispositivo é reconhecido com o comando: `adb devices`
- Verifique se os pacotes estão instalados com: `adb --version & fastboot --version`
- Execute o comando para reiniciar em mobo do boot: `adb reboot bootloader`
- Ou desligue o aparelho e ligue segurando Power + Volume Acima até aparecer o modo Fastboot

4. Desbloquear com XiaoMiTool
- Baixe o XiaoMiTool V2
- Execute o comando: `chmod +x XMT2_Linux_20.7.28.run && ./XMT2_Linux_20.7.28.run`
- Siga as instruções. Pode ser necessário aguardar entre 72h e 168h
- Clique em Unlock > Unlock Anyway
- No aparelho um ícone de cadeado aberto aparecerá na tela indicando sucesso

## Etapa 2: Transferir Arquivos via Fastboot

- Com o dispositivo em modo Fastboot, verifique a conexão: `astboot devices`
- Transfira os arquivos para o dispositivo:

```
fastboot flash boot boot-lineage-20.0-20231215-UNOFFICIAL-yunluo.img
fastboot flash vendor_boot-lineage-20.0-20231215-UNOFFICIAL-yunluo.img
fastboot flash boot twrp_3.7.1_xun.img
```

- Para iniciar o TWRP, desligue o aparelho e pressione Power + Volume Acima.

Observação: a Xiaomi utiliza a partição boot para o TWRP em alguns modelos. Por isso, não use fastboot flash recovery.

## Etapa 3: Instalar a Custom ROM

1. Formatar dados
- No TWRP: vá em Factory Reset > Format Data > Format Data

2. Instalar ROM via ADB
- No TWRP: Apply Update > Apply from ADB
- Execute o comando: `db sideload lineage-20.0-20231215-UNOFFICIAL-yunluo.zip`

3. Instalar GApps
- Execute o comando: `db sideload NikGapps-core-arm64-15-20250716-signed.zip`
- Confirme com Yes se aparecer aviso de assinatura

4. Reiniciar o sistema
- No TWRP: Reboot > System

5. (Opcional) Backup da ROM original
- No TWRP: Backup > selecione todas as partições > Swipe para salvar

## Considerações Finais

- Se ocorrer bootloop, volte ao TWRP e limpe Cache e Dalvik, ou reinstale a ROM
- Mantenha backups da ROM original e do TWRP em local seguro
- Verifique sempre a compatibilidade da ROM com o codinome xun

## Links Úteis

Tutoriais em vídeo:
- https://www.youtube.com/watch?v=xlEp9NLjeD4
- https://youtu.be/F74wVDGm5Ts?feature=shared

Ferramentas:
- https://github.com/francescotescari/XiaoMiToolV2/releases
- https://xiaomifirmware.com/downloads/download-adb-fastboot-platform-tools-r34-0-5-usb-drivers

TWRP:
- https://unofficialtwrp.com/twrp-3-7-0-root-redmi-pad-se-xun
- https://t.me/Redmi_Pad_SE/1339

ROMs:
- https://github.com/xiaomi-mt6789-devs/releases/wiki/Installation

GApps:
- https://opengapps.org
- https://nikgapps.com
- https://www.droidthunder.com/gapps

Root:
- https://github.com/topjohnwu/Magisk/releases

Downloads:
- [LineageOS for Redmi Pad SE](https://github.com/xiaomi-mt6789-devs/releases/releases)
- [XiaomiTool 1](https://xiaomitool.com/V2/download)
- [XiaomiTool 2](https://github.com/francescotescari/XiaoMiToolV2/releases)
- [TWRP 1](https://www.mediafire.com/file/xuzwckutp9v75hf/XUN_recovery.rar/file)
- [TWRP 2](https://t.me/Redmi_Pad_SE/1339)
- [Magisk](https://github.com/topjohnwu/Magisk/releases)
- [Gapps](https://sourceforge.net/projects/nikgapps/files/Releases/Android-15)
