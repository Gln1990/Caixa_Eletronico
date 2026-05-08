# 🏧 Simulação de Caixa Eletrônico (ATM) - Java

Este projeto consiste em um sistema de **Caixa Eletrônico** desenvolvido em Java, focado em lógica de algoritmos para saque e gestão de estoque de cédulas. O sistema implementa regras de negócio reais, como a trava de segurança para restos de valores impossíveis (R$ 1 e R$ 3) e o cálculo inteligente para notas de R$ 5 e R$ 2.

## 🚀 Funcionalidades

- **Saque Inteligente**: Algoritmo que prioriza notas maiores, mas ajusta a entrega para garantir que valores ímpares (como 11, 21, 31) possam ser sacados usando notas de R$ 5 e R$ 2.
- **Gestão de Inventário**: Controle em tempo real do estoque de notas (R$ 100, 50, 20, 10, 5 e 2).
- **Reposição de Cédulas**: Função para operadores abastecerem o caixa com quantidades específicas de cada nota.
- **Relatórios Detalhados**: Emissão de relatório de cédulas restantes e monitoramento do total sacado durante a sessão.
- **Cota Mínima**: Sistema de segurança que impede saques caso o valor total no caixa esteja abaixo de um limite definido.

## 🛠️ Tecnologias e Ferramentas

<table>
  <tr>
    <th bgcolor="#222" align="center"><font color="#58a6ff">Linguagem & Framework</font></th>
    <th bgcolor="#222" align="center"><font color="#58a6ff">Ambiente & Ferramentas</font></th>
  </tr>
  <tr>
    <td align="center" valign="top">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/java/java-original.svg" width="50" height="50" alt="Java" />
      <br>Java (Swing / AWT)
    </td>
    <td align="center" valign="top">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/eclipse/eclipse-original.svg" width="50" height="50" alt="Eclipse" />
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vscode/vscode-original.svg" width="50" height="50" alt="VS Code" />
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/git/git-original.svg" width="50" height="50" alt="Git" />
      <br>Eclipse | VS Code | Git
    </td>
  </tr>
</table>

## 🧠 Conceitos de ADS Aplicados

Neste desenvolvimento, foram aplicados conceitos fundamentais de Engenharia de Software:

1. **Interfaces**: Implementação da interface `ICaixaEletronico`, garantindo o cumprimento do contrato de métodos.
2. **Matrizes (Arrays Multidimensionais)**: Uso de `int[][] estoqueCedulas` para organizar a relação entre valor da nota e quantidade em estoque.
3. **Algoritmos Gulosos (Greedy Algorithms)**: Lógica de saque que tenta resolver o problema da melhor forma local (notas maiores) com correções para restrições globais.
4. **Encapsulamento**: Uso de modificadores `private` e métodos `get/set` para proteger o estado interno do caixa.
5. **Interface Gráfica (GUI)**: Utilização de `JOptionPane` e `EventQueue` para interação com o usuário final.



## 📝 Regras de Saque Implementadas

O algoritmo possui proteções especiais:
- **Regra do Resto**: Se ao retirar notas de valor alto sobrar R$ 1 ou R$ 3, o sistema recua e retira uma nota a menos para tentar compor o valor com notas menores.
- **Lógica da Nota de R$ 5**: Verificação de paridade para garantir que o resto do saque seja sempre par quando houver necessidade de usar notas de R$ 2.

---
Projeto desenvolvido por **Gln1990** como parte do portfólio de estudante de Análise e Desenvolvimento de Sistemas.
