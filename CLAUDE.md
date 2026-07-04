# CLAUDE.md — Projeto do livro "Do Chat ao Cowork e Code"

## Visão geral
Este repositório é um **livro técnico em Quarto** (HTML + PDF) intitulado
*Do Chat ao Cowork e Code — colaboração, automação e desenvolvimento com
agentes de IA*. O livro ensina o uso de Claude Chat, Claude Cowork e Claude
Code, com ênfase em Cowork e Code.

## Público-alvo
Professores e estudantes universitários de **todas as áreas** (medicina,
direito, história, biologia, etc.), **não-desenvolvedores**. Toda explicação
parte do princípio de que o leitor é academicamente sofisticado, mas não
tem experiência com terminal ou programação. Evite pressupor conhecimento
técnico; introduza cada conceito antes de usá-lo.

## Tese editorial
O livro segue um arco progressivo de autonomia delegada ao agente:
**conversar (Chat) → colaborar (Cowork) → automatizar/programar (Code)**.
Cada parte sobe um degrau nessa escala.

## Idioma e terminologia
- Idioma: **português do Brasil**.
- Termo principal em **PT-BR** (como aparece na interface), com o termo em
  inglês entre parênteses **apenas na primeira menção** de cada conceito.
- Mantêm-se em inglês (itálico na estreia) termos sem tradução consagrada:
  *token*, *prompt*, *skill*, *MCP*, *commit*. Todos entram no glossário.
- Há um quadro de equivalências PT-BR ↔ inglês no Apêndice C.
- Grafias fixadas pelo autor: **PUBMED** (caixa alta, artigo masculino: "o PUBMED"),
  não "PubMed". Aplicar em todo o livro.

## Tom e estilo
- Registro **técnico-profissional e sóbrio**. Nada de títulos "de chamada"
  ou linguagem de marketing. Títulos de seção nomeiam o assunto, não o vendem.
- Texto majoritariamente em **prosa**; listas apenas quando realmente
  esclarecem (passos, comparações, requisitos).
- Explique conceitos com exemplos do contexto acadêmico das diversas áreas.

## Vícios de escrita a evitar (lista viva — ampliar conforme o autor apontar)
- **Menos palavras.** Frase enxuta; não encher o saco do leitor. Cortar tudo
  que pode sair sem perder o sentido.
- **Sem frases de embrulho/meta:** nada de "é disso que trata este capítulo",
  "é dele que trata…", "vale abrir o mecanismo com um exemplo", "neste capítulo
  veremos…". Ir direto ao ponto.
- **Termos a evitar** (soam a IA ou a gíria): *deslocamento*, *despenca*.
  (lista cresce conforme a revisão do autor)
- **Clichês/transições de IA a cortar:** "porta de entrada", "em três atos",
  "a Parte/capítulo X fecha/encerra…", "convém (também) ter presentes…",
  "que acabamos de descrever", "o mesmo movimento…", "que hoje organizam/
  dominam…", "por isso fala/é/faz…" (personificação + "por isso"), "a diferença
  é de grau, não de espécie", "as próximas seções tratam de… / o Cap. X
  retoma…" (anúncio do que vem), abrir frase com "Quando…" (soa infantil),
  molduras-revelação ("A virtude/razão que explica tudo é uma só:", "A diferença
  aparece quando…"), fórmulas de resumo ("Em uma frase:", "Em suma:") e
  retro-referência meta ("No capítulo anterior vimos…"). Dizer de forma direta
  e simples.
- **Sem pompa nem exagero.** Evitar tom autoritário ou grandioso ("explora a
  fundo", "domina", "definitivo", "exaustivo"). O livro é introdutório e
  prático; **não** trata do funcionamento interno (o que é um *transformer*,
  como uma LLM funciona por dentro). Voz de conversa, modesta. Nada de frases
  de marketing ou autoajuda ("está no lugar certo", "domine de uma vez").
- **A arquitetura do agente é permitida; o interior do modelo, não.** A regra
  acima veda o que está *dentro* do modelo (pesos, atenção, como o *transformer*
  computa). Ela **não** veda a camada *acima* do modelo — o **harness** (loop,
  ferramentas, montagem de contexto, permissões), a **orquestração** de
  subagentes e o **comportamento observável** (por que o agente alucina, por que
  a mesma pergunta varia, o que o esforço/pensamento estendido faz). Essa
  profundidade é o diferencial do livro (Cap. 5, O harness) e deve ser tratada
  na altitude comportamental: descrever o que se observa e por quê, sem abrir a
  matemática interna. Tese editorial: **um modelo, muitos harnesses** — o que
  distingue Chat, Cowork e Code é o harness, não o modelo.
- **Nunca afirmar algo falso sobre o funcionamento.** Ex.: o agente **grava** o
  código nos arquivos (scripts, documentos Quarto) e o executa — é errado dizer
  que "você não vê o código".
- **Cuidado com "sem código"/"sem programar".** O agente (Cowork e Code)
  escreve e executa código; quem não precisa programar é o **usuário**. Deixar o
  sujeito (o usuário) explícito, para não dar a impressão de que o produto não
  lida com código.
- **Sem endereçamento direto ao leitor.** Nada de "você" nem possessivos de 2ª
  pessoa ("seu/sua" referidos ao leitor) na voz do livro. Preferir, alternando:
  "o usuário", construção impessoal, "quem pesquisa/escreve". **Exceção:** falas
  de exemplo (prompts entre aspas/itálico) mantêm o "você". **Imperativos
  dirigidos ao leitor são permitidos** em trechos práticos ("Reveja", "peça",
  "anexe") — instrução direta sem "você" explícito (decisão de jul/2026).

## Conteúdo reaproveitado do curso (Vibe_Coding_Project)
- **Tudo que vem de `Vibe_Coding_Project` é NÃO VERIFICADO** — texto e
  bibliografia foram gerados por IA e ainda não conferidos pelo autor. Tratar
  como rascunho a verificar; **nunca** apresentar como fato. Conferir cada
  afirmação e cada referência (o DOI resolve? o ano confere?) antes de validar.

## Regras de exatidão (importante)
- **Não invente funcionalidades.** Antes de afirmar como uma função do Claude
  funciona, verifique na documentação oficial (code.claude.com/docs,
  docs.claude.com, support.claude.com). Se incerto, sinalize.
- **Não invente citações.** Toda referência deve ser verificável: o DOI
  resolve, o periódico existe, o ano confere. Citações fabricadas são o pior
  erro possível neste livro.
- Marque trechos a confirmar com `<!-- TODO: verificar -->`.

## Convenções técnicas (Quarto)
- Um arquivo `.qmd` por capítulo, em `capitulos/`; apêndices em `apendices/`.
- Cada capítulo começa com um `#` (título) e usa `##` para as seções
  (os "tópicos" definidos no sumário) e `###` para subseções.
- **Títulos curtos.** Tanto o título de capítulo (`#`) quanto os de seção
  (`##`/`###`) devem ser curtos (ideal ≤ 5 palavras), nominais e diretos — para
  não poluir a barra lateral nem o índice "Nesta página". Evitar a construção
  "Tema: explicação" com dois-pontos e não listar todos os itens no título.
- Figuras ficam em `images/`, com nomes descritivos (ex.:
  `cowork-tela-inicial-home.png`), referenciadas com legenda e rótulo.
- **Referências cruzadas**: todo título de capítulo/apêndice leva um ID
  `{#sec-...}` — slug curto, em inglês (ex.: `sec-harness`, `sec-glossary`).
  A remissão no texto mantém "Cap."/"Capítulo"/"Apêndice" e usa a forma sem
  prefixo no número: `(Cap. -@sec-mcp)` renderiza "(Cap. 6)". Não usar
  `@sec-x` puro, que renderizaria "Capítulo 6" por extenso. Menções a
  "Parte I–V" ficam manuais (partes não recebem ID no Quarto).
- **Citações**: bibliografia em BibTeX (`references/references.bib`); citar com `[@chave]`.
  Estilo padrão **Nature** (`references/csl_styles/nature.csl`), por poluir
  menos o visual; Vancouver e ABNT disponíveis como alternativas. O `_quarto.yml` usa
  `reference-section-title: "Referências"`, que põe esse título antes da lista
  de referências no fim de cada capítulo (recurso nativo do Quarto book — sem
  extensão).
- Use *callouts* do Quarto para boxes ("Na prática", "Atenção", "Para
  aprofundar").
- Formatos de saída: **HTML e PDF**. Opções de formato ficam no `_quarto.yml`,
  não nos capítulos.
- **Sem hard-wrap.** Nos arquivos `.qmd`, escrever cada parágrafo em **uma única
  linha** (sem quebra de linha manual) — facilita a edição e os diffs.

## Estrutura de pastas
- `capitulos/` — os capítulos (`.qmd`), em subpastas por parte
  (`p1-fundamentos/`, `p2-conversar/`, `p3-colaborar/`, `p4-programar/`,
  `p5-pratica-responsavel/`); o prefixo `NN-` mantém a ordem global. Figuras
  referenciadas com caminho a partir da raiz: `/images/...` (não `../images/...`).
- `apendices/` — apêndices
- `images/` — capturas de tela e diagramas
- `references/csl_styles/` — estilos de citação (Nature padrão; Vancouver, ABNT)
- `_source/`, `code/` — material de apoio e exemplos de código
- `fonts/` — fontes (tipografia ainda a definir)
- `_quarto.yml` — configuração do livro; `index.qmd` — prefácio/início

## Convenções de imagens
Nomes em minúsculas, com hífens, descritivos do conteúdo da tela
(`produto-area-elemento.png`). Sempre adicionar legenda e texto alternativo.

## Fluxo de trabalho
- **Antes de escrever, ler `notas.md`** (decisões, status e mapa de
  reaproveitamento do curso) **e `figuras.md`** (mapa de imagens). A
  bibliografia importada do curso está marcada como **NÃO VERIFICADA**.
- **Antes de redigir a prosa, usar a skill `writing-style`**
  (`.claude/skills/writing-style/SKILL.md`): retrato do estilo do autor +
  ofício (Zinsser, Friedman, Bates) + leitor e fluxo (Pinker, Williams, Othon
  Garcia, Clark, Provost), com checklist único de revisão. Correções do autor
  em trechos redigidos viram pares antes/depois na "Lista viva" da skill.
  (`_source/guia-escrita-resumo.txt` é a versão estendida do mesmo material,
  com marcadores de fonte; mudanças de conteúdo devem ser feitas nos dois.)
- Discutir estrutura/decisões no chat **antes** de escrever arquivos, quando
  a mudança for editorial.
- Ao escrever um capítulo, seguir os tópicos já definidos no sumário.
- Ao terminar, conferir links, citações e consistência terminológica.

## Decisões em aberto (não tratar como fechadas)
- Tipografia/fontes do livro.
- Inclusão do Apêndice E (folha de referência de Markdown).
- Menção a Zotero/Mendeley no Cap. 16.
