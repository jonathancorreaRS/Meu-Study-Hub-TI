# 📊 Otimização Aplicada à Ciência de Dados

## 📚 Sobre a disciplina

Este espaço reúne os conteúdos estudados, anotações, atividades e conceitos relacionados à disciplina de **Otimização Aplicada à Ciência de Dados**.

Nesta aula, o conteúdo aborda o caminho completo entre o dado bruto e a tomada de decisão, utilizando **ETL (Extract, Transform, Load)** e técnicas de **otimização aplicada**.

---

# 📌 Aula 03 — Do Dado Bruto à Decisão

## 🎯 Tema da aula

**ETL completo e otimização aplicada — os dados da turma como estudo de caso**

A aula apresenta o processo:

**Extract → Transform → Load → Decidir**

O objetivo é mostrar como dados brutos podem ser transformados em informações úteis para apoiar uma decisão.

---

# 🧠 A pergunta central da aula

Uma das perguntas apresentadas é:

> "Qual informação eu não tenho hoje e precisaria ter para resolver isso de verdade?"

A partir dessa ideia, o conteúdo mostra que a resposta muitas vezes está nos **dados**.

Porém, os dados normalmente não chegam prontos para serem utilizados.

É necessário realizar processos de preparação, limpeza e transformação antes da análise.

---

# 🔄 ETL

ETL representa três etapas principais:

- **Extract (Extrair)**
- **Transform (Transformar)**
- **Load (Carregar)**

Na aula, o processo é ampliado para chegar à etapa de **decisão**.

---

# 1. 📥 Extract — Extração

A primeira etapa é a **extração dos dados**.

Extrair significa trazer os dados da fonte original sem realizar alterações inicialmente.

No estudo de caso da aula, os dados utilizados são respostas objetivas de estudantes da turma, apresentadas de forma anonimizada.

Cada estudante é representado por identificadores como:

- `aluno_01`
- `aluno_02`
- `aluno_03`

Entre as informações utilizadas estão:

- tempo de resposta;
- interesses em áreas;
- dinâmica de aprendizagem preferida;
- conhecimentos anteriores em otimização;
- situação profissional;
- horas de estudo por semana;
- nível de Python;
- bibliotecas utilizadas;
- ferramentas utilizadas;
- conforto com matemática;
- experiência com Machine Learning.

---

# 2. 🧹 Transform — Transformação

A etapa de **Transformação** é responsável por preparar os dados para análise.

O material destaca que o trabalho pesado do processo de dados está principalmente nessa etapa.

Os dados podem apresentar:

- textos diferentes para representar a mesma informação;
- espaços desnecessários;
- informações agrupadas em uma mesma coluna;
- categorias que precisam ser padronizadas;
- valores que precisam ser convertidos;
- informações que precisam ser separadas.

O objetivo é transformar os dados brutos em dados estruturados e prontos para análise.

---

# 🧹 Limpeza dos dados

A limpeza transforma informações desorganizadas em valores que podem ser utilizados em análises.

Entre os procedimentos apresentados estão:

- limpeza de textos;
- padronização de categorias;
- conversão de informações;
- separação de respostas múltiplas;
- criação de variáveis numéricas;
- organização das informações para análise.

Depois da transformação, os dados ficam mais adequados para utilização com ferramentas como **Pandas** e **Matplotlib**.

---

# 3. 📦 Load — Carregamento

Depois da transformação, os dados preparados podem ser carregados para utilização na análise.

No material, o conjunto de dados tratado é salvo como:

`perfil_turma_limpo.csv`

O objetivo é ter uma versão organizada dos dados que possa ser utilizada nas próximas etapas.

---

# 📊 Análise descritiva

Com os dados limpos, a análise passa a ser mais simples.

A aula utiliza informações como:

- nível de Python;
- conforto com matemática;
- horas de estudo por semana;
- interesses da turma;
- situação profissional.

Também são utilizados recursos de contagem e visualização para compreender o perfil dos estudantes.

---

# 📈 Visualização dos dados

Depois da limpeza, os dados podem ser apresentados por meio de gráficos.

Entre as análises apresentadas estão:

- distribuição do nível de Python;
- distribuição do conforto com matemática;
- ranking dos interesses da turma;
- relação entre nível de Python e matemática.

---

# 🔗 Correlação

A aula também apresenta uma análise de correlação entre:

**nível de Python × conforto com matemática**

O valor apresentado no material é:

**0,43**

A interpretação apresentada é de que existe uma associação moderada e positiva entre as duas variáveis dentro dos dados analisados.

Porém, o material ressalta que isso **não significa causalidade**.

Ou seja:

**Correlação é uma pista, não um veredito.**

Uma correlação não permite afirmar que matemática causa habilidade em programação ou o contrário.

---

# 🎯 Do descritivo ao prescritivo

Até esse ponto, a análise é principalmente **descritiva**.

A análise descritiva procura mostrar:

> **O que os dados mostram?**

A otimização passa para uma etapa diferente:

> **O que devemos fazer?**

Essa mudança representa a passagem do **descritivo para o prescritivo**.

---

# 👥 Formação dos grupos

Um dos problemas de decisão utilizados na aula é a formação dos grupos para o trabalho final da disciplina.

O objetivo é distribuir os estudantes em **4 grupos**, utilizando as informações coletadas no diagnóstico da turma.

O modelo procura:

**maximizar a afinidade de interesses entre os integrantes**

ao mesmo tempo em que respeita determinadas regras.

---

# 🧩 Tríade da otimização

O problema é representado por três elementos principais:

| Elemento | Aplicação no problema |
|---|---|
| **Variáveis de decisão** | Definir se o estudante fica no grupo |
| **Função objetivo** | Maximizar a soma dos interesses em comum entre colegas do mesmo grupo |
| **Restrições** | Definir regras para tamanho e composição dos grupos |

---

# 🔢 Variáveis de decisão

As variáveis de decisão representam as escolhas que o modelo precisa fazer.

No problema da aula:

> O estudante `i` fica no grupo `g`?

Essa decisão pode ser representada como:

- sim;
- não.

---

# 🎯 Função objetivo

A função objetivo define aquilo que o modelo deve tentar maximizar ou minimizar.

No problema apresentado:

**Maximizar a soma dos interesses em comum entre os estudantes que pertencem ao mesmo grupo.**

---

# 🚧 Restrições

As restrições definem as regras que precisam ser respeitadas.

No modelo apresentado:

- cada grupo deve ter entre **3 e 4 estudantes**;
- cada grupo deve possuir pelo menos **1 pessoa com conhecimento suficiente em Python**;
- cada grupo pode possuir no máximo **1 pessoa que nunca programou**;
- cada grupo deve possuir pelo menos **1 pessoa confortável com matemática**.

---

# 🤝 Afinidade

A afinidade entre duas pessoas é calculada considerando a quantidade de áreas de interesse que elas possuem em comum.

Quanto maior o número de interesses em comum, maior a afinidade entre as duas pessoas.

A partir dessas informações, o modelo consegue avaliar diferentes possibilidades de composição dos grupos.

---

# ⚙️ Busca pela melhor composição

O material apresenta uma estratégia sistemática para procurar uma boa composição dos grupos.

O processo parte de uma divisão inicial e realiza alterações enquanto encontra possibilidades melhores.

Entre as operações consideradas estão:

- trocar uma pessoa de um grupo com uma pessoa de outro grupo;
- mover uma pessoa de um grupo para outro;
- avaliar se a alteração melhora a pontuação.

---

# ⚖️ Penalização das restrições

O modelo utiliza uma técnica de **penalização de restrições**.

Em vez de simplesmente proibir uma composição que viola uma regra, o modelo aplica uma penalidade muito grande à sua pontuação.

Assim:

**composição irregular → grande penalidade**

**composição regular → pode competir pela melhor pontuação**

Essa técnica está relacionada às **metaheurísticas** estudadas na disciplina.

---

# 🧠 Metaheurísticas

O conteúdo apresenta a ideia de utilizar uma busca sistemática para melhorar uma solução.

A estratégia apresentada procura realizar mudanças na composição dos grupos enquanto essas mudanças melhorarem o resultado.

O material relaciona essa abordagem com técnicas de **metaheurísticas**.

---

# 🏆 Soluções boas e soluções ótimas

A aula diferencia uma solução muito boa de uma solução que possui garantia de ser a melhor possível.

A busca utilizada no exemplo encontra uma solução muito boa, mas não prova que ela é a melhor de todas as combinações existentes.

Para problemas profissionais de otimização, podem ser utilizados **solvers**.

---

# 🐍 PuLP

O material apresenta o **PuLP** como uma biblioteca utilizada em Python para modelagem de problemas de otimização.

A estrutura básica apresentada envolve:

- criação do modelo;
- definição da função objetivo;
- criação das variáveis;
- definição das restrições;
- resolução do modelo.

A ideia principal é que a mesma estrutura continua existindo:

**objetivo + variáveis + restrições**

---

# 🤖 Relação com Machine Learning

A aula mostra que problemas de otimização e Machine Learning possuem uma estrutura semelhante.

| Elemento | Formação de grupos | Treinamento de modelo | Ajuste de hiperparâmetros |
|---|---|---|---|
| **Variáveis** | Quem fica com quem | Pesos do modelo | Profundidade, taxa de aprendizado |
| **Objetivo** | Maximizar afinidade | Minimizar erro | Maximizar desempenho na validação |
| **Restrições** | Tamanho e composição | Tempo, dados e memória | Tempo e capacidade da máquina |

A ideia apresentada é que diferentes problemas podem possuir a mesma estrutura de:

**variáveis → objetivo → restrições**

---

# 🧪 Estressando o modelo

A aula propõe alterar as regras do modelo para observar o comportamento da solução.

### Experimento 1

Exigir **2 pessoas fluentes em Python por grupo**.

A pergunta é:

> Ainda existe solução?

No exemplo apresentado, existem 7 pessoas fluentes e seriam necessárias 8 para colocar 2 em cada um dos 4 grupos.

Portanto, essa configuração seria inviável.

---

### Experimento 2

Alterar a quantidade de grupos.

Exemplo:

`grupos = [1, 2, 3]`

Nesse caso, também é necessário ajustar os tamanhos considerados na função de resolução.

---

### Experimento 3

Remover a regra relacionada aos iniciantes.

A ideia é observar se a afinidade total aumenta e analisar o que pode ser perdido em troca.

---

### Experimento 4

Inverter o objetivo.

Em vez de procurar aumentar a afinidade, modificar a busca para tentar minimizar a afinidade.

Isso permite observar como a função objetivo altera o resultado encontrado pelo modelo.

---

# ❌ Problema inviável

Um modelo pode se tornar inviável quando suas restrições não podem ser satisfeitas simultaneamente.

Isso não significa necessariamente que existe um erro no código.

Pode significar que:

> **As regras definidas não cabem nos dados disponíveis.**

Esse tipo de análise é importante porque permite identificar problemas nas próprias regras antes de continuar o desenvolvimento.

---

# 🔗 ETL + Otimização + Machine Learning

Uma das principais ideias da aula é a relação entre essas etapas.

O fluxo pode ser entendido como:

**Dados brutos**

↓

**ETL**

↓

**Dados limpos**

↓

**Análise**

↓

**Modelo de decisão**

↓

**Otimização**

↓

**Decisão**

---

# 📌 Principais aprendizados

## 1. ETL não é apenas uma etapa burocrática

A transformação dos dados concentra grande parte do trabalho necessário para preparar os dados para análise.

---

## 2. Dados limpos facilitam a análise

Quando os dados são organizados e padronizados, análises e visualizações se tornam mais simples.

---

## 3. Análise descritiva e otimização possuem objetivos diferentes

A análise descritiva ajuda a entender:

**o que aconteceu / como os dados estão**

A otimização busca ajudar a decidir:

**o que fazer**

---

## 4. Objetivo, variáveis e restrições

A tríade utilizada na Aula 02 aparece novamente na implementação:

- **Objetivo**
- **Variáveis de decisão**
- **Restrições**

---

## 5. Muitas restrições podem tornar um problema inviável

Quando existem regras demais ou regras incompatíveis com os dados disponíveis, pode não existir uma solução possível.

---

# 📝 Tarefa para a próxima aula

A tarefa apresentada consiste em escolher uma das áreas mais votadas pela turma e escrever um problema de decisão.

O problema deve conter:

- uma **função objetivo**;
- pelo menos **duas variáveis de decisão**;
- pelo menos **duas restrições**;
- classificação das restrições como **duras (D)** ou **negociáveis (N)**.

A função objetivo deve indicar o que será:

- maximizado; ou
- minimizado.

Também deve indicar a unidade utilizada.

---

# 📚 Conceitos estudados

- ETL
- Extract
- Transform
- Load
- Limpeza de dados
- Padronização de dados
- Análise descritiva
- Correlação
- Otimização
- Problema de decisão
- Variáveis de decisão
- Função objetivo
- Restrições
- Afinidade
- Penalização de restrições
- Metaheurísticas
- Solvers
- PuLP
- Machine Learning
- Problemas inviáveis

---

# 💻 Ferramentas e tecnologias utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook
- CSV
- PuLP

---

# 📊 Material utilizado

### Aula

**Aula 03 — Do Dado Bruto à Decisão**

### Subtítulo

**ETL completo e otimização aplicada — os dados da nossa turma como estudo de caso**

### Disciplina

**Otimização Aplicada à Ciência de Dados**

### Professor

**Prof. MSc. Weslley R.**

---

# 📌 Acompanhamento

| Conteúdo | Status |
|---|---|
| ETL | ✅ Estudado |
| Extract | ✅ Estudado |
| Transform | ✅ Estudado |
| Load | ✅ Estudado |
| Limpeza de dados | ✅ Estudado |
| Análise descritiva | ✅ Estudado |
| Correlação | ✅ Estudado |
| Função objetivo | ✅ Estudado |
| Variáveis de decisão | ✅ Estudado |
| Restrições | ✅ Estudado |
| Formação de grupos | ✅ Estudado |
| Penalização | ✅ Estudado |
| Metaheurísticas | ✅ Estudado |
| PuLP | ✅ Estudado |
| Relação com Machine Learning | ✅ Estudado |
| Problemas inviáveis | ✅ Estudado |

---

# 🚀 Em constante evolução

Este espaço será atualizado conforme novos conteúdos, atividades, exercícios e projetos forem desenvolvidos durante a disciplina de **Otimização Aplicada à Ciência de Dados**.
