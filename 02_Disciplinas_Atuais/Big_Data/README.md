# 📊 Big Data

## 📚 Sobre a disciplina

Esta pasta reúne os conteúdos, anotações e materiais estudados na disciplina de **Big Data**.

Um dos conteúdos trabalhados é o **SDD — Spec-Driven Development**, utilizando o **GitHub Spec Kit** e o **GitHub Copilot** para estruturar o desenvolvimento de software com Inteligência Artificial.

---

# 🤖 SDD — Spec-Driven Development

## O que é SDD?

SDD significa **Spec-Driven Development**, ou **Desenvolvimento Orientado por Especificação**.

A ideia central é utilizar a **especificação como fonte da verdade do projeto**.

No SDD:

**Especificação → Planejamento → Implementação → Validação**

O código é tratado como um detalhe da implementação daquilo que foi definido na especificação.

A especificação declara a intenção do projeto e a IA utiliza essa especificação para ajudar na implementação.

---

# 💡 SDD x Vibe Coding

## Vibe Coding

No modelo de Vibe Coding:

**Prompt solto → IA interpreta → código é gerado**

Nesse processo, a IA pode fazer suposições que não correspondem exatamente ao que o desenvolvedor queria.

## SDD

No SDD:

**Especificação clara → IA trabalha contra um contrato → código alinhado à intenção**

O objetivo é reduzir ambiguidades antes da implementação.

---

# 🔄 As quatro fases do SDD

O material apresenta quatro fases principais:

### 1. Especificar — O QUÊ

Define o que o sistema deve fazer.

### 2. Planejar — O COMO

Define como a solução será construída.

### 3. Implementar — CONSTRUIR

O código é desenvolvido de acordo com a especificação e o planejamento.

### 4. Validar — VERIFICAR

O resultado é conferido para verificar se corresponde ao que foi especificado.

Existe uma **revisão humana entre as etapas**.

---

# 🧑‍💻 GitHub Spec Kit

O **GitHub Spec Kit** é um toolkit open-source que estrutura o desenvolvimento com IA em fases explícitas.

Ele transforma o processo do SDD em comandos que podem ser utilizados pelo agente de IA.

O material destaca três características:

- CLI + comandos;
- agnóstico de agente;
- artefatos versionados junto ao código no Git.

O Spec Kit não é um modelo de Inteligência Artificial.

Ele é uma forma de estruturar o processo utilizado pelo agente de IA.

---

# 📄 Artefatos do Spec Kit

O processo trabalha com documentos que permanecem no repositório.

## constitution.md

Define os princípios que devem ser respeitados pelo projeto.

Local:

    .specify/memory/constitution.md

---

## spec.md

Contém a especificação funcional.

Representa principalmente:

**O QUÊ**

Também contém os critérios de aceite.

As especificações das funcionalidades ficam em:

    specs/

---

## plan.md

Representa o planejamento técnico.

Pode conter:

- arquitetura;
- dados;
- contratos;
- decisões técnicas.

Representa principalmente:

**O COMO**

---

## tasks.md

Divide a implementação em tarefas menores e ordenáveis.

---

# 🧩 Comandos do Spec Kit

O fluxo apresentado no material utiliza os seguintes comandos:

    /speckit.constitution

Define os princípios do projeto.

    /speckit.specify

Cria a especificação funcional.

    /speckit.clarify

Procura ambiguidades na especificação.

    /speckit.plan

Cria o planejamento técnico e a arquitetura.

    /speckit.tasks

Divide o projeto em tarefas.

    /speckit.analyze

Verifica a consistência entre os artefatos.

É um comando de análise e não deve alterar o projeto.

    /speckit.implement

Executa as tarefas e gera o código.

Existe também:

    /speckit.checklist

Pode ser utilizado para gerar listas de verificação da qualidade da especificação.

---

# 🔁 Fluxo completo

O fluxo principal apresentado na aula é:

    constitution
          ↓
       specify
          ↓
       clarify
          ↓
         plan
          ↓
        tasks
          ↓
       analyze
          ↓
      implement
          ↓
       validar

A revisão humana acompanha o processo.

---

# 🛠️ Ambiente utilizado

Para acompanhar o exemplo apresentado na aula, são necessários:

- Python 3.11 ou superior;
- uv;
- VS Code;
- GitHub Copilot;
- Git.

O Python é utilizado como base para a CLI do Spec Kit.

O `uv` é utilizado para instalar e executar a CLI `specify`.

O VS Code é utilizado como ambiente de desenvolvimento.

O Git é utilizado para versionar o projeto e seus artefatos.

---

# 💻 Instalação do Spec Kit

No terminal, o material apresenta:

    uv tool install specify-cli \
       --from git+https://github.com/github/spec-kit.git@v0.11.3

Depois:

    specify check

O número da versão pode mudar. O material orienta conferir a tag disponível em Releases.

---

# 🚀 Criando um projeto

Para criar um projeto integrado ao Copilot:

    specify init lista-tarefas --integration copilot

Depois:

    cd lista-tarefas

Também existe uma alternativa utilizando `uvx` sem realizar uma instalação permanente.

---

# 🔎 Verificando a instalação

No VS Code:

1. Abra a pasta do projeto.
2. Utilize **File → Open Folder**.
3. Abra a pasta do projeto e não a pasta pai.
4. No terminal, execute:

    dir .github\prompts

Devem existir arquivos relacionados aos comandos `speckit`.

Depois:

1. Abra o GitHub Copilot Chat.
2. Utilize `Ctrl + Alt + I`.
3. Coloque o Copilot no modo **Agent**.
4. Digite `/`.
5. Verifique se os comandos `/speckit.*` aparecem.

Se os comandos não aparecerem:

- reinicie completamente o VS Code;
- confirme se a pasta correta foi aberta.

---

# 📋 Exemplo da aula — Lista de tarefas

O exemplo utilizado na aula é uma aplicação simples de **lista de tarefas**.

O objetivo do exemplo é demonstrar o fluxo do Spec Kit, e não trabalhar com um domínio complexo.

A aplicação deve permitir:

- adicionar tarefas;
- marcar tarefas como concluídas;
- remover tarefas;
- manter as tarefas depois de recarregar a página;
- mostrar o contador de tarefas pendentes;
- apresentar um estado vazio quando não houver tarefas.

O exemplo utiliza uma página única.

---

# 1️⃣ Constitution

O primeiro passo é definir os princípios do projeto.

Com o Copilot no modo Agent:

    /speckit.constitution

A constituição utilizada no exemplo define um projeto simples para aprendizado, utilizando:

- HTML;
- CSS;
- JavaScript puro;
- sem frameworks;
- sem build;
- funcionamento offline;
- solução direta.

O comando gera:

    .specify/memory/constitution.md

---

# 2️⃣ Specify

Depois é definida a especificação.

Comando:

    /speckit.specify

No exemplo, a especificação descreve uma lista de tarefas de página única capaz de:

- adicionar tarefas;
- marcar tarefas como concluídas;
- remover tarefas;
- manter as tarefas depois de recarregar;
- mostrar contador de pendentes;
- mostrar estado vazio.

Também são definidos não-objetivos:

- sem login;
- sem nuvem.

Neste momento, o foco deve estar no comportamento e na necessidade do sistema.

A tecnologia ainda não é definida.

---

# 3️⃣ Clarify

Depois da especificação é feita a etapa de esclarecimento.

Comando:

    /speckit.clarify

O agente procura ambiguidades e faz perguntas.

As respostas são incorporadas à especificação.

### Exemplo

Uma possível dúvida apresentada no material é:

O que acontece quando o usuário tenta adicionar uma tarefa vazia?

A decisão apresentada é:

**ignorar e avisar o usuário.**

Essa etapa serve para evitar que requisitos vagos sejam transformados em código incorreto.

---

# 4️⃣ Plan

Depois de esclarecer a especificação, entra o planejamento técnico.

Comando:

    /speckit.plan

No exemplo da aula:

- HTML;
- CSS;
- JavaScript puro;
- sem frameworks;
- tarefas persistidas no `localStorage`;
- um único arquivo `index.html`;
- sem servidor.

O resultado é o planejamento técnico, incluindo arquitetura e decisões técnicas.

---

# 5️⃣ Tasks

Depois do planejamento:

    /speckit.tasks

O projeto é dividido em tarefas menores e ordenáveis.

A ideia é transformar a implementação em pequenos passos.

---

# 6️⃣ Analyze

Depois das tarefas:

    /speckit.analyze

O objetivo é verificar a consistência e a cobertura entre os artefatos.

O `analyze` é utilizado antes da implementação.

Ele ajuda a identificar inconsistências antes que o código seja gerado.

Também pode ser utilizado:

    /speckit.checklist

para gerar listas de qualidade da especificação.

---

# 7️⃣ Implement

Depois das etapas anteriores:

    /speckit.implement

A implementação deve ser feita de forma incremental.

A orientação apresentada no material é:

**uma tarefa por vez.**

Cada incremento deve ser revisado antes de continuar para o próximo.

---

# ✅ Validação

Depois da implementação, o projeto deve ser executado e comparado com a especificação.

No exemplo da lista de tarefas, verificar:

- adicionar tarefa funciona;
- concluir tarefa funciona;
- tarefa concluída aparece riscada;
- remover tarefa funciona;
- recarregar mantém as tarefas;
- contador de pendentes está correto;
- estado vazio aparece.

Se o resultado estiver diferente da intenção:

**voltar para a especificação e reimplementar a partir dela.**

A orientação do material é evitar simplesmente remendar o código diretamente.

---

# 👨‍💻 Humano no Loop

Um dos pontos centrais do SDD apresentado na aula é manter o **humano no loop**.

Isso significa que a IA não deve simplesmente receber um pedido e gerar todo o sistema sem acompanhamento.

Existem momentos de revisão durante o processo.

## Principais pontos de revisão

### Depois do `/speckit.clarify`

Verificar as ambiguidades encontradas e as decisões adicionadas ao `spec.md`.

### Antes do `/speckit.implement`

Executar:

    /speckit.analyze

Também pode ser utilizado:

    /speckit.checklist

### Durante o `/speckit.implement`

Implementar uma tarefa por vez e revisar cada resultado.

---

# 📌 Boas práticas

## 1. Uma tarefa por vez

Durante a implementação, trabalhar com pequenos incrementos.

---

## 2. Não superespecificar

A especificação deve detalhar o suficiente para remover ambiguidades.

Ela não deve simplesmente virar um pseudocódigo.

---

## 3. Revisar cada saída

O código gerado deve ser comparado com a especificação.

---

## 4. Corrigir a especificação

Quando o resultado estiver diferente da intenção:

**corrigir a especificação e não simplesmente o código.**

---

# ⚖️ Quando utilizar o Spec Kit?

Segundo o material, o Spec Kit pode ser interessante para:

- funcionalidades com requisitos reais;
- trabalhos utilizando agentes de IA;
- código que será mantido;
- projetos com colaboração entre várias pessoas.

Pode ser exagero para:

- protótipos descartáveis;
- scripts pequenos e únicos;
- exploração rápida;
- tarefas triviais e óbvias.

A ideia apresentada é utilizar o nível de rigor necessário para remover as ambiguidades do contexto.

---

# 📚 Conceitos importantes

| Conceito | Significado |
|---|---|
| SDD | Spec-Driven Development |
| Specification | Especificação que orienta o desenvolvimento |
| Constitution | Princípios do projeto |
| spec.md | Especificação funcional |
| plan.md | Planejamento técnico |
| tasks.md | Lista de tarefas de implementação |
| clarify | Etapa de esclarecimento |
| analyze | Verificação de consistência |
| implement | Implementação |
| Human in the loop | Participação humana durante o processo |
| Spec Kit | Toolkit para estruturar o desenvolvimento orientado por especificação |
| Copilot Agent | Modo do Copilot utilizado para executar o fluxo |

---

# 📝 Exemplo Template SDD — APP Meu Bolso

Na disciplina também foi disponibilizado o material:

**Exemplo Template SDD - APP Meu Bolso**

A página da disciplina disponibiliza o arquivo:

    MeuBolso_Especificacao_SDD.md

Esse arquivo é apresentado como um recurso separado dentro do ambiente da disciplina.

Como o arquivo Markdown não está incluído diretamente no HTML enviado, seu conteúdo específico não foi reproduzido aqui.

---

# 🧠 O que aprendi

- O que é SDD;
- diferença entre especificação e implementação;
- importância da especificação como fonte da verdade;
- conceito de Human in the Loop;
- funcionamento do GitHub Spec Kit;
- utilização do GitHub Copilot no modo Agent;
- utilização dos comandos `/speckit`;
- criação de `constitution.md`;
- criação de `spec.md`;
- criação de `plan.md`;
- criação de `tasks.md`;
- utilização do `clarify`;
- utilização do `analyze`;
- implementação incremental;
- validação baseada na especificação;
- importância de corrigir a especificação quando a implementação diverge da intenção.

---

# 🔄 Resumo do fluxo

    1. Constitution
       ↓
    2. Specify
       ↓
    3. Clarify
       ↓
    4. Plan
       ↓
    5. Tasks
       ↓
    6. Analyze
       ↓
    7. Implement
       ↓
    8. Validate

**Especificar → Revisar → Planejar → Revisar → Implementar → Validar**

---

# 📖 Material de estudo

- Aula: **SDD na Prática com o GitHub Spec Kit**
- Professor: **Prof. Dan Lopes**
- Instituição: **Centro Universitário de Brasília (CEUB)**
- Tema: **Spec-Driven Development**
- Ferramenta: **GitHub Spec Kit**
- Ambiente: **VS Code + GitHub Copilot**
- Exemplo: **Lista de tarefas**
- Material complementar: **Exemplo Template SDD - APP Meu Bolso**

---

# 📌 Status

- [x] Fundamentos de SDD
- [x] Quatro fases do SDD
- [x] GitHub Spec Kit
- [x] Artefatos do Spec Kit
- [x] Comandos `/speckit`
- [x] Pré-requisitos
- [x] Instalação
- [x] Integração com Copilot
- [x] Exemplo de lista de tarefas
- [x] Constitution
- [x] Specify
- [x] Clarify
- [x] Plan
- [x] Tasks
- [x] Analyze
- [x] Implement
- [x] Validação
- [x] Boas práticas
- [x] Human in the Loop
- [x] Exemplo Template SDD — APP Meu Bolso

---

## 🚀 Em constante evolução

Este README será atualizado conforme novos conteúdos, aulas, atividades e projetos forem estudados na disciplina de Big Data.
