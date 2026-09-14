---
title: "Navier–Stokes (I): anatomia de um problema do milênio"
date: 2026-09-14 08:00:00 -0300
categories: [Miscelânea, Matemática]
tags: [Navier-Stokes, Euler, equações diferenciais parciais, mecânica dos fluidos, problemas do milênio, singularidades, blow-up, Boussinesq, IPM, inteligência artificial, OpenAI, Clay Mathematics Institute]
math: true
---

> **Primeiro de três textos.** Este é o mais técnico da série: trata do que é o problema de Navier–Stokes, de onde ele vem, e do que exatamente foi anunciado em setembro de 2026. Os dois seguintes tratarão da polêmica de prioridade entre a OpenAI e os matemáticos que chegaram primeiro, e do papel da matemática numa era em que máquinas produzem demonstrações.

Em **8 de setembro de 2026**, a OpenAI anunciou que um sistema interno de agentes havia produzido — e formalizado no assistente de provas Lean — uma demonstração de que um fluido tridimensional incompressível, inicialmente **em repouso**, pode desenvolver uma singularidade em tempo finito sob a ação de uma força externa suave. No dia anterior, Tristan Buckmaster e Levent Alpöge haviam tornado público um resultado similar, sobre as equações de Euler forçadas. Dois dias depois, o Clay Mathematics Institute publicou uma nota dizendo que compartilha do entusiasmo, que seguirá suas regras, e que **"o processo é deliberadamente sem pressa"**.

A imprensa converteu isso em "IA resolve problema de um milhão de dólares". A situação real é mais interessante e bem mais delicada. Para entendê-la é preciso saber três coisas: o que a equação diz, por que ela resiste há noventa anos, e — sobretudo — que o problema do milênio tem **quatro enunciados distintos**, e o que foi anunciado responde a dois deles, não aos dois que quase todo mundo tem em mente ao dizer "Navier–Stokes". A referência de fundo aqui é o tratado de Pierre Gilles Lemarié-Rieusset, *The Navier–Stokes Problem in the 21st Century*, hoje o mapa mais completo do território.

## De Newton a Stokes: como a equação foi escrita

A história começa com Isaac Newton (1643–1727), que primeiro aplicou suas leis da mecânica ao movimento dos fluidos. Em **1755**, Leonhard Euler (1707–1783) escreveu as equações diferenciais de um fluido *perfeito* — sem dissipação. Faltava a viscosidade, e ela chegou em duas etapas: Claude-Louis Navier (1785–1836) em **1822**, partindo de um modelo molecular hoje considerado incorreto mas que produziu o termo certo, e George Gabriel Stokes (1819–1903) em **1845**, com a dedução baseada no tensor de tensões que é a que usamos até hoje.

A dedução é, no fundo, a segunda lei de Newton para um elemento de fluido, mais a conservação da massa. Seguindo uma partícula que se move com o fluido, a aceleração é a **derivada material**

$$
\frac{D u}{D t} \;=\; \partial_t u + (u\cdot\nabla)u ,
$$

onde o primeiro termo mede a mudança da velocidade num ponto fixo e o segundo, o **transporte**: a partícula chega a um lugar onde a velocidade já era outra. É esse segundo termo, quadrático em $u$, que torna a equação não linear e está na raiz de toda a dificuldade. Igualando massa vezes aceleração às forças — gradiente de pressão, atrito viscoso, força externa — e normalizando $\rho = 1$:

$$
\partial_t u + (u\cdot\nabla)u \;=\; -\nabla p + \nu\,\Delta u + f,
\qquad
\nabla\cdot u \;=\; 0 .
$$

Vale ler cada peça com calma, porque o texto inteiro depende disso.

- $u(x,t)\in\mathbb{R}^3$ é o campo de velocidades e $p(x,t)$ a pressão.
- O termo $\nu\Delta u$ é o **atrito viscoso**: camadas vizinhas que deslizam uma sobre a outra trocam momento e tendem a igualar suas velocidades. É difusivo, e *suaviza*. Com $\nu = 0$ recuperamos Euler.
- A condição $\nabla\cdot u = 0$ é a **incompressibilidade**: o volume de qualquer porção de fluido não muda.
- A pressão não é aqui uma variável termodinâmica independente: é o **multiplicador de Lagrange** que força a incompressibilidade. Tomando o divergente da equação, obtém-se $-\Delta p = \nabla\cdot\big((u\cdot\nabla)u\big)$ — isto é, $p$ fica determinada instantaneamente por $u$ em **todo** o espaço, por uma inversão do laplaciano. Essa não localidade é uma das razões de o problema ser duro: um acontecimento aqui altera a pressão ali, sem atraso.

A competição entre o transporte não linear, que concentra energia em escalas cada vez menores, e a viscosidade, que a dissipa, é medida pelo **número de Reynolds**, batizado em homenagem a Osborne Reynolds (1842–1912). Reynolds alto significa turbulência. A pergunta matemática é se, para $\nu>0$ fixo, a não linearidade pode vencer *localmente* a viscosidade a ponto de a solução deixar de existir.

## Vorticidade: por que três dimensões não é como duas

A variável decisiva não é a velocidade, e sim a **vorticidade** $\omega = \nabla\times u$, que mede a rotação local. Tomando o rotacional da equação de Euler, a pressão desaparece — porque $\nabla\times\nabla p = 0$ — e sobra

$$
\partial_t\omega + (u\cdot\nabla)\omega \;=\; (\omega\cdot\nabla)u .
$$

À esquerda está o transporte da vorticidade pelo próprio fluido. À direita está o **estiramento de vórtices** (*vortex stretching*): um tubo de vorticidade que é esticado pelo escoamento fica mais fino e, por conservação do momento angular, gira mais rápido. É o efeito da patinadora que recolhe os braços. Esse termo é quadrático em $u$ e não tem sinal favorável — ele pode amplificar $\omega$ indefinidamente.

Em **duas dimensões**, a vorticidade é um escalar perpendicular ao plano, o termo de estiramento **desaparece identicamente**, e a equação vira transporte puro:

$$
\partial_t\omega + (u\cdot\nabla)\omega = 0 .
$$

A vorticidade é então simplesmente carregada pelo fluido, e todas as suas normas $L^p$ se conservam. Daí o teorema de Wolibner e Hölder, de **1933**: em 2D, soluções suaves existem para todo tempo. O problema, em 2D, está resolvido há quase um século.

Toda a dificuldade de 3D mora naquele termo. E o critério de **Beale–Kato–Majda** (1984) — de J. Thomas Beale, Tosio Kato (1917–1999) e Andrew Majda (1949–2021) — diz que ele é a *única* fonte possível de catástrofe: se $T_{\max}$ é o tempo máximo de existência de uma solução suave, então

$$
\int_0^{T_{\max}} \|\omega(\cdot,t)\|_{L^\infty}\, dt \;=\; \infty .
$$

Em palavras: uma solução suave só pode colapsar se a vorticidade se tornar incontrolável, e de um modo suficientemente sustentado para que essa integral divirja. Buscar uma singularidade é buscar um mecanismo que amplifique vorticidade sem limite.

## O século XX: Leray, e o abismo entre fraco e forte

Em **1934**, Jean Leray (1906–1998) publicou o trabalho que fundou o assunto. Ele provou duas coisas de naturezas opostas.

Primeiro: para todo dado inicial suave de energia finita existe uma solução **suave e única** num intervalo de tempo $[0,T)$, com $T$ dependendo do dado. Isso é a *boa colocação local*, e é o que se espera de uma equação de evolução decente.

Segundo — e é aqui que o problema nasce: para todo dado inicial em $L^2$ existe uma **solução fraca global**, definida para todo tempo, satisfazendo a equação apenas no sentido das distribuições e obedecendo à desigualdade de energia. A identidade de energia, que é a estimativa *a priori* fundamental, lê-se

$$
\frac{1}{2}\frac{d}{dt}\int_{\mathbb{R}^3} |u|^2\,dx \;=\; -\,\nu\int_{\mathbb{R}^3}|\nabla u|^2\,dx \;+\; \int_{\mathbb{R}^3} u\cdot f\,dx .
$$

Sem força externa, a energia cinética só decresce. Parece uma boa notícia. O problema é que ela **não é suficiente**, e a razão é de escala.

As equações são invariantes pelo reescalamento

$$
u_\lambda(x,t) = \lambda\, u(\lambda x,\lambda^2 t),
\qquad
p_\lambda(x,t) = \lambda^2 p(\lambda x, \lambda^2 t),
$$

que preserva soluções. Sob ele, a norma da energia se comporta como $\lVert u_\lambda\rVert_{L^2} = \lambda^{-1/2}\lVert u\rVert_{L^2}$: ao ampliar os pequenos detalhes, ela **diminui**. Diz-se que a energia é *supercrítica* em 3D. Concretamente: a única quantidade que sabemos controlar globalmente é cega justamente para as escalas pequenas onde uma singularidade se formaria. Em 2D, o mesmo cálculo dá invariância exata — e o problema é resolvido. A diferença entre um problema do milênio e um exercício de doutorado é um expoente.

Setenta anos de trabalho não fecharam essa lacuna, mas a mapearam com precisão. Eberhard Hopf (1902–1983) estendeu Leray a domínios limitados em 1951. Olga Ladyzhenskaya (1922–2004), Giovanni Prodi e James Serrin deram critérios de regularidade **condicional**: se a solução pertence a $L^p_t L^q_x$ com $\tfrac{2}{p}+\tfrac{3}{q}\le 1$, ela é suave. E Caffarelli, Kohn e Nirenberg provaram em **1982** um teorema de regularidade parcial: o conjunto singular de uma solução fraca adequada tem **medida de Hausdorff parabólica unidimensional nula**.

Vale abrir o termo, porque ele é mais informativo do que parece. A medida de Hausdorff usual mede um conjunto cobrindo-o por bolas pequenas e somando potências dos raios: com o expoente $1$, mede-se comprimento. Aqui, porém, o conjunto vive no espaço-tempo, e o reescalamento natural das equações não trata espaço e tempo do mesmo jeito — $x$ escala como $\lambda$ e $t$ como $\lambda^2$. Por isso a cobertura não é feita por bolas, mas por **cilindros parabólicos**

$$
Q_r(x,t) \;=\; B_r(x)\times(t-r^2,\,t),
$$

e a soma é dos raios $r$ elevados a $1$. Dizer que essa medida é **nula** é dizer que o conjunto onde a solução pode falhar é menor do que uma curva no espaço-tempo: não cabe nele nenhum filamento de singularidades, nenhuma linha de pontos ruins persistindo no tempo. Uma eventual singularidade teria de ser um evento muito esparso, quase pontual. O teorema não exclui que exista — só limita drasticamente o tamanho do estrago.

São todos resultados condicionais ou parciais: nenhum decide a questão.

Em 2016, Terence Tao (n. 1975) deu o argumento que melhor explica por que nada disso basta, e ele merece ser contado com algum cuidado, porque é o pano de fundo de tudo o que veio depois.

Escreva a equação na forma abstrata $\partial_t u = \nu\Delta u + B(u,u)$, onde $B$ é o termo bilinear que reúne o transporte e a projeção que elimina a pressão. Tao substituiu $B$ por um operador $\tilde{B}$ **com média**: grosso modo, uma superposição de cópias de $B$ compostas com multiplicadores de Fourier que reembaralham as interações entre frequências. A escolha é feita de modo a preservar tudo aquilo que a teoria clássica sabe usar — a mesma simetria de escala, o mesmo cancelamento $\langle \tilde{B}(u,u),u\rangle = 0$ e, portanto, a **mesma identidade de energia**, e as mesmas estimativas nos mesmos espaços funcionais. Do ponto de vista de qualquer argumento que conheça apenas energia e escala, $\tilde{B}$ e $B$ são indistinguíveis.

E então Tao construiu, dentro dessa equação com média, o análogo abstrato de uma máquina autorreplicante: um estado que transfere quase toda a sua energia para uma cópia de si mesmo, operando numa escala espacial menor por um fator fixo, gastando para isso uma fração fixa do tempo que ainda resta. Repetindo o processo, os tempos de cada geração formam uma série geométrica convergente — e, na soma, a solução explode em tempo finito.

A conclusão é metodológica e é dura. **Nenhuma demonstração de regularidade global que se apoie apenas na identidade de energia e na estrutura de escala pode funcionar**, porque existe um objeto que satisfaz as duas coisas e explode. Quem quiser provar (A) ou (B) terá de usar alguma propriedade específica da não linearidade de Navier–Stokes que a versão com média não compartilha — algum cancelamento, alguma estrutura geométrica fina que ninguém identificou até hoje. É o que se chama de **barreira de supercriticidade**, e é a razão pela qual noventa anos de análise funcional refinada não produziram uma resposta.

## Os quatro enunciados de Clay

Em 2000, o Clay Mathematics Institute incluiu Navier–Stokes entre os sete Problemas do Milênio, com o enunciado oficial redigido por Charles Fefferman (n. 1949). É indispensável saber que esse enunciado não é uma pergunta, mas **quatro**, e que basta provar uma delas.

Seja $\nu>0$, $n=3$, e $u^\circ$ um dado inicial suave, de divergente nulo e com decaimento rápido.

- **(A)** Em $\mathbb{R}^3$, **sem força** ($f\equiv 0$): provar que existe solução suave, de energia limitada, para todo tempo.
- **(B)** O mesmo no toro $\mathbb{R}^3/\mathbb{Z}^3$, isto é, com condições periódicas, e ainda **sem força**.
- **(C)** Em $\mathbb{R}^3$, exibir um dado inicial suave $u^\circ$ **e uma força externa suave** $f$, ambos com o decaimento exigido, para os quais **não exista** solução fisicamente razoável — ou seja, demonstrar o colapso.
- **(D)** O mesmo no toro.

A assimetria é a chave de tudo o que se seguiu. Os enunciados (A) e (B) proíbem a força externa; (C) e (D) a permitem — e Fefferman foi explícito quanto ao motivo: incluí-los era **dar margem razoável a quem tentasse resolver**. A intenção era generosa; o efeito, vinte e seis anos depois, foi criar uma porta lateral. Provar (C) satisfaz a letra do problema, mas não satisfaz, para a maior parte da comunidade, o espírito: quando um físico ou um matemático diz "o problema de Navier–Stokes", está falando de (A) e (B) — de um fluido que, deixado em paz, se desorganiza sozinho. Guarde essa distinção; ela é o eixo do que vem a seguir.

## Os laboratórios: IPM, Boussinesq e Euler

Atacar Navier–Stokes 3D de frente não funcionou. A estratégia que produziu resultados nos últimos dez anos foi outra: trabalhar em **modelos reduzidos** que retêm o mecanismo suspeito de gerar a singularidade e descartam o resto. Três deles são os laboratórios padrão.

**A equação do meio poroso incompressível (IPM).** Substitui a lei de Newton pela **lei de Darcy** — de Henri Darcy (1803–1858), o engenheiro que estudou as fontes de Dijon —, válida para um fluido que percola lentamente por um meio poroso, onde o atrito com a matriz sólida domina a inércia. A velocidade passa a ser proporcional à força motriz, não à sua integral no tempo:

$$
u = -\big(\nabla p + \rho\, e_3\big),
\qquad
\partial_t \rho + u\cdot\nabla\rho = 0,
\qquad
\nabla\cdot u = 0 .
$$

Aqui $\rho$ é a densidade, transportada pelo fluido, e $\rho\,e_3$ é a gravidade. É o modelo de aquíferos, de reservatórios de petróleo, de infiltração — e o cenário natural da **instabilidade de Rayleigh–Taylor**, quando um fluido denso repousa sobre um leve e qualquer perturbação dispara a mistura.

**A equação de Boussinesq 2D.** Deve o nome a Joseph Boussinesq (1842–1929) e descreve um fluido em que as variações de densidade são pequenas o bastante para serem ignoradas na inércia, mas não na flutuação:

$$
\partial_t u + (u\cdot\nabla)u = -\nabla p + \theta\, e_2,
\qquad
\partial_t \theta + (u\cdot\nabla)\theta = 0,
\qquad
\nabla\cdot u = 0 ,
$$

com $\theta$ a temperatura (ou o desvio de densidade). É o modelo básico de convecção térmica — de uma panela no fogo à circulação atmosférica. E tem uma propriedade que a torna preciosa: fora do eixo de simetria, a equação de Boussinesq em 2D é **formalmente idêntica** à equação de Euler 3D axissimétrica sem giro, com $\theta$ no papel do giro. Um problema bidimensional que carrega a dificuldade de um tridimensional.

**Euler 3D incompressível.** É Navier–Stokes com $\nu = 0$: o fluido perfeito, sem atrito, com o estiramento de vórtices atuando sem nenhum freio dissipativo. Se nem aqui houvesse singularidades, a esperança de encontrá-las com viscosidade seria mínima.

A cadeia é clara: IPM é o mais dócil, Boussinesq o intermediário, Euler o degrau imediatamente abaixo de Navier–Stokes. Quem constrói uma explosão nos três tem, plausivelmente, um método.

## Duas estratégias para explodir um fluido

Diego Córdoba e Luis Martínez Zoroa, do ICMAT em Madri, publicaram em janeiro de 2026 um panorama do campo que identifica **dois mecanismos** e cinco grupos ativos.

O primeiro é a **autossemelhança**. Procura-se uma solução que, perto do colapso, é sempre igual a si mesma a menos de um reescalamento: a mesma forma, cada vez menor e mais rápida. Reduz-se assim uma EDP de evolução a uma equação de perfil, estacionária. É o caminho de Thomas Hou e Jiajie Chen, com provas assistidas por computador a partir de simulações de altíssima precisão; de Tristan Buckmaster e Javier Gómez-Serrano, que usam redes neuronais para achar os perfis; e de Tarek Elgindi, que em **2021** obteve, sem assistência computacional, uma singularidade autossemelhante para Euler 3D axissimétrico sem giro em espaços de Hölder $C^{1,\alpha}$ — marco histórico, mas ainda longe do $C^\infty$ exigido por Clay.

O segundo é a **cascata de camadas de vorticidade**, desenvolvido no ICMAT a partir da tese de Martínez Zoroa. Em vez de uma forma que se repete, constrói-se uma sequência infinita de camadas $\omega_n$ de suporte compacto, cada vez menores, acumulando-se no ponto singular, escolhidas de modo que as autointerações se cancelem a ordem zero e que cada camada **alimente** a seguinte. A dinâmica se reduz a um sistema infinito de EDOs do tipo

$$
\dot{x}_n \;=\; x_n\,(x_0+\cdots+x_{n-1}) \;+\; \text{Erro},
$$

onde $x_n$ é a amplitude da $n$-ésima camada. É um método de papel e lápis, e foi ele que produziu os avanços decisivos: singularidades não autossemelhantes para Euler 3D sem força em $C^\infty(\mathbb{R}^3\setminus\{0\})\cap C^{1,\beta}\cap L^2$ (Córdoba, Martínez Zoroa e Fan Zheng, *Annals of PDE*, 2025), blow-up para IPM com fonte suave, e — o mais próximo do alvo — blow-up em tempo finito para Navier–Stokes **hipodissipativo**, com viscosidade fracionária $\lvert\nabla\rvert^{\alpha}$, e força em $L^1_t C_x^{1,\varepsilon}\cap L^\infty_t L^2_x$.

Note o padrão: em cada um desses resultados, o que falta para satisfazer Clay é a **regularidade da força**. Consegue-se $C^{1,\alpha}$, consegue-se $C^{1,\varepsilon}$ integrável no tempo — mas não $C^\infty$. Era essa a última trincheira.

## Setembro de 2026

Ela caiu duas vezes em dois dias.

Em **7 de setembro**, Levent Alpöge e Tristan Buckmaster tornaram público — e Terence Tao comentou no mesmo dia [em seu blog](https://terrytao.wordpress.com/2026/09/07/finite-time-blowup-with-smooth-forcing-term-for-the-incompressible-porous-medium-boussinesq-and-incompressible-euler-equations/) — um resultado que, nas palavras dele, se constrói "sobre o trabalho prévio de Córdoba e Martínez-Zoroa": **blow-up em tempo finito com termo de forçamento suave** para as três equações modelo, IPM, Boussinesq 2D e Euler 3D incompressível. A estratégia é iterativa: adicionam-se repetidamente correções de alta frequência a uma solução forçada anterior, explorando instabilidades linearizadas em torno de um escoamento de fundo cuidadosamente desenhado, mantendo a força suave a cada passo. O trabalho foi verificado em Lean.

Em **8 de setembro**, a OpenAI anunciou o passo seguinte: o mesmo fenômeno para **Navier–Stokes**, com viscosidade genuína. O enunciado reivindicado é o seguinte.

**Teorema (OpenAI, setembro de 2026).** *Para todo $\nu>0$ existem uma força suave de suporte compacto $f\in C_c^\infty(\mathbb{R}^3\times(0,\infty);\mathbb{R}^3)$, um compacto $K\subset\mathbb{R}^3$ e campos suaves $u$, $p$ em $\mathbb{R}^3\times[0,1)$, com $\nabla\cdot u = 0$, satisfazendo*

$$
\partial_t u + (u\cdot\nabla)u - \nu\Delta u + \nabla p = f,
\qquad
u(\cdot,0)=0,
$$

*com suporte contido em $K$ para todo $t<1$, tais que*

$$
\sup_{0\le t<1}\|u(t)\|_{L^2(\mathbb{R}^3)} < \infty,
\qquad
\limsup_{t\uparrow 1}\ \|u(t)\|_{L^\infty(\mathbb{R}^3)} = \infty .
$$

Energia cinética limitada, velocidade ilimitada, a partir do repouso. Isso resolve, se correto, os enunciados **(C)** e **(D)**.

Vale descrever o escoamento, porque ele é geometricamente compreensível. A construção vive em coordenadas cilíndricas $(r,\theta,z)$ em torno de um eixo vertical, e a parte principal é axissimétrica **com giro**. No plano horizontal, o fluido converge para o eixo ($u_r<0$) enquanto circula em torno dele; como o momento angular $r\,u_\theta$ é aproximadamente conservado ao longo de cada trajetória, a velocidade de giro dispara à medida que a partícula se aproxima — de novo a patinadora — e o caminho de cada partícula é uma espiral que se fecha. Como fluido incompressível não pode se acumular no eixo, ele escapa ao longo dele: dois jatos opostos, para cima e para baixo do plano médio, alimentados pela mesma espiral convergente. Escrevendo $\tau = 1-t$ para o tempo restante, o núcleo colapsa de modo autossemelhante,

$$
\ell_r \sim \tau^{1/2},
\qquad
\ell_z \sim \tau^{1/2-h},
\qquad
|u_\theta|,\,|u_z| \sim \tau^{-1/2-h},
$$

com $h$ pequeno e fixo. O núcleo vira uma coluna cada vez mais fina e alongada — a OpenAI descreveu a estrutura como um espaguete —, e a energia cinética nele escala como $\tau^{1/2-3h}\to 0$: o volume da região veloz encolhe mais rápido do que a velocidade cresce, o que é exatamente o que permite explodir em $L^\infty$ mantendo $L^2$ limitada. A singularidade é um ponto único, $r=z=0$, no instante $t=1$; em qualquer outro lugar, e para qualquer $t<1$, o escoamento é perfeitamente suave.

![Visualização do vórtice construído na demonstração da OpenAI: linhas de corrente helicoidais convergindo para um eixo vertical, com o núcleo alongando-se numa coluna fina](/assets/img/posts/navier-stokes-vortice-openai.webp){: width="900" height="1000" }
_A solução da OpenAI é um vórtice, visualizado aqui, em que o amarelo representa velocidade de rotação mais alta e o azul, mais baixa. Imagem: [OpenAI](https://openai.com/index/navier-stokes-solution/)._

Vale contrastar essa imagem com o estado de espírito da área até bem pouco tempo atrás. Como resumiu Diego Córdoba à *Quanta Magazine*: *"Dez anos atrás, ninguém acreditava que houvesse uma singularidade para Navier–Stokes"* — embora muitos já acreditassem que as equações de Euler admitissem uma.

E a força? Aqui está o truque estrutural, e ele merece ser entendido porque é também o motivo da desconfiança. A construção **não** parte de uma força e resolve para o escoamento. Faz o inverso: escolhido qualquer par incompressível $(u,p)$, define-se

$$
f \;:=\; \mathcal{R}(u,p) \;=\; \partial_t u + (u\cdot\nabla)u - \nu\Delta u + \nabla p ,
$$

e a equação forçada passa a valer **por construção**. Toda a dificuldade técnica se transfere para um único ponto: escolher $(u,p)$ com a singularidade desejada de modo que esse resíduo $f$ seja suave e de suporte compacto — apesar de cada parcela isolada (aceleração, gradiente de pressão, termo viscoso) explodir por conta própria. A demonstração organiza esses termos para que se cancelem a toda ordem quando $t\to 1$, deixando um resto suave. Fisicamente, esse resto tem duas peças: **pulsos breves e localizados** num fino anel cilíndrico em torno do núcleo, cada um semeado por um empurrão exponencialmente pequeno e depois amplificado pelo cisalhamento do próprio vórtice — como empurrar um balanço no instante certo — até ser amortecido pela viscosidade; e um corte suave a um raio fixo, cuja única função é manter tudo com suporte compacto. Os pulsos disparam a raios cada vez menores e em tempos cada vez mais curtos, espelhando o colapso, e ainda assim toda derivada espaço-temporal da força se estende continuamente a $t=1$, onde a força fica **plana**.

## O que continua aberto

Três qualificações, e nenhuma delas é detalhe.

**Primeira: os enunciados (A) e (B) continuam completamente abertos.** A força não é um adereço técnico da construção — é o motor. É ela que fornece o fluxo de momento adicional, nos instantes e nas escalas exatas, que os pulsos autoamplificados precisam para vencer a viscosidade e o amortecimento não linear do próprio escoamento. Retirada a força, não há demonstração, e tampouco uma rota aceita para uma. A pergunta que a maioria das pessoas tem em mente ao dizer "o problema de Navier–Stokes" — um fluido que, sozinho, se rompe — segue exatamente onde estava.

**Segunda: nada disso passou por arbitragem.** O resultado é um *preprint* acompanhado de formalização em Lean. A formalização é uma garantia forte de que a cadeia lógica fecha — elimina de saída a classe de erro que mais atormenta demonstrações longas em EDP. Mas ela verifica o teorema **tal como enunciado**, e não responde às perguntas que um árbitro humano faria: se as definições capturam o objeto pretendido, se as hipóteses são as de Clay, se o resultado significa o que se diz que significa.

**Terceira: o Clay não tem pressa, e está certo.** O instituto publicou que espera "ver ondas de nova compreensão humana desencadeadas à medida que as inovações por trás deste trabalho forem analisadas e interrogadas", e acrescentou a frase que define o tom: *"o processo é deliberadamente sem pressa, mas forneceremos atualizações"*. As regras do prêmio exigem publicação, aceitação e verificação por especialistas — lentas de propósito, porque o custo de errar para cima é maior do que o de demorar.

Fica um último ponto, que é o assunto do próximo texto. O que aconteceu em setembro de 2026 não foi uma máquina resolvendo sozinha um problema que humanos não conseguiam. Foi o desfecho — contestado, e em menos de quarenta e oito horas — de um programa de pesquisa **humano**, construído ao longo de uma década em Madri, Princeton, Duke, Caltech e Nova York, sobre cascatas de vorticidade e perfis autossemelhantes. A última trincheira era a regularidade da força, e ela caiu quando dois matemáticos e uma frota de agentes de software chegaram a ela quase ao mesmo tempo, partindo do mesmo mapa.

## Referências e leituras

**Tratado de referência**

- Lemarié-Rieusset, P. G. *The Navier–Stokes Problem in the 21st Century*. Boca Raton: Chapman & Hall/CRC, 2016 (2ª ed., 2023).

**Clássicos**

- Navier, C.-L. *Mémoire sur les lois du mouvement des fluides*. **Mémoires de l'Académie des Sciences de l'Institut de France**, v. 6, p. 389–440, 1822.
- Stokes, G. G. *On the theories of the internal friction of fluids in motion*. **Transactions of the Cambridge Philosophical Society**, v. 8, p. 287–319, 1845.
- Leray, J. *Sur le mouvement d'un liquide visqueux emplissant l'espace*. **Acta Mathematica**, v. 63, p. 193–248, 1934. [DOI: 10.1007/BF02547354](https://doi.org/10.1007/BF02547354).
- Beale, J. T.; Kato, T.; Majda, A. *Remarks on the breakdown of smooth solutions for the 3-D Euler equations*. **Communications in Mathematical Physics**, v. 94, p. 61–66, 1984. [DOI: 10.1007/BF01212349](https://doi.org/10.1007/BF01212349).
- Caffarelli, L.; Kohn, R.; Nirenberg, L. *Partial regularity of suitable weak solutions of the Navier–Stokes equations*. **Communications on Pure and Applied Mathematics**, v. 35, p. 771–831, 1982. [DOI: 10.1002/cpa.3160350604](https://doi.org/10.1002/cpa.3160350604).

**O problema do milênio**

- Fefferman, C. L. *Existence and smoothness of the Navier–Stokes equation*. Official Problem Description, Clay Mathematics Institute, 2000. [PDF](https://www.claymath.org/wp-content/uploads/2022/06/navierstokes.pdf).
- Clay Mathematics Institute. [*Navier–Stokes Equation*](https://www.claymath.org/millennium/Navier-Stokes-Equation/).
- Clay Mathematics Institute. [*Navier–Stokes Announcement*](https://www.claymath.org/news/navier-stokes-announcement/), setembro de 2026.

**Singularidades: o estado da arte**

- Tao, T. *Finite time blowup for an averaged three-dimensional Navier–Stokes equation*. **Journal of the AMS**, v. 29, p. 601–674, 2016. [DOI: 10.1090/jams/838](https://doi.org/10.1090/jams/838).
- Elgindi, T. M. *Finite-time singularity formation for $C^{1,\alpha}$ solutions to the incompressible Euler equations on $\mathbb{R}^3$*. **Annals of Mathematics**, v. 194, n. 3, p. 647–727, 2021. [DOI: 10.4007/annals.2021.194.3.2](https://doi.org/10.4007/annals.2021.194.3.2).
- Córdoba, D.; Martínez Zoroa, L.; Zheng, F. *Finite time singularities to the 3D incompressible Euler equations for solutions in $C^\infty(\mathbb{R}^3\setminus\{0\})\cap C^{1,\alpha}\cap L^2$*. **Annals of PDE**, v. 11, n. 2, art. 19, 2025.
- Córdoba, D.; Martínez Zoroa, L.; Zheng, F. *Finite time blow-up for the hypodissipative Navier–Stokes equations with a force in $L^1_t C^{1,\epsilon}_x\cap L^\infty_t L^2_x$*. Preprint [arXiv:2407.06776](https://arxiv.org/abs/2407.06776).
- Córdoba, D.; Martínez Zoroa, L. *Singularidades en 3D: el desafío matemático de Euler y Navier-Stokes*. **[Revista de divulgación]**, v. III, n. 1, p. 95–108, jan. 2026.

**Setembro de 2026**

- Tao, T. [*Finite time blowup with smooth forcing term for the incompressible porous medium, Boussinesq, and incompressible Euler equations*](https://terrytao.wordpress.com/2026/09/07/finite-time-blowup-with-smooth-forcing-term-for-the-incompressible-porous-medium-boussinesq-and-incompressible-euler-equations/). *What's new*, 7 set. 2026.
- OpenAI. [*On the Navier–Stokes Millennium Prize Problem*](https://openai.com/index/navier-stokes-solution/), 8 set. 2026. Preprint: [*Finite Time Blowup for Navier–Stokes*](https://cdn.openai.com/pdf/32d9f210-8b73-45e0-91bc-82a30aef8a9a/navier-stokes.pdf).
- *AI Has Solved One of Math's \$1 Million Millennium Prize Problems*. **Quanta Magazine**, 8 set. 2026. [Link](https://www.quantamagazine.org/ai-has-solved-one-of-maths-1-million-millennium-prize-problems-20260908/).
