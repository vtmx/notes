# zram

Verifica se o kernel tem suporte para zram (caso não houver erro suporta):

```bash
sudo modprobe zram
```

Verifica se o dispositivo pode ser criado:

```bash
ls /sys/class/zram-control/
```

Verifica os algoritmos disponíveis:

```bash
cat /sys/block/zram0/comp_algorithm
```

Cria arquivo de configuração:

```bash
sudo vim /etc/system/zram-generator.conf
```

Conteúdo do arquivo:

```ini
[zram0]
# Total de ram dividido por 3
zram-size = ram /3
# Algoritmo mais equilibrado
compression-algorithm = zstd
```

Verifica se o módulo zram está carregado:

```bash
lsmod | grep zram
```

Verifica o tamanho da zram:

```bash
cat /sys/block/zram0/size
```

Verifica a utilização da zram:

```bash
cat /sys/block/zram0/usage
```

Verifica processos que estão usando a zram:

```bash
lsof /dev/zram0
```
