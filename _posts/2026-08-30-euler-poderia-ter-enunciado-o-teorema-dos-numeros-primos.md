---
title: "Euler poderia ter enunciado o Teorema dos Números Primos?"
date: 2026-08-30 18:00:00 -0300
categories: [Miscelânea, Matemática]
tags: [Euler, números primos, função zeta, produto de Euler, teorema dos números primos, Bernoulli]
math: true
---

Leonhard Euler chegou muito perto de enxergar uma das leis mais profundas da aritmética: a densidade assintótica dos números primos. Ele conhecia a divergência da série harmônica, descobriu que a soma dos inversos dos primos cresce como um duplo logaritmo e, sobretudo, encontrou a identidade que transformou a fatoração única dos inteiros numa fórmula analítica:

$$
\zeta(s)=\sum_{n=1}^{\infty}\frac1{n^s}
=\prod_{p\ \mathrm{primo}}\frac1{1-p^{-s}}.
$$

Em um artigo recente, Alexander Aycock pergunta como Euler poderia ter usado essas ideias para **enunciar** o Teorema dos Números Primos:

$$
\pi(x)\sim\frac{x}{\log x},
\qquad x\longrightarrow\infty,
$$

onde $\pi(x)$ é o número de primos menores ou iguais a $x$. O argumento de Aycock é historicamente sugestivo e conduz à forma correta da conjectura, mas permanece deliberadamente heurístico. Isso não é uma deficiência acidental: seu propósito é reconstruir uma possível descoberta do **enunciado**, não oferecer uma prova que Euler teria deixado escapar.

O objetivo deste texto é conservar essa bela intuição e examinar com rigor até onde as fórmulas conhecidas por Euler realmente permitiam avançar. A resposta à pergunta do título será afirmativa: **Euler dispunha de elementos suficientes para conjecturar que $\pi(x)\sim x/\log x$, muitas décadas antes da observação atribuída ao jovem Gauss**. Isso não significa que ele pudesse demonstrar o resultado.

Depois de reconstruir essa possível dedução e identificar exatamente seu caráter heurístico, apresentaremos também a cadeia matemática que transforma a conjectura em teorema. Essa parte posterior servirá como contraste: ela mostrará por que a prova estava fora do alcance não apenas de Euler, mas também da matemática disponível quando Gauss formulou sua previsão.

## A lei que procuramos

Se $f(x)$ e $g(x)$ são positivas para $x$ suficientemente grande, escrevemos

$$
f(x)\sim g(x)
$$

quando

$$
\lim_{x\to\infty}\frac{f(x)}{g(x)}=1.
$$

O Teorema dos Números Primos afirma, portanto, que a proporção de inteiros próximos de $x$ que são primos é aproximadamente $1/\log x$. Não se trata de dizer que os primos seguem um padrão local simples. O teorema descreve uma regularidade global que emerge depois de grandes oscilações:

$$
\boxed{\displaystyle \pi(x)\sim\frac{x}{\log x}.}
$$

Em uma carta a Johann Encke, escrita em 1849, Gauss afirmou ter começado a investigar a frequência dos primos em 1792 ou 1793, quando tinha cerca de quinze ou dezesseis anos. Segundo seu relato retrospectivo, ele percebeu que a densidade dos primos próximos de $x$ deveria ser aproximadamente $1/\log x$, o que conduz à integral logarítmica

$$
\operatorname{Li}(x)=\int_2^x\frac{dt}{\log t}.
$$

Como uma integração por partes fornece

$$
\operatorname{Li}(x)\sim\frac{x}{\log x},
$$

as duas formulações possuem o mesmo termo principal.

Legendre publicou em 1798 uma aproximação relacionada. O trabalho de Euler que contém o produto sobre os primos, porém, havia sido escrito em 1737 — mais de meio século antes das investigações juvenis relatadas por Gauss. Não afirmaremos que Euler efetivamente formulou o Teorema dos Números Primos: não há documento conhecido que sustente essa prioridade. A tese é contrafactual e mais cuidadosa: **a partir de resultados que ele realmente possuía, Euler poderia ter reconhecido e enunciado a mesma lei assintótica antes de Gauss**.

## A fórmula de Euler, agora sem produtos formais

Comecemos pelo ponto realmente euleriano. Para um número complexo $s$ com parte real $\sigma=\operatorname{Re}s>1$, a série

$$
\zeta(s)=\sum_{n=1}^{\infty}\frac1{n^s}
$$

converge absolutamente. Para tornar o produto infinito rigoroso, fixemos inicialmente apenas os primos menores ou iguais a um número $y$:

$$
P_y(s)=\prod_{p\le y}\frac1{1-p^{-s}}.
$$

Cada fator é uma série geométrica absolutamente convergente,

$$
\frac1{1-p^{-s}}=1+p^{-s}+p^{-2s}+\cdots.
$$

Como o produto contém somente um número finito de fatores, podemos multiplicar essas séries. Pelo Teorema Fundamental da Aritmética, cada escolha das potências dos primos produz exatamente um inteiro cujos fatores primos são menores ou iguais a $y$, e nenhum inteiro aparece duas vezes. Logo,

$$
P_y(s)
=\sum_{\substack{n\ge1\\p\mid n\Rightarrow p\le y}}\frac1{n^s}.
$$

Quando $y$ cresce, os conjuntos de inteiros do lado direito aumentam e acabam contendo todo inteiro positivo. Para $s=\sigma>1$ real, os termos são não negativos e

$$
P_y(\sigma)\le\sum_{n=1}^{\infty}\frac1{n^\sigma}=\zeta(\sigma).
$$

A convergência monótona dá

$$
\lim_{y\to\infty}P_y(\sigma)=\zeta(\sigma).
$$

A convergência absoluta permite estender a mesma identidade a todo $s$ com $\operatorname{Re}s>1$. Assim obtemos, sem multiplicações meramente formais,

$$
\boxed{\displaystyle
\zeta(s)=\prod_p(1-p^{-s})^{-1},
\qquad \operatorname{Re}s>1.}
$$

Essa fórmula apareceu no trabalho de Euler *Variae observationes circa series infinitas*, escrito em 1737 e publicado em 1744. É difícil exagerar sua importância: de um lado está uma soma sobre todos os inteiros; do outro, um produto apenas sobre os primos. A igualdade é a fatoração única transformada em análise.

## Tomando o logaritmo: onde a contagem dos primos aparece

Na região $\sigma>1$, temos convergência absoluta de

$$
\sum_p\sum_{k=1}^{\infty}\frac1{k p^{ks}}.
$$

Podemos, portanto, tomar o logaritmo do produto e expandir $-\log(1-z)=\sum_{k\ge1}z^k/k$:

$$
\log\zeta(s)
=\sum_p\log\frac1{1-p^{-s}}
=\sum_p\sum_{k=1}^{\infty}\frac1{k p^{ks}}.
$$

Existe também uma forma que introduz diretamente $\pi(x)$. Interpretando a soma sobre os primos como uma integral de Stieltjes e integrando por partes, obtemos

$$
\begin{aligned}
\log\zeta(s)
&=\int_{2^-}^{\infty}
\log\left(\frac1{1-x^{-s}}\right)d\pi(x)\\
&=s\int_2^{\infty}\frac{\pi(x)}{x(x^s-1)}\,dx,
\qquad \operatorname{Re}s>1.
\end{aligned}
$$

O termo de fronteira no infinito desaparece porque $\pi(x)\le x$ e

$$
\log\left(\frac1{1-x^{-s}}\right)=O(x^{-\sigma}).
$$

Esta é a identidade central usada por Aycock. Para $s=1+\varepsilon$, com $\varepsilon>0$, sabemos que

$$
\zeta(1+\varepsilon)=\frac1\varepsilon+O(1),
$$

e, portanto,

$$
\log\zeta(1+\varepsilon)
=\log\frac1\varepsilon+O(\varepsilon).
$$

A fórmula sugere que a função $\pi(x)$ deve produzir exatamente essa divergência logarítmica. Se inserirmos formalmente

$$
\pi(x)\approx\frac{x}{\log x},
$$

o comportamento previsto realmente aparece. A intuição está correta. A recíproca, contudo, não é automática.

### O passo heurístico que Euler poderia ter dado

Na linguagem de infinitos empregada por Euler, a divergência da série harmônica e a identidade anterior sugerem, depois de introduzir um corte superior $X$, a comparação formal

$$
\log\log X
\approx
\int_2^X\frac{\pi(t)}{t(t-1)}\,dt.
$$

Se essa comparação for tratada como uma igualdade entre os termos dominantes e diferenciada em relação a $X$, obtemos

$$
\frac1{X\log X}
\approx
\frac{\pi(X)}{X(X-1)}.
$$

Isolando $\pi(X)$,

$$
\pi(X)
\approx
\frac{X-1}{\log X}
\sim
\frac{X}{\log X}.
$$

Esse cálculo não prova o teorema, mas produz exatamente o seu enunciado. É neste sentido — e somente neste — que os resultados de Euler poderiam tê-lo levado à lei assintótica dos primos antes de Gauss.

## O ponto em que a heurística falha

Do fato de uma integral crescer como $\log\log x$ não podemos concluir que seu integrando seja assintótico à derivada de $\log\log x$. A diferenciação não preserva equivalências assintóticas sem hipóteses adicionais.

Um exemplo explícito deixa o problema visível. Considere

$$
F(x)=\log\log x+\frac{\sin(\log x)}{\log x}.
$$

Como o segundo termo tende a zero,

$$
F(x)\sim\log\log x.
$$

Entretanto,

$$
F'(x)
=\frac1{x\log x}
+\frac{\cos(\log x)}{x\log x}
-\frac{\sin(\log x)}{x(\log x)^2},
$$

de modo que

$$
\frac{F'(x)}{1/(x\log x)}
=1+\cos(\log x)-\frac{\sin(\log x)}{\log x}
$$

não possui limite. Logo,

$$
F'(x)\not\sim\frac1{x\log x}.
$$

É precisamente esse tipo de oscilação que uma prova rigorosa deve excluir. A identidade integral de Aycock explica por que $x/\log x$ é o candidato correto, mas não demonstra que $\pi(x)$ tenha esse comportamento.

Há ainda uma segunda cautela: o produto de Euler é uma igualdade de números finitos somente para $\operatorname{Re}s>1$. Escrever diretamente $s=1$ produz a série harmônica e um produto divergente. O limite $s\to1^+$ deve ser tomado apenas depois de estabelecidas as estimativas necessárias.

## Do enunciado à prova: a matemática que viria depois

Até aqui reconstruímos o caminho que poderia conduzir Euler à conjectura e mostramos por que o último passo não é uma demonstração. A partir deste ponto deixamos deliberadamente a matemática do século XVIII. Para manter o quadro matemático completo, apresentaremos a rota moderna que elimina as oscilações e prova o resultado. Ela depende da análise complexa desenvolvida no século XIX e de um princípio tauberiano do século XX; portanto, nada do que segue deve ser retrospectivamente atribuído a Euler.

### A quantidade certa: a função de von Mangoldt

O reparo começa quando, em vez de olhar apenas para $\log\zeta(s)$, diferenciamos sua expansão absolutamente convergente na região $\sigma>1$:

$$
-\frac{\zeta'(s)}{\zeta(s)}
=\sum_p\sum_{k=1}^{\infty}\frac{\log p}{p^{ks}}.
$$

Definimos a função de von Mangoldt por

$$
\Lambda(n)=
\begin{cases}
\log p, & n=p^k\text{ para algum primo }p\text{ e }k\ge1,\\
0, & \text{caso contrário}.
\end{cases}
$$

Então

$$
\boxed{\displaystyle
-\frac{\zeta'(s)}{\zeta(s)}
=\sum_{n=1}^{\infty}\frac{\Lambda(n)}{n^s},
\qquad \operatorname{Re}s>1.}
$$

Introduzimos também a função de Chebyshev

$$
\psi(x)=\sum_{n\le x}\Lambda(n).
$$

Como $\Lambda(n)\ge0$, a função $\psi$ é crescente. Em linguagem de integrais de Stieltjes,

$$
-\frac{\zeta'(s)}{\zeta(s)}
=\int_{1^-}^{\infty}x^{-s}\,d\psi(x).
$$

Agora o problema assume uma forma precisa: mostrar que o polo de $-\zeta'/\zeta$ em $s=1$ força

$$
\psi(x)\sim x.
$$

Esta implicação não resulta de uma diferenciação informal. Ela é um problema tauberiano.

### A continuação de $\zeta$ até a reta $\operatorname{Re}s=1$

Não precisamos, para o Teorema dos Números Primos, de toda a continuação meromorfa da função zeta ao plano complexo. Basta chegar ao semiplano $\operatorname{Re}s>0$.

Para $\sigma>1$, podemos escrever

$$
\zeta(s)
=s\int_1^{\infty}\frac{\lfloor x\rfloor}{x^{s+1}}\,dx.
$$

De fato, cada inteiro $n$ é contado na integral para todo $x\ge n$, e a convergência absoluta justifica a troca entre soma e integral. Como

$$
\lfloor x\rfloor=x-\{x\},
$$

segue que

$$
\boxed{\displaystyle
\zeta(s)=\frac{s}{s-1}
-s\int_1^{\infty}\frac{\{x\}}{x^{s+1}}\,dx.}
$$

A parte fracionária satisfaz $0\le\{x\}<1$. A integral do lado direito converge uniformemente em compactos de $\operatorname{Re}s>0$ e define ali uma função holomorfa. Portanto, essa fórmula prolonga $\zeta$ ao semiplano $\operatorname{Re}s>0$, exceto por um polo simples em $s=1$, de resíduo $1$.

Consequentemente,

$$
\zeta(s)=\frac1{s-1}+h(s),
$$

com $h$ holomorfa perto de $s=1$, e

$$
-\frac{\zeta'(s)}{\zeta(s)}
=\frac1{s-1}+H(s),
$$

onde $H$ é holomorfa numa vizinhança de $1$.

Ainda resta um obstáculo: para que $-\zeta'/\zeta$ não tenha outros polos sobre a reta $\operatorname{Re}s=1$, precisamos provar que

$$
\zeta(1+it)\ne0
\qquad(t\in\mathbb R,\ t\ne0).
$$

### A desigualdade que elimina zeros em $\operatorname{Re}s=1$

É aqui que surge um argumento particularmente bonito. Para $\sigma>1$, a expansão logarítmica do produto de Euler dá

$$
\log|\zeta(\sigma+it)|
=\sum_p\sum_{k=1}^{\infty}
\frac{\cos(kt\log p)}{k p^{k\sigma}}.
$$

Usamos a desigualdade trigonométrica elementar

$$
3+4\cos\theta+\cos(2\theta)
=2(1+\cos\theta)^2\ge0.
$$

Aplicando-a termo a termo com $\theta=kt\log p$, obtemos

$$
3\log\zeta(\sigma)
+4\log|\zeta(\sigma+it)|
+\log|\zeta(\sigma+2it)|\ge0.
$$

Depois de exponenciar,

$$
\boxed{\displaystyle
\zeta(\sigma)^3
|\zeta(\sigma+it)|^4
|\zeta(\sigma+2it)|\ge1.}
$$

Suponhamos, buscando uma contradição, que $\zeta(1+it_0)=0$ para algum $t_0\ne0$. Como $\zeta$ é holomorfa nesse ponto, se o zero tem ordem $m\ge1$, então

$$
|\zeta(\sigma+it_0)|=O((\sigma-1)^m)
\qquad(\sigma\to1^+).
$$

Além disso,

$$
\zeta(\sigma)\sim\frac1{\sigma-1},
$$

enquanto $\zeta(\sigma+2it_0)$ permanece limitada, pois $1+2it_0\ne1$. Logo, o lado esquerdo da desigualdade anterior seria

$$
O\bigl((\sigma-1)^{4m-3}\bigr),
$$

que tende a zero porque $m\ge1$. Isso contradiz o fato de o produto ser sempre maior ou igual a $1$. Portanto,

$$
\boxed{\displaystyle
\zeta(1+it)\ne0\quad\text{para todo }t\ne0.}
$$

Esse é o núcleo analítico das provas clássicas de Hadamard e de la Vallée Poussin. É notável que a exclusão dos zeros na reta $\operatorname{Re}s=1$ possa ser condensada numa desigualdade trigonométrica tão simples, aplicada ao produto descoberto por Euler.

### A ponte que faltava: Wiener–Ikehara

Chegamos ao ponto em que a heurística deve ser substituída por um teorema de passagem entre informação analítica e crescimento aritmético.

> **Teorema de Wiener–Ikehara, forma para séries de Dirichlet.** Seja $a_n\ge0$ e suponha que
> $$
> F(s)=\sum_{n=1}^{\infty}\frac{a_n}{n^s}
> $$
> convirja para $\operatorname{Re}s>1$. Se, para algum $A\ge0$,
> $$
> F(s)-\frac{A}{s-1}
> $$
> admite extensão contínua à reta $\operatorname{Re}s=1$ — em particular, se é holomorfa numa vizinhança dessa reta —, então
> $$
> \sum_{n\le x}a_n\sim Ax.
> $$

A hipótese $a_n\ge0$ é decisiva. Ela impede que oscilações escondidas por uma transformação integral destruam a conclusão pontual — exatamente o problema presente na diferenciação heurística.

Aplicamos o teorema com

$$
a_n=\Lambda(n)
$$

e

$$
F(s)=-\frac{\zeta'(s)}{\zeta(s)}.
$$

Já verificamos todos os pontos:

1. $\Lambda(n)\ge0$;
2. a série de Dirichlet converge para $\operatorname{Re}s>1$;
3. $\zeta$ tem polo simples de resíduo $1$ em $s=1$;
4. $\zeta$ não se anula no restante da reta $\operatorname{Re}s=1$.

Assim,

$$
-\frac{\zeta'(s)}{\zeta(s)}-\frac1{s-1}
$$

é regular sobre a reta $\operatorname{Re}s=1$. O teorema de Wiener–Ikehara fornece

$$
\boxed{\displaystyle \psi(x)=\sum_{n\le x}\Lambda(n)\sim x.}
$$

Esse é o Teorema dos Números Primos em sua forma ponderada.

### De $\psi(x)$ para $\pi(x)$

Para completar a prova, precisamos retirar as potências superiores dos primos e depois remover o peso $\log p$.

Defina

$$
\vartheta(x)=\sum_{p\le x}\log p.
$$

Como $\psi$ conta todas as potências $p^k$, enquanto $\vartheta$ conta apenas os próprios primos,

$$
0\le\psi(x)-\vartheta(x)
=\sum_{\substack{k\ge2\\p^k\le x}}\log p.
$$

Todo primo que aparece nessa diferença satisfaz $p\le\sqrt{x}$. Além disso, para cada primo há no máximo $\log x/\log 2$ expoentes possíveis. Usando apenas $\pi(\sqrt{x})\le\sqrt{x}$, obtemos

$$
\begin{aligned}
0\le\psi(x)-\vartheta(x)
&\le\frac{\log x}{\log 2}
\sum_{p\le\sqrt{x}}\log p\\
&\le C\sqrt{x}(\log x)^2
=o(x).
\end{aligned}
$$

Como $\psi(x)\sim x$, segue que

$$
\vartheta(x)\sim x.
$$

Por integração de Stieltjes,

$$
\pi(x)
=\int_{2^-}^{x}\frac1{\log t}\,d\vartheta(t).
$$

Uma integração por partes dá

$$
\pi(x)
=\frac{\vartheta(x)}{\log x}
+\int_2^x\frac{\vartheta(t)}{t(\log t)^2}\,dt.
$$

O primeiro termo satisfaz

$$
\frac{\vartheta(x)}{\log x}
\sim\frac{x}{\log x}.
$$

No segundo, usamos $\vartheta(t)\sim t$:

$$
\int_2^x\frac{\vartheta(t)}{t(\log t)^2}\,dt
=O\left(\int_2^x\frac{dt}{(\log t)^2}\right)
=O\left(\frac{x}{(\log x)^2}\right)
=o\left(\frac{x}{\log x}\right).
$$

Portanto,

$$
\boxed{\displaystyle
\pi(x)\sim\frac{x}{\log x}.}
$$

Com isso, a demonstração moderna está concluída. Sua presença aqui não pretende sugerir que Euler pudesse executá-la. Ao contrário: ela localiza com precisão a enorme distância entre **adivinhar o enunciado correto** a partir do produto de Euler e **provar** que nenhuma oscilação escondida altera a densidade assintótica dos primos.

## Então, o que exatamente Euler poderia ter feito?

Agora podemos responder sem confundir três afirmações diferentes.

**Primeiro:** Euler certamente possuía o ponto de partida. O produto sobre os primos, a série harmônica, o uso sofisticado de séries infinitas e a fórmula de Euler–Maclaurin pertenciam ao seu universo matemático.

**Segundo:** a identidade

$$
\log\zeta(s)
=s\int_2^{\infty}\frac{\pi(x)}{x(x^s-1)}\,dx
$$

permite descobrir corretamente qual deveria ser a ordem de grandeza de $\pi(x)$. Nesse sentido, o artigo de Aycock mostra de forma convincente como Euler poderia ter **formulado** o Teorema dos Números Primos.

**Terceiro:** formular não é demonstrar. O salto da informação integral para a assíntota pontual requer controle das oscilações. As primeiras demonstrações foram obtidas somente em 1896, independentemente, por Jacques Hadamard e Charles-Jean de la Vallée Poussin, mediante métodos de análise complexa e o estudo dos zeros da função zeta. Na apresentação moderna acima, o passo final é condensado pelo teorema de Wiener–Ikehara, publicado em 1931.

Assim, a conclusão historicamente responsável é esta:

> **Sim, o enunciado do Teorema dos Números Primos estava latente no produto de Euler.** O comportamento da série harmônica e a identidade integral associada à contagem dos primos apontavam naturalmente para a densidade $1/\log x$. Euler poderia, portanto, ter formulado essa lei antes do jovem Gauss. O que não estava disponível era a demonstração.

Essa antecipação seria inteiramente compatível com os resultados e com o estilo de cálculo de Euler. Permanece, contudo, um contrafactual matemático, não uma reivindicação de prioridade histórica.

## Uma curiosidade: a zeta nos inteiros ímpares

No texto [**A prova que Euler perdeu**](https://ailtoncnascimento.github.io/posts/a-prova-que-euler-perdeu/), discutimos outra fronteira euleriana: o comportamento de $\zeta(3)$ e a tentativa de encontrar para os valores ímpares uma expressão comparável à fórmula

$$
\zeta(2m)
=(-1)^{m+1}\frac{B_{2m}(2\pi)^{2m}}{2(2m)!}
$$

dos valores pares.

O produto de Euler fornece imediatamente

$$
\zeta(2m+1)
=\prod_p\frac1{1-p^{-(2m+1)}},
$$

mas não transforma esse número numa combinação finita de constantes conhecidas. Há, entretanto, uma representação integral exata, registrada por Niels Erik Nörlund em 1924:

$$
\boxed{\displaystyle
\zeta(2m+1)
=\frac{(-1)^{m+1}(2\pi)^{2m+1}}{2(2m+1)!}
\int_0^1 B_{2m+1}(t)\cot(\pi t)\,dt,}
$$

válida para todo inteiro $m\ge1$. Aqui $B_n(t)$ é o $n$-ésimo polinômio de Bernoulli, definido por

$$
\frac{ze^{tz}}{e^z-1}
=\sum_{n=0}^{\infty}B_n(t)\frac{z^n}{n!}.
$$

Vale a pena demonstrar a fórmula, pois ela reúne séries de Fourier, ortogonalidade trigonométrica e uma delicada justificativa de convergência.

Para $m\ge1$, a série de Fourier do polinômio de Bernoulli ímpar é

$$
B_{2m+1}(t)
=(-1)^{m+1}\frac{2(2m+1)!}{(2\pi)^{2m+1}}
\sum_{n=1}^{\infty}\frac{\sin(2\pi nt)}{n^{2m+1}}.
$$

Por outro lado,

$$
\int_0^1\sin(2\pi nt)\cot(\pi t)\,dt=1.
$$

Para verificar esta identidade, fazemos $\theta=\pi t$ e usamos

$$
\frac{\sin(2n\theta)}{\sin\theta}
=2\sum_{j=1}^{n}\cos((2j-1)\theta).
$$

Multiplicando por $\cos\theta$ e integrando em $[0,\pi]$, a ortogonalidade dos cossenos elimina todos os termos, exceto $j=1$. O termo restante é

$$
\frac2\pi\int_0^\pi\cos^2\theta\,d\theta=1.
$$

Resta justificar a integração termo a termo, pois $\cot(\pi t)$ tem singularidades em $0$ e $1$. A estimativa

$$
\left|\sin(2\pi nt)\cot(\pi t)\right|
\le2n
$$

implica

$$
\sum_{n=1}^{\infty}
\int_0^1
\left|
\frac{\sin(2\pi nt)\cot(\pi t)}{n^{2m+1}}
\right|dt
\le2\sum_{n=1}^{\infty}\frac1{n^{2m}}<\infty.
$$

O teorema de Fubini para séries permite, portanto, integrar termo a termo. Substituindo a integral trigonométrica, obtemos

$$
\int_0^1B_{2m+1}(t)\cot(\pi t)\,dt
=(-1)^{m+1}
\frac{2(2m+1)!}{(2\pi)^{2m+1}}
\zeta(2m+1),
$$

e basta isolar $\zeta(2m+1)$.

Para $m=1$, como

$$
B_3(t)=t^3-\frac32t^2+\frac12t,
$$

resulta a fórmula exata

$$
\boxed{\displaystyle
\zeta(3)
=\frac{2\pi^3}{3}
\int_0^1
\left(t^3-\frac32t^2+\frac12t\right)
\cot(\pi t)\,dt.}
$$

A singularidade aparente é removível: $B_3(0)=B_3(1)=0$, e o zero do polinômio cancela o polo simples da cotangente em cada extremo.

Essa representação não é uma “forma fechada” algébrica para $\zeta(3)$. Ela desloca a dificuldade aritmética para uma integral exata. Em particular, não demonstra a antiga expectativa de escrever

$$
\zeta(3)
=\alpha(\log 2)^3+\beta\pi^2\log 2,
\qquad \alpha,\beta\in\mathbb Q.
$$

Os valores ímpares continuam resistindo. O contraste é instrutivo: o produto de Euler foi suficientemente forte para revelar a distribuição assintótica dos primos, depois de acrescentada a ponte tauberiana; mas nem ele nem a representação de Nörlund resolvem a natureza aritmética de $\zeta(3)$.

## Conclusão

O artigo de Aycock recupera uma possibilidade histórica muito bonita: Euler já possuía fórmulas capazes de apontar para

$$
\pi(x)\sim\frac{x}{\log x}.
$$

A heurística é suficiente para motivar o enunciado, mas não pode ser promovida a prova apenas diferenciando uma equivalência integral. A demonstração moderna revela a arquitetura que somente seria completada muito depois:

$$
\text{fatoração única}
\longrightarrow
\text{produto de Euler}
\longrightarrow
-\frac{\zeta'}{\zeta}
\longrightarrow
\Lambda(n)
\longrightarrow
\psi(x)
\longrightarrow
\pi(x).
$$

Entre a função zeta e a contagem dos primos aparecem dois pilares ausentes da matemática de Euler: a não anulação de $\zeta$ na reta $\operatorname{Re}s=1$ e um mecanismo tauberiano que transforme informação integral em comportamento pontual. São eles que convertem a previsão plausível numa demonstração.

Esse é o sentido preciso da pergunta do título. Não estamos dizendo que uma prova estivesse pronta e escondida numa linha dos escritos de Euler. Estamos dizendo que a ideia necessária para **enunciar a lei assintótica** — converter a decomposição dos inteiros em informação sobre a frequência dos primos — já estava em suas mãos. Se tivesse dado mais um passo heurístico, Euler poderia ter antecipado, antes do jovem Gauss, o enunciado do Teorema dos Números Primos.

## Referências e leituras

- Aycock, A. *How Euler Could Have Done It: Euler and a Heuristic Derivation of the Prime Number Theorem*. **Euleriana**, v. 6, n. 1, p. 97–104, 2026. [DOI: 10.56031/2693-9908.1102](https://doi.org/10.56031/2693-9908.1102).
- Euler, L. *Variae observationes circa series infinitas* (E72). *Commentarii Academiae Scientiarum Petropolitanae*, v. 9, p. 160–188, 1744; escrito em 1737. [Euler Archive](https://scholarlycommons.pacific.edu/euler-works/72/).
- Euler, L. *Introductio in analysin infinitorum*, v. 1. Lausanne: Marc-Michel Bousquet, 1748.
- Gauss, C. F. Carta a Johann Franz Encke, 24 dez. 1849. Reproduzida em *Werke*, v. 2, p. 444–447.
- Hadamard, J. *Sur la distribution des zéros de la fonction $\zeta(s)$ et ses conséquences arithmétiques*. *Bulletin de la Société Mathématique de France*, v. 24, p. 199–220, 1896. [DOI: 10.24033/bsmf.545](https://doi.org/10.24033/bsmf.545).
- de la Vallée Poussin, C.-J. *Recherches analytiques sur la théorie des nombres premiers*. *Annales de la Société Scientifique de Bruxelles*, v. 20, p. 183–256, 1896.
- Ikehara, S. *An Extension of Landau's Theorem in the Analytical Theory of Numbers*. *Journal of Mathematics and Physics*, v. 10, p. 1–12, 1931. [DOI: 10.1002/sapm19311011](https://doi.org/10.1002/sapm19311011).
- Wiener, N. *Tauberian Theorems*. *Annals of Mathematics*, v. 33, n. 1, p. 1–100, 1932.
- Newman, D. J. *Simple Analytic Proof of the Prime Number Theorem*. *The American Mathematical Monthly*, v. 87, n. 9, p. 693–696, 1980. [DOI: 10.1080/00029890.1980.11995126](https://doi.org/10.1080/00029890.1980.11995126).
- Zagier, D. *Newman's Short Proof of the Prime Number Theorem*. *The American Mathematical Monthly*, v. 104, n. 8, p. 705–708, 1997. [Texto disponível](https://people.mpim-bonn.mpg.de/zagier/files/doi/10.2307/2975232/fulltext.pdf).
- Titchmarsh, E. C.; Heath-Brown, D. R. *The Theory of the Riemann Zeta-Function*. 2. ed. Oxford: Clarendon Press, 1986.
- Apostol, T. M. *Introduction to Analytic Number Theory*. New York: Springer, 1976.
- Nörlund, N. E. *Vorlesungen über Differenzenrechnung*. Berlin: Springer, 1924, fórmula (81*), p. 66. [Texto digitalizado](https://archive.org/details/in.ernet.dli.2015.492994).
- NIST Digital Library of Mathematical Functions. *Riemann Zeta Function: Integer Arguments*, §25.6(i), Eq. 25.6.6. [DLMF 25.6.6](https://dlmf.nist.gov/25.6.E6).
- Nascimento, A. C. [*A prova que Euler perdeu*](https://ailtoncnascimento.github.io/posts/a-prova-que-euler-perdeu/), 21 jul. 2026.
