# Lista 1

## Inteligência Artificial

### **1.** Defina com suas próprias palavras: (a) inteligência, (b) inteligência artificial, (c) agente, (d) racionalidade, (e) raciocínio lógico

* **Inteligência:** habilidade de aprender e aplicar novos conhecimentos e habilidades.
* **Inteligência artificial:** habilidade de softwares de computador de aprender e aplicar novos conhecimentos e habilidades.
* **Agente:** aquele que age e reage de acordo com o ambiente.
* **Racionalidade:** tendência para entender (compreender) os fatos e/ou ideias em conformidade com a lógica. Escolher a melhor ação a ser executada dada uma situação.
* **Raciocínio lógico:** caminho percorrido para se tomar uma decisão.

### **2.** Ações reflexas (por exemplo, afastar a mão imediatamente ao tocar um objeto muito quente) são racionais? Elas são inteligentes?

Sim, pois não tomar a ação resulta em prejuízos (queimadura). Mas não são inteligentes, pois não é baseada em aplicar conhecimento adquirido.

### **3.** “Computadores não podem ser inteligentes – eles podem fazer apenas o que seus programadores dizem a eles”. Esta última afirmação é verdadeira? A última afirmação implica na primeira?

É verdadeira, computadores só fazem aquilo que são programados para fazer. Não, pois o programador pode ensinar habilidades para tomar decisões e aprender com elas.

### **4.** “Certamente animais não podem ser inteligentes – eles podem fazer apenas o que seus genes dizem a eles”. Esta última afirmação é verdadeira? A última afirmação implica na primeira?

--Todo--

### **5.** Certamente animais, computadores e humanos não podem ser inteligentes – eles podem fazer apenas o que os átomos que os constituem são obrigados a fazer pelas leis da física”. Esta última afirmação é verdadeira? A última afirmação implica na primeira?

--Todo--

## Agentes

### **1.** Para cada uma das seguintes atividades, forneça a descrição PEAS da tarefa a caracterize-a de acordo com as propriedades [Observável/Não observável; Determinístico/Estocástico; Episódico/Sequencial; Estático/Dinâmico; Discreto/Contínuo; Conhecido/Desconhecido]

#### Jogando futebol

|Agente|Performance|Ambiente|Atuadores|Sensores|
|------|-----------|--------|---------|--------|
|Jogadores, juíz|Velocidade, habilidade|Campo, bola, adversário|Chutar, passar bola|Visão, tato

Observável, estocástico, sequencial, dinâmico, contínuo, conhecido.

#### Explorando os oceanos subterrâneos de Titan

|Agente|Performance|Ambiente|Atuadores|Sensores|
|------|-----------|--------|---------|--------|
|Submarino|Seguro, Iluminar|Oceano, vida marinha|Navegar, iluminar|Visão, tato

Não observável, estocástico, sequêncial, dinâmico, contínuo, desconhecido.

#### Comprando livros de IA usados na internet

|Agente|Performance|Ambiente|Atuadores|Sensores|
|------|-----------|--------|---------|--------|
|Comprador|Seguro, confiável|Sites da internet|Navegar páginas, escolher livro mais barato|Leitor de tela

Observável, determinístico, episódico, estático, discreto, desconhecido.

#### Jogando uma partida de tênis

|Agente|Performance|Ambiente|Atuadores|Sensores|
|------|-----------|--------|---------|--------|
|Jogadores, Juíz|Acertar bola dentro da quadra|Quadra, Bola|, sacar, movimentar|Visão, tato

Observável, estocástico, sequencial, dinâmico, contínuo, conhecido.

#### Praticando tênis na (contra a) parede

|Agente|Performance|Ambiente|Atuadores|Sensores|
|------|-----------|--------|---------|--------|
|Jogador|Acertar bola dentro da quadra|Quadra, bola, parede|movimentar|Visão, tato

Observável, determinístico, sequencial, dinâmico, contínuo, conhecido.

#### Praticando salto em altura (atletismo)

|Agente|Performance|Ambiente|Atuadores|Sensores|
|------|-----------|--------|---------|--------|
|Atleta|Saltar o mais longe possível, a partir da marca de salto|Pista de salto|Correr, saltar, cair|Visão, tato

Observável, determinístico, sequencial, estático, contínuo, conhecido.

#### Tricotando um suéter

|Agente|Performance|Ambiente|Atuadores|Sensores|
|------|-----------|--------|---------|--------|
|Pessoa tricotando, |Habilidade|Cadeira, agulhas|tricotar|Visão, tato

Observável, determinístico, sequencial, estático, discreto.

#### Fazendo lances em um leilão

|Agente|Performance|Ambiente|Atuadores|Sensores|
|------|-----------|--------|---------|--------|
|Cliente|Cobrir lançes, saber quando parar|Local do leilão|Efetuar lançe|Visão, preço do lance

Observável, estocástico, episódico, dinâmico, contínuo.

### **2.** Defina os seguintes termos com suas próprias palavras: agente, função de agente, programa de agente, racionalidade, autonomia, agente reativo (reflexivo), agente baseado em modelo, agente baseado em objetivo, agente baseado em utilidade

#### Agente

Um agente é definido pelo ambiente que ele consegue perceber através de seus sensores e as ações que ele pode escolher para atingir um certo objetivo.

#### Função do agente

Entender o ambiente ao seu redor, e executar ações a partir deste entendimento, para chegar a um objetivo final.

#### Programa de agente

Tradução de um agente para linhas de código.

#### Racionalidade

Habilidade de maximizar seu desempenho, em cada tomada de decisão.

#### Autonomia

Habilidade de tomar decisões.

#### Agente reativo

Desenvolve sua inteligência a partir do ambiente, sem modelo estabelecido

#### Agente baseado em modelo

Possui um modelo interno que mapeia o mundo, e pode utilizar estados passados para tomar decisões futuras.

#### Agente baseado em objetivo

Toma suas decisões visando alcançar um objetivo final.

#### Agente baseado em utilidade

Toma suas decisões visando alcançar um objetivo final, levando em conta a probabilidade de sucesso.

### **3.** Implemente um agente reativo (reflexivo) simples para o problema do aspirador de pó automático, considerando o mundo de dois quadriculados (Figura 2.2 do livro) e as especificações da página 38. Simule o ambiente com este agente para todas as possíveis configurações iniciais sujo/limpo e posição do agente. Grave a medida de desempenho para cada configuração e o desempenho médio geral

```python
def reflex(perception)
  loc, status = perception
  if status == "sujo":
    limpa()
  if loc == "A":
    direita()
  else: esquerda()
```

Desempenho: nº de ações limpar() executadas, nº de vezes que A e B estão limpos.

### **4.** Considere uma versão modificada do problema do aspirador de pó automático, no qual a geografia do ambiente – extensão, limites e obstáculos – e as condições iniciais (quadriculados limpos/sujos) são desconhecidos. (Assuma que o agente pode se movimentar para cima, baixo, direita e esquerda)

#### Poderia um agente reativo (reflexivo) simples atuar de forma perfeitamente racional neste ambiente? Explique

Não, pois o ambiente pode possuir deformidades na sua geografia, obstáculos, que simples ações direcionais sem levar em conta estados anteriores não poderia prever. Você também não conhece a extensão total do ambiente.

#### Poderia um agente reativo (reflexivo) simples com função de agente aleatória superar o desempenho de um agente reativo simples? Projete esse agente e meça seu desempenho em vários ambientes

Sim, o desempenho pode ser melhor para passar por obstáculos, mas ainda possuiria um desempenho baixo, pois não faria o caminho ótimo.

```python
def reflex_random(perception)
  loc, status = perception
  if status == "sujo":
    limpa()  
  go_to_random_direction()
```

#### Você poderia projetar um ambiente no qual seu agente de função aleatória teria um desempenho ruim? Mostre os resultados

```
┌───┐   ┌───┐
│ R │   │ o │
├───┤   ├───┼───┐
│ o │   │   │   │
├───┼───┼───┼───┤
│   │   │   │   │
├───┼───┴───┴───┘
│ o │
└───┘
```
Suponha um ambiente com o formato acima e que o robô só possa se deslocar pelos quadrados. Cada ``o`` é um ponto de sujeira que deve ser limpo e o ``R`` é a posição inicial do robô. Se o deslocamento for randômico, há 25% de chance da direção a ser tomada ser um espaço possível para se deslocar e 75% de chance de permanecer parado. Além disso, no terceiro quadrado de baixo para cima, para ir ao outro quadrante da direita em que há sujeira, é necessário escolher a direção para a direita e continuar indo reto (ainda há chance do robô dar meia volta, permanecendo no lado esquerdo do ambiente).

#### Poderia um agente reativo baseado em modelo superar o desempenho de um agente reativo simples? Projete esse agente e meça o desempenho em vários ambientes

Sim. O agente, dado o histórico de ações tomadas, atualiza o estado atual de acordo com as observações feito de seu histórico, possibilitando uma maximização da função desempenho do algoritmo. Para casos em que o ambiente é sequencial (por exemplo, um jogo de xadrez), o algoritmo conseguirá tomar uma ação muito mais eficiente.

## Busca

### **1.** Formule o problema (estado inicial, possíveis ações, modelo de transição, função de objetivo, custo de caminho) para os casos a seguir. Escolha o nível de abstração adequado para a implementação

#### Usando somente 4 cores, você deve colorir um mapa de forma que duas regiões (ou países) adjacentes não tenham a mesma cor

* **Estado Inicial:** mapa sem cores, dividido em n países;
* **Possíveis ações:** verificar cores dos países adjacentes a um país Y, colorir estado com cor X;
* **Modelo de transição:** ( TODO )
* **Função de objetivo:** verificar se todos países estão coloridos sem repetições nos seus adjacentes;
* **Custo de caminho:** Cada vez que um país é pintado, custa 1. O custo total é a soma destes custos até atingir o objetivo;

#### Um macaco de 1 m de altura está em uma sala onde há algumas bananas suspensas a 2,5 m de altura. Ele gostaria de pegar as bananas. A sala contém duas caixas móveis de 1 m de altura, passíveis de serem empilhadas e escaladas

* **Estado Inicial:** caixas em qualquer posição, macaco no chão;
* **Possíveis ações:** verificar altura da pilha de caixas, empilhar caixa;
* **Modelo de transição:** ( TODO )
* **Função de objetivo:** quando a altura das caixas empilhadas somada a altura do macaco forem maior que 2,5m, o objetivo foi atingido;
* **Custo de caminho:** Cada vez que uma caixa é empilhada o custo é 1, o custo total é a soma de todos os custos;

#### Você tem um programa que exibe a mensagem “entrada ilegal” quando este recebe como entrada certo arquivo. Você sabe que o processamento de cada arquivo é independente um do outro. Você quer descobrir qual arquivos são ilegais.

* **Estado Inicial:**

  [ file1, file2, file3, ..., file *n*].  
  Programa esperando os arquivos a serem enviados e **n** arquivos a serem enviados.

* **Possíveis ações:** enviar arquivo, analisar arquivo e exibir mensagem de erro.

* **Modelo de transição:**  
  (i) enviar um dos *n* arquivos  
  (ii) analisar arquivo enviado  
  (iii) exibir mensagem de erro caso arquivo seja ilegal

* **Função de objetivo:** *n* arquivos processados, *m* mensagens de erros apontando quais arquivos são ilegais.

* **Custo de caminho:** Número de arquivos analisados.

#### Você tem 3 jarros que medem 12 L, 8 L e 3 L, e uma torneira. Você pode: (i) completar os jarros com água até a boca, (ii) transferir o conteúdo de um jarro para outro ou (iii) esvaziá-los descartando seu conteúdo. Deseja-se obter uma quantidade de água de exatamente 1 L

* **Estado Inicial:**

  [ x, y, z ] = [ 0, 0, 0 ]  
  Jarros de 12L, 8L e 3L com 0L cada um.

* **Possíveis ações:** Completar jarro, transferir água, esvaziar jarro.

* **Modelo de transição:**  

  (i) completar *x*, *y* ou *z*  
  (ii) gerar [ 12, y, z ], [ x, 8, z ] ou [ x, y, 3 ].  
  (iii) transferir de um jarro **a** para um jarro **b**  
  jarro b = min(a + b, b)  
  jarro a = max(0, (a + b) - max(b))

* **Função de objetivo:** x, y ou z = 1

* **Custo de caminho:** Número de ações

### **2.** O problema dos missionários e canibais é usualmente descrito como a seguir. Três missionários e três canibais encontram-se em um mesma margem de um rio, e possuem ao alcance um barco a remo que pode carregar uma ou duas pessoas. Encontre uma maneira de levar todos para a outra margem do rio sem nunca deixar um grupo de missionários com número de pessoas menor que aquele dos canibais

#### Formule o problema de forma precisa, fazendo somente as distinções necessárias para garantir uma solução válida.  Desenhe o diagrama completo do espaço de estados.

O estado inicial é de todos os missionários e canibais de um lado do rio.

As ações devem ser de levar duas pessoas por viagem para cada lado do rio.

Antes de cada viagem, deve-se analisar se o número de missionários que ficará é maior ou igual o número de canibais.

#### Usando um algoritmo de busca apropriado, implemente e resolva o problema de forma ótima. É uma boa ideia checar estados que se repetem?

--Todo--

#### Por que você acha que pessoas teriam dificuldades em resolver esse problema, dado que o espaço de estados é tão simples?

--Todo--

### **3.** Defina com suas próprias palavras: estado, espaço de estados, árvore de busca, nó, objetivo, ação, modelo de transição e fator de ramificação

**estado:** situação em que se encontra o agente.

**espaço de estados:** grafo onde os nós são estados e as conexões as ações que transformam um estado.

**árvore de busca:** árvore onde a raíz é o estado inicial e os filhos são estados alcançáveis a partir de uma ação.

**nó:** nó de uma árvore

**objetivo:** estado que o agente quer alcançar.

**ação:** algo que o agente escolhe fazer.

**modelo de transição:** dado um estado, retorna uma ação e um estado alcançável.

**fator de ramificação:** número de ações disponíveis para um agente.