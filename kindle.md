# kindle

## WinterBreaker


### Pré-requisitos

- Versões menor que 5.18
- O Kindle registrado
- Wifi

### Passos

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

### Instalando o KOReader

- Verifique a versão disponível no [link](https://kindlemodding.org/jailbreaking/post-jailbreak/koreader.html)
- Baixe no [link](https://github.com/koreader/koreader/releases)
- Extraia as pastas
- Copie o diretório koreader para a raiz e os arquivos da extensions para o diretório que já existe na raiz do Kindle
- A versão v comigo não funcinou, testarei a versão hf

## Método Sanctuary (mais simples)

- Pressione 3 pontos, escolha o navegador
- Vá ao site http://sanctuary.skyvincent.com/scroll (http não https)
- Verifique o tipo de scroll, se for uma barra semelhante a do Windows o método funciona caso seja uma barra flat fina de traço preto não
- Vá na página http://sanctuary.skyvincent.com/scroll
- Uma contagem se iniciará espere a contagem terminar, ao terminar será exibido uma página de ID
- Preencha no campo abaixo o mesmo valor exibido no campo de cima e clique em Connect (não precisa pressionar shift só ir digitando só caracteres hexadecimal sempre 0 nunca O)
- Uma nova página será exibida e arquivos serão baixados, algumas mensagens podem ser exibida
- Não dá pra saber o tempo de download mas é rápido, clique no X do navegador depois de alguns minutos
- Clique nos 3 pontos Configurações > Ajuda > Introdução
- Deixe a mágica acontecer
- Ao iniciar ele gera um gerenciador de pacote próprio que pode ser executado pela barra de pesquisa padrão com o comando: `;kpm`
- Para baixar o Koreader faça os comandos `;kpm update` `;kpm install koreader`

## Koreader:

Logs:

```
/mnt/koreader/crash.log
```

## Links

- [Site JailBreaker](https://kindlemodding.org/jailbreaking)
- [Repositório KOReader](https://github.com/koreader/koreader/releases)
