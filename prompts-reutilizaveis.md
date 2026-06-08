# 🔁 Prompts Reutilizáveis — Claude Code

> Banco de prompts validados e organizados por categoria para apoiar revisões futuras, aprofundamento de estudos e uso prático do Claude Code.

---

## Como Usar Este Banco de Prompts

Cada prompt usa **variáveis entre colchetes** `[ASSIM]` para indicar onde você deve inserir o conteúdo específico da sua situação. Os prompts foram organizados por **intenção de uso**:

1. [Revisão de Conteúdo](#1-revisão-de-conteúdo)
2. [Aprofundamento Técnico](#2-aprofundamento-técnico)
3. [Aplicação Prática](#3-aplicação-prática)
4. [Solução de Problemas (Troubleshooting)](#4-solução-de-problemas-troubleshooting)
5. [Comparação e Análise Crítica](#5-comparação-e-análise-crítica)
6. [Criação de Conteúdo e Documentação](#6-criação-de-conteúdo-e-documentação)
7. [Aprendizado Ativo e Autoavaliação](#7-aprendizado-ativo-e-autoavaliação)
8. [Uso Direto no Claude Code](#8-uso-direto-no-claude-code)

---

## 1. Revisão de Conteúdo

Use estes prompts para revisar e consolidar o que foi estudado.

---

```
Resuma os principais conceitos sobre [TÓPICO] em no máximo 5 pontos,
priorizando o que é mais importante para um iniciante entender primeiro.
```

---

```
Explique [CONCEITO] como se eu fosse um desenvolvedor com experiência
em [SUA ÁREA ATUAL] mas sem conhecimento prévio de IA agêntica.
```

---

```
Quais são as 3 informações mais contraintuitivas ou surpreendentes
sobre [TÓPICO] que alguém vindo do desenvolvimento tradicional
provavelmente não esperaria?
```

---

```
Crie um resumo estruturado do seguinte conteúdo que estudei,
destacando: (1) conceitos-chave, (2) como eles se relacionam entre si,
e (3) o que é mais importante na prática:

[COLE AQUI O CONTEÚDO QUE VOCÊ QUER RESUMIR]
```

---

```
Qual é a distinção mais importante entre [CONCEITO A] e [CONCEITO B]
no contexto do Claude Code? Dê um exemplo prático de cada um.
```

---

## 2. Aprofundamento Técnico

Use estes prompts quando quiser ir além do básico em um tópico específico.

---

```
Como funciona [MECANISMO TÉCNICO] "por baixo dos panos"?
Explique o processo completo, da entrada à saída.
```

---

```
Quais são os limites e casos extremos de [FUNCIONALIDADE DO CLAUDE CODE]?
Quando ela funciona melhor e quando ela falha?
```

---

```
Como o [CONCEITO] evoluiu nas versões mais recentes do Claude Code?
O que mudou e por quê isso importa para quem está começando agora?
```

---

```
Me explique o Model Context Protocol (MCP) em detalhes:
como ele funciona tecnicamente, quais são os servidores disponíveis,
e como configurar uma integração do zero com [SERVIÇO ESPECÍFICO].
```

---

```
Quais são as melhores práticas para estruturar o arquivo claude.md
para um projeto de [TIPO DE PROJETO]?
Inclua exemplos de seções recomendadas e anti-padrões a evitar.
```

---

```
Como o framework WAT (Workflows, Agent, Tools) se aplica especificamente
para o caso de uso de [OBJETIVO ESPECÍFICO]?
Descreva cada componente com exemplos concretos.
```

---

## 3. Aplicação Prática

Use estes prompts para traduzir o conhecimento em ação.

---

```
Crie um passo a passo detalhado para implementar [TAREFA ESPECÍFICA]
usando Claude Code, incluindo:
- Os comandos necessários no terminal
- O conteúdo do arquivo claude.md para este projeto
- Os possíveis pontos de falha e como lidar com eles
```

---

```
Como eu estruturaria um Agent Team para construir [TIPO DE PRODUTO/SISTEMA]?
Defina os papéis de cada agente, suas responsabilidades e como eles se coordenam.
```

---

```
Quais Skills (arquivos de habilidades) eu precisaria criar para o Claude Code
ser eficiente em projetos de [ÁREA ESPECÍFICA]?
Descreva o conteúdo recomendado para cada uma.
```

---

```
Descreva o workflow ideal para usar Claude Code para criar um MVP de
[TIPO DE PRODUTO] do zero até o primeiro deploy, em etapas sequenciais.
```

---

```
Como eu integraria o Claude Code com [FERRAMENTA/SERVIÇO] via MCP?
Quais são os passos de configuração e as limitações dessa integração?
```

---

```
Crie um template de arquivo claude.md para um projeto de [TIPO DE PROJETO],
incluindo seções para: contexto do projeto, tecnologias utilizadas,
convenções de código, restrições e critérios de conclusão de tarefas.
```

---

## 4. Solução de Problemas (Troubleshooting)

Use estes prompts quando encontrar dificuldades durante o uso.

---

```
Estou tendo o seguinte problema com Claude Code:
[DESCRIÇÃO DETALHADA DO PROBLEMA]

O erro que aparece é:
[MENSAGEM DE ERRO SE HOUVER]

O que pode estar causando isso e como posso resolver?
```

---

```
O Claude Code entrou em loop sem concluir a tarefa de [DESCRIÇÃO DA TAREFA].
Quais são as causas mais prováveis desse comportamento e como interromper
e reiniciar o processo de forma segura?
```

---

```
Estou experimentando "Context Rot" — as respostas estão ficando menos
precisas conforme a sessão avança. Quais estratégias posso usar para
recuperar a qualidade sem perder o progresso feito até agora?
```

---

```
O Claude Code tomou uma decisão inesperada ao executar [DESCRIÇÃO DA AÇÃO].
Como posso entender o raciocínio por trás dessa decisão e ajustar
minhas instruções para prevenir que isso aconteça novamente?
```

---

```
Meu arquivo claude.md está com [NÚMERO] linhas e suspeito que está
causando consumo excessivo de tokens. Como posso refatorá-lo para
manter as informações essenciais usando menos tokens?
```

---

```
Tenho [TIPO DE WORKFLOW] no n8n que quero migrar ou integrar com Claude Code.
Quais são as etapas para auditar esse workflow, identificar o que o Claude
Code pode assumir e o que deve permanecer no n8n?
```

---

## 5. Comparação e Análise Crítica

Use estes prompts para desenvolver pensamento crítico sobre as ferramentas.

---

```
Quando faz mais sentido usar Claude Code em vez de [FERRAMENTA ALTERNATIVA]
para [CASO DE USO ESPECÍFICO]? Liste os critérios de decisão com exemplos.
```

---

```
Quais são as vantagens e limitações do Claude Code em relação a
[FERRAMENTA/ABORDAGEM] para [OBJETIVO ESPECÍFICO]?
Seja específico sobre quando cada um é claramente superior.
```

---

```
Para o cenário de [DESCRIÇÃO DO CASO DE USO], compare as seguintes abordagens:
1. Usar apenas Claude Code
2. Usar apenas [FRAMEWORK TRADICIONAL]
3. Usar os dois em conjunto

Qual é o trade-off de cada opção em termos de custo, complexidade e manutenção?
```

---

```
Quais são as situações em que o Claude Code seria uma escolha errada
ou excessivamente complexa? Quando o simples é melhor?
```

---

```
Como o desenvolvimento agêntico com Claude Code se compara ao desenvolvimento
tradicional em termos de: velocidade de entrega, qualidade do código,
manutenibilidade a longo prazo e curva de aprendizado?
```

---

## 6. Criação de Conteúdo e Documentação

Use estes prompts para produzir materiais de estudo ou documentação de projetos.

---

```
Com base neste conteúdo sobre [TÓPICO], crie:
1. Um resumo executivo em 3 parágrafos
2. Uma lista de 10 conceitos-chave com definições de uma linha
3. Três perguntas frequentes com respostas concisas

[COLE O CONTEÚDO AQUI]
```

---

```
Crie um glossário com os 15 termos mais importantes do seguinte conteúdo,
organizados por categoria temática, com definições claras e exemplos práticos:

[COLE O CONTEÚDO AQUI]
```

---

```
Transforme este conteúdo técnico em uma explicação acessível para
[PÚBLICO-ALVO: ex. empreendedores sem background técnico], sem perder
as informações essenciais:

[COLE O CONTEÚDO AQUI]
```

---

```
Crie um README.md profissional para um projeto de [DESCRIÇÃO DO PROJETO]
que usa Claude Code, incluindo: descrição, pré-requisitos, instalação,
uso básico, exemplos e referências.
```

---

```
Documente o seguinte processo técnico em um formato step-by-step claro,
com atenção especial para os pontos de falha e como o usuário reconhece
que cada etapa foi concluída com sucesso:

[DESCREVA O PROCESSO AQUI]
```

---

## 7. Aprendizado Ativo e Autoavaliação

Use estes prompts para testar e consolidar seu aprendizado.

---

```
Me faça 5 perguntas de múltipla escolha sobre [TÓPICO],
com nível crescente de dificuldade (do básico ao avançado).
Após eu responder cada uma, corrija e explique o raciocínio correto.
```

---

```
Identifique as possíveis lacunas ou equívocos no meu entendimento
sobre [TÓPICO] a partir do seguinte resumo que escrevi:

[SEU RESUMO AQUI]
```

---

```
Quais conceitos de [TÓPICO BÁSICO] são pré-requisitos essenciais para
entender [TÓPICO AVANÇADO]? Crie um mapa de dependências de aprendizado.
```

---

```
Me desafie com um cenário prático: descreva uma situação real onde
eu precisaria usar [CONCEITO/FERRAMENTA] e me peça para explicar
como eu resolveria o problema passo a passo.
```

---

```
Avalie a seguinte abordagem que planejei para [OBJETIVO]:

[DESCREVA SUA ABORDAGEM]

O que está bom? O que poderia ser melhorado? Quais riscos não estou
considerando? Como um especialista em Claude Code abordaria diferente?
```

---

```
Crie um plano de estudos de [NÚMERO] semanas para dominar [TÓPICO/FERRAMENTA],
considerando que já sei [O QUE VOCÊ JÁ SABE] e meu objetivo final é [OBJETIVO].
Inclua recursos recomendados, projetos práticos e marcos de avaliação.
```

---

## 8. Uso Direto no Claude Code

Estes prompts são para usar diretamente no terminal do Claude Code (não no NotebookLM).

---

```
Antes de começar qualquer implementação, analise o projeto e crie um plano
detalhado incluindo: arquitetura proposta, tecnologias recomendadas,
etapas sequenciais, estimativa de complexidade e potenciais riscos.
Aguarde minha aprovação antes de escrever qualquer código.
```

---

```
Implemente [FUNCIONALIDADE] seguindo estas restrições:
- Linguagem/Framework: [ESPECIFIQUE]
- Padrões de código: [ESPECIFIQUE]
- A tarefa estará concluída quando: [CRITÉRIO CLARO DE CONCLUSÃO]
- Não modifique: [ARQUIVOS/PASTAS QUE NÃO DEVEM SER ALTERADOS]
```

---

```
Audite o seguinte workflow e identifique: (1) ineficiências, (2) pontos
de falha, (3) oportunidades de automação com Claude Code, e (4) o que
deveria permanecer no sistema atual:

[DESCREVA OU COLE O WORKFLOW]
```

---

```
Revise o código em [ARQUIVO/PASTA] e forneça um relatório com:
- Bugs identificados (classificados por severidade)
- Code smells e problemas de qualidade
- Sugestões de refatoração com exemplos
- Riscos de segurança
Não faça alterações ainda — apenas o relatório.
```

---

```
Configure o ambiente de desenvolvimento para [TIPO DE PROJETO] do zero,
incluindo: estrutura de pastas, arquivos de configuração essenciais,
dependências necessárias e o arquivo claude.md inicial. Documente
cada decisão tomada.
```

---

## Dicas de Uso Deste Banco

**Para o NotebookLM:** os prompts das seções 1 a 7 funcionam melhor quando você tem fontes carregadas na sessão. Quanto mais contexto as fontes fornecerem, mais precisa será a resposta.

**Para o Claude Code diretamente:** os prompts da seção 8 são otimizados para o terminal. Sempre defina critérios claros de conclusão para evitar loops.

**Iteração é fundamental:** use os prompts como ponto de partida, não como fórmulas fixas. Adapte com base no contexto específico e refine conforme a resposta não atender ao esperado.

**Registre as variações que funcionaram:** quando um prompt adaptado produzir um resultado superior, salve a versão melhorada neste arquivo para uso futuro.
