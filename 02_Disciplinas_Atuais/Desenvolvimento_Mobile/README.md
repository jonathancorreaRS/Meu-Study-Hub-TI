# 📱 Desenvolvimento Mobile

## 📚 Sobre a disciplina

Este espaço reúne os conteúdos estudados, anotações, atividades, comandos e materiais relacionados à disciplina de **Desenvolvimento Mobile**.

O material estudado apresenta um tutorial sobre como executar um projeto **Expo** em um celular **Android**, utilizando conexão por cabo USB e **ADB**.

---

# 📌 Conteúdo estudado

## 📱 Rodando um Projeto Expo no Celular Android

O material apresenta o processo para executar um projeto Expo diretamente em um celular Android.

A execução utiliza:

- Android
- Cabo USB
- ADB
- Expo
- Metro Bundler

---

# 🔧 1. Ativar a Depuração USB

Antes de conectar o celular ao computador, é necessário ativar a **Depuração USB**.

### Passos

1. Abra **Configurações**.
2. Entre em **Sobre o telefone**.
3. Localize **Número da versão**.
4. Toque aproximadamente 7 vezes sobre **Número da versão** para ativar o modo desenvolvedor.
5. Volte para as configurações.
6. Entre em **Opções do desenvolvedor**.
7. Ative **Depuração USB**.

---

# 🔌 2. Conectar o celular ao computador

Conecte o celular ao computador utilizando um cabo USB.

Depois, abra o terminal e execute:

    adb devices

O comando verifica os dispositivos Android conectados ao computador.

O resultado esperado é semelhante a:

    List of devices attached
    ABC123456789    device

Caso apareça `unauthorized`, desbloqueie o celular e aceite a autorização de depuração USB.

---

# ⚛️ 3. Criar um projeto Expo

Para criar um projeto Expo utilizando JavaScript, execute:

    npx create-expo-app@latest meu-app --template blank

Depois, entre na pasta do projeto:

    cd meu-app

---

# 📂 4. Estrutura básica do projeto

A estrutura apresentada no material é:

    meu-app/
    ├── App.js
    ├── assets/
    ├── package.json
    └── node_modules/

### Principais elementos

**App.js**

É o ponto de entrada do aplicativo.

**assets/**

Pasta utilizada para os arquivos de recursos do projeto.

**package.json**

Arquivo que contém informações e configurações do projeto.

**node_modules/**

Pasta que contém as dependências instaladas do projeto.

---

# 🔗 5. Configurar a comunicação USB

Depois de conectar o celular e criar o projeto, execute:

    adb reverse tcp:8081 tcp:8081

Esse comando permite que o celular se comunique com o servidor de desenvolvimento utilizando a conexão USB.

Dessa forma, não é necessário depender da conexão Wi-Fi para essa comunicação.

---

# ▶️ 6. Iniciar o Expo

Dentro da pasta do projeto, execute:

    npx expo start

O comando inicia o **Metro Bundler**, responsável pelo servidor de desenvolvimento do projeto Expo.

Quando o Metro Bundler estiver iniciado, pressione:

    a

Essa opção abre o projeto no dispositivo Android conectado.

Também é possível iniciar diretamente utilizando:

    npx expo start --android

---

# 🔄 Fluxo completo

O processo estudado pode ser resumido da seguinte maneira:

1. Ativar as **Opções do desenvolvedor** no celular.
2. Ativar a **Depuração USB**.
3. Conectar o celular ao computador através do cabo USB.
4. Executar `adb devices`.
5. Verificar se o dispositivo foi reconhecido.
6. Criar o projeto Expo.
7. Entrar na pasta do projeto.
8. Executar `adb reverse tcp:8081 tcp:8081`.
9. Iniciar o Expo com `npx expo start`.
10. Pressionar `a` para abrir o aplicativo no Android.

---

# 💻 Comandos utilizados

| Comando | Função |
|---|---|
| `adb devices` | Verifica os dispositivos Android conectados |
| `npx create-expo-app@latest meu-app --template blank` | Cria um projeto Expo utilizando JavaScript |
| `cd meu-app` | Entra na pasta do projeto |
| `adb reverse tcp:8081 tcp:8081` | Permite a comunicação do celular com o servidor de desenvolvimento através do USB |
| `npx expo start` | Inicia o Expo e o Metro Bundler |
| `npx expo start --android` | Inicia o Expo diretamente para Android |

---

# 🧠 Conceitos estudados

## ADB

**ADB (Android Debug Bridge)** é utilizado no processo para estabelecer a comunicação entre o computador e o dispositivo Android.

No material, ele é utilizado principalmente para:

- verificar o dispositivo conectado;
- autorizar a comunicação com o celular;
- realizar a comunicação através da porta 8081.

---

## Expo

O **Expo** é utilizado para criar e executar o projeto mobile apresentado no material.

O projeto é criado utilizando:

    npx create-expo-app@latest meu-app --template blank

---

## Metro Bundler

O **Metro Bundler** é iniciado quando o comando do Expo é executado:

    npx expo start

Ele participa do processo de desenvolvimento e execução do projeto Expo no dispositivo.

---

# 📝 Atividade / Material estudado

### Tema

**Rodando um Projeto Expo no Celular Android**

### Conteúdos

- Configuração das opções do desenvolvedor;
- Depuração USB;
- Conexão Android através de USB;
- ADB;
- Criação de projeto Expo;
- Estrutura básica de um projeto Expo;
- Comunicação através da porta 8081;
- Metro Bundler;
- Execução do projeto no Android.

---

# 🎯 Objetivo do estudo

Aprender o processo básico para executar um projeto **Expo** diretamente em um celular **Android**, utilizando conexão USB, ADB e o ambiente de desenvolvimento do Expo.

---

# 📚 Material utilizado

Material de aula:

**Tutorial: Rodando um Projeto Expo no Celular — Android**

Conteúdo relacionado à execução de projetos Expo utilizando cabo USB e ADB.

---

# 📌 Acompanhamento

| Conteúdo | Status |
|---|---|
| Ativar opções do desenvolvedor | ✅ Estudado |
| Ativar depuração USB | ✅ Estudado |
| Verificar dispositivo com ADB | ✅ Estudado |
| Criar projeto Expo | ✅ Estudado |
| Conhecer estrutura do projeto | ✅ Estudado |
| Configurar comunicação USB | ✅ Estudado |
| Iniciar Expo | ✅ Estudado |
| Executar no Android | ✅ Estudado |

---

# 🚀 Em constante evolução

Este espaço será atualizado conforme novos conteúdos, atividades, projetos e conhecimentos forem desenvolvidos durante a disciplina de **Desenvolvimento Mobile**.
