# SVG animado no GitHub: SMIL, não CSS

O GitHub sanitiza SVG do repositório: remove `<script>`, atributos de evento e `<foreignObject>`. `<style>` ainda passa, mas é candidato a cair na próxima revisão de política — e aí a animação morre sem erro.

Elementos SMIL (`<animate>`, `<animateMotion>`) são SVG nativo, não script. Nenhum sanitizador os remove.

```xml
<animate attributeName="stroke-dashoffset" from="1400" to="0" dur="3s" fill="freeze"/>
```

Spec obsoleta, suporte universal. Nesse contexto é a aposta mais segura.
