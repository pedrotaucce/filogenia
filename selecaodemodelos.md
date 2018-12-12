# Seleção de modelos e particionamento da matriz

Para os métodos filogenéticos de máxima verossimilhança e inferência Bayesiana, antes de começarmos nossas análises, é necessário escolher o modelo de substituição nucleotídica que mais se encaixa nos nossos dados. Estes modelos descrevem as diferentes probabilidades de mudança de um nucleotídeo para outro ao longo de uma árvore filogenética. O uso de um modelo ou outro pode afetar os resultados de uma análise filogenética, por isso devemos escolher o melhor modelo com muito cuidado! Além disso, modelos mais simples, apesar de serem computacionalmente menos custosos (deixando a análise mais rápida) podem fazer com que um clado pareça mais bem suportado do que ele na verdade é. Quanto mais complexo (*i.e.*, mais parâmetros ele tem) é um modelo molecular, mais computacionalmente custoso ele é. Então, a escolha do modelo molecular é importante porque deve ser uma razão entre custo computacional e adequabilidade do modelo aos dados.

Outra coisa importante é que o genoma não evolui de maneira homogênea, então é interessante que possamos adequar os modelos moleculares a cada uma das partições que formos analisar (normalmente cada um dos genes da nossa análise). Para estimar o modelo de evolução mais adequado aos nossos dados, usaremos os programas [jModelTest2](https://github.com/ddarriba/jmodeltest2/releases) e [PartitionFinder2](https://github.com/brettc/partitionfinder/releases/tag/v2.1.1).

## jModelTest2

O jModelTest2 tem uma versão em linha de comando, normalmente utilizada em clusters e supercompudadores com sistemas operacionais sem interface gráfica e uma versão com interface gráfica (ou GUI, *graphical user interface*). Como vamos utilizar o programa em nossos computadores pessoais, utilizaremos a versão GUI. Primeiramente, vá até o diretório em que descomprimiu o jModelTest2 e abra o arquivo *jModelTest.jar*. A pártir de agora as instruções e imagens serão baseadas no manual do programa, disponível [aqui](https://github.com/ddarriba/jmodeltest2/files/157130/manual.pdf).

Vamos começar pelo nosso fragmento COI. Carregue o arquivo *hylodidae_coi_alinhado.fas*:
```
File > Load DNA alignment
```
Depois, vá até:
```
Analysis > Compute Likelihood Scores
```
E então selecione os modelos a serem computados. Para que gastemos um tempo razoável (poucos minutos), vamos restringir o número de esquemas de substituição para 11. Marque os outros parâmetros como na figura abaixo e depois é só apertar o botão **Compute Likelihoods**. Lembrando que o número de processadores varia conforme o modelo do computador.

![Fig1](https://github.com/pedrotaucce/filogenia/blob/master/figures/fig_01_model.png?raw=true)

Agora que computamos as verossimilhanças, vamos selecionar os modelos estatisticamente. Existem alguns critérios para isto, mas no nosso curso utilizaremos o Bayesian Information Criterion (BIC; Schwarz, 1978). Então vá em:
```
Analysis > Do BIC calculations
```
Uma janela se abrirá, e então aperte o botão **Do BIC calculations**. Os resultados serão mostrados no console. Para ver melhor os resultados, vá em:
```
Results > Show results table
```
O melhor modelo será aquele com menor valor de BIC, no nosso caso, TrN + G + I. Se você quiser, pode salvar os resultados no formato HTML e pode abri-lo com seu navegador. Para isso, vá em:
```
Results > Build HTML log
```
Repita o processo com as sequências de 16S. **Você espera que o resultado seja o mesmo?**

## PartitionFinder2


## Referências

Schwarz GE. (1978). Estimating the dimension of a model. Annals of Statistics, 6: 461–464




