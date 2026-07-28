# Baseline de lint que só pode diminuir

Proibir um anti-padrão de uma vez em base legada gera centenas de erros e o time desliga a regra.

Em vez disso: conte as violações hoje, grave num `baseline.json`, e faça o CI falhar se o número **subir**. Ao cair, atualize o baseline.

Vira catraca — só anda num sentido. Serve pra `any` de TypeScript, warning de compilador, arquivo sem teste.
