---
title: "Números contra letras: uma breve história da abstração"
date: 2026-08-06 10:00:00 -0300
categories: [Matemática, Filosofia das Ciências]
tags: [história da matemática, álgebra, teoria dos números, cayley-dickson]
math: true
description: "Dizem que a matemática ficou difícil quando trocaram números por letras. Essa queixa esconde a descoberta mais poderosa da história da matemática: a generalidade."
---

Há uma frase que todo professor de matemática já ouviu, dita com um misto de nostalgia e ressentimento:

> *Eu entendia matemática quando era só número. Aí inventaram de botar letra, e eu me perdi.*

A frase é simpática, e por trás dela mora uma intuição verdadeira: alguma coisa realmente muda quando o $x$ entra em cena. Mas a queixa inverte os papéis. Ela trata a letra como uma complicação gratuita, um capricho de matemáticos para dificultar a vida alheia. É o oposto. A letra não é onde a matemática ficou difícil --- é onde ela ficou **poderosa**.

Este texto é sobre essa passagem: do número à letra, do particular ao geral. É uma das histórias mais longas e dramáticas da matemática, com direito a uma morte no mar, uma reconciliação no século XVII e teoremas modernos cujas demonstrações se afastam quase completamente da aritmética elementar.

## O que uma letra faz que um número não faz

Comecemos pelo essencial, porque é aqui que a queixa popular erra o alvo.

Um número é um **objeto particular**. O símbolo $7$ se refere a uma coisa específica, sempre a mesma. Uma letra, num contexto matemático, é outra coisa inteiramente: ela fala de **todos os objetos de uma vez**. Quando escrevo

$$
(a+b)^2 = a^2 + 2ab + b^2,
$$

não estou falando de nenhum par de números em particular. Estou afirmando algo sobre *qualquer* par --- os que já existem, os que ninguém nunca calculou, os que jamais serão calculados. Uma única linha captura uma infinidade de fatos aritméticos.

Essa é a troca que a álgebra propõe: você abre mão da familiaridade do particular e recebe, em troca, o **domínio sobre o geral**. A letra é o instrumento da generalidade. Dizer que a matemática ficou pior quando surgiram as letras é como dizer que a escrita piorou quando saímos dos desenhos de bisões e adotamos um alfabeto: perde-se a figura concreta, ganha-se a capacidade de dizer qualquer coisa.

A resistência às letras é, no fundo, uma resistência à abstração. E a abstração é exatamente o que a matemática tem de mais próprio. A história a seguir mostra que essa tensão --- entre o número que se toca e a estrutura que se pensa --- não é nova. Ela é o próprio motor da disciplina.

## Babilônia: a álgebra antes da letra

A álgebra é muito mais antiga do que suas letras. Mais de mil e quinhentos anos antes de Cristo, os escribas da Babilônia já resolviam o que hoje chamaríamos de equações do segundo grau. Tábuas de argila como a famosa Plimpton 322 revelam um domínio sofisticado de relações numéricas, incluindo ternos pitagóricos, muito antes de Pitágoras.

Mas havia uma diferença crucial. A álgebra babilônica era **retórica**: os problemas e suas soluções eram escritos por extenso, em palavras, e sempre com números concretos. Um escriba não dizia "para resolver $ax^2+bx+c=0$, faça...". Ele dizia algo como: "encontrei uma pedra, não a pesei; depois de somar um sétimo e mais um..." --- e resolvia aquele caso específico, com aqueles números específicos. O método era geral na cabeça de quem o executava, mas a linguagem só sabia falar do particular.

Faltava o símbolo que dissesse "qualquer". Faltava a letra. E, sem ela, cada problema era uma ilha; a generalidade existia na prática, mas não podia ser escrita, guardada, manipulada. A humanidade levaria três mil anos para dar esse passo.

## O escândalo da diagonal: quando o número não bastou

Antes de a letra chegar para salvar a generalidade, os números sofreram um golpe que abalou suas fundações --- e o golpe veio da geometria.

Os pitagóricos, no século V a.C., viviam sob um lema que era quase uma religião: *tudo é número*. Por número, entendiam os inteiros e suas razões --- as frações. Acreditavam que quaisquer duas grandezas eram **comensuráveis**: sempre existiria uma unidade pequena o bastante para medir as duas um número inteiro de vezes. O mundo era, para eles, um tecido de proporções entre inteiros.

Então alguém olhou para o objeto mais simples possível: um quadrado de lado $1$. Pelo teorema de Pitágoras, sua diagonal $d$ satisfaz

$$
d^2 = 1^2 + 1^2 = 2, \qquad \text{ou seja} \qquad d = \sqrt{2}.
$$

E aqui está a catástrofe: **$\sqrt{2}$ não é uma fração**. Não existem inteiros $p$ e $q$ tais que $\sqrt2 = p/q$. A demonstração é curta e devastadora --- talvez a primeira prova por absurdo da história. Suponha que $\sqrt2 = p/q$ em termos mínimos. Então $p^2 = 2q^2$, logo $p^2$ é par, logo $p$ é par, digamos $p=2k$. Substituindo, $4k^2 = 2q^2$, ou seja $q^2 = 2k^2$, e então $q$ também é par. Mas $p$ e $q$ pares contradizem a hipótese de que a fração era mínima. Absurdo. Logo $\sqrt2$ não pode ser escrito como razão de inteiros.

A diagonal do quadrado, o objeto mais banal da geometria, era **incomensurável** com o lado. O lema "tudo é número" acabava de ruir --- pelo menos se "número" significava apenas os inteiros e suas frações.

## Hipaso e a lenda do mar

A esse descobrimento a tradição associa o nome de **Hipaso de Metaponto**, um pitagórico do século V a.C., e uma história que se tornou o mito de origem da matemática rigorosa: Hipaso teria revelado o segredo dos incomensuráveis ao mundo exterior e, por essa traição, os pitagóricos o teriam afogado no mar --- ou os deuses o teriam feito, como punição pela impiedade.

Vale, aqui, um cuidado que a boa história exige. Essa narrativa é **quase certamente lenda**. As fontes antigas são poucas, tardias e contraditórias: algumas falam em expulsão, não em morte; outras dizem que o afogamento se deu por revelar a construção do dodecaedro na esfera, não os irracionais; e nenhum escritor antigo atribui explicitamente a descoberta da irracionalidade a Hipaso. A cena do naufrágio punitivo é boa demais para ser verdade, e provavelmente não é.

Mas a lenda sobrevive por uma razão: ela é *simbolicamente* verdadeira. Captura o trauma real de uma comunidade que via sua visão de mundo desmoronar diante de uma verdade que não queria existir. O número, sozinho, não dava conta da geometria. Havia comprimentos que nenhuma fração podia nomear. E a matemática precisaria de dois mil anos para construir a linguagem capaz de domar esses novos objetos.

## A letra chega: de al-Khwārizmī a Viète

O caminho até a letra foi lento. A palavra *álgebra* vem do árabe *al-jabr*, do título do tratado de **al-Khwārizmī** (século IX), cujo próprio nome nos deu *algarismo* e *algoritmo*. Ele sistematizou a resolução de equações --- mas ainda de forma retórica, em palavras.

O salto decisivo veio no fim do século XVI, com o francês **François Viète** (por volta de 1591, em seu *In artem analyticem isagoge*), muitas vezes chamado o pai da álgebra simbólica. Sua ideia foi de uma simplicidade genial: usar letras não só para a incógnita que se procura, mas também para os **coeficientes conhecidos** --- as vogais para o que é desconhecido, as consoantes para o que é dado. Pela primeira vez, era possível escrever uma equação *geral*, com parâmetros literais, e manipulá-la como estrutura.

Foi a invenção da letra como a conhecemos. E, com ela, a matemática ganhou o poder de falar do geral com a mesma facilidade com que antes falava do particular. A queixa popular do início deste texto data, historicamente, deste momento: foi aqui que os números ganharam companhia --- e que a matemática se tornou, para sempre, uma ciência de estruturas.

## Descartes: a grande reconciliação

Se o escândalo de $\sqrt2$ tinha aberto um fosso entre o número (aritmética) e a forma (geometria), coube ao século XVII fechá-lo --- e de maneira espetacular.

Em 1637, **René Descartes** publicou *La Géométrie*, e com ela a **geometria analítica**. A ideia é tão familiar hoje que custa perceber quão revolucionária foi: associar a cada ponto do plano um par de números, suas coordenadas $(x,y)$. De um só golpe, as duas metades da matemática se reencontravam. Uma curva --- objeto geométrico, visual --- passava a ter uma equação --- objeto algébrico, simbólico. A reta vira $y = ax+b$; o círculo, $x^2+y^2=r^2$; a parábola, $y = x^2$.

Foi a reconciliação da álgebra com a geometria, mediada precisamente pela **letra**. E note a inversão histórica: a geometria, que no tempo dos pitagóricos havia *derrotado* o número ao exibir a diagonal incomensurável, agora se deixava *escrever* em números e letras. O que antes era ruptura virava tradução. A letra, longe de complicar, era a ponte que unia os dois continentes.

A partir de Descartes, álgebra e geometria deixam de ser rivais e passam a ser duas línguas para as mesmas verdades --- e a fluência em traduzir uma na outra torna-se a marca do matemático.

## Teoria dos Números: onde os números somem

Chegamos à ironia suprema desta história, e ao seu ápice.

A **Teoria dos Números** é o ramo da matemática que estuda os números inteiros --- os objetos mais concretos e antigos que existem, aqueles que a criança conta nos dedos. Seria de esperar que fosse o reino do número puro, livre de letras. O que ocorre nos grandes teoremas é quase o oposto: o enunciado continua sendo aritmético, mas a demonstração abandona rapidamente a manipulação direta de inteiros e passa a trabalhar com **funções, curvas, espaços, simetrias, representações e operadores**.

Isso não significa, literalmente, que os números desapareçam. Significa que eles deixam de ser o objeto imediato de cada etapa da prova. O problema aritmético é **traduzido** para outra linguagem, estudado nessa linguagem mais ampla e, somente ao final, traduzido de volta. Muitas dessas ferramentas pertencem à análise real e complexa, à geometria algébrica, à teoria de Galois e à álgebra abstrata; em sua forma natural, elas não são simples operações com números inteiros. Contudo, conseguem codificar informações aritméticas que seriam praticamente inacessíveis por cálculos elementares.

Dois exemplos monumentais tornam essa passagem particularmente nítida.

### O Último Teorema de Fermat: dos inteiros às curvas e às formas modulares

O enunciado é de uma simplicidade que qualquer estudante entende: a equação $x^n + y^n = z^n$ não tem solução em inteiros positivos para $n>2$. Fermat registrou a afirmação na margem de um livro por volta de 1637, alegando possuir uma demonstração que aquela margem não comportaria. A prova moderna, anunciada por **Andrew Wiles** em 1994 e publicada em 1995 --- com a etapa corretiva desenvolvida em colaboração com **Richard Taylor** ---, não ataca a equação por uma busca direta entre inteiros.

O caminho é indireto e conceitualmente extraordinário. Uma hipotética solução da equação de Fermat permitiria construir uma **curva elíptica** muito especial, hoje associada ao nome de Frey. O trabalho de **Gerhard Frey** (1985), **Jean-Pierre Serre** e **Ken Ribet** (que fechou o argumento em 1986--1990) mostrou que essa curva teria um comportamento incompatível com a modularidade. Por outro lado, Wiles demonstrou o caso necessário da conjectura de Taniyama--Shimura --- formulada em 1955 --- de que toda curva elíptica semiestável sobre os racionais é modular. A curva produzida por uma suposta solução de Fermat teria, portanto, de ser simultaneamente modular e não modular. A contradição elimina a solução inteira hipotética.

Observe a mudança de cenário. O problema começa com potências de inteiros, mas a demonstração passa por **curvas elípticas**, objetos da geometria algébrica; por **formas modulares**, funções holomorfas definidas no semiplano complexo superior e dotadas de simetrias muito rígidas; por **representações de Galois**, que transformam simetrias algébricas em matrizes; e por **anéis de deformação e álgebras de Hecke**, pertencentes à álgebra comutativa e à teoria das representações. O argumento não deixa de ser Teoria dos Números, mas mostra que a estrutura profunda dos inteiros aparece refletida em objetos geométricos e analíticos que, à primeira vista, parecem pertencer a outro universo.

Essa é também a força narrativa destacada por Simon Singh: o Último Teorema de Fermat não foi resolvido por uma conta gigantesca, nem por testar valores cada vez maiores, mas pela descoberta de uma ponte inesperada entre áreas que se desenvolveram separadamente durante séculos.

### O Teorema dos Números Primos: contar inteiros no plano complexo

Quantos primos existem até um número $x$? A resposta, conjecturada por Gauss ainda adolescente (por volta de 1792--1796), é que essa contagem $\pi(x)$ se comporta como $x/\ln x$ para $x$ grande:

$$
\pi(x) \sim \frac{x}{\ln x}.
$$

A afirmação fala apenas sobre números primos, mas a demonstração clássica, obtida independentemente em 1896 por **Jacques Hadamard** e **Charles de la Vallée Poussin**, é um triunfo da **análise complexa**. O ponto de partida é a função zeta de Riemann $\zeta(s)$, cujo papel central foi delineado por Riemann em seu célebre artigo de 1859. Por meio de seu produto de Euler, essa função analítica reúne, em um único objeto, a informação multiplicativa de todos os números primos. Em vez de contar os primos um a um, estuda-se o comportamento de uma função de variável complexa.

A passagem decisiva consiste em controlar $\zeta(s)$ próximo da reta $\mathrm{Re}(s)=1$ e demonstrar que ela não possui zeros nessa reta. Esse fato analítico permite, por argumentos de integração complexa e estimativas assintóticas --- ou, em formulações modernas, por teoremas de natureza tauberiana ---, recuperar informações sobre a distribuição dos primos. O raciocínio começa nos inteiros, desloca-se para funções holomorfas, prolongamento analítico, polos, zeros e estimativas no plano complexo, e retorna aos inteiros na forma da equivalência assintótica acima.

Na apresentação clássica de Montgomery e Vaughan, essa filosofia aparece de maneira sistemática: somas aritméticas, funções multiplicativas e a distribuição dos primos são estudadas mediante séries de Dirichlet, funções $L$, estimativas analíticas e propriedades da função zeta. São ferramentas que não operam apenas sobre inteiros isolados; elas convertem conjuntos de inteiros em objetos globais, capazes de revelar padrões que nenhum exame termo a termo deixaria visível.

Existem, desde os trabalhos de **Atle Selberg** e **Paul Erdős** (1948), demonstrações chamadas *elementares* do Teorema dos Números Primos. Aqui, “elementar” significa que se evita a análise complexa, não que a prova seja simples ou puramente escolar. Mesmo essas demonstrações recorrem a identidades aritméticas profundas, médias, estimativas assintóticas e argumentos analíticos sofisticados. A conclusão filosófica permanece: compreender a distribuição dos inteiros exige construir uma linguagem que ultrapassa largamente a simples manipulação dos próprios inteiros.

### A conjectura fraca de Goldbach: somar primos com análise de Fourier

Um terceiro exemplo, mais recente, torna o fenômeno quase tangível --- e traz um sabor pessoal, por vir de um matemático latino-americano. A **conjectura fraca de Goldbach** (também chamada ternária, ou "problema dos três primos") nasceu na correspondência entre Goldbach e Euler em 1742, e afirma algo que uma criança entende:

> Todo número ímpar maior que $5$ pode ser escrito como soma de três primos.

Por exemplo, $7 = 2+2+3$, $\;9 = 3+3+3$, $\;21 = 3+5+13$. Some inteiros, obtenha inteiros: não há nada mais aritmético. E, no entanto, o enunciado resistiu por **271 anos**.

Foi finalmente demonstrado em 2013 pelo matemático peruano **Harald Helfgott**, de forma incondicional. E a prova não tem quase nada a ver com "somar números". Ela se apoia no **método do círculo** de Hardy--Littlewood (desenvolvido nos anos 1920, a partir de trabalho de Vinogradov nos anos 1930), no **grande crivo**, em **somas exponenciais** $\sum_{p\le x} e(\alpha p)$ estudadas no círculo unitário do plano complexo, e numa engenhosa divisão do problema em *arcos maiores* e *arcos menores* --- linguagem que pertence à análise de Fourier e à análise harmônica, não à aritmética escolar. Para fechar o caso, Helfgott combinou essa maquinaria analítica com uma verificação computacional rigorosa da Hipótese de Riemann Generalizada até certa altura, e uma checagem numérica direta para todo ímpar até cerca de $8{,}8\times 10^{30}$.

Ou seja: para provar que basta somar *três* primos, foi preciso convocar integrais no plano complexo, funções $L$, estimativas de Fourier e supercomputadores. O enunciado cabe numa linha de aritmética; a demonstração atravessa boa parte da análise moderna. Helfgott recebeu por esse trabalho, entre outras honrarias, o Prêmio de Pesquisa Humboldt em 2015.

A lição é clara e bela: quanto mais fundo se quer entender o número, mais longe do número é preciso ir. A verdade sobre o particular mora no geral.

## A escada dos números: a foto que resume tudo

Termino com uma imagem que sintetiza toda esta viagem. A queixa popular achava que "número" era uma coisa só, simples e acabada. Mas o próprio conceito de número não parou de se expandir --- e cada expansão foi, ela mesma, um ato de abstração, uma nova generalidade conquistada.

Existe uma construção, chamada **construção de Cayley--Dickson**, que produz uma escada infinita de sistemas numéricos, cada degrau com o dobro da dimensão do anterior ($2^n$). A cada passo se ganha algo em generalidade e se perde uma propriedade familiar --- como se a abstração cobrasse um pedágio.

<figure style="margin: 1.5em auto; text-align: center;">
  <img
    src="{{ '/assets/img/posts/cayley-dickson-diagrama.jpeg' | relative_url }}"
    alt="Diagrama concêntrico das extensões de Cayley--Dickson, dos números reais aos sistemas hipercomplexos de dimensões sucessivamente duplicadas"
    style="display: block; width: 100%; max-width: 1134px; height: auto; margin: 0 auto;"
    loading="lazy">
  <figcaption style="margin-top: 0.6em; font-size: 0.9em; line-height: 1.4;">
    Diagrama das extensões obtidas pela construção de Cayley--Dickson, com duplicação sucessiva da dimensão.
  </figcaption>
</figure>

Traduzindo a legenda para o português, e lendo de dentro para fora --- do mais concreto ao mais abstrato:

| Símbolo | Sistema | Dimensão | O que se perde ao avançar |
| :-: | :-- | :-: | :-- |
| $\mathbb{R}$ | Números reais | 1D | — |
| $\mathbb{C}$ | Números complexos | 2D | a ordem (não se diz qual é "maior") |
| $\mathbb{H}$ | Quatérnios | 4D | a comutatividade ($ab \neq ba$) |
| $\mathbb{O}$ | Octônios | 8D | a associatividade |
| $\mathbb{S}$ | Sedênios | 16D | a ausência de divisores de zero |
| $\mathbb{P}$ | Pátions | 32D | — |
| $\mathbb{X}$ | Chingons | 64D | — |
| $\mathbb{U}$ | Routons | 128D | — |
| $\mathbb{V}$ | Voudons | 256D | — |

<small>Nota: uso $\mathbb{H}$ (de Hamilton) para os quatérnios, notação padrão; a imagem original usava $\mathbb{Q}$, símbolo que em geral designa os racionais. Todos com dimensão acima de 2 são chamados **hipercomplexos**.</small>

Repare no que a escada conta. No degrau mais concreto, os reais, temos tudo: ordem, comutatividade, associatividade. A cada passo rumo à abstração, uma dessas comodidades é sacrificada. Nos complexos, perde-se a ordem --- não faz sentido dizer que $i$ é "maior" que $1$. Nos quatérnios de Hamilton, perde-se a comutatividade: a ordem dos fatores altera o produto, como no mundo real das rotações no espaço. Nos octônios, perde-se a associatividade. E assim por diante.

É a mesma lição da diagonal do quadrado, repetida em oitava mais alta: cada vez que os objetos que tínhamos não bastam, inventamos objetos novos, mais gerais, ao preço de abrir mão de alguma familiaridade. O número nunca foi "uma coisa só". Foi sempre uma escada que sobe --- e cada degrau exige uma letra nova para ser nomeado.

## Conclusão

Volto, para encerrar, à queixa do começo: *"eu entendia quando era só número"*. Agora podemos ler nela o que ela de fato diz. Ela expressa saudade do particular, do concreto, do que se pode contar nos dedos. É uma saudade legítima --- mas confunde conforto com compreensão.

A matemática não ficou difícil quando surgiram as letras. Ela ficou *ela mesma*. Porque a matemática nunca foi sobre números; foi sempre sobre as **estruturas** que os números habitam, e sobre as verdades gerais que só uma letra pode enunciar. O número é onde começamos. A letra é para onde vamos.

E talvez seja essa a definição mais honesta da disciplina: a arte de encontrar, atrás de cada objeto particular que nos é dado, a estrutura geral que ninguém nos mostrou --- e de inventar os símbolos capazes de nomeá-la.

## Referências

- SINGH, Simon. *O Último Teorema de Fermat*. Edição em português. Editora‎ Record, 1998.
- MONTGOMERY, Hugh L.; VAUGHAN, Robert C. *Multiplicative Number Theory I: Classical Theory*. Cambridge Studies in Advanced Mathematics, v. 97. Cambridge: Cambridge University Press, 2007. ISBN 978-0-521-84903-6.
- WILES, Andrew. “Modular Elliptic Curves and Fermat's Last Theorem”. *Annals of Mathematics*, v. 141, n. 3, p. 443–551, 1995.
- TAYLOR, Richard; WILES, Andrew. “Ring-Theoretic Properties of Certain Hecke Algebras”. *Annals of Mathematics*, v. 141, n. 3, p. 553–572, 1995.
- HELFGOTT, Harald A. *The Ternary Goldbach Conjecture is True*. Preprint, arXiv:1312.7748 (2013). Ver também *Major arcs for Goldbach's problem*, arXiv:1305.2897.
- SELBERG, Atle. “An Elementary Proof of the Prime-Number Theorem”. *Annals of Mathematics*, v. 50, n. 2, p. 305–313, 1949. ERDŐS, Paul. “On a New Method in Elementary Number Theory Which Leads to an Elementary Proof of the Prime Number Theorem”. *PNAS*, v. 35, p. 374–384, 1949. (Os resultados centrais datam de 1948.)

