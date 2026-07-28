# Webfont não carrega em SVG usado como <img>

SVG referenciado por `<img>` renderiza isolado: sem script, sem rede, sem CSS herdado. Nenhum recurso externo é buscado — `@import` de fonte é ignorado.

O texto cai no fallback, muda de largura, e como SVG **não tem layout automático**, atravessa a borda da caixa sem avisar.

Use só stack de sistema: `ui-monospace, SFMono-Regular, Menlo, Consolas, monospace`.
