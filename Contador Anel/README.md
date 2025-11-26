# 🔄 Estudo e Implementação: Contador Anel (Ring Counter)

![Logisim Badge](https://img.shields.io/badge/Tools-Logisim-blue?style=for-the-badge&logo=appveyor)
![Status Badge](https://img.shields.io/badge/Status-Concluído-green?style=for-the-badge)

## 📖 Descrição do Projeto

Este projeto consiste na implementação e análise de um **Contador Anel**. 
O circuito baseia-se num **registrador de deslocamento** (Shift Register) em malha fechada.

[cite_start]O conceito fundamental explorado é a recirculação de dados: ao receber um pulso de entrada, o bit é deslocado pelos Flip-Flops sequencialmente até chegar ao final, onde é reintroduzido no início, formando um ciclo ou "anel" de dados.

## ⚙️ Componentes e Lógica

### Estrutura Principal
* [cite_start]**Flip-Flops:** Utilizados do **Tipo D** para armazenamento e transferência do bit.
* **Controle de Feedback:** A saída do último estágio é conectada à entrada do primeiro.
* **Inicialização:** O circuito possui uma lógica (porta OR) para inserir o bit inicial no sistema.

### Funcionamento
1.  **Inserção:** Um bit é inserido na entrada.
2.  **Deslocamento:** A cada pulso de *clock*, este bit avança para o próximo Flip-Flop.
3.  **Loop:** Ao atingir o último estágio, o bit retorna ao primeiro, repetindo o ciclo indefinidamente.
4.  **Visualização:** Em simulações físicas ou no Tinkercad, LEDs conectados às saídas acendem sequencialmente, visualizando a passagem do bit.


