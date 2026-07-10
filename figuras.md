# Mapa de figuras — *Do Chat ao Cowork e Code*

> Liga cada figura ao capítulo onde será inserida, com legenda e texto
> alternativo sugeridos. Três blocos: **diagramas** (já gerados), **capturas
> existentes** e **capturas a fazer**. Atualizar à medida que o livro avança.

## Diagramas gerados — `images/diagramas/`

| Arquivo | Cap. | Legenda sugerida | Alt-text |
|---|---|---|---|
| `arco-chat-cowork-code.svg` | 1, 3 | O arco Chat → Cowork → Code como escala de autonomia. | Três caixas ascendentes: Chat, Cowork e Code. |
| `chatbot-vs-agente.svg` | 1 | Assistente que responde × colaborador que age. | Comparação entre uma ida e volta e um fluxo de várias etapas. |
| `linha-do-tempo-anthropic-claude.svg` | 2 | Marcos da Anthropic e do Claude (2021–2026). **[verificar datas]** | Linha do tempo com cinco marcos. |
| `loop-do-agente.svg` | 4 | O agente repete um ciclo: raciocinar, agir e observar, volta após volta. | Ciclo do agente: raciocinar (ler o contexto e decidir), agir com uma ferramenta e observar o resultado, repetido em loop. |
| `janela-de-contexto-e-tokens.svg` | 4 | A janela de contexto e os tokens. | Barra dividida em instruções, arquivos, conversa e espaço livre. |
| `mcp-encaixe-universal.svg` | 6 | MCP: um encaixe padrão entre o Claude e suas ferramentas. | Claude ao centro, ligado a seis conectores. |
| `anatomia-de-um-bom-prompt.svg` | 10 | Os componentes de um bom prompt. | Cinco linhas: papel, tarefa, exemplos, formato, restrições. |
| `markdown-fonte-vs-renderizado.svg` | 7 | Markdown: a fonte e o resultado. | Painel de código à esquerda, resultado à direita. |
| `codigo-executavel-quarto.svg` | 7 | Uma célula de código executável: o Quarto roda o código e insere o resultado. | Célula de código à esquerda; resultado calculado à direita. |
| `fluxo-de-citacao.svg` | 17 | Da busca à referência verificada. | Cinco etapas terminando em "verificar". |
| `bibtex-csl-quarto.svg` | 17, 29 | Como a bibliografia é gerada: .bib + .csl + Quarto. | Dois arquivos alimentam o Quarto, que gera o documento. |
| `modos-de-permissao.svg` | 8, 25 | Modos de permissão, do mais controlado ao mais autônomo. | Cinco modos em escala de cor. |
| `estrutura-projeto-quarto.svg` | 29 | A estrutura de um projeto Quarto. | Árvore de pastas e arquivos do projeto. |

**Resolvido sem figura:** a árvore mínima do projeto de dados (cap. 16) entrou
como bloco de texto monoespaçado no próprio capítulo; o SVG
(`diagrama-pasta-projeto-dados.svg`, no traço de `estrutura-projeto-quarto.svg`)
fica como opção se o autor preferir figura.

## Capturas de tela existentes — `images/`

| Arquivo | Cap. | Legenda sugerida |
|---|---|---|
| `cowork-tela-inicial-home.png` | 8, 12 | A tela inicial do aplicativo de desktop (Chat, Cowork e Code numa janela). |
| `cowork-menu-adicionar.png` | 12, 15 | O menu "+": arquivos, pasta, comandos, conectores, plugins. |
| `cowork-caixa-de-composicao-e-contexto.png` | 13 | A caixa de tarefa e os chips de contexto. |
| `cowork-modos-de-permissao.png` | 8, 25 | O seletor de modos de permissão. |
| `cowork-seletor-de-modelos.png` | 3 | O seletor de modelos. |
| `cowork-controle-de-esforco.png` | 3 | O controle de esforço. |
| `cowork-uso-do-plano.png` | 8, 31 | O painel de uso do plano. |
| `cowork-painel-de-estatisticas.png` | 31 | As estatísticas de uso. |
| `cowork-recentes-indicador-de-atividade.png` | 12, 19 | O indicador de atividade (pontinho azul) na lista Recentes. |
| `claude-configuracoes-geral-perfil-instrucoes.png` | 9 | Configurações: perfil e instruções personalizadas. |
| `comandos-de-barra.png` | 14 | A lista de comandos de barra, aberta ao digitar `/`, agrupada por finalidade (geral e Data). |
| `conectores.png` | 15 | O menu de conectores: serviços ligados (Gmail, Google Calendar, Drive, PUBMED…) com interruptor, e os atalhos de adicionar/gerenciar. |
| `cowork-comandos-data-analyze.png` | 16 | O comando `analyze` do plugin Data, com sua descrição, na lista filtrada ao digitar `/data`. |
| `permissao-explicita.png` | 23 | O Claude recusa criar um repositório público sem autorização explícita (o sistema de permissões em ação). |
| `claude-code-ide-terminal.png` | 27 | O Claude Code rodando no terminal integrado do editor (tela de boas-vindas com versão, modelo e pasta). |
| `claude-code-ide-extensao.png` | 27 | O Claude Code como aba/extensão do editor, com o campo de composição próprio. |

## Capturas a fazer (nomes sugeridos)

**Conectar e estender:** `cowork-conectar-mcp-login.png` (tela de autorização/OAuth, cap. 15); `cowork-plugins-lista.png`, `cowork-marketplace.png` (cap. 15).

**Barra lateral:** `cowork-projetos-aberto.png` (cap. 13); `cowork-artefatos-galeria.png`, `cowork-artefato-aberto.png` (cap. 18); `cowork-programado-lista.png`, `cowork-programado-criar.png` (cap. 19); `cowork-despacho.png` (cap. 19); `claude-configuracoes-conta.png`, `claude-configuracoes-privacidade.png`, `claude-configuracoes-cobranca.png` (cap. 8).

**Caixa de composição:** `cowork-alternador-chat-cowork.png` (cap. 12) — plano fechado do alternador Chat↔Cowork na caixa; o gesto que cruza a fronteira do Cap. 11.

**Agente em ação:** `cowork-tarefa-em-andamento-todos.png` (cap. 13 — a tarefa de renomeação em execução, etapas concluídas e ação corrente; realocada de 4/12: o Cap. 4 usa o diagrama do loop e o Cap. 12 pronto não a usa); `cowork-pedido-de-permissao.png` (cap. 13 — o pedido de permissão durante a renomeação; realocada de 8, que usa o diagrama e o seletor); `cowork-analise-dados-tarefa.png` (cap. 16 — tarefa de análise de dados em execução sobre uma planilha; substitui a antiga `cowork-skill-gerando-documento.png`, do foco descartado do capítulo). As duas primeiras saem da mesma sessão: rodar a tarefa real do Cap. 13 no Cowork.

**Parte IV (Code):** `code-aba-sessao-terminal.png` (cap. 21 — a aba Code); `code-terminal-boas-vindas.png` (cap. 23 — a tela de boas-vindas do `claude` num terminal limpo, fora de um editor); `code-positron-terminal.png`, `code-cursor.png`, `code-antigravity.png` (cap. 27).

**Outras:** `claude-planos-assinatura.png` (cap. 8); `cowork-onboarding-papel.png` (cap. 8); `chat-conversa-bom-prompt.png`, `chat-resumo-pdf.png`, `chat-projetos.png` (caps. 10–11).

## Capa e favicon — `images/capa-favicon/`

`capa-do-chat-ao-cowork-e-code.svg` (capa, Conceito B grafite) · `favicon.svg`
(+ PNGs e `.ico`). Capa na página de rosto (PDF) e na home (HTML); favicon via
`format: html: favicon:` no `_quarto.yml`.

## Imagens externas (com atribuição)

| Arquivo | Cap. | Legenda | Crédito / licença |
|---|---|---|---|
| `claude-shannon-retrato.jpg` | 2 | Claude Shannon (1916–2001), o "pai da teoria da informação", que dá nome ao assistente. | Foto: **Tekniska museet**, via Wikimedia Commons, **CC BY 2.0 Generic** (<https://creativecommons.org/licenses/by/2.0/>). Origem: <https://commons.wikimedia.org/wiki/File:C.E._Shannon._Tekniska_museet_43069.jpg> · Alt-text: retrato em P&B de Claude Shannon, anos 1950. |

> Licença **CC BY 2.0**: exige dar **crédito** ao autor (Tekniska museet),
> **link para a licença** e **indicar se houve alterações** (recorte,
> redimensionamento). O crédito já consta na legenda da figura, aqui e na
> página de **Ficha técnica** (`ficha-tecnica.qmd`). Se a imagem for recortada/ajustada,
> registrar "imagem redimensionada/recortada" no crédito.

## Caixas (não são figuras, mas a registrar)

- **Curiosidade — os *spinner verbs*** (cap. 4): as palavras enquanto o agente
  "pensa". Fontes no `.bib`.
- **Para aprofundar — Fable 5, Mythos 5 e o controle de exportação** (parte V):
  tratar de forma factual e equilibrada; **[verificar]** antes de publicar.
