# Testes de Performance:

**URL:** https://www.blazedemo.com

**Cenário:** Compra de passagem aérea - Passagem comprada com sucesso.

**Critério de Aceitação:** 250 requisições por segundo com um tempo de resposta 90th percentil inferior a 2 segundos.

**Testes:** Teste de Carga e Teste de Pico

**Ferramenta:** Jmeter

Arquitetura do Projeto - buyTicket_BlazeDemo.jmx

    🧪 TestPlan
        └── 📊 View Results Tree
        └── 📊 View Results in Table
        └── 📊 Aggregate Report
              ├─ ⚙️ BlazeDemo (Thread Group)
                  └─ 🥍 Buy Ticket (HTTP Request)

**Como executar os testes:**

1. Faça o clone do projeto
2. Abra o Jmeter
3. Vá em File -> Open -> selecione o arquivo buyTicket_BlazeDemo.jmx
4. Clique em Start

## Teste de Carga:

**Configurações usadas no teste:**

![image](https://github.com/user-attachments/assets/45154d3c-98f5-488c-be75-2be83ba1a27a)

![image](https://github.com/user-attachments/assets/cf1f5940-08e4-4a21-96bc-08fa445ee3e3)

**Resultado:**

![image](https://github.com/user-attachments/assets/02a6f160-82bb-4907-885a-de3023f1e08e)

**Conclusão:** 

90th percentil foi de 3641ms (3,64s), sendo assim NÃO atendeu o critério de aceitação que seria um tempo de resposta inferior a 2s.


## Teste de Pico:

**Configurações usadas no teste:**

![image](https://github.com/user-attachments/assets/b4e8db27-b6a5-4eae-b878-4f3cabb71334)

![image](https://github.com/user-attachments/assets/9016f899-84eb-4688-8ec8-204f50c0d543)

**Resultado:**

![image](https://github.com/user-attachments/assets/7a75633d-a462-468f-8b82-8a1e1b8b0b89)


**Conclusão:**

Com um Pico de 2500 usuários em um período de 10 segundos, o sistema ficou indisponível e com uma taxa de erro de aproximadamente 64% e throughput de aproximadamente 62s.



