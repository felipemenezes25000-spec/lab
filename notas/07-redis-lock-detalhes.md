# Redis SET NX PX: os três detalhes

```
SET lock:{recurso} {tokenUnico} NX PX 30000
```

- **NX** — só grava se não existir. É daí que vem a atomicidade.
- **PX** — expiração obrigatória. Sem ela, task que morre no meio trava o recurso pra sempre.
- **token único** — na liberação, compare o valor antes de apagar (script Lua). Sem isso, uma task lenta cujo lock já expirou apaga o lock de outra.
