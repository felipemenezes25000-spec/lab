# Duas fontes de verdade de schema é bomba-relógio

É comum existir um runner de migration versionado **e** um `.sql` grandão que alguém roda à mão em produção.

Os dois divergem. Um dia a mesma tabela existe com definições diferentes em ambientes diferentes, e o bug aparece só em prod. Escolha qual manda e faça o outro derivar dele.
