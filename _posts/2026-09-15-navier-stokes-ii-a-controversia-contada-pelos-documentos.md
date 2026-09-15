---
title: "Navier–Stokes (II): a controvérsia, contada pelos documentos"
date: 2026-09-15 08:00:00 -0300
categories: [Miscelânea, Matemática]
tags: [Navier-Stokes, Buckmaster, Alpöge, Córdoba, Martínez-Zoroa, OpenAI, inteligência artificial, prioridade, ética na ciência, problemas do milênio]
math: true
---

> **Segundo de três textos.** O [primeiro](/posts/navier-stokes-i-anatomia-de-um-problema-do-milenio/) tratou do problema e do que foi efetivamente provado. Este reconstrói a disputa de prioridade de setembro de 2026 a partir dos documentos públicos — sobretudo da nota que Tristan Buckmaster publicou na página dele no Courant Institute. O terceiro tratará do que tudo isso significa para a matemática.

Há uma tentação forte, ao contar esta história, de escolher um vilão. Resisto a ela deliberadamente, e por uma razão simples: **o próprio Buckmaster resistiu**. A nota que ele publicou por volta da meia-noite de 7 de setembro de 2026 termina com um parágrafo que vale reproduzir antes de qualquer outra coisa:

> "Gostaria de ser claro sobre o que **não** estou afirmando. Não vi a demonstração da OpenAI. Não sei o que o modelo deles fez, nem como. Não sei se nossos dados foram usados. **Não estou acusando ninguém de nada.** Estou declarando o que me foi dito, quando, e o que me foi proposto."

Esse é o padrão de prova que este texto vai seguir. Nada aqui é inferência sobre intenções. É cronologia e documento.

## O que Alpöge e Buckmaster provaram — e a quem deram o crédito

A nota abre com o anúncio: Levent Alpöge e Tristan Buckmaster tornavam públicos três resultados — **blow-up em tempo finito com forçamento suave** para o meio poroso incompressível, para Boussinesq e para Euler 3D incompressível. E acrescenta um quarto, retido:

> "Acreditamos que também temos blow-up para Navier–Stokes hipodissipativo. Não estamos publicando esse artigo hoje: ao contrário dos anteriores, a verificação em Lean ainda não terminou. [...] Menciono-o porque ele sugere um caminho para o Euler **não forçado**."

O parágrafo seguinte é, a meu ver, o mais importante de todo o documento, e é o que a cobertura de imprensa quase inteiramente ignorou:

> "O programa no qual isto se insere não foi iniciado por nós, nem foi proposto por um Modelo de Linguagem. O crédito pela ideia básica desse programa é de **Diego Córdoba e Luis Martínez-Zoroa**, que há vários anos vêm explorando a construção de blow-ups forçados. Tomamos o trabalho deles como ponto de partida, usando Modelos de Linguagem para levar seu programa à conclusão."

E, algumas linhas adiante, uma frase que um matemático não escreve levianamente:

> "Deixe-me tornar explícito o que já disse em particular a colegas: à vista deste conjunto de trabalhos, **acredito que Luis Martínez-Zoroa merece uma Medalha Fields**."

Registre-se o que está acontecendo aqui. O homem cuja prioridade foi supostamente atropelada usa o primeiro terço de sua defesa pública para dizer que o mérito não é dele — é de dois colegas espanhóis do ICMAT que passaram anos construindo o método. O artigo sobre Boussinesq diz o mesmo em linguagem técnica: o trabalho "desenvolve o programa iniciado por Diego Córdoba e Luis Martínez-Zoroa, cujas construções multiescala inovadoras constituem seu principal alicerce intelectual".

Terence Tao, comentando no dia seguinte, situou a contribuição com precisão: *"A construção de Alpöge–Buckmaster tem alguns aperfeiçoamentos técnicos sobre a construção mais antiga de Córdoba–Martínez-Zoroa que lhes permitem tratar equações de fluidos mais gerais; ainda não digeri as diferenças precisas, mas as EDOs parecem ser mais instáveis e as correções de alta frequência parecem ter melhores propriedades de localização espacial."*

Aperfeiçoamentos técnicos sobre um método existente. Não um método novo. É exatamente assim que a matemática funciona, e é exatamente o que Buckmaster diz.

### O que exatamente foi melhorado

Vale ser concreto, porque a diferença é de uma linha e é toda a história.

O artigo de partida é *Blow-up for the incompressible 3D-Euler equations with uniform $C^{1,\frac12-\epsilon}\cap L^2$ force*, de Córdoba e Martínez-Zoroa, de setembro de 2023. Ali se constroem, em $\mathbb{R}^3$, soluções **não axissimétricas** das equações de Euler forçadas, na classe $C^{3,\frac12}\cap L^2$ num intervalo $[0,T)$ finito, sujeitas a uma força uniformemente em $C^{1,\frac12-\epsilon}\cap L^2$, tais que

$$
\int_0^t \lVert\nabla u(\cdot,s)\rVert_{L^\infty}\,ds \;\longrightarrow\; \infty
\qquad (t\to T),
$$

com a solução permanecendo suave em toda parte, **exceto na origem**. Duas escolhas metodológicas merecem registro: o argumento **não usa coordenadas autossemelhantes**, e ele atravessa o limiar $C^{1,\frac13+}$ que barrava as soluções axissimétricas sem giro.

Ou seja: em 2023 já existiam blow-up forçado, não axissimetria, e um mecanismo de cascata que dispensa perfis autossemelhantes. Faltava uma coisa só — **a força tinha regularidade de Hölder finita**, $C^{1,\frac12-\epsilon}$, e o enunciado de Clay exige $C^\infty$.

É esse degrau, e apenas esse, que Alpöge e Buckmaster subiram: levaram a mesma arquitetura de $C^{1,\frac12-\epsilon}$ a $C^\infty$, e de Euler para também IPM e Boussinesq. Nos termos de Tao, à custa de EDOs mais instáveis e de correções de alta frequência com localização espacial melhor. Um degrau — mas o último degrau antes da porta.

## O método de trabalho, declarado sem rodeios

A nota é também um documento notável sobre **como** se faz matemática em 2026, e Buckmaster não esconde nada:

> "Usamos vários LLMs ao longo de todo o trabalho: o Claude, da Anthropic, e o Codex, da OpenAI, especialmente com o GPT-5.6 Sol e, mais recentemente, o Astra. Este último foi usado apenas para redação e para auditar nossos argumentos."

A cronologia que ele dá é precisa. Durante quase um ano, progresso lento: leitura da literatura, melhoria de resultados preliminares, até obter blow-up com forçamento suave para o meio poroso. Então, cerca de um mês antes:

> "Em 15 de agosto obtivemos os resultados de blow-up, com forçamento suave, tanto para Boussinesq quanto para Euler. Posso dizer que a primeira demonstração gerada por LLM que o Levent me mandou foi a mais horrenda que já li; verificamos em Lean no dia 22 de agosto. Desde então, temos trabalhado sem parar para entender essa demonstração e transformá-la em algo legível."

E, com uma franqueza rara:

> "Não estou satisfeito com a qualidade de apresentação destes artigos. [...] Os textos sobre Boussinesq e Euler em particular estão muito mais perto do que os modelos produzem sob direção humana do que de um artigo escrito por uma pessoa. O texto sobre Euler, em particular, só pode ser descrito como *AI slop*. Peço desculpas por isso."

Guarde esse trecho. Ele contém, sem alarde, a tese central de toda a série: **uma demonstração verificada não é a mesma coisa que uma demonstração compreendida.** O Lean certificou a cadeia lógica em 22 de agosto. Levou mais três semanas — de trabalho humano ininterrupto — para que os autores entendessem o que a máquina tinha feito. E, pela avaliação do próprio autor, o resultado ainda não está compreendido a contento.

Buckmaster diz também o que teria preferido anunciar:

> "Eu havia planejado dizer, ao anunciar nosso trabalho, que os resultados não são o mais importante. O importante é o significado de que um matemático e um modelo possam agora fazer todo esse trabalho em um mês. [...] **Este é um momento Deep Blue–Kasparov.** A comunidade precisa ter uma discussão séria e sem pressa sobre para onde ir a partir daqui."

Em vez disso, ele passou a semana escrevendo sobre outra coisa.

## O plano de voo estava publicado

Antes da cronologia, é preciso entender uma coisa: em 7 de setembro de 2026, o caminho até Navier–Stokes **não era um mistério**. Era uma escada com os degraus numerados, visível para quem acompanhasse a literatura. Terence Tao a descreveu no mesmo dia, e a mecânica é esta.

Constrói-se a solução por **iteração**. Parte-se de um escoamento de fundo cuidadosamente desenhado e adicionam-se repetidamente **pequenas correções de alta frequência**, cada uma explorando uma instabilidade da equação linearizada em torno do que já foi construído. As amplitudes dessas correções obedecem a um sistema explícito de EDOs cujo comportamento é o do blow-up desejado — é a cascata de camadas de vorticidade descrita no [primeiro texto](/posts/navier-stokes-i-anatomia-de-um-problema-do-milenio/). O ofício todo está em escolher as frequências e as localizações de modo que os erros de interação entre camadas fiquem controlados e, sobretudo, que **o resíduo que sobra — a força — permaneça suave**.

Com essa máquina em mãos, a escada tem degraus bem definidos, e cada um deles é uma classe de regularidade da força:

1. **Córdoba–Martínez-Zoroa, 2023** — Euler 3D forçado, não axissimétrico, força em $C^{1,\frac12-\epsilon}\cap L^2$.
2. **Córdoba–Martínez-Zoroa–Zheng, 2024** — Navier–Stokes **hipodissipativo**, com viscosidade fracionária, força em $L^1_t C_x^{1,\epsilon}\cap L^\infty_t L^2_x$. É aqui que a viscosidade entra pela primeira vez, ainda que enfraquecida.
3. **Córdoba–Martínez-Zoroa–Zheng, 2025** (*Annals of PDE*) — Euler 3D **sem força**, em $C^\infty(\mathbb{R}^3\setminus\{0\})\cap C^{1,\beta}\cap L^2$.
4. **Alpöge–Buckmaster, agosto de 2026** — força $C^\infty$, para IPM, Boussinesq 2D e Euler 3D.
5. **OpenAI, setembro de 2026** — Navier–Stokes com viscosidade genuína $\nu>0$, força $C_c^\infty$, a partir do repouso. Enunciados (C) e (D) de Clay.

Leia a coluna da direita de cima a baixo: $C^{1,\frac12-\epsilon}$, depois $L^1_t C_x^{1,\epsilon}$, depois sem força mas com regularidade limitada, depois $C^\infty$. **O que avançou, em cada etapa, foi a regularidade da força.** Não o mecanismo — o mecanismo é o mesmo desde 2023.

E Tao registrou no mesmo post qual era o degrau seguinte, também previsível: *"deveria ser possível fazer sem o termo de forçamento"*. Ou seja, o passo 5 não era uma incógnita. Era a próxima linha de uma tabela que qualquer especialista sabia ler — desde que soubesse que existia a tabela, e que o passo 4 acabara de ser dado.

Guarde isso. É o que dá peso ao que vem a seguir.

## A cronologia da colisão

**Quinta-feira, 3 de setembro.** Circula o boato de que a Anthropic teria resolvido um grande problema em aberto; Alpöge recebe avisos de que informação sobre o progresso deles havia chegado à OpenAI. Buckmaster escreve a um matemático de destaque da OpenAI — e reproduz o e-mail integralmente na nota, dizendo preferir que se leia o texto completo a seu resumo. O conteúdo é cordial e preventivo: explica que a colaboração é estritamente pessoal, sem qualquer acordo institucional ("pago as ferramentas que meu grupo usa com meus próprios recursos de pesquisa, incluindo uma conta alta com a OpenAI"), que o trabalho será publicado em breve, artigo e formalização juntos, e que a escolha foi deliberada:

> "Decidimos intencionalmente contra despejar um certificado Lean ao lado de um *preprint* mal-acabado. Sinto fortemente que a primeira coisa que alguém lê deve ser um argumento matemático apresentado da maneira normal, e não apenas um certificado formal."

A resposta, no mesmo dia, oferece ajuda e pede detalhes: *"Se estiver disposto a dar detalhes, seria útil para evitar competirmos aqui"*, mais uma oferta de capacidade computacional.

**Sexta-feira, 4 de setembro.** Pedem para conversar naquele mesmo dia. Buckmaster propõe a semana seguinte.

**Domingo, 6 de setembro, 12h45.** Perguntam se ele pode conversar "em qualquer momento hoje". Sébastien Bubeck entra na chamada. Falam duas vezes naquela tarde; Alpöge não participa.

Nessas conversas Buckmaster é informado de que um modelo interno da OpenAI produziu uma demonstração de blow-up em tempo finito para Navier–Stokes forçado. Quando Alpöge pede por mensagem o enunciado preciso, a resposta é: *"Existência de blow-up forçado em $\mathbb{R}^3$ e $\mathbb{T}^3$"*, com *"a função de forçamento é suave, opções c e d em Fefferman"*. A demonstração teria cerca de cem páginas. Buckmaster não a viu — e, até a publicação da nota, continuava sem tê-la visto.

E aqui está a razão pela qual ele achou aquilo estranho, que é o argumento mais forte de todo o documento:

> "A rota para o problema de Clay através de uma força suave, as opções c e d no enunciado de Fefferman, é a rota que Luis e Diego abriram e a que Levent e eu havíamos discretamente escolhido atacar. **Quase ninguém que eu saiba estava trabalhando nela.** Não é a direção a que se chega em poucos dias dando o enunciado do problema a um modelo. Quando ouvi 'forçado', foi uma bandeira vermelha."

Esse ponto merece ser entendido bem, porque é técnico e decisivo. Como vimos no [texto anterior](/posts/navier-stokes-i-anatomia-de-um-problema-do-milenio/), o enunciado oficial de Clay tem quatro versões, e as opções (C) e (D) — as que permitem força externa — foram incluídas por Fefferman apenas para "dar margem razoável" a quem tentasse. Praticamente ninguém as perseguia como alvo primário. Escolher justamente essa porta lateral, e chegar a ela em dias, é uma coincidência que pede explicação.

## O que foi dito, e depois desdito

Buckmaster relata que lhe mostraram um *prompt* e disseram que o modelo de pesquisa interno simplesmente recebera o enunciado do problema. A Alpöge, Bubeck havia dito que "muito pouca entrada humana" fora usada.

> "Isso acabou não sendo verdade. Ao longo da chamada, à medida que membros da equipe mandavam correções e detalhes para o Sebastien pelo chat interno, emergiu que **uma equipe inteira** vinha trabalhando no problema, que essa era uma entre várias coisas tentadas, que o trabalho havia começado pelo problema não forçado, que a equipe primeiro pôs o modelo em problemas mais fáceis, incluindo Euler, que até mesmo o *prompt* que me foi mostrado havia sido escrito por meio de *prompting* no Codex, e que uma quantidade insana de computação foi usada."

Sobre quando o primeiro *prompt* fora enviado, a resposta demorou: *"Essa pergunta não foi respondida diretamente pela OpenAI por algum tempo. Eventualmente concordou-se que ele havia sido enviado nos últimos dias, depois de informação sobre nosso trabalho ter chegado à OpenAI."*

## A pergunta que não foi respondida

Este é o ponto que merece mais cuidado de todo o episódio, e ele costuma ser mal contado — inclusive por quem defende Buckmaster. Vale citar o parágrafo inteiro, porque cada frase importa:

> "Perguntei se o modelo havia sido treinado nas nossas sessões do Codex, ou tido acesso a elas — sessões nas quais vínhamos depositando todos os nossos rascunhos ao longo de todo o projeto. **Foi-me dito que o modelo não consulta dados de usuários. Perguntei de novo, sobre treinamento, e não obtive resposta.**"

Repare que **são duas perguntas diferentes**, e que apenas uma foi respondida.

A primeira é sobre **acesso em tempo de execução**: o modelo, enquanto trabalhava no problema, foi buscar arquivos de usuários? A resposta foi não. É uma afirmação verificável em princípio — basta auditar o que o sistema consultou — e é a afirmação que a OpenAI sustentou publicamente desde o primeiro dia.

A segunda é sobre **treinamento**: os rascunhos depositados no Codex ao longo de um ano entraram, em alguma forma, no corpus que produziu o modelo? Essa é uma pergunta de natureza completamente distinta. Não se responde olhando o log de uma execução; responde-se auditando pipelines de coleta, políticas de retenção, procedimentos de desidentificação e o histórico de treinamentos anteriores. E, no dia 6 de setembro, ela não foi respondida.

A distinção não é um preciosismo. **Dizer que o modelo "não consulta dados de usuários" é perfeitamente compatível com o modelo ter sido treinado com esses dados.** Um enunciado é sobre recuperação; o outro, sobre memória incorporada nos pesos. Responder ao primeiro quando se pergunta o segundo é responder a outra coisa.

A posição pública da OpenAI evoluiu ao longo dos dias seguintes, e a evolução é ela própria informativa. Na manhã de 8 de setembro, a formulação era cuidadosa: nem os pesquisadores nem os agentes viram o trabalho da dupla por qualquer meio até a divulgação pública; nenhum dado específico de usuário foi acessado; e — a ressalva decisiva — *ainda que improvável, não podemos descartar que dados desidentificados derivados do uso de nossos produtos tenham ajudado a melhorar nossos modelos*. No dia 9, passou-se a dizer que seria "categoricamente impossível" que os *prompts* de Buckmaster tivessem influenciado o sistema. No dia 10, após investigação interna, a formulação final: os *prompts* do Codex nos dois meses anteriores **não poderiam ter influenciado o sistema de nenhuma forma, inclusive por treinamento**.

Ou seja: a pergunta acabou respondida — três a quatro dias depois, publicamente, sob pressão, e não no momento em que foi feita. Três observações honestas sobre isso.

Primeira: a resposta final é a que a pergunta pedia, e cobre explicitamente o treinamento. Isso é um ponto a favor da OpenAI, e seria desonesto omiti-lo.

Segunda: ela cobre **dois meses**. O projeto durou mais de um ano, e os rascunhos estavam no Codex desde o começo. Buckmaster não perguntou sobre dois meses; perguntou sobre o projeto inteiro.

Terceira, e mais incômoda: uma afirmação dessas é **inverificável de fora**. Não existe hoje mecanismo pelo qual um matemático — ou o Clay, ou um árbitro de periódico — possa checar de forma independente o que entrou no corpus de treinamento de um modelo fechado. A comunidade é convidada a acreditar. Pode ser que a OpenAI esteja inteiramente correta; provavelmente está. Mas a única garantia disponível é a palavra da parte interessada, e isso é uma novidade estrutural na maneira como a matemática estabelece fatos. Historicamente, o que sustenta uma reivindicação de prioridade é um registro público e datado — um *preprint*, uma carta selada, uma ata de sessão. Aqui, parte do registro relevante é privado por construção.

É exatamente por isso que Buckmaster escreve, com uma economia que vale imitar: *"Não sei se nossos dados foram usados."* Ele não sabe. Eu também não. E o desenho atual do sistema faz com que ninguém fora da empresa possa saber.

## As duas propostas

Foram-lhe oferecidas duas saídas. A primeira: que eles publicassem o resultado sobre Euler e a OpenAI publicasse o de Navier–Stokes no dia seguinte. A segunda: que, depois de publicar Euler, **Buckmaster sozinho** escrevesse um artigo apresentando o resultado de Navier–Stokes, reconhecendo que um modelo interno da OpenAI o havia resolvido.

> "Sebastien afirmou duas vezes que queria Levent removido da autoria, e disse que tudo seria simples se não fosse o caso de — e que era tão irritante que — Levent trabalha na Anthropic."

Disseram-lhe também que, se a OpenAI publicasse depois deles, diria que eles mereciam o Prêmio Clay e que eram "os humanos mais próximos do problema". Buckmaster recusou as duas propostas e avisou que, se a OpenAI publicasse daquela forma, ele tornaria público o que havia acontecido. Segue o trecho mais citado da nota:

> "A resposta foi: 'Por que você arruinaria sua carreira?' Respondi que sou um acadêmico, e perguntei por que ele achava que tornar aquilo público arruinaria minha carreira. A resposta foi: 'Se você não quer que eu seja gentil, então eu não preciso ser gentil.'"

Mais tarde, Alpöge recebeu mensagem propondo uma conversa individual com Bubeck, com a observação: *"Não sei se o Tristan está sendo totalmente racional neste momento."* Alpöge declinou, dizendo que as conversas deveriam ser com Buckmaster.

## A outra versão

Nada disso é incontestado, e seria desonesto apresentá-lo como se fosse.

Bubeck publicou no X: *"Uma série de alegações falsas e inflamatórias contra mim está circulando nos canais sociais. Para esclarecer, entrei na discussão seguindo normas acadêmicas, e estou decepcionado que se tenha chegado a isto."* Em entrevista coletiva, negou o acesso a dados: *"Não usamos os *prompts* nem as demonstrações deles para instruir nossos modelos ou dirigir nossos agentes"*, e acrescentou que a equipe tem "nada além de parabéns a eles por essa conquista monumental". Sobre a frase a respeito da carreira, pediu desculpas pela escolha de palavras.

A OpenAI, por sua vez, afirmou que nem os pesquisadores nem os agentes viram o trabalho da dupla por qualquer meio antes da divulgação pública, e que nenhum dado específico de usuário foi acessado — admitindo inicialmente apenas que não podia descartar que dados desidentificados derivados do uso de seus produtos tivessem ajudado a melhorar seus modelos em geral. Dias depois, após investigação interna, endureceu a formulação: seria **categoricamente impossível** que os *prompts* de Buckmaster no Codex nos dois meses anteriores tivessem influenciado o sistema de qualquer forma, inclusive por treinamento. E a empresa reconheceu publicamente a prioridade de Alpöge e Buckmaster sobre o Euler forçado, além de sustentar que as demonstrações diferem significativamente e que os resultados provados são distintos no caso de Euler — forçado *versus* não forçado.

Sobre esse último ponto há divergência técnica genuína e não resolvida: Alpöge afirmou que a demonstração da OpenAI se parece mais com outra prova de blow-up para Euler que a dupla tinha.

## O balanço honesto

Vale separar o que está estabelecido do que está em disputa.

**Estabelecido.** Alpöge e Buckmaster trabalharam mais de um ano; obtiveram os resultados em 15 de agosto e os verificaram em Lean em 22 de agosto; usaram LLMs da OpenAI e da Anthropic; o método é um desenvolvimento do programa de Córdoba e Martínez-Zoroa, com aperfeiçoamentos técnicos; Buckmaster escreveu à OpenAI em 3 de setembro; houve duas chamadas em 6 de setembro com Bubeck; foram feitas duas propostas envolvendo autoria; Buckmaster publicou em 7 de setembro e a OpenAI, cerca de doze horas depois; a OpenAI reconheceu a prioridade deles sobre o Euler forçado.

**Em disputa.** Se houve qualquer vazamento — Buckmaster registra que foram avisados disso, mas diz explicitamente não estar acusando ninguém, e a OpenAI nega. Se dados desidentificados do Codex influenciaram o resultado — a OpenAI passou de "não podemos descartar que tenham melhorado nossos modelos" para "categoricamente impossível". Se os métodos são realmente distintos — a OpenAI diz que sim, Alpöge diz que não. E o tom das conversas de 6 de setembro, que cada lado descreve de maneira incompatível.

**Não estabelecido, e importa dizê-lo:** que alguém tenha roubado alguma coisa. Essa não é a alegação de Buckmaster, e não é o que os documentos mostram. O que está documentado é uma pergunta sobre treinamento feita em 6 de setembro, deixada sem resposta naquele dia, e respondida publicamente dias depois — com um recorte de dois meses sobre um projeto de um ano, e de um modo que ninguém fora da empresa tem como verificar.

O que os documentos mostram é outra coisa, e talvez mais desconfortável: uma corrida profundamente assimétrica. De um lado, dois matemáticos, uma colaboração pessoal sem acordo institucional, financiada com recursos de pesquisa do próprio bolso, um ano de trabalho. Do outro, uma empresa que iniciou o treinamento em 28 de agosto, rodou 88 horas com cerca de dez mil agentes simultâneos — 2,7 milhões de mensagens, 130 bilhões de *tokens* de saída — e anunciou doze horas depois deles. Nenhuma regra foi obviamente quebrada. E, ainda assim, quase ninguém olha para esse quadro e acha que a matemática saiu bem da história.

## A pergunta que fica

Fica, então, a pergunta que este texto não tem como responder e que o próximo vai tentar enfrentar.

A rota pelo forçamento suave foi aberta por Córdoba e Martínez-Zoroa ao longo de anos. Os aperfeiçoamentos que a levaram a Euler e a Boussinesq em $C^\infty$ são de Alpöge e Buckmaster, e foram tornados públicos um dia antes. A OpenAI enviou seu primeiro *prompt* dias antes do anúncio, sobre a rota exata que quase ninguém mais perseguia, depois de informação sobre esse trabalho ter circulado — e, como emergiu durante a chamada, com uma equipe inteira dirigindo o processo, testando o modelo antes em problemas mais fáceis, incluindo Euler.

**A OpenAI teria resolvido o problema sem os trabalhos de Córdoba–Martínez-Zoroa e de Alpöge–Buckmaster?**

Ninguém sabe, e é possível que ninguém venha a saber. Mas a pergunta tem uma irmã mais geral, que é a que realmente interessa: **as máquinas substituem mesmo o trabalho dos matemáticos humanos, ou dependem dele de um modo que a forma como anunciamos resultados esconde?**

Terence Tao deu, no mesmo dia, a imagem mais dura do debate: a de que empresas de IA estão minerando problemas matemáticos em busca de soluções e não de compreensão — e que isso *"pode destruir o ecossistema a partir do qual a próxima geração de técnicas, problemas e praticantes da matemática teria se desenvolvido"*. Ele comparou o processo a saquear um sítio arqueológico: extrai-se o objeto, destrói-se o contexto que lhe dava sentido. E lembrou o que deveria ser óbvio e anda sendo esquecido: *"a resolução efetiva desses problemas é apenas um objetivo indireto; o objetivo primário é desenvolver compreensão e discernimento matemáticos."*

É esse o assunto do terceiro texto.

## Coda: como se atribui crédito

Termino com o documento que, a meu ver, acertou o tom melhor do que todos os outros — e que quase não circulou, abafado pela polêmica.

A American Mathematical Society emitiu uma nota sobre o anúncio. Ela começa reconhecendo o feito sem reservas: a notícia de progresso na resolução do problema de Navier–Stokes, um dos grandes desafios da matemática, *"representa um avanço marcante no conhecimento humano"*. E então faz a única coisa que realmente importava fazer — **conta a história inteira**, na ordem certa:

> Esta história começou com Navier, Stokes […] os avanços recentes de **Córdoba** e **Martínez-Zoroa**, depois — assistidos por novas tecnologias — **Alpöge** e **Buckmaster**, com os passos finais dados pelos **matemáticos da OpenAI**.

Leia devagar, porque cada vírgula dessa frase é uma decisão.

Ela começa em **1822 e 1845**, não em setembro de 2026. Nomeia **Córdoba e Martínez-Zoroa em primeiro lugar** entre os contemporâneos — dois pesquisadores de um instituto público em Madri que passaram anos construindo o mecanismo e que, na cobertura de imprensa, apareceram em nota de rodapé quando apareceram. Registra que Alpöge e Buckmaster foram **"assistidos por novas tecnologias"** — sem eufemismo e sem alarde, exatamente como os próprios declararam. E credita à OpenAI **"os passos finais"** — nem mais, nem menos: passos finais são passos reais, e são finais.

E note a última palavra: *matemáticos* da OpenAI. Não "a IA da OpenAI". A AMS escolheu atribuir o feito a pessoas, numa empresa, que dirigiram um sistema — o que, como se soube durante aquela chamada de 6 de setembro, é a descrição correta: uma equipe inteira, várias tentativas, problemas mais fáceis antes, *prompts* escritos com ajuda do Codex.

Não há nisso nenhuma diminuição de ninguém. Há o contrário: cada um recebe exatamente o que lhe cabe, e a corrente aparece como corrente. Nenhuma das quatro contribuições faz sentido sem a anterior. **Todos têm seus créditos, como deveria ser** — e, talvez, como só a comunidade matemática organizada ainda saiba fazer, num ambiente em que o resto do mundo tende a atribuir tudo a quem anuncia por último e mais alto.

Se esta história deixar alguma coisa de saldo, que seja essa frase da AMS. Ela é mais curta que qualquer um dos comunicados das partes, e é a única que não precisou ser corrigida depois.

## Fontes

**Documentos primários**

- Buckmaster, T. *Statement*. Courant Institute of Mathematical Sciences, New York University, 7 set. 2026. [PDF](https://cims.nyu.edu/~tristanb/statement.pdf).
- Alpöge, L.; Buckmaster, T. *Blowup for the Boussinesq Equations with Smooth Forcing*, set. 2026. [PDF](https://cims.nyu.edu/~tristanb/boussinesq.pdf).
- Córdoba, D.; Martínez-Zoroa, L. *Blow-up for the incompressible 3D-Euler equations with uniform $C^{1,\frac12-\epsilon}\cap L^2$ force*, set. 2023. [arXiv:2309.08495](https://arxiv.org/abs/2309.08495).
- American Mathematical Society. [*Statement on the Navier–Stokes announcement*](https://www.ams.org/news?news_id=7686), set. 2026.
- OpenAI. [*On the Navier–Stokes Millennium Prize Problem*](https://openai.com/index/navier-stokes-solution/), 8 set. 2026.
- Clay Mathematics Institute. [*Navier–Stokes Announcement*](https://www.claymath.org/news/navier-stokes-announcement/), set. 2026.

**Comentário técnico**

- Tao, T. [*Finite time blowup with smooth forcing term for the incompressible porous medium, Boussinesq, and incompressible Euler equations*](https://terrytao.wordpress.com/2026/09/07/finite-time-blowup-with-smooth-forcing-term-for-the-incompressible-porous-medium-boussinesq-and-incompressible-euler-equations/). *What's new*, 7 set. 2026.
- Córdoba, D.; Martínez Zoroa, L. *Singularidades en 3D: el desafío matemático de Euler y Navier-Stokes*, v. III, n. 1, p. 95–108, jan. 2026.

**Cobertura**

- *An NYU mathematician clashed with OpenAI over a \$1 million proof*. **The Seattle Times**, set. 2026.
- *OpenAI says it cracked Navier–Stokes, one of math's grand challenges*. **Fortune**, 8 set. 2026.
- [*Navier–Stokes priority controversy*](https://en.wikipedia.org/wiki/Navier%E2%80%93Stokes_priority_controversy). Wikipedia (verbete em formação; consultado em 14 set. 2026).
