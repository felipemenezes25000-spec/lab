# Hook de pre-push valida a árvore, não o commit

Um pre-push que escolhe o que compilar pelo diff de commits, mas compila o **working tree**, bloqueia qualquer push quando existe WIP não commitado de outro trabalho.

Se for validar a árvore, diga isso na mensagem de erro. O dev perde meia hora procurando erro no código que ele nem mexeu.
