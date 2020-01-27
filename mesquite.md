# Mesquite

O Mesquite é um programa para análises em biologia evolutiva desenvolvido pelos irmãos Wayne Maddison e David Maddison. Sua principal 
função é organizar dados a respeito dos organismos, além de realizar análises comparativas. Este tutorial apresenta apenas o básico para
a construção de uma matriz de caracteres, mas o Mesquite tem uma variedade imensa de ferramentas. Através do seu 
[site](https://www.mesquiteproject.org/) você poderá explorar tudo que o programa pode oferecer. :)

## Instalando o Mesquite
Se você ainda não tem o Mesquite instalado em seu computador, baixe-o no [site oficial](https://www.mesquiteproject.org/).<br> 
Obs: O Mesquite utilizado neste tutorial é a versão 3.01 para Mac. Dependendo da sua versão e sistema operacional, é provável que alguns 
passos sejam diferentes dos apresentados aqui.

## Como fazer uma matriz de caracteres
Ao abrir o Mesquite, irá aparecer uma janela inicial com as informações sobre o programa.
Para criar um novo arquivo, clique em `File >> New`

![Fig1](https://github.com/pedrotaucce/filogenia/blob/master/figures/mesquite1.png?raw=true)

Antes de mais nada, o programa pedirá para você salvar o novo arquivo em algum diretório do seu computador. Em seguida, aparecerá uma 
janela onde você deve inserir o número de terminais (taxa) que terá sua matriz de caracteres (não se preocupe, você poderá adicionar 
ou remover terminais posteriormente). Como estamos interessados em criar uma matriz de caracteres, selecione a opção *Make Character 
Matrix*, e depois aperte *OK*.

![Fig2](https://github.com/pedrotaucce/filogenia/blob/master/figures/mesquite2.png?raw=true)

Em seguida, você deve informar o número e o tipo de caracteres que terá em sua matriz. Observe que existem seis tipos diferentes de 
caracteres: dados categóricos, DNA, proteína, dados contínuos, dados geográficos e dados merísticos. No nosso exemplo, usaremos dados 
categóricos (“Standard Categorical Data”) que são um tipo de caracteres discretos (na maioria das vezes, os dados categóricos são 
morfológicos). Você pode atribuir um nome a sua matriz em *Name of character matrix* (eu escolhi Hylodidae). Veja os diferentes tipos 
de dados no [site](https://www.mesquiteproject.org/Characters%20%26%20Matrices.html#types). 

![Fig3](https://github.com/pedrotaucce/filogenia/blob/master/figures/mesquite3.png?raw=true)

Pronto! Você já tem uma matriz de caracteres na qual você irá inserir seus dados. 

![Fig4](https://github.com/pedrotaucce/filogenia/blob/master/figures/mesquite4.png?raw=true)

Observe que no lado esquerdo há alguns ícones. Os mais importantes para a construção da nossa matriz são os quatro primeiros:<br>

![Icon1](https://github.com/pedrotaucce/filogenia/blob/master/figures/icone1.png?raw=true) Insere os estados de caracteres na matriz;<br>
![Icon2](https://github.com/pedrotaucce/filogenia/blob/master/figures/icone2.png?raw=true) Escreve o nome do táxon ou do caráter;<br>
![Icon3](https://github.com/pedrotaucce/filogenia/blob/master/figures/icone3.png?raw=true) Adiciona colunas, ou seja, adiciona terminais;<br>
![Icon4](https://github.com/pedrotaucce/filogenia/blob/master/figures/icone4.png?raw=true) Adiciona linhas, ou seja, adiciona caracteres.<br>

Agora você já pode incluir as informações sobre seus caracteres e táxons. Para inserir os estados de cada caráter, vá em 
`Matrix >> Edit state name`. Assim, uma nova aba se abrirá (*StatesNames (Hylodidae)*) onde você poderá inserir todas as informações 
sobre caracteres e estados de caracteres. 

![Fig5](https://github.com/pedrotaucce/filogenia/blob/master/figures/mesquite5.png?raw=true)

Em seguida, inicia-se o preenchimento dos estados de caráter presentes em cada táxon.

![Fig6](https://github.com/pedrotaucce/filogenia/blob/master/figures/mesquite6.png?raw=true)

Para uma melhor visualização, é possível colorir as células com cores diferentes para cada estado de caráter. Para isso, vá em 
`Display >> Color Matrix Cells >> Character State`.

![Fig7](https://github.com/pedrotaucce/filogenia/blob/master/figures/mesquite7.png?raw=true)

Uma outra opção de visualização é ter o estado escrito por extenso (ou invés de representado por número). Para isso, vá em 
`Display >> Names >> Show State Names`.

![Fig8](https://github.com/pedrotaucce/filogenia/blob/master/figures/mesquite8.png?raw=true)


## Salvando e exportando sua matriz de caracteres

Lembre que você já criou o arquivo lá no início deste tutorial. É importante ir salvando (um ‘ctr + s’ basta, ou ir em
`File >> Save File`) periodicamente para não perder nenhuma informação ao longo do processo. Não é incomum o Mesquite fechar 
inesperadamente. :(

Após terminar de preencher toda sua matriz, você poderá exportá-la para que possa ser usada em outros programas. O caminho para exportar 
a matriz é `File >> Export`. Uma janela irá se abrir com todas as opções de exportação permitidas pelo Mesquite. Aqui no nosso curso, 
nós iremos exportá-la com a extensão *.tnt* para que possa ser usada no programa TNT, que será utilizado na próxima aula (veja [tutorial 
do TNT](https://pedrotaucce.github.io/filogenia/parcimonia)). O programa irá perguntar se você deseja converter *gap* em *missing*, essa
escolha dependerá dos objetivos da sua análise em TNT, que será melhor abordada na próxima aula. Em uma matriz com dados morfológicos,
o *gap* significa “a estrutura não existe neste terminal, portanto não posso codificar”; ou seja, é como se você tivesse o caráter 
“cor do testículo” para ser codificado em uma fêmea. Já *missing* significa “não sei”, por exemplo, se o testículo do animal macho 
tivesse sido removido previamente. Se você selecionar *tranform gap in missing*, todo ‘gap’ será tratado como se fosse um *missing* 
durante sua análise. 

![Fig9](https://github.com/pedrotaucce/filogenia/blob/master/figures/mesquite9.png?raw=true)


