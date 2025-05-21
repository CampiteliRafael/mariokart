# 🏁 Corrida de Kart Simples em JavaScript 🏁

Este projeto é uma simulação de uma corrida de kart entre dois personagens icônicos, Mario e Luigi, implementada em JavaScript puro e executada via Node.js. A cada rodada, os jogadores enfrentam diferentes tipos de desafios (Reta, Curva ou Confronto), e seus atributos, combinados com a sorte dos dados, determinam o resultado.

## 🎮 Como Jogar

O jogo é executado em um terminal. Ao iniciar:
1.  A corrida começa com Mario e Luigi, cada um com seus atributos (Velocidade, Manobrabilidade, Poder) e 0 pontos.
2.  A corrida dura 5 rodadas.
3.  Em cada rodada:
    * Um tipo de bloco (Reta, Curva, Confronto) é sorteado aleatoriamente.
    * Ambos os jogadores "rolam um dado".
    * O resultado do dado é somado ao atributo correspondente ao tipo de bloco:
        * **Reta:** Velocidade
        * **Curva:** Manobrabilidade
        * **Confronto:** Poder
    * No bloco "Confronto", o jogador com maior resultado de poder pode fazer o oponente perder um ponto (se o oponente tiver pontos). O resultado do confronto de poder também determina o desempenho na "disputa da rodada".
    * O jogador com o maior valor total na disputa da rodada (considerando o atributo do bloco + dado) ganha 1 ponto.
    * Empates na disputa da rodada não concedem pontos.
4.  Ao final das 5 rodadas, o jogador com mais pontos é declarado o vencedor.

## 🚀 Como Executar

1.  Certifique-se de ter o [Node.js](https://nodejs.org/) instalado.
2.  Salve o código como um arquivo `.js` (por exemplo, `corrida.js`).
3.  Abra um terminal ou prompt de comando.
4.  Navegue até o diretório onde você salvou o arquivo.
5.  Execute o comando: `node corrida.js`

## 💡 Conceitos Fundamentais Aplicados

Este projeto, embora simples, aplica diversos conceitos essenciais da programação e do JavaScript:

1.  **Estrutura de Dados (Objetos):**
    * Os jogadores (`player1`, `player2`) são representados como objetos, cada um contendo seus atributos (`NOME`, `VELOCIDADE`, `MANOBRABILIDADE`, `PODER`, `PONTOS`). Isso demonstra como agrupar dados relacionados de forma lógica.

2.  **Funções para Modularidade:**
    * O código é dividido em funções (`rollDice`, `getRandomBlock`, `logRollResult`, `playRaceEngine`, `declareWinner`, `main`), cada uma com uma responsabilidade específica. Isso torna o código mais organizado, legível e reutilizável.

3.  **Programação Assíncrona (`async/await`):**
    * Embora as operações neste script (como `Math.random()`) sejam síncronas e rápidas, o uso de `async/await` simula a estrutura que seria usada para operações genuinamente assíncronas (ex: chamadas de API, leitura de arquivos). É uma boa prática para entender o fluxo de código assíncrono moderno em JavaScript.

4.  **Lógica Condicional (`if/else if/else`, `switch`):**
    * Usado extensivamente para determinar o tipo de bloco (`switch`), calcular resultados baseados no tipo de bloco (`if/else if`) e determinar vencedores de confrontos e rodadas.

5.  **Loops (`for`):**
    * O loop `for` é usado para controlar o número de rodadas da corrida.

6.  **Geração de Números Aleatórios (`Math.random()`):**
    * Fundamental para a mecânica de sorte do jogo, tanto na rolagem de dados quanto na seleção do tipo de bloco.

7.  **Manipulação do Console (`console.log`):**
    * Utilizado como interface de usuário primária para exibir o progresso do jogo, resultados de dados, e o vencedor final. Demonstra o feedback básico ao usuário.

8.  **Escopo de Variáveis (`let`):**
    * Variáveis como `totalTestSkill1`, `diceResult1` são declaradas com `let` dentro do escopo da rodada, garantindo que sejam reiniciadas a cada nova rodada.

9.  **Função Auto-Invocável (IIFE - Immediately Invoked Function Expression):**
    * A função `main` é envolvida em uma IIFE `(async function main() { ... })();` para iniciar a execução do jogo assim que o script é carregado, permitindo o uso de `await` no nível superior do fluxo principal.

## 🌱 Como um Projeto Simples Como Este é Útil para o Desenvolvimento?

Mesmo um projeto aparentemente simples como esta corrida de kart oferece um valor imenso para o desenvolvimento de um programador:

1.  **Construção de Lógica de Programação:**
    * Traduzir regras de um "jogo" (mesmo que básico) para código funcional exige pensar algoritmicamente, decompor problemas em etapas menores e implementar a lógica de decisão.

2.  **Prática com Fundamentos:**
    * Reforça o entendimento e a aplicação prática de estruturas de controle (loops, condicionais), variáveis, funções e tipos de dados – o alicerce de qualquer linguagem de programação.

3.  **Depuração (Debugging) na Prática:**
    * Ao construir e testar, é quase inevitável encontrar bugs ou comportamentos inesperados (como o problema original de não mostrar o vencedor da rodada consistentemente). Identificar, analisar e corrigir esses erros é uma habilidade crucial e este tipo de projeto oferece um ambiente seguro para praticá-la.

4.  **Organização e Estrutura do Código:**
    * Incentiva a pensar sobre como organizar o código de forma legível e modular. A decisão de criar funções separadas em vez de um único bloco de código monolítico é um passo inicial importante para escrever software manutenível.

5.  **Entendimento de Fluxo de Controle:**
    * Acompanhar como os dados mudam de rodada para rodada, como os pontos são acumulados e como as condições afetam o resultado ajuda a solidificar o entendimento do fluxo de execução de um programa.

6.  **Iteração e Refatoração:**
    * Muitas vezes, a primeira versão de uma funcionalidade pode ser melhorada. Este projeto passou por ajustes (por exemplo, para corrigir a lógica de exibição do vencedor da rodada e as mensagens de log). Esse processo de iterar e refatorar é central no desenvolvimento de software.

7.  **Base para Projetos Mais Complexos:**
    * Os conceitos aqui aplicados são escaláveis. Gerenciar o "estado" dos jogadores, criar um "loop de jogo" (rodadas), e lidar com "eventos" (tipos de bloco) são ideias que se expandem para jogos e aplicações muito mais complexas.

8.  **Confiança e Motivação:**
    * Concluir um projeto funcional, por menor que seja, constrói confiança e fornece motivação para enfrentar desafios maiores. Ver o código ganhar "vida" é gratificante.

Em resumo, projetos como este são excelentes "playgrounds" para solidificar conhecimentos teóricos, praticar a resolução de problemas e desenvolver as habilidades analíticas e de depuração que são indispensáveis para qualquer desenvolvedor de software. Eles transformam conceitos abstratos em resultados tangíveis.

## 🚀 Possíveis Próximas Etapas (Para Evoluir o Projeto)

* Adicionar mais jogadores.
* Criar diferentes "pistas" com sequências de blocos variadas.
* Implementar "itens especiais" que os jogadores podem usar.
* Desenvolver uma interface gráfica simples (talvez com HTML/CSS/JS no navegador, ou bibliotecas como `ncurses` para terminal).
* Permitir que os jogadores escolham seus personagens.

---