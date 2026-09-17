# 🗃️ Big Data

## 📚 Sobre a disciplina

Espaço destinado à organização dos conteúdos, atividades, anotações, resumos e projetos relacionados à disciplina de Big Data.

---

## 📖 Conteúdo estudado

### SDD na Prática com o GitHub Spec Kit

Material apresentado pelo Prof. Dan Lopes, do Centro Universitário de Brasília (CEUB), sobre a aplicação de **Spec-Driven Development (SDD)** utilizando o **GitHub Spec Kit** e o **GitHub Copilot**.

O conteúdo apresenta uma abordagem de desenvolvimento na qual a especificação funciona como fonte da verdade, orientando a geração do código por meio de etapas estruturadas e com revisão humana. 

---

## 🧠 Principais conceitos

### 🔹 SDD — Spec-Driven Development

No SDD, a especificação define a intenção do projeto e orienta a implementação.

O material apresenta a ideia:

**Especificar → Planejar → Implementar → Validar**

Cada etapa possui um momento de revisão humana.

---

## 🛠️ GitHub Spec Kit

O GitHub Spec Kit é apresentado como um toolkit open-source que estrutura o desenvolvimento com IA em fases explícitas.

Ele utiliza uma CLI e comandos específicos para organizar o processo de desenvolvimento.

Os artefatos ficam versionados junto ao código dentro do repositório Git.

---

## 📄 Principais artefatos

O processo apresentado utiliza documentos que orientam as diferentes etapas:

| Artefato | Função |
|---|---|
| `constitution.md` | Define os princípios do projeto |
| `spec.md` | Define a especificação funcional e os critérios de aceite |
| `plan.md` | Define o plano técnico, arquitetura, dados e contratos |
| `tasks.md` | Divide o projeto em tarefas menores e ordenáveis |

---

## 🔄 Fluxo do Spec Kit

O material apresenta a seguinte sequência:

```text
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
