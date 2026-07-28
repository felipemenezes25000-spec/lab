# Artefato gerado + gitignored = "funciona na minha máquina"

Arquivo que o dev server gera mas o git ignora (tipo `.expo/types/router.d.ts`) fica defasado em clone limpo. O typecheck falha em CI por um motivo que não tem nada a ver com o código.

Ou gere como parte do build, ou versione. O meio-termo é o pior dos dois.
