---
title: "73, o melhor número, e os primos de Sheldon"
date: 2026-08-26 10:00:00 -0300
categories: [Miscelânea, Teoria dos Números]
tags: [primos, primos de sheldon, conjectura de sheldon, emirps, primos reversíveis, teorema dos números primos]
math: true
---

Às vezes uma boa história de matemática começa num jantar. A minha começou numa mesa do Mangaí, em Recife, na véspera de um colóquio que eu daria no Departamento de Matemática da UFPE.

Eu estava com meu amigo, o professor Davi Lima, da UFAL, e fazíamos o que dois matemáticos costumam fazer quando ficam sem assunto: passamos a olhar os números de quatro dígitos impressos nos cartõezinhos de consumo do restaurante e a apostar se cada um era primo. Era um passatempo bobo — até que um dos cartões trouxe um número que não era apenas primo: o seu **reverso**, lido de trás para frente, também era primo.

Aquilo mudou o tom da noite. Da brincadeira nasceu a pergunta que nos ocupou o resto do jantar e que eu levaria para o quadro no dia seguinte:

> Existem infinitos primos cujo reverso também é primo?

Guardei a pergunta. Ela costura, de um jeito que eu não esperava, o número favorito de um físico fictício e um problema de pesquisa muito real.

## 73, o melhor número

Quem assiste *The Big Bang Theory* conhece a cena. Num episódio da série, Sheldon Cooper decreta, com a habitual falta de modéstia, que só existe uma resposta correta para "qual é o melhor número?", e a resposta é **73**. Ele justifica: 73 é o 21º número primo; o seu espelho, 37, é o 12º; e 21, por sua vez, é o produto de 7 por 3. De brinde, observa que, em binário, 73 se escreve $1001001$ — um palíndromo, igual de trás para frente. Cada uma dessas afirmações é verdadeira.

Há ainda uma coincidência deliciosa, que os próprios matemáticos que estudaram o assunto fizeram questão de registrar: o episódio em que Sheldon elogia o 73 é, ele mesmo, o 73º episódio da série.

## Duas propriedades e um "primo de Sheldon"

Para transformar a bravata em matemática, precisamos de duas definições. Escrevo $p(n)$ para o $n$-ésimo primo (assim $p(1)=2$, $p(3)=5$) e $m(x)$ para o **reverso** de $x$, obtido invertendo a ordem dos dígitos (por exemplo, $m(25)=52$).

A **propriedade do espelho**: o $n$-ésimo primo a satisfaz quando

$$
m(p(n)) = p(m(n)).
$$

Refletir o primo devolve outro primo — e mais: exatamente o primo que ocupa a posição refletida.

A **propriedade do produto**: escrevendo $\Pi(x)$ para o produto dos dígitos de $x$, o $n$-ésimo primo a satisfaz quando

$$
\Pi(p(n)) = n.
$$

Um **primo de Sheldon** cumpre as duas ao mesmo tempo. E o 73 cumpre, redondamente:

$$
\Pi(73) = 7 \times 3 = 21, \qquad 73 = p(21),
$$

$$
m(73) = 37 = p(12), \qquad m(21) = 12.
$$

Ou seja, $\Pi(p(21)) = 21$ e $m(p(21)) = p(m(21))$ — as duas propriedades, verificadas na mão.

Vale sentir o quanto a propriedade do produto é restritiva. O produto dos dígitos só pode ter fatores primos entre 2, 3, 5 e 7 — é sempre um número 7-suave —, e basta um único dígito zero para zerar tudo. Logo o índice $n$ precisa ser 7-suave, o que elimina quase todo mundo: dos primeiros mil milhões de primos, apenas cerca de 3.039 sobrevivem só a esse critério — uns 99,9997% caem de imediato.

## Um limite que cabe numa demonstração

O mais bonito é que dá para cercar os candidatos com um argumento curto. Só a propriedade do produto já obriga qualquer primo de Sheldon a ser menor que $10^{45}$.

**Proposição.** *Se $p(n)$ satisfaz a propriedade do produto, então $p(n) < 10^{45}$.*

**Ideia da prova.** Digamos que $p(n)$ tenha $k$ dígitos, com primeiro dígito $a$. Como $n$ é o produto dos dígitos de $p(n)$, temos

$$
n = \Pi(p(n)) \le a \cdot 9^{\,k-1}.
$$

Por outro lado, uma desigualdade explícita de Rosser e Schoenfeld garante que $\pi(x) > x/\log x$ para todo $x \ge 17$. Como $n = \pi(p(n))$ é justamente a posição de $p(n)$, e como $t \mapsto t/\log t$ é crescente, segue que

$$
n > \frac{p(n)}{\log p(n)} \ge \frac{a \cdot 10^{\,k-1}}{\log\!\left(a \cdot 10^{\,k-1}\right)},
$$

onde usamos $p(n) \ge a\cdot 10^{\,k-1}$ (afinal, são $k$ dígitos). Juntando as duas cotas,

$$
a \cdot 9^{\,k-1} > \frac{a \cdot 10^{\,k-1}}{\log\!\left(a \cdot 10^{\,k-1}\right)} \quad\Longrightarrow\quad \log a + (k-1)\log 10 > \left(\tfrac{10}{9}\right)^{k-1}.
$$

O lado esquerdo cresce linearmente em $k$; o direito, exponencialmente. Logo a desigualdade falha para $k$ grande — e uma indução simples mostra que ela falha para todo $k \ge 46$. Portanto $p(n)$ tem no máximo 45 dígitos. $\blacksquare$

Repare no espírito da coisa: uma piada de seriado foi confinada, com poucas linhas de análise, a um universo *finito* de números.

## A conjectura de Sheldon

A afirmação implícita — de que 73 é o único primo de Sheldon — foi tornada explícita em novembro de 2015 por Jessie Byrnes, Chris Spicer e Alyssa Turnquist, que a batizaram de **Conjectura de Sheldon**. E aqui vem o que eu acho mais encantador: uma bravata solta por um físico *fictício* numa comédia de TV virou objeto de estudo de matemáticos de verdade.

A conjectura ficou em aberto por um tempo respeitável: nomeada em 2015, só foi resolvida em 2019 — cerca de **quatro anos** como conjectura formal, e quase **nove anos** depois de o episódio de 2010 ter plantado a semente. A prova veio de Carl Pomerance — um dos grandes nomes da teoria analítica e computacional dos números, que costuma citar Paul Erdős como sua maior influência — em parceria com Chris Spicer, no artigo *Proof of the Sheldon Conjecture* (*American Mathematical Monthly*, vol. 126, 2019).

> **Teorema (Pomerance–Spicer, 2019).** 73 é o único primo de Sheldon.

Depois de cercar tudo abaixo de $10^{45}$, faltava varrer o intervalo finito. Como calcular $p(n)$ diretamente para $n$ gigantesco é inviável, troca-se $p(n)$ pela inversa da integral logarítmica, $\mathrm{Li}^{-1}(n)$, e controla-se com estimativas explícitas o quão perto elas ficam. No fim, o 73 fica sozinho. E o motor de toda essa manobra é um só: o Teorema dos Números Primos.

## O Teorema dos Números Primos: o coração da história

Se há uma estrela nesta história, não é o 73 — é o teorema que permite domá-lo.

Tudo começa com uma precocidade absurda. Em 1792, aos **15 anos**, Carl Friedrich Gauss observou que os primos rareiam a uma taxa governada por $1/\log x$ e passou a comparar $\pi(x)$ — a quantidade de primos até $x$ — com a integral logarítmica $\mathrm{Li}(x) = \int_2^{x} \frac{dt}{\log t}$. A tabela abaixo, uma versão moderna daquela ideia, mostra por que a intuição do menino era tão boa: $\mathrm{Li}(x)$ acompanha $\pi(x)$ casa por casa, muito melhor do que a aproximação mais ingênua $x/\log x$.

| $x$ | $\pi(x)$ | $\mathrm{li}(x)$ | $x/\log x$ |
|:--|--:|--:|--:|
| 10¹ | 4 | 5.12 | 4.34 |
| 10² | 25 | 29.08 | 21.71 |
| 10³ | 168 | 176.56 | 144.76 |
| 10⁴ | 1229 | 1245.09 | 1085.74 |
| 10⁵ | 9592 | 9628.76 | 8685.89 |
| 10⁶ | 78498 | 78626.50 | 72382.41 |
| 10⁷ | 664579 | 664917.36 | 620420.69 |
| 10⁸ | 5761455 | 5762208.33 | 5428681.02 |
| 10⁹ | 50847534 | 50849233.90 | 48254942.43 |
| 10¹⁰ | 455052511 | 455055613.54 | 434294481.90 |
| 10¹¹ | 4118054813 | 4118066399.58 | 3948131653.67 |
| 10¹² | 37607912018 | 37607950279.76 | 36191206825.27 |
| 10¹³ | 346065536839 | 346065645890.05 | 334072678387.12 |
| 10¹⁴ | 3204941750802 | 3204942065692.94 | 3102103442166.08 |
| 10¹⁵ | 29844570422669 | 29844571475286.54 | 28952965460216.79 |
| 10¹⁶ | 279238341033925 | 279238344248555.75 | 271434051189532.39 |
| 10¹⁷ | 2623557157654233 | 2623557165610820.07 | 2554673422960304.87 |
| 10¹⁸ | 24739954287740860 | 24739954309690413.98 | 24127471216847323.76 |
| 10¹⁹ | 234057667276344607 | 234057667376222382.22 | 228576043106974446.13 |
| 10²⁰ | 2220819602560918840 | 2220819620780463483.55 | 2171472409516259138.26 |
| 10²¹ | 21127269486018731928 | 21127269486616126182.33 | 20680689614440563221.48 |
| 10²² | 201467286689315906290 | 201467286691248261498.15 | 197406582683296285295.97 |

O padrão que a tabela sugere é o **Teorema dos Números Primos**:

$$
\lim_{x\to\infty} \frac{\pi(x)}{x/\log x} = 1,
$$

equivalente a dizer que $\pi(x)$ é assintótica a $\mathrm{Li}(x)$. Como corolário, o $n$-ésimo primo satisfaz $p(n) \approx n\log n$. Por exemplo, esse corolário estima o milionésimo primo em $10^{6}\ln(10^{6})$, ou seja, cerca de 13.815.510 — enquanto o valor exato é 15.485.863. Perto, mas não na mosca: é justamente essa diferença fina que a demonstração da Conjectura de Sheldon precisa controlar.

Conjecturado por Gauss e Legendre, o teorema resistiu por **mais de cem anos**. Só em 1896 — mais de um século depois da observação de Gauss — ele foi demonstrado, independentemente, por Jacques Hadamard e Charles de la Vallée Poussin, com análise complexa pesada, apoiada nas propriedades da função zeta de Riemann.

E há um segundo ato memorável. Muitos, incluindo G. H. Hardy, acreditavam que o teorema era "profundo" por natureza e jamais teria uma prova elementar. Em 1948–49, Atle Selberg e Paul Erdős provaram que estavam errados: obtiveram uma demonstração **elementar**, sem análise complexa. O episódio, porém, virou uma célebre disputa de prioridade entre os dois. Selberg recebeu a **Medalha Fields de 1950**, em boa parte por esse trabalho; Erdős — que, ao contrário do que às vezes se diz, não dividiu a medalha — foi laureado com o Prêmio Cole de Teoria dos Números em 1951. Hoje o resultado é creditado a ambos.

Note o fio que amarra tudo: é exatamente esse teorema, em sua forma explícita e quantitativa, que Pomerance e Spicer usam para prender os primos de Sheldon abaixo de $10^{45}$ e para aproximar $p(n)$ por $\mathrm{Li}^{-1}(n)$. O 73 só se rende porque, um século e meio antes, um garoto de 15 anos soube olhar para uma tabela.

## De volta ao jantar: emirps e primos reversíveis

E a pergunta que o Davi e eu levantamos no Mangaí? Ela é, com todas as letras, o problema dos **emirps** — "prime" (primo, em inglês) escrito de trás para frente. Um emirp é um primo $p$ cujo reverso $m(p)$ também é primo e *diferente* de $p$ (os primos palíndromos, como 131 ou 757, ficam de fora por definição, já que para eles $m(p)=p$).

Uma observação simples já organiza a busca: se $p > 5$ é um emirp, o seu primeiro dígito só pode ser 1, 3, 7 ou 9. O motivo é que o último dígito de $m(p)$ é o primeiro dígito de $p$ — e um primo maior que 5 não pode terminar em dígito par nem em 5.

Os primeiros emirps deixam o 37 e o 73 reaparecerem, fiéis:

| Índice | $p$ | $m(p)$ |
|--:|--:|--:|
| 1 | 13 | 31 |
| 2 | 17 | 71 |
| 3 | 31 | 13 |
| 4 | 37 | 73 |
| 5 | 71 | 17 |
| 6 | 73 | 37 |
| 7 | 79 | 97 |
| 8 | 97 | 79 |
| 9 | 107 | 701 |
| 10 | 113 | 311 |
| 11 | 149 | 941 |
| 12 | 157 | 751 |
| 13 | 167 | 761 |
| 14 | 179 | 971 |
| 15 | 199 | 991 |

E qual é a situação do problema? **Em aberto.** Não se sabe demonstrar que existem infinitos emirps, nem que são finitos — há listas com milhares de exemplos (catalogados, por exemplo, na sequência A006567 da OEIS) e forte evidência computacional, mas nenhum teorema de infinitude. O tema aparece já na matemática recreativa de Martin Gardner e segue vivo na pesquisa séria: além do trabalho que menciono a seguir, há contribuições recentes, como a de Chourasiya e colaboradores sobre palíndromos livres de potências e primos reversíveis (2025). Para se ter ideia do tamanho da dificuldade, sequer sabemos se existem infinitos primos palíndromos.

É aqui que a nossa pergunta de mesa de bar encosta na fronteira da pesquisa. Em 2024, Cécile Dartyge, Bruno Martin, Joël Rivat, Igor Shparlinski e Cathy Swaenepoel publicaram no *Journal of the London Mathematical Society* o artigo *Reversible primes*, dedicado exatamente a isso. Trabalhando sobretudo na base 2, eles chamam de $\Theta(n)$ a quantidade de primos reversíveis com $n$ bits e avançam em várias frentes — sem, contudo, fechar o problema central:

- não conseguem provar que há infinitos primos reversíveis (isso continua em aberto), mas obtêm um limitante superior da ordem esperada, $\Theta(n) \ll 2^n/n^2$;
- provam que existem infinitos **quase-primos reversíveis**: infinitos números de $n$ bits tais que o número *e* o seu reverso têm, cada um, no máximo 8 fatores primos — um resultado obtido com um crivo bidimensional feito sob medida;
- estabelecem uma fórmula assintótica para a contagem de inteiros reversíveis *livres de quadrados*;
- e, apoiados em heurística e em cálculo até 50 bits, conjecturam que $\Theta(n) = (3+o(1))\,\dfrac{2^{n-1}}{(\log 2^n)^2}.$

Em outras palavras: hoje sabemos capturar quase-primos e acertar a ordem de grandeza, mas provar que os primos reversíveis genuínos nunca acabam continua fora do alcance. O problema pertence a uma família badalada — a dos primos com restrições sobre os dígitos, onde brilham resultados como os de Maynard (primos sem certos dígitos) e de Mauduit e Rivat (soma dos dígitos dos primos).

## O que um jantar de matemáticos gera

O Davi levou a pergunta a sério. De volta à UFAL, decidiu propô-la como tema aos seus alunos de iniciação científica e de pós-graduação. Foi assim que um jantar que começou apostando se números de cartões de consumo eram primos terminou gerando temas de pesquisa — e enriquecendo, no dia seguinte, a palestra que eu daria na UFPE.

Paulo Ribenboim gostava de chamar os primos de "amigos que causam problemas". A trajetória do 73 é o emblema perfeito disso: um número que um personagem de ficção declarou o melhor de todos virou teorema; e uma brincadeira à mesa de um restaurante foi tocar num problema que ninguém no planeta sabe resolver. Entre a certeza de que o 73 é único e o mistério de saber se os emirps jamais terminam mora, inteirinho, o encanto da teoria dos números.

## Referências

- Byrnes, J., Spicer, C., Turnquist, A. *The Sheldon Conjecture*. Math Horizons **23**(2), 12–15, 2015.
- Pomerance, C., Spicer, C. *Proof of the Sheldon Conjecture*. American Mathematical Monthly **126**(8), 688–698, 2019.
- Dartyge, C., Martin, B., Rivat, J., Shparlinski, I. E., Swaenepoel, C. *Reversible primes*. Journal of the London Mathematical Society **109**(3), e12883, 2024.
- Chourasiya, S. et al. *Power-free palindromes and reversed primes*. arXiv:2503.21136, 2025.
- Hadamard, J. *Sur la distribution des zéros de la fonction $\zeta(s)$ et ses conséquences arithmétiques*. Bull. Soc. Math. France **24**, 199–220, 1896.
- de la Vallée Poussin, C. J. *Recherches analytiques sur la théorie des nombres premiers*. Ann. Soc. Sci. Bruxelles **20**, 1896.
- Selberg, A. *An elementary proof of the prime-number theorem*. Annals of Mathematics **50**, 305–313, 1949.
- Erdős, P. *On a new method in elementary number theory which leads to an elementary proof of the prime number theorem*. Proc. Nat. Acad. Sci. USA **35**, 374–384, 1949.
- Rosser, J. B., Schoenfeld, L. *Approximate formulas for some functions of prime numbers*. Illinois J. Math. **6**, 64–94, 1962.
- Crandall, R., Pomerance, C. *Prime Numbers: A Computational Perspective*. 2ª ed., Springer, 2005.
- Ribenboim, P. *The Little Book of Bigger Primes*. 2ª ed., Springer, 2004.
- Gardner, M. *The Magic Numbers of Dr. Matrix*. Prometheus Books, 1985.
- OEIS: A006567 (emirps), A074832 (primos reversíveis na base 2), A007500 (primos reversíveis na base 10).
