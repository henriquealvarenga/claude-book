# Revisão — remoção do "você" (2ª pessoa)

> Documento de trabalho (não entra no livro). Cada ocorrência de "você" e de
> possessivo de 2ª pessoa foi classificada: **corrigir** (endereçamento ao leitor
> na voz do livro), **manter (prompt)** (dentro de fala de exemplo — não mexer) ou
> **manter (3ª pessoa)** (o "seu/sua" se refere a outro sujeito — correto).
>
> **Como revisar:** escreva `OK` ou `NÃO` ao lado do número do item (ex.:
> `#### 3. … — OK`), ou responda no chat por números ("Cap. 1: todos OK menos o 13").
> Itens aprovados serão aplicados; os demais ficam como estão.
>
> Capítulos 11+ (Cowork em diante) já seguem a regra desde a redação.

## Resumo

| Arquivo | Ocorrências | A corrigir | A manter |
|---|---|---|---|
| apresentacao.qmd (ex-prefácio/index) | 9 (7 itens) | 5 itens | 2 |
| ficha-tecnica.qmd | 1 | 0 | 1 |
| Cap. 1 — virada agêntica | 21 | 21 (16 itens) | 0 |
| Cap. 2 — Anthropic e Claude | 1 (+1 nota) | 0 | 1 |
| Cap. 3 — ecossistema | 14 | 13 (9 itens) | 1 |
| Cap. 4 — como o agente trabalha | 7 | 7 (5 itens) | 0 |
| Cap. 6 — MCP | 10 | 9 | 1 |
| Cap. 7 — Markdown | 7 | 4 | 3 |
| Cap. 8 — Setup | 13 (+1 nota) | 12 | 1 |
| Cap. 9 — Personalização | 11 | 10 (8 itens) | 1 |
| Cap. 10 — Prompt | 22 | 19 | 3 |
| Cap. 11 — Chat na prática | 13 | 12 (8 itens) | 1 |
| Cap. 21 — terminal (esqueleto) | 1 | 0 | 1 |
| Cap. 25 — MCP e dados | 13 | 13 (7 itens) | 0 |
| Cap. 26 — editores (esqueleto) | 1 | 1 | 0 |
| Cap. 29 — ética (esqueleto) | 1 | 0 | 1 |
| Apêndice F — spinner | 1 | 1 | 0 |

**Duas decisões além do "você"** (apontadas pelos revisores):

1. **Imperativos de 2ª pessoa sem "você"** ("Reveja esses ajustes", "Suba na
   escala", "não se prenda ao número", "mostre um exemplo", "peça", "anexe") —
   a regra alcança também o imperativo? Ele endereça o leitor diretamente, mas
   é a voz natural de instrução prática. Caps. 2, 8, 10 e 11 dependem disso.
2. **"a decisão é sua" repetida** — o Cap. 6, item 9, nota que a moral já
   aparece em outros capítulos; avaliar cortar a frase em vez de reescrevê-la.

---

## apresentacao.qmd (ex-prefácio — linhas referem-se ao arquivo novo; o título mudou de "Prefácio" para "Apresentação")

#### 1. (linha 3) corrigir
- Original: "Ela lê seus arquivos, executa tarefas em várias etapas, conecta-se a outras ferramentas e leva um trabalho até o fim, sob sua supervisão."
- Proposta: "Ela lê arquivos, executa tarefas em várias etapas, conecta-se a outras ferramentas e leva um trabalho até o fim, sob a supervisão do usuário."

#### 2. (linha 5) manter (3ª pessoa)
- Original: "Seu foco são três formas de usar o Claude, o assistente da Anthropic" — "Seu" refere-se ao livro, não ao leitor.

#### 3. (linha 5) corrigir
- Original: "da conversa que organiza ideias, à colaboração que manipula seus documentos, até a automação que torna uma pesquisa inteira reproduzível"
- Proposta: "…à colaboração que manipula documentos…" (só remove o "seus")

#### 4. (linha 15) corrigir
- Original: "Não ensina a fazer essas tarefas — a metodologia, o julgamento e a redação continuam sendo seus; o livro mostra como o agente pode ajudar."
- Proposta: "Não ensina a fazer essas tarefas — a metodologia, o julgamento e a redação continuam sendo de quem pesquisa; o livro mostra como o agente pode ajudar."

#### 5. (linha 19) corrigir
- Original: "A **Parte III**, a mais extensa, dedica-se ao **Cowork**: a colaboração com seus próprios arquivos, sem que você precise programar."
- Proposta: "A **Parte III**, a mais extensa, dedica-se ao **Cowork**: a colaboração com os próprios arquivos, sem que o usuário precise programar."

#### 6. (linha 32) manter (3ª pessoa)
- Original: "O Claude e seus produtos evoluem com rapidez" — "seus" refere-se ao Claude.

#### 7. (linha 34) corrigir
- Original: "Quando uma tela ou um comando aqui descrito não corresponder exatamente ao que você vê, o conceito por trás dele tende a permanecer válido — e é nele que vale a pena se apoiar."
- Proposta: "Se uma tela ou um comando aqui descrito não corresponder exatamente ao que o usuário vê, o conceito por trás dele tende a permanecer válido — e é nele que vale a pena se apoiar."
  (Também troca a abertura "Quando…", vetada na lista de vícios do CLAUDE.md.)

---

## ficha-tecnica.qmd

#### 1. (linha 44) manter (3ª pessoa)
- Original: ""Claude", "Anthropic" e demais marcas… pertencem aos seus respectivos titulares…" — "seus" refere-se às marcas, não ao leitor.

---

## capitulos/p1-fundamentos/01-virada-agentica.qmd

#### 1. (linha 9) corrigir
- Original: "Você provavelmente já conversou com um chatbot: digita uma mensagem, o modelo lê e devolve texto. Para *fazer* algo com essa resposta — executar o cálculo, salvar o arquivo, formatar a tabela —, quem age é você. O chatbot responde, mas não executa: não enxerga o seu computador nem altera nada no sistema. O texto só vira ação quando você o executa."
- Proposta: "Um chatbot funciona assim: digita-se uma mensagem, o modelo lê e devolve texto. Para *fazer* algo com essa resposta — executar o cálculo, salvar o arquivo, formatar a tabela —, quem age é o usuário. O chatbot responde, mas não executa: não enxerga o computador nem altera nada no sistema. O texto só vira ação quando alguém o executa."
  (4 ocorrências resolvidas numa proposta)

#### 2. (linha 11) corrigir
- Original: "Disso resulta o **fluxo de cópia-e-cola**: você pergunta, copia a resposta, cola no seu programa, vê um erro, volta ao chat, cola de novo."
- Proposta: "Disso resulta o **fluxo de cópia-e-cola**: perguntar, copiar a resposta, colar no programa, ver um erro, voltar ao chat, colar de novo."

#### 3. (linha 13) corrigir
- Original: "**autonomia para iterar**, encadeando ações e observando cada resultado sem esperar você entre os passos"
- Proposta: "…sem esperar o usuário entre os passos"

#### 4. (linha 17) corrigir
- Original: "Suponha que você peça: *"calcule a média final da turma na planilha `notas/turma-2026.csv`."*"
- Proposta: "Suponha o pedido: *"calcule a média final da turma na planilha `notas/turma-2026.csv`."*"
  (o prompt entre aspas fica intacto; só a moldura muda)

#### 5. (linha 19) corrigir
- Original: "Um chatbot devolve um trecho de código para você copiar, executar e depurar por conta própria."
- Proposta: "Um chatbot devolve um trecho de código para o usuário copiar, executar e depurar por conta própria."

#### 6. (linha 21) corrigir
- Original: "Em vez de entregar um trecho para você copiar, o agente grava o código no próprio projeto"
- Proposta: "Em vez de entregar um trecho para copiar, o agente grava o código no próprio projeto"

#### 7. (linha 29) corrigir — tabela
- Original: "| Você pede | "Gere o código da análise." | "Faça a análise dos meus dados." |"
- Proposta: "| Pedir | "Gere o código da análise." | "Faça a análise dos meus dados." |"
  (rótulo em infinitivo, em paralelo com "Executar" e "Tratar um erro"; os prompts das células são exemplos e ficam)

#### 8. (linha 31) corrigir — tabela
- Original: "| Executar | Você copia, cola e roda. | Ele roda. |"
- Proposta: "| Executar | O usuário copia, cola e roda. | Ele roda. |"

#### 9. (linha 32) corrigir — tabela
- Original: "| Tratar um erro | Você devolve o erro ao chat e espera. | Ele lê o erro, corrige e roda de novo. |"
- Proposta: "| Tratar um erro | O usuário devolve o erro ao chat e espera. | …|"

#### 10. (linha 33) corrigir — tabela
- Original: "| Resultado final | Saída na tela, que você ainda salva e formata. | …|"
- Proposta: "| Resultado final | Saída na tela, ainda por salvar e formatar. | …|"

#### 11. (linha 42) corrigir
- Original: "Com um agente, você diz "separe os resultados por grupo" e vê o resultado em segundos — e por isso explora mais."
- Proposta: "Com um agente, basta dizer "separe os resultados por grupo" para ver o resultado em segundos — e por isso se explora mais."

#### 12. (linha 44) corrigir
- Original: "No chatbot, um pedido ruim gera uma resposta ruim, que você descarta. No agente, um pedido ruim gera arquivos ruins no projeto antes de você revisar (Cap. 10)."
- Proposta: "No chatbot, um pedido ruim gera uma resposta ruim, que se descarta. No agente, um pedido ruim gera arquivos ruins no projeto antes de qualquer revisão (Cap. 10)."

#### 13. (linha 58) corrigir
- Original: "Embora o agente atue, a responsabilidade continua sua."
- Proposta: "Embora o agente atue, a responsabilidade continua do usuário."

#### 14. (linha 58) corrigir
- Original: "nos modos mais autônomos, esses pedidos diminuem — por escolha sua."
- Proposta: "nos modos mais autônomos, esses pedidos diminuem — por escolha do usuário."

#### 15. (linha 66) corrigir
- Original: "E o **julgamento metodológico continua seu** — se a abordagem é adequada ao problema, se uma fonte é confiável."
- Proposta: "E o **julgamento metodológico não se delega** — se a abordagem é adequada ao problema, se uma fonte é confiável."

#### 16. (linha 74) corrigir
- Original: "Há ainda o cuidado com os dados: o agente lê o que você lhe der acesso."
- Proposta: "Há ainda o cuidado com os dados: o agente lê tudo a que recebe acesso."

---

## capitulos/p1-fundamentos/02-anthropic-e-claude.qmd

#### 1. (linha 5) manter (3ª pessoa)
- Original: "…explicam muito do seu comportamento." — "seu" refere-se ao Claude.

**Nota extra (decisão 1 do resumo):** a linha 33 tem imperativo dirigido ao leitor — "então **não se prenda** ao número…". Proposta impessoal: "então o número importa menos que a posição do modelo na escala capacidade × custo × velocidade."

---

## capitulos/p1-fundamentos/03-ecossistema-claude.qmd

#### 1. (linha 9) corrigir — 2 ocorrências
- Original: "no **Chat**, ele conversa e pesquisa, mas não toca nos seus arquivos; no **Cowork**, trabalha com os seus arquivos; no **Code**, trabalha no terminal."
- Proposta: "no **Chat**, ele conversa e pesquisa, mas não toca em arquivos; no **Cowork**, trabalha com os arquivos de uma pasta; no **Code**, trabalha no terminal."

#### 2. (linha 13) corrigir — 4 ocorrências
- Original: "Você escreve, ele responde; você pode anexar arquivos e imagens e reunir contexto em **Projetos**, que reaproveitam instruções entre conversas. O Chat não mexe sozinho no seu computador: o que sai dali é texto, que você usa como quiser."
- Proposta: "O usuário escreve, o Claude responde; é possível anexar arquivos e imagens e reunir contexto em **Projetos**, que reaproveitam instruções entre conversas. O Chat não mexe no computador: o resultado é texto."
  (Aplica também duas correções da lista viva: "o que sai dali" e corta "que você usa como quiser".)

#### 3. (linha 17) corrigir
- Original: "…o Claude trabalha com uma **pasta** que você conecta: lê, cria e edita arquivos…"
- Proposta: "…o Claude trabalha com uma **pasta conectada**: lê, cria e edita arquivos…"

#### 4. (linha 17) corrigir
- Original: "Tudo por uma interface gráfica, sem que **você** precise programar — o agente cuida da parte técnica…"
- Proposta: "Tudo por uma interface gráfica, sem que o usuário precise programar — o agente cuida da parte técnica…"

#### 5. (linha 17) manter (3ª pessoa)
- Original: "É para quem quer trabalhar com seus documentos e dados sem dominar programação." — "seus" remete a "quem". (Se quiser eliminar a ambiguidade: "com os próprios documentos e dados".)

#### 6. (linha 21) corrigir
- Original: "Por operar ali, com acesso ao terminal do seu computador, ele **vai além** do Cowork…"
- Proposta: "Por operar ali, com acesso ao terminal do computador, ele **vai além** do Cowork…"

#### 7. (linha 25) corrigir
- Original: "A escolha segue do que você precisa fazer:"
- Proposta: "A escolha depende da tarefa:"

#### 8. (linha 27) corrigir — cabeçalho de tabela
- Original: "Age nos seus arquivos?"
- Proposta: "Age nos arquivos?"

#### 9. (linha 33) corrigir
- Original: "Na prática: para organizar ideias ou redigir, fique no Chat; para trabalhar com seus documentos e dados sem precisar programar, use o Cowork; para automatizar e tornar uma pesquisa reproduzível, vá ao Code."
- Proposta: "Na prática: organizar ideias ou redigir pede o Chat; trabalhar com documentos e dados sem programar, o Cowork; automatizar e tornar uma pesquisa reproduzível, o Code."
  (Remove também os imperativos "fique/use/vá".)

#### 10. (linha 37) corrigir
- Original: "Os três produtos usam a mesma família de modelos, e você escolhe, dentro de cada interface, o modelo e o **esforço** — …"
- Proposta: "Os três produtos usam a mesma família de modelos; dentro de cada interface, escolhem-se o modelo e o **esforço** — …"

---

## capitulos/p1-fundamentos/04-como-um-agente-trabalha.qmd

#### 1. (linha 7) corrigir
- Original: "…até concluir a tarefa ou pedir a sua confirmação…"
- Proposta: "…até concluir a tarefa ou pedir confirmação ao usuário…"

#### 2. (linha 21) corrigir
- Original: "Tudo o que o agente "enxerga" de uma vez — as suas instruções, os arquivos abertos, a conversa até ali —…"
- Proposta: "…— as instruções recebidas, os arquivos abertos, a conversa até ali —…"

#### 3. (linha 21) corrigir
- Original: "…o que se disse na anterior não vem junto — a menos que você o traga de volta, como mostra o Cap. 9."
- Proposta: "…— a menos que seja trazido de volta, como mostra o Cap. 9."

#### 4. (linha 29) corrigir — 2 ocorrências
- Original: "…o consumo — quanto você "gasta" — também é contado assim. Você não precisa contá-los à mão; basta saber…"
- Proposta: "…o consumo — quanto se "gasta" — também é contado assim. Não é preciso contá-los à mão; basta saber…"

#### 5. (linha 41) corrigir — 2 ocorrências
- Original: "Por tudo isso, a responsabilidade continua sua. Você revisa o que sai e aprova o que o agente faz — e os **modos de permissão** (Cap. 8)…"
- Proposta: "Por tudo isso, a responsabilidade continua com o usuário: revisar o que sai e aprovar o que o agente faz — e os **modos de permissão** (Cap. 8)…"

---

## capitulos/p1-fundamentos/05-mcp.qmd

#### 1. (linha 9) corrigir
- Original: "No **Cowork**, mexer nos arquivos da sua pasta é nativo…"
- Proposta: "No **Cowork**, mexer nos arquivos da pasta conectada é nativo…"

#### 2. (linha 9) corrigir
- Original: "Quando o agente edita um documento ou roda um comando no seu computador, **não** está usando MCP: está usando uma ferramenta que já é dele."
- Proposta: "Ao editar um documento ou rodar um comando no computador, o agente **não** usa MCP: usa uma ferramenta que já é dele."
  (Elimina também a abertura com "Quando…".)

#### 3. (linha 11) corrigir
- Original: "…ligar o agente a serviços e dados de fora — o seu Gmail, o PUBMED, o GitHub."
- Proposta: "…— o Gmail, o PUBMED, o GitHub."

#### 4. (linha 13) corrigir — 2 ocorrências
- Original: "Você não precisa conectar MCP algum para o agente trabalhar com os seus arquivos, escrever código ou consultar a web — isso ele já faz sozinho."
- Proposta: "Não é preciso conectar MCP algum para o agente trabalhar com os arquivos, escrever código ou consultar a web — isso ele já faz sozinho."

#### 5. (linha 17) manter (3ª pessoa)
- Original: "…OpenAI, Google e Microsoft também passaram a dar suporte ao MCP em seus próprios produtos" — refere-se às empresas.

#### 6. (linha 23) corrigir
- Original: "um programa que sabe falar com o Gmail, com o PUBMED ou com os seus arquivos, e que oferece capacidades"
- Proposta: "um programa que sabe falar com o Gmail, com o PUBMED ou com os arquivos locais, e que oferece capacidades"

#### 7. (linha 23) corrigir
- Original: "Quando você vê **"Conectores"** no Cowork, cada um deles é, por baixo, um MCP."
- Proposta: "Cada **"Conector"** do Cowork é, por baixo, um MCP."

#### 8. (linha 31) corrigir — 2 frases
- Original: "No **Cowork**, você conecta um MCP pelo menu de **Conectores**, de modo gráfico (Cap. 15). No **Code**, adiciona um servidor MCP à configuração do projeto (Cap. 25)."
- Proposta: "No **Cowork**, o usuário conecta um MCP pelo menu de **Conectores**, de modo gráfico (Cap. 15). No **Code**, adiciona um servidor MCP à configuração do projeto (Cap. 25)."

#### 9. (linha 35) corrigir
- Original: "Por isso a decisão é sua — o que conectar e o que o agente pode fazer com isso."
- Proposta: "Por isso a decisão fica com o usuário: o que conectar e o que o agente pode fazer com isso."
  (Ver decisão 2 do resumo: avaliar cortar a frase em vez de reescrever.)

---

## capitulos/p1-fundamentos/06-markdown.qmd

#### 1. (linha 7) manter (3ª pessoa) — "seus arquivos de configuração" = do Claude.
#### 2. (linha 9) manter (3ª pessoa) — "sua adoção" = do Markdown.

#### 3. (linha 14) corrigir — título de callout
- Original: "## Você já escreve assim"
- Proposta: "## As marcas do WhatsApp"

#### 4. (linha 16) corrigir
- Original: "Talvez sem perceber, você já usa marcas inspiradas no Markdown todo dia."
- Proposta: "Quem troca mensagens já usa marcas inspiradas no Markdown todo dia, talvez sem perceber."

#### 5. (linha 87) manter (3ª pessoa) — "à sua maneira" = de cada programa.

#### 6. (linha 105) corrigir — 2 ocorrências
- Original: "A conversão corre por baixo no Pandoc, e o Claude o aciona por você. Você escreve uma vez, em texto simples, e o resultado sai no formato que a ocasião pedir…"
- Proposta: "A conversão corre por baixo no Pandoc, que o Claude aciona. Escreve-se uma vez, em texto simples, e o resultado sai no formato que a ocasião pedir…"

---

## capitulos/p1-fundamentos/07-setup.qmd

#### 1. (linha 23) corrigir
- Original: "O Cowork existe só no aplicativo de desktop (macOS e Windows), que você baixa e instala."
- Proposta: "…, que se baixa e instala."

#### 2. (linha 23) corrigir
- Original: "…em que as tarefas rodam na nuvem, não na sua máquina."
- Proposta: "…, não na máquina do usuário."

#### 3. (linha 23) manter (3ª pessoa)
- Original: "Sua instalação fica na Parte IV…" — "Sua" = do Code. (Se quiser eliminar ambiguidade após o item 2: "A instalação do Code fica na Parte IV…")

#### 4. (linha 29) corrigir
- Original: "O agente lê o que você lhe dá acesso, e só isso."
- Proposta: "O agente lê aquilo a que recebeu acesso, e só isso."

#### 5. (linha 29) corrigir
- Original: "O que compartilhar é decisão sua, e as configurações de privacidade controlam, por exemplo, se as suas conversas podem servir para treinar os modelos."
- Proposta: "O que compartilhar é decisão do usuário, e as configurações de privacidade controlam, por exemplo, se as conversas podem servir para treinar os modelos."

#### 6. (linha 31) corrigir
- Original: "Tudo o que você dá ao agente sai do seu computador: vai para os servidores que rodam o modelo."
- Proposta: "Tudo o que o agente recebe sai do computador: vai para os servidores que rodam o modelo."

#### 7. (linha 31) corrigir
- Original: "…mas a decisão é sua: anonimize o que puder e confira as regras da sua instituição e do comitê de ética…"
- Proposta: "…mas a decisão é de quem pesquisa: anonimizar o que for possível e conferir as regras da instituição e do comitê de ética…"

#### 8. (linha 35) corrigir
- Original: "O agente age, mas a responsabilidade pelo resultado é sua."
- Proposta: "O agente age, mas a responsabilidade pelo resultado é do usuário."

#### 9. (linha 35) corrigir
- Original: "Cabe a você revisar o que sai e validar antes de usar (Cap. 28)."
- Proposta: "É preciso revisar o que sai e validar antes de usar (Cap. 28)."

#### 10. (linha 41) corrigir
- Original: "No aplicativo, você ajusta o modo num seletor ao pé da caixa de composição…"
- Proposta: "No aplicativo, o modo se ajusta num seletor ao pé da caixa de composição…"

**Nota extra (decisão 1 do resumo):** imperativos sem "você" na voz do livro — "Reveja esses ajustes antes de começar." (l. 29) e "Suba na escala à medida que a confiança na tarefa cresce, não antes." (l. 49).

---

## capitulos/p1-fundamentos/08-personalizacao.qmd

#### 1. (linha 7) corrigir — 3 ocorrências
- Original: "Nas configurações, você informa seu nome, como quer ser chamado e o que descreve seu trabalho."
- Proposta: "Nas configurações, o usuário informa o nome, como quer ser chamado e uma descrição do trabalho."

#### 2. (linha 11) corrigir
- Original: "As instruções personalizadas são preferências que valem em toda conversa, sem você reescrevê-las. Servem para dizer como quer as respostas: …"
- Proposta: "…sem precisar reescrevê-las. Servem para dizer como devem ser as respostas: …" (instruções entre aspas são fala de exemplo — ficam)

#### 3. (linha 13) corrigir — texto alternativo da figura
- Original: "…como o Claude deve chamar você…"
- Proposta: "…como o Claude deve chamar o usuário…"

#### 4. (linha 15) manter (3ª pessoa) — "as suas próprias regras" = de cada projeto.

#### 5. (linha 19) corrigir
- Original: "Em vez de montar o contexto a cada conversa, você o prepara uma vez, e tudo o que acontece dentro do projeto já parte dali."
- Proposta: "O contexto é montado uma vez, não a cada conversa, e tudo o que acontece dentro do projeto já parte dali."

#### 6. (linha 19) corrigir
- Original: "Para uma disciplina que você leciona todo semestre, ou um artigo em andamento, isso evita recomeçar do zero a cada sessão."
- Proposta: "Para uma disciplina lecionada todo semestre, ou um artigo em andamento, isso evita recomeçar do zero a cada sessão."

#### 7. (linha 25) corrigir
- Original: "Além do que você configura, o agente guarda o que aprende sozinho."
- Proposta: "Além do que o usuário configura, o agente guarda o que aprende sozinho."

#### 8. (linha 25) corrigir
- Original: "…e a grava num arquivo (`memory.md`) que você pode abrir, editar ou apagar."
- Proposta: "…e a grava num arquivo (`memory.md`) que pode ser aberto, editado ou apagado."

#### 9. (linha 27) corrigir
- Original: "As instruções são suas; a memória, o agente preenche."
- Proposta: "O usuário escreve as instruções; o agente preenche a memória."

---

## capitulos/p2-conversar/09-prompt.qmd

#### 1. (linha 5) corrigir
- Original: "…por meio de um *prompt*: a pergunta, o pedido, a instrução que você escreve ao modelo."
- Proposta: "…por meio de um *prompt*: a pergunta, o pedido, a instrução dirigida ao modelo."

#### 2. (linha 9) corrigir
- Original: "Mas o nome ficou: tudo o que você escreve ao Claude continua sendo um prompt."
- Proposta: "Mas o nome ficou: tudo o que se escreve ao Claude continua sendo um prompt."

#### 3. (linha 17) manter (prompt) — ""você é um revisor de metodologia"" é fala de exemplo.

#### 4. (linha 18) corrigir
- Original: "**Tarefa** — o que você quer, dito com precisão."
- Proposta: "**Tarefa** — o que se quer, dito com precisão."

#### 5. (linha 19) corrigir
- Original: "**Exemplos** — um modelo do que você espera."
- Proposta: "**Exemplos** — um modelo do resultado esperado."

#### 6. (linha 29) corrigir — 3 ocorrências
- Original: "O Claude não sabe o que está na sua tela nem na sua cabeça. Ele tem o que você escreve e os arquivos que anexa."
- Proposta: "O Claude não sabe o que está na tela nem na cabeça de quem escreve. Ele tem o prompt e os arquivos anexados."

#### 7. (linha 29) manter (3ª pessoa) — "a área e suas convenções" = da área.

#### 8. (linha 31) corrigir
- Original: "…devolve o que você precisa."
- Proposta: "…devolve o que interessa."

#### 9. (linha 33) corrigir
- Original: "O Claude implementa melhor do que decide: a escolha do método é sua, a execução é dele."
- Proposta: "O Claude implementa melhor do que decide: a escolha do método cabe ao usuário, a execução ao Claude."

#### 10. (linha 42) corrigir — 2 ocorrências
- Original: "Quando você tem uma referência clara do que quer, mostre um exemplo. Descrever "quero um resumo conciso e crítico" rende menos que colar um resumo que você considera bom e pedir "no mesmo estilo"."
- Proposta: "Com uma referência clara do que se quer, mostre um exemplo. Descrever "quero um resumo conciso e crítico" rende menos que colar um resumo considerado bom e pedir "no mesmo estilo"."
  (Elimina também a abertura "Quando…"; aspas internas ficam.)

#### 11. (linha 44) corrigir
- Original: ""fale sobre os estudos" produz texto que você ainda terá de reorganizar."
- Proposta: ""fale sobre os estudos" produz texto ainda por reorganizar."

#### 12. (linha 48) manter (prompt) — ""pense passo a passo; liste suas suposições…"" é fala de exemplo.

#### 13. (linha 50) corrigir — 2 ocorrências
- Original: "Quando você não sabe ao certo o que pedir, deixe o Claude apontar a lacuna: "antes de responder, diga que informações faltariam para uma resposta de qualidade". A pergunta de volta costuma revelar o que você deixaria de fora."
- Proposta: "Sem saber ao certo o que pedir, deixe o Claude apontar a lacuna: "antes de responder, diga que informações faltariam para uma resposta de qualidade". A pergunta de volta costuma revelar o que ficaria de fora."

#### 14. (linha 54) corrigir
- Original: "No Chat, a conversa continua: você corrige, acrescenta, redireciona, e cada resposta parte do que já foi dito."
- Proposta: "No Chat, a conversa continua: o usuário corrige, acrescenta, redireciona, e cada resposta parte do que já foi dito."

#### 15. (linha 56) corrigir
- Original: "E um problema por vez: se você aponta três defeitos juntos, ele tenta resolver tudo de uma vez e costuma piorar dois enquanto conserta um."
- Proposta: "E um problema por vez: com três defeitos apontados juntos, ele tenta resolver tudo de uma vez e costuma piorar dois enquanto conserta um."

#### 16. (linha 69) corrigir
- Original: "A conferência final é sua: os números batem? a fonte existe? o argumento se sustenta?"
- Proposta: "A conferência final cabe ao usuário: os números batem? a fonte existe? o argumento se sustenta?"

#### 17. (linha 69) corrigir
- Original: "Lembre, ainda, que o que você cola na conversa é enviado ao servidor — cuidado com dados sensíveis (Cap. 29)."
- Proposta: "Além disso, o que se cola na conversa é enviado ao servidor — cuidado com dados sensíveis (Cap. 29)."

#### 18. (linha 77) corrigir
- Original: "…só ganham peso, porque ali ele executa o que você pede."
- Proposta: "…só ganham peso, porque ali ele executa o que se pede."

---

## capitulos/p2-conversar/10-chat-na-pratica.qmd

#### 1. (linha 3) manter (3ª pessoa) — "extrair sua tese" = do artigo.

#### 2. (linha 3) corrigir — 2 ocorrências
- Original: "O resultado é texto, e nada muda no seu computador enquanto você não copiar e colar."
- Proposta: "O resultado é texto, e nada muda no computador enquanto ele não for copiado e colado."

#### 3. (linha 13) corrigir — 3 ocorrências
- Original: "Deixar que ele escreva o texto inteiro no seu lugar troca a sua voz pela dele e leva a autoria para um terreno incômodo (Cap. 29). Corrigir a partir do diagnóstico mantém o texto seu."
- Proposta: "Deixar que ele escreva o texto inteiro troca a voz de quem escreve pela dele e leva a autoria para um terreno incômodo (Cap. 29). Corrigir a partir do diagnóstico preserva essa voz."

#### 4. (linha 17) corrigir
- Original: "enuncie sua tese e peça a objeção mais forte contra ela, o Claude no papel de advogado do diabo."
- Proposta: "enuncie a tese e peça a objeção mais forte contra ela, o Claude no papel de advogado do diabo."

#### 5. (linha 19) corrigir
- Original: "O Claude pode organizar o material que você fornece, propor arranjos e oferecer um mapa de opções."
- Proposta: "O Claude pode organizar o material fornecido, propor arranjos e oferecer um mapa de opções."

#### 6. (linha 23) corrigir — 2 ocorrências
- Original: "…hipóteses rivais para uma correlação que você observou; as perguntas que uma banca faria à sua dissertação…"
- Proposta: "…hipóteses rivais para uma correlação observada; as perguntas que uma banca faria à dissertação…"

#### 7. (linha 29) corrigir
- Original: "Uma busca ancorada em resultados reais, com links que você segue, é mais segura que um pedido respondido de memória."
- Proposta: "Uma busca ancorada em resultados reais, com links que levam às fontes, é mais segura que um pedido respondido de memória."

#### 8. (linha 49) corrigir
- Original: "…não um arquivo de regras na sua pasta — o `CLAUDE.md` chega com o Cowork e o Code (Cap. 23)."
- Proposta: "…não um arquivo de regras numa pasta do computador — o `CLAUDE.md` chega com o Cowork e o Code (Cap. 23)."

#### 9. (linha 49) corrigir
- Original: "Quando você quer que o agente não fale sobre os arquivos, e sim trabalhe neles — abra, edite, gere, execute —, cruzou a fronteira para o Cowork."
- Proposta: "Pedir que o agente não fale sobre os arquivos, e sim trabalhe neles — abra, edite, gere, execute —, cruza a fronteira para o Cowork."
  (Elimina também a abertura "Quando…".)

---

## capitulos/p4-programar/20-por-que-o-terminal.qmd

#### 1. (linha 12) manter (3ª pessoa) — título "## A aba Code e sua relação com o Cowork": "sua" = da aba. (Esqueleto; sem prosa.)

---

## capitulos/p4-programar/24-mcp-e-dados.qmd

#### 1. (linha 9) corrigir
- Original: "Escrever esse programa é trabalho de quem programa — e é o que você delega ao Code."
- Proposta: "Escrever esse programa é trabalho de quem programa — e é o que se delega ao Code."

#### 2. (linha 11) corrigir — 4 ocorrências
- Original: "A primeira é a credencial do Google, que só você obtém: ela depende da sua conta, da sua autorização, dos seus cliques no navegador."
- Proposta: "A primeira é a credencial do Google, que só o usuário obtém: ela depende da conta, da autorização, dos cliques no navegador."

#### 3. (linha 11) corrigir — 2 ocorrências
- Original: "Você não programou nada; o Claude gravou cerca de cem linhas de código num arquivo, rodou esse arquivo e o conectou ao Code. O código existe, está no disco e roda — apenas não passou pelas suas mãos."
- Proposta: "O usuário não programou nada; o Claude gravou cerca de cem linhas de código num arquivo, rodou esse arquivo e o conectou ao Code. O código existe, está no disco e roda — apenas não passou pelas mãos de quem pediu."

#### 4. (linha 13) corrigir — 2 ocorrências
- Original: "Você cria um "projeto" no Google Cloud — uma caixa de organização dentro do site, sem arquivo algum no seu computador —, ativa a API do Forms…"
- Proposta: "O usuário cria um "projeto" no Google Cloud — uma caixa de organização dentro do site, sem arquivo algum no computador —, ativa a API do Forms…"

#### 5. (linha 13) corrigir
- Original: "o agente o usa, uma única vez, para abrir a janela em que você concede a permissão."
- Proposta: "o agente o usa, uma única vez, para abrir a janela em que se concede a permissão."

#### 6. (linha 17) corrigir
- Original: "…nascem não publicados: você os edita pelo link, mas precisa publicá-los para receber respostas"
- Proposta: "…nascem não publicados: o link permite editá-los, mas é preciso publicá-los para receber respostas"

#### 7. (linha 21) corrigir — 2 ocorrências + imperativos
- Original: "O arquivo de credenciais e o *refresh token* dão acesso à sua conta na medida das permissões concedidas. Ficam no seu computador, não num repositório: mantenha-os fora do controle de versão — uma linha no `.gitignore` basta — e não os compartilhe."
- Proposta: "O arquivo de credenciais e o *refresh token* dão acesso à conta na medida das permissões concedidas. Ficam no computador do usuário, não num repositório: devem ficar fora do controle de versão — uma linha no `.gitignore` basta — e não ser compartilhados."

---

## capitulos/p4-programar/25-claude-code-no-editor.qmd

#### 1. (linha 16) corrigir — título de seção (esqueleto)
- Original: "## Escolhendo o seu ambiente"
- Proposta: "## A escolha do ambiente"

---

## capitulos/p5-pratica-responsavel/28-etica-privacidade-custos.qmd

#### 1. (linha 11) manter (3ª pessoa) — título "## Vieses e seus efeitos no trabalho acadêmico": "seus" = dos vieses. (Esqueleto.)

---

## apendices/apendice-f-verbos-do-spinner.qmd

#### 1. (linha 8) corrigir — título de callout
- Original: "## Você pode mudá-los"
- Proposta: "## É possível mudá-los"
