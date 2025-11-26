# ⚡ Estudo e Implementação: Flip-Flop RS com Clock

![Logisim Badge](https://img.shields.io/badge/Tools-Logisim-blue?style=for-the-badge&logo=appveyor)
![Status Badge](https://img.shields.io/badge/Status-Concluído-green?style=for-the-badge)

## 📖 Descrição do Projeto

Este projeto documenta o estudo prático de **Flip-Flops RS**, focando no comportamento do circuito mediante a introdução de um sinal de **Clock**.

O objetivo foi analisar como o clock controla a mudança de estados, permitindo que o circuito atue como:
* Armazenador e deslocador de dados (Registradores);
* Contador de pulsos e divisor de frequência;
* Controlador de transferência de dados em sistemas digitais.

## 🧠 Conceitos Abordados

### 1. Flip-Flop RS com Clock (Nível)
Diferente do Latch RS básico, este circuito possui uma entrada de controle (Clock) que define quando as saídas podem ser alteradas:
* **Clock = 0:** O estado das saídas (`Q` e `Q'`) se mantém inalterado, ignorando as entradas `S` e `R` (efeito de memória).
* **Clock = 1:** O circuito se comporta como um Flip-Flop RS básico, respondendo às entradas.

### 2. O Estado "Proibido"
Durante a simulação, observou-se que quando `S=1` e `R=1` (com Clock ativo), ambas as saídas vão para nível lógico alto (`1`). Isso é considerado um estado indeterminado ou proibido, pois quebra a lógica de que as saídas devem ser complementares (inversas).

### 3. Flip-Flop de Borda (Edge-Triggered)
Também foi estudado o conceito de disparo por borda. Diferente do acionamento por nível (descrito acima), o Flip-Flop de borda altera seu estado apenas na **transição** do clock (subida ou descida), perdendo a característica de mudar continuamente enquanto o clock está alto.

## 📊 Tabelas Verdade

As simulações validaram as seguintes lógicas de funcionamento:

### Lógica do Clock
| Clock | Comportamento |
| :---: | :--- |
| 0 | Mantém o estado anterior |
| 1 | Atua como RS Básico |

### Tabela Verdade (Quando Clock = 1)
| S (Set) | R (Reset) | Saída (Q) | Estado |
| :---: | :---: | :---: | :--- |
| 0 | 0 | Mantém | Memória |
| 0 | 1 | 0 | Reset |
| 1 | 0 | 1 | Set |
| 1 | 1 | **X** | Indeterminado |

## 🛠️ Exercício Proposto: Implementação com Portas NOR

Como parte do estudo, foi proposto o desafio de esquematizar um **Flip-Flop RS com Clock utilizando apenas portas NOR**.

**Tabela Verdade Obtida (NOR):**

| Clock | S | R | Set | Reset | Q | Q' |
| :---: | :-: | :-: | :-: | :-: | :-: | :-: |
| 0 | x | x | 0 | 0 | Qa | Qa (Mantém) |
| 1 | 0 | 0 | 0 | 0 | 0 | 0 |
| 1 | 1 | 0 | 1 | 0 | 1 | 0 |
| 1 | 0 | 1 | 0 | 1 | 0 | 1 |
| 1 | 1 | 1 | 0 | 0 | 1 | 1 |
