# Contar PRs mergeados de um usuário

```bash
gh api "search/issues?q=is:pr+is:merged+author:USUARIO&per_page=1" --jq '.total_count'
```

Só enxerga repositório público — o número real pode ser maior. Útil quando alguma métrica depende dessa contagem e você não quer chutar.
