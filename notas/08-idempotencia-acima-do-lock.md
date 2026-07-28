# Idempotência vale mais que o lock

Lock distribuído reduz contenção; ele **não** garante exclusão mútua absoluta. GC pause, partição de rede e relógio dessincronizado furam qualquer implementação.

Então cheque o estado dentro da transação antes de agir. O lock é otimização; a correção vem da idempotência.
