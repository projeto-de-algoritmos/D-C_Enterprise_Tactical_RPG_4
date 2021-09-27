# Enterprise Tactical RPG 4

**Número da Lista**: 25<br>
**Conteúdo da Disciplina**: D&C<br>

## Alunos

| Matrícula | Aluno |
| ---------- | -- |
| 15/0058462 |  Davi Antônio da Silva Santos |
| 18/0100840 |  Gabriel Azevedo Batalha |

## Sobre

Um jogo cujo objetivo é sobreviver o maior número de turnos. É uma evolução do
projeto de *Greed*, agora permitindo habilitar animação dos movimentos e com
adição de inimigos *Median*.

## Screenshots

![Menu](https://i.imgur.com/m8vTIQG.png)
Menu

![Jogo em execução em mapa 20x20](https://i.imgur.com/rithhNi.png)
Jogo em execução em mapa 20x20

![Jogo em execução em mapa 16x16](https://i.imgur.com/9Ore9el.png)
Jogo em execução em mapa 16x16

## Instalação 
**Linguagem**: Java<br>
**Framework**: Swing<br>

### Requisitos

- Java JRE 11 ou superior.
  - JDK 11 ou superior exigido para compilar ou desenvolver
- Computador com *mouse*.

## Uso 

Clone o repositório para compilar o projeto ou baixe somente o `.jar` disponível
nas [releases](https://github.com/projeto-de-algoritmos/D-C_Enterprise_Tactical_RPG_4/releases)

Para executar o programa, use
```
java -jar EnterpriseTacticalRPG4.jar
```
O jogo é controlado pelo *mouse*. Há a possibilidade de escolha do tamanho do
mapa até no máximo 30x30 e no mínimo 16x16 posições.

O jogador é um ponto azul na tela e deve fugir dos pontos vermelhos inimigos.
Os quadrados vermelhos são inimigos que seguem o jogador independentemente,
traçando o caminho de menor custo usando o algoritmo de Dijkstra.

Já os círculos vermelhos são um exército que persegue o jogador usando um
algoritmo ganancioso. O exército ganancioso tem um número fixo de casas que
pode movimentar, e escolhe o inimigo que chega mais próximo do jogador no menor
número de casas.

Os semicírculos vermelhos são um exército que persegue o jogador escolhendo
sempre a unidade na mediana dos custos para chegar até o jogador. Esses
inimigos seguem a mesma limitação de custo de movimento por unidade presente
nos inimigos comuns.

As áreas são coloridas conforme os custos para atravessá-las. Regiões verdes
possuem o custo mais baixo, e quanto mais amarelo, mais alto o custo. Regiões
pretas são intransponíveis.

A partida termina quando o jogador é alcançado por qualquer um dos inimigos ou
quando não há movimentos válidos restantes.

## Desenvolvimento

Ao importar o projeto em sua IDE talvez seja necessário retirar o `.jar` gerado
do caminho do projeto. É possível que a IDE tente usar as classes empacotadas
no lugar das que estão definidas no código fonte.

## Outros

Agora é possível escolher se a movimentação dos inimigos e do jogador será
animada. Além disso, foram corrigidos *bugs* referentes ao movimento dos
inimigos no tabuleiro, garantindo agora que dois inimigos não ocupem o mesmo
lugar.

Houve também um trabalho de manutenção para reduzir a duplicação de código
responsável por controlar a lógica do jogo.