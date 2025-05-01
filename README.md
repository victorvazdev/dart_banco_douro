# 🏦 Dart Asynchronism - Banco d'Ouro

Este projeto é um **simulador de operações bancárias** que utiliza programação assíncrona em Dart, com persistência via [GitHub Gists API](https://docs.github.com/en/rest/gists/gists) e comunicação em tempo real com `StreamController`. A aplicação roda em linha de comando e simula ações típicas de um sistema bancário digital.

---

## 🚀 Funcionalidades

- ✅ Criar contas bancárias com tipos e saldo inicial
- 📄 Listar contas existentes
- 🔁 Realizar transações entre contas com cálculo de taxas dinâmicas
- 🧾 Ver histórico completo de transações
- 🧠 Assistente virtual em CLI para interação com o usuário

---

## 📦 Estrutura do Projeto

```
lib/
├── models/             # Account, Transaction
├── services/           # AccountService, TransactionService
├── screens/            # AccountScreen (interface via terminal)
├── helpers/            # Funções de validação e taxas
├── exceptions/         # Exceções customizadas
bin/
└── main.dart           # Ponto de entrada da aplicação
```

---

## ▶️ Como Executar

1. Certifique-se de ter o [Dart SDK](https://dart.dev/get-dart) instalado.
2. Clone o repositório.
3. Crie o arquivo `lib/api_key.dart` com sua chave pessoal do GitHub:

```dart
const String githubApiKey = 'sua_chave_aqui';
```

4. No terminal, execute:

```bash
dart run bin/main.dart
```

---

## 💡 Funcionamento

- A aplicação inicia com a `AccountScreen`, que interage com o usuário por meio de um chatbot em CLI.
- Os dados de contas e transações são lidos e gravados remotamente em um Gist público no GitHub.
- Toda ação gera logs de status utilizando `StreamController<String>`.
- As taxas são dinâmicas de acordo com o tipo de conta e valor da transação.

---

## 🧪 Exemplo de Interação

```
Bom dia! Eu sou Lewis, assistente do Banco d'Ouro!

Como eu posso te ajudar? (Digite o número desejado)
1 - Ver todas sua contas.
2 - Adicionar nova conta.
3 - Executar uma transação.
4 - Obter histório de transações.
5 - Sair
```

---

## 📄 Licença

Projeto licenciado sob a licença MIT.

---

## 👤 Autor

Desenvolvido por Victor Vaz  
🔗 [https://victorvaz.dev](https://victorvaz.dev)
