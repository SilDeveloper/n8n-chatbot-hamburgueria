# 🍔 Chatbot de Hamburgueria — n8n

Um workflow de demonstração que usa um agente de IA para simular o atendimento de uma hamburgueria: apresentar o cardápio, orientar o cliente durante o pedido e organizar a resposta em um arquivo de texto.

## ✨ Como funciona

1. **Recebe a mensagem** pelo Chat Trigger do n8n.
2. **Processa o atendimento** com um agente de IA conectado a um modelo de chat via OpenRouter.
3. **Mantém contexto** usando uma memória de janela curta.
4. **Organiza a resposta** com os dados da conversa.
5. **Gera um arquivo de texto** e o grava no ambiente configurado.

## 🧰 Tecnologias e recursos

- [n8n](https://n8n.io/) — automação do fluxo
- Agente de IA e modelo de chat via OpenRouter
- Memória de conversa
- Expressões do n8n para organizar os dados
- Conversão de texto em arquivo

## 🚀 Como importar

1. Baixe ou clone este repositório.
2. No n8n, importe o arquivo `workflow.json`.
3. No nó **OpenRouter Chat Model**, selecione ou configure sua própria credencial.
4. Confira se o modelo selecionado está disponível para sua conta.
5. Revise o caminho de saída `/data/bot_hamburgueria.txt` e as permissões de escrita do ambiente.
6. Execute um teste com mensagens fictícias antes de usar o workflow em outro contexto.

## 🔐 Segurança

- Este repositório não deve conter chaves de API, tokens, senhas ou dados reais de clientes.
- Configure credenciais diretamente no n8n; não as inclua no JSON exportado.
- O `.gitignore` ajuda a evitar a inclusão acidental de arquivos locais, mas não substitui a revisão do conteúdo antes de cada publicação.
- O workflow sanitizado não inclui o bloco de credenciais nem identificadores específicos da instância original.

## 📌 Observações

- O fluxo grava o arquivo no ambiente onde o n8n está executando; o caminho `/data` depende da configuração desse ambiente.
- O cardápio e a identidade **Brutus Burger** fazem parte do cenário demonstrativo e devem ser adaptados se o workflow for reutilizado.
- Antes de usar em um atendimento real, revise as mensagens, os preços, o tratamento dos pedidos e a forma de armazenamento dos dados.

---

Projeto de estudo com n8n e IA.