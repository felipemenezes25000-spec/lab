# Por que badge externo quebra e asset local não

Imagem de host externo no README passa pelo proxy **camo** do GitHub, que depende do serviço de origem responder. Rate limit lá vira ícone quebrado aqui.

Asset no próprio repositório é reescrito pra caminho same-origin (`/user/repo/raw/main/...`) e nem toca no camo. Dá pra confirmar lendo o HTML da página renderizada.
