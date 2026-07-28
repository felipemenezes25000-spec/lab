# Cor que funciona no escuro não funciona no claro

`#00D9FF` fica ótimo sobre `#0d1117` e ilegível sobre branco.

A correção não é achar um valor que "quase serve" nos dois: é ter um valor por tema (`#0969DA` no claro). E validar o par (texto, fundo) contra o WCAG no gerador de tokens, quebrando o build quando reprova.
