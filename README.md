💰 Exercicio Conta Bancária
Projeto desenvolvido em Java utilizando Eclipse IDE e Maven, com o objetivo de praticar conceitos de Programação Orientada a Objetos (POO), como encapsulamento, tratamento de exceções e estruturação de pacotes.

🧾 Descrição
O projeto exercicio_conta_bancaria simula operações bancárias básicas realizadas em uma conta, como depósito e saque, respeitando limites e validando o saldo disponível.

O sistema solicita os dados da conta e um valor de saque, executando verificações e exibindo mensagens apropriadas em caso de erro.

🧩 Estrutura do Projeto
exercicio_conta_bancaria/ ├── src/ │ ├── application/ │ │ └── Program.java │ ├── model/ │ │ ├── entities/ │ │ │ └── Account.java │ │ └── exception/ │ │ └── Exception.java ├── pom.xml ├── .project └── README.md

markdown Copy code

⚙️ Classes Principais
🧱 Account (model.entities)
Classe que representa uma conta bancária, com os seguintes atributos:

number — número da conta
holder — nome do titular
balance — saldo atual
withdrawLimit — limite máximo permitido para saque
Métodos principais:
deposit(double amount) — adiciona um valor ao saldo
withdraw(double amount) — realiza o saque, com validações:
O valor não pode ultrapassar o limite de saque
O valor não pode ser maior que o saldo disponível
Caso uma dessas condições ocorra, é lançada uma Exception personalizada
Exemplo de mensagem de erro:
The amount exceeds withdraw limit. (A quantia atingiu o limite de saque).

yaml Copy code

⚠️ Exception (model.exception)
Classe personalizada que herda de RuntimeException.
Responsável por tratar e lançar mensagens específicas de erro durante as operações da conta.

🖥️ Program (application)
Classe principal do programa, responsável por:

Ler os dados de entrada do usuário
Criar uma instância de Account
Realizar a operação de saque
Exibir os dados da conta atualizados ou mensagens de erro
🧮 Exemplo de Execução
Entrada do usuário: Enter account data Number: 1234 Holder: Maria Silva Initial balance: 1000.00 Withdraw limit: 300.00

Enter amount for withdraw: 250.00

markdown Copy code

Saída esperada: Account data: Number: 1234, Holder: Maria Silva, Balance: 750.00.

java Copy code

Caso de erro (exemplo): Enter amount for withdraw: 400.00 Withdraw error: The amount exceeds withdraw limit. (A quantia atingiu o limite de saque).

markdown Copy code

🚀 Como Executar
🧩 Opção 1 — Usando o Eclipse IDE
Importe o projeto no Eclipse:

Vá em File > Import > Existing Projects into Workspace
Selecione a pasta do projeto exercicio_conta_bancaria
Clique em Finish
Execute o programa:

Abra Program.java
Clique com o botão direito → Run As > Java Application
Interaja com o console:

Informe os dados da conta e teste diferentes valores de saque para verificar o tratamento de erros.
💻 Opção 2 — Usando Maven (via Terminal)
⚠️ É necessário ter o Java JDK 8+ e o Maven instalados.

Compile o projeto:
mvn compile
Execute a aplicação:

bash Copy code mvn exec:java -Dexec.mainClass="application.Program" Saída esperada:

yaml Copy code Enter account data Number: 1001 Holder: João Santos Initial balance: 1200.00 Withdraw limit: 500.00

Enter amount for withdraw: 200.00

Account data: Number: 1001, Holder: João Santos, Balance: 1000.00. 📚 Conceitos Aplicados Programação Orientada a Objetos (POO)

Encapsulamento e abstração

Tratamento de exceções (try/catch)

Estrutura de pacotes (application, model.entities, model.exception)

Formatação de saída com String.format

Execução via Eclipse IDE e Maven

💡 Possíveis Melhorias Adicionar opção de depósito via console

Permitir múltiplas operações (menu interativo)

Criar subclasses de Account (ex: SavingsAccount, BusinessAccount)

Implementar persistência de dados (arquivos ou banco de dados)

👨‍💻 Autor Vitor Melo 📧 vitordutra1125.com 🌐 GitHub: Vitor2209
