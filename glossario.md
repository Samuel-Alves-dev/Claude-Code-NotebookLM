# 📚 Glossário — Claude Code e Desenvolvimento Agêntico

> Principais conceitos e definições aprendidas durante a pesquisa. Organizado em ordem alfabética por categoria temática.

---

## Como Usar Este Glossário

Os termos estão organizados em **6 categorias temáticas** para facilitar a consulta:

1. [Conceitos Fundamentais do Claude Code](#1-conceitos-fundamentais-do-claude-code)
2. [Arquitetura e Funcionamento](#2-arquitetura-e-funcionamento)
3. [Modelos e Configuração](#3-modelos-e-configuração)
4. [Automação e Integrações](#4-automação-e-integrações)
5. [Desenvolvimento e Deploy](#5-desenvolvimento-e-deploy)
6. [Negócio e Metodologia](#6-negócio-e-metodologia)

---

## 1. Conceitos Fundamentais do Claude Code

### CLI (Command Line Interface)
**Tradução:** Interface de Linha de Comando

Interface textual do computador onde o usuário interage com o sistema digitando comandos — ao contrário de interfaces gráficas com botões e janelas. O Claude Code opera exclusivamente como uma CLI.

**Exemplo de uso:** Ao abrir o terminal do computador e digitar `claude` para iniciar uma sessão, você está usando a CLI do Claude Code.

---

### Claude Code
**Tipo:** Ferramenta / CLI Agêntica

Interface de linha de comando desenvolvida pela Anthropic que vai além da geração de texto: o Claude Code age diretamente no computador, sendo capaz de ler e editar arquivos locais, executar comandos no terminal, depurar código, gerenciar repositórios Git e integrar-se a serviços externos via MCP.

**Diferença crítica:** o Claude no navegador gera texto; o Claude Code age no sistema.

---

### Desenvolvimento Agêntico
**Tipo:** Paradigma de desenvolvimento

Abordagem onde a IA atua como um **agente autônomo** — planejando, executando e iterando — em vez de apenas responder perguntas. O desenvolvedor assume o papel de arquiteto (define a visão e valida resultados) enquanto a IA executa o trabalho técnico.

---

### Loop Agêntico
**Tipo:** Mecanismo de funcionamento

Ciclo contínuo de operação do Claude Code: **Obter contexto → Tomar uma ação → Verificar resultado → Repetir** até que o objetivo seja concluído ou o usuário interrompa o processo.

---

### Self-Healing (Autocorreção)
**Tradução literal:** Autocura

Capacidade exclusiva do Claude Code de, ao encontrar um erro durante a execução, analisar o log de erro de forma autônoma, pesquisar a solução na documentação e corrigir seus próprios scripts ou ferramentas — sem intervenção humana. O processo continua automaticamente após a correção.

**Limitação importante:** o self-healing pleno ocorre principalmente durante sessões supervisionadas. Após o deploy em produção, o comportamento tende a ser determinístico.

---

### Vibe Coding
**Tipo:** Abordagem de desenvolvimento

Modelo de trabalho onde o desenvolvedor atua como **arquiteto**, descrevendo objetivos e intenções em linguagem natural, sem escrever código linha a linha. O Claude Code interpreta a descrição e constrói a implementação técnica correspondente.

**Analogia:** como contratar um engenheiro experiente que você instrui em português — você não precisa saber construir, mas precisa saber o que quer construir.

---

## 2. Arquitetura e Funcionamento

### Agent (Agente)
**No contexto do WAT:** o componente central do framework — o próprio Claude Code atuando como o "cérebro" que interpreta os Workflows, toma decisões e orquestra a execução das Tools.

---

### Agent Team (Time de Agentes)
**Tipo:** Funcionalidade avançada

Configuração onde múltiplos agentes Claude Code trabalham **simultaneamente** em diferentes frentes de um mesmo projeto. Exemplo clássico para SaaS: Agente 1 (Front-end) + Agente 2 (Back-end) + Agente 3 (QA testando os outros dois).

---

### claude.md
**Tipo:** Arquivo de configuração

Arquivo em formato Markdown que funciona como as "instruções permanentes" do Claude Code para um projeto específico. Define contexto, regras, preferências e comportamentos esperados da IA.

**Tamanho ideal:** entre 150 e 200 linhas. Acima disso, os tokens são desperdiçados a cada interação. Use roteamento para arquivos auxiliares quando necessário.

---

### Context Rot (Podridão de Contexto)
**Tradução:** Degradação de Contexto

Fenômeno onde a qualidade das respostas do Claude Code diminui progressivamente à medida que a janela de contexto se aproxima do limite de tokens. Sessões longas com muita informação acumulada produzem respostas menos precisas e confiáveis.

**Como evitar:** compactar ou encerrar a sessão após tarefas grandes; iniciar novas sessões para novos objetivos.

---

### Framework WAT
**Tipo:** Estrutura organizacional

Framework de organização para uso agêntico do Claude Code com três componentes:
- **W — Workflows:** o processo descrito em linguagem natural
- **A — Agent:** o Claude Code como o cérebro decisor
- **T — Tools:** os scripts (geralmente Python) que executam as ações reais

---

### Modo Plano (Plan Mode)
**Tipo:** Funcionalidade

Modo de operação onde o Claude Code elabora e apresenta um **plano de implementação completo** antes de executar qualquer ação. Permite ao usuário revisar a arquitetura proposta, identificar problemas e ajustar a direção antes que qualquer código seja escrito ou arquivo modificado.

**Por que usar:** evita erros de arquitetura que são difíceis de corrigir depois da construção.

---

### Tools (Ferramentas)
**No contexto do WAT:** scripts — geralmente escritos em Python — que executam as ações reais no sistema operacional. São os "braços" do agente: enquanto o Claude Code decide o que fazer (Agent), as Tools executam fisicamente.

---

### Workflows
**No contexto do WAT:** a descrição do processo em linguagem natural. É o "roteiro" que o agente seguirá — com início, meio, fim, condições e resultados esperados claramente definidos.

---

## 3. Modelos e Configuração

### Claude Haiku
Modelo Claude mais rápido e econômico. Ideal para tarefas simples, respostas rápidas e operações que não exigem raciocínio profundo. Recomendado quando o volume de chamadas é alto e o custo importa.

---

### Claude Opus
Modelo Claude de maior capacidade de raciocínio. Recomendado para tarefas complexas que exigem análise profunda, raciocínio em múltiplas etapas ou tomada de decisão em contextos ambíguos. Mais lento e custoso que Haiku e Sonnet.

---

### Claude Sonnet
Modelo Claude de uso geral — equilibra velocidade, custo e qualidade. É o modelo recomendado para a maioria dos casos de uso do Claude Code no dia a dia.

---

### Janela de Contexto
**Tipo:** Conceito técnico de IA

O limite máximo de texto (medido em tokens) que um modelo de IA consegue processar e "lembrar" em uma única sessão. Quando esse limite se aproxima, a qualidade das respostas deteriora (Context Rot). Cada modelo tem um limite diferente.

---

### settings.json
**Tipo:** Arquivo de configuração

Arquivo no formato JSON que armazena as configurações técnicas do Claude Code para um projeto ou ambiente. Inclui preferências de comportamento, permissões e parâmetros de execução.

---

### Skills (Habilidades)
**Tipo:** Módulo de configuração

Arquivos em Markdown que ensinam ao Claude Code como executar tipos específicos de tarefas — como criar interfaces de front-end modernas, escrever documentação técnica ou seguir convenções específicas de código. Funcionam como "manuais de instruções especializados" para o agente.

---

### Tokens
**Tipo:** Unidade de medida de IA

Unidade básica de processamento de linguagem em modelos de IA. Aproximadamente 1 token = 4 caracteres em inglês (ou ~3 em português). O custo de uso da API e o limite da janela de contexto são medidos em tokens.

**Impacto prático:** quanto mais tokens uma sessão consume, maior o custo e maior o risco de Context Rot.

---

## 4. Automação e Integrações

### API (Application Programming Interface)
**Tradução:** Interface de Programação de Aplicações

Mecanismo que permite que dois sistemas de software se comuniquem entre si. O Claude Code usa APIs para interagir com serviços externos (GitHub, Gmail, Google Drive etc.).

---

### Determinístico
**Tipo:** Característica de processo

Processo cujo resultado é sempre o mesmo para as mesmas entradas — previsível, repetível, sem variabilidade. Ferramentas como n8n, Make e Zapier são otimizadas para fluxos determinísticos.

**Oposto:** Não-determinístico (envolve julgamento, variabilidade, criação).

---

### MCP (Model Context Protocol)
**Tradução:** Protocolo de Contexto de Modelo

Protocolo desenvolvido pela Anthropic que funciona como um "conector universal" — permite ao Claude Code integrar-se a dezenas de serviços externos como Gmail, Google Drive, GitHub, Slack, n8n e ferramentas de busca na web. Cada serviço disponível é conectado via um "servidor MCP".

---

### n8n
**Tipo:** Framework de automação (open source)

Ferramenta de automação visual (baseada em nós) para criar fluxos de trabalho entre aplicações. É open source e pode ser hospedado na própria infraestrutura. Complementa o Claude Code: ideal para automações determinísticas em produção.

---

### Não-Determinístico
**Tipo:** Característica de processo

Processo cujo resultado varia conforme o contexto, julgamento e circunstâncias — não é possível prever exatamente o output a partir do input. O Claude Code é a ferramenta indicada para processos não-determinísticos.

---

### Webhook
**Tipo:** Mecanismo de integração

Mecanismo onde um sistema notifica outro automaticamente quando um evento específico ocorre — em vez de um sistema perguntar repetidamente se algo mudou (polling). O sistema A "empurra" a informação para o sistema B assim que o evento acontece.

**Exemplo:** quando um novo lead preenche um formulário, um webhook dispara automaticamente uma ação no CRM.

---

## 5. Desenvolvimento e Deploy

### .env
**Tipo:** Arquivo de configuração segura

Arquivo que armazena variáveis de ambiente — como chaves de API, credenciais e segredos — separadas do código-fonte. Deve **sempre** ser adicionado ao `.gitignore` para não ser enviado a repositórios públicos.

**Por que importa:** colar chaves de API diretamente no código ou no chat é um erro crítico de segurança.

---

### Deploy
**Tipo:** Etapa de desenvolvimento

Processo de colocar uma aplicação em ambiente de produção — tornando-a acessível aos usuários finais. Inclui a transferência do código, configuração do servidor e ativação do serviço.

---

### Git
**Tipo:** Sistema de controle de versão

Ferramenta que registra o histórico de mudanças em um projeto de código, permitindo reverter alterações, trabalhar em paralelo (branches) e colaborar com outros desenvolvedores com segurança.

---

### GitHub
**Tipo:** Plataforma de hospedagem de código

Plataforma online que hospeda repositórios Git e adiciona funcionalidades de colaboração, revisão de código, issues, Actions (automação de CI/CD) e portfólio público de projetos.

---

### Modal
**Tipo:** Plataforma de computação em nuvem

Plataforma para execução de código Python na nuvem de forma escalável — ideal para hospedar o backend e as automações de um SaaS criado com Claude Code.

---

### Trigger.dev
**Tipo:** Plataforma de automação para desenvolvedores

Ferramenta para criar e executar jobs e automações recorrentes na nuvem, com suporte a código TypeScript/JavaScript. Integra-se bem com projetos SaaS criados com Claude Code.

---

### Vercel
**Tipo:** Plataforma de hospedagem front-end

Plataforma especializada em deploy de aplicações front-end (React, Next.js, Vue etc.) com CI/CD automático integrado ao GitHub. Muito utilizada para hospedar o site e a interface de SaaS.

---

### VPS (Virtual Private Server)
**Tradução:** Servidor Privado Virtual

Ambiente de computação em nuvem que simula um servidor dedicado, onde o Claude Code pode ser instalado e executado continuamente — 24 horas por dia, 7 dias por semana — sem depender do computador local do usuário.

---

## 6. Negócio e Metodologia

### Engenharia de Prompt
**Tipo:** Habilidade técnica

Prática de formular perguntas e instruções para modelos de IA de forma estratégica — com clareza, contexto, restrições e critérios de conclusão — para extrair respostas de alta qualidade e relevância. É considerada uma das habilidades mais valiosas no mercado de IA.

**Princípio central:** "garbage in, garbage out" — a qualidade da resposta é proporcional à qualidade da pergunta.

---

### MVP (Minimum Viable Product)
**Tradução:** Produto Mínimo Viável

Versão inicial de um produto com apenas as funcionalidades essenciais para validar a hipótese de negócio com usuários reais — antes de investir no desenvolvimento completo.

---

### SaaS (Software as a Service)
**Tradução:** Software como Serviço

Modelo de negócio onde um software é disponibilizado via internet por assinatura, sem necessidade de instalação local pelo usuário. Exemplos: Slack, Notion, Figma, Netflix.

---

### Scope Creep
**Tradução:** Expansão de Escopo

Fenômeno onde o escopo de um projeto aumenta gradualmente além do que foi acordado inicialmente — geralmente sem ajuste de prazo ou remuneração. Um dos maiores riscos para consultores que vendem soluções com Claude Code.

**Como evitar:** documento de escopo detalhado, acordado e assinado antes do início do projeto.

---

## Índice Rápido (A–Z)

| Termo | Categoria | Seção |
|-------|-----------|-------|
| .env | Desenvolvimento | 5 |
| Agent Team | Arquitetura | 2 |
| API | Automação | 4 |
| Claude Code | Fundamentais | 1 |
| Claude Haiku | Modelos | 3 |
| Claude Opus | Modelos | 3 |
| Claude Sonnet | Modelos | 3 |
| claude.md | Arquitetura | 2 |
| CLI | Fundamentais | 1 |
| Context Rot | Arquitetura | 2 |
| Deploy | Desenvolvimento | 5 |
| Determinístico | Automação | 4 |
| Desenvolvimento Agêntico | Fundamentais | 1 |
| Engenharia de Prompt | Negócio | 6 |
| Framework WAT | Arquitetura | 2 |
| Git | Desenvolvimento | 5 |
| GitHub | Desenvolvimento | 5 |
| Janela de Contexto | Modelos | 3 |
| Loop Agêntico | Fundamentais | 1 |
| MCP | Automação | 4 |
| Modal | Desenvolvimento | 5 |
| Modo Plano | Arquitetura | 2 |
| MVP | Negócio | 6 |
| n8n | Automação | 4 |
| Não-Determinístico | Automação | 4 |
| SaaS | Negócio | 6 |
| Scope Creep | Negócio | 6 |
| Self-Healing | Fundamentais | 1 |
| settings.json | Modelos | 3 |
| Skills | Modelos | 3 |
| Tokens | Modelos | 3 |
| Tools | Arquitetura | 2 |
| Trigger.dev | Desenvolvimento | 5 |
| Vercel | Desenvolvimento | 5 |
| Vibe Coding | Fundamentais | 1 |
| VPS | Desenvolvimento | 5 |
| Webhook | Automação | 4 |
| Workflows | Arquitetura | 2 |
