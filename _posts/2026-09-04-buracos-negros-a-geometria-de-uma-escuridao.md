---
title: "Buracos negros: a geometria de uma escuridão"
date: 2026-09-04 18:00:00 -0300
categories: [Miscelânea, Matemática]
tags: [relatividade geral, buracos negros, Oppenheimer, Lemaître, Penrose, Hawking, Witten, teorema da massa positiva, conjectura de Penrose, geometria diferencial]
math: true
---

Em **1º de setembro de 1939**, a *Physical Review* publicou um artigo de cinco páginas assinado por J. Robert Oppenheimer e por seu aluno Hartland Snyder: *On Continued Gravitational Contraction*. No mesmo dia, a Alemanha invadiu a Polônia.

A coincidência é quase literária e ajuda a explicar por que o artigo passou despercebido, mas não é a única razão. A relatividade geral vivia um período de baixa: elegante, matematicamente pesada e experimentalmente estéril. E a conclusão — que uma estrela suficientemente massiva, ao esgotar seu combustível termonuclear, simplesmente **continua a colapsar, sem que nada a detenha** — soava menos como previsão e mais como sinal de que faltava algum ingrediente físico. Nem Oppenheimer nem Snyder escreveram "buraco negro"; o termo só se popularizaria nos anos 1960, com John Wheeler.

Quero usar essa data como fio para puxar uma história em que a física propõe as perguntas e a **geometria diferencial** acaba encarregada de respondê-las. Ela passa por um padre católico belga, por um físico esquecido em Calcutá, pelo único físico a receber uma Medalha Fields, e termina em dois problemas de geometria — um resolvido pela metade, outro em aberto.

## O padre que descongelou a singularidade

Antes de Oppenheimer é preciso falar de **Georges Lemaître** (1894–1966), padre católico belga, doutor pelo MIT, professor em Louvain, lembrado por ter obtido em 1927 soluções em expansão das equações de Einstein — dois anos antes de Hubble — e por ter proposto, em 1931, a hipótese do *átomo primitivo*. Menos conhecida, e mais relevante aqui, é sua contribuição de **1933**.

A métrica de Schwarzschild, de 1916,

$$
g = -\Big(1-\frac{2m}{r}\Big)\,dt^{2} + \Big(1-\frac{2m}{r}\Big)^{-1} dr^{2} + r^{2} d\Omega^{2},
$$

parece degenerar em dois lugares: em $r=0$ e em $r=2m$, o raio gravitacional, que em unidades usuais vale $r_s = 2GM/c^{2}$. Por quase duas décadas acreditou-se que $r=2m$ era uma fronteira física, uma parede onde a teoria deixava de valer.

Lemaître mostrou que não. Em coordenadas comóveis com a matéria em queda livre — as que hoje levam seu nome — a singularidade em $r=2m$ simplesmente **desaparece**. Era, nas palavras dele, uma *singularidade fictícia*: artefato do sistema de coordenadas, não da geometria. O que existe em $r=2m$ não é uma parede; é uma **superfície de não-retorno**.

Há aí uma lição que vale muito além do assunto: **um obstáculo pode ser artefato da linguagem em que o problema foi escrito**. Trocar a carta, mudar o espaço funcional, reescolher a norma — boa parte do que fazemos em equações dispersivas é isso.

## Oppenheimer, Snyder — e Datt

Removido o obstáculo, a pergunta seguinte é dinâmica: o que acontece com uma estrela que colapsa?

O modelo de Oppenheimer e Snyder é uma idealização deliberadamente brutal: uma esfera homogênea de **poeira**, matéria sem pressão, colapsando sob a própria gravidade. Fora dela, por Birkhoff, a geometria é a de Schwarzschild; dentro, é um pedaço de universo de Friedmann em contração. As duas peças se colam na superfície da estrela, e o problema fica solúvel. O resultado tem uma estrutura dupla que é o coração da coisa:

- Para um observador **comóvel com a matéria** — alguém caindo junto com a estrela — o colapso tem duração **finita**. O tempo próprio até o centro é finito e, para massas estelares típicas, da ordem de **um dia**.
- Para um observador **externo**, distante e estático, o colapso **nunca termina**. A superfície da estrela aproxima-se assintoticamente do raio gravitacional, a luz que dela escapa é cada vez mais desviada para o vermelho, e o cone de ângulos por onde os fótons ainda fogem se estreita. A estrela não explode nem some com um estalo: ela *apaga*.

Nenhum dos dois está errado. É uma das declarações mais limpas da relatividade geral: **o tempo não é um pano de fundo comum, e "o que acontece" depende de quem pergunta.**

Há aqui um capítulo que costuma ficar de fora das versões apressadas. Um ano antes, em **1938**, o físico indiano **Bhaktibhusan Datt**, do Presidency College de Calcutá, publicou na *Zeitschrift für Physik* uma classe mais geral de soluções de colapso de poeira, da qual o caso de Oppenheimer–Snyder é essencialmente um subcaso. O trabalho ficou obscuro por décadas; Datt morreu jovem, e só em 1999 o artigo foi reimpresso na série *Golden Oldies* da *General Relativity and Gravitation*. Por isso o modelo é às vezes chamado de **Oppenheimer–Snyder–Datt**.

Freeman Dyson chamaria o artigo de 1939 de "a única e verdadeiramente revolucionária contribuição de Oppenheimer à ciência" — o próprio Oppenheimer, segundo Abraham Pais, não concordava, e apontava seus trabalhos iniciais sobre elétrons e pósitrons.

## Penrose: quando a topologia entra em campo

O modelo de Oppenheimer–Snyder é *perfeitamente simétrico*, e a objeção óbvia — feita durante décadas — era que a singularidade seria artefato dessa simetria: bastaria um pouco de rotação e a matéria "erraria" o centro. Em **1965**, **Roger Penrose** encerrou o debate com três páginas na *Physical Review Letters*. A ideia central é a de **superfície aprisionada**: uma superfície fechada bidimensional $S$ tal que **ambas** as congruências de geodésicas nulas ortogonais a $S$ têm expansão negativa — isto é, mesmo a luz emitida para fora está convergindo. Formada uma superfície assim, não há como desfazê-la. O teorema diz, em essência: se o espaço-tempo satisfaz uma condição de energia razoável, tem superfície de Cauchy não compacta e contém uma superfície aprisionada, então é **geodesicamente incompleto** — há geodésicas que simplesmente terminam. A singularidade não é acidente de simetria; é consequência estrutural.

O marco não é só o enunciado, mas o **método**: Penrose não resolveu equação nenhuma, importou para a relatividade geral o arsenal da topologia diferencial e da geometria global — mudança de linguagem tão radical quanto a de Lemaître, que lhe valeria metade do Nobel de Física de 2020.

## Hawking: área, temperatura, entropia

**Stephen Hawking** entra com um resultado geométrico e uma consequência termodinâmica. O geométrico é o **teorema da área** (1971): sob condições de energia adequadas, e supondo censura cósmica, a área do horizonte de eventos nunca decresce, $dA/dt \geq 0$. A semelhança com a segunda lei da termodinâmica é evidente demais para ser coincidência, e Jacob Bekenstein levou-a a sério. Hawking resistiu, tentou refutar, e provou algo mais forte: em 1974, incorporando teoria quântica de campos ao espaço-tempo curvo, mostrou que um buraco negro **irradia** como um corpo negro, com temperatura e entropia

$$
T_H = \frac{\hbar c^{3}}{8\pi G M k_B},
\qquad
S = \frac{k_B A}{4 \ell_P^{2}} .
$$

A entropia — uma medida de informação — é proporcional à **área**, não ao volume: daí nasce o programa holográfico. E a radiação faz o buraco negro perder massa e **diminuir** a área do horizonte, violando o teorema clássico no regime quântico — conflito do qual nasceu o paradoxo da informação.

## Witten: o único físico com uma Medalha Fields

Em 1990, no ICM de Kyoto, a União Matemática Internacional concedeu a Medalha Fields a **Edward Witten** — até hoje o único físico a recebê-la. No endereço escrito ao Congresso, Michael Atiyah observou:

> *Although he is definitely a physicist (as his list of publications clearly shows) his command of mathematics is rivaled by few mathematicians, and his ability to interpret physical ideas in mathematical form is quite unique. ... In his hands physics is once again providing a rich source of inspiration and insight in mathematics.*

A citação costuma ser lembrada pelos invariantes de Donaldson e pela teoria de Chern–Simons. Mas há um item na lista que interessa diretamente a esta história, e é onde a narrativa dobra da física para a matemática pura: em **1981**, Witten deu uma demonstração espinorial do **teorema da massa positiva**.

## Massa: um número que vive no infinito

Considere uma variedade riemanniana tridimensional $(M,g)$ **assintoticamente plana**: fora de um compacto ela é difeomorfa ao complementar de uma bola em $\mathbb{R}^{3}$ e, nessa carta, os coeficientes da métrica se aproximam dos euclidianos a uma taxa controlada. Fisicamente, é um **dado inicial** — no caso simétrico no tempo — para um sistema gravitacional isolado. A construção de Arnowitt, Deser e Misner lhe associa um invariante assintótico, a **massa ADM**:

$$
m_{ADM}(M,g) \;=\; \lim_{r\to+\infty}\frac{1}{16\pi}\int_{S^{2}_{r}} \big(g_{ij,j}-g_{jj,i}\big)\,\mu^{i}\, dS^{2}_{r},
$$

onde $\mu$ é o normal unitário exterior às esferas coordenadas grandes. Sob decaimento razoável, esse número é conservado na evolução dos dados iniciais.

O **teorema da massa positiva** afirma que, sob uma condição de energia dominante — no caso simétrico no tempo, simplesmente **curvatura escalar não negativa**, $R_g \geq 0$ — vale $m_{ADM} \geq 0$, com igualdade **se e somente se** $(M,g)$ é isométrica ao espaço euclidiano.

O enunciado parece inofensivo, mas a dificuldade está numa assimetria de natureza: a massa ADM é uma **integral de fluxo no infinito**, cujo integrando não guarda relação algébrica direta com a curvatura escalar, que é a densidade de energia relevante. Provar o teorema exige construir um **objeto global** que medeie entre o comportamento no infinito e a curvatura no interior.

As duas primeiras soluções escolheram mediadores diferentes. **Schoen e Yau** (1979) usaram **superfícies mínimas**, cuja existência a segunda variação, combinada com $R_g\ge 0$ e Gauss–Bonnet, acaba proibindo se a massa for negativa. **Witten** (1981) usou **espinores harmônicos**: resolvendo a equação de Dirac com condição assintótica constante, a massa aparece como uma integral manifestamente não negativa — mais curto e mais transparente, ao custo de exigir que a variedade seja *spin*. É o exemplo perfeito da observação de Atiyah: energia como norma de um espinor, ideia inteiramente física, convertida em teorema de geometria riemanniana global.

## A conjectura de Penrose

Se a massa é não negativa, quanto ela vale *no mínimo* quando o sistema já contém um buraco negro?

Penrose respondeu com um argumento heurístico admirável, essencialmente um teste de consistência da relatividade geral consigo mesma. Suponha um dado inicial com horizonte de área $A$ e evolua no tempo. Pela **censura cósmica**, o sistema deve relaxar para um buraco negro de Kerr, para o qual vale $m_{\text{fin}} \geq \sqrt{A_{\text{fin}}/16\pi}$; pelo **teorema da área**, $A_{\text{fin}} \geq A$; e como energia só é irradiada para fora, $m_{ADM} \geq m_{\text{fin}}$. Encadeando:

$$
\boxed{\;m_{ADM} \;\geq\; \sqrt{\frac{A}{16\pi}}\;}
$$

Note a lógica: a desigualdade é uma **consequência** da censura cósmica, de modo que um contraexemplo geométrico a ela seria um contraexemplo à censura cósmica — provavelmente o maior problema em aberto da relatividade geral matemática.

Devo ser honesto sobre os limites do que posso dizer: **não sou da área**, sou um admirador. Registro só o essencial. O caso **riemanniano** — dados iniciais simétricos no tempo — está demonstrado em dimensão três por meio de fluxos geométricos, e a prova *usa* o teorema da massa positiva como degrau. O caso **geral, espaço-temporal, continua em aberto**. Para o panorama técnico, o artigo de Hubert Bray nas *Notices of the AMS* é melhor do que eu saberia fazer.

## Uma palestra num workshop de verão

Confesso que, até pouco tempo atrás, eu observava tudo isso da arquibancada — meu território é outro: equações dispersivas, boa colocação, tempos longos. O que mudou foi uma palestra. No **Workshop de Verão de 2026**, aqui mesmo, assisti ao seminário do colega **Rondinelle Marcolino Batista**, do nosso Programa de Pós-Graduação em Matemática. Foi ali, ouvindo alguém do corredor ao lado falar de massa positiva e da conjectura de Penrose com a naturalidade de quem trabalha nisso há anos, que o assunto deixou de ser leitura de fim de semana e passou a me ocupar de verdade.

Rondinelle e **Levi Lopes de Lima** (UFC) publicaram na *Proceedings of the American Mathematical Society* o artigo *A harmonic level set proof of a positive mass theorem*. A técnica, introduzida por Daniel Stern, é recente e bonita: em vez de superfícies mínimas ou espinores, o mediador global é uma **função harmônica**, e a informação geométrica sai dos seus **conjuntos de nível**, que folheiam a variedade. O cenário é uma variação sutil do clássico: variedades assintoticamente planas com **bordo não compacto**, modeladas no semiespaço euclidiano, para as quais Almaraz, Barbosa e de Lima introduziram o invariante de massa apropriado, $\mathfrak{m}_{(M,g)}$. O resultado é quantitativo:

$$
\mathfrak{m}_{(M,g)} \;\geq\; \frac{1}{16\pi}\int_{M_{\mathrm{ext}}}\left(\frac{|\nabla^{2}u|^{2}}{|\nabla u|} + R_g |\nabla u|\right) dV \;+\; \frac{1}{8\pi}\int_{\Sigma_{\mathrm{ext}}} H_g |\nabla u|\, dA,
$$

para uma função harmônica $u$ escolhida adequadamente na região exterior. A não negatividade da massa é imediata: se a curvatura escalar $R_g$ e a curvatura média do bordo $H_g$ são não negativas, o lado direito é soma de termos não negativos.

A estrutura é bonita: à esquerda, um número que só existe **no infinito**; à direita, integrais de curvatura **no interior** e **no bordo**. A função $u$ é o mediador global de que falei acima — o mesmo papel das superfícies mínimas em Schoen–Yau e dos espinores em Witten. Três gerações de técnicas, três mediadores, um mesmo teorema.

A distância entre meu território e esse, aliás, era menor do que eu imaginava. Um campo escalar sobre um fundo de Schwarzschild obedece a uma equação de onda com potencial; separando variáveis, sobra uma **equação radial** do tipo **Heun confluente**, e os modos quase-normais — as frequências que o LIGO escuta no *ringdown* — são um problema espectral não autoadjunto para essa EDO: o mesmo vocabulário que eu já usava, aplicado a outro operador. Nos últimos meses tenho colaborado nesse terreno com **Helder Alexander Santos e Costa**, do Programa de Pós-Graduação em Física da UFPI, num trabalho sobre ondas escalares num buraco negro de Schwarzschild com **violação da simetria de Lorentz**; em julho participei, como examinador externo, da banca de qualificação de mestrado de João Guilherme Rodrigues Valangelis sobre esse mesmo problema.

## O fio

A conjectura de Penrose no caso geral continua aberta, e a censura cósmica permanece sem prova e sem contraexemplo, meio século depois de formulada. É um caso raro em que a física fez a pergunta, a geometria assumiu a responsabilidade de respondê-la, e a resposta ainda não veio — não por falta de ideias, mas porque o problema é, simplesmente, muito difícil.

De Louvain em 1933, de Calcutá em 1938, de Berkeley em 1939, até um seminário de verão em Teresina em 2026 — a linha é contínua. É bom, de vez em quando, percebê-la.

## Referências e leituras

- Oppenheimer, J. R.; Snyder, H. *On Continued Gravitational Contraction*. **Physical Review**, v. 56, p. 455–459, 1939. [DOI: 10.1103/PhysRev.56.455](https://doi.org/10.1103/PhysRev.56.455).
- Datt, B. *Über eine Klasse von Lösungen der Gravitationsgleichungen der Relativität*. **Zeitschrift für Physik**, v. 108, p. 314, 1938. Reimpresso como *Golden Oldie* em **General Relativity and Gravitation**, 1999, com nota de A. Krasiński.
- Lemaître, G. *L'Univers en expansion*. **Annales de la Société Scientifique de Bruxelles**, A, v. 53, p. 51–85, 1933.
- Penrose, R. *Gravitational Collapse and Space-Time Singularities*. **Physical Review Letters**, v. 14, p. 57–59, 1965. [DOI: 10.1103/PhysRevLett.14.57](https://doi.org/10.1103/PhysRevLett.14.57).
- Hawking, S. W. *Black hole explosions?* **Nature**, v. 248, p. 30–31, 1974. [DOI: 10.1038/248030a0](https://doi.org/10.1038/248030a0).
- Schoen, R.; Yau, S.-T. *On the proof of the positive mass conjecture in general relativity*. **Communications in Mathematical Physics**, v. 65, p. 45–76, 1979.
- Witten, E. *A new proof of the positive energy theorem*. **Communications in Mathematical Physics**, v. 80, p. 381–402, 1981.
- Bray, H. L. *Black Holes, Geometric Flows, and the Penrose Inequality in General Relativity*. **Notices of the AMS**, v. 49, n. 10, p. 1372–1381, 2002. [PDF](https://www.ams.org/notices/200211/fea-bray.pdf).
- **Batista, R. M.; de Lima, L. L.** *A harmonic level set proof of a positive mass theorem*. **Proceedings of the American Mathematical Society**, v. 153, p. 1761–1770, 2025. [DOI: 10.1090/proc/17192](https://doi.org/10.1090/proc/17192) · [arXiv:2306.09097](https://arxiv.org/abs/2306.09097).
- Nascimento, A. C.; Costa, H. A. S. e; Wuc, S.; Valangelis, J. G. R. *An analytical study on the scalar waves scattering by a Lorentz-violating Schwarzschild black-hole*. Submetido, 2026.
