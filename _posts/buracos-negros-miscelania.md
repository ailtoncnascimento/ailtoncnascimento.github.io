---
title: "Buracos negros: a geometria de uma escuridão"
subtitulo: "De um padre belga a uma desigualdade ainda em aberto"
categoria: Miscelânia
autor: Ailton C. Nascimento
data: 2026-09-04
tags: [relatividade geral, geometria diferencial, buracos negros, massa positiva, conjectura de Penrose, história da matemática]
---

# Buracos negros: a geometria de uma escuridão

*De um padre belga a uma desigualdade ainda em aberto*

## 1. Uma data e duas histórias

No dia **1º de setembro de 1939**, a *Physical Review* publicou um artigo de cinco páginas
assinado por J. Robert Oppenheimer e por seu aluno Hartland Snyder, intitulado
*On Continued Gravitational Contraction* (Phys. Rev. **56**, 455–459). No mesmo dia, a
Alemanha invadiu a Polônia.

A coincidência é quase literária, e ajuda a explicar por que o artigo passou tão despercebido.
Mas não é a única razão. A relatividade geral vivia então um período de baixa: era vista como
uma teoria elegante, matematicamente pesada e experimentalmente estéril. Não havia o menor
indício observacional de que os objetos descritos naquelas cinco páginas pudessem existir. E a
conclusão do artigo — que uma estrela suficientemente massiva, ao esgotar seu combustível
termonuclear, simplesmente **continua a colapsar, sem que nada a detenha** — soava, para a
maior parte dos físicos da época, menos como uma previsão e mais como um sinal de que algum
ingrediente físico estava faltando.

Levaria quase trinta anos para que o assunto voltasse ao centro da cena. Nem Oppenheimer nem
Snyder usaram a expressão "buraco negro"; o termo só se popularizaria nos anos 1960, sobretudo
depois de John Wheeler. Até lá, esses objetos eram chamados de *estrelas congeladas* ou, com
mais cerimônia, de *objetos gravitacionalmente colapsados por completo*.

Quero usar essa data como fio para puxar uma história que me interessa cada vez mais — e que,
para minha própria surpresa, começou a se cruzar com o que faço. É uma história em que a
física propõe as perguntas, e a **geometria diferencial** e a **análise** acabam sendo as
disciplinas encarregadas de respondê-las. Ela passa por um padre católico belga, por um
matemático indiano esquecido, por um físico que ganhou a Medalha Fields, e termina em dois
problemas dos quais um está resolvido pela metade e o outro continua aberto — problemas nos
quais um colega meu do PPGMat trabalha há anos.

---

## 2. O padre que descongelou a singularidade

Antes de Oppenheimer, é preciso falar de **Georges Lemaître** (1894–1966), padre católico
belga, doutor pelo MIT, professor em Louvain. Lemaître é hoje lembrado como o homem que, em
1927, obteve soluções em expansão das equações de Einstein e relacionou a expansão à
velocidade de recessão das galáxias — dois anos antes de Hubble — e que em 1931 propôs a
hipótese do *átomo primitivo*, o embrião do que chamaríamos depois de Big Bang.

Menos conhecida, e mais relevante aqui, é sua contribuição de **1933**, no artigo
*L'Univers en expansion* (Ann. Soc. Sci. Bruxelles A **53**, 51–85). A métrica de
Schwarzschild, obtida em 1916,

$$
g = -\Big(1-\frac{2m}{r}\Big)\,dt^{2} + \Big(1-\frac{2m}{r}\Big)^{-1} dr^{2} + r^{2} d\Omega^{2},
$$

parece degenerar em dois lugares: em $r=0$ e em $r=2m$ (o *raio gravitacional*, ou raio de
Schwarzschild, que em unidades usuais vale $r_s = 2GM/c^2$). Durante quase duas décadas
acreditou-se que $r=2m$ marcava uma fronteira física, uma espécie de parede intransponível
onde a teoria deixava de valer.

Lemaître mostrou que não. Passando a um sistema de coordenadas comóveis com a matéria em
queda livre — as coordenadas que hoje levam seu nome — a singularidade em $r=2m$
simplesmente **desaparece**. Nas palavras dele, era uma *singularidade fictícia*: um artefato
do sistema de coordenadas, não da geometria. O que existe em $r=2m$ não é uma parede, é uma
**superfície de não-retorno**. A distinção entre singularidade de coordenadas e singularidade
genuína de curvatura — banal para qualquer geômetra hoje — foi, naquele momento, uma
libertação conceitual.

Há aqui uma lição metodológica que vale para além do assunto: **um obstáculo pode ser um
artefato da linguagem em que o problema foi escrito**. Trocar a carta de coordenadas, mudar o
espaço funcional, reescolher a norma — boa parte do que fazemos em equações dispersivas é
exatamente isso. A singularidade de Schwarzschild em $r=2m$ é o exemplo histórico canônico.

---

## 3. Oppenheimer, Snyder — e Datt

Com a fronteira desmistificada, a pergunta seguinte é dinâmica: o que acontece de fato com
uma estrela que colapsa?

O modelo de Oppenheimer e Snyder é uma idealização deliberadamente brutal: uma esfera de
**poeira**, isto é, matéria sem pressão, homogênea, colapsando sob a própria gravidade. Fora
dela, pelo teorema de Birkhoff, a geometria é necessariamente a de Schwarzschild. Dentro, é um
pedaço de universo de Friedmann em contração. As duas peças se colam ao longo da superfície da
estrela, e o problema fica completamente solúvel.

O resultado tem uma estrutura dupla que é, a meu ver, o coração da coisa:

- Para um observador **comóvel com a matéria** — alguém caindo junto com a estrela — o colapso
  é um processo de duração **finita**. O tempo próprio até o centro é finito e, para massas
  estelares típicas, da ordem de **um dia**.
- Para um observador **externo**, distante e estático, o colapso **nunca termina**. A superfície
  da estrela aproxima-se assintoticamente do raio gravitacional; a luz que dela escapa é cada vez
  mais desviada para o vermelho, e o cone de ângulos por onde os fótons ainda conseguem fugir
  se estreita progressivamente. A estrela não explode nem desaparece com um estalo: ela
  *apaga*, exponencialmente.

Nenhum dos dois observadores está errado. É uma das declarações mais limpas da relatividade
geral: **o tempo não é um pano de fundo comum, e "o que acontece" depende de quem pergunta.**

E aqui entra um capítulo que costuma ficar de fora das versões apressadas. Um ano antes,
em **1938**, o físico indiano **Bhaktibhusan Datt**, do Presidency College de Calcutá,
publicou na *Zeitschrift für Physik* (**108**, 314) um artigo — *Über eine Klasse von Lösungen
der Gravitationsgleichungen der Relativität* — contendo uma classe de soluções de colapso
mais geral, da qual o caso de Oppenheimer–Snyder é essencialmente um subcaso. O trabalho de
Datt permaneceu obscuro por décadas. Ele morreu jovem, poucos anos depois. Sua biografia só
foi reconstruída muito mais tarde, e o artigo acabou reimpresso em **1999** na série
*Golden Oldies* da *General Relativity and Gravitation*, com nota editorial de Andrzej
Krasiński. Por isso o modelo é hoje às vezes chamado de **Oppenheimer–Snyder–Datt (OSD)**,
embora "Oppenheimer–Snyder" continue de longe o nome mais usado.

Freeman Dyson chamaria depois o artigo de 1939 de "a única e verdadeiramente revolucionária
contribuição de Oppenheimer à ciência". O próprio Oppenheimer, segundo o relato de Abraham
Pais, não parecia concordar: perguntado sobre suas principais contribuições científicas,
apontava seus trabalhos iniciais sobre elétrons e pósitrons.

---

## 4. Penrose: quando a topologia entra em campo

O renascimento veio nos anos 1960, e veio pela via mais matemática possível.

O modelo OSD é *perfeitamente simétrico*. A objeção óbvia — e foi feita durante décadas — é
que a singularidade poderia ser um artefato dessa simetria: bastaria uma perturbação, um
pouco de rotação, uma assimetria qualquer, e a matéria "erraria" o centro e voltaria a se
expandir.

Em **1965**, **Roger Penrose** encerrou o debate com um artigo de três páginas na *Physical
Review Letters* (**14**, 57), *Gravitational Collapse and Space-Time Singularities*. A ideia
central é a de **superfície aprisionada** (*trapped surface*): uma superfície fechada
bidimensional $S$ tal que **ambas** as congruências de geodésicas nulas ortogonais a $S$ —
tanto a "para fora" quanto a "para dentro" — têm expansão negativa. Isto é: mesmo a luz emitida
para fora está convergindo. Uma vez formada uma superfície assim, não há como desfazê-la.

O teorema de Penrose diz, em essência: se um espaço-tempo satisfaz uma condição de energia
razoável, possui uma superfície de Cauchy não compacta e contém uma superfície aprisionada,
então ele é **geodesicamente incompleto** — há geodésicas que simplesmente terminam. A
singularidade não é um acidente da simetria; é uma consequência estrutural.

O que torna esse resultado um marco não é apenas o enunciado, mas o **método**. Penrose não
resolveu equação nenhuma. Ele importou para a relatividade geral o arsenal da **topologia
diferencial e da geometria global**: estruturas causais, hipersuperfícies de Cauchy, técnicas
de índice, argumentos de compacidade. Foi uma mudança de linguagem tão radical quanto a de
Lemaître, e abriu a era dos teoremas de singularidade — logo generalizados por
Hawking e Penrose para o contexto cosmológico. Penrose receberia por isso metade do Prêmio
Nobel de Física de **2020**.

---

## 5. Hawking: área, temperatura, e um problema que não acabou

**Stephen Hawking** entra nessa história com um resultado de sabor puramente geométrico e uma
consequência de sabor puramente termodinâmico.

O resultado geométrico é o **teorema da área** (1971): sob condições de energia adequadas e
supondo censura cósmica, a área do horizonte de eventos **nunca decresce**,

$$
\frac{dA}{dt} \geq 0 .
$$

A semelhança formal com a segunda lei da termodinâmica é evidente demais para ser
coincidência, e Jacob Bekenstein levou-a a sério, propondo em 1972–73 que a área *é* uma
entropia. Hawking resistiu, tentou refutar, e acabou provando algo mais forte: incorporando
teoria quântica de campos ao espaço-tempo curvo, mostrou em 1974 que um buraco negro **irradia**
como um corpo negro, com temperatura

$$
T_H = \frac{\hbar c^{3}}{8\pi G M k_B},
$$

e entropia

$$
S = \frac{k_B c^{3}}{4 G \hbar}\, A = \frac{k_B A}{4 \ell_P^{2}} .
$$

Note o que essa fórmula diz: a entropia — uma medida de informação — é proporcional à **área**,
não ao volume. É daí que nasce todo o programa holográfico. E note também que a radiação de
Hawking faz o buraco negro perder massa, portanto **diminuir** a área do horizonte: o teorema
clássico da área é violado no regime quântico. Desse conflito nasceu o *paradoxo da
informação*, que continua vivo cinquenta anos depois.

Registro aqui uma coisa que me parece pouco comentada: o teorema da área é, em espírito, um
resultado de **monotonicidade sob fluxo geométrico**, exatamente o tipo de estrutura que
reencontraremos daqui a pouco na demonstração da desigualdade de Penrose.

---

## 6. Witten: o único físico com uma Medalha Fields

Em 1990, no ICM de Kyoto, a União Matemática Internacional concedeu a Medalha Fields a
**Edward Witten** — até hoje o único físico a recebê-la. No endereço escrito ao Congresso,
Michael Atiyah escreveu:

> *Although he is definitely a physicist (as his list of publications clearly shows) his
> command of mathematics is rivaled by few mathematicians, and his ability to interpret
> physical ideas in mathematical form is quite unique. Time and again he has surprised the
> mathematical community by a brilliant application of physical insight leading to new and
> deep mathematical theorems ... He has made a profound impact on contemporary mathematics.
> In his hands physics is once again providing a rich source of inspiration and insight in
> mathematics.*

A citação costuma ser lembrada por causa dos invariantes de Donaldson, da teoria de
Chern–Simons e do polinômio de Jones, da teoria quântica de campos topológica. Mas há um item
nessa lista que interessa diretamente a esta história, e é onde a narrativa dobra da física
para a matemática pura: em **1981**, Witten deu uma demonstração espinorial do **teorema da
massa positiva** (Comm. Math. Phys. **80**, 381–402).

Para entender por que isso importa, precisamos enunciar o problema.

---

## 7. Massa: um número que vive no infinito

Considere uma variedade riemanniana tridimensional $(M,g)$ **assintoticamente plana**: fora de
um compacto, ela é difeomorfa ao complementar de uma bola em $\mathbb{R}^3$, e nessa carta os
coeficientes da métrica se aproximam dos coeficientes euclidianos a uma taxa controlada,

$$
|g_{ij}(x) - \delta_{ij}| + r\,|g_{ij,k}(x)| + r^{2}|g_{ij,kl}(x)| = O(r^{-\tau}), \qquad \tau > \tfrac{1}{2}.
$$

Fisicamente, $(M,g)$ é um **dado inicial** (no caso simétrico no tempo) para um sistema
gravitacional isolado. A construção ADM — Arnowitt, Deser, Misner — associa a essa geometria um
invariante assintótico, a **massa ADM**:

$$
m_{ADM}(M,g) \;=\; \lim_{r\to+\infty}\frac{1}{16\pi}\int_{S^{2}_{r}} \big(g_{ij,j}-g_{jj,i}\big)\,\mu^{i}\, dS^{2}_{r},
$$

onde $\mu$ é o campo normal unitário exterior às esferas coordenadas grandes $S^2_r$ e usamos a
convenção de soma de Einstein. Sob hipóteses razoáveis de decaimento dos campos de matéria,
esse número é conservado ao longo da evolução temporal dos dados iniciais, e portanto é um
invariante fundamental do sistema.

O **teorema da massa positiva** (PMT) afirma que, sob uma condição de energia dominante — no
caso simétrico no tempo, simplesmente **curvatura escalar não negativa**, $R_g \geq 0$ — vale

$$
m_{ADM}(M,g) \;\geq\; 0,
$$

com igualdade **se e somente se** $(M,g)$ é isométrica ao espaço euclidiano $(\mathbb{R}^3,\delta)$.

O enunciado parece inofensivo. A dificuldade está numa assimetria de natureza: a massa ADM é
uma **integral de fluxo no infinito espacial**, cujo integrando não guarda nenhuma relação
algébrica direta com a curvatura escalar, que é a densidade de energia relevante. Provar o
teorema exige, portanto, construir um **objeto global** que faça a mediação entre a 1-forma
$\omega_i = g_{ij,j}-g_{jj,i}$ no infinito e a curvatura escalar no interior.

As duas primeiras soluções escolheram objetos globais diferentes:

- **Schoen e Yau (1979)** usaram **superfícies mínimas**. Supondo $m<0$, constroem-se
  superfícies mínimas estáveis completas que a fórmula da segunda variação, combinada com
  $R_g\ge 0$ e Gauss–Bonnet, proíbe de existir. Contradição.
- **Witten (1981)** usou **espinores harmônicos**. Resolvendo a equação de Dirac com condição
  assintótica constante e aplicando a fórmula de Lichnerowicz–Weitzenböck, a massa aparece como
  uma integral manifestamente não negativa. É mais curto e mais transparente — ao custo de
  exigir que a variedade seja **spin**.

O argumento de Witten é, para mim, o exemplo perfeito da observação de Atiyah: uma ideia
inteiramente física (supergravidade, energia como norma de um espinor) que se converte em um
teorema de geometria riemanniana global.

---

## 8. A conjectura de Penrose: a desigualdade que ainda resiste

Se a massa é não negativa, quanto ela vale *no mínimo* quando o sistema já contém um buraco
negro?

Penrose respondeu com um argumento heurístico admirável, que é essencialmente um teste de
consistência da relatividade geral consigo mesma. Suponha um dado inicial contendo um horizonte
aparente de área $A$. Evolua no tempo. Pela **censura cósmica**, o sistema deve relaxar
assintoticamente para um buraco negro de Kerr, de massa $m_{\text{fin}}$. Para Kerr vale
$m_{\text{fin}} \geq \sqrt{A_{\text{fin}}/16\pi}$. Pelo **teorema da área** de Hawking,
$A_{\text{fin}} \geq A$. E como a energia só pode ser irradiada para fora,
$m_{ADM} \geq m_{\text{fin}}$. Encadeando:

$$
\boxed{\;m_{ADM} \;\geq\; \sqrt{\frac{A}{16\pi}}\;}
$$

Note a lógica: essa desigualdade é uma **consequência** da censura cósmica. Logo, um
contraexemplo geométrico à desigualdade seria um contraexemplo à censura cósmica — que é,
provavelmente, o maior problema em aberto da relatividade geral matemática. É por isso que a
comunidade a leva tão a sério: ela é um teste falseável de uma conjectura que ninguém sabe como
atacar diretamente.

O estado da arte, resumido honestamente:

- **Caso riemanniano** (dado inicial simétrico no tempo, $A$ a área do bordo mínimo mais
  externo), em dimensão 3: **provado**. Huisken e Ilmanen (2001) obtiveram a desigualdade para
  a maior componente conexa do horizonte, via **fluxo de curvatura média inversa fraco**; Bray
  (2001), com um **fluxo conforme** engenhoso, obteve a versão com a área total, permitindo
  múltiplas componentes. Bray e Lee (2009) estenderam para dimensões $\le 7$.
- **Caso geral (espaço-temporal)**, sem simetria no tempo: **em aberto**. É o coração da
  conjectura, e continua sem demonstração.

Vale sublinhar a ordem lógica: a demonstração de Bray *usa* o teorema da massa positiva. Massa
positiva é o degrau; a desigualdade de Penrose é o andar seguinte. E o andar acima ainda não
tem escada.

---

## 9. Conjuntos de nível harmônicos — e um colega de corredor

Aqui a história chega perto de casa.

Em 2022, **Daniel Stern** introduziu um método novo para relacionar curvatura escalar e
topologia: em vez de superfícies mínimas ou espinores, usar os **conjuntos de nível de funções
harmônicas**. A ideia é elegante: se $u$ é harmônica, seus conjuntos de nível $\Sigma_t =
u^{-1}(t)$ formam uma folheação (fora dos pontos críticos), e a fórmula de Bochner combinada
com Gauss–Bonnet em cada folha produz identidades integrais que controlam $\int R_g$.

Logo em seguida, **Bray, Kazaras, Khuri e Stern** aplicaram o método ao teorema da massa
positiva, obtendo uma demonstração — e, mais do que isso, uma **cota inferior explícita** para
a massa. A estrutura do argumento guarda um parentesco genuíno com Schoen–Yau e com Witten:
as funções harmônicas e seus conjuntos de nível ocupam o papel que antes cabia às superfícies
mínimas.

Foi nesse terreno que **Rondinelle Marcolino Batista**, colega do Programa de Pós-Graduação em
Matemática da UFPI, e **Levi Lopes de Lima** (UFC) publicaram, na *Proceedings of the American
Mathematical Society* **153** (2025), 1761–1770, o artigo *A harmonic level set proof of a
positive mass theorem* (DOI: 10.1090/proc/17192).

O cenário deles é uma variação sutil e importante do problema clássico. Em vez de variedades
assintoticamente planas sem bordo, consideram variedades 3-dimensionais assintoticamente
planas **com bordo não compacto** $\Sigma$, modeladas no semiespaço euclidiano
$\mathbb{R}^3_+ = \{x \in \mathbb{R}^3 : x_3 \geq 0\}$ — um contexto motivado por problemas de
tipo Yamabe em variedades com bordo, e no qual Almaraz, Barbosa e de Lima introduziram, em
2016, o invariante de massa apropriado:

$$
\mathfrak{m}_{(M,g)} = \lim_{r\to+\infty}\frac{1}{16\pi}\left\{ \int_{S^{2}_{r,+}} (g_{ij,j}-g_{jj,i})\,\mu^{i}\,dS^{2}_{r} \;+\; \int_{S^{1}_{r}} g_{\alpha 3}\,\vartheta^{\alpha}\, ds \right\},
$$

onde $S^2_{r,+}$ é uma semiesfera coordenada e o segundo termo é uma correção **de bordo**,
integrada ao longo do círculo $S^1_r = \partial S^2_{r,+}$ com a co-normal exterior $\vartheta$.
O teorema de massa positiva correspondente diz: se $R_g \geq 0$ em $M$ e a **curvatura média**
do bordo satisfaz $H_g \geq 0$ ao longo de $\Sigma$, então $\mathfrak{m}_{(M,g)} \geq 0$, com
igualdade apenas para o semiespaço plano.

O que Batista e de Lima fazem é dar uma nova demonstração desse teorema pelo método dos
conjuntos de nível harmônicos. O resultado principal é quantitativo:

$$
\mathfrak{m}_{(M,g)} \;\geq\; \frac{1}{16\pi}\int_{M_{\mathrm{ext}}}\left(\frac{|\nabla^{2}u|^{2}}{|\nabla u|} + R_g |\nabla u|\right) dV \;+\; \frac{1}{8\pi}\int_{\Sigma_{\mathrm{ext}}} H_g |\nabla u|\, dA,
$$

para uma função harmônica $u$ adequadamente escolhida na *região exterior* $M_{\mathrm{ext}}$
(o que sobra depois de remover a região aprisionada). A não negatividade da massa é uma
consequência imediata: sob as hipóteses $R_g\ge 0$ e $H_g \ge 0$, o lado direito é uma soma de
termos não negativos.

Chamo atenção para a estrutura da fórmula, porque ela é bonita: à esquerda, um número que só
existe **no infinito**; à direita, integrais de curvatura **no interior** e **no bordo**. A
função harmônica $u$ é exatamente o "objeto global mediador" de que falei na Seção 7 — o
mesmo papel desempenhado pelas superfícies mínimas em Schoen–Yau e pelos espinores em Witten.
Três gerações de técnicas, três escolhas diferentes de mediador, um mesmo teorema.

Os autores contam, aliás, que já existem pelo menos **cinco** demonstrações distintas desse
resultado com bordo. Isso não é redundância: em geometria, cada nova demonstração de um
teorema conhecido é sobretudo o teste de uma ferramenta nova em terreno já mapeado — e é a
ferramenta, não o teorema, que depois viaja para onde ninguém foi.

---

## 10. Uma aventura pessoal, com a devida modéstia

Confesso que, até pouco tempo atrás, eu observava tudo isso da arquibancada. Meu território é
outro: equações dispersivas, boa colocação, comportamento em tempos longos — Benjamin–Ono,
Zakharov–Kuznetsov, Kadomtsev–Petviashvili e companhia.

Só que a distância era menor do que eu imaginava. Um campo escalar propagando-se sobre um
fundo de Schwarzschild obedece a uma equação de onda com potencial; separando variáveis,
sobra uma **equação radial** que é uma EDO de coeficientes variáveis com pontos singulares
regulares no horizonte e na origem, e um ponto singular irregular no infinito. Isto é, uma
equação do tipo **Heun confluente**. Os modos quase-normais — as "frequências de decaimento"
do buraco negro, aquilo que o LIGO efetivamente escuta no *ringdown* — são um problema
espectral não autoadjunto para essa EDO. Espalhamento, decaimento local de energia, estimativas
resolventes: é o mesmo vocabulário técnico que eu já usava, aplicado a outro operador.

Nos últimos meses tenho colaborado nesse terreno com **Helder Alexander Santos e Costa**, do
Programa de Pós-Graduação em Física da UFPI. O trabalho *An analytical study on the scalar
waves scattering by a Lorentz-violating Schwarzschild black-hole* (submetido, 2026), em
coautoria com Helder, S. Wuc e J. G. R. Valangelis, estuda o espalhamento de ondas escalares
por um buraco negro de Schwarzschild **com violação da simetria de Lorentz** — uma deformação
do fundo geométrico motivada por modelos de gravidade quântica, na qual as seções de choque
de absorção e espalhamento adquirem correções calculáveis.

Em paralelo, participei em **14 de julho de 2026** da banca de qualificação de mestrado de
**João Guilherme Rodrigues Valangelis**, no PPG em Física/CCN da UFPI, com dissertação
intitulada *Estudo Analítico sobre o Espalhamento de Ondas Escalares em um Buraco Negro de
Schwarzschild com Violação da Simetria de Lorentz*, sob a presidência do professor Helder
Alexander. Sentar-se numa banca de Física como examinador externo, vindo da Matemática, é uma
experiência que recomendo: obriga a distinguir, com uma clareza que a rotina não exige, o que
é hipótese, o que é aproximação controlada e o que é convenção da área.

Tenho ainda em andamento um trabalho conectando a equação radial de Schwarzschild para um
campo escalar massivo à expansão hipergeométrica de Svartholm–Schmidt e à teoria de Heun
confluente. Uma observação que me parece valer o registro — e que só aparece quando se leva a
sério a estrutura analítica — é **negativa**: a recorrência de cinco termos que emerge
naturalmente ali **não** serve como resolvedor de modos quase-normais no estilo de Leaver. Há
duas razões independentes. Primeiro, o polinômio característico assintótico tem uma raiz
confluente quádrupla, o que elimina a separação exponencial entre os ramos de soluções da qual
o método de fração continuada depende. Segundo, as funções de base hipergeométricas impõem
analiticidade em $z=1$, tornando a condição de Thomé de radiação puramente emergente
**invisível** tanto para o método matricial de frações continuadas quanto para o determinante
espectral de Hill.

Registro isso porque resultados negativos raramente são publicados, e quase nunca são
contados. Mas eles economizam meses de quem viria depois.

---

## 11. O fio

Vale recapitular o fio, porque ele tem uma forma:

**Lemaître** mostrou que o obstáculo era de linguagem. **Oppenheimer, Snyder e Datt**
mostraram que, removido o obstáculo, o colapso não para. **Penrose** mostrou que a
singularidade não depende de simetria, e para isso trocou a análise pela topologia. **Hawking**
mostrou que a área do horizonte se comporta como entropia, e que o buraco negro é quente.
**Witten** mostrou que uma ideia física — a energia como norma de um espinor — pode ser um
teorema de geometria riemanniana, e ganhou por isso a única Medalha Fields concedida a um
físico. **Schoen, Yau, Huisken, Ilmanen, Bray, Stern, Batista, de Lima** transformaram tudo
isso em desigualdades geométricas precisas sobre variedades riemannianas, com hipóteses
verificáveis e demonstrações completas.

E depois de tudo isso, a **conjectura de Penrose no caso geral continua aberta**, e a
**censura cósmica** — a hipótese de que a natureza não expõe suas singularidades — permanece
sem prova e sem contraexemplo, meio século depois de formulada.

É isso que me parece mais fascinante nessa história: ela é um caso raro em que a física fez a
pergunta, a geometria diferencial e a análise assumiram a responsabilidade de respondê-la, e a
resposta ainda não veio. Não por falta de ideias — em cinquenta anos foram inventados fluxos
geométricos, métodos espinoriais, técnicas de superfície mínima e agora conjuntos de nível
harmônicos, cada um deixando um rastro de teoremas próprios. Mas porque o problema é,
simplesmente, muito difícil.

De Calcutá em 1938, de Louvain em 1933, de Berkeley em 1939, até um corredor do Centro de
Ciências da Natureza em Teresina em 2026 — a linha é contínua. É bom, de vez em quando,
percebê-la.

---

## Referências e leituras

**Fontes históricas**

- J. R. Oppenheimer, H. Snyder, *On Continued Gravitational Contraction*, Phys. Rev. **56** (1939), 455–459. DOI: [10.1103/PhysRev.56.455](https://doi.org/10.1103/PhysRev.56.455)
- B. Datt, *Über eine Klasse von Lösungen der Gravitationsgleichungen der Relativität*, Z. Phys. **108** (1938), 314. Reimpresso como *Golden Oldie*, Gen. Relativ. Gravit. (1999), com nota editorial de A. Krasiński.
- G. Lemaître, *L'Univers en expansion*, Ann. Soc. Sci. Bruxelles A **53** (1933), 51–85.
- R. Penrose, *Gravitational Collapse and Space-Time Singularities*, Phys. Rev. Lett. **14** (1965), 57.
- S. W. Hawking, *Black hole explosions?*, Nature **248** (1974), 30–31.

**Massa positiva e desigualdade de Penrose**

- R. Schoen, S.-T. Yau, *On the proof of the positive mass conjecture in general relativity*, Comm. Math. Phys. **65** (1979), 45–76.
- E. Witten, *A new proof of the positive energy theorem*, Comm. Math. Phys. **80** (1981), 381–402.
- G. Huisken, T. Ilmanen, *The inverse mean curvature flow and the Riemannian Penrose inequality*, J. Differential Geom. **59** (2001), 353–437.
- H. Bray, *Proof of the Riemannian Penrose inequality using the positive mass theorem*, J. Differential Geom. **59** (2001), 177–267. [projecteuclid](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-59/issue-2/Proof-of-the-Riemannian-Penrose-Inequality-Using-the-Positive-Mass/10.4310/jdg/1090349428.full)
- H. Bray, *Black Holes, Geometric Flows, and the Penrose Inequality in General Relativity*, Notices AMS (nov. 2002). [PDF](https://www.ams.org/notices/200211/fea-bray.pdf)
- D. Stern, *Scalar curvature and harmonic maps to $S^1$*, J. Differential Geom. (2022).
- H. Bray, D. Kazaras, M. Khuri, D. Stern, *Harmonic functions and the mass of 3-dimensional asymptotically flat Riemannian manifolds*, J. Geom. Anal. (2022).
- S. Almaraz, E. Barbosa, L. L. de Lima, *A positive mass theorem for asymptotically flat manifolds with a non-compact boundary*, Comm. Anal. Geom. (2016).
- **R. M. Batista, L. L. de Lima**, *A harmonic level set proof of a positive mass theorem*, Proc. Amer. Math. Soc. **153** (2025), 1761–1770. DOI: [10.1090/proc/17192](https://doi.org/10.1090/proc/17192) · [arXiv:2306.09097](https://arxiv.org/abs/2306.09097)

**Trabalhos próprios citados**

- A. C. Nascimento, H. A. S. e Costa, S. Wuc, J. G. R. Valangelis, *An analytical study on the scalar waves scattering by a Lorentz-violating Schwarzschild black-hole* (submetido, 2026).
