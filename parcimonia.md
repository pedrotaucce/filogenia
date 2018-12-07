## TNT - Tree analysis using New Technology

Uma vez que você esteja com suas sequências alinhadas e concatenadas, o próximo passo é abrir o seu dataset em um software de análise filogenética. Uma das opções é o TNT: um software gratuito que lida exclusivamente com o critério da Máxima Parcimônia. Ao abrir o programa, a primeira coisa a se fazer é criar um output file (esse será um arquivo .txt que registrará todas as ações realizadas por você no programa). Sugerimos que salve todos os arquivos de uma análise em um mesmo diretório.

![Fig1](https://github.com/pedrotaucce/filogenia/blob/master/figures/fig1_tnt.png?raw=true)

```
File > Output > Open Output File
```

Feito isso, você deverá agora, antes de abrir seu dataset, decidir como tratará os gaps das suas sequências. Provavelmente, seu alinhamento conterá gaps devido a inserções/deleções prováveis nas diferentes sequências sendo empregadas. Não é nosso objetivo neste curso discutir qual tratamento dar. Basicamente, se você considerar os gaps como “missing data”, um dado gap não contará como um passo transformacional na sua árvore, ou seja, vai contar como 0. Se você tratar os gaps como um 5º estado de transformação (sequências de DNA têm 4 estados: A, C, G, T), um dado gap vai contar como um ou mais passos na sua árvore (vai depender de você pesar ou não este estado caráter). Se você optar por tratar gaps como 5º estado, pode simplesmente abrir sua matriz, pois este é o default do TNT. Se quiser abordá-los como entrada faltante, vá em:

```
Format > Data Format > Read Gaps as Missing
```
![Fig2](https://github.com/pedrotaucce/filogenia/blob/master/figures/fig2tnt.png?raw=true)

Feito isso é hora de abrir sua matriz. Pode-se fazer isso de duas maneiras:

```
File > Open input file
```
![Fig3](https://github.com/pedrotaucce/filogenia/blob/master/figures/fig3tnt.png?raw=true)

Ou ir no Display, no primeiro ícone com uma pasta aberta, com arquivos:

![Fig4](https://github.com/pedrotaucce/filogenia/blob/master/figures/fig4tnt.png?raw=true)

Depois de aberta a matriz, é importante definir sua raiz. Por default, o TNT reconhece o primeiro táxon da matriz como a raiz. Se você pretende usar outro, recomendamos definir antes de rodar sua análise. Vá em:

```
Data > Outgroup taxon
```
![Fig5](https://github.com/pedrotaucce/filogenia/blob/master/figures/fig5tnt.png?raw=true)

Selecione o táxon de interesse e clique em OK. A seguinte mensagem deverá aparecer na última linha do buffer: 
```
Outgroup is taxon XXX – Espécie_qualquer
```
Finalmente agora vamos rodar sua análise. Existem três maneiras básicas de realizar sua busca (estamos aqui fazendo análises sem pesagem de caracteres). Se o seu conjunto de dados possui menos que 25 terminais, recomenda-se fazer uma busca por enumeração implícita (Implicit enumeration). Este método irá analisar todas as possíveis árvores existentes de acordo com o número de terminais da sua matriz e encontrar quais as topologias mais curtas. Porém, a maioria dos datasets hoje em dia lida com mais do que 25 terminais, o que torna o número de árvores possíveis completamente absurdo, e nenhum computador moderno consegue examinar todas possibilidades de árvores existentes com seu conjunto de dados. Isto é um problema NP completo (para mais a respeito Wheeler, 2012).
Para esta situação pode-se fazer buscas tradicionais ou por novas tecnologias. Hoje sabemos que a segunda opção rende maiores resultados, pois foge de ilhas de resultados (para maior discussão a respeito, ver Page, 1993).
Obs.: No caso de datasets extensos, recomenda-se aumentar a capacidade de memoria do programa para armazenar árvores. Assim evita-se que sua busca seja interrompida por saturação de memória. Para isso há dois caminhos:
Na linha de comando (parte inferior da tela do programa) digitar:
```
hold XXXX 
```
onde X é o número de árvores possíveis de se reter. Ou acessar pelo menu:
```
Settings > Memory
```
A seguinte tela aparecerá:

![Fig6](https://github.com/pedrotaucce/filogenia/blob/master/figures/fig6tnt.png?raw=true)

Em Max. Trees (canto superior esquerdo), digite o numero desejado (o programa tem limite de capacidade de acordo com o banco de dados a ser trabalhado.
