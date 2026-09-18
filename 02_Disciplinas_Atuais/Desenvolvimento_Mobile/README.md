# 📱 Desenvolvimento Mobile

## 📚 Sobre a disciplina

Esta pasta reúne os conteúdos, atividades, anotações, resumos e projetos relacionados à disciplina de **Desenvolvimento Mobile**.

O primeiro material estudado aborda a execução de um projeto **Expo** em um celular **Android**, utilizando conexão por cabo USB e **ADB**.

---

# 📌 Conteúdo estudado

## 📱 Rodando um projeto Expo no celular Android

O material apresenta o processo para executar um projeto Expo diretamente em um celular Android.

A comunicação entre o computador e o celular pode ser realizada utilizando:

- Cabo USB;
- ADB;
- Expo;
- Metro Bundler.

---

# 🔧 Configuração do celular

Para executar o projeto utilizando cabo USB, é necessário ativar a **Depuração USB** no celular.

O processo apresentado é:

1. Abrir **Configurações**;
2. Entrar em **Sobre o telefone**;
3. Localizar **Número da versão**;
4. Tocar aproximadamente 7 vezes em **Número da versão** para ativar o modo desenvolvedor;
5. Voltar para as configurações;
6. Entrar em **Opções do desenvolvedor**;
7. Ativar **Depuração USB**.

---

# 🔌 Conexão utilizando ADB

Depois de ativar a depuração USB, o celular deve ser conectado ao computador utilizando um cabo USB.

Para verificar se o dispositivo foi reconhecido, é utilizado:

```bash
adb devices
