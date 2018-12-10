# Aquisição de sequências no GenBank
## O que é o GenBank?

O [GenBank](www.ncbi.nlm.nih.gov/genbank/) é uma base de dados que contem todas as sequências de DNA disponíveis publicamente. Quando você publica um artigo utilizando sequências de DNA, provavelmente você visitou o GenBank para adquirir sequências antes de começar suas análises e muito provavelmente irá acessá-lo depois para depositar as sequências que produziu. Uma funcionalidade muito útil do GenBank é o [BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=blastn&PAGE_TYPE=BlastSearch&LINK_LOC=blasthome), onde você pode pegar uma sequência e comparar com **TODAS** as sequências disponíveis na imensa base de dados do GenBank. É muito útil, por exemplo, para saber se a sequência em questão está contaminada.

## Usando o BLAST

Como dito anteriormente, a ferramenta BLAST compara a sequência desejada com todas as sequências disponíveis no banco de dados do GenBank. Para utilizá-lo, primeiro baixe esta sequência de <a href="sequencias/panthera_onca.fas" download="panthera_onca.fas">onça pintada</a>. Depois, abra-a no bloco de notas, notepad ou programa equivalente. Agora vá até o site do [BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=blastn&PAGE_TYPE=BlastSearch&LINK_LOC=blasthome) e então, copie (ctrl + c) a sequência baixada, e logo depois cole na janela correspondente e então aperte o botão "BLAST", como na figura abaixo:

![Fig1](https://github.com/pedrotaucce/filogenia/blob/master/figures/fig_01_gb.png?raw=true)

Outra maneira de usar o BLAST é coocando como input o arquivo todo, clicando no botão "Escolher arquivo.

Qual foi a sequência mais próxima à nossa? Se você tivesse acabado de produzir esta sequência, o que isto poderia significar?

## Usando a plataforma R para adquirir sequêcias

Se todas as sequências de DNA públicas já produzidas estão no GenBank, é lá que vamos quando queremos adquirir alguma sequência. Experimente navegar no [site](www.ncbi.nlm.nih.gov/genbank/): busque pela sequência de algum organismo e de um fragmento. Se estiver sem ideia, vamos ver sequências de rã-de-unhas-africana (*Xenopus laevis*) para o fragmento 16S. Digite no campo de busca:
```
Xenopus laevis 16S
```

E então aperte o botão search.
