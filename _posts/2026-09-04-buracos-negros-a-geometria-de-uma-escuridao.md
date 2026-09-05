---
title: "Buracos negros: a geometria de uma escuridão"
date: 2026-09-04 18:00:00 -0300
categories: [Miscelânea, Matemática]
tags: [relatividade geral, buracos negros, Oppenheimer, Lemaître, Penrose, Hawking, Witten, Einstein, teorema da massa positiva, conjectura de Penrose, geometria diferencial, unificação]
math: true
---

Em **1º de setembro de 1939**, a *Physical Review* publicou um artigo de cinco páginas assinado por J. Robert Oppenheimer (1904–1967) e por seu aluno Hartland Snyder (1913–1962): *On Continued Gravitational Contraction*. No mesmo dia, a Alemanha invadiu a Polônia.

A coincidência é quase literária e ajuda a explicar por que o artigo passou despercebido, mas não é a única razão. A relatividade geral vivia um período de baixa: elegante, matematicamente pesada e experimentalmente estéril. E a conclusão — que uma estrela suficientemente massiva, ao esgotar seu combustível termonuclear, simplesmente **continua a colapsar, sem que nada a detenha** — soava menos como previsão e mais como sinal de que faltava algum ingrediente físico.

Vale medir o que aquelas cinco páginas fizeram. Até 1939, a relatividade geral havia dito coisas notáveis sobre o *estado* das coisas: a órbita de Mercúrio, o desvio da luz, a geometria em torno de uma massa parada. O artigo de Oppenheimer e Snyder foi a primeira vez em que a teoria descreveu, do começo ao fim e com solução explícita, um **processo irreversível** acontecendo com um objeto astrofísico real. Não é uma curiosidade sobre uma solução exótica das equações de Einstein: é a afirmação de que a gravitação, levada às últimas consequências, produz regiões do universo das quais nada retorna. Tudo o que veio depois — os teoremas de singularidade, a termodinâmica dos horizontes, a astronomia de ondas gravitacionais, e boa parte da geometria que este texto vai percorrer — desce daquele artigo. Nem Oppenheimer nem Snyder escreveram "buraco negro"; o termo só se popularizaria nos anos 1960, com John Archibald Wheeler (1911–2008).

Quero usar essa data como fio para puxar uma história em que a física propõe as perguntas e a **geometria diferencial** acaba encarregada de respondê-las. Ela passa por um padre católico belga, por um físico esquecido em Calcutá, pelo único físico a receber uma Medalha Fields, e termina em dois problemas de geometria — um resolvido pela metade, outro em aberto — e no sonho mais antigo e mais teimoso da física.

## O padre que descongelou a singularidade

Antes de Oppenheimer é preciso falar de **Georges Lemaître** (1894–1966), padre católico belga, doutor pelo MIT, professor em Louvain, lembrado por ter obtido em 1927 soluções em expansão das equações de Einstein — dois anos antes das medidas de Edwin Hubble (1889–1953) — e por ter proposto, em 1931, a hipótese do *átomo primitivo*. Menos conhecida, e mais relevante aqui, é sua contribuição de **1933**.

A métrica obtida por Karl Schwarzschild (1873–1916) em 1916, poucos meses depois de Albert Einstein (1879–1955) publicar as equações de campo,

$$
g = -\Big(1-\frac{2m}{r}\Big)\,dt^{2} + \Big(1-\frac{2m}{r}\Big)^{-1} dr^{2} + r^{2} d\Omega^{2},
$$

parece degenerar em dois lugares: em $r=0$ e em $r=2m$, o raio gravitacional, que em unidades usuais vale $r_s = 2GM/c^{2}$. Por quase duas décadas acreditou-se que $r=2m$ era uma fronteira física, uma parede onde a teoria deixava de valer.

Lemaître mostrou que não. Em coordenadas comóveis com a matéria em queda livre — as que hoje levam seu nome — a singularidade em $r=2m$ simplesmente **desaparece**. Era, nas palavras dele, uma *singularidade fictícia*: artefato do sistema de coordenadas, não da geometria. A distinção é a mesma que separa o polo norte de um globo, onde os meridianos se encontram e as coordenadas falham, de um bico genuíno numa superfície: no primeiro caso a geometria está perfeitamente bem, é o mapa que não serve. O que existe em $r=2m$ não é uma parede; é uma **superfície de não-retorno**.

Há aí uma lição que vale muito além do assunto: **um obstáculo pode ser artefato da linguagem em que o problema foi escrito**. Trocar a carta, mudar o espaço funcional, reescolher a norma — boa parte do que fazemos em equações dispersivas é isso.

## Oppenheimer, Snyder — e Datt

Removido o obstáculo, a pergunta seguinte é dinâmica: o que acontece com uma estrela que colapsa?

O modelo de Oppenheimer e Snyder é uma idealização deliberadamente brutal: uma esfera homogênea de **poeira** — matéria sem pressão, que não oferece nenhuma resistência ao próprio peso — colapsando sob a gravidade. A engenhosidade está em como as duas regiões, dentro e fora da estrela, são tratadas.

**Fora**, vale o teorema provado por George David Birkhoff (1884–1944) em 1923: *toda solução das equações de Einstein no vácuo que seja esfericamente simétrica é automaticamente estática e coincide com a de Schwarzschild*. É o análogo relativístico do teorema das cascas de Newton, e a consequência é forte: a região vazia em torno de qualquer distribuição esférica de matéria tem exatamente a geometria de Schwarzschild — mesmo que a matéria esteja pulsando, ou desabando. O colapso não emite ondas gravitacionais nem altera o campo externo; visto de fora, nada muda.

**Dentro**, a poeira homogênea obedece às mesmas equações que Alexander Friedmann (1888–1925) escreveu em 1922 para descrever um universo em expansão, com uma só diferença: o sinal da velocidade inicial. Em vez de expandir, contrai. O interior da estrela é, literalmente, um pedaço de cosmologia rodando de trás para a frente. As duas peças se colam ao longo da superfície da estrela, e o problema fica exatamente solúvel.

O resultado tem uma estrutura dupla que é o coração da coisa:

- Para um observador **comóvel com a matéria** — alguém caindo junto com a estrela — o colapso tem duração **finita**. O tempo próprio até o centro é finito e, para massas estelares típicas, da ordem de **um dia**.
- Para um observador **externo**, distante e estático, o colapso **nunca termina**. A superfície da estrela aproxima-se assintoticamente do raio gravitacional, a luz que dela escapa é cada vez mais desviada para o vermelho, e o cone de ângulos por onde os fótons ainda fogem se estreita. A estrela não explode nem some com um estalo: ela *apaga*.

Nenhum dos dois está errado. É uma das declarações mais limpas da relatividade geral: **o tempo não é um pano de fundo comum, e "o que acontece" depende de quem pergunta.**

Há aqui um capítulo que costuma ficar de fora das versões apressadas. Um ano antes, em **1938**, o físico indiano **Bhaktibhusan Datt**, do Presidency College de Calcutá, publicou na *Zeitschrift für Physik* uma classe mais geral de soluções de colapso de poeira, da qual o caso de Oppenheimer–Snyder é essencialmente um subcaso. O trabalho ficou obscuro por décadas; Datt morreu por volta de 1940, ainda muito jovem, em consequência de uma cirurgia malsucedida, e só em 1999 o artigo foi reimpresso na série *Golden Oldies* da *General Relativity and Gravitation*. Por isso o modelo é às vezes chamado de **Oppenheimer–Snyder–Datt**.

Sobre o peso do artigo de 1939, o julgamento mais citado é o de Freeman Dyson (1923–2020), que o chamou de "a única e verdadeiramente revolucionária contribuição de Oppenheimer à ciência" — afirmação forte sobre alguém que também assinou trabalhos fundadores sobre estrelas de nêutrons e sobre chuveiros de raios cósmicos, e que dirigiria o laboratório de Los Alamos. O próprio Oppenheimer, segundo Abraham Pais (1918–2000), não concordava: perguntado sobre suas principais contribuições, apontava seus trabalhos iniciais sobre elétrons e pósitrons. É um caso raro em que a posteridade e o autor discordam frontalmente, e a posteridade venceu.

## Penrose: quando a topologia entra em campo

O modelo de Oppenheimer–Snyder é *perfeitamente simétrico*, e a objeção óbvia — feita durante décadas — era que a singularidade seria artefato dessa simetria: bastaria um pouco de rotação e a matéria "erraria" o centro. Em **1965**, **Roger Penrose** (n. 1931) encerrou o debate com três páginas na *Physical Review Letters*.

A ideia central é a de **superfície aprisionada**: uma superfície fechada bidimensional $S$ tal que **ambas** as congruências de geodésicas nulas ortogonais a $S$ têm expansão negativa — isto é, mesmo a luz emitida para fora está convergindo. Formada uma superfície assim, não há como desfazê-la.

O enunciado exige mais uma hipótese, e ela merece explicação. Uma **superfície de Cauchy** é uma "fatia de agora": uma hipersuperfície que toda trajetória causal — todo raio de luz, toda partícula — atravessa exatamente uma vez. Dar dados sobre ela determina, em princípio, o passado e o futuro inteiros do espaço-tempo, do mesmo modo que uma condição inicial determina a solução de uma equação diferencial; o nome homenageia Augustin-Louis Cauchy (1789–1857), que formulou o problema de valores iniciais. Pedir que ela seja **não compacta** é pedir que o espaço se estenda indefinidamente, como o de um sistema isolado mergulhado num universo aberto, em vez de se fechar sobre si mesmo.

O teorema diz então: se o espaço-tempo satisfaz uma condição de energia razoável, tem uma superfície de Cauchy não compacta e contém uma superfície aprisionada, então é **geodesicamente incompleto** — há geodésicas que simplesmente terminam. A singularidade não é acidente de simetria; é consequência estrutural.

O marco não é só o enunciado, mas o **método**: Penrose não resolveu equação nenhuma, importou para a relatividade geral o arsenal da topologia diferencial e da geometria global — mudança de linguagem tão radical quanto a de Lemaître, que lhe valeria metade do Nobel de Física de 2020.

## Hawking: área, temperatura, entropia

**Stephen Hawking** (1942–2018) entra com um resultado geométrico e uma consequência termodinâmica. O geométrico é o **teorema da área** (1971): sob condições de energia adequadas, e supondo censura cósmica, a área do horizonte de eventos nunca decresce, $dA/dt \geq 0$. A semelhança com a segunda lei da termodinâmica é evidente demais para ser coincidência, e Jacob Bekenstein (1947–2015) levou-a a sério. Hawking resistiu, tentou refutar, e provou algo mais forte: em 1974, incorporando teoria quântica de campos ao espaço-tempo curvo, mostrou que um buraco negro **irradia** como um corpo negro, com temperatura e entropia

$$
T_H = \frac{\hbar c^{3}}{8\pi G M k_B},
\qquad
S = \frac{k_B A}{4 \ell_P^{2}} .
$$

A entropia — uma medida de informação — é proporcional à **área**, não ao volume: daí nasce o programa holográfico. E a radiação faz o buraco negro perder massa e **diminuir** a área do horizonte, violando o teorema clássico no regime quântico — conflito do qual nasceu o paradoxo da informação. Guarde esse ponto: é a primeira vez que a relatividade geral e a mecânica quântica são forçadas a falar uma com a outra sobre o mesmo objeto, e voltaremos a ele no fim.

## Witten: o único físico com uma Medalha Fields

Em 1990, no Congresso Internacional de Matemáticos em Kyoto, a União Matemática Internacional concedeu a Medalha Fields a **Edward Witten** (n. 1951) — até hoje o único físico a recebê-la. No endereço escrito ao Congresso, Michael Atiyah (1929–2019) observou:

> *Although he is definitely a physicist (as his list of publications clearly shows) his command of mathematics is rivaled by few mathematicians, and his ability to interpret physical ideas in mathematical form is quite unique. Time and again he has surprised the mathematical community by a brilliant application of physical insight leading to new and deep mathematical theorems ... In his hands physics is once again providing a rich source of inspiration and insight in mathematics.*

A citação costuma ser lembrada pelos invariantes de Donaldson e pela teoria de Chern–Simons. Mas há um item na lista que interessa diretamente a esta história, e é onde a narrativa dobra da física para a matemática pura: em **1981**, Witten deu uma demonstração espinorial do **teorema da massa positiva**.

## Massa: um número que vive no infinito

Considere uma variedade riemanniana tridimensional $(M,g)$ **assintoticamente plana**: fora de um compacto ela é difeomorfa ao complementar de uma bola em $\mathbb{R}^{3}$ e, nessa carta, os coeficientes da métrica se aproximam dos euclidianos a uma taxa controlada. Fisicamente, é um **dado inicial** — no caso simétrico no tempo — para um sistema gravitacional isolado. A construção de Richard Arnowitt (1928–2014), Stanley Deser (1931–2023) e Charles Misner (1932–2023) lhe associa um invariante assintótico, a **massa ADM**:

$$
m_{ADM}(M,g) \;=\; \lim_{r\to+\infty}\frac{1}{16\pi}\int_{S^{2}_{r}} \big(g_{ij,j}-g_{jj,i}\big)\,\mu^{i}\, dS^{2}_{r},
$$

onde $\mu$ é o normal unitário exterior às esferas coordenadas grandes. Sob decaimento razoável, esse número é conservado na evolução dos dados iniciais.

O **teorema da massa positiva** afirma que, sob uma condição de energia dominante — no caso simétrico no tempo, simplesmente **curvatura escalar não negativa**, $R_g \geq 0$ — vale $m_{ADM} \geq 0$, com igualdade **se e somente se** $(M,g)$ é isométrica ao espaço euclidiano.

O enunciado parece inofensivo, e a dificuldade está numa incompatibilidade de naturezas. A massa ADM é uma **integral de superfície no infinito**: o que se mede é o fluxo de uma certa 1-forma através de esferas cada vez maiores. A hipótese, por outro lado, é uma desigualdade **pontual no interior**, sobre a curvatura escalar. Nenhuma manipulação algébrica leva de uma à outra, porque o integrando no infinito não é a curvatura escalar nem função dela.

O que uma demonstração precisa produzir, então, é uma **identidade integral**: uma igualdade que converta aquele fluxo no infinito numa integral, sobre todo o interior, de uma quantidade que a hipótese $R_g \ge 0$ obrigue a ser não negativa. Todo o trabalho está em encontrar um objeto — uma superfície, um campo, uma função — definido na variedade inteira, cuja equação diferencial produza exatamente essa igualdade, com a massa aparecendo como termo de fronteira no infinito. Chamemos esse objeto de **testemunha**. As três grandes provas do teorema são três escolhas de testemunha.

**Richard Schoen** (n. 1950) e **Shing-Tung Yau** (n. 1949), em 1979, escolheram **superfícies mínimas**. Supondo por absurdo que a massa fosse negativa, constroem uma superfície mínima estável completa; a fórmula da segunda variação da área, combinada com $R_g\ge 0$ e com o teorema de Gauss–Bonnet, mostra que tal superfície não pode existir.

**Witten**, em 1981, escolheu **espinores**. Um espinor é o objeto que se transforma sob rotações como uma "raiz quadrada" de um vetor — o campo dos elétrons na equação de Paul Dirac (1902–1984). Witten toma um espinor $\psi$ que tende a um espinor constante no infinito e resolve a equação de Dirac, $D\psi = 0$. A fórmula de Lichnerowicz — devida a André Lichnerowicz (1915–1998) — relaciona o quadrado do operador de Dirac ao laplaciano bruto e à curvatura escalar:

$$
D^{2} \;=\; \nabla^{*}\nabla + \tfrac{1}{4}R_g .
$$

Integrando essa identidade sobre a variedade e usando o decaimento assintótico, o termo de fronteira no infinito reproduz **exatamente** a massa ADM, e o que sobra no interior é

$$
m_{ADM} \;=\; \frac{1}{16\pi}\int_{M}\Big(|\nabla\psi|^{2} + \tfrac{1}{4} R_g\,|\psi|^{2}\Big)\,dV .
$$

A não negatividade é imediata: os dois termos são não negativos. E o caso de igualdade sai de graça — se a massa é zero, então $\nabla\psi=0$, o espinor é paralelo, e uma variedade que admite espinores paralelos suficientes é plana. A prova cabe em poucas páginas, contra as dezenas de Schoen–Yau. O preço é uma hipótese topológica: a variedade precisa ser *spin*, isto é, admitir a estrutura sobre a qual espinores podem ser definidos.

É o exemplo perfeito da observação de Atiyah. A energia escrita como norma ao quadrado de um espinor é uma ideia inteiramente física — vem da supergravidade — e vira, sem tradução, um teorema de geometria riemanniana global.

## A conjectura de Penrose

Se a massa é não negativa, quanto ela vale *no mínimo* quando o sistema já contém um buraco negro?

Penrose respondeu com um argumento heurístico admirável, essencialmente um teste de consistência da relatividade geral consigo mesma. Suponha um dado inicial com horizonte de área $A$ e evolua no tempo. Pela **censura cósmica** — a hipótese de que singularidades ficam sempre escondidas atrás de horizontes —, o sistema deve relaxar para um buraco negro de Kerr, a família de soluções em rotação descoberta por Roy Kerr (n. 1934) em 1963, para a qual vale $m_{\text{fin}} \geq \sqrt{A_{\text{fin}}/16\pi}$; pelo **teorema da área**, $A_{\text{fin}} \geq A$; e como energia só é irradiada para fora, $m_{ADM} \geq m_{\text{fin}}$. Encadeando:

$$
\boxed{\;m_{ADM} \;\geq\; \sqrt{\frac{A}{16\pi}}\;}
$$

Note a lógica: a desigualdade é uma **consequência** da censura cósmica, de modo que um contraexemplo geométrico a ela seria um contraexemplo à censura cósmica — provavelmente o maior problema em aberto da relatividade geral matemática.

Devo ser honesto sobre os limites do que posso dizer: **não sou da área**, sou um admirador. Registro só o essencial. O caso **riemanniano** — dados iniciais simétricos no tempo — está demonstrado em dimensão três por meio de fluxos geométricos, e a prova *usa* o teorema da massa positiva como degrau. O caso **geral, espaço-temporal, continua em aberto**. Para o panorama técnico, o artigo de Hubert Bray nas *Notices of the AMS* é melhor do que eu saberia fazer.

## Uma palestra num workshop de verão

Confesso que, até pouco tempo atrás, eu observava tudo isso da arquibancada — meu território é outro: equações dispersivas, boa colocação, tempos longos. O que mudou foi uma palestra. No **Workshop de Verão de 2026**, aqui mesmo, assisti ao seminário do colega **Rondinelle Marcolino Batista**, do nosso Programa de Pós-Graduação em Matemática. Foi ali, ouvindo alguém do corredor ao lado falar de massa positiva e da conjectura de Penrose com a naturalidade de quem trabalha nisso há anos, que o assunto deixou de ser leitura de fim de semana e despertou em mim uma curiosidade que não passou mais.

Rondinelle e **Levi Lopes de Lima** (UFC) publicaram na *Proceedings of the American Mathematical Society* o artigo *A harmonic level set proof of a positive mass theorem*. A técnica, introduzida por Daniel Stern, é recente e bonita: a testemunha, aqui, não é uma superfície nem um espinor, mas uma **função harmônica**, e a informação geométrica é extraída dos seus **conjuntos de nível**, que folheiam a variedade. O cenário é uma variação sutil do clássico: variedades assintoticamente planas com **bordo não compacto**, modeladas no semiespaço euclidiano, para as quais Almaraz, Barbosa e de Lima introduziram o invariante de massa apropriado, $\mathfrak{m}_{(M,g)}$. O resultado é quantitativo:

$$
\mathfrak{m}_{(M,g)} \;\geq\; \frac{1}{16\pi}\int_{M_{\mathrm{ext}}}\left(\frac{|\nabla^{2}u|^{2}}{|\nabla u|} + R_g |\nabla u|\right) dV \;+\; \frac{1}{8\pi}\int_{\Sigma_{\mathrm{ext}}} H_g |\nabla u|\, dA,
$$

para uma função harmônica $u$ escolhida adequadamente na região exterior. A não negatividade da massa é imediata: se a curvatura escalar $R_g$ e a curvatura média do bordo $H_g$ são não negativas, o lado direito é soma de termos não negativos.

A estrutura é exatamente a que descrevi: à esquerda, um número que só existe **no infinito**; à direita, integrais de curvatura **no interior** e **no bordo**. Três gerações de técnicas, três testemunhas — superfície mínima, espinor, função harmônica —, um mesmo teorema.

A distância entre meu território e esse, aliás, era menor do que eu imaginava. Um campo escalar sobre um fundo de Schwarzschild obedece a uma equação de onda com potencial; separando variáveis, sobra uma **equação radial** do tipo Heun confluente. Quando dois buracos negros se fundem, o objeto resultante fica "vibrando" e se acalma emitindo ondas gravitacionais em frequências características — um estágio final que os físicos chamam de *ringdown*, por analogia com um sino que vai silenciando. Foram justamente essas ondas que o **LIGO** (*Laser Interferometer Gravitational-Wave Observatory*), o par de interferômetros gigantes instalados nos Estados Unidos, detectou pela primeira vez em setembro de 2015. E as frequências desse repicar final são, do ponto de vista matemático, os autovalores de um problema espectral não autoadjunto para aquela equação radial: os chamados **modos quase-normais**. Espalhamento, decaimento local de energia, estimativas resolventes — o mesmo vocabulário que eu já usava, aplicado a outro operador.

Nos últimos meses tenho colaborado nesse terreno com **Helder Alexander Santos e Costa**, do Programa de Pós-Graduação em Física da UFPI, num trabalho sobre ondas escalares num buraco negro de Schwarzschild com **violação da simetria de Lorentz**; em julho participei, como examinador externo, da banca de qualificação de mestrado de João Guilherme Rodrigues Valangelis sobre esse mesmo problema.

## O sonho de Einstein

Falta dizer para onde tudo isso aponta.

Einstein passou os últimos trinta anos de vida, em Princeton, atrás de uma **teoria de campo unificada**: uma única estrutura geométrica que contivesse, ao mesmo tempo, a gravitação e o eletromagnetismo — e, mais tarde, tudo o mais. Tentou métricas não simétricas, conexões com torção, dimensões extras no espírito de Theodor Kaluza (1885–1954) e Oskar Klein (1894–1977), a geometria conforme de Hermann Weyl (1885–1955). Não chegou a lugar nenhum, e a comunidade da época o considerou um homem brilhante que havia perdido o passo, teimando com o passado enquanto a mecânica quântica ganhava o mundo.

O veredito envelheceu mal. A unificação avançou de fato, só que por um caminho que Einstein não previu: entre 1961 e 1968, em trabalhos independentes, Sheldon Glashow (n. 1932), Steven Weinberg (1933–2021) e Abdus Salam (1926–1996) mostraram que o eletromagnetismo e a força nuclear fraca são a mesma força vista em regimes de energia diferentes — a primeira unificação genuína desde Maxwell, e Nobel em 1979. O Modelo Padrão juntou a esse par a força forte. Três das quatro interações fundamentais estão hoje descritas por uma mesma linguagem, a das teorias de gauge.

A quarta é a gravidade, e ela resiste. O ponto exato onde a resistência aparece é o buraco negro — que é a razão de este texto terminar aqui. A radiação de Hawking não é uma curiosidade: é o único fenômeno conhecido em que relatividade geral e mecânica quântica se pronunciam sobre o mesmo objeto e discordam. O paradoxo da informação, a entropia proporcional à área, a correspondência holográfica proposta por Juan Maldacena (n. 1968) em 1997 — tudo isso são tentativas de resolver essa discordância, e todas nasceram de horizontes de eventos. O buraco negro virou o laboratório teórico da unificação.

E é aí que a figura de Witten fecha o círculo. Sua Medalha Fields premiou exatamente o tipo de trabalho que Einstein tentava fazer em Princeton: procurar matemática nova capaz de estender a relatividade geral até uma descrição unificada das forças e das partículas. Lee Smolin (n. 1955) fez essa leitura de forma direta:

> *I would suggest that the resolution of the paradox is that Einstein's dissent from quantum mechanics and immersion in the search for a unified field theory were not failures but anticipations. After all, even if many string theorists would disagree with Einstein about the incompleteness of quantum mechanics, much of what goes on in string theory these days looks a lot like what Einstein was doing in his Princeton years.*
>
> — Lee Smolin, *The Other Einstein*, **The New York Review of Books**, 14 de junho de 2007.

Não é uma canonização retroativa: Einstein errou muito, e errou em coisas específicas que hoje sabemos identificar. Mas o *programa* — procurar a estrutura geométrica que unifique — deixou de ser excentricidade de um velho isolado e virou trabalho de rotina em institutos do mundo inteiro. Chamar aqueles trinta anos de fracasso talvez seja apenas um problema de escala de tempo.

O que me parece mais bonito nessa história é que ela é um caso raro em que a física fez a pergunta, a geometria assumiu a responsabilidade de respondê-la, e a resposta ainda não veio. A conjectura de Penrose no caso geral continua aberta. A censura cósmica permanece sem prova e sem contraexemplo, meio século depois de formulada. A gravidade continua sem se deixar quantizar. Não por falta de ideias — de Lemaître a Stern, cada geração inventou uma linguagem nova —, mas porque os problemas são, simplesmente, muito difíceis.

De Louvain em 1933, de Calcutá em 1938, de Berkeley em 1939, de Princeton nos anos 1950, até um seminário de verão em Teresina em 2026 — a linha é contínua. É bom, de vez em quando, percebê-la.

## Referências e leituras

**Fontes históricas**

- Schwarzschild, K. *Über das Gravitationsfeld eines Massenpunktes nach der Einsteinschen Theorie*. **Sitzungsberichte der Königlich Preußischen Akademie der Wissenschaften**, p. 189–196, 1916.
- Friedmann, A. *Über die Krümmung des Raumes*. **Zeitschrift für Physik**, v. 10, p. 377–386, 1922.
- Birkhoff, G. D. *Relativity and Modern Physics*. Cambridge, MA: Harvard University Press, 1923.
- Lemaître, G. *L'Univers en expansion*. **Annales de la Société Scientifique de Bruxelles**, A, v. 53, p. 51–85, 1933.
- Datt, B. *Über eine Klasse von Lösungen der Gravitationsgleichungen der Relativität*. **Zeitschrift für Physik**, v. 108, p. 314–321, 1938. Reimpresso como *Golden Oldie* em **General Relativity and Gravitation**, v. 31, p. 1619, 1999, com nota editorial de A. Krasiński.
- Oppenheimer, J. R.; Snyder, H. *On Continued Gravitational Contraction*. **Physical Review**, v. 56, p. 455–459, 1939. [DOI: 10.1103/PhysRev.56.455](https://doi.org/10.1103/PhysRev.56.455).
- Penrose, R. *Gravitational Collapse and Space-Time Singularities*. **Physical Review Letters**, v. 14, p. 57–59, 1965. [DOI: 10.1103/PhysRevLett.14.57](https://doi.org/10.1103/PhysRevLett.14.57).
- Hawking, S. W. *Gravitational Radiation from Colliding Black Holes*. **Physical Review Letters**, v. 26, p. 1344–1346, 1971. [DOI: 10.1103/PhysRevLett.26.1344](https://doi.org/10.1103/PhysRevLett.26.1344).
- Bekenstein, J. D. *Black Holes and Entropy*. **Physical Review D**, v. 7, p. 2333–2346, 1973. [DOI: 10.1103/PhysRevD.7.2333](https://doi.org/10.1103/PhysRevD.7.2333).
- Hawking, S. W. *Black hole explosions?* **Nature**, v. 248, p. 30–31, 1974. [DOI: 10.1038/248030a0](https://doi.org/10.1038/248030a0).
- Abbott, B. P. *et al.* (LIGO Scientific Collaboration and Virgo Collaboration). *Observation of Gravitational Waves from a Binary Black Hole Merger*. **Physical Review Letters**, v. 116, 061102, 2016. [DOI: 10.1103/PhysRevLett.116.061102](https://doi.org/10.1103/PhysRevLett.116.061102).

**Massa positiva, desigualdade de Penrose e método dos conjuntos de nível**

- Arnowitt, R.; Deser, S.; Misner, C. W. *The Dynamics of General Relativity*. In: WITTEN, L. (ed.). **Gravitation: An Introduction to Current Research**. New York: Wiley, 1962, p. 227–265. [arXiv:gr-qc/0405109](https://arxiv.org/abs/gr-qc/0405109).
- Lichnerowicz, A. *Spineurs harmoniques*. **Comptes Rendus de l'Académie des Sciences de Paris**, v. 257, p. 7–9, 1963.
- Schoen, R.; Yau, S.-T. *On the proof of the positive mass conjecture in general relativity*. **Communications in Mathematical Physics**, v. 65, p. 45–76, 1979. [DOI: 10.1007/BF01940959](https://doi.org/10.1007/BF01940959).
- Witten, E. *A new proof of the positive energy theorem*. **Communications in Mathematical Physics**, v. 80, p. 381–402, 1981. [DOI: 10.1007/BF01208277](https://doi.org/10.1007/BF01208277).
- Atiyah, M. *On the work of Edward Witten*. In: **Proceedings of the International Congress of Mathematicians**, Kyoto, 1990, v. 1, p. 31–35.
- Bray, H. L. *Black Holes, Geometric Flows, and the Penrose Inequality in General Relativity*. **Notices of the AMS**, v. 49, n. 10, p. 1372–1381, 2002. [PDF](https://www.ams.org/notices/200211/fea-bray.pdf).
- Almaraz, S.; Barbosa, E.; de Lima, L. L. *A positive mass theorem for asymptotically flat manifolds with a non-compact boundary*. **Communications in Analysis and Geometry**, v. 24, n. 4, p. 673–715, 2016.
- Stern, D. *Scalar curvature and harmonic maps to $S^1$*. **Journal of Differential Geometry**, v. 122, n. 2, 2022. [arXiv:1908.09754](https://arxiv.org/abs/1908.09754).
- Bray, H.; Kazaras, D.; Khuri, M.; Stern, D. *Harmonic functions and the mass of 3-dimensional asymptotically flat Riemannian manifolds*. **Journal of Geometric Analysis**, v. 32, art. 184, 2022.
- **Batista, R. M.; de Lima, L. L.** *A harmonic level set proof of a positive mass theorem*. **Proceedings of the American Mathematical Society**, v. 153, p. 1761–1770, 2025. [DOI: 10.1090/proc/17192](https://doi.org/10.1090/proc/17192) · [arXiv:2306.09097](https://arxiv.org/abs/2306.09097).

**Unificação**

- Weinberg, S. *A Model of Leptons*. **Physical Review Letters**, v. 19, p. 1264–1266, 1967. [DOI: 10.1103/PhysRevLett.19.1264](https://doi.org/10.1103/PhysRevLett.19.1264).
- Maldacena, J. *The Large N Limit of Superconformal Field Theories and Supergravity*. **Advances in Theoretical and Mathematical Physics**, v. 2, p. 231–252, 1998. [arXiv:hep-th/9711200](https://arxiv.org/abs/hep-th/9711200).
- Smolin, L. *The Other Einstein*. **The New York Review of Books**, 14 jun. 2007. [Texto](https://www.nybooks.com/articles/2007/06/14/the-other-einstein/).
- Pais, A. *Subtle is the Lord: The Science and the Life of Albert Einstein*. Oxford: Oxford University Press, 1982.

**Deste blog**

- Nascimento, A. C. [*O mar cruzado e a equação que estudei no doutorado*](https://ailtoncnascimento.github.io/miscelanea/), 25 jul. 2026.
