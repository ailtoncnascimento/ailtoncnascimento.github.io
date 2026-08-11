---
title: "A hipótese que Hilbert queria ver provada — e um avanço inesperado"
date: 2026-08-11 10:00:00 -0300
categories: [Matemática, Curiosidades]
tags: [hipótese de riemann, inteligência artificial, teoria dos números, criptografia, claude]
math: true
description: "Uma IA não resolveu o mais famoso problema em aberto da matemática. Mas, ao tentar, fez algo que talvez seja igualmente notável — e escreveu história."
---

Conta-se que perguntaram certa vez a David Hilbert, o maior matemático de sua geração, o que ele faria se pudesse, como o lendário imperador Barbarossa, adormecer e despertar séculos depois. A resposta virou uma das frases mais célebres da matemática:

> Se eu acordasse depois de ter dormido por mil anos, minha primeira pergunta seria: a hipótese de Riemann já foi provada?

A frase mede a estatura do problema. Para Hilbert, entre tudo o que a humanidade poderia descobrir num milênio, *aquela* era a questão que valia a pena atravessar o tempo para conhecer a resposta. Ele a colocou como o oitavo item de sua lista histórica de 23 problemas, apresentada no Congresso Internacional de Matemáticos de 1900, e ela segue de pé --- um dos sete **Problemas do Milênio**, com um prêmio de um milhão de dólares do Instituto Clay para quem a resolver.

Esta semana, ela voltou às manchetes por um motivo que Hilbert não poderia ter imaginado.

## O que é a hipótese de Riemann

Vou tentar explicá-la sem pressupor nada além de curiosidade.

Tudo começa com os **números primos** --- $2, 3, 5, 7, 11, \ldots$ ---, os átomos da aritmética, a partir dos quais todos os outros inteiros se constroem por multiplicação. Os primos parecem espalhados ao acaso pela reta dos números, sem padrão óbvio. Um dos grandes sonhos da matemática é entender a *ordem escondida* nessa aparente desordem.

Em 1859, Bernhard Riemann percebeu que a chave para esse mistério estava numa função de variável complexa, hoje chamada **função zeta de Riemann**, escrita $\zeta(s)$. Ela se define, para valores adequados, pela soma infinita

$$
\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s} = \frac{1}{1^s} + \frac{1}{2^s} + \frac{1}{3^s} + \cdots
$$

O elo com os primos é profundo: a maneira como essa função se anula --- os pontos onde $\zeta(s) = 0$, chamados **zeros** --- controla, com precisão espantosa, a distribuição dos números primos. Cada zero acrescenta um detalhe fino ao padrão dos primos, como um instrumento numa orquestra.

A hipótese de Riemann é uma afirmação de uma simplicidade enganosa sobre onde esses zeros moram. Descontados alguns zeros "triviais", todos os demais --- os interessantes --- teriam **exatamente a mesma parte real**, igual a $1/2$. Em linguagem geométrica: se desenharmos os zeros no plano complexo, todos eles cairiam sobre uma única reta vertical, a chamada **reta crítica**. Nem um milímetro fora.

$$
\text{Hipótese de Riemann: todo zero não trivial tem } \mathrm{Re}(s) = \tfrac{1}{2}.
$$

É só isso. E ninguém, em 167 anos, conseguiu provar --- nem encontrar um contraexemplo.

## Onde tudo começou: Euler e o problema da Basileia

Antes de Riemann, houve Euler --- e vale contar essa origem, porque ela explica por que a função zeta é tão especial.

No início do século XVIII, um enigma atormentava os melhores matemáticos da Europa, incluindo a poderosa família Bernoulli. Ficou conhecido como **problema da Basileia**: qual é o valor exato da soma dos inversos dos quadrados?

$$
1 + \frac{1}{4} + \frac{1}{9} + \frac{1}{16} + \frac{1}{25} + \cdots
$$

Sabia-se que a soma convergia para algo próximo de $1{,}64$, mas ninguém conseguia dizer *que número* era aquele. O problema resistiu por décadas. Foi **Leonhard Euler** quem, em 1735, o resolveu --- e a resposta é uma das mais belas de toda a matemática:

$$
1 + \frac{1}{4} + \frac{1}{9} + \frac{1}{16} + \cdots = \frac{\pi^2}{6}.
$$

De onde vem $\pi$, o número do círculo, numa soma que só envolve quadrados de inteiros? A aparição inesperada de $\pi$ num problema puramente aritmético foi um choque, e foi ela que tornou Euler célebre em toda a Europa.

Mas Euler foi além, e é o segundo passo que muda tudo. Ele percebeu que aquela soma era um caso particular de uma família de somas. Para cada expoente $n>1$, a série

$$
\zeta(n) = 1 + \frac{1}{2^n} + \frac{1}{3^n} + \frac{1}{4^n} + \cdots
$$

converge para um valor que depende de $n$. (Para $n=1$ ela é a série harmônica, que se sabe divergir há séculos; é preciso $n>1$ para haver soma finita.) O problema da Basileia é simplesmente o caso $\zeta(2) = \pi^2/6$.

E então veio a descoberta decisiva, por volta de 1737: Euler mostrou que essa mesma soma pode ser reescrita como um **produto infinito percorrendo todos os números primos**:

$$
\sum_{k=1}^{\infty} \frac{1}{k^n} = \prod_{p \text{ primo}} \frac{1}{1 - 1/p^n}.
$$

Pare um instante diante dessa igualdade, porque ela é uma das mais profundas já escritas. Do lado esquerdo, uma soma sobre *todos* os inteiros. Do lado direito, um produto sobre *todos* os primos. A identidade constrói uma ponte entre a aditividade dos inteiros e a estrutura multiplicativa dos primos --- e é essa ponte, a **fórmula do produto de Euler**, que faz da função zeta o instrumento supremo para estudar os números primos. Foi aqui que tudo começou.

Por mais de um século, a função foi estudada apenas para valores reais de $n$. O salto seguinte veio em 1859, quando **Bernhard Riemann** teve a ideia de permitir que a variável fosse um **número complexo** $s$, e mostrou que a função assim estendida tem uma "continuação analítica" natural a quase todo o plano complexo. É por isso que a chamamos hoje **função zeta de Riemann**. E foi olhando para essa versão complexa que Riemann conjecturou o que ninguém até hoje conseguiu decidir: que todos os seus zeros não triviais têm parte real igual a $1/2$.

## Por que é tão difícil

Poder-se-ia pensar: se acreditamos que os zeros estão todos na reta, por que não simplesmente calculá-los e verificar? O problema é que há **infinitos** zeros. Já se checou por computador os primeiros muitos trilhões deles --- todos, sem exceção, sobre a reta crítica. Mas verificar trilhões não prova nada sobre a infinidade restante. Uma única exceção, lá longe, no zero de número $10^{10^{100}}$, derrubaria tudo.

O matemático Terence Tao, uma das maiores autoridades vivas em análise, costuma descrever a hipótese de Riemann como um problema de dificuldade excepcional justamente porque nos falta uma "razão estrutural" que force os zeros a se alinharem. Temos evidência numérica esmagadora, temos analogias sedutoras com outras áreas onde afirmações parecidas *foram* provadas --- mas o mecanismo profundo, aquele que explicaria *por que* a natureza dos números insiste naquela reta, permanece fora de alcance. É o tipo de problema em que cada técnica conhecida parece chegar perto e então esbarrar num muro invisível.

Diante da impossibilidade de provar tudo, os matemáticos recuaram para uma meta mais modesta, porém concreta: se não podemos mostrar que *todos* os zeros estão na reta, quantos por cento conseguimos garantir que estão? Essa **porcentagem mínima** virou um campo de batalha próprio, avançado a duras penas ao longo de décadas.

## O muro dos 41%

Aqui a história fica interessante. Provar que uma fração dos zeros está na reta crítica é, por si só, uma conquista difícil. Em 1942, Atle Selberg mostrou que uma proporção positiva estava lá. Décadas de trabalho de gigantes da teoria analítica dos números --- Levinson, Conrey, e muitos outros --- foram empurrando esse piso para cima, lentamente. O melhor resultado incondicional consolidado situava-se em torno de **41,6%**: pouco mais de dois quintos dos zeros, comprovadamente, obedecem à hipótese.

E ali a coisa mais ou menos empacou. Mover esse número exigia combinar ferramentas técnicas cada vez mais pesadas, com ganhos cada vez menores. Alguns matemáticos chegaram a especular se $1/2$ --- metade dos zeros --- não seria uma espécie de barreira natural, difícil de ultrapassar sem uma ideia genuinamente nova.

## O que aconteceu esta semana

Em 10 de agosto de 2026, a Anthropic anunciou que havia pedido a uma versão de pesquisa ainda não lançada de seu sistema de IA, o **Claude**, que "desse uma chance real" à hipótese de Riemann.

Sejamos claros de imediato, porque é a parte mais importante e a mais distorcida nas redes: **Claude não resolveu a hipótese de Riemann.** O problema continua tão aberto quanto estava. Um prêmio de um milhão de dólares continua sem dono.

Mas, no processo de tentar e falhar, aconteceu algo notável. Em vez de produzir apenas mais uma tentativa fracassada de prova, o sistema encontrou um caminho para **melhorar substancialmente aquele piso histórico** --- elevando a porcentagem garantida de zeros na reta crítica de $41{,}6\%$ para cerca de $\mathbf{67{,}2\%}$.

Para dimensionar: um salto que o esforço humano acumulado moveu poucos pontos ao longo de décadas foi, de uma vez, empurrado para dois terços. É, segundo os relatos, o maior avanço isolado na história desse indicador específico.

E a matemática por trás não é fumaça. O caminho encontrado combina um resultado recente de Baluyot e colaboradores (2025) com um trabalho de Enrico Bombieri, de 2000, sobre uma forma quadrática associada à fórmula explícita de Weil --- uma identidade que liga os primos aos zeros da zeta. Dois matemáticos da própria Anthropic estudaram e validaram o argumento, e dois especialistas externos de renome na área, Brian Conrey e Dan Goldston, examinaram o texto. O resultado foi ainda **formalizado em Lean**, o assistente de prova que confere cada passo mecanicamente.

## O que foi realmente notável: o *como*

Se o número é a manchete, o método é a parte que merece estudo --- e é aqui que este episódio conversa diretamente com [o que venho registrando aqui neste site](/posts/matematica-na-era-da-ia/) sobre matemática na era da IA.

A abordagem foi, na palavra usada pelos próprios pesquisadores, **agêntica**. Claude não "cuspiu" uma resposta. Ele conduziu um processo de pesquisa: coordenou dezenas de subagentes trabalhando em paralelo, gerou e testou centenas de ideias (na primeira sessão, relata-se que produziu e descartou 650 abordagens, todas falhas), vasculhou a literatura, contestou os próprios argumentos, e ao final formalizou o que restou de pé. Um detalhe quase cômico, e revelador: o operador humano --- que nem era matemático --- limitou-se, em boa parte, a mandar mensagens de encorajamento, variações de "continue" e "acredite em você".

É essa a mudança de figura. Não uma máquina que responde perguntas, mas um sistema que **forma hipóteses, delega tarefas, explora possibilidades, rejeita as próprias ideias, formaliza resultados** --- e, ao cabo, contribui com algo que os humanos ainda não sabiam.

A pergunta que orienta este momento, portanto, deixou de ser apenas "a IA consegue resolver problemas científicos?". Ela passou a ser mais funda: *a IA consegue descobrir, de forma autônoma, coisas que os humanos ainda não conheciam?* Este episódio sugere que a resposta, cada vez mais, tende ao sim.

## Uma dose de honestidade

No espírito de precisão que tento manter aqui, três ressalvas que a própria Anthropic faz questão de registrar, e que a euforia das redes costuma apagar.

Primeiro, isto **não é uma prova da hipótese de Riemann**, e a companhia afirma explicitamente que não espera que a técnica usada leve a uma prova completa. É um resultado dentro de uma das questões técnicas *ao redor* da hipótese, não a hipótese em si.

Segundo, o resultado ainda **não passou pelo crivo completo da comunidade** --- a arbitragem por pares, a digestão lenta de que falava o diagrama de Tao. Foi examinado por especialistas de renome em curto prazo, o que é um bom sinal, e formalizado em Lean, o que é um sinal ainda melhor; mas a validação plena leva tempo.

Terceiro, o modelo usado é uma versão de pesquisa não identificada, sem checkpoint público, o que significa que o experimento não é hoje reproduzível de ponta a ponta por terceiros.

Nada disso diminui o feito. Apenas o coloca no seu devido lugar: um avanço matemático real e verificável dentro de um problema lendário, obtido por um processo de pesquisa em larga parte autônomo. É extraordinário sem precisar ser aquilo que não é.

## E se um dia for provada? A revolução silenciosa

Vale fechar imaginando o que estaria em jogo numa eventual prova completa --- porque a hipótese de Riemann não é uma curiosidade encerrada em si mesma. Ela é uma peça estrutural sobre a qual repousam **centenas de outros teoremas**, muitos deles começando com a frase "assumindo a hipótese de Riemann...". Prová-la validaria, de um só golpe, toda essa arquitetura condicional.

E há um fio que liga a zeta a algo bem concreto do seu dia a dia: a **criptografia**. Boa parte da segurança digital do mundo --- transações bancárias, mensagens cifradas, assinaturas eletrônicas, o cadeado do seu navegador --- apoia-se na dificuldade de fatorar números enormes em seus fatores primos. Ora, a hipótese de Riemann é, no fundo, uma afirmação profunda sobre *como os primos se distribuem*. Um entendimento realmente completo dessa distribuição poderia, em princípio, iluminar os primos de maneiras hoje inimagináveis --- e ferramentas que compreendem os primos com profundidade suficiente são exatamente as que poderiam, um dia, ameaçar ou refundar os alicerces da segurança de dados.

Convém não exagerar: provar a hipótese de Riemann não quebraria a criptografia amanhã de manhã, e a ameaça mais concreta à criptografia atual vem de outra frente (os computadores quânticos). Mas o ponto simbólico permanece: um enunciado sobre uma reta no plano complexo, formulado por pura curiosidade em 1859, está entrelaçado com a infraestrutura invisível que sustenta o mundo conectado. É a "irrazoável eficácia da matemática" em sua forma mais vertiginosa --- a poesia mais abstrata revelando-se, um século depois, a espinha dorsal da vida prática.

## Conclusão

Hilbert queria atravessar mil anos de sono para saber se a hipótese fora provada. Não precisaríamos acordá-lo ainda --- ela continua em aberto. Mas talvez lhe interessasse saber que, no verão de 2026, o caminho até ela ganhou um companheiro de viagem improvável: um sistema que não dorme, coordena sessenta versões de si mesmo, descarta seiscentas ideias antes do café, e precisa, de vez em quando, que lhe digam "acredite em você".

A montanha continua lá, com seu cume ainda inviolado. Mas subiu-se, esta semana, um trecho inesperado da encosta --- e, pela primeira vez, quem deu boa parte dos passos não foi humano.

## Referências

1. Anthropic. *Learning more about Claude's mathematical capabilities.* 10 de agosto de 2026. Disponível em: <https://www.anthropic.com/research/riemann-zeta>.
2. B. Riemann. *Über die Anzahl der Primzahlen unter einer gegebenen Grösse.* 1859.
3. D. Hilbert. Lista dos 23 problemas, Congresso Internacional de Matemáticos, Paris, 1900 (a hipótese de Riemann é o oitavo).
4. C. E. SANDIFER. *How Euler Did Even More.* Washington: The Mathematical Association of America, 2015. (Fonte do material histórico sobre o problema da Basileia e a fórmula do produto.)
5. T. Tao. Entradas sobre a hipótese de Riemann no blog *What's new*.
