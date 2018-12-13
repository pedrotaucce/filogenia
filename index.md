## Bem-vindos ao nosso Workshop!

Sejam bem-vindos ao nosso workshop **Noções básicas em softwares para filogenia molecular: do acesso ao GenBank à construção da hipótese filogenética**. A sistemática filogenética é uma disciplina central nas Ciências Biológicas e a modernização dos computadores e algoritmos proporcionou uma revolução nos métodos utilizados em filogenia. Pensando nisso, este minicurso tem por objetivo familiarizar os alunos com alguns dos softwares mais utilizados em filogenia molecular, desde a aquisição de sequências em repositórios públicos até a construção das árvores filogenéticas.

## Pré-requisitos

Noções básicas de sistemática. Como o minicurso visa a familiarização com os softwares, o mesmo não abordará a teoria dos métodos
detalhadamente.

## Quando e onde?

15 e 16 de dezembro de 2018<br>
Universidade Federal de Minas Gerais (UFMG)

## Material a ser levado pelos alunos

Notebook com os programas a serem utilizados previamente instalados (a seguir). Lembre-se de baixar a versão de acordo com o seu sistema operacional!

1. [R](https://vps.fmvz.usp.br/CRAN/)
2. [R Studio](https://www.rstudio.com/products/rstudio/download/#download) (necessita do R previamente instalado)
3. [Mega software](https://www.megasoftware.net/)
4. [MAFFT 7](https://mafft.cbrc.jp/alignment/software/)
5. [SequenceMatrix](https://github.com/gaurav/taxondna/releases/tag/1.8)
6. [PartitionFinder2](https://github.com/brettc/partitionfinder/releases/tag/v2.1.1)
7. [JModelTest2](https://github.com/ddarriba/jmodeltest2/files/157117/jmodeltest-2.1.10.tar.gz)
8. [TNT 1.5](http://www.lillo.org.ar/phylogeny/tnt/)
9. [RAxML 8.2.10](https://github.com/stamatak/standard-RAxML) (baixe a versão *PTHREADS-SSE3, AVX* ou *AVX2*, dependendo da idade do seu processador: *SS3* para os mais velhos e *AVX2* para os mais novos, mais informações no [manual](https://github.com/stamatak/standard-RAxML/raw/master/manual/NewManual.pdf)).
10. [MrBayes 3.2](http://mrbayes.sourceforge.net/download.php)

**MUITO IMPORTANTE** é que vocês tenham o [java](https://www.java.com/pt_BR/download/) e o [python 2.7](https://www.python.org/downloads/) (a maneira mais fácil de instalar este python é instalar o programa [Anaconda](https://www.anaconda.com/download/)). Não é o python 3, tem que ser o **python 2!!!**

## Instrutores

- [Dr. Pedro Taucce](http://www.pedrotaucce.org)<br>
- [Dr. Paulo Pinheiro](http://lattes.cnpq.br/8623318349513480)


## Horário

Cique nos links no quadro abaixo para ver o conteúdo das aulas:

|Dia|Horário|Aula|Conteúdo|
|:---|:---:|:---:|:---:|
|Sábado (15/12) |08:00<br>10:00|Introdução            |- Introdução ao minicurso<br>- Instalação dos softwares nas máquinas dos alunos<br>- [Aquisição de sequências do GenBank através da Plataforma R](https://pedrotaucce.github.io/filogenia/genbank)|
|               |10:00<br>12:00|Construindo a Matriz  |[- Alinhamento: qual software utilizar?<br>- Alinhamento: utilizando o software Muscle implementado no programa MEGA 7<br>- Alinhamento: utilizando o software MAFFT através de linha de comando e servidor online](https://pedrotaucce.github.io/filogenia/alinhamento)<br>- [Concatenamento: programa Sequence Matrix](https://pedrotaucce.github.io/filogenia/sequencematrix)|
|               |14:00<br>16:00|Particionando a Matriz e escolhendo <br>o modelo molecular que mais se encaixa nos dados|[- Particionamento da matriz: PartitionFinder 2<br>- Escolha do melhor modelo: PartitionFinder 2 e jModelTest2](https://pedrotaucce.github.io/filogenia/selecaodemodelos)|
|               |16:00<br>18:00|Construindo a árvore utilizando o <br>critério da máxima parcimônia|[-O que é máxima parcimônia?<br>-Introdução ao programa TNT](https://pedrotaucce.github.io/filogenia/parcimonia)|
|Domingo (16/12)|08:00<br>10:00|Construindo a árvore utilizando o <br>critério da máxima verossimilhança|-O que é máxima verossimilhança<br> - Introdução ao programa RAxML
|               |10:00<br>12:00|Construindo a árvore utilizando <br> inferência Bayesiana|-O que é inferência Bayesiana?<br>-Introdução ao programa MrBayes

## Subiremos o conteúdo do nosso workshop em breve, neste mesmo site!
