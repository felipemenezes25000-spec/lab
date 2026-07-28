# Imagem por tema no README com <picture>

```html
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/x-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="assets/x-light.svg">
  <img alt="descrição real" src="assets/x-light.svg">
</picture>
```

Dois arquivos é mais confiável que `@media` dentro do SVG: em contexto `<img>` o suporte a media query interna é inconsistente.
