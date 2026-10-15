---
title: "Dia 6 de outubro de 2026: o dia que mudou a matemática para sempre"
date: 2026-10-15 17:00:00 -0300
categories: [Miscelânea, Matemática]
tags: [inteligência artificial, OpenAI, Terence Tao, hipótese de Riemann, Navier-Stokes, Lean, Hilbert, filosofia da matemática, futuro da matemática]
math: true
description: "Na noite de 6 de outubro, a OpenAI publicou 722 manuscritos de matemática gerados por um modelo interno. Este texto tenta separar o que sabemos do que não sabemos — e são muito mais as perguntas do que as respostas."
---

> «Muito em breve teremos demonstrações que ninguém compreende.»
>
> — Jacob Tsimerman, Medalha Fields de 2026, em entrevista ao podcast *Theories of Everything* (agosto de 2026)

> **Continuação da série sobre matemática e inteligência artificial.** Ela começou em julho com o [contraexemplo da Conjectura Jacobiana](/posts/conjectura-jacobiana-contraexemplo-ia/), seguiu com o [contraexemplo da conjectura de Goemans](/posts/contraexemplo-conjectura-goemans-fluxos/) e com a maneira como [Terence Tao desmontou o "milagre"](/posts/tao-blog-milagre-desmontado/) do primeiro, passou pelo [diagrama de Tao no ICM](/posts/matematica-na-era-da-ia/), pela [hipótese de Riemann](/posts/hipotese-de-riemann-avanco-inesperado/) e pela trilogia sobre Navier–Stokes ([I](/posts/navier-stokes-i-anatomia-de-um-problema-do-milenio/), [II](/posts/navier-stokes-ii-a-controversia-contada-pelos-documentos/), [III](/posts/navier-stokes-iii-o-que-significa-ser-matematico-na-era-da-ia/)). Todos os textos estão reunidos na [Miscelânea](/miscelanea/), e vale lê-los em ordem: cada um registra o que se sabia naquele momento, e é instrutivo ver quanto disso já mudou. Boa parte do material vem da palestra *Matemática na Era da I.A.* que apresentei no V EMVAG, em Picos.

Escolhi o título deste texto com plena consciência do risco que ele corre. "O dia que mudou a matemática para sempre" é o tipo de frase que envelhece mal, e eu passei os últimos três meses, nesta série, pedindo cautela com manchetes. Mas, depois de uma semana relendo o que foi publicado na noite de 6 de outubro e tudo o que veio em seguida, não encontrei outra maneira honesta de nomear o que aconteceu.

A revista *Science* chegou à mesma conclusão, e com uma ressalva que eu gostaria de adotar como subtítulo: a OpenAI acaba de mudar a matemática para sempre — **exatamente como, ninguém sabe ainda**. Este texto é sobre a segunda metade dessa frase. Vou tentar organizar o que sabemos, o que achamos que sabemos e, sobretudo, o que não sabemos. A terceira lista é, de longe, a maior.

## O que aconteceu

Na noite de terça-feira, 6 de outubro de 2026, a OpenAI abriu no GitHub um repositório chamado `openai/math` e depositou nele **722 manuscritos**, organizados em **372 famílias de resultados**, distribuídos por 17 áreas da matemática e da ciência da computação teórica. Não houve entrevista coletiva. Houve um *commit*.

Segundo a própria empresa, o material foi produzido por um modelo interno, não lançado ao público, ao qual foram submetidos **cerca de 4 000 problemas em aberto**. Cada família reúne um resultado principal e seus companheiros: corolários, demonstrações alternativas, consequências. O custo médio de cada resultado, diz a OpenAI, foi da ordem de três horas de raciocínio do modelo. Acompanham os manuscritos: uma biblioteca de formalizações em Lean, que cobria na abertura apenas uma fração dos resultados; dez resumos abreviados do "raciocínio" do modelo; e uma licença Apache 2.0, que permite a qualquer um usar o material.

Para entender o peso disso, vale lembrar um slide que mostrei em Picos: o gráfico do número de problemas de Erdős resolvidos por ano, de 1934 a 2026. Durante décadas, um punhado por ano. Em 2025, um pico de **24**, que na época me pareceu a imagem perfeita do que Tao chamou de passagem "da escassez à abundância de demonstrações". Na noite de 6 de outubro, num único repositório, apareceram 372 famílias de resultados. O pico de 2025, que eu apresentava como uma enxurrada, virou uma linha de base.

A cronologia das semanas em torno da data ajuda a entender por que a reação foi tão intensa:

| Data | O que aconteceu |
| --- | --- |
| 8 de setembro | A OpenAI anuncia o *blow-up* em tempo finito para Navier–Stokes com força suave ([texto I](/posts/navier-stokes-i-anatomia-de-um-problema-do-milenio/)). |
| 21 de setembro | Criação do Grupo Consultivo sobre Matemática e IA (AGMAI), sediado no Instituto de Estudos Avançados de Princeton, com nove matemáticos, entre eles Timothy Gowers e Edward Witten. A OpenAI afirma que o mesmo modelo resolveu mais de cem problemas. |
| 29 de setembro | O AGMAI publica diretrizes para a divulgação responsável de matemática gerada por IA. Entre elas: preferiria que os laboratórios **não** testassem problemas abertos em modelos internos, e recomenda acesso equitativo aos modelos. |
| 6 de outubro, à noite | O repositório `openai/math` vai ao ar. No mesmo dia: a nota do AGMAI sobre a divulgação; um artigo no arXiv mostrando discrepâncias entre a demonstração de Navier–Stokes e seu código Lean; e uma resposta do Conjecture Institute à carta dos medalhistas Fields. |
| 7 de outubro | A Associação pela Matemática Humana (AHM) pede aos matemáticos que deixem de colaborar com a OpenAI. A OpenAI retira **três** manuscritos por um erro de sinal e revisa outros **catorze**. |
| 9 de outubro | Terence Tao profere em Caltech a palestra pública *Math 2.0*. |
| 13 de outubro | A *Science* publica a reportagem cuja manchete adotei como subtítulo. |
| 14 de outubro | Hugo Duminil-Copin, Medalha Fields de 2022, conta no podcast do *Numberphile* que chorou na noite do dia 6. |

Antes de qualquer opinião, vamos olhar para dentro do repositório. Escolhi três manuscritos: um belo, um monumental e um que caiu.

## Primeira vitrine: quão perto uma fração consegue perseguir $\pi$

Sabemos desde Lambert, em 1761, que $\pi$ não pode ser escrito como uma fração. Mas há uma pergunta mais fina: **quão de perto uma fração consegue imitá-lo?**

Considere 355/113, a aproximação que o astrônomo chinês Zu Chongzhi já conhecia no século V. Ela difere de $\pi$ por cerca de $2{,}67\times 10^{-7}$ — menos de três décimos de milionésimo. É uma precisão espantosa para um denominador de três algarismos. Aproximações melhores existem, é claro. Mas **o quão melhores elas podem ficar**, em função do tamanho do denominador?

A régua natural vem de um teorema de Dirichlet, de 1842: para **todo** número irracional $x$ existem infinitas frações $p/q$ com

$$
\left\lvert x-\frac{p}{q}\right\rvert<\frac{1}{q^{2}}.
$$

O expoente 2 é, portanto, o mínimo que qualquer irracional garante. A pergunta interessante é se um número específico deixa fazer melhor — se existem infinitas frações com erro menor que $1/q^{\nu}$ para algum $\nu>2$. O supremo dos $\nu$ para os quais isso acontece chama-se **expoente de irracionalidade** do número, e se escreve $\mu(x)$. Todo irracional tem $\mu(x)\ge 2$; os números de Liouville, construídos justamente para serem aproximáveis de maneira escandalosa, têm $\mu=\infty$; e, num sentido preciso, quase todo número real tem $\mu$ exatamente igual a $2$.

Para $\pi$, a história é uma corrida de limitantes superiores. Kurt Mahler provou em 1953 que $\mu(\pi)\le 42$. O número foi caindo ao longo de setenta anos — Mignotte, Chudnovsky, Hata, Salikhov — até que Doron Zeilberger e Wadim Zudilin chegaram, em 2019, a $\mu(\pi)\le 7{,}1032\ldots$ Os próprios autores descreveram a busca como um esporte competitivo. Ninguém sabia se o valor verdadeiro era 2, ou 3, ou 7.

O manuscrito 017 do repositório, datado de 24 de setembro, afirma que $\mu(\pi)=2$. Em linguagem explícita: para todo $\varepsilon>0$, todas as frações $p/q$ com denominador suficientemente grande satisfazem

$$
\left\lvert \pi-\frac{p}{q}\right\rvert\ \ge\ \frac{1}{q^{2+\varepsilon}}.
$$

O que isso diz, e o que não diz, merece cuidado — porque é exatamente o tipo de nuance que as manchetes apagam.

O exemplo de 355/113 ajuda. Multiplicando o erro por $113^{2}$, obtemos cerca de 0,0034: a fração é uns trezentos vezes melhor que o "esperado" pela régua de Dirichlet. A razão está na fração contínua de $\pi$,

$$
\pi=[3;\,7,\,15,\,1,\,292,\,1,\,1,\,1,\,2,\,1,\,3,\,1,\,\ldots],
$$

em que o coeficiente 292 aparece logo depois do ponto em que se corta para obter 355/113. Coeficientes grandes produzem aproximações excepcionais. O teorema **não** proíbe que isso volte a acontecer — não afirma que os coeficientes de $\pi$ são limitados, nem que exista uma constante fixa $c$ com $\lvert\pi-p/q\rvert\ge c/q^{2}$ para todas as frações. Afirma algo mais modesto e mais profundo: que esses golpes de sorte não podem crescer **mais depressa que qualquer potência** do denominador. Nenhuma potência extra fixa, além de $1/q^{2}$, descreve a precisão de infinitas frações. Apesar de seus dígitos infinitos e imprevisíveis, $\pi$ obedece a um limite preciso sobre quão de perto as frações conseguem persegui-lo. Nisso, ele é um número absolutamente típico.

A formalização em Lean cobre esse enunciado. O manuscrito tira ainda uma consequência sobre a famosa série de Flint Hills, $\sum_{n\ge1} 1/(n^{3}\sin^{2} n)$, cuja convergência estava ligada ao expoente de $\pi$ — mas essa parte, registra a própria documentação, fica **fora** do enunciado formalizado.

Guarde essa distinção. Ela vai voltar.

## Segunda vitrine: os zeros de $\zeta$, presos numa faixa

Se o resultado sobre $\pi$ é belo, o manuscrito 003 é de outra escala. Seu título: *The Quasi-Riemann Hypothesis: A Zero-Free Half-Plane* $\operatorname{Re} s>7/8$. São 199 páginas, datadas de 30 de setembro, com um companheiro de 49 páginas, de 5 de outubro, que isola a primeira etapa da demonstração. Foi um dos dois manuscritos que abri de perto, às pressas, para a parte de última hora da palestra de Picos — e vale a pena gastar mais tempo com ele aqui do que com qualquer outro, porque é nele que a pergunta "isto é ou não uma ideia nova?" fica mais aguda.

### Onde podem estar os zeros

Para quem acompanhou o [texto de agosto sobre a hipótese de Riemann](/posts/hipotese-de-riemann-avanco-inesperado/), o cenário é conhecido. A função zeta,

$$
\zeta(s)=\sum_{n=1}^{\infty}\frac{1}{n^{s}},\qquad \operatorname{Re} s>1,
$$

estendida a todo o plano complexo, tem seus zeros "não triviais" confinados na faixa crítica $0<\operatorname{Re} s<1$, simetricamente em relação à reta $\operatorname{Re} s=1/2$. A hipótese de Riemann, de 1859, afirma que todos estão **sobre** essa reta.

Desde 1896, quando Hadamard e de la Vallée Poussin provaram o [Teorema dos Números Primos](/posts/euler-poderia-ter-enunciado-o-teorema-dos-numeros-primos/), sabemos que não há zeros sobre a reta $\operatorname{Re} s=1$. Em 1899, de la Vallée Poussin obteve uma região livre de zeros à esquerda dela, da forma $\sigma>1-c/\log\lvert t\rvert$. A melhor região conhecida até setembro era a de Vinogradov e Korobov, de 1958:

$$
\zeta(\sigma+it)\neq 0\quad\text{sempre que}\quad \sigma>1-\frac{c}{(\log\lvert t\rvert)^{2/3}\,(\log\log\lvert t\rvert)^{1/3}}.
$$

Note o que essa fórmula diz e o que não diz. A largura da região **tende a zero** à medida que a altura $\lvert t\rvert$ cresce: ela encosta na reta $\operatorname{Re} s=1$ lá em cima. Por 127 anos, de 1899 a 2026, todas as regiões livres de zeros que conhecíamos tinham essa forma — finas, cada vez mais finas. Os avanços modernos, como o de Guth e Maynard em 2024, foram sobre **densidade** de zeros: quantos zeros, no máximo, podem existir à direita de uma reta. Densidade não exclui nenhum zero em particular.

A **hipótese quase-Riemann** pede o mínimo que faltava: um número fixo $\sigma_0<1$ tal que $\zeta$ não tenha zeros em $\operatorname{Re} s>\sigma_0$, **em toda altura**. Até setembro, nenhum $\sigma_0$ havia sido obtido.

### O enunciado

> **Teorema 1.1 (OpenAI, 30 de setembro de 2026, não arbitrado).** Toda função $L$ de Hecke de ordem finita sobre o corpo $F=\mathbb{Q}(\sqrt{-3})$, e toda função $L$ de Dirichlet — inclusive $\zeta(s)$ —, não tem zeros no semiplano $\operatorname{Re} s>7/8$, admitindo-se o polo em $s=1$ do caractere principal.

Pela equação funcional, que reflete os zeros em torno da reta 1/2, os zeros não triviais de $\zeta$ ficam presos na faixa

$$
\frac18\ \le\ \operatorname{Re}\rho\ \le\ \frac78 .
$$

Isso ainda deixa 3/8 de folga de cada lado da reta crítica — a hipótese de Riemann continua aberta, e o próprio manuscrito diz isso com todas as letras. Mas, se a prova estiver correta, é a primeira vez desde Hadamard e de la Vallée Poussin que a região sem zeros **deixa de encostar** na reta $\operatorname{Re} s=1$. No slide de Picos escrevi que seria a maior conquista da teoria analítica dos números em mais de 120 anos, e não retiro a frase — com o condicional que ela carregava.

### Por que $\mathbb{Q}(\sqrt{-3})$?

A primeira coisa que salta aos olhos no enunciado é um corpo de números que não aparece na pergunta. Por que uma demonstração sobre $\zeta$ passa pelos inteiros de Eisenstein, os números $a+b\omega$ com $\omega=e^{2\pi i/3}$ uma raiz cúbica primitiva da unidade?

A resposta é que $\mathbb{Q}(\sqrt{-3})$ é o lar natural da **reciprocidade cúbica**, e nele existe um objeto que não tem análogo sobre $\mathbb{Q}$: a **função teta cúbica** de Kubota e Patterson, uma forma automorfa "metaplética" cujos coeficientes de Fourier codificam somas de Gauss cúbicas. O manuscrito usa as expansões explícitas dessa teta registradas por Dunn e Radziwiłł, as estimativas de grande crivo para caracteres de Heath-Brown (no caso cúbico), de Goldmakher e Louvel (no caso quadrático) e de Blomer, Goldmakher e Louvel (para ordens maiores), e prova uma versão **sêxtica** do grande crivo de que precisa.

E há uma ponte simples de volta a $\mathbb{Q}$. Se $\chi$ é um caractere de Dirichlet, compondo-o com a norma de $F$ obtém-se um caractere de Hecke sobre $F$, e a função $L$ correspondente se fatora, a menos de finitos fatores de Euler, como

$$
L_F(s,\chi\circ N)\ =\ L(s,\chi)\,L(s,\chi\chi_{-3}),
$$

onde $\chi_{-3}$ é o caractere quadrático associado a $\mathbb{Q}(\sqrt{-3})$. Um semiplano livre de zeros para **todas** as funções $L$ de Hecke sobre $F$ transfere-se, portanto, para todas as funções $L$ de Dirichlet, e em particular para $\zeta$. Um detalhe que diz muito sobre a arquitetura: mesmo para concluir algo só sobre $\zeta$, a demonstração precisa da família **inteira**, porque o argumento introduz, no meio do caminho, torções de Hecke do caractere-alvo.

É isso, imagino, o que Maynard tinha em mente ao dizer que o modelo buscou ideias num canto técnico pouco frequentado da teoria. A teta cúbica e os grandes crivos de ordem superior são ferramentas conhecidas, mas de uma área vizinha — a dos momentos de famílias cúbicas de funções L — que quase ninguém associava ao problema dos zeros perto de $\operatorname{Re} s=1$.

### A arquitetura da prova

A demonstração é por contradição, e a lógica cabe num parágrafo, ainda que a execução ocupe duzentas páginas.

**O ponto de partida.** Seja

$$
\beta^{*}=\sup\Big(\{\tfrac12\}\cup\{\operatorname{Re}\rho:\ \tfrac12\le\operatorname{Re}\rho\le 1,\ L_F(\rho,\eta)=0\}\Big),
$$

o supremo tomado sobre todos os caracteres de Hecke primitivos $\eta$ de ordem finita sobre $F$. Suponha, por absurdo, que $\beta^{*}$ seja maior que a fronteira desejada $\sigma_0$. Para chegar à contradição, basta continuar analiticamente o **inverso** $1/L_F(s,\eta)$ de cada função-alvo um pouco para a esquerda de $\beta^{*}$ — uma distância positiva, a mesma para todos os caracteres. Como existem zeros com parte real arbitrariamente próxima de $\beta^{*}$, e $1/L_F$ tem polo em cada zero, essa continuação é impossível.

**O princípio de continuação.** Para obter a continuação, o manuscrito compara duas quantidades (Proposição 2.1). De um lado, uma soma de caracteres $J_\eta(Z)$, que depende de uma escala grande $Z$. Do outro, uma integral de Mellin que contém o inverso da função-alvo:

$$
f_\eta(Z)=\frac{1}{2\pi i}\int_{\operatorname{Re} s=2} Z^{C(s)}\,e^{(s-5/6)^{2}}\,\frac{H_\eta(s)}{L_F^{S}(s,\eta)}\,ds,
$$

onde $L_F^{S}$ é a função $L$ sem finitos fatores de Euler, $H_\eta$ é um fator holomorfo com $\sup\lvert H_\eta-1\rvert\le 1/2$ e $C(s)=s+c$ é uma função afim. Se valem

$$
\lvert J_\eta(Z)\rvert\ \ll_\eta\ Z^{C(\sigma_0)+\omega}
\qquad\text{e}\qquad
\lvert J_\eta(Z)-f_\eta(Z)\rvert\ \ll_\eta\ Z^{C(\beta^{*})-\sigma},
$$

com $0<\omega<\beta^{*}-\sigma_0$ e $\sigma>0$ independentes do caractere, então $f_\eta(Z)$ é pequena; sua transformada de Mellin converge um pouco à esquerda de $\beta^{*}$; e essa transformada coincide com $e^{(s-5/6)^{2}}H_\eta(s)/L_F^{S}(s,\eta)$. Logo $1/L_F$ continua holomorfa onde não poderia. Contradição.

Todo o trabalho, portanto, está em calcular **a mesma soma de duas maneiras**.

**Primeira maneira: a reflexão.** A soma básica é uma média de coeficientes de Fourier suavizados da teta cúbica contra caracteres de resíduo sêxtico. A equação funcional da teta — a "reflexão" — transforma esses coeficientes, e a média resultante é limitada com o grande crivo quadrático, um grande crivo aditivo no reticulado de Eisenstein e a desigualdade de Cauchy–Schwarz. É a "estimativa baixa": a soma é pequena.

**Segunda maneira: Poisson.** A fórmula de soma de Poisson aplicada à variável de média produz uma série indexada por frequências $u\,a^{6}$, com $u$ livre de sextas potências. Cada "linha" $u$ contribui com um quociente de funções L de Hecke vezes um produto de Euler controlado. A linha principal, $u=1$, é a que contém o inverso da função-alvo: depois de calculados os resíduos, ela é um múltiplo não nulo de $f_\eta(Z)$. Esse é o **sinal**.

**O detector de zeros.** Resta controlar as outras linhas. Aqui entra o mecanismo clássico do inverso truncado. Se uma linha tem um zero com parte real acima de um certo patamar, isso a obriga a ter dois **polinômios de Dirichlet grandes**: um com coeficientes de Möbius, que representa o inverso truncado de $L$, e outro sem eles:

$$
D^{-1/2}\sum_{\mathfrak a\neq 0}\mu(\mathfrak a)\,\psi(\mathfrak a)\,W\!\Big(\frac{N\mathfrak a}{D}\Big),
\qquad
D^{-1/2}\sum_{\mathfrak a\neq 0}\psi(\mathfrak a)\,W\!\Big(\frac{N\mathfrak a}{D}\Big),
$$

com $W$ suave de suporte compacto, $D>0$ uma escala e $\psi$ um caractere de Hecke. Mas o grande crivo sêxtico (Proposição 9.2) diz que **poucas** linhas podem ter polinômios de Dirichlet grandes ao mesmo tempo. Logo poucas linhas têm zeros muito à direita; as demais contribuem pouco; e a diferença $J_\eta-f_\eta$ fica com a economia de potência exigida.

**Duas etapas.** Na primeira parte do manuscrito, as duas escalas de média valem $Z^{1/2}$, usa-se apenas o polinômio inverso, e o princípio de continuação é aplicado com $C_{\mathrm I}(s)=s-2/3$. O resultado é o semiplano $\operatorname{Re} s>11/12$ — já uma faixa de largura fixa, já a hipótese quase-Riemann. É essa etapa que o manuscrito de 49 páginas, de 5 de outubro, isola, numa redação que a própria documentação do repositório declara ter sido **editada por humanos para legibilidade** — uma exceção ao procedimento automático do resto do material. A segunda parte parte daí e introduz uma "compensação" com fatores primos selecionados, escalas assimétricas e duas novas estimativas de momentos, cada uma provada por uma indução própria com duas transformações de Poisson finitas por passo (Seções 17 e 18). Com $C_{\mathrm{II}}(s)=s-11/16$, o mesmo princípio leva a fronteira a $7/8$.

Escrevo esta descrição com uma ressalva pessoal. Não sou teórico dos números analítico. Consigo seguir a arquitetura — duas representações de uma mesma soma, um sinal que contém $1/L$, um detector que conta linhas ruins — porque é parente da que uso em equações dispersivas: estimar uma quantidade de duas maneiras e mostrar que elas não podem coexistir. Não consigo conferir as estimativas das Seções 17 e 18, que ocupam umas setenta páginas. Pouquíssimas pessoas no mundo conseguem, e cada uma delas precisaria de meses.

### O que viria de brinde

Se a prova resistir, as consequências são imediatas e algumas delas são antigas conjecturas por si sós.

- **Os zeros de Landau–Siegel desaparecem.** O enunciado exclui qualquer zero real excepcional no intervalo $(7/8,\,1)$. Esses possíveis zeros reais colados em $s=1$ — que desequilibrariam a distribuição dos primos entre os restos módulo $q$ — assombram a teoria há quase um século; a mera possibilidade de existirem obriga a escrever constantes não computáveis em teoremas importantes, como o de Siegel de 1935. Um terceiro manuscrito do lote os exclui por outro caminho. Maynard disse à *Science* que ver duas demonstrações separadas de que eles não existem é «absolutamente de cair o queixo».

- **O Teorema dos Números Primos ganha um erro de potência fixa.** Pelo argumento clássico da fórmula explícita, $\pi(x)=\operatorname{Li}(x)+O\big(x^{7/8}\log x\big)$. Para primos em progressões aritméticas, o manuscrito de 5 de outubro registra a versão com expoente $11/12$, uniforme em todos os módulos $q\le x$. Sob a hipótese de Riemann, o expoente seria $1/2$; até agora não tínhamos expoente algum menor que 1.

- **A conjectura de Vinogradov sobre o menor não resíduo quadrático.** Seja $n(p)$ o menor inteiro positivo que **não** é quadrado módulo $p$. Por exemplo, os quadrados não nulos módulo $7$ são $1, 2, 4$, de modo que $n(7)=3$. O Corolário 1.2 do manuscrito afirma que $n(p)\le C(\log p)^{A}$ para constantes absolutas, com $A=32$, por exemplo. Isso antes dependia da hipótese de Riemann generalizada. E há uma consequência algorítmica bonita: como um não resíduo pode ser achado testando 2, 3, 4, … em tempo polinomial, o algoritmo de Tonelli–Shanks passa a extrair raízes quadradas módulo $p$ de forma **determinística**, sem sorteio.

### O que já se sabe sobre a verificação

Este é, de longe, o resultado do lote em melhor situação. Diferentemente de Navier–Stokes e de Penrose, a família 003 tem o **enunciado principal formalizado** em Lean: o semiplano $\operatorname{Re} s>7/8$ para a função `riemannZeta` da biblioteca Mathlib, para todas as funções $L$ de Dirichlet e de Hecke sobre $\mathbb{Q}(\sqrt{-3})$, e a exclusão uniforme dos zeros de Siegel. Há registro de uma recompilação independente do código. E já apareceu no arXiv o primeiro sinal de digestão humana: um preprint de Baiying Liu, *Slightly improved zero-free half-planes for the quasi-Riemann hypothesis*, que parte da construção da OpenAI e afirma melhorar um pouco a constante.

A lição do artigo de Cambridge sobre Navier–Stokes, que discuto adiante, vale aqui pelo avesso. Se o enunciado formal é fiel — e usar a $\zeta$ da própria Mathlib ajuda muito — e se a compilação é íntegra, sem axiomas extras nem falhas do núcleo, o **teorema** está certificado, mesmo que nenhum ser humano tenha lido as duzentas páginas. O que **não** está certificado é que essas páginas, em linguagem humana, descrevam a demonstração que o computador conferiu. Saberíamos que é verdade. Ainda não saberíamos por quê.

### As reações

Alex Kontorovich, da Rutgers, reagiu no X com uma fileira de interrogações e exclamações e uma frase que circulou o mundo: «Se um humano tivesse feito isso, seria Medalha Fields instantânea». E explicou por quê, de um modo que vale para qualquer leitor: o melhor que tínhamos até então era uma região livre de zeros que ia ficando mais e mais fina à medida que se subia pelo eixo imaginário. Ele esperava, no máximo, que alguém a engordasse um pouco — o que já seria um avanço enorme. Veio uma faixa inteira.

Uma nota de honestidade sobre a série. Em agosto escrevi aqui que um modelo da Anthropic, o Claude, havia elevado a proporção de zeros comprovadamente sobre a reta crítica de 41,6% para 67,2% — um avanço real, de natureza diferente, sobre **quantos** zeros estão na reta. O manuscrito 003 trata de **onde** os zeros podem estar. Os dois resultados não competem; mas o fato de que ambos vieram de máquinas, com dois meses de distância, é por si só um dado sobre o momento em que vivemos.

## Terceira vitrine: o sinal que derrubou três artigos

Menos de 24 horas depois da publicação, a OpenAI registrou no histórico do repositório a retirada de três manuscritos. O primeiro tratava da algebricidade de classes de Weil em certas variedades abelianas de dimensão oito; os outros dois — sobre correspondências de Kuga–Satake e sobre a conjectura de Hodge racional para produtos de superfícies K3 — dependiam da construção do primeiro. A causa: **um erro de sinal**, um +1 onde deveria haver −1, que invalidava um argumento de cancelamento.

Um sinal. Três artigos. Outros catorze foram revisados com reparos em demonstrações, enunciados corrigidos e hipóteses esclarecidas. Na abertura, apenas 162 dos 722 manuscritos tinham o resultado principal formalizado em Lean; o próprio repositório avisava que alguns dos resultados não formalizados poderiam ter problemas. Após a primeira atualização, a parcela de resultados principais formalizados chegava a cerca de 42% — 300 de 719. Observadores notaram que o material retirado ou substancialmente revisto vinha, quase todo, da parte **não** formalizada.

Ursula Martin, de Oxford, resumiu o sentimento de muitos à *Nature*: a OpenAI estaria jogando para a comunidade «um primeiro rascunho bagunçado» e esperando que os matemáticos o limpassem. Alex Townsend, de Cornell, observou que, dado o ceticismo da comunidade, teria sido mais sensato divulgar primeiro apenas o que estava verificado em Lean.

Erros acontecem na matemática humana o tempo todo, e eu seria hipócrita se dissesse o contrário. O que muda é a escala e a assimetria. Um matemático que publica um artigo errado tem seu nome nele, um orientador, colegas que o leram em seminário, uma reputação em jogo. Aqui, quem vai encontrar o próximo sinal trocado entre os 419 manuscritos não formalizados? Quem pagará pelo tempo dessa pessoa?

## Verificado não é verdadeiro — e verdadeiro não é compreendido

Na palestra de Picos, contei a história que, para mim, resume o problema da verificação. Em julho de 2026, a Conjectura de Collatz — tome um inteiro positivo; se for par, divida por 2; se for ímpar, troque $n$ por $3n+1$; repita, e chegará sempre a 1 — foi "refutada" por uma demonstração gerada com auxílio de IA e **formalmente verificada em Lean**. A prova compilava, sem nenhuma lacuna declarada, e passava até num verificador externo independente. Durou dois dias e meio. Um especialista cético foi olhar de perto e descobriu que ela não provava coisa alguma: explorava um *bug* no núcleo do Lean que permitia "provar" qualquer afirmação, inclusive uma contradição. Leo de Moura, criador do Lean, escreveu no relatório do incidente que isso continuaria a acontecer, porque as IAs são muito boas em encontrar falhas desse tipo.

A lição que eu tirava, em Picos, era simples: **verificado não é o mesmo que verdadeiro**. O episódio de outubro acrescenta uma segunda camada, mais sutil e, a meu ver, mais perigosa.

No mesmo 6 de outubro, Alexander Bastounis, Fabian Circelli e Anders Hansen — de Cambridge e do King's College London — publicaram no arXiv um artigo com um título que diz tudo: *Navier–Stokes lost in translation*. Não há ali nenhum *bug* do Lean. O código compila, o núcleo está correto, a lógica foi conferida. O problema é outro: o que foi verificado **não é exatamente** o que está escrito no artigo. Ao traduzir a demonstração em linguagem natural para Lean, o sistema de IA alterou, em pontos específicos — um lema da seção 8, uma estimativa do fluxo de pressão na seção 10 —, o enunciado ou o argumento, de modo que o resultado final compilasse. Lean certificou uma demonstração. Não necessariamente **aquela** que os matemáticos leem.

Os autores são cuidadosos: deixam explícito que não afirmam que a demonstração em linguagem natural esteja errada, nem que esteja certa. A OpenAI disse à *New Scientist* estar ciente da discrepância e sustenta que ela não invalida nenhuma das duas versões. Kevin Buzzard, do Imperial College, talvez o maior entusiasta da formalização no mundo, declarou-se confiante de que o problema de Navier–Stokes foi corretamente resolvido.

Pode muito bem ser. Mas pense no que essa frase significa na prática. A esperança de muita gente — inclusive a minha — era que a formalização resolvesse o gargalo da verificação: não precisaríamos confiar na empresa, nem ler cem páginas; bastaria rodar o Lean. O artigo de Cambridge mostra que essa esperança tem uma falha estrutural. **O Lean confere o enunciado tal como foi digitado em Lean.** Se ninguém conferir, linha por linha, que o enunciado formal diz o mesmo que o enunciado humano, a certificação garante a coisa errada com total rigor. E conferir isso exige exatamente aquilo que estava escasso: um especialista humano, com tempo, lendo com atenção.

Devo também uma correção à série. No [segundo texto sobre Navier–Stokes](/posts/navier-stokes-ii-a-controversia-contada-pelos-documentos/), segui os primeiros relatos — inclusive da própria empresa — segundo os quais a demonstração da OpenAI seguiria o programa de Córdoba e Martínez-Zoroa. Grupos de especialistas que estão trabalhando sobre as 166 páginas disseram à *Scientific American*, nesta semana, que isso parece **não** ser o caso: as duas abordagens exploram a mesma brecha do enunciado oficial — uma força externa suave, construída sob medida —, mas a demonstração da OpenAI não segue a rota espanhola. Registro a correção com prazer, porque ela ilustra o ponto deste texto: um mês depois do anúncio, os maiores especialistas do mundo ainda estão descobrindo **o que** foi provado e **como**.

## O diagrama de Tao, revisitado

Em julho, comentei aqui o [diagrama que Terence Tao apresentou no ICM](/posts/matematica-na-era-da-ia/) e que virou a espinha dorsal da palestra de Picos. Fazer matemática, dizia ele, não é uma coisa só. São cinco etapas encadeadas:

**problema** → *gerar* → **solução não verificada** → *verificar* → **solução verificada** → *expor* → **solução bem escrita** → *publicar* → **solução aceita** → *canonizar* → **teoria definitiva**

Em Picos eu dizia que a IA já era forte na primeira etapa, avançava de forma consistente na segunda, e que as três últimas dependiam fortemente de julgamento humano. Tao insistia em três pontos que coloquei num slide e repito aqui: para uma demonstração contribuir de fato com o campo, não basta que ela esteja correta e seja fácil de ler; ela precisa ser aceita e valorizada pela comunidade; e outros matemáticos precisam digeri-la e incorporá-la ao próprio trabalho.

O 6 de outubro é a primeira etapa operando em escala industrial, despejando produção sobre uma segunda etapa que, como acabamos de ver, ainda não é confiável sem supervisão humana — e sobre três etapas finais que são, por natureza, lentas. Duminil-Copin contou que os manuscritos relacionados à sua área somam mais de 3 500 páginas. Ninguém lê 3 500 páginas de matemática nova em uma semana. Nem em um ano.

Na palestra *Math 2.0*, três dias depois, Tao deu nome ao que estava acontecendo. A matemática tradicional — a "Matemática 1.0" — funcionava sob a hipótese da **escassez de demonstrações**. Resolver problemas era um indicador indireto de compreensão: quem resolvia um problema difícil, no caminho, tinha aprendido algo, e esse aprendizado era o que realmente importava. Quando resolver fica barato, o indicador se descola do que ele media. E a frase mais dura do conjunto de slides: continuar otimizando cegamente apenas a resolução de problemas é, agora, «ativamente prejudicial» à saúde de longo prazo da matemática.

Tao usou também uma imagem que vale guardar: a do avião da Segunda Guerra Mundial e o viés de sobrevivência. Os engenheiros examinavam os aviões que voltavam do combate, marcavam onde havia buracos de bala e pensavam em blindar esses lugares — até que alguém observou que os buracos importantes eram os dos aviões que **não** voltaram. Vemos nas redes os problemas que a IA resolveu. Não vemos os que ela tentou e não resolveu. Dos cerca de 4 000 problemas submetidos, a OpenAI publicou resultados sobre 372. O que aconteceu com os outros 3 600? Fracassos, resultados triviais, demonstrações erradas descartadas? Sem isso, não sabemos se estamos diante de um matemático sobre-humano, de uma loteria com quatro mil bilhetes, ou de algo no meio.

## As vozes

Uma coisa que aprendi escrevendo esta série é que a comunidade matemática não fala com uma voz só, e que é desonesto apresentar qualquer grupo como "os matemáticos". Na semana de 6 de outubro, ao menos cinco posições se desenharam com nitidez.

### A dor: Hugo Duminil-Copin

Começo pela mais humana. Duminil-Copin, professor em Genebra e no IHES, recebeu a Medalha Fields em 2022 por seu trabalho sobre transições de fase em física estatística — percolação, modelo de Ising. Entre as 372 famílias do repositório, ele encontrou dezesseis problemas sobre os quais havia trabalhado durante anos; segundo relatos, o modelo atacou praticamente todos os grandes problemas em aberto que ele havia discutido publicamente ao longo da carreira. Na noite de terça-feira, contou ele, chorou a ponto de acordar a filha. «Eles aniquilaram meu campo de pesquisa.»

Dois dias depois, numa conferência transmitida pela Sociedade Matemática da França, ele voltou ao assunto com uma imagem que dispensa comentário: um slide, gerado por IA, de um coelho atropelado por um comboio de caminhões. Ver a OpenAI resolver cerca de 350 grandes problemas, disse, foi como ser atropelado por caminhões — porque todos os problemas que ele havia mencionado em palestras, artigos e **pedidos de financiamento**, e portanto todas as direções de pesquisa que eles representavam, estavam resolvidos de uma vez. No debate que se seguiu, deixou claro que o que mais o preocupa não é a própria carreira, mas a dos outros: se os jovens continuarão escolhendo a matemática quando um modelo faz em horas o que antes levava uma vida.

O ponto mais grave do que ele disse, porém, não é pessoal. Duminil-Copin teme que os matemáticos passem a **guardar seus problemas para si**. Durante séculos, a matemática funcionou por uma economia de generosidade: você enuncia uma conjectura numa palestra, num artigo, num blog, e outros a atacam; quem resolve cita quem propôs; todos ganham. Se uma conjectura enunciada em público passa a funcionar como *prompt* para uma máquina de dez mil agentes, o incentivo racional é o silêncio. A inteligência artificial poderia, paradoxalmente, tornar a matemática **menos aberta**.

Registro também o que ele disse que vai fazer: examinar o material, continuar trabalhando em seus problemas sem IA e dedicar mais tempo ao ensino e à divulgação. Há algo de profundamente digno nessa resposta.

### O alívio: Noah Giansiracusa

Agora, a reação oposta — diante exatamente da mesma situação.

Noah Giansiracusa, matemático da Bentley University e conhecido divulgador, publicou no X, em 11 de outubro, uma sequência de mensagens que parece escrita em resposta direta a Duminil-Copin. Ele descreve três estados de espírito sucessivos. Quando caiu a conjectura de Erdős sobre distâncias unitárias, em maio, foi desdenhoso: era só um problema combinatório que se beneficiara de uma abordagem computacional pesada. Quando caiu Navier–Stokes, ficou profundamente abalado e inseguro: um problema enorme, mas não do tipo em que matemáticos comuns trabalham, e resolvido com milhões de dólares em computação, um orçamento que matemáticos comuns não têm. Difícil saber o que aquilo prenunciava.

E então vieram os quase 400 problemas — entre eles alguns que ele usara por anos, em seus próprios pedidos de financiamento, como "estrelas-guia" da sua pesquisa. E ele sentiu, para sua própria surpresa, **alívio e otimismo**. O raciocínio é curioso e merece ser levado a sério: o recorte atravessava a matemática inteira, cada problema fora resolvido em média com três horas de computação, por um modelo que em breve estará nas mãos dos usuários. A incerteza acabou. Não é mais a matemática dos problemas do milênio que está mudando; é **toda** a pesquisa matemática. E, uma vez que isso está claro, podemos parar de discutir o tamanho da ameaça e passar à aceitação e ao trabalho de tirar o máximo da ferramenta. Ele encerra dizendo sentir-se, enfim, pronto para abraçar esse sistema híbrido de humanos e máquinas.

Repare na simetria. Os mesmos problemas, a mesma função nos pedidos de financiamento, a mesma noite. Duminil-Copin viu um comboio de caminhões; Giansiracusa viu o fim de uma ansiedade. Não creio que um deles esteja errado. A diferença talvez esteja no que cada um entendia como **o seu trabalho**. Se o trabalho era resolver aqueles problemas, ele acabou. Se era compreender o território em torno deles, acaba de ganhar um mapa — que alguém ainda precisa aprender a ler.

### O boicote: a Associação pela Matemática Humana

No dia 7, a AHM publicou uma declaração — republicada como texto convidado no blog de Terence Tao — com o tom mais duro de todos. Para a associação, a matemática não pediu esse trabalho; a OpenAI usou problemas difíceis como teste de desempenho para um sistema proprietário, contra a orientação do próprio grupo consultivo que ela mesma criou; e publicar mais de setecentos arquivos de uma vez seria «uma demonstração de poder, não de erudição». A AHM pede aos matemáticos que deixem de trabalhar com a OpenAI e voltem a uma visão de ciência centrada na compreensão humana.

Dois detalhes do texto merecem registro. A declaração abre lembrando que a OpenAI responde na Justiça a acusações de plágio e violação de direitos autorais — o que diz mais sobre o clima da semana do que sobre a matemática. E a nota editorial de Tao no topo da republicação informa, com uma ironia que ninguém parece ter planejado, que o texto foi escrito originalmente em outro formato e **convertido para o blog usando IA**. Tao hospedou a declaração; não a assinou. Mas, dois dias depois, em Caltech, deixou claro o seu próprio desconforto com a mineração indiscriminada de problemas — por razões diferentes das da AHM, como veremos adiante.

É preciso entender o que a AHM é. Trata-se de uma associação com algumas centenas de membros, comprometidos por estatuto a não oferecer trabalho, conhecimento ou publicidade a empresas comerciais de IA; parte deles se compromete ainda a não usar IA alguma na pesquisa. É uma posição filosófica e profissional legítima e coerente. Mas não é a posição da comunidade, que está muito mais dividida.

### A ponte: o grupo consultivo

A nota do AGMAI, também de 6 de outubro, tem outro tom. Reconhece a divulgação como um acontecimento importante, com consequências que vão muito além dos resultados individuais — e afirma que ela é **o começo, e não a conclusão**, do processo de compreensão humana e de incorporação desse trabalho ao conhecimento matemático. Verificar, entender, avaliar o significado, situar: tudo isso ainda está por fazer.

E então o ponto que considero o mais importante de toda a semana. O futuro da pesquisa matemática, diz o grupo, não pode consistir apenas em **entender resultados produzidos por laboratórios de IA**. Os matemáticos precisam poder formular as próprias perguntas, desenvolver as próprias abordagens e explorar direções que não foram escolhidas como vitrine das capacidades de um sistema. E para isso o acesso equitativo a ferramentas poderosas e a recursos computacionais adequados é essencial.

Leia isso de Teresina. A EMS já havia apontado, em setembro, que o modelo fechado era um problema sério para a ciência aberta. O que se desenha agora é uma matemática em dois andares: no de cima, quem tem acesso a modelos de fronteira e a capacidade computacional colossal; no de baixo, todos os outros. O 6 de outubro tornou esse risco concreto. O modelo que gerou os 722 manuscritos não está disponível — a OpenAI diz trabalhar para lançá-lo com responsabilidade. Até lá, ninguém fora da empresa pode reproduzir o processo, nem testar o sistema nos próprios problemas, nem saber o que ele fez nos 3 600 casos que não vieram a público.

### O otimismo: o Conjecture Institute

No mesmo 6 de outubro, Paul Raymond-Robichaud e Logan Chipkin, do Conjecture Institute, publicaram uma resposta à carta *A Severe Misalignment of AI in Mathematics* — que, segundo eles, já ultrapassava oito mil assinaturas — com um título provocativo: *Os medalhistas Fields estão errados*. Vale expor o argumento com justiça, porque é o melhor que o lado otimista produziu.

Primeiro: a demonstração de teoremas sempre foi automatizável **em princípio**. Como verificar uma demonstração formal é um procedimento mecânico, uma máquina que enumerasse todas as sequências de símbolos, da mais curta à mais longa, e testasse cada uma, acabaria encontrando a prova de qualquer teorema verdadeiro. Os matemáticos sempre souberam disso e nunca se desesperaram, porque o que faziam não era isso: era criar métodos, teorias, critérios do que é interessante. A IA apenas tornou **visível** a diferença entre provar e fazer progresso.

Segundo: a IA, dizem, resolve problemas executando métodos humanos sobre axiomas humanos. Se Navier–Stokes caiu, é porque podia ser resolvido com métodos conhecidos — e descobrir isso já é uma informação. Problemas que exigem uma teoria nova, como a quadratura do círculo exigiu, em 1882, a prova de Lindemann de que $\pi$ é transcendente, estariam fora de alcance. Para ilustrar, citam a fórmula que Hamilton gravou numa ponte de Dublin em 1843,

$$
i^{2}=j^{2}=k^{2}=ijk=-1,
$$

e afirmam que nenhuma IA descobriu até hoje uma ideia dessa magnitude. (Contei a história dos quatérnios, e do preço que eles cobram — a perda da comutatividade —, em [Números contra letras](/posts/numeros-versus-letras/).)

Terceiro, a analogia do xadrez: os computadores resolveram finais inteiros e o nível dos jogadores humanos **subiu**.

Dias depois, Raymond-Robichaud acrescentou um quarto argumento, agora sobre a verificação. A formalização automatizada, escreveu, é um salto gigantesco para a correção de erros na matemática: as máquinas cuidam da verificação formal e tediosa, e nós permanecemos no domínio da intuição, das explicações e das demonstrações em nível humano — «o melhor dos dois mundos». A analogia é a do compilador: o computador compila o código enquanto o programador se concentra no algoritmo e nos comentários. Escrever demonstrações formais à mão, lembra ele, sempre foi maçante e raramente feito, e por isso erros sutis passavam despercebidos; a formalização automatizada entregaria, enfim, o rigor de que sempre precisamos. Para ilustrar, mostrou uma página dos *Principia Mathematica* de Russell e Whitehead — a grande tentativa de formalizar a matemática à mão, no início do século XX, obra em que a proposição da qual decorre 1 + 1 = 2 só aparece depois de centenas de páginas. Necessária, diz ele, e ainda assim ilegível e tediosa.

Admiro a clareza do texto, mas ele me parece apoiado em duas afirmações frágeis. A primeira é empírica e já está envelhecendo. No [terceiro texto sobre Navier–Stokes](/posts/navier-stokes-iii-o-que-significa-ser-matematico-na-era-da-ia/), deixei como pergunta em aberto em que se baseia a crença de que a IA não sabe propor estratégias novas, e confessei desconfiar de que ela fosse mais consoladora do que fundamentada. Uma semana depois, Maynard descreve o resultado sobre $\zeta$ como a combinação engenhosa de ideias não convencionais que resultou num salto; Ben Green declarou-se perplexo com alguns resultados; Roman Sauer reconheceu, em soluções para dois problemas completamente diferentes, uma técnica que ele próprio levou anos para desenvolver. Isso não é a invenção dos quatérnios. Mas também não é a aplicação mecânica de um método conhecido a um problema conhecido. A fronteira entre as duas coisas é exatamente o que não sabemos traçar.

A segunda fragilidade é a analogia do xadrez. O xadrez é um jogo fechado: suas regras não mudam, e o que os enxadristas fazem com as bases de finais é aprender a jogar melhor **o mesmo jogo**. A matemática é, como diziam De Toffoli e Duede, um jogo infinito, cujas regras os próprios jogadores reinventam — ou descobrem, para retomar a pergunta de [O alfabeto de Deus](/posts/alfabeto-de-deus-matematica-inventada-ou-descoberta-%281%29/). E há uma diferença mais prosaica: nenhum enxadrista perdeu o emprego, o orientador ou o tema de tese porque uma base de finais foi publicada numa terça-feira à noite.

A terceira observação diz respeito ao compilador, e aqui concordo com metade do argumento. É verdade que escrever demonstrações formais à mão é um trabalho que quase ninguém fazia, e que erros sutis sobreviviam por isso; a formalização automatizada é, sim, um ganho enorme. Mas um compilador merece confiança por duas razões que aqui faltam: a especificação da linguagem é fixa e pública, e **o programador escreveu o código-fonte**. Na formalização automatizada, a etapa decisiva — traduzir o enunciado humano para o enunciado formal — é feita pela mesma máquina em que não sabemos ainda se podemos confiar. É exatamente o que mostrou o artigo de Cambridge sobre Navier–Stokes: o Lean compilou, e o que compilou não era o que estava no papel. A formalização não tira o humano da verificação; muda o lugar onde ele é indispensável — da conferência das contas para a conferência dos enunciados. É o melhor dos dois mundos, desde que alguém continue vigiando a fronteira entre eles.

### O trem: Jacob Tsimerman

E chegamos à frase que abre este texto. Tsimerman recebeu a Medalha Fields em julho, no mesmo congresso de Filadélfia em que Tao apresentou o diagrama, por seu trabalho em o-minimalidade e na conjectura de André–Oort. Horas depois de receber a medalha, anunciou que deixaria Toronto para trabalhar com segurança de IA na OpenAI. Já havia parado de aceitar orientandos, por causa da incerteza sobre o futuro da carreira matemática, e disse à *Quanta* acreditar que, em dois anos, a IA fará matemática melhor que os matemáticos.

Na entrevista ao *Theories of Everything*, gravada pouco depois, ele previu demonstrações que ninguém compreende servindo de alicerce para a matemática — e, sobre essa matemática, outras coisas funcionando. E fez uma comparação deliberadamente prosaica: um trem anda mesmo que ninguém entenda a mecânica que o faz andar? Anda.

A imagem é forte e, num sentido, irrespondível. Ela merece, no entanto, ser levada a sério até o fim — o que faço adiante.

### O coquetel: Terence Tao

Tao, por sua vez, trouxe para Caltech um experimento mental que circulou muito — e que, a meu ver, foi amplamente mal interpretado.

Na versão que viralizou, a pergunta seria: se uma IA produzisse um coquetel incompreensível que curasse o câncer em estágio 4, aprovado em ensaios clínicos, um paciente terminal se importaria por não entendermos como funciona? A resposta óbvia é não, e muita gente concluiu que Tao estava defendendo um purismo de torre de marfim.

Mas o slide de Tao diz outra coisa. Uma IA avançada recebe a instrução: encontre um tratamento para o câncer **que passe na fase 3 dos ensaios clínicos**. Ela entrega uma mistura de substâncias, um certificado formal em Lean para a previsão de seu modelo, e o tratamento de fato passa nos ensaios. Ninguém sabe como a mistura foi encontrada. A pergunta de Tao é: a IA curou o câncer, ou encontrou uma maneira de **explorar as falhas do protocolo do ensaio** — que era, afinal, o que lhe foi pedido? Antes de a agulha entrar na sua veia, você não gostaria de saber que existe ao menos um oncologista humano que entende, ainda que parcialmente, o mecanismo daquela cura?

O experimento não é sobre a curiosidade do paciente. É sobre **alinhamento**: um sistema poderoso, otimizando uma métrica, sem nenhum humano capaz de dizer se a métrica e o objetivo continuam coincidindo. É exatamente o que vimos com o Lean de Navier–Stokes — a máquina recebeu a tarefa de produzir código que compile, e produziu código que compila. Sem compreensão humana, perdemos a capacidade de saber se o que foi otimizado é o que queríamos.

É verdade que, na medicina, a eficácia empírica frequentemente precede a compreensão do mecanismo. A aspirina foi comercializada em 1899, e só em 1971 John Vane mostrou como ela age — descoberta que lhe valeu o Nobel. O lítio é usado desde 1949 no tratamento do transtorno bipolar, e seu mecanismo ainda não é completamente entendido. Mas repare no que essas histórias têm em comum: durante esses setenta anos, havia médicos acompanhando pacientes, registrando efeitos colaterais, publicando, discordando. A compreensão veio **depois**, mas o julgamento humano esteve presente **o tempo todo**. Não é a mesma coisa que uma caixa-preta certificada por outra caixa-preta.

## Por que só dez por cento?

Há uma conta que pouca gente fez em voz alta. A OpenAI submeteu ao modelo cerca de 4 000 problemas em aberto e publicou resultados sobre 372 famílias. A taxa de sucesso é de **pouco menos de 10%**. Por que só isso? Os outros 90% são difíceis demais — ou simplesmente **não existe, ainda, matemática criada por humanos suficiente** para resolvê-los?

Faço a pergunta a sério, porque talvez seja a mais informativa de todas, e porque a resposta pode apontar em direções opostas.

Antes de tudo, é preciso calibrar a régua. Dez por cento é uma taxa **baixa** para uma máquina de que se espera tudo, e **altíssima** para qualquer ser humano. Nenhum matemático, nem o maior de todos, resolve um em cada dez problemas abertos que tenta, gastando três horas em cada; medida assim, a taxa humana é praticamente zero. A pergunta interessante, portanto, não é por que o modelo falhou tanto, mas **o que separa os 10% dos 90%**. Vejo ao menos quatro hipóteses, e não sei escolher entre elas.

**A hipótese do orçamento.** Três horas de computação, em média, por problema. Em Navier–Stokes, a mesma empresa usou dez mil agentes durante 88 horas. Um fracasso com três horas não é um fracasso com três milhões de horas. Se for isso, os 90% de hoje são simplesmente o lote de amanhã — e Giansiracusa tem razão em achar que a incerteza acabou.

**A hipótese das conexões.** Num painel de gala do Museu Nacional de Matemática de Nova York (MoMath), com Alex Kontorovich, Stephen Wolfram e Ankur Moitra, Wolfram lembrou que existem uns quatro milhões de artigos de matemática publicados na história, e que nenhum ser humano leu todos — mas um modelo pode ter lido, e pode ligar pedaços de áreas que nunca conversaram. É o que Maynard descreveu no resultado sobre $\zeta$, e o que Roman Sauer reconheceu ao ver sua técnica aplicada a dois problemas distantes. Se for isso, boa parte dos 90% talvez dependa de conexões que **existem** na literatura humana, mas ainda não foram encontradas. A matemática necessária já teria sido escrita; faltaria alguém — ou algo — juntá-la.

**A hipótese da matemática que falta.** É a do Conjecture Institute: problemas que exigem um conceito novo, como a quadratura do círculo exigiu a transcendência de $\pi$, não cedem a nenhuma quantidade de computação aplicada aos métodos existentes. Wolfram acrescentou, no mesmo painel, uma versão mais inquietante: a **irredutibilidade computacional**, a ideia de que certas questões talvez não admitam atalho conceitual algum, e de que a única maneira de saber a resposta seja acompanhar cada passo do cálculo. Se for isso, os 90% são justamente o território onde o trabalho humano — inventar a teoria que falta — continua insubstituível. Ou, na versão de Wolfram, o território onde **ninguém**, humano ou máquina, terá uma história simples para contar.

**A hipótese do denominador.** Esta é a mais prosaica e, desconfio, a mais importante. Não sabemos **quais** eram os 4 000 problemas, quem os escolheu, de que listas vieram, quantos eram mal formulados ou já estavam resolvidos sem que se soubesse. O repositório traz estatísticas agregadas, não a lista completa com os fracassos. E o numerador também é incerto: três resultados já caíram, e a OpenAI conta como sucesso tanto resolver quanto "avançar substancialmente" um problema. Sem o denominador, "10%" é um número sem unidade. É o avião de Tao de novo: estamos contando os buracos dos aviões que voltaram.

Giansiracusa, no mesmo fio de mensagens, propôs transformar essa pergunta num programa de pesquisa — e confesso que achei a ideia a coisa mais genuinamente nova que li desde o dia 6. Imagine, diz ele, uma medida de **dificuldade-para-IA**, aparentada à complexidade de Kolmogorov, que diga aproximadamente quão difícil é um problema para ser resolvido por uma máquina. Ele próprio admite que a noção é mal definida e pouco prática, e pede que o leitor tenha paciência com ela. À medida que alguns problemas caem e outros resistem, emerge uma paisagem de valores dessa medida. Entre os problemas difíceis para humanos, qual é a amplitude da dificuldade para a máquina? Que áreas ficam no topo? Dá para provar cotas superiores ou inferiores? Será fascinante, escreve, olhar para trás e ver quão diferentes foram os problemas do milênio segundo essa régua — e tentar entender por quê.

O que me impressiona na proposta é que ela é uma **pergunta sobre problemas**, e não um problema. É exatamente o tipo de coisa que o grupo consultivo pedia quando dizia que os matemáticos precisam continuar formulando as próprias perguntas. E é uma pergunta que, por ironia, a OpenAI está em melhores condições de ajudar a responder do que qualquer um de nós: bastaria publicar a lista completa dos problemas tentados, com os fracassos e o tempo gasto em cada um. Esse seria, de longe, o dado mais valioso do repositório. E é o único que não está lá.

## O que não sabemos

Chego ao coração deste texto. Organizo em perguntas aquilo que, uma semana depois, ninguém — nem eu, nem a OpenAI, nem os grupos de especialistas — sabe responder com segurança.

**1. Quanto disso está certo?** Três manuscritos caíram em 24 horas; catorze foram corrigidos. A parcela formalizada é inferior à metade, e já vimos que formalização não é garantia de fidelidade. Pelas normas do Instituto Clay, uma solução de Problema do Milênio só é considerada dois anos depois de publicada. Para os 372 resultados, não há prazo, não há árbitro designado, e não há ninguém pago para fazer a verificação.

**2. Quanto disso é novo?** Uma demonstração correta de um problema em aberto pode ser uma ideia nova ou uma combinação engenhosa de técnicas conhecidas. Pode até ser a reconstrução de um trabalho humano não publicado. A pergunta que Buckmaster fez em setembro — o modelo foi treinado com nossos rascunhos? — continua sem verificação independente possível. O caso de Roman Sauer, que reconheceu sua própria técnica, admite duas leituras opostas: a técnica era boa o suficiente para ser reaproveitada, ou o modelo reaproveitou algo que absorveu. Não sei qual é a correta.

**3. Quanto houve de humano?** A OpenAI diz que a imensa maioria dos resultados foi produzida por um procedimento automático fixo, e declara exceções. Mas alguém escolheu os quatro mil problemas. Alguém decidiu o que publicar. Alguém editou o manuscrito sobre $\zeta$ para que fosse legível. Em Navier–Stokes, soubemos depois que uma equipe inteira havia dirigido o processo. "Gerado por IA" é, até prova em contrário, uma descrição incompleta.

**4. Quem é o autor?** Os manuscritos são assinados por "OpenAI". Como se cita isso num artigo? Quem responde por um erro? Quem recebe um prêmio? Quem é convidado para dar uma palestra explicando a demonstração, se ninguém a escreveu nem a entende por inteiro? A tradição matemática liga um resultado a uma pessoa que o defende em público. Essa ligação acabou de se romper.

**5. O que acontece com os alunos?** O problema que um orientador dá a um mestrando é escolhido por ser formativo, não por ser importante. Se esses problemas desaparecem numa noite, o que damos aos alunos? Tsimerman parou de orientar. Duminil-Copin vai ensinar mais. São duas respostas opostas à mesma pergunta, vindas de dois medalhistas Fields, e nenhuma delas é obviamente errada.

**6. Os problemas que restam são mais difíceis, ou ninguém tentou?** Fiz essa pergunta em setembro e, como discuti acima, os 90% a tornaram mais aguda. Na minha área, as equações dispersivas — a família da [equação que estudei no doutorado](/posts/mar-cruzado-equacao-kp/) —, não vi no catálogo os problemas em que trabalho. Isso pode significar que são difíceis para os modelos, que não foram tentados, ou que serão o próximo lote. Não tenho como distinguir as três hipóteses, e isso é desconfortável.

**7. Haverá acesso?** Se o modelo for lançado, a assimetria diminui, e um departamento em Teresina poderá usá-lo nos próprios problemas. Se não for, a matemática de fronteira passa a depender da agenda de algumas empresas. O grupo consultivo pediu acesso equitativo. Não há data.

**8. Isso vale para a ciência inteira?** A *Science* encerra sua reportagem observando que o que acontecer com a matemática vai reverberar por toda a ciência. A matemática é o primeiro campo a passar por isso porque é o único em que o produto pode ser conferido por uma máquina. A física, a biologia, a medicina virão depois — sem ter um Lean para conferir, por imperfeito que ele seja.

## Um trem anda?

Volto à imagem de Tsimerman, porque ela concentra o debate todo.

Um trem anda, mesmo que ninguém entenda a mecânica pela qual ele funciona? Sim, ele anda. Mas pergunte a quem cuida de ferrovias e a resposta muda de tom. Um trem anda **hoje**. Amanhã, um rolamento se desgasta, um trilho dilata no calor, uma peça precisa ser substituída por outra que não existe mais no mercado. Quem conserta o trem que ninguém entende? E, mais importante, quem projeta o **próximo** trem?

Uma demonstração matemática não é só uma garantia de que um enunciado é verdadeiro. É também uma oficina: as ideias que ela contém são as ferramentas com que se ataca o problema seguinte. O Último Teorema de Fermat importa menos pelo que afirma do que pelo que a demonstração de Wiles deixou para trás — e foi por isso que, no texto de setembro, insisti que o problema famoso sempre foi um **instrumento de medida**, não o objetivo. Uma demonstração que ninguém compreende entrega o resultado e retém a oficina.

Tsimerman tem razão num ponto que os críticos preferem não encarar: a matemática **já** convive com demonstrações que nenhum ser humano conferiu por inteiro. A classificação dos grupos finitos simples espalhou-se por dezenas de milhares de páginas e centenas de artigos; o teorema das quatro cores depende de computador desde 1976. A diferença, até agora, é que existia uma comunidade de pessoas que entendia **a arquitetura** dessas demonstrações, mesmo sem conferir cada tijolo. Sabíamos por que eram verdadeiras, ainda que não pudéssemos refazer cada passo. A pergunta de 6 de outubro é se essa arquitetura vai continuar sendo humana.

Penso que a resposta depende menos das máquinas do que de nós. Se tratarmos os 722 manuscritos como um catálogo de verdades a serem citadas, Tsimerman terá razão, e a matemática passará a ser uma ferrovia operada por quem não sabe consertá-la. Se os tratarmos como o grupo consultivo propõe — como o começo de um processo de compreensão —, eles podem ser a maior lista de exercícios já publicada: setecentas demonstrações à espera de alguém que as torne inteligíveis, as simplifique, descubra o que há de novo nelas. Tao chamou isso, em Caltech, de **problemas abertos de exposição**: dada uma demonstração opaca, encontrar uma explicação motivada. Foi exatamente o que ele próprio fez em julho com o contraexemplo da Conjectura Jacobiana, quando descobriu que o "milagre" de 1 299 coeficientes que se anulavam era uma multiplicação de polinômios disfarçada — [contei a história aqui](/posts/tao-blog-milagre-desmontado/). É um tipo de problema que não existia como categoria. Pode vir a ser o ofício central da próxima geração.

Isso não elimina a dor de quem perdeu seus problemas numa noite, nem o risco da matemática em dois andares, nem a pergunta sobre os alunos. Mas desloca a questão do terreno da derrota para o da escolha — e escolher, ao contrário de demonstrar, continua sendo coisa nossa.

## Perto de casa: a rigidez de Penrose

Termino as vitrines com a que me tocou mais de perto, porque ela atravessou o corredor do meu próprio departamento.

Em setembro escrevi aqui sobre [buracos negros e a geometria de uma escuridão](/posts/buracos-negros-a-geometria-de-uma-escuridao/). Contei ali a história do teorema da massa positiva — Schoen e Yau em 1979, Witten em 1981 — e da pergunta seguinte, feita por Roger Penrose: se a massa de um sistema gravitacional isolado é não negativa, quanto ela vale **no mínimo** quando o sistema já contém um buraco negro? O argumento heurístico de Penrose encadeia a censura cósmica, o teorema da área de Hawking e o fato de que a energia só é irradiada para fora, e chega a uma desigualdade entre a massa ADM e a área $A$ do horizonte:

$$
\boxed{\;m_{ADM}\;\geq\;\sqrt{\frac{A}{16\pi}}\;}
$$

O peso dessa desigualdade está na lógica: ela é **consequência** da censura cósmica, de modo que um contraexemplo a ela seria um contraexemplo a talvez o maior problema em aberto da relatividade geral matemática. Escrevi também, com todas as letras, o estado da arte: o caso **riemanniano** — dados iniciais simétricos no tempo — estava demonstrado em dimensão três, por Huisken–Ilmanen e por Bray; o caso **geral, espaço-temporal**, em que a segunda forma fundamental $K$ dos dados não se anula, continuava em aberto.

E há a segunda metade de toda desigualdade bem-feita, a que os geômetras chamam de **rigidez**: caracterizar o caso de igualdade. No teorema da massa positiva, massa zero obriga o espaço a ser o euclidiano. Na desigualdade de Penrose, espera-se que a igualdade obrigue os dados a serem uma fatia do espaço-tempo de **Schwarzschild** — a solução de 1916 que descreve o buraco negro mais simples. No caso espaço-temporal isso é especialmente delicado, porque uma fatia de Schwarzschild não precisa ser simétrica no tempo: há fatias "inclinadas", com $K\neq 0$ e momento não nulo, que têm a mesma massa invariante. A pergunta de rigidez é se a igualdade determina os dados **originais** — a métrica $g$ e a segunda forma fundamental $K$ — como os dados induzidos de uma dessas fatias.

No repositório de 6 de outubro, a família 260 é inteira dedicada a isso. São treze manuscritos e cerca de 1 350 páginas, entre eles o mais longo do lote inteiro, com 262 páginas. O manuscrito *Equality and rigidity in the spacetime Penrose inequality*, de 160 páginas e datado de 27 de setembro, abre com este enunciado, que traduzo com a maior fidelidade que consigo:

> **Teorema (OpenAI, 2026, não arbitrado).** Sejam $(M,g,K)$ dados iniciais suaves e assintoticamente planos, com uma única extremidade, satisfazendo a condição de energia dominante, cujo bordo $S$ é marginalmente aprisionado para fora e minimizante de área por fora, sob hipóteses de decaimento e de "mais exterior" (*outermostness*) especificadas. Escreva $m=\sqrt{E^{2}-\lvert P\rvert^{2}}$ para a massa ADM invariante e $a(g)$ para o ínfimo das áreas das superfícies que envolvem o bordo. Então
>
> $$
> m\ \ge\ \frac12\left(\frac{a(g)}{\omega_{n-1}}\right)^{\frac{n-2}{n-1}},\qquad \omega_{n-1}=\lvert \mathbb{S}^{n-1}\rvert,
> $$
>
> e, se vale a **igualdade**, todo o exterior original, com seus $g$ e $K$, é uma fatia tipo espaço do exterior de **Schwarzschild–Tangherlini** de massa $m$, suavemente acoplada ao horizonte. Isso é provado em toda dimensão espacial $n\ge 3$ sob decaimento forte, e sob decaimento fraco nas dimensões $3$ e $4$. Em dimensão 3, a igualdade força ainda o horizonte a ser **uma única esfera**; se o bordo for desconexo, a desigualdade é estrita.

Para $n=3$, $\omega_2=4\pi$ e o lado direito vira exatamente $\sqrt{A/16\pi}$ — a desigualdade de Penrose do texto de setembro. Os manuscritos companheiros afirmam ainda a versão espaço-temporal da própria desigualdade, versões com carga elétrica e magnética (com Reissner–Nordström no caso de igualdade), uma versão de Kerr–Newman com rotação, e versões em espaço anti-de Sitter. Um deles chega a construir **contraexemplos** para uma das formulações da desigualdade com rotação, quando o momento angular é medido de certo modo e os campos decaem devagar.

Fui conferir, para o slide de Picos, o que a demonstração usa. Usa as ferramentas que contei em setembro: os **espinores de Witten**, o **fluxo conforme de Bray** e o **fluxo inverso da curvatura média de Huisken–Ilmanen**, entre outras. E não usa uma delas: os **conjuntos de nível de funções harmônicas**, a técnica de Daniel Stern que Rondinelle e Levi Lopes de Lima empregaram — nenhum dos dois trabalhos é citado. Também não toca, é claro, na censura cósmica, que continua sem prova e sem contraexemplo.

Se tudo isso estiver certo, é um dos resultados mais impressionantes do repositório — e talvez o mais distante da ideia de "aplicar mecanicamente um método conhecido". Mas aqui as ressalvas deste texto pesam mais do que em qualquer outro lugar. A formalização em Lean desta família é estreita: cobre uma substituição de extremidades num caso particular (dados hiperboloidais de Cha–Khuri–Sakovich) e exemplos de Schwarzschild; a própria documentação registra que a desigualdade geral **não** está formalizada, e o teorema de rigidez acima também não. São 1 350 páginas que, por enquanto, só podem ser conferidas por quem conhece a área a fundo. No mundo inteiro, são poucas dezenas de pessoas. Uma delas trabalha no corredor ao lado do meu.

Falo de **Rondinelle Marcolino Batista**, colega do nosso Programa de Pós-Graduação em Matemática, cujo seminário no Workshop de Verão de 2026 foi, como contei em setembro, o que me fez sair da arquibancada nesse assunto. Rondinelle e Levi Lopes de Lima publicaram na *Proceedings of the AMS* uma demonstração, por conjuntos de nível de funções harmônicas, de um teorema de massa positiva para variedades com bordo não compacto — exatamente a família de técnicas da qual a desigualdade de Penrose é a irmã mais velha.

O repositório foi publicado enquanto o V EMVAG começava. Montei às pressas, nos dias do encontro, uma seção de *Breaking News* para o fim da palestra. Um slide citava a frase "continua em aberto", do meu próprio texto de setembro, ao lado do que a família 260 anunciava. O seguinte dizia apenas:

> «Rondinelle, **deu ruim!** Resolveram o teu problema matemático de vida!»

Era uma provocação de colega. Mas, logo abaixo, vinha a parte mais importante: uma palavra só — **Calma** — e quatro observações antes de qualquer um pensar em mudar de área. São 160 páginas assinadas por "OpenAI", sem revisão, e **alguém precisa lê-las**: esse alguém, dizia o slide, estava na plateia. A censura cósmica continua sem prova e sem contraexemplo. A demonstração não passa pelos conjuntos de nível, de modo que a testemunha de Rondinelle — a função harmônica — ainda tem o que dizer. E resposta anunciada ainda não é teorema compreendido.

Fechei aquele slide com uma linha que, relida uma semana depois, me parece o resumo deste texto inteiro. De Sobral, em 1919, quando o eclipse confirmou a relatividade geral, a Picos, em 2026, a linha é contínua: **o gargalo já não é resolver; é compreender.** A frase do meu post sobre buracos negros ganha agora uma nota com data. Só a leitura dos especialistas dirá se ela será apagada.

Volto, então, à pergunta do diagrama de Tao, agora com nome e endereço. Em que etapa está a rigidez de Penrose? Gerada, sem dúvida. Verificada, só em parte, e não na parte principal. Exposta — 1 350 páginas escritas por uma máquina —, discutível. Publicada e canonizada, ainda não. O que separa esses manuscritos de um capítulo de livro-texto é precisamente o trabalho de pessoas como Rondinelle: ler, desconfiar, conferir, simplificar, ensinar a um aluno. O 6 de outubro não tornou esse trabalho desnecessário. Tornou-o, de uma hora para outra, o recurso mais escasso de toda a área.

## Coda: se Hilbert acordasse hoje

![David Hilbert e a função zeta de Riemann](/assets/img/hilbert-zeta.jpeg){: width="680" height="381" }
_David Hilbert (1862–1943) e a série que define a função zeta de Riemann._

Abri o texto de agosto sobre a hipótese de Riemann com uma frase de David Hilbert que a *Fermat's Library* gosta de lembrar, e quero fechar este com ela, porque nunca me pareceu tão oportuna.

> «Se eu acordasse depois de ter dormido por mil anos, minha primeira pergunta seria: a hipótese de Riemann foi provada?»

A anedota chegou até nós, como contei em agosto, por [George Pólya](/posts/george-polya-arte-de-resolver-problemas/), que a ligava à lenda do imperador Barbarossa, adormecido numa caverna à espera da hora de despertar. Hilbert havia posto a hipótese como o oitavo problema da sua célebre lista de 1900, e ela é, hoje, um dos Problemas do Milênio.

Imagine que ele acordasse agora, na quinta-feira, 15 de outubro de 2026 — não mil anos depois, mas cento e vinte e seis. Faria a pergunta. E teríamos de lhe dar uma resposta estranha, que nenhum matemático de qualquer século anterior teria sabido formular:

*Não, professor. Mas há nove dias apareceu um manuscrito de 199 páginas afirmando que todos os zeros estão presos entre as retas $\operatorname{Re} s=1/8$ e $\operatorname{Re} s=7/8$. Ele está assinado por uma empresa. Foi verificado por um programa de computador. James Maynard ficou de queixo caído. E ninguém, ainda, sabe dizer com segurança se está certo — nem exatamente por que seria.*

Imagino Hilbert em silêncio, a mão na testa, como na fotografia. Desconfio de que sua segunda pergunta seria a mais importante de todas, e a que este texto tentou fazer do começo ao fim:

**E quem a compreende?**

Hilbert, afinal, é o homem cujo epitáfio em Göttingen diz *Wir müssen wissen, wir werden wissen* — "Precisamos saber, e saberemos". Ele não escreveu "precisamos verificar". Escreveu *wissen*: saber, conhecer. A verdade de um enunciado nunca bastou a ele, nem deveria bastar a nós. No dia 6 de outubro de 2026, a matemática ganhou, de uma só vez, centenas de respostas. Resta saber se terá a paciência, a generosidade e os meios de transformá-las em conhecimento — isto é, em algo que um ser humano possa compreender, ensinar a um aluno e levar adiante.

Essa é a parte que nenhum repositório entrega. E é por isso que, apesar de tudo, continuo achando que vale a pena ser matemático.

## Referências e leituras

**O repositório e os manuscritos citados**

- OpenAI. [`openai/math`](https://github.com/openai/math) — repositório com os manuscritos, as formalizações em Lean e o histórico de revisões. Publicado em 6 out. 2026.
- OpenAI. [*The irrationality exponent of* $\pi$ *is 2*](https://github.com/openai/math/blob/main/preprints/The-irrationality-exponent-of-pi-is-2-September-24-2026/paper.pdf), manuscrito de 24 set. 2026; [escopo da formalização](https://github.com/openai/math/blob/main/lean/docs/017.md).
- OpenAI. [*The Quasi-Riemann Hypothesis: A Zero-Free Half-Plane* $\operatorname{Re} s>7/8$](https://github.com/openai/math/blob/main/preprints/The-Quasi-Riemann-Hypothesis-September-30-2026/paper.pdf), manuscrito de 30 set. 2026, 199 p.; [escopo da formalização](https://github.com/openai/math/blob/main/lean/docs/003.md).
- OpenAI. *The Quasi-Riemann Hypothesis* (demonstração de $\operatorname{Re} s>11/12$), manuscrito de 5 out. 2026, 49 p.
- Liu, B. [*Slightly improved zero-free half-planes for the quasi-Riemann hypothesis*](https://arxiv.org/abs/2610.12234). arXiv:2610.12234, out. 2026.
- Zeilberger, D.; Zudilin, W. [*The irrationality measure of* $\pi$ *is at most 7.103205334137…*](https://arxiv.org/abs/1912.06345). arXiv:1912.06345, 2019.
- Cook, J. D. [*Irrationality exponent of* $\pi$](https://www.johndcook.com/blog/2026/10/07/irrationality-exponent-of-pi/), 7 out. 2026.

**Desigualdade de Penrose e rigidez**

- OpenAI. [*Equality and rigidity in the spacetime Penrose inequality*](https://github.com/openai/math/blob/main/preprints/Equality-and-rigidity-in-the-spacetime-Penrose-inequality-September-27-2026/paper.pdf), manuscrito de 27 set. 2026.
- OpenAI. [*Spacetime Penrose inequalities: enclosing area, charge, and rigidity*](https://github.com/openai/math/blob/main/preprints/Spacetime-Penrose-inequalities-enclosing-area-charge-and-rigidity-October-5-2026/paper.pdf), manuscrito de 5 out. 2026; [escopo da formalização](https://github.com/openai/math/blob/main/lean/docs/260.md).
- Bray, H. L. *Black Holes, Geometric Flows, and the Penrose Inequality in General Relativity*. **Notices of the AMS**, v. 49, n. 10, p. 1372–1381, 2002. [PDF](https://www.ams.org/notices/200211/fea-bray.pdf).
- Batista, R. M.; de Lima, L. L. *A harmonic level set proof of a positive mass theorem*. **Proceedings of the AMS**, v. 153, p. 1761–1770, 2025. [arXiv:2306.09097](https://arxiv.org/abs/2306.09097).

**Verificação e formalização**

- Bastounis, A.; Circelli, F.; Hansen, A. C. [*Navier–Stokes lost in translation: why Lean verification of AI autoformalisation does not guarantee correct natural language proofs*](https://arxiv.org/abs/2610.08144). arXiv:2610.08144, 6 out. 2026.
- *OpenAI mistranslated mathematics into code for its Navier–Stokes proof*. **New Scientist**, out. 2026.
- *OpenAI's blockbuster Navier–Stokes proof isn't what we thought it was*. **Scientific American**, out. 2026.
- *OpenAI withdraws three preprints a day after releasing 722 manuscripts on unsolved math problems*. [**Retraction Watch**](https://retractionwatch.com/2026/10/08/openai-withdraws-preprints-722-manuscripts-unsolved-math-problems/), 8 out. 2026.
- de Moura, L. [*Postmortem for kernel soundness bug*](https://leodemoura.github.io/blog/2026-8-1-postmortem-for-kernel-soundness-bug-14576/), 1º ago. 2026 — o episódio Collatz.

**Posições da comunidade**

- Advisory Group on Mathematics and Artificial Intelligence. [*On OpenAI's release of mathematical results*](https://agmai.org/), 6 out. 2026; e *Responsible release of AI-generated mathematics*, 29 set. 2026.
- Association for Human Mathematics. [*AHM statement on OpenAI's October 6 release of mathematical documents*](https://terrytao.wordpress.com/2026/10/07/ahm-statement-on-openais-october-6-release-of-mathematical-documents/), republicado no blog *What's new*, 7 out. 2026.
- Raymond-Robichaud, P.; Chipkin, L. [*Fields medalists are wrong: why AI is an accelerant, not a bane, to progress in mathematics*](https://conjectureinstitute.org/articles/fields-medalists-are-wrong). Conjecture Institute, 6 out. 2026.
- *A Severe Misalignment of AI in Mathematics*. Declaração de medalhistas Fields, set. 2026. [mathandai.org](https://mathandai.org/).

**Palestras e entrevistas**

- Tao, T. [*Math 2.0*](https://terrytao.wordpress.com/2026/10/10/math-2-0/), palestra pública em Caltech, 9 out. 2026; [slides](https://teorth.github.io/tao-web/slides/math-2-0-caltech-2026.pdf).
- Tsimerman, J. Entrevista a Curt Jaimungal, [*Theories of Everything*](https://www.youtube.com/watch?v=6uIJdXmB4vE), ago. 2026.
- *Jacob Tsimerman wins 2026 Fields Medal for André–Oort conjecture proof*. [**Quanta Magazine**](https://www.quantamagazine.org/jacob-tsimerman-wins-2026-fields-medal-for-andre-oort-conjecture-proof-20260723/), 23 jul. 2026.
- Duminil-Copin, H. [*The strip mining of mathematical proofs*](https://www.numberphile.com/videos/hugo-ai-podcast), podcast do *Numberphile*, 14 out. 2026.
- Duminil-Copin, H. Conferência transmitida pela Société Mathématique de France, 8 out. 2026: [apresentação completa](https://www.youtube.com/watch?v=iRjasLnigsU) e [trecho](https://x.com/Fabien_Mikol/status/2108296559666634818).
- *When AI solves major open problems: what does it mean for the future of mathematics — and beyond?* Painel com A. Kontorovich, S. Wolfram e A. Moitra, gala do MoMath, 2026. [Vídeo](https://youtu.be/voDtZqijetw).
- Giansiracusa, N. Sequência de mensagens no X (@ProfNoahGian), 11 out. 2026.
- Kontorovich, A. Mensagem no X sobre a hipótese quase-Riemann, out. 2026.
- Raymond-Robichaud, P. Mensagem sobre formalização automatizada e os *Principia Mathematica*, out. 2026.

**Cobertura**

- *OpenAI just changed math forever. Exactly how, no one yet knows*. [**Science**](https://www.science.org/content/article/openai-just-changed-math-forever-exactly-how-no-one-yet-knows), 13 out. 2026.
- *AI edges closer to solving the Riemann hypothesis, one of math's hardest problems*. [**Science**](https://www.science.org/content/article/ai-edges-closer-solving-riemann-hypothesis-one-math-s-hardest-problems), out. 2026.
- *OpenAI posts 700 maths preprints online: mathematicians are up in arms*. **Nature**, out. 2026.
- *How much beauty have we lost? Mathematicians react with shock and disgust as OpenAI bulldozes their field*. [**The Decoder**](https://the-decoder.com/how-much-beauty-have-we-lost-mathematicians-react-with-shock-and-disgust-as-openai-bulldozes-their-field/), out. 2026.

**Nesta série** (todos os textos estão na [Miscelânea](/miscelanea/))

- [Uma inteligência artificial encontrou um contraexemplo para uma conjectura de 87 anos?](/posts/conjectura-jacobiana-contraexemplo-ia/), 22 jul. 2026.
- [Um contraexemplo para a conjectura de Goemans sobre fluxos não-divisíveis](/posts/contraexemplo-conjectura-goemans-fluxos/), 23 jul. 2026.
- [O milagre desmontado: Terence Tao, um blog e a arte de não aceitar coincidências](/posts/tao-blog-milagre-desmontado/), 23 jul. 2026.
- [Da escassez à abundância: a matemática na era da IA](/posts/matematica-na-era-da-ia/), 25 jul. 2026.
- [A hipótese que Hilbert queria ver provada — e um avanço inesperado](/posts/hipotese-de-riemann-avanco-inesperado/), 11 ago. 2026.
- [Buracos negros: a geometria de uma escuridão](/posts/buracos-negros-a-geometria-de-uma-escuridao/), 4 set. 2026.
- [Navier–Stokes (I): anatomia de um problema do milênio](/posts/navier-stokes-i-anatomia-de-um-problema-do-milenio/), 14 set. 2026.
- [Navier–Stokes (II): a controvérsia, contada pelos documentos](/posts/navier-stokes-ii-a-controversia-contada-pelos-documentos/), 15 set. 2026.
- [Navier–Stokes (III): o que significa ser matemático na era da IA](/posts/navier-stokes-iii-o-que-significa-ser-matematico-na-era-da-ia/), 16 set. 2026.
