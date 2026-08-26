---
title: "Perfeitos demais para serem ímpares: um problema de 2.300 anos"
date: 2026-08-26 14:00:00 -0300
categories: [Matemática, Teoria dos Números]
tags: [números perfeitos, números perfeitos ímpares, primos de mersenne, euclides, euler, gimps]
math: true
description: "Euclides explicou os números perfeitos pares e Euler completou a classificação. Mas ninguém sabe se existe um único número perfeito ímpar."
---

Há problemas de matemática que parecem difíceis desde a primeira linha. Este faz o contrário: começa com uma brincadeira que uma criança pode entender.

Tome um número, liste os seus divisores e some todos eles, exceto o próprio número. Se a soma devolver exatamente o número de partida, nós o chamamos de **perfeito**. Assim,

$$
6=1+2+3
$$

e

$$
28=1+2+4+7+14.
$$

Portanto, $6$ e $28$ são perfeitos. Os próximos são $496$ e $8128$. Tudo parece muito amigável --- até alguém fazer a pergunta que atravessou mais de dois milênios sem resposta:

> Existe algum número perfeito ímpar?

Foi essa pergunta que reapareceu no vídeo do Veritasium que circulou pelo Facebook e que motivou este texto. Ela passa por Euclides, Nicômaco, Mersenne, Fermat, Descartes, Euler, Sylvester e chega aos computadores modernos. É um daqueles raros problemas em que conseguimos dizer muita coisa, impor condições quase absurdas e eliminar extensões inimagináveis da reta numérica, mas ainda não conseguimos responder apenas **sim** ou **não**.

## A soma dos divisores

A linguagem certa para organizar a pergunta é a função soma de divisores. Para um inteiro positivo $n$, definimos

$$
\sigma(n)=\sum_{d\mid n}d,
$$

onde a notação $d\mid n$ significa que $d$ divide $n$. Como essa soma inclui o próprio $n$, a definição de número perfeito fica particularmente curta:

$$
n \text{ é perfeito}\quad\Longleftrightarrow\quad \sigma(n)=2n.
$$

No caso de $28$, por exemplo,

$$
\sigma(28)=1+2+4+7+14+28=56=2\cdot 28.
$$

### Uma pequena caixa de ferramentas aritméticas

Antes de prosseguir, vale recordar algumas ideias básicas da teoria dos números. Dizemos que um inteiro $d$ **divide** um inteiro $n$, e escrevemos $d\mid n$, quando existe um inteiro $k$ tal que

$$
n=dk.
$$

Um inteiro $p\geq 2$ é **primo** quando seus únicos divisores positivos são $1$ e o próprio $p$. Todo inteiro maior que $1$ pode ser escrito, de maneira única a menos da ordem dos fatores, como produto de números primos. É essa fatoração que organiza boa parte dos argumentos deste texto.

O **máximo divisor comum** de dois inteiros $a$ e $b$, abreviado por $\mathrm{mdc}(a,b)$, é o maior inteiro positivo que divide ambos. Quando

$$
\mathrm{mdc}(a,b)=1,
$$

dizemos que $a$ e $b$ são **coprimos**.

Também usaremos o conceito de **congruência**. Escrevemos

$$
a\equiv b\pmod m
$$

quando $a$ e $b$ deixam o mesmo resto na divisão por $m$. De modo equivalente, isso significa que $m$ divide $a-b$. Por exemplo,

$$
17\equiv 1\pmod 4,
$$

pois tanto $17$ quanto $1$ deixam resto $1$ na divisão por $4$. Essa notação aparecerá mais adiante na descrição da forma que um eventual número perfeito ímpar teria.

Há outra propriedade decisiva. Se $a$ e $b$ não têm fator primo em comum, então $\sigma$ é multiplicativa:

$$
\mathrm{mdc}(a,b)=1
\quad\Longrightarrow\quad
\sigma(ab)=\sigma(a)\sigma(b).
$$

Isso não significa que $\sigma(a+b)=\sigma(a)+\sigma(b)$, nem que a fórmula valha sem a condição de coprimalidade. Significa apenas que a fatoração prima de um número permite desmontar uma soma de divisores aparentemente enorme em produtos muito mais simples. É essa pequena engrenagem que faz funcionar o grande teorema da história.

## Antes da prova, a mística

Os antigos não escolheram a palavra “perfeito” por modéstia. Para a tradição pitagórica, os números tinham personalidade, simbolismo e até valor moral. O $6$ parecia especialmente harmonioso: além de ser igual à soma de seus divisores próprios, também é o produto dos três primeiros inteiros positivos,

$$
6=1+2+3=1\cdot 2\cdot 3.
$$

Por volta do ano 100, Nicômaco de Gerasa registrou os quatro primeiros números perfeitos e lhes atribuiu uma ordem quase cósmica. Também propôs padrões que mais tarde se mostraram falsos, como a ideia de que os finais $6$ e $8$ sempre se alternariam. Esse detalhe é saudável: a história da matemática não é uma fila de gênios que nunca erram, mas uma conversa longa em que exemplos sugerem conjecturas, e novos exemplos obrigam a corrigi-las.

O passo decisivo havia ocorrido séculos antes. Euclides retirou a perfeição do terreno da contemplação e a colocou dentro de uma demonstração.

## Euclides encontra uma fábrica

Por volta de 300 a.C., na Proposição 36 do Livro IX dos *Elementos*, Euclides percebeu uma ligação entre números perfeitos e números da forma

$$
M_p=2^p-1.
$$

Hoje esses números são chamados **números de Mersenne**, em homenagem ao monge francês Marin Mersenne, que os estudou no século XVII. Quando $M_p$ é primo, dizemos que ele é um **primo de Mersenne**.

A receita de Euclides é simples:

$$
M_p=2^p-1 \text{ primo}
\quad\Longrightarrow\quad
N=2^{p-1}M_p \text{ perfeito}.
$$

Ela produz os primeiros exemplos de uma só vez:

| $p$ | $M_p=2^p-1$ | $2^{p-1}M_p$ |
|--:|--:|--:|
| $2$ | $3$ | $6$ |
| $3$ | $7$ | $28$ |
| $5$ | $31$ | $496$ |
| $7$ | $127$ | $8128$ |

É necessário que $p$ seja primo para que $M_p$ possa ser primo. De fato, se $p=ab$ é composto, então

$$
2^{ab}-1=(2^a)^b-1
$$

tem a fatoração usual de uma diferença de potências. Mas o caminho inverso falha: $p$ primo não garante que $M_p$ seja primo. O primeiro tropeço é

$$
M_{11}=2^{11}-1=2047=23\cdot 89.
$$

Isso explica por que procurar números perfeitos pares e procurar primos de Mersenne são, essencialmente, a mesma aventura.

## Euler fecha a porta dos pares

Euclides construiu números perfeitos pares, mas não provou que todos eles vinham de sua receita. Mais de dois mil anos depois, no século XVIII, Leonhard Euler demonstrou a volta. O resultado completo, hoje chamado **Teorema de Euclides--Euler**, diz:

**Teorema (Euclides--Euler).** Um inteiro positivo par $N$ é perfeito se, e somente se,

$$
N=2^{p-1}(2^p-1),
$$

onde $2^p-1$ é primo.

É uma classificação perfeita, nos dois sentidos da palavra. Não conhecemos apenas alguns exemplos: sabemos exatamente qual forma **todo** número perfeito par precisa ter.

### A ida: a parte de Euclides

Suponha que $M_p=2^p-1$ seja primo e tome

$$
N=2^{p-1}M_p.
$$

Como $2^{p-1}$ e $M_p$ são coprimos, a multiplicatividade de $\sigma$ dá

$$
\begin{aligned}
\sigma(N)
&=\sigma\!\left(2^{p-1}\right)\sigma(M_p)\\
&=(1+2+\cdots+2^{p-1})(1+M_p)\\
&=(2^p-1)2^p\\
&=2N.
\end{aligned}
$$

Logo $N$ é perfeito.

### A volta: a parte de Euler

Agora suponha que $N$ seja um número perfeito par. Podemos escrever

$$
N=2^{p-1}m,
$$

com $m$ ímpar e $p\geq 2$. Novamente pela multiplicatividade,

$$
\begin{aligned}
2^p m
&=2N\\
&=\sigma(N)\\
&=\sigma\!\left(2^{p-1}\right)\sigma(m)\\
&=(2^p-1)\sigma(m).
\end{aligned}
$$

Como

$$
\mathrm{mdc}(2^p-1,2^p)=1,
$$

segue que $2^p-1$ divide $m$. Escrevamos

$$
m=(2^p-1)r.
$$

A igualdade anterior passa a dizer que

$$
\sigma(m)=2^p r.
$$

Se $r>1$, então $1$, $r$ e $m$ são três divisores distintos de $m$. Portanto,

$$
\sigma(m)\geq 1+r+m
=1+r+(2^p-1)r
=1+2^p r,
$$

o que contradiz $\sigma(m)=2^p r$. Logo $r=1$ e

$$
m=2^p-1.
$$

Por fim, $\sigma(m)=2^p=m+1$. Isso só pode acontecer se $m$ for primo, pois um número composto teria, além de $1$ e de si mesmo, pelo menos mais um divisor positivo. Assim,

$$
N=2^{p-1}(2^p-1),
$$

com $2^p-1$ primo. A receita de Euclides não deixava escapar nenhum perfeito par. $\blacksquare$

## Mersenne, Fermat e um silêncio de uma hora

Os números de Mersenne também guardam uma história deliciosamente humana. Em 1644, Mersenne publicou uma lista dos expoentes $p\leq 257$ para os quais acreditava que $2^p-1$ fosse primo. A lista continha acertos extraordinários, mas também erros --- inevitáveis numa época em que cada cálculo era feito à mão.

Um dos casos mais famosos era $M_{67}$. Em 1903, durante uma reunião da American Mathematical Society, Frank Nelson Cole foi ao quadro e não disse uma palavra. De um lado calculou

$$
2^{67}-1=147\,573\,952\,589\,676\,412\,927.
$$

Do outro, multiplicou

$$
193\,707\,721\cdot 761\,838\,257\,287
$$

e chegou ao mesmo número. Sentou-se sob aplausos. Segundo o próprio Cole, a fatoração lhe havia custado “três anos de domingos”. Uma palestra sem discurso havia resolvido uma dúvida de séculos.

Essa dificuldade explica por que os primos de Mersenne se tornaram um campo natural para a computação. Eles são raros, mas sua forma especial permite testes muito mais eficientes do que os disponíveis para um inteiro arbitrário do mesmo tamanho.

## O gigante atual

Em 21 de outubro de 2024, o projeto colaborativo GIMPS anunciou o maior primo conhecido:

$$
M_{136\,279\,841}=2^{136\,279\,841}-1.
$$

Ele tem **41.024.320 algarismos decimais**, foi encontrado por Luke Durant e é o 52º primo de Mersenne conhecido. O teste inicial utilizou uma infraestrutura distribuída de GPUs; a confirmação foi feita de modo independente, inclusive com o teste de Lucas--Lehmer.

Pelo Teorema de Euclides--Euler, a descoberta entrega imediatamente um novo número perfeito:

$$
2^{136\,279\,840}\left(2^{136\,279\,841}-1\right).
$$

Esse número tem **82.048.640 algarismos**. É grande demais para caber em qualquer página razoável, mas a sua estrutura cabe numa linha.

Há uma beleza particular nisso: a mesma fórmula escrita por Euclides há mais de dois milênios continua transformando descobertas feitas em centros de dados, espalhados por vários países, em novos números perfeitos.

## E os ímpares?

Aqui a história muda de tom. O Teorema de Euclides--Euler encerra completamente o caso par, mas não diz que números perfeitos ímpares não existem. Até hoje, ninguém encontrou um. Tampouco alguém demonstrou que sejam impossíveis.

Eles desafiaram alguns dos maiores nomes da teoria dos números. René Descartes e Pierre de Fermat estudaram condições que um candidato teria de satisfazer. Euler obteve a forma estrutural fundamental. James Joseph Sylvester provou restrições adicionais no século XIX. Nos séculos XX e XXI, matemáticos como Peter Hagis Jr., Pace Nielsen, Takeshi Goto, Yasuo Ohno, Pascal Ochem e Michaël Rao apertaram o cerco com argumentos teóricos e buscas computacionais.

O efeito acumulado é curioso. Um número perfeito ímpar, se existir, não será pequeno, não terá poucos fatores primos e não terá uma fatoração simples. Ele precisará passar por um labirinto de condições necessárias. Ainda assim, nenhuma delas fechou a saída.

## A forma de Euler: quase tudo é quadrado

Euler demonstrou que todo número perfeito ímpar $N$, se existir, terá a forma

$$
N=q^\alpha p_1^{2e_1}p_2^{2e_2}\cdots p_k^{2e_k},
$$

onde $q,p_1,\ldots,p_k$ são primos ímpares distintos e

$$
q\equiv \alpha\equiv 1\pmod 4.
$$

Em outras palavras, todos os expoentes da fatoração são pares, exceto um. O termo excepcional $q^\alpha$ é chamado **componente euleriana**.

Vale acompanhar a ideia, porque a demonstração é curta e mostra como uma informação aparentemente fraca --- a paridade --- impõe uma arquitetura inteira.

Escreva a fatoração prima de $N$ como

$$
N=\prod_{i=1}^s p_i^{a_i}.
$$

Como $N$ é ímpar e perfeito,

$$
\sigma(N)=2N
$$

é divisível por $2$, mas não por $4$. Pela multiplicatividade,

$$
\sigma(N)=\prod_{i=1}^s
\left(1+p_i+p_i^2+\cdots+p_i^{a_i}\right).
$$

Cada $p_i$ é ímpar. Logo a soma

$$
1+p_i+\cdots+p_i^{a_i}
$$

é par exatamente quando $a_i$ é ímpar. Como o produto inteiro possui apenas um fator $2$, existe exatamente um expoente ímpar. Chamemos esse expoente de $\alpha$ e o primo correspondente de $q$; todos os demais expoentes são pares.

Além disso,

$$
\sigma(q^\alpha)\equiv 2\pmod 4.
$$

Se $q\equiv 3\pmod 4$, podemos agrupar os termos em pares,

$$
(1+q)+(q^2+q^3)+\cdots,
$$

e cada par é divisível por $4$, uma contradição. Portanto $q\equiv 1\pmod 4$. Nesse caso, cada potência de $q$ é congruente a $1$ módulo $4$, e então

$$
\sigma(q^\alpha)\equiv \alpha+1\equiv 2\pmod 4.
$$

Consequentemente,

$$
\alpha\equiv 1\pmod 4.
$$

Essa é a forma de Euler. Ela diz que um perfeito ímpar seria “quase um quadrado”: um quadrado perfeito multiplicado por uma única potência prima especial.

## O cartaz de procurado

Dois milênios de trabalho transformaram o hipotético perfeito ímpar num fugitivo com descrição minuciosa. Entre as restrições publicadas, temos:

| Se $N$ é um número perfeito ímpar, então... | Resultado |
|:--|:--|
| ele é gigantesco | $N>10^{1500}$ |
| tem muitos primos distintos | $\omega(N)\geq 10$ |
| tem muitos fatores contando multiplicidades | $\Omega(N)\geq 101$ |
| possui um fator primo enorme | algum primo divisor excede $10^8$ |
| possui uma componente prima potente | algum $p^a\mid N$ excede $10^{62}$ |
| escapa de uma divisibilidade tentadora | $105\nmid N$ |

Aqui $\omega(N)$ conta os fatores primos **distintos**, enquanto $\Omega(N)$ os conta com multiplicidade. Por exemplo,

$$
\omega(3^2\cdot 5^4)=2,
\qquad
\Omega(3^2\cdot 5^4)=6.
$$

A cota $N>10^{1500}$ e a desigualdade $\Omega(N)\geq 101$ foram publicadas por Ochem e Rao. A página do projeto registra que as buscas computacionais posteriores já empurraram essas barreiras para $N>10^{2200}$ e $\Omega(N)\geq 115$. Para manter a distinção importante entre teorema publicado e atualização computacional, fico com as primeiras na tabela e registro as segundas aqui.

O resultado de Nielsen de que $\omega(N)\geq 10$ também atualiza drasticamente os enunciados antigos. Na notação da forma de Euler, isso significa que aparecem pelo menos nove primos $p_i$, além do primo especial $q$. O velho limite de Hagis, importante em sua época, já foi largamente superado.

Tudo isso parece quase uma prova de inexistência. Mas “não existe abaixo de $10^{1500}$” é muito diferente de “não existe”. A reta dos inteiros não termina, e problemas infinitos não se deixam vencer apenas por exaustão.

## O falso perfeito de Descartes

É aqui que entra a nova frente descrita no artigo de Steve Nadis, [*Mathematicians Open a New Front on an Ancient Number Problem*](https://www.quantamagazine.org/mathematicians-open-a-new-front-on-an-ancient-number-problem-20200910/), publicado pela *Quanta Magazine*. Em 1638, Descartes escreveu a Mersenne com um objeto estranho:

$$
D=3^2\cdot 7^2\cdot 11^2\cdot 13^2\cdot 22021.
$$

Se tratarmos $22021$ **como se fosse primo**, a fórmula multiplicativa da soma de divisores produz

$$
\begin{aligned}
\widetilde{\sigma}(D)
&=(1+3+3^2)(1+7+7^2)(1+11+11^2)\\
&\qquad\cdot(1+13+13^2)(1+22021)\\
&=2D.
\end{aligned}
$$

O problema é que

$$
22021=19^2\cdot 61.
$$

Portanto, a conta não é a verdadeira $\sigma(D)$: ela usa uma fatoração falsa. O número de Descartes não é perfeito. É uma **imitação de número perfeito**, ou *spoof perfect factorization*: um objeto que satisfaz formalmente a equação certa quando suas bases são fingidas primas.

Em 1999, John Voight encontrou um exemplo ainda mais excêntrico, com uma base negativa:

$$
3^4\cdot 7^2\cdot 11^2\cdot 19^2\cdot(-127).
$$

À primeira vista, estudar imitações pode parecer um desvio. Na verdade, é justamente a estratégia: ampliar o universo para enxergar melhor quais argumentos dependem apenas da multiplicatividade de $\sigma$ e quais realmente usam o fato de as bases serem primas.

## A nova frente

Pace Nielsen e o grupo de Teoria Computacional dos Números da Universidade Brigham Young decidiram classificar sistematicamente essas imitações ímpares. Depois de anos de cálculo paralelo, o grupo encontrou **21 fatorações perfeitas falsas, ímpares, primitivas e não triviais com menos de sete bases**, além de exemplos com sete bases.

O resultado revelou duas coisas que puxam em direções opostas.

Primeiro, há muito mais estrutura nesse mundo falso do que o exemplo isolado de Descartes sugeria. O grupo encontrou famílias infinitas de imitações e demonstrou, ao mesmo tempo, que para um número fixo de bases existe apenas um número finito de candidatas primitivas. Em vez de uma curiosidade histórica, surgiu uma teoria própria.

Segundo, essas imitações funcionam como um teste de resistência para possíveis provas. Se um argumento usa somente a multiplicatividade da função soma de divisores e também vale para todos os *spoofs*, ele provavelmente não bastará para eliminar os números perfeitos ímpares genuínos. Será preciso explorar alguma característica mais profunda da primalidade.

Essa conclusão é valiosa mesmo sem resolver o problema. Às vezes a matemática avança não encontrando imediatamente a porta de saída, mas descobrindo quais corredores terminam numa parede.

## Por que o problema continua aberto?

A equação

$$
\sigma(N)=2N
$$

mistura duas naturezas difíceis de controlar ao mesmo tempo. A fatoração de $N$ é multiplicativa e local, organizada primo a primo; já a exigência de que o produto de todas as somas geométricas seja exatamente o dobro de $N$ cria uma restrição global. Cada novo fator primo ajuda a satisfazer algumas condições e complica muitas outras.

Para os pares, a potência de $2$ deixa uma assinatura forte o bastante para o argumento de Euclides--Euler funcionar. Nos ímpares, essa âncora desaparece. A forma de Euler, as congruências, as cotas e as buscas computacionais vão estreitando o conjunto, mas o conjunto restante continua infinito.

É isso que torna a pergunta tão resistente e tão bonita. Ela não pede uma fórmula sofisticada nem uma máquina conceitual enorme para ser enunciada. Pede apenas que somemos divisores. O abismo se abre depois.

## Conclusão

Os números perfeitos pares vivem numa ordem impecável:

$$
2^{p-1}(2^p-1),
$$

um primo de Mersenne de um lado, um número perfeito do outro. Euclides construiu a ponte; Euler provou que não havia outra passagem; o GIMPS continua atravessando-a com números de dezenas de milhões de algarismos.

Do lado ímpar, porém, temos apenas pegadas. Sabemos que um candidato seria quase um quadrado, teria ao menos dez fatores primos distintos, passaria muito além de $10^{1500}$ e obedeceria a uma longa coleção de congruências. Sabemos até construir impostores convincentes. O que não sabemos é se o personagem procurado existe.

Talvez algum dia apareça um número perfeito ímpar gigantesco. Talvez alguém prove que toda essa busca perseguiu uma sombra. Até lá, uma pergunta compreensível por qualquer estudante continuará fazendo o que os melhores problemas fazem: obrigando cada geração de matemáticos a inventar uma maneira nova de olhar para os inteiros.

## Referências

- EUCLIDES. *Os Elementos*, Livro IX, Proposição 36. Texto e comentário disponíveis no [Euclid's Elements, de D. E. Joyce](https://mathcs.clarku.edu/~djoyce/java/elements/bookIX/propIX36.html).
- DICKSON, Leonard Eugene. *History of the Theory of Numbers*. v. I: *Divisibility and Primality*. Washington: Carnegie Institution of Washington, 1919.
- COLE, Frank Nelson. “On the Factoring of Large Numbers”. *Bulletin of the American Mathematical Society*, v. 10, p. 134--137, 1903.
- DUNHAM, William. *Euler: The Master of Us All*. Washington: Mathematical Association of America, 1999.
- NIELSEN, Pace P. “Odd Perfect Numbers Have at Least Nine Distinct Prime Factors”. *Mathematics of Computation*, v. 76, p. 2109--2126, 2007. <https://doi.org/10.1090/S0025-5718-07-01990-4>.
- NIELSEN, Pace P. “Odd Perfect Numbers, Diophantine Equations, and Upper Bounds”. *Mathematics of Computation*, v. 84, p. 2549--2567, 2015. <https://doi.org/10.1090/S0025-5718-2015-02941-X>.
- GOTO, Takeshi; OHNO, Yasuo. “Odd Perfect Numbers Have a Prime Factor Exceeding $10^8$”. *Mathematics of Computation*, v. 77, p. 1859--1868, 2008. <https://doi.org/10.1090/S0025-5718-08-02050-4>.
- OCHEM, Pascal; RAO, Michaël. “Odd Perfect Numbers Are Greater Than $10^{1500}$”. *Mathematics of Computation*, v. 81, p. 1869--1877, 2012. <https://doi.org/10.1090/S0025-5718-2012-02563-4>.
- BYU COMPUTATIONAL NUMBER THEORY GROUP. “Odd, Spoof Perfect Factorizations”. *Journal of Number Theory*, v. 234, p. 31--47, 2022. <https://doi.org/10.1016/j.jnt.2021.07.028>.
- NADIS, Steve. “[Mathematicians Open a New Front on an Ancient Number Problem](https://www.quantamagazine.org/mathematicians-open-a-new-front-on-an-ancient-number-problem-20200910/)”. *Quanta Magazine*, 10 set. 2020.
- O'CONNOR, J. J.; ROBERTSON, E. F. “[Perfect Numbers](https://mathshistory.st-andrews.ac.uk/HistTopics/Perfect_numbers/)”. *MacTutor History of Mathematics Archive*.
- GIMPS. “[Mersenne Prime Discovery: $2^{136279841}-1$ Is Prime!](https://www.mersenne.org/primes/?press=M136279841)”. Great Internet Mersenne Prime Search, 21 out. 2024.
- VERITASIUM. “[The Oldest Unsolved Problem in Math](https://www.youtube.com/watch?v=Zrv1EDIqHkY)”. Vídeo, 2024.
