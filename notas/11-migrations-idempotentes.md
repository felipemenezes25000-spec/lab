# Migration no startup precisa ser idempotente

Com N tasks subindo juntas, elas **vão** correr em paralelo na primeira subida. Não confie só na tabela de controle:

```sql
CREATE TABLE IF NOT EXISTS ...
ALTER TABLE x ADD COLUMN IF NOT EXISTS ...
```

E envolva tudo num `pg_advisory_lock`.
