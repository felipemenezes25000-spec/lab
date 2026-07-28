# Hash no rodapé do PDF não protege nada

Quem edita o PDF edita o rodapé junto. Imagem de assinatura então é só desenho.

O que protege é assinatura **dentro** do PDF (padrão PAdES): ela cobre criptograficamente o byte range. Alterou um byte, a validação quebra — e o próprio leitor de PDF mostra, sem depender do seu sistema.
