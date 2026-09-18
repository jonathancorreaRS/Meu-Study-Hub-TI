# 📚 Resumo — SDD na Prática com o GitHub Spec Kit

## 📌 Material da aula

**Tema:** SDD na Prática com o GitHub Spec Kit  
**Professor:** Dan Lopes  
**Instituição:** Centro Universitário de Brasília (CEUB)  
**Ano:** 2026

---

# 1. O que é SDD?

SDD significa **Spec-Driven Development**.

A ideia central apresentada na aula é utilizar a **especificação como fonte da verdade** durante o desenvolvimento.

No SDD:

Especificação clara
        ↓
Planejamento
        ↓
Implementação
        ↓
Validação

O código é tratado como um detalhe de implementação da especificação.

A especificação define a intenção do projeto e orienta a IA durante a geração do código.

---

# 2. SDD x Vibe Coding

O material apresenta uma diferença entre o desenvolvimento baseado em especificação e o chamado Vibe Coding.

## Vibe Coding

Prompt solto
     ↓
IA interpreta
     ↓
Código plausível
     ↓
Possíveis suposições erradas

## SDD

Especificação clara
        ↓
IA trabalha contra um contrato
        ↓
Código alinhado à intenção

A especificação ajuda a reduzir ambiguidades antes que elas cheguem ao código.

---

# 3. As quatro fases do SDD

O ciclo apresentado no material possui quatro fases principais:

## 3.1 Especificar

Define **o que** será desenvolvido.

Nesta etapa é definida a intenção e o comportamento esperado.

---

## 3.2 Planejar

Define **como** o projeto será desenvolvido.

É nesta etapa que entram as decisões técnicas, como arquitetura e tecnologias.

---

## 3.3 Implementar

É a etapa de construção do projeto.

O código é desenvolvido seguindo as especificações e o planejamento.

---

## 3.4 Validar

Verifica se o resultado produzido está de acordo com o que foi especificado.

---

# 4. Revisão humana

Um ponto importante apresentado na aula é a presença do **humano no loop**.

Existe uma revisão entre as etapas do processo.

Especificar
    ↓
Revisão humana
    ↓
Planejar
    ↓
Revisão humana
    ↓
Implementar
    ↓
Revisão humana
    ↓
Validar

A revisão ajuda a identificar problemas antes que eles avancem para as próximas etapas.

---

# 5. O que é o GitHub Spec Kit?

O **GitHub Spec Kit** é apresentado como um toolkit open-source que organiza o desenvolvimento com IA em fases explícitas.

Ele utiliza:

- CLI;
- comandos `/speckit`;
- artefatos versionados no Git;
- integração com agentes de IA.

O material destaca que o Spec Kit não é um modelo de IA.

Ele funciona como um processo que organiza e disciplina o agente de IA utilizado.

---

# 6. Artefatos do processo

O processo cria documentos que orientam as etapas seguintes.

| Arquivo | Função |
|---|---|
| `constitution.md` | Define os princípios do projeto |
| `spec.md` | Define a especificação funcional e critérios de aceite |
| `plan.md` | Define o plano técnico, arquitetura, dados e contratos |
| `tasks.md` | Divide o projeto em tarefas menores |

Esses documentos ficam versionados junto com o código no repositório.

---

# 7. Comandos do Spec Kit

O material apresenta o seguinte fluxo:

/speckit.constitution
        ↓
/speckit.specify
        ↓
/speckit.clarify
        ↓
/speckit.plan
        ↓
/speckit.tasks
        ↓
/speckit.analyze
        ↓
/speckit.implement

---

## 7.1 `/speckit.constitution`

Define os princípios que devem ser respeitados durante o desenvolvimento.

---

## 7.2 `/speckit.specify`

Cria a especificação.

O foco é definir **o que** será desenvolvido, sem decidir inicialmente a tecnologia.

---

## 7.3 `/speckit.clarify`

Procura ambiguidades na especificação.

O agente pode fazer perguntas para esclarecer pontos que não foram definidos.

---

## 7.4 `/speckit.plan`

Cria o plano técnico.

Nesta etapa entram decisões relacionadas à tecnologia, arquitetura e implementação.

---

## 7.5 `/speckit.tasks`

Divide o projeto em tarefas menores e ordenáveis.

---

## 7.6 `/speckit.analyze`

Verifica a consistência e a cobertura entre os artefatos.

É uma etapa de análise antes da implementação.

---

## 7.7 `/speckit.implement`

Executa as tarefas e produz o código.

A recomendação apresentada é implementar uma tarefa por vez e revisar cada incremento.

---

# 8. Ambiente utilizado

O material apresenta os seguintes pré-requisitos:

- Python 3.11+
- `uv`
- VS Code
- GitHub Copilot
- GitHub Copilot Chat
- Git

O GitHub Copilot e o Copilot Chat devem estar instalados e conectados à conta GitHub.

---

# 9. Instalação

A aula apresenta a instalação da CLI do Spec Kit utilizando o `uv`.

Exemplo apresentado:

uv tool install specify \
  --from git+https://github.com/github/spec-kit.git@v0.11.3

Depois:

specify check

Para criar um projeto integrado ao Copilot:

specify init lista-tarefas --integration copilot

Depois:

cd lista-tarefas

---

# 10. Confirmação da instalação

Depois da instalação, é necessário verificar se o ambiente está funcionando.

No VS Code:

File → Open Folder

Deve ser aberta a pasta do projeto.

No terminal:

dir .github\prompts

Devem existir arquivos relacionados aos comandos do Spec Kit.

No Copilot Chat:

Ctrl + Alt + I

O modo deve estar configurado como:

Agent

Depois é possível digitar `/` para verificar os comandos `/speckit`.

---

# 11. Exemplo prático

O exemplo utilizado na aula é uma **lista de tarefas de página única**.

O projeto possui:

- adicionar tarefas;
- marcar tarefas como concluídas;
- remover tarefas;
- manter as tarefas após recarregar a página;
- contador de tarefas pendentes;
- estado vazio.

O exemplo utiliza:

HTML
CSS
JavaScript
localStorage

O projeto funciona no navegador sem servidor.

---

# 12. Exemplo de especificação

A especificação apresentada descreve uma lista de tarefas com funcionalidades de:

Adicionar
    ↓
Concluir
    ↓
Remover

As tarefas devem permanecer após o recarregamento da página.

Também deve existir um contador de tarefas pendentes e um estado vazio.

O exemplo não possui:

- login;
- nuvem.

---

# 13. Planejamento técnico do exemplo

Depois da especificação, o planejamento apresentado utiliza:

- HTML;
- CSS;
- JavaScript puro;
- `localStorage`;
- um único arquivo `index.html`;
- sem servidor.

---

# 14. Portões de revisão

O material destaca três momentos importantes de revisão.

## Portão 1 — Depois do `/speckit.clarify`

Verificar as ambiguidades encontradas e as decisões tomadas.

---

## Portão 2 — Antes do `/speckit.implement`

Executar:

/speckit.analyze

A análise verifica possíveis inconsistências entre os artefatos.

---

## Portão 3 — Durante o `/speckit.implement`

Implementar uma tarefa por vez.

Cada incremento deve ser revisado antes de continuar.

---

# 15. Validação

Depois da implementação, o projeto deve ser executado e comparado com a especificação.

No exemplo apresentado, devem ser verificadas:

- Adicionar tarefa;
- Concluir tarefa;
- Remover tarefa;
- Recarregar e manter as tarefas;
- Contador de pendentes;
- Estado vazio.

Se o resultado estiver diferente da intenção, a orientação apresentada é voltar à especificação e corrigir o processo a partir dela.

---

# 16. Boas práticas

O material apresenta algumas boas práticas:

### ✅ Uma tarefa por vez

Implementar e revisar pequenos incrementos.

### ✅ Não superespecificar

Detalhar apenas o necessário para remover ambiguidades.

### ✅ Revisar cada saída

O código gerado deve ser comparado com a especificação.

### ✅ Corrigir a especificação

Quando a implementação divergir da intenção, a correção deve começar pela especificação.

---

# 17. Quando utilizar o Spec Kit?

Segundo o material, o Spec Kit pode ser utilizado em situações como:

- Features com requisitos reais;
- Trabalhos com agentes de IA;
- Código que será mantido;
- Projetos com colaboração entre várias pessoas.

Pode ser exagero em situações como:

- Protótipos descartáveis;
- Scripts pequenos e únicos;
- Exploração rápida;
- Tarefas triviais e óbvias.

---

# 18. Síntese

O fluxo apresentado pode ser resumido em:

CONSTITUTION
     ↓
SPECIFY
     ↓
CLARIFY
     ↓
PLAN
     ↓
TASKS
     ↓
ANALYZE
     ↓
IMPLEMENT

A principal ideia é utilizar a especificação para orientar o desenvolvimento e manter a revisão humana durante o processo.

---

# 📌 O que aprendi

Com este material, registrei os seguintes conceitos:

- SDD — Spec-Driven Development;
- GitHub Spec Kit;
- Especificação como fonte da verdade;
- Revisão humana;
- Artefatos do processo;
- Comandos `/speckit`;
- GitHub Copilot;
- Desenvolvimento orientado por especificação;
- Processo de especificação, planejamento, implementação e validação.

---

## 📚 Material utilizado

**SDD na Prática com o GitHub Spec Kit**

**Professor:** Dan Lopes  
**Instituição:** Centro Universitário de Brasília (CEUB)  
**Aula prática:** 2026
