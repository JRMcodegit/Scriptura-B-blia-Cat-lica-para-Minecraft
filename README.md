# Scriptura — Bíblia Católica para Minecraft

> **Resumo:** Bíblia católica em português, organizada em livros e volumes para leitura dentro do Minecraft Java e de implementações compatíveis com datapacks, como o Horizon Client.

**Autor / mantenedor:** `JRMcodegit`  
**Versão do projeto:** `1.0.0`  
**Idioma:** Português  
**Cânon pretendido:** 73 livros (46 do Antigo Testamento e 27 do Novo Testamento)  
**Formato:** datapack Minecraft (`pack.mcmeta`, funções `.mcfunction` e livros escritos)  
**Licença do código original:** MIT — ver `LICENSE`  
**Licença dos textos bíblicos:** não abrangida pela licença MIT; ver `TEXTOS-E-FONTES.md`.

## Sobre o projeto

O **Scriptura** organiza uma edição portuguesa histórica da Bíblia, associada à tradução da Vulgata pelo Padre António Pereira de Figueiredo, em livros escritos do Minecraft. O objetivo é permitir leitura e consulta dentro do jogo, com os livros bíblicos separados em volumes e distribuídos por lotes de comandos.

Este é um projeto comunitário e não oficial. Não é afiliado, patrocinado ou endossado pela Mojang, Microsoft, Igreja Católica, Iter Fidei ou Bíblia Traduzida.

## O que contém

- Organização prevista dos 73 livros do cânon católico.
- Separação do texto em livros e volumes adequados às limitações dos livros escritos do Minecraft.
- Funções para consultar informações e distribuir lotes de volumes.
- Estrutura de datapack para instalação por mundo.

> **Integridade textual:** a conclusão do processo de geração não substitui uma revisão bíblica/editorial independente. Correções de transcrição, numeração, acentuação e divisão de volumes podem ser necessárias. Consulte o relatório produzido pelo gerador e confira os volumes no jogo.

## Instalação — Minecraft Java

1. Faça uma cópia de segurança do mundo.
2. Copie a pasta `Biblia_Catolica_Minecraft` para `<pasta-do-mundo>/datapacks/`.
3. Confirme que `pack.mcmeta` está diretamente dentro da pasta instalada, ao lado de `data/`.
4. Entre no mundo e execute `/reload`.
5. Verifique com `/datapack list` se o datapack está habilitado.

## Instalação — Horizon Client

1. Abra a instância e o mundo desejados no Horizon.
2. Na seção **Data packs** do mundo, adicione a pasta do datapack ou um ZIP válido.
3. Se preferir instalação manual, use **Open folder** na seção de datapacks e copie a pasta inteira.
4. Entre no mundo, execute `/reload` e confira `/datapack list`.

O Horizon implementa um subconjunto das funcionalidades de datapacks. A compatibilidade deve ser confirmada na versão específica do cliente; recursos que não sejam usados por este datapack podem não estar implementados.

## Comandos

Consulte primeiro as informações do pacote:

```mcfunction
/function biblia:info
```

Distribua os volumes em lotes, guardando os livros antes de solicitar o seguinte:

```mcfunction
/function biblia:give_batch_001
/function biblia:give_batch_002
/function biblia:give_batch_003
```

Continue seguindo a numeração efetivamente gerada. Não presuma que existam exatamente três lotes. Se o namespace ou os nomes de função da sua geração forem diferentes, use os caminhos presentes em `data/`.

## Estrutura esperada

```text
Biblia_Catolica_Minecraft/
├── pack.mcmeta
├── README.md
├── LICENSE
├── TEXTOS-E-FONTES.md
├── CREDITOS.md
├── CHANGELOG.md
├── CONTRIBUTING.md
└── data/
    └── ... arquivos do datapack ...
```

Os documentos desta distribuição são complementares. Não substitua o `pack.mcmeta` gerado: o campo `pack_format` e demais campos de compatibilidade devem permanecer os que o gerador criou para a versão-alvo.

## Licença

A licença MIT aplica-se **somente ao código original deste projeto**, como scripts de geração e funções/comandos escritos originalmente para automatizar o datapack, na medida em que sejam efetivamente criação do mantenedor. Ela não concede direitos sobre textos bíblicos de terceiros, transcrições digitais, edições modernas, imagens, fontes ou conteúdo editorial de sites.

Consulte `TEXTOS-E-FONTES.md` antes de redistribuir publicamente uma compilação que contenha texto obtido de transcrições eletrônicas de terceiros.

## Como contribuir

Consulte `CONTRIBUTING.md`. Ao relatar um erro bíblico, informe livro, capítulo, versículo, texto observado, texto esperado e a fonte consultada. Evite corrigir um versículo sem registrar a edição e a referência usada.

## Aviso

O projeto é fornecido “como está”, sem garantia de ausência de erros. Faça backup dos mundos antes de instalar datapacks e teste primeiro em um mundo de cópia.
