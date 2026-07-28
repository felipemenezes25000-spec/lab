# Certificado e segredo fora do repositório

PFX, chave privada e senha vão pra secrets manager ou KMS. Nunca no repositório, nunca embutido em imagem Docker, nunca em variável de ambiente commitada.

Vale lembrar: apagar num commit posterior **não** remove do histórico.
