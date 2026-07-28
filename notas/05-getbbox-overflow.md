# Detectar overflow de texto em SVG com getBBox()

Errar a largura média do caractere em 1,5px já estoura uma pílula. Meça, não estime:

```js
const b = el.getBBox();
if (b.x + b.width > caixa.x + caixa.width - 8) console.log('OVERFLOW', el.textContent);
```

**Falso positivo clássico:** ao achar "a caixa que contém este texto", exija que o *início* do texto esteja dentro dela. Se você só exigir que fique à direita da borda esquerda, toda caixa mais à esquerda casa e o detector acusa overflow inexistente.
