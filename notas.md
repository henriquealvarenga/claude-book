# Notas do livro — *Do Chat ao Cowork e Code*

> Arquivo de trabalho. Reúne as decisões editoriais e os conteúdos discutidos
> no chat que devem constar no livro. Serve de base para a redação dos
> capítulos. Itens marcados com **[verificar]** precisam de conferência factual
> antes da publicação (regra do `CLAUDE.md`: não inventar). As fontes citadas
> estão em `references/references.bib`.

## 1. Identidade e metadados

- **Título:** Do Chat ao Cowork e Code
- **Subtítulo:** colaboração, automação e desenvolvimento com agentes de IA
- **Público:** professores e estudantes universitários de todas as áreas
  (medicina, direito, história, biologia, etc.), **não-desenvolvedores**.
- **Tese editorial:** **um modelo, muitos harnesses** — existe *um* modelo; o
  que distingue Chat, Cowork e Code é o harness montado em volta dele. Sobre
  essa espinha corre um arco progressivo de autonomia delegada ao agente —
  **conversar (Chat) → colaborar (Cowork) → programar (Code)**. As partes são
  nomeadas pela **atividade** (o produto entre parênteses); os conceitos comuns
  (harness, MCP, permissões, CLAUDE.md, skills) moram **uma vez** na Parte I, e
  os capítulos de produto remetem a ela em vez de reexplicar. O Cap. 5 (O
  harness) dá a fundamentação técnica dessa tese.
- **Tom:** técnico-profissional, sóbrio; títulos nomeiam o assunto, não vendem.
- **Idioma/terminologia:** PT-BR como termo principal (como na interface), com
  o inglês entre parênteses na 1ª menção; glossário no Apêndice C. Ficam em
  inglês: *token*, *prompt*, *skill*, *MCP*, *commit*.
- **Formato de saída:** HTML + PDF. Citação em BibTeX + CSL (**Nature padrão**;
  Vancouver e ABNT alternativos — ver §8, "CSL").
- **Tipografia:** **em aberto** (fontes Playfair/Inter/JetBrains presentes na
  pasta, mas não confirmadas).

### Identidade visual
- **Paleta:** grafite `#26211D`, terracota `#C15F3C`, papel `#F6F3EC`, texto
  claro `#F2ECE3`, apagado `#9A8E80`.
- **Capa:** Conceito B (fundo grafite), em `images/capa-favicon/`. Motivo: cada
  produto na sua tipografia (serifa=humano, sans=ponte, mono=máquina) + degrau
  de três blocos. Kicker "TRABALHANDO COM O CLAUDE".
- **Favicon:** degrau de três blocos terracota sobre grafite, em
  `images/capa-favicon/`.

## 2. Estrutura (33 capítulos, 5 partes + apêndices)

> Reestruturada em jul/2026: partes nomeadas pela **atividade** (produto entre
> parênteses); dois capítulos novos (5 O harness; 30 Injeção de prompt). Ver §1
> (tese "um modelo, muitos harnesses").

**Parte I — Fundamentos** (9): 1 A virada agêntica · 2 A Anthropic e o Claude:
breve história · 3 O ecossistema Claude · 4 Como um agente trabalha · **5 O
harness** *(novo)* · 6 MCP · 7 Markdown · 8 Setup · 9 Personalização.

**Parte II — Conversar (Claude Chat)** (2): 10 Prompt · 11 O Chat na prática.
(Chat enxuto, por decisão editorial.)

**Parte III — Colaborar (Claude Cowork)** (9): 12 Primeiros passos · 13 Tarefas
e pastas · 14 Skills · 15 Conectores e Plugins · 16 Análise de dados (era
"Documentos acadêmicos" — reformulação de 04/07/2026, ver §13) · 17 Referências
e citações (BibTeX) · 18 Artefatos · 19 Programado e Despacho · 20 Estudos de
caso por área.

**Parte IV — Programar (Claude Code)** (9): 21 Code (apresentação do produto) ·
22 Terminal · 23 Instalação e o primeiro projeto · 24 CLAUDE.md e configuração ·
25 Comandos, skills e permissões · 26 MCP e conectores · 27 Claude Code no IDE ·
28 Dados e análise · 29 Pesquisa reproduzível.

**Parte V — Prática** (4): 30 Boas práticas, limites e verificação ·
31 Ética, integridade acadêmica, privacidade e custos · **32 Injeção de prompt /
a tríade letal** *(penúltimo)* · 33 O futuro do trabalho intelectual com
agentes.

**Apêndices:** A Instalação por SO · B Referência rápida de comandos ·
C Glossário PT-BR↔inglês · D Recursos e documentação oficial · E Folha de
referência de Markdown **(proposto)** · F Os verbos do *spinner* (lista lúdica;
`apendices/apendice-f-verbos-do-spinner.qmd`) · G Claude Science (vertical de
ciências da vida) **(proposto, jul/2026 — ver §3)**.

> Nota: numeração pode oscilar; ao escrever, confirmar no `_quarto.yml`.

### 2.1 Por que a estrutura mudou (reestruturação de jul/2026)

> Registro para quem retomar o livro (humano ou agente): o que foi feito e por
> quê. O mapa antigo→novo completo está em `mapa-renumeracao.md` (raiz).

**O que mudou.** O livro passou de **29 para 31 capítulos** e as partes deixaram
de ser nomeadas pelo produto (Claude Chat / Cowork / Code) para serem nomeadas
pela **atividade**, com o produto entre parênteses:

- **Antes:** Parte II *Claude Chat* · III *Claude Cowork* · IV *Claude Code*.
- **Depois:** Parte II *Conversar (Claude Chat)* · III *Colaborar (Claude
  Cowork)* · IV *Programar (Claude Code)*.

Dois capítulos novos entraram: **5 O harness** (Parte I) e **30 Injeção de
prompt / a tríade letal** (penúltimo da Parte V). Tudo o que vinha depois foi
renumerado uma única vez.

As **pastas** em `capitulos/` também foram renomeadas para espelhar as partes:
`p2-chat`→`p2-conversar`, `p3-cowork`→`p3-colaborar`, `p4-code`→`p4-programar`
(as pastas `p1-fundamentos` e `p5-pratica-responsavel` já eram temáticas e não
mudaram). Ao mover uma pasta de parte, lembrar de atualizar os caminhos no
`_quarto.yml` — é lá que a ordem e a inclusão de cada capítulo são definidas.

**Por que mudou.** Três razões, na ordem em que pesaram:

1. **Sobreposição real entre os produtos.** Chat, Cowork e Code compartilham os
   mesmos conceitos (MCP, permissões, `CLAUDE.md`, skills). Nomear as partes
   pelo produto obrigava a reexplicar cada conceito três vezes e sugeria três
   ferramentas separadas, quando na prática são três formas de acionar **o mesmo
   modelo**. Nomear pela atividade (conversar / colaborar / programar) descreve o
   que o leitor *faz*, não qual botão aperta, e permite que cada conceito comum
   more **uma vez** na Parte I, com os capítulos de produto remetendo a ela.
2. **A tese "um modelo, muitos harnesses".** A reestruturação ganhou uma espinha
   conceitual: existe um modelo; o que distingue Chat, Cowork e Code é o
   **harness** montado em volta dele (o loop, as ferramentas, a montagem de
   contexto, os limites de permissão). O novo **Cap. 5 (O harness)** fundamenta
   isso e passa a sustentar o arco inteiro do livro. Por isso ele entra cedo, na
   Parte I, antes dos capítulos de produto.
3. **Custo baixo no momento certo.** A mudança foi feita quando só os Caps. 1–11
   estavam redigidos e o restante era esqueleto — reorganizar custou pouco.
   Adiar significaria reescrever prosa pronta.

**O que NÃO mudou (e por quê).** O **Claude Science** não virou uma parte
("Pesquisar"). Pesquisar é o guarda-chuva do livro todo, não uma atividade
paralela às outras três; e o Science é vertical por domínio (ciências da vida),
estava em beta e restrito a macOS/Linux. Mantida a decisão original: **apêndice
substantivo + presença em ação nos estudos de caso** (Cap. 20).

O **título** — *Do Chat ao Cowork e Code* — também foi **mantido de propósito**
(decisão de jul/2026), apesar de nomear os produtos e não as atividades. Razão:
título e partes fazem trabalhos diferentes. O título descreve o **arco** de
autonomia (do Chat ao Code, "do… ao…"), que continua intacto; o **subtítulo**
("Colaboração, automação e desenvolvimento com agentes de IA") já carrega o
enquadramento por atividade. Além disso, a **capa** foi desenhada em torno do
título (cada produto na sua tipografia: serifa=humano, sans=ponte, mono=máquina;
degrau de três blocos), e trocá-lo obrigaria a redesenhar capa, favicons e ficha
técnica. Não é esquecimento: se um dia o título for revisto, o custo de capa é a
primeira coisa a pesar.

**Regra de estilo que a mudança destravou.** O `CLAUDE.md` foi emendado para
deixar claro que a arquitetura do agente (harness, orquestração, comportamento
observável) **pode** ser tratada — o que continua vedado é o *interior do
modelo* (como um *transformer* computa). A profundidade "acima do modelo" é o
diferencial do livro, não uma violação da regra.

### 2.2 Split do Cap. 21 em Code + Terminal (05/07/2026)

Cada parte de produto abre apresentando o produto (Parte II → Chat, no Cap. 10; Parte III → Cowork, no Cap. 12), mas a Parte IV abria pelo *terminal*, não pelo Code. O antigo Cap. 21 ("Terminal") acumulava dois assuntos: o primer do terminal (o que é, o *shell*, Mac × Windows — já redigido) e a apresentação do Code como produto (o que faz além do Cowork, casos acadêmicos, a aba Code, panorama de agentes CLI, expectativas — só esqueleto). O próprio esqueleto de `##` denunciava a divisão.

**Decisão do autor:** separar em dois, na ordem **Code → Terminal**. O novo **Cap. 21 Code** (`21-code.qmd`, `{#sec-code}`) abre a Parte IV apresentando o produto, paralelo ao Cap. 12 (Cowork), e recebeu as cinco seções de produto. O **Cap. 22 Terminal** (`22-terminal.qmd`, mantém `{#sec-terminal}`) fica com o primer do terminal, logo antes da Instalação (Cap. 23), onde o leitor de fato usa o terminal.

**Custo baixo.** Como as remissões já são `-@sec-` nativas (conversão de 04/07/2026), renumerar não quebrou nenhuma — só mudaram o `_quarto.yml`, os prefixos `NN-` dos arquivos, `figuras.md` (refs numéricas) e este `notas.md`. Renumeração: Parte IV 22→23…27→28; Parte V 28→29…31→32. Total: **31 → 32 capítulos**. Injeção de prompt passou a 31; O futuro, a 32. O novo `21-code.qmd` ganhou `{#sec-code}` (estava livre; `sec-code-ide` é o do Cap. 27). `sec-terminal` não era citado em lugar nenhum, então a reatribuição foi trivial. Corrigido de passagem o clichê "porta de entrada" no primer do terminal (lista do CLAUDE.md).

**A fazer:** redigir a prosa dos dois capítulos — o Cap. 21 (Code) é a abertura da parte; o Cap. 22 (Terminal) já tem a prosa descritiva e só precisa da seção de desmistificação. Confirmar/encurtar os títulos das seções do Cap. 21 no app.

## 3. Conteúdos específicos a não esquecer

### Origem do nome "Claude" → Cap. 2
Homenagem a **Claude Shannon** (1916–2001), pai da teoria da informação. É a
explicação amplamente atribuída; a Anthropic nunca a transformou em anúncio
formal enfático. **[verificar]** Fontes: `wikipedia_claude_lm`,
`bostonglobe_shannon_2026`.

### Os *spinner verbs* (palavras enquanto "pensa") → caixa "Curiosidade", Cap. 4
Gerúndios bem-humorados no indicador de atividade do Claude Code/Cowork
(*Sautéing…*, *Pondering…*, *Lollygagging…*). ~185 por padrão, em categorias
(*Culinary*, *Cerebral*, *Whimsical*…). Personalizáveis/desligáveis; viraram
culto na comunidade (dicionários). Fontes: `spinner_verbs_dictionary`,
`centricle_spinner_words`.

### Fable 5, Mythos 5 e a ordem executiva → Cap. 2 (menção) + Parte V (caso)
- 09/06/2026: Anthropic lança **Claude Fable 5** e **Claude Mythos 5** (este com
  acesso restrito).
- 02/06/2026: ordem executiva de Trump *"Promoting Advanced Artificial
  Intelligence Innovation and Security"* (classificação de "covered frontier
  models").
- 12/06/2026: diretiva de **controle de exportação** proíbe o uso por quem **não
  é cidadão dos EUA** → na prática, bloqueia o acesso fora dos EUA. Anthropic
  **suspende** os dois modelos.
- Motivo não oficial: suspeita de *jailbreak* no Fable; um concorrente (apontado
  como a Amazon) teria alertado o Dep. de Comércio.
- Até o fim de junho/2026, modelos offline, mesmo após Trump sinalizar alívio
  ao encontrar Dario Amodei no G7 (Évian-les-Bains).
- **01/07/2026: Fable 5 restabelecido globalmente** (controles retirados em
  30/06), com filtro de segurança novo. Fonte oficial verificada:
  `anthropic_redeploying_fable_2026`; Cap. 2 já conta a suspensão e a volta.
- **Tratamento:** factual e equilibrado; tema político e **em curso**.
  **[verificar]** antes de publicar. Fontes: `nbc_fable_2026`,
  `aljazeera_fable_2026`, `conversation_fable_2026`.

### MCP → Cap. 6 (capítulo próprio)
Analogia do **USB-C da IA**: padrão aberto que conecta o Claude a ferramentas
externas. Anatomia: servidor (lado da ferramenta), cliente (Claude), ferramentas
e dados. "Conectores" no Cowork são MCPs. Segurança: conectar = conceder acesso.
Aplicado no Cowork (Cap. 15) e no Code (Cap. 26).

### BibTeX e citação → Caps. 17 e 29
Anatomia do `.bib` (chave de citação, tipos `@article`/`@book`/…). Fluxo:
encontrar → metadados → gerar `.bib` → formatar (`.csl` ABNT/Vancouver via
Quarto) → **verificar**. Cuidado central: **alucinação de citações** (checklist:
o DOI resolve? o periódico existe? o ano confere?). Zotero/Mendeley como origem
das `.bib`: RESOLVIDO — mencionados (ver §6).

### Git e GitHub → Cap. 29 (+ toque leve no Cap. 23)
**Decisão:** concentrar git/GitHub no **Cap. 29** (controle de versão + GitHub
Pages para publicar — o livro é Quarto e pode ir ao GitHub Pages). **Toque leve
no Cap. 23**: git **recomendado**, não obrigatório, na instalação do Code (rede
de segurança — commits para desfazer edições do agente; instalador nativo não
exige git, mas no Windows o Git for Windows ajuda o Bash). Enquadramento
**git-para-supervisão**: o Claude Code roda git por você; o leitor entende para
supervisionar, não decora comandos. Referenciar o **Manual de Git e GitHub** do
autor [@alvarenga_github_manual] no Apêndice D e num boxe "Para aprofundar" no
Cap. 29 — não reescrever git do zero.

### Estrutura de projeto completa (árvore Quarto) → Cap. 29
**Material aprovado pelo autor (04/07/2026)** para "O fluxo: do dado bruto ao
relatório final" e "Estudo de caso: como este livro foi feito": árvore de um
projeto-livro Quarto completo — `_quarto.yml`, `index.qmd`, pré-textuais,
capítulos numerados, apêndices, `data/raw` × `data/processed`, `code/` com
scripts numerados (`01-limpeza`, `02-modelos`), `images/figures` (geradas por
código) × `images/static` (manuais), `references/` + CSL, `_extensions/`,
`.gitignore`, `README.md`. É a versão adulta da árvore mínima do Cap. 16
(as cinco pastas do 16 crescidas). **Dois reparos ao usar:** (a) nomes de
pastas em PT-BR, batendo com o repositório real deste livro (`capitulos/`,
`apendices/` — o estudo de caso deve mostrar a árvore verdadeira, não uma
genérica em inglês); (b) `csl_styles/` fica dentro de `references/`, como no
repositório real. O Cap. 16 já remete ao 29 por "exemplos de árvores mais
completas" — o 29 precisa pagar essa promessa.

### Bases de referência → Cap. 17; estudos de caso Cap. 20
- **PubMed/médicas:** conector dedicado (MCP) — metadados estruturados.
- **Google Scholar/genérica:** web + pesquisa profunda; ancorar no DOI.
- **Jurídicas:** sites oficiais; cuidado com alucinação de nº de processo/lei;
  ABNT tem regras próprias p/ legislação e jurisprudência.
- **Arquivos históricos:** citar acervo/fundo/caixa/data; Claude organiza e
  normaliza, não "descobre".

### Markdown → Cap. 7 (e possível Apêndice E)
Substrato do ecossistema: respostas do Claude, `CLAUDE.md`, skills (`SKILL.md`),
artefatos e o próprio livro (Quarto = Markdown). Ensinar o essencial e a
conversão para Word/PDF/HTML.

### Configurações → Cap. 9
Tela de Configurações (abas: Geral, Conta, Privacidade, Cobrança, Uso,
Capacidades, Conectores, Claude Code, Cowork, Claude in Chrome). Instruções
personalizadas (valem em conversas e no Cowork), Perfil, Memória, Preferências
(Aparência, "Fonte do chat: Anthropic Serif").

### CLAUDE.md → prévia no Cap. 9; tratamento completo no Cap. 24 (Code)
**Verificado** ([doc de memória](https://code.claude.com/docs/en/memory)): o
`CLAUDE.md` (arquivo de instruções persistentes, lido a cada sessão) vale no
**Cowork e no Code**, não só no Code. No Chat não há arquivo — o equivalente são
instruções personalizadas + Projetos. O Cowork tem ainda uma *auto-memória*
(`memory.md`), que é a "Memória" do Cap. 9. **Decisão:** prévia curta no Cap. 9
(dentro do eixo contexto persistente: as instruções personalizadas têm uma
versão em arquivo, o `CLAUDE.md`, para Cowork e Code), com remissão ao Cap. 24,
que mantém o tratamento completo (configuração, `settings.json`, hierarquia).
Exemplo vivo: o `CLAUDE.md` deste livro (Cap. 29). **Fonte para o Cap. 24:**
guia oficial de boas práticas de `CLAUDE.md` [@anthropic_claude_md_2025]
(documentar arquitetura/fluxos, comando `/init`, manter conciso, conectar
ferramentas).

### IDEs → Cap. 27
- **Positron** (Posit): IDE de ciência de dados, ótimo p/ R/Python/**Quarto**.
  Claude Code roda no terminal integrado; **sem extensão oficial no marketplace
  ainda** (só pedido aberto). Tem "Posit Assistant" com Claude via chave (BYOK).
- **Cursor:** editor com IA, base VS Code; roda Claude Code no terminal.
- **Antigravity** (Google): IDE "agent-first"; suporta **modelos Claude**
  (Opus 4.8, Sonnet 4.6) com chave Anthropic; harness próprio (≠ Claude Code);
  virou app standalone (não mais fork do VS Code); Agent Teams e tarefas
  agendadas. **[verificar]**

### Modos de permissão → Caps. 8 e 24
Solicitar permissões · Aceitar edições · Modo de planejamento · Modo automático
· Ignorar permissões. Escala de autonomia/risco.

### O "pontinho azul" → Cap. 12 (apresenta) + Cap. 19 (Programado/Despacho)
Indicador de **atividade não vista** na lista Recentes (como "não lido"): avisa
que a tarefa avançou/espera você. Some ao abrir. Ícones: lista=tarefa,
balão=conversa. Glossário: "indicador de atividade".

### Claude Science → Apêndice G (novo; decisão jul/2026)
**Verificado** no anúncio oficial (Anthropic newsroom, **30/06/2026**, "Claude
Science: an AI workbench for scientists"). É um **aplicativo de pesquisa em
beta**, vertical para **ciências da vida computacionais** (genômica, célula
única, proteômica, biologia estrutural, quimioinformática) — **não** um degrau
do arco Chat→Cowork→Code, e sim um produto especializado por domínio.
- **Decisão editorial:** não vira capítulo do **arco principal** porque não é um
  degrau da escala Chat→Cowork→Code (é um vertical por domínio), e por limites de
  acesso — **beta**, só **macOS/Linux**, planos Pro/Max/Team/Enterprise. **Não**
  porque o leitor não usaria: para pesquisadores de **ciências da vida e
  biomédicas** (público nomeado no livro) é diretamente útil, e o produto se
  vende como algo que habilita o **biólogo não-computacional** — encaixa na tese
  "sem que você precise programar" dentro da área. Por isso o tratamento é um
  **apêndice substantivo** + presença **em ação no Cap. 20** (Medicina/saúde e
  Ciências da vida), não um rodapé; também referenciado nos Caps. **3**
  (ecossistema) e **29** (pesquisa reproduzível). Retrofit **depois do Cap. 11**.
  *(Em aberto: se o autor quiser, dá para promover a um capítulo curto e
  opcional, ou a uma seção forte no Cap. 20 — ver conversa.)*
- **Fatos citáveis (do anúncio):** artefatos reprodutíveis ("cada artefato vem
  com seu histórico": código + ambiente + conversa que o geraram); **agente
  revisor** que confere citações e cálculos; gestão de *compute* (laptop,
  cluster HPC, GPUs sob demanda, Modal, SSH); kernels Python/R persistentes;
  **60+ skills e conectores**; bases UniProt, PDB, Ensembl, Reactome, ClinVar,
  ChEMBL, GEO, PubMed; integração NVIDIA BioNeMo (Evo 2, Boltz-2, OpenFold3).
- **Disponibilidade:** beta para Pro, Max, Team e Enterprise; **macOS e Linux**;
  plano Team para labs acadêmicos. Parceiros citados: Manifold Bio, Allen
  Institute, UCSF Brain Tumor Center, NVIDIA, Modal.
- **A fazer:** entrada no `.bib` (`anthropic_claude_science_2026`); reconferir
  detalhes antes de publicar (é **beta**, muda) e a relação Science × Code ×
  Cowork; decidir se o apêndice ganha uma captura de tela.

## 4. Terminologia da interface (PT-BR, do print)

Abas **Home / Code**; **Nova tarefa**; **Projetos**; **Artefatos**;
**Programado**; **Despacho** (Beta); **Personalizar**; **Fixado**; **Recentes**;
alternador **Chat ↔ Cowork**; seletor de **modelo** (Opus 4.8) e **esforço**
(Alto, "Mais rápido ↔ Mais inteligente"); **Uso do plano** (Limite de 5 horas,
Semanal, Apenas Sonnet, Créditos de uso); menu **+** (Adicionar arquivos,
Adicionar pasta, Importar issue do GitHub, Comandos de barra, Conectores,
Plugins); **Modelos** (Opus 4.8, Sonnet 4.6, Haiku 4.5, Fable 5, Modo rápido);
chips **Local** / pasta; **Solicitar permissões**.

## 5. Páginas de frente/trás (já criadas)

- **Prefácio** → **`prefacio.qmd`**: RESERVADO para texto de um **colega
  convidado** (decisão jul/2026); hoje só placeholder com TODO.
- **Apresentação** → **`apresentacao.qmd`** (voz do autor): recebeu todo o
  conteúdo do ex-prefácio — abertura ("Durante décadas…"), A quem se destina,
  Conteúdo e limites, Como o livro está organizado, Como ler, Convenções e o
  callout de atualidade. O `index.qmd` é página de abertura curta (home do
  HTML) — texto provisório, autor vai ajustar. Ordem em `chapters`: index →
  ficha-tecnica → agradecimentos → **prefacio** (colega) → **apresentacao**
  (autor) → Parte I.
- **Agradecimentos** → `agradecimentos.qmd` (esqueleto p/ preencher).
- **Ficha técnica** (página de direitos) → `ficha-tecnica.qmd` (esqueleto):
  dados da obra/ISBN, licença, tipografia, produção (Quarto + transparência
  sobre uso do Claude), créditos de imagens, **aviso de isenção** (obra
  independente, sem vínculo com a Anthropic). Posição: **no início**, logo
  após o `index.qmd` e antes dos Agradecimentos, como o verso da folha de
  rosto num impresso (não é apêndice; o Quarto só tem `chapters` e
  `appendices`, então a matéria de abertura vai no começo de `chapters`).

## 6. Decisões em aberto

- Tipografia/fontes do livro.
- Apêndice E (folha de referência de Markdown): incluir?
- Zotero/Mendeley no Cap. 17: **RESOLVIDO (04/07/2026)** — o autor os mencionou
  na introdução (Zotero, Mendeley e JabRef; datas com fonte `ivey2018citation`);
  a seção "Importar de gerenciadores de referência (Zotero/Mendeley)" os trata.
- Data/edição de referência a fixar no prefácio.
- *vibe coding*: **RESOLVIDO** — boxe "Para aprofundar" no Cap. 1, com
  @karpathy2025vibe e @willison2025vibe.

## 7. Tópicos da Parte I (aprovados, registro técnico)

- **Cap. 1:** definição de agente vs. chatbot · componentes de um sistema
  agêntico · resposta vs. execução · aplicações acadêmicas · capacidades e
  limitações · organização do livro.
- **Cap. 2:** fundação da Anthropic e segurança em IA · o que é um modelo de
  linguagem · famílias Claude (Opus/Sonnet/Haiku) · IA Constitucional ·
  cronologia dos produtos · nome e identidade (Shannon).
- **Cap. 3:** visão geral dos três produtos · Chat · Cowork · Code · critérios
  de escolha · relação modelos/planos/produtos.
- **Cap. 4:** ciclo de execução · janela de contexto · tokens · ferramentas ·
  limitações (alucinação, corte, viés) · supervisão humana · *(caixa: spinner
  verbs)*.
- **Cap. 6:** limitações de acesso a dados · definição e padrão aberto ·
  arquitetura (servidor/cliente/ferramentas/dados) · catálogo · MCP no Cowork ×
  Code · segurança.
- **Cap. 7:** por que Markdown · sintaxe básica · tabelas/citações/código ·
  conversão · usos no Claude · relação com Quarto.
- **Cap. 8 (Setup):** conta e plano · limites/créditos · instalação (visão
  geral) · privacidade · responsabilidade · modos de permissão.
- **Cap. 9 (Personalização):** tela de Configurações · perfil ·
  instruções personalizadas · projetos · memória · preferências.

> Tópicos das Partes II–V: **definidos** e já gravados nas seções (`##`) dos
> respectivos `.qmd` em `capitulos/`. Falta redigir a prosa de cada capítulo.

## 8. Status atual e handoff (para continuar em nova sessão)

**Pronto:** esqueleto completo (29 caps + apêndices A–F, `_quarto.yml` só HTML,
`styles.scss`, capa e favicon em `images/capa-favicon/`). Prefácio (`index.qmd`)
redigido e revisado. **Caps. 1 a 7 redigidos e revisados**; **Caps. 8 (Setup) e 8 (Personalização)
redigidos** nesta sessão (a revisar pelo autor).
Bibliografia com ~57 entradas (30 importadas do curso, **NÃO VERIFICADAS**; o
resto verificado nesta etapa). Diagramas em `images/diagramas/`. PDF desativado
(reativar: descomentar bloco no `_quarto.yml` + `quarto install tinytex`).

**Cap. 6 × Cap. 26 — remissão "servidor próprio" (08/07/2026):** o Cap. 26
(`26-mcp-e-dados.qmd:9`) dizia "o caminho que o Cap. 6 chamou de servidor
próprio", mas o Cap. 6 nunca usava o termo nem traçava a distinção **conector
pronto no catálogo × servidor sob medida** — remissão falsa. Corrigido no lado
do Cap. 6 (não mover para o 26), coerente com a tese "conceito mora uma vez na
Parte I; capítulo de produto remete e aplica": a seção "Catálogo e ecossistema"
(`06-mcp.qmd:29`) ganhou duas frases que nomeiam o **servidor próprio** (escrito
sob medida quando não há conector pronto) e apontam o "como" para o Cap. 26
(`Cap. -@sec-mcp-data`). Altitude conceitual no 6; o worked example (OAuth, Node,
`claude mcp add`) segue inteiro no 26. Frasagem respeita o "sem programar": o
usuário não programa, o Claude escreve o servidor. Nota: o Cap. 6 passou a ter
duas remissões a `sec-mcp-data` (linhas 29 e 33) — pontos distintos (registrar
servidor qualquer × escrever um sob medida), mantidas.

**Cap. 26 — exemplo do servidor Google Forms atualizado com fatos verificados
(08/07/2026):** o servidor MCP real do exemplo (em `~/Developer/Outros/Google_MCP`,
repo `claude-book/mcp-server-google-forms`) passou por reorganização + revisão
`/code-review high` numa **sessão paralela do Claude Code** (v0.3.1). Fonte da
verdade do código: `docs/revisao-de-codigo.md` do repo (tabela de status +
histórico). Três correções factuais no `26-mcp-e-dados.qmd` (com `writing-style`):
(a) removida a falsa "chave **duradoura**" (linha 13) — o *refresh token* só é
durável em produção; (b) lista de ferramentas atualizada para as **oito** reais
(entraram publicar/`set_publish` e ver estrutura/`get_form`); (c) reescrito o
parágrafo dos "limites": app OAuth nasce em **modo de teste**, onde o token
**expira em 7 dias**; a correção é **publicar em produção** (sem verificação do
Google, atravessando uma vez a tela de "app não verificado"), onde o token não
expira. Regra dos formulários **não publicados desde 30/06/2026**: agora
**verificada** (código + doc oficial + teste ao vivo pela sessão paralela) — TODO
removido; ligada à ferramenta de publicação. **Em aberto no Cap. 26:** a edição do
autor no §9 tirou o cross-ref `(Cap. -@sec-mcp)` de "servidor próprio" e deixou
"google forms" em minúscula — decisão do autor; as seções 24–30 seguem por
redigir. **Não** mexer no repo MCP (regra de convívio: mudança no código atualiza
`docs/revisao-de-codigo.md` no mesmo commit).

**Caps. 26 e 27 REDIGIDOS (09/07/2026), com `writing-style` — aguardam revisão
do autor.** Fatos verificados (agente `claude-code-guide` na doc oficial + buscas
na web); cross-refs conferidos contra os IDs reais de `capitulos/`.

- **Cap. 26 (`26-mcp-e-dados.qmd`):** escritas a intro e cinco seções em volta do
  exemplo do Forms (que já estava pronto): "MCP no Code" (escopos **local /
  project / user** do `claude mcp add`; `.mcp.json` × `~/.claude.json`; contraste
  com os Conectores gráficos do Cowork), "Dados no Code" (retitulada de "Trabalhar
  com dados: planilhas, CSV e bases" — dois-pontos proibido; o Code como analista
  com o ambiente inteiro; escala × Cowork; reprodutibilidade → Cap. 29), "Análise
  e visualização" (pergunta→resultado; método é de quem assina; `/dataviz`),
  "Conectores úteis para pesquisa" (PUBMED/Drive/Postgres; catálogo cresce;
  conferir a origem) e "Segurança ao conectar no Code" (conectar = conceder
  acesso; servidor de terceiros = rodar código alheio; **tríade letal** → Cap. 31;
  o que o agente lê vai para o modelo → anonimizar, Cap. 30).
- **Cap. 27 (`27-code-no-ide.qmd`):** redigido inteiro. Títulos com dois-pontos
  encurtados: "Positron/Cursor/Antigravity" e "Comparação: …" → "Terminal-first e
  agent-first". Espinha (mostrada, não declarada — regra do CLAUDE.md): **mesma
  máquina, superfícies diferentes**. Fatos: extensões **oficiais** de VS Code e
  JetBrains = mesmo harness/CLI por baixo; **Positron** = Claude Code no terminal
  integrado, sem extensão oficial no catálogo (só feature request) + o *Positron
  Assistant* próprio (Claude via chave); **Cursor** = extensão/terminal + agente
  próprio, histórico compartilhado (`claude --resume`); **Antigravity** =
  *agent-first*, harness próprio, aceita Claude via chave de API.
- **Notas corrigidas na verificação (§3, IDEs):** Antigravity agora pluga **Opus
  4.8/Sonnet 4.6** (não "4.6") e virou **app standalone**, não mais fork do VS
  Code. Atualizar o §3 se for reusar.
- **TODOs deixados no Cap. 27** (voláteis): status da extensão do Positron;
  detalhes do Antigravity. **Figuras a fazer** (já em `figuras.md`):
  `code-positron-terminal.png`, `code-cursor.png`, `code-antigravity.png`.

**Reestruturação da Parte IV + renome da Parte V (09/07/2026).** Decisão do autor
após conversa: o Cap. 26 tratava MCP **e** dados, e as seções de dados partiam o
arco do MCP ao meio. Separado:
- **26 MCP e conectores** (`26-mcp-e-conectores.qmd`, ID **`sec-mcp-code`**, era
  `sec-mcp-data`): só MCP/conectores (intro, MCP no Code, servidor próprio,
  conectores úteis, segurança). Exemplo do Forms intacto.
- **28 Dados e análise** *(novo)* (`28-dados-e-analise.qmd`, **`sec-code-data`**):
  recebeu "Dados no Code" e "Análise e visualização" (do 26) + "Documentos
  executáveis (Quarto)" (do antigo 28). **Seção Quarto REDIGIDA (09/07/2026,
  writing-style):** 3 parágrafos — dos arquivos soltos das seções 1–2 ao
  documento único; a célula executável remetida ao Cap. 7 (não reexplicada);
  este livro como exemplo; ponte à reprodutibilidade (Cap. 29). Refs conferidas
  (`sec-markdown`, `sec-research`). **Em aberto:** a seção "Dados no Code" ecoa o
  título do capítulo — decisão do autor sobre retítulo (comentário no `.qmd`).
- **29 Pesquisa reproduzível** (era 28; `29-pesquisa.qmd`, mantém
  `sec-research`): perdeu a seção "Quarto" (foi p/ o 28). **Git e `.bib`/`.csl`
  ficam como seções** (→ Manual de Git do autor e Cap. 17), NÃO capítulos —
  decidido contra os caps. separados de git/bibtex que se cogitou.
- **Parte V renumerada +1** (29→30 … 32→33), **pasta `p5-pratica-responsavel` →
  `p5-pratica`**, título da parte encurtado para **"Prática"**. **32 → 33 caps.**
- Varredura: `sec-mcp-data` → `sec-mcp-code` (2 refs no Cap. 6). `_quarto.yml`,
  `figuras.md` (28→29, 30→31) e `CLAUDE.md` (pasta p5) atualizados. Remissões são
  `-@sec-` nativas → renumerar não quebrou nada; conferido (todos os caminhos
  existem, zero remissão órfã). **Etapa 2:** prosa da seção Quarto do 28
  **REDIGIDA (09/07/2026)** — ver bullet do Cap. 28 acima. **A fazer:** redigir a
  prosa do 29 (esqueleto: reprodutibilidade, fluxo, git, bib/csl, estudo de caso)
  e a decisão de retítulo da seção "Dados no Code".

**Cap. 23 (Instalação) REDIGIDO (09/07/2026), com `writing-style` — aguarda
revisão do autor.** Fatos verificados na doc oficial (agente `claude-code-guide`:
`quickstart`, `setup`, `authentication`, `commands`, `permissions`). **Duas
rodadas:** (1) versão enxuta, que delegava o passo a passo por SO ao Apêndice A;
(2) **decisão do autor: o leitor deve conseguir instalar lendo só o capítulo** →
reescrito autossuficiente, fundindo a densidade prática de um rascunho paralelo do
GPT com o estilo do livro. Do feedback do GPT foram acatados: preservar a
**supervisão humana** (cortada a frase "quem opera o terminal passa a ser o
Claude"); requisitos explícitos + "não precisa de placa de vídeo" (o modelo roda
nos servidores); **tirar "Opus 4.8" do corpo** (envelhece → "o modelo em uso");
**hedge no plano** (assinatura inclui; Console/API cobram à parte); dar destaque a
`/init`, Shift+Tab, `/diff`, `--continue`/`--resume`. **Rejeitado:** o over-hedge
"em geral, mantém histórico local" (é documentado → afirmação direta); e a prosa
do rascunho do GPT (que reincidia nos vícios: abertura-embrulho, "você", títulos
com "?", "Conclusão" com resumo/aforismo, ~18 seções). **Oito seções:** Requisitos
· Instalação (macOS/Windows/Linux em `###`, + Homebrew/WinGet/WSL/apt em uma linha
cada, Git for Windows → Bash, callout "Na prática" com `--version`/`doctor`) · A
primeira sessão (login OAuth + `/login` + tela de boas-vindas + loop do Cap. 4 +
comandos de barra → Cap. 25) · A primeira tarefa (`/init` → Cap. 24; pedidos de
leitura primeiro; callout "comece por tarefas reversíveis") · Aprovar e revisar
(menu de permissão; Shift+Tab = escala do Cap. 8; `/diff`; git desfaz; regras
finas → Cap. 25) · Encerrar e retomar · Quando algo não funciona (3 tropeços +
remissão ao Apêndice A). Remissões conferidas no render (zero órfã). **Fronteira
Cap. × Apêndice A:** o capítulo cobre o caminho normal completo; o Apêndice A fica
com a cauda longa (telas passo a passo, casos raros de troubleshooting) — Apêndice
A ainda é stub, a redigir. **Figura usada:** `permissao-explicita.png`
(`@fig-permissao-explicita`); se o autor preferir, cabe no Cap. 25. **Imagens
novas** `claude-code-ide-terminal.png` e `claude-code-ide-extensao.png` são do
**Cap. 27** (mapeadas em `figuras.md`). **TODO de figura:**
`code-terminal-boas-vindas.png` (tela do `claude` num terminal limpo, fora de
editor).

**Cap. 23 — passe de revisão + reenquadramento da abertura (09/07/2026).** Depois
da redação, o autor pediu ajustes finos (aplicados um a um, sem reescrever):
supervisão preservada (cortada "quem opera o terminal passa a ser o Claude");
hedge no plano (assinatura inclui; Console/API/corporativo podem cobrar por uso);
"Linux" → "distribuições Linux compatíveis"; `apt`/`dnf`/`apk` com "conforme a
distribuição e a documentação vigente"; cautela no `/init` ("revise o conteúdo
antes de aceitá-lo como instrução permanente"); `fig-alt` encurtado; "A conversa
fica guardada" → "Em geral, o histórico da sessão fica disponível" (autor pediu o
hedge, mesmo sendo documentado — o "em geral" contraria a skill, fica o registro);
padronização Claude Code (ferramenta) / Claude (agente) / Code (só quando o
referente é claro). **Abertura reescrita (decisão do autor: o leitor deve saber
que há várias vias):** o §1 agora abre pelas **três formas de usar/instalar** —
app de desktop (traz o Code embutido, sem instalação à parte), extensão do VS Code
(idem, pelo marketplace) e o **terminal** (instalar `claude`, a via deste
capítulo). **Fatos verificados** (agente `claude-code-guide`, doc oficial
`desktop-quickstart`/`vs-code`/`jetbrains`): app de desktop e extensão do **VS
Code embutem o CLI** (dispensam a instalação no terminal); **JetBrains exige** o
CLI avulso; navegador (`claude.ai/code`) = nuvem; app de desktop Local = na
máquina. **DECISÃO EDITORIAL (autor, 09/07/2026): NÃO mencionar o JetBrains em
lugar nenhum do livro.** Por isso a abertura do Cap. 23 saiu de "plugins como o do
JetBrains" para só "o terminal integrado de um editor". **Afeta o Cap. 27**
(`27-code-no-ide.qmd`): a nota §8 dizia "extensões oficiais de VS Code e JetBrains
= mesmo harness/CLI por baixo" — ao revisar o 27, **remover o JetBrains** e manter
só VS Code (que embute o CLI) e o terminal integrado (Positron/Cursor). O `.bib` e
`figuras.md` não citam JetBrains; nada a limpar além do Cap. 27.

**Cross-references e git (04/07/2026):** as remissões manuais a capítulos
viraram cross-references nativas do Quarto. Todos os 31 caps. e 6 apêndices têm
identificador no título: **slug curto em inglês** com prefixo `sec-` (ex.:
`sec-harness`, `sec-mcp-data`, `sec-glossary`); colisão Cap. 22/Apêndice A
resolvida com `sec-install` / `sec-install-os`. IDs antigos renomeados:
`sec-como-trabalha`→`sec-how-agents-work`, `sec-o-harness`→`sec-harness`,
`sec-injecao`→`sec-prompt-injection` (`sec-spinner-verbs` mantido). **Estilo
fixado para remissões novas:** manter o texto "Cap."/"Capítulo"/"Apêndice" e
usar a forma **sem prefixo** `-@sec-x` só no número — ex.: `(Cap. -@sec-mcp)`
renderiza "(Cap. 6)". Não usar `@sec-x` puro, que renderizaria "Capítulo 6"
por extenso e quebraria a convenção tipográfica do livro. 134 remissões
convertidas e conferidas contra o render (sem warnings; número renderizado =
número original em todas). **Ficam manuais:** menções a "Parte I–V" (partes
são strings no `_quarto.yml`, não recebem ID — atenção ao reordenar partes) e
os números citados em comentários `<!-- TODO -->`. **Git:** repositório
iniciado nesta data como rede de segurança (`73facd8` estado pré-conversão,
`01c3396` conversão); `_book/` e `.quarto/` fora do versionamento. Regra
prática daqui em diante: capítulo novo ganha `{#sec-...}` no título, e toda
remissão nova usa `Cap. -@sec-x`.

**Reorganização (esta sessão):** capítulos movidos para subpastas por parte
(`capitulos/pN-.../`), figuras com caminho a partir da raiz (`/images/...`).
**Setup e Personalização trocados de ordem:** Setup vem antes da
personalização. (Numeração atual, após a reestruturação de jul/2026: **8 —
Setup**, `08-setup.qmd`, e **9 — Personalização**, `09-personalizacao.qmd`.)

**Cap. 16 reformulado e REDIGIDO (04/07/2026):** "Documentos acadêmicos" virou
**"Análise de dados"** (`16-analise-de-dados.qmd`, `sec-data-analysis`) —
decisão e estrutura de 7 seções no **§13**. Prosa redigida com a skill
writing-style; **aguarda revisão do autor**. Refs novas verificadas
(`noble2009organizing`, `wilson2017good` — DOI conferido na PLOS). Ajustados
`_quarto.yml`, remissão do Cap. 11, `figuras.md` e CLAUDE.md (Zotero → Cap. 17).
TODOs de interface no arquivo: fluxo do `/skill-creator` e comandos do grupo
Data; captura `cowork-analise-dados-tarefa.png` a fazer.

**Cap. 17 — introdução com referências verificadas (04/07/2026):** o autor
redigiu a introdução; todas as afirmações históricas foram conferidas com
dupla verificação e receberam fonte — 5 entradas novas no `.bib` (seção
"Historia da referencia bibliografica"): `avram1975marc` (MARC/Library of
Congress; ERIC + WorldCat), `lesk1978refer` (refer/troff, Bell Labs 1978),
`patashnik2003bibtex` (TUGboat 24(1):25–30; PDF integral lido — BibTeX 0.98
em mar/1985, projetado para o LaTeX de Lamport, .bib modelado nos registros
do Scribe), `fenner2014reference` (Opening Science, Springer 2014, DOI no
Crossref) e `ivey2018citation` (JMLA 2018, DOI + PMC: EndNote 1988, Zotero
2006, Mendeley 2008). As datas do texto do autor conferiram todas. Com
aprovação do autor: typo "boibtex" corrigido e frase nova sobre o Scribe
(elo direto do formato .bib, cf. Patashnik). Duplicata `wilson2017good`
removida do `.bib`. Render conferido: 6 citações resolvem, sem órfãs.
**Seção CSL verificada (04/07/2026, na sequência):** o autor enxugou a seção
(saíram D'Arcus/Kornblith e o CSL 1.0/2010) e unificou os títulos duplicados;
as afirmações restantes foram todas confirmadas em páginas oficiais e
receberam fonte — `csl_project` (citationstyles.org: definição, >10 mil
estilos, adotantes), `csl_history` (citationstyles.org/about: "Zotero was the
first program to adopt CSL"; "their roots have always been firmly
intertwined"), `zotero_styles_docs` (docs do Zotero: >10 mil estilos, todos em
CSL) e `quarto_citations` (Quarto usa Pandoc; campos `bibliography:`/`csl:`;
padrão Chicago autor-data). **Nenhum erro factual na seção**; única correção
(aprovada): concordância "associada"→"associado". Render conferido: 9
citações resolvem. **PDFs das fontes do Cap. 17 em `_source/`** (padrão
autor-ano-tema, todos abertos e conferidos):
`avram-1975-marc-history-implications.pdf` (scan ERIC ED127954),
`lesk-1978-inverted-indexes-refer.pdf` (recomposição groff/1997 dos fontes do
manual UNIX v7, mirror de W. Schneider; o paper do Lesk começa na p. 5,
precedido do memo-companheiro "Updating Publication Lists"),
`patashnik-2003-bibtex-yesterday-today-tomorrow.pdf` (TUGboat),
`fenner-2014-reference-management.pdf` (capítulo OA, Springer) e
`ivey-2018-choosing-citation-management-tool.pdf` (via Europe PMC; as três
datas — EndNote 1988, Zotero 2006, Mendeley 2008 — visíveis na p. 399).
As fontes CSL são páginas web (sem PDF).

**Próximo passo (atualizado 03/07/2026):** **Cap. 13 REDIGIDO** (estrutura em
§12) e passado pela verificação em 3 lentes — estilo, exatidão, leitor — com
~20 correções aplicadas; **aguarda revisão do autor**. Na verificação, a tabela
antes/depois trocou Buckhout (Scientific American) por **Loftus & Palmer 1974**
(J. Verbal Learning and Verbal Behavior, Elsevier), porque `sdarticle.pdf` é
nome de download do ScienceDirect e não poderia conter um artigo da Scientific
American. Depois da revisão: rodar a tarefa real no Cowork (gera as capturas
das figs. da lista de etapas e do pedido de permissão e resolve os TODOs de
interface dos Caps. 12 e 13); em seguida, Cap. 14 (Skills) ou retrofit do
Claude Science.
Estado: Caps. 1–10 redigidos e revisados (inclusive o passe de voz — ver
"Feito em 02/07/2026"); **Cap. 12 (Cowork) redigido e REVISADO pelo autor**
(estrutura em §11; 5 `TODO: verificar` de interface permanecem no arquivo, a
resolver com o app aberto). Pendências gerais: retrofit do **Claude Science**
(§3 — apêndice G + menções nos Caps. 3, 19, 26); "arco" na legenda da figura
dos Caps. 1/3; typo "do usuário(autor)" no Cap. 11, linha 11 (falta espaço).
**Imperativos: RESOLVIDO** — permitidos (ver §12 e CLAUDE.md).

**Cap. 10 (Prompt) — redigido nesta sessão:** Parte II mantida em **2
capítulos** (Chat enxuto). Títulos encurtados: **Prompt** (era "Conversas
que funcionam (prompting)") e **O Chat na prática** (era "O Chat no
trabalho intelectual"); numeração atual: **10 — Chat e Prompt**
(`10-prompt.qmd`) e **11 — O Chat na prática** (`11-chat-na-pratica.qmd`).
**Título atual: "Chat e Prompt"** (decisão do autor).
Roteiro: **O Chat** (abertura histórica: datas do ChatGPT 30/11/2022, Claude
mar/2023 c/ acesso amplo jul/2023, Bard→Gemini 2023; chat = como os LLMs
chegaram ao público; def. de *prompt*; origem da engenharia de prompt no GPT-3
de 2020, *antes* dos produtos de chat — fontes primárias novas
`openai2022chatgpt`, `anthropic2023claude`, `google2023bard`) →
Anatomia de um bom prompt (5 componentes, ancorado em
`anatomia-de-um-bom-prompt.svg`) → Contexto e especificidade → Exemplos e
formato → Raciocínio passo a passo → Iteração e refinamento → Erros comuns.
Foco no Chat com **remissão leve** ao Cowork/Code; exemplos generalizados (todas
as áreas), não médico-only como no curso. **Referências conferidas nesta
sessão** (busca na web + arXiv; marcadores `TODO: verificar` removidos):
`brown2020language` (few-shot, NeurIPS 2020), `wei2022chain` +
`kojima2022large` (chain-of-thought, NeurIPS 2022) — **mantida a forma
publicada nos anais** (mais forte que o preprint arXiv). No boxe "Para
aprofundar": `schulhoff2025promptreport` (The Prompt Report; key
`schulhoff2025prompt`→`schulhoff2025promptreport`, `@misc` arXiv com lista
completa de 31 autores, ano 2025 = versão v6) + `liu2023pretrain` (ACM Computing
Surveys, com DOI — **substituiu** `white2023prompt`, que ficou no .bib mas sem
uso). Callouts: "Na prática" (anexar material), "Atenção" (verificação + dados
sensíveis), "Para aprofundar".

**PDFs das fontes em `_source/`:** os artigos de prompting foram **lidos e
conferidos contra o texto** (não inventados) e renomeados para o padrão
**autor-ano-tema** (`brown-2020-few-shot-learners.pdf`,
`wei-2022-chain-of-thought.pdf`, `kojima-2022-zero-shot-reasoners.pdf`,
`white-2023-prompt-pattern-catalog.pdf`, `schulhoff-2025-prompt-report.pdf`,
`liu-2023-pre-train-prompt-predict.pdf`).
Confirmado: Wei/Kojima = NeurIPS **2022**; Kojima traz literalmente "Let's think
step by step". **Liu et al. 2023 conferida no PDF:** título corrigido para
"Pre-**train**…", revista usa **Article 195** (ACM Comput. Surv. 55(9), 2023,
DOI 10.1145/3560815); `.bib` ajustado (articleno/numpages + `pages=195` p/ o
Nature CSL renderizar "55, 195 (2023)"). **Todas as refs do Cap. 10 conferidas
contra PDF.** (PDFs de escrita — Zinsser/Friedman/Bates — seguem com nomes
originais; padronizar se o autor quiser.)

**CSL:** padrão do livro agora é **Nature** (`nature.csl`) — CLAUDE.md
atualizado (antes dizia Vancouver); alinhado ao `_quarto.yml`.

**A fazer (panorama):** redigir a prosa dos caps. 9–29 (hoje só têm título +
seções `##`) e preencher apêndices A–E. Em cada capítulo: encurtar os `##`,
generalizar exemplos para todas as áreas, marcar `<!-- TODO: verificar -->` no
que vier do curso.

**Feito em 02/07/2026 (voz do livro):** removido o endereçamento direto ao
leitor ("você" + possessivos de 2ª pessoa) em TODO o livro — apresentação e
Caps. 1–10, 24, 25, apêndice F (~100 correções, aprovadas item a item pelo
autor em `revisao-voce.md`, mantido na raiz como registro). Falas de exemplo
(prompts) preservadas. Regra fixada no CLAUDE.md. **Imperativos: RESOLVIDO
(jul/2026)** — permitidos em trechos práticos (ver §12; CLAUDE.md atualizado).
**Em aberto:** "a decisão fica com o usuário" (Cap. 6) segue candidata a corte
por repetição.

**Feito em 01/07/2026 (revisão editorial Caps. 1–9):**
- **Cap. 10:** história da palavra *prompt* inserida na abertura (etimologia:
  latim *promptus*, ponto de teatro, *command prompt*; era da completação →
  instruções). Refs novas verificadas: `liu2023pretrain` (já havia),
  `ouyang2022training` (InstructGPT). Frase de abertura reescrita.
- **Revisão ponto a ponto dos Caps. 1–9** (relatório aprovado item a item pelo
  autor): Cap. 1 — componentes do agente unificados (ferramentas/autonomia/
  loop), metáfora "mãos" removida, portões de aprovação condicionados aos modos
  de permissão, exemplo neutro de notas de turma, callout "*Vibe coding*";
  Cap. 2 — IA Constitucional datada de 2022 (`bai2022constitutional`, nova),
  duplicata "Introducing Claude" unificada em `anthropic_introducing_claude_2023`,
  suspensão + volta do Fable 5 (`anthropic_redeploying_fable_2026`, nova);
  Cap. 3 — remissões corrigidas (esforço → Cap. 8), "só conversa" ajustado,
  tabela com Code no navegador; Cap. 4 — "quase duzentos" spinner verbs, frase
  "janela vazia a cada conversa" (sustenta remissão do Cap. 9), ***tokens*** sem
  parêntese redundante; Cap. 6 — molduras cortadas, abertura sem "suas coisas";
  Cap. 7 — .docx = pacote compactado, Sibyllenbuch verificado (fragmento,
  Museu Gutenberg), `[@chave]` herdado do Pandoc, tabela renderizada adicionada;
  Cap. 8 — sexto modo do terminal verificado na doc oficial (nega o que não foi
  liberado), parágrafos fundidos, seletor modelo/esforço documentado, Code no
  navegador (nuvem) com ressalva; bordões repetidos ("aprovar sem olhar",
  "parte do método") reduzidos a uma ocorrência cada. Decisões de manter:
  frase-resumo do Cap. 1 (linha 13), tomadas/equipamento do Cap. 6, abertura do
  Cap. 9.
- **Bibliografia:** renomeada e movida para `references/references.bib`
  (`_quarto.yml`, CLAUDE.md, notas e Cap. 31 atualizados; render conferido).
  Varredura de duplicatas: só o par falso-positivo `allaire2022quarto` ×
  `quarto_site` (software × site oficial) — **mantidos ambos**, por decisão.

**Feito nesta sessão (jun/2026):**
- **Cap. 6 (MCP):** seção "Ferramentas nativas e MCP" movida para o início
  (distinção nativo × MCP antes do resto); história/adoção do MCP por OpenAI,
  Google e Microsoft com **fontes oficiais** (`openai_mcp_2025`,
  `google_mcp_2025`, `microsoft_mcp_2025`). `wikipedia_mcp` rebaixada a panorama.
  Seção redundante "O que o Claude não vê" removida.
- **Cap. 7 (Markdown):** redigido do zero, adaptando o curso e generalizando.
  Roteiro: O que é Markdown → A sintaxe essencial → Tabelas, código e citações →
  Markdown e o Quarto → Conversão → Código que roda → Markdown no Claude.
  Inclui história (Gruber/Swartz, `gruber2004markdown`), callout do WhatsApp,
  e a distinção **exibir × executar** código (Word não roda; Quarto/R Markdown/
  Jupyter sim — 3 condições). Refs novas: `gruber2004markdown`, `quarto_site`.
  Figuras: `markdown-fonte-vs-renderizado.svg` e **nova**
  `codigo-executavel-quarto.svg` (rótulos fora dos boxes).
- **Ficha técnica:** ex-`creditos.qmd` renomeado para **`ficha-tecnica.qmd`**,
  título `# Ficha técnica`, e **movido para o início** (em `chapters`, após
  `index.qmd`, antes de `agradecimentos.qmd`) — é página de direitos, não
  apêndice. Subseção interna "Ficha técnica" → "Dados da obra".
- **Cap. 25 (MCP e dados):** redigida a seção "Adicionar um servidor MCP a um
  projeto" como exemplo trabalhado — conectar o Code ao **Google Forms** via
  servidor MCP próprio (não há conector pronto). Ilustra a tese (técnica fica com
  o agente; autorização OAuth fica com o usuário). Inclui callout de segurança
  sobre credenciais/`refresh token`. Caso real montado fora do repo, em
  `~/Developer/_Outros/Google_MCP` (servidor Node com 7 ferramentas). Demais
  seções do Cap. 25 seguem como TODO. Dois pontos marcados `<!-- TODO: verificar -->`:
  disponibilidade do conector no catálogo e a regra de formulários "não publicados"
  a partir de 30/06/2026.

**Pendências do Cap. 1: RESOLVIDAS (jul/2026).** Exemplo condutor trocado por um
neutro entre áreas (média final de notas de turma, `notas/turma-2026.csv`); título
da seção já é "O que muda na prática".

**Lembretes/decisões em aberto:**
- Chave `perez2019publishing` no `.bib` tem ano enganoso (artigo é de 2016).
  Verificar/renomear.
- Tipografia/produção: hoje na Ficha técnica; avaliar se viram **colofão** no fim.
- Apêndice E (folha de Markdown): incluir? (ver §6).
- Data de referência a fixar no prefácio (§6).

## 9. Mapa de reaproveitamento do curso (Vibe_Coding_Project)

Pasta montada, **somente leitura, NÃO VERIFICADA** (texto e bib gerados por IA).
Adaptar (não copiar), generalizando exemplos médicos para todas as áreas.

- Cap. 1 ← `M1-ia-pesquisa/B2-agentes/01-chatbot-agente.qmd` — **redigido**
- Cap. 2 ← `M1-ia-pesquisa/B2-agentes/02-claude.qmd` — **redigido**
- Cap. 3 ← `M1-ia-pesquisa/B2-agentes/02-claude.qmd` (modos; Cowork × Code) — **redigido**
- Cap. 4 ← `M1-ia-pesquisa/B1-conceitos/02-tokens.qmd` + `01-ia-generativa.qmd` — **redigido**
- Cap. 6 (MCP) ← sem fonte no curso (conteúdo original) — **redigido**
- Cap. 7 ← `M3-analise/B1-markdown/01-markdown.qmd` — **redigido**
- Cap. 10 ← `M1-ia-pesquisa/B3-prompts/01-anatomia-prompt.qmd` + `B1-conceitos/04-prompts.qmd`
- Cap. 17 ← `M3-analise/B1-markdown/03-citacao.qmd`
- Caps. 21–22 ← `M2-fundamentos-tecnicos/B1-terminal/*` (9 páginas) — 21 Code (motivação/panorama) + 22 Terminal (o conceito)
- Cap. 27 ← `M2-fundamentos-tecnicos/B2-ambientes/02-positron.qmd` (+ rstudio, vscode)
- Cap. 29 ← `M3-analise/B1-markdown/02-quarto.qmd` + `M4-publicacao/B1-git/*`
- Cap. 29 ← `M1-ia-pesquisa/B4-limites/01-quando-ia-falha.qmd` + `02-validacao-responsabilidade.qmd`
- Cap. 30 ← `M1-ia-pesquisa/B4-limites/03-etica-regulacao.qmd` + `B1-conceitos/05-citar-ia.qmd` + `06-lgpd.qmd`

## 10. Code × Cowork: diferença de "poder" (não dizer "mesmo poder")

Verificado na documentação oficial (How Claude Code works, Overview, Permissions,
Sandboxing):
- **Code** roda no computador do usuário, com **terminal/shell completo**: executa
  qualquer comando, instala programas, sobe servidores e opera **git** (commit,
  push, branches, PRs). Mais alcance → **mais risco** (daí permissões/sandbox).
- **Cowork** é mais contido/guard-railed: trabalha com a pasta conectada,
  conectores, artefatos e tarefas agendadas, por interface gráfica. Força em
  **orquestração** (rotear, agendar, segundo plano), não em acesso profundo.
- Resumo: **Code = mais poder técnico; Cowork = mais orquestração e conveniência.**
- **[verificar]** Alguns detalhes do subagente sobre o Cowork (rodar sempre em
  "VM na nuvem", sem acesso à máquina local) **não batem** com o Cowork de
  desktop, que lê/grava arquivos locais. Não afirmar isso sem conferir.
- **Terminologia (consistência da Parte III):** o **agente é o Claude**; Cowork e
  Code são os **aplicativos/interfaces** em que ele age. Não escrever "o Cowork é
  um agente" — e sim "o Claude, como agente, trabalha…". Subagentes aparecem só no
  Despacho (Cap. 19).

## 11. Cap. 12 (Cowork) — estrutura decidida (jul/2026)

Esqueleto antigo (tour em 6 fatias) substituído: 3 seções violavam fronteiras
(modelo/esforço e modos de permissão = Cap. 8; "Conectar pasta: Projeto" = Caps.
9 e 13). Estrutura nova, aprovada pelo autor (síntese de 3 propostas):

1. **Exemplo de uso** — (revisão do autor: substituiu a cena em 1ª pessoa por
   exposição direta) o trabalho recorrente entre o manuscrito e a submissão
   (referências, estilo da revista, análise, figuras, IMRaD) e o que o Claude
   faz no Cowork: busca no PUBMED via conector (14), monta o `.bib` fidedigno
   (16), escreve o código de análise, baixa o `.csl`, estrutura em Quarto (6),
   gera PDFs anonimizados. A contenção e a conferência de DOIs saíram desta
   seção — retomar no menu + (contenção) e no Cap. 17 (DOIs). Fig.
   `cowork-tarefa-em-andamento-todos.png`: manter aqui ou mover — decidir.
2. **A tela inicial** — reuso da captura do Cap. 8, rótulo novo.
3. **A caixa de composição** — alternador Chat↔Cowork; modelo/esforço/permissão em
   1 frase cada c/ remissão ao 7; ponto novo: com agente que age, o modo de
   permissão ganha consequência. Fig. NOVA: `cowork-alternador-chat-cowork.png`.
4. **O menu +** — portas com destino: arquivos, pasta (12), comandos (13),
   conectores/plugins (14), issue do GitHub (Parte IV). Fig. existente.
5. **A barra lateral** — inventário funcional c/ remissões; a interface é o
   sumário da Parte III (prosa não declara estrutura).
6. **Recentes e o indicador** — pontinho azul; fecho em círculo com a cena.

Decisões do autor: cena SIM; contenção diluída (sem seção própria); captura nova
do alternador SIM. Risco vigiado: a cena não pode virar tutorial (esvazia o 12) —
na revisão, frase que ensina migra para o 12.

## 12. Cap. 13 (Tarefas e pastas) — estrutura decidida (jul/2026)

Esqueleto antigo (6 seções) refeito por workflow de 3 propostas (jornada do
leitor, anatomia da tarefa, ensinar pelo exemplo) + juiz. Estrutura final
(7 seções), aprovada pelo autor:

1. **A tarefa** — unidade de trabalho do Cowork: pedido → etapas → resultado
   gravado em arquivos. Critério prático: mudança em arquivos = tarefa; resposta
   = conversa (Cap. 11). A cena condutora abre o capítulo ANTES do primeiro `##`.
2. **A pasta conectada** — menu + → Adicionar pasta; chip troca "Local" pelo
   nome da pasta. O que o acesso significa (aquela pasta e só ela); anexar ×
   conectar; primeiro movimento: pedir o reconhecimento da pasta. Callout "Na
   prática": primeira tarefa sobre cópia. Fig. `cowork-caixa-de-composicao-e-contexto.png`.
3. **O pedido** — descrever o estado final dos arquivos, não o formato da
   resposta: padrão de nomes, antes/depois, limites ("não apague nada"), criar
   o inventário `.md`. Prompt completo em fala de exemplo ("você" permitido).
4. **A lista de etapas** — ler a tela enquanto o agente trabalha. ABSORVE a
   ex-seção "Ler, criar e editar arquivos" (os três verbos em ação, sem
   catálogo). Fig. `cowork-tarefa-em-andamento-todos.png` (realocada de 4/11).
5. **Aprovação e revisão** — durante (pedido de permissão; o PDF escaneado que
   faz o agente perguntar; corrigir o rumo sem cancelar) e depois (conferir no
   Finder — os arquivos mudaram de verdade; o ano errado por metadado ruim,
   corrigido na mesma tarefa). Teto ~6 parágrafos. Fig.
   `cowork-pedido-de-permissao.png` (realocada de 7).
6. **Organização de pastas** — a lição generalizada, ancorada no exemplo: a
   pasta ilegível da abertura termina como modelo. Nomes descritivos, uma pasta
   por frente, fontes × produtos. Remissões: CLAUDE.md (22), .bib (16).
7. **Tarefas dentro de Projetos** — paga a promessa dos Caps. 9 e 12 como
   FECHO: tarefa avulsa → rotina; a tarefa num Projeto herda pasta e
   instruções. Emenda no Cap. 14 sem anúncio. Fig. `cowork-projetos-aberto.png`.

**Exemplo condutor (aprovado por unanimidade das 3 propostas):** pasta de PDFs
de artigos com nomes ilegíveis (`fulltext(3).pdf`, `sdarticle.pdf`) renomeada
para autor-ano-tema — prática real do autor (os PDFs de `_source` deste livro).
Fronteira: o exemplo fica DENTRO da pasta — sem conector, sem PUBMED, sem
`.bib` (distingue do exemplo do manuscrito do Cap. 12; o 12 para no nome do
arquivo). Generalizar em uma linha (acórdãos, digitalizações de acervo).

**Decisões do autor (02/07/2026):** (a) o pedido INCLUI criar o inventário
antes/depois em `.md` (faz o agente criar um arquivo no capítulo); (b) redigir
já, com TODOs — a tarefa real roda depois no Cowork (resolve também os TODOs de
interface do Cap. 12) e gera as capturas das figs. 4 e 5; (c) **imperativos
dirigidos ao leitor: PERMITIDOS** em trechos práticos (decisão vale para o
livro todo; CLAUDE.md atualizado); (d) antes/depois da pasta = tabela curta na
prosa, sem figura nova.

## 13. Cap. 16 — de "Documentos acadêmicos" a "Análise de dados" (04/07/2026)

**Por que mudou (decisão do autor).** O capítulo antigo era um catálogo em que
cada seção resumia outro capítulo (geração de documentos e formatação = 14;
leitura de PDFs = 13; "das fontes ao documento" = 12; verificação = 17) — nada
era dele. "Documentos acadêmicos" é categoria grande demais (CSV, parquet,
grant proposals, versões de manuscrito, código, figuras) para render capítulo.
No lugar entrou o buraco real da Parte III: **o Cowork como analista de
dados** — possivelmente o caso de uso mais forte para o público. A sequência
15→16→17→18 passa a encadear conectores → análise → referências → artefatos.
Posição e numeração preservadas (exigência do autor). Texto antigo no
histórico do git; o pouco aproveitável (editável × PDF, skill por revista) já
existe nos Caps. 7 e 14.

**Arquivo/ID:** `16-analise-de-dados.qmd`, `{#sec-data-analysis}` (era
`sec-academic-docs`; a única remissão externa, no Cap. 11, foi redirecionada
para `sec-tasks`).

**Estrutura decidida (7 seções; roteiro em comentários no `.qmd`):**

1. **Arquivos de dados** — CSV/Excel/parquet, dado tabular (linha =
   observação, coluna = variável); callout Atenção: dados identificáveis →
   anonimizar antes de enviar (Cap. 30).
2. **Estrutura de arquivos do projeto** (título do autor) — a pasta é o que o
   agente vê; dados originais numa pasta onde nada escreve; árvore mínima
   (dados-brutos, dados-processados, codigo, resultados, manuscrito); o prompt
   que monta a estrutura + convenção no CLAUDE.md da pasta. FECHO: criar a
   skill `estrutura-de-projeto` (mostrar um SKILL.md curto) para reutilizar a
   cada projeto novo — aplica o critério "procedimento que se repete" do
   Cap. 14, que **não é alterado**. Prosa direta, sem subtítulos internos nem
   rótulos de chamada (pedido do autor).
3. ***Vibe coding*** — o agente escreve o script, grava e executa; loop do
   Cap. 4 sobre dados; código visível e auditável; eco da definição do Cap. 1
   (saber pedir e saber avaliar). Título homônimo ao do Cap. 1: ok, capítulos
   diferentes, sem colisão de ID.
4. **Da pergunta à análise** — descritivas, cruzamentos, testes; exemplos
   multi-área; método estatístico = decisão de quem assina; comandos do grupo
   Data (`/analyze`).
5. **Limpeza de dados** — inconsistências, faltantes, juntar planilhas,
   largo↔longo; sempre em cópia.
6. **Tabelas e figuras** — saídas em `resultados/`; estilo do destino via
   skill (Cap. 14); `/create-viz`, `/build-dashboard`; interativo → artefato
   (Cap. 18).
7. **Conferir a análise** — análogo estatístico do checklist do Cap. 17 (o N
   bate? somas conferem?); pedir explicação do método; "acelera, não assina".
   Callout Para aprofundar → Cap. 29 (reprodutibilidade).

**Pendências do Cap. 16:** (a) ~~verificar e adicionar ao `.bib` Noble 2009 e
Wilson et al. 2017~~ **FEITO em 04/07/2026** — DOIs conferidos na PLOS,
entradas `noble2009organizing` e `wilson2017good`; (b) entrada *vibe coding*
no glossário (Apêndice C, ainda stub); (c) figuras: captura
`cowork-analise-dados-tarefa.png` a fazer; a árvore de pastas entrou como
bloco de texto no capítulo (SVG dispensado — opcional, ver figuras.md);
(d) confirmar no app os comandos do grupo Data (`/analyze`, `/create-viz`,
`/build-dashboard`) e o fluxo do `skill-creator` (TODOs no `.qmd`).
