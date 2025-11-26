# 🔢 Estudo e Implementação: Contador de Década (0 a 9)

![Logisim Badge](https://img.shields.io/badge/Tools-Logisim-blue?style=for-the-badge&logo=appveyor)
![Tinkercad Badge](https://img.shields.io/badge/Simulação-Tinkercad-orange?style=for-the-badge)
![Status Badge](https://img.shields.io/badge/Status-Concluído-green?style=for-the-badge)

## 📖 Descrição do Projeto

Este projeto consiste na implementação de um **Contador de Década**, um circuito sequencial assíncrono projetado para realizar a contagem de **0 a 9** (base decimal).

O circuito utiliza lógica binária para contar pulsos de clock e reinicia automaticamente ao atingir o valor 10 ($1010_2$), sendo fundamental para interfaces que utilizam o sistema numérico decimal.

## ⚙️ Componentes e Funcionamento

### Estrutura
* **Flip-Flops JK:** Elementos de memória responsáveis por armazenar os estados da contagem.
* **Contador Assíncrono (Ripple):** O sinal de clock é aplicado apenas ao primeiro Flip-Flop. Nos demais, o clock é derivado da saída invertida do estágio anterior.

### Lógica de Reset (Zerar)
Para garantir que a contagem pare no 9 e retorne ao 0, foi implementada uma lógica de feedback:
1.  **Detecção do 10:** Quando o contador atinge o binário **1010** (decimal 10).
2.  **Porta AND:** Uma porta lógica monitora as saídas dos Flip-Flops. Ao identificar o nível lógico alto nas saídas correspondentes (Q3 e Q2 no contexto do relatório), ela envia um sinal de nível lógico 1.
3.  **Clear (Limpeza):** Esse sinal ativa o pino **CLEAR** de todos os Flip-Flops simultaneamente, zerando o
