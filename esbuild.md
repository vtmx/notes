# esbuild

```
--bundle
Faz o bundle dos arquivos, import css e js

--minify
Minifica os arquivos

--watch
Verifica a cada mudança para atualizar

--outbase=static
Diretório base

--outdir=public
Diretório de saída

--loader:.woff2=copy
Copia arquivos para o local de origem

--inject:src/livereload.js
Injeta script do livereload
new EventSource('/esbuild').addEventListener('change', () => location.reload());
```

## Links

- https://til.jakelazaroff.com/esbuild/run-a-development-server-with-live-reload
