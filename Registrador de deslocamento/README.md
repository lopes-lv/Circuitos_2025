# ➡️ Estudo e Implementação: Registrador de Deslocamento (Shift Register)

![Logisim Badge](https://img.shields.io/badge/Tools-Logisim-blue?style=for-the-badge&logo=appveyor)
![Status Badge](https://img.shields.io/badge/Status-Concluído-green?style=for-the-badge)

## 📖 Descrição do Projeto

Este projeto documenta o funcionamento de um **Registrador de Deslocamento**, um componente essencial na eletrônica digital que atua primariamente como uma memória temporária e volátil para dados binários.

A característica definidora deste circuito é a capacidade de **deslocar** dados serialmente: em sincronia com um sinal de clock, os bits armazenados são movidos de uma posição para a próxima.

## ⚙️ Construção e Funcionamento

### Estrutura Base
* [cite_start]**Flip-Flops:** O circuito é construído pela interconexão em série de múltiplos flip-flops, geralmente do **Tipo D**.
* **Armazenamento:** Cada flip-flop armazena 1 bit. [cite_start]O conjunto deles forma o registrador.
* [cite_start]**Escalabilidade:** Embora chips de 4 ou 8 bits sejam comuns, eles podem ser conectados em série para criar registradores maiores (16, 32, 64 bits) conforme a necessidade do sistema.

## 🔀 Tipos e Classificações

O arranjo das conexões define como os dados entram e saem do registrador. Abaixo estão os quatro tipos principais estudados:

| Sigla | Entrada | Saída | Função Principal |
| :---: | :---: | :---: | :--- |
| **SISO** | Série | Série | Atraso de Dados |
| **SIPO** | Série | Paralelo | Conversor Serial para Paralelo  |
| **PISO** | Paralelo | Série | Conversor Paralelo para Serial  |
| **PIPO** | Paralelo | Paralelo | Armazenamento Temporário  |

## 🚀 Aplicações Práticas

A capacidade de mover informação de forma serial torna este componente vital para:

1.  **Conversão de Dados:** Transforma dados seriais (ideais para transmissão com poucos fios) em paralelos (ideais para processamento rápido) e vice-versa.
2.  **Controle de Hardware:** Permite controlar múltiplos dispositivos (como LEDs ou displays de 7 segmentos) utilizando um número reduzido de pinos do processador/microcontrolador.
3.  **Atraso (Delay):** Introduz um atraso de tempo preciso em um sinal digital.

