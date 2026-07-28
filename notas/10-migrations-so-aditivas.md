# Migration automática só pode ser aditiva

Se a task nova sobe, migra, e o deploy é revertido, a versão antiga encontra um schema que ela não conhece.

`DROP COLUMN` e `DROP TABLE` ficam fora do startup. Remoção é passo manual, em deploy separado, depois que ninguém mais lê a coluna.
