# kindle

## JailBreaker WindBreaker

Esse método só funciona nas versões abaixo da 5.18.

## Pré-requisitos

- O Kindle precisa está registrado
- Wifi

## Passos

- Ative o modo avião (sem wifi)
- Reinicie o Kindle
- Plugue o Kindle no PC
- Delete os arquivos update-whatever.bin ou update.partial.bin caso existam
- Gere um arquivo de espaço deixando entre 50M-90M de espaço disponível afim de evitar qualquer update

```bash
# Recomendo gerar vários arquivos de 1GB e no fim ir ajustando
dd if=/dev/zero of=arquivo_1GB.img bs=1M count=1024 status=progress
```
- Copie os arquivos gerado para a raiz
- Baixe o arquivo do [WinterBreak](https://github.com/KindleModding/WinterBreak/releases/latest/download/)
- Extraia o arquivo
- Habilite a visualização de arquivos ocultos
- Copie todos os arquivos para inclusive os ocultos a raíz do Kindle
- Desconecte o Kindle
- Clique no carrinho de compras ou em um livro e desative o modo avião (com wifi)

Comigo apareceu algumas telas muito esquisitas, depois eu reiniciei e apareceu um livro chamado JAILBROKEN (o que é um bom sinal)
Esse livro pode ser apagado posteriormente.

- Conecte o Kindle no PC
- Baixe o Peki e Kual [Link](https://kindlemodding.org/jailbreaking/post-jailbreak/installing-kual-mrpi)
- Extraia o Kual e copie os diretórios extensions e mrpackages para a raiz do Kindle
- Extraia o Peki e copie os arquivos KUAL.sh e KUAL.jar para Kindle/docs
- Desconecte o Kindle
- Aparecerá um livro chamado Kual e parece

## Instalando o KOReader

- Verifique a versão disponível no [link](https://kindlemodding.org/jailbreaking/post-jailbreak/koreader.html)
- Baixe no [link](https://github.com/koreader/koreader/releases)
- Extraia as pastas
- Copie o diretório koreader para a raiz e os arquivos da extensions para o diretório que já existe na raiz do Kindle
- A versão v comigo não funcinou, testarei a versão hf

## Links

- [Site JailBreaker](https://kindlemodding.org/jailbreaking/)
- [Repositório KOReader](https://github.com/koreader/koreader/releases)
