# Operação longa em HTTP síncrono multiplica a corrida

Se assinar 40 documentos leva mais que o timeout do cliente, o cliente **repete**. E o retry é exatamente o que gera duas execuções concorrentes.

Tire da requisição: job assíncrono + progresso por WebSocket/SignalR, com polling de fallback. Some o timeout, some o retry, some a corrida.
