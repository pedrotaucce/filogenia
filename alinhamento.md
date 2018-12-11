# Alinhamento

Apesar de muitos sistematas darem pouca importância ao alinhamento e o tratarem apenas como parte do processo para a obtenção de uma árvore filogenética, esta etapa é extremamente importante para a análise filogenética como um todo, pois é a etapa em que definimos a **hipótese de homologia primária** entre as nossas sequências. Em outras palavras, nesta etapa assumimos que as bases que estão alinhadas em uma mesma coluna **divergiram de um mesmo estado ancestral**. Sendo esta uma etapa tão importante, existem vários softwares e algoritmos que são comumente utilizados para alinhar sequências de DNA (e também de aminoácidos, mas não vamos abordar esta parte no curso), como por exemplo [ClustalW](http://www.clustal.org/clustal2/) (Larkin et al., 2007), [T-Coffee](http://www.tcoffee.org/Projects/tcoffee/index.html#DOWNLOAD) (Notredame et al., 2000), [MUSCLE](https://www.drive5.com/muscle/) (Edgard, 2004) e [MAFFT](https://mafft.cbrc.jp/alignment/software/) (Katoh & Standley, 2013). No nosso curso abordaremos somente os dois últimos.

## Muscle (implementado no Mega7)

Voltando ao seu trabalho com a filogenia de Hylodidae do item anterior. Agora que você adquiriu as sequências de 16S rRNA e COI no GenBank você precisa alinhá-las. Para te poupar o trabalho de filtrar o mundo de sequências baixadas, preparamos versões com um exemplar por espécie apenas tanto de <a href="sequencias/hylodidae_16S.fas" download="hylodidae_16S.fas">16S</a> quanto de <a href="sequencias/hylodidae_coi.fas" download="hylodidae_coi.fas">COI</a>. Também adicionamos uma sequência de *Limnomedusa macroglossa* para servir como raiz da sua árvore nas futuras análises.

Vamos primeiro abrir as sequências de COI no software MEGA. Está tudo desalinhado. Selecione todas as sequências (com ctrl + a) e então vá em:
```
Alignment > Align By Muscle
```
Uma tela irá se abrir, onde você poderá mudar alguns parâmetros no algoritmo MUSCLE. Vamos utilizar o default, clique no botão **Compute**. Agora aguarde um pouquinho e pronto! Suas sequências estão alinhadas. 

O COI é um gene codificante, então algo interessante a se fazer é ver se as sequências estão corretas, começando no codon certo, por exemplo. Isso influenciará em etapas posteriores, então é interessante que sempre comecemos no codon 1. Isso também serve para checar se não existem *stop codons* no meio das suas sequências, o que poderia indicar que você sequenciou um pseudogene ou o gene errado.  Após o alinhamento pronto, clique em **Translated Protein Sequences**, e então quando a caixa se abrir com a pergunta *The Current Genetic Code is: Standard. Is this correct?* clique em *No*, como na figura abaixo:

![Fig1](https://github.com/pedrotaucce/filogenia/blob/master/figures/fig_01_al.png?raw=true)

Então outra caixa se abrirá e, já que se trata do fragmento COI de anfíbios marque a opção *Vertebrate mitochondrial*:

![Fig2](https://github.com/pedrotaucce/filogenia/blob/master/figures/fig_02_al.png?raw=true)

Agora é só ver se não há *stop codons* (indicado pelo símbolo \*) em nenhuma das posições. Se houver, provavelmente seu arquivo não começa em uma posição 1 do códon ou o gene que você sequenciou não é o que você queria.

Repita o processo com as sequências de 16S mas, visto que este não é um gene codificante, não faz sentido traduzir as sequências. Observe seu alinhamento: **qual a principal diferença entre este alinhamento e o do COI? Qual dos dois alinhamentos demorou mais para ser concluído? Por que?**

## Referências

Edgar RC. (2004). MUSCLE: multiple sequence alignment with high accuracy and high throughput. Nucleic Acids Research, 32, 1792-1797.<br>
Katoh K, Standley DM. (2013). MAFFT Multiple Sequence Alignment Software Version 7: Improvements in Performance and Usability. Molecular Biology and Evolution 30, 772-780.<br> 
Larkin MA, Blackshields G, Brown NP, Chenna R, McGettigan PA, McWilliam H, Valentin F, Wallace IM, Wilm A, Lopez R, Thompson JD, Gibson TJ, Higgins DG. (2007). Clustal W and Clustal X version 2.0. Bioinformatics, 23, 2947-2948.<br>
Notredame C, Higgins DG, Heringa J. (2000). T-Coffee: A Novel Method for Fast and Accurate Multiple Sequence Alignment. Journal of Molecular Biology, 302,205-217.<br>
