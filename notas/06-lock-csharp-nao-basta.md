# lock do C# não serve pra várias instâncias

`lock`, `Monitor`, `SemaphoreSlim` e `Mutex` coordenam **threads do mesmo processo**. Com N tasks no ECS você tem N processos em máquinas diferentes — cada um respeita o próprio lock e faz a operação duplicada.

Precisa de árbitro externo: lock distribuído em Redis, ou `pg_advisory_lock` se o Postgres já está no caminho.
