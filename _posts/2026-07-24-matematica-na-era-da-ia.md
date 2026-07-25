---
title: "Da escassez à abundância: a matemática na era da IA"
date: 2026-07-25 06:00:00 -0300
categories: [Matemática, Miscelânea]
tags: [inteligência artificial, terence tao, filosofia da matemática, formalização, icm 2026]
math: true
description: O que muda, e o que não muda, quando máquinas passam a gerar demonstrações. Uma reflexão a partir da palestra de Terence Tao no ICM 2026.
---

Esta semana fechei, sem planejar, uma pequena trilogia. Comentei aqui o [contraexemplo da Conjectura Jacobiana]({% post_url 2026-07-22-conjectura-jacobiana-contraexemplo-ia %}), depois o [da conjectura de Goemans]({% post_url 2026-07-23-contraexemplo-conjectura-goemans-fluxos %}), e em seguida a [conversa de Terence Tao com uma IA]({% post_url 2026-07-23-tao-blog-milagre-desmontado %}) que desmontou o primeiro. Três episódios em poucos dias, todos com o mesmo protagonista coadjuvante: um modelo de linguagem.

Ontem, no Congresso Internacional de Matemáticos em Filadélfia, o próprio Tao subiu ao palco para dar sentido a tudo isso. A palestra se chamava *Mathematics in the Age of AI*, e o slide que resume seu argumento circulou rápido. Vou usá-lo como espinha dorsal deste texto — porque ele responde, com uma clareza que eu não conseguiria improvisar, à pergunta que todo colega meu anda fazendo em voz baixa: *e agora?*

## O diagrama

A tese de Tao começa desmontando uma confusão. Quando alguém pergunta "a IA vai fazer matemática?", está tratando "fazer matemática" como uma coisa só — resolver o problema. Mas não é uma coisa só. Tao decompõe a atividade em cinco etapas encadeadas:

$$
\text{problema} \;\xrightarrow{\text{gerar}}\; \text{solução não verificada} \;\xrightarrow{\text{verificar}}\; \text{solução verificada}
$$

$$
\xrightarrow{\text{expor}}\; \text{solução bem escrita} \;\xrightarrow{\text{publicar}}\; \text{solução aceita} \;\xrightarrow{\text{canonizar}}\; \text{teoria definitiva}
$$

Ou seja: uma demonstração nasce como rascunho (geração), precisa ser conferida (verificação), depois explicada de modo que outros entendam (exposição), então submetida e aceita pela comunidade (publicação) e, por fim, digerida e incorporada aos livros-texto, de onde as próximas gerações a herdam sem precisar reconstruí-la (canonização).

Só a última etapa é o que faz o conhecimento *durar*. O teorema de Pitágoras não é uma folha solta num servidor; é parte do tecido comum da matemática, algo que um estudante recebe pronto. Chegar lá é um trabalho coletivo de décadas.

A pergunta de Tao, então, deixa de ser "a IA faz matemática?" e passa a ser muito mais precisa: **em qual das cinco etapas?**

## Onde a IA já é forte

Na primeira etapa — gerar —, a resposta de 2026 é inequívoca: sim, e às vezes espetacularmente.

Não são mais promessas. É um portfólio. Em maio, um modelo de raciocínio da OpenAI refutou uma conjectura de Erdős sobre distâncias unitárias no plano, aberta desde 1946, com uma construção que conectou teoria algébrica dos números a um problema de geometria discreta de um jeito inédito — e Tim Gowers julgou que o resultado, vindo de um humano, mereceria os *Annals of Mathematics*. Em julho, um sistema produziu uma demonstração da Conjectura do Duplo Recobrimento por Ciclos, aberta há meio século, acompanhada de formalização em Lean. Os dois contraexemplos que comentei nesta semana pertencem à mesma onda.

E não é só matemática pura. Sistemas de IA encontraram centenas de vulnerabilidades de segurança genuínas em software auditado havia anos — a Anthropic relata mais de 500 falhas de alta severidade validadas por seu modelo, e um sistema independente encontrou todas as 12 vulnerabilidades de uma atualização do OpenSSL, algumas despercebidas por décadas. O AlphaEvolve, do Google, descobriu um algoritmo para multiplicar matrizes complexas $4\times4$ com 48 multiplicações escalares, batendo o recorde anterior. O AI Co-Scientist gerou hipóteses de reposicionamento de fármacos que foram validadas em células hepáticas humanas reais.

O traço comum a esses casos — e é o que os torna convincentes, não apenas impressionantes — é que **a verificação foi externa e objetiva**. Uma vulnerabilidade recebe um CVE e é corrigida, ou não. Um algoritmo de multiplicação retorna o produto certo com menos operações, ou não. Uma demonstração em Lean compila, ou não. Nenhum desses veredictos depende da eloquência do modelo.

## Onde a coisa fica interessante

Repare, porém, no que todos esses exemplos têm em comum na *segunda* etapa. O duplo recobrimento por ciclos veio com Lean. Os oito problemas do Caderno de Kourovka resolvidos pelo sistema da Harmonic vieram com Lean. A conjectura da Jacobiana veio com um certificado de verificação quase trivial — três pontos e um determinante. A vulnerabilidade veio com um caso de teste executável.

Isso não é coincidência. É a condição de credibilidade. Um modelo de linguagem é, por construção, uma máquina de produzir texto plausível — e texto plausível é exatamente o que uma demonstração falsa mas convincente também é. A única defesa robusta contra a "prosa persuasiva porém errada" é uma instância externa que não se deixa persuadir: um verificador formal, um compilador, um mantenedor de software cético, um experimento de laboratório.

A verificação, segunda etapa do diagrama, é onde a IA está avançando agora — e é o gargalo que decide se a abundância da primeira etapa vira conhecimento ou ruído. Tao é explícito sobre isso: são as ferramentas de verificação formal, acopladas aos modelos, que tornam a geração em escala *confiável*. Sem elas, um mar de demonstrações geradas automaticamente seria um mar de afirmações que alguém ainda teria de conferir uma a uma — e conferir é caro.

## Onde continua sendo humano

E aí chegamos às três etapas restantes — expor, publicar, canonizar —, que é onde a palestra de Tao vira, no fundo, uma defesa do que a matemática tem de humano.

Considere a diferença entre **verificar** e **entender**. O contraexemplo da Jacobiana estava correto desde o primeiro instante: qualquer um podia substituir os três pontos e conferir. Isso é verificação. Mas ninguém *entendia* aquilo — os números pareciam arbitrários, o cancelamento parecia um milagre. O entendimento só veio quando Tao perguntou "que estrutura torna isso menos milagroso?" e descobriu que o objeto era, disfarçadamente, a multiplicação de um polinômio de grau 1 por um de grau 2. A máquina produziu o objeto verificável. O humano produziu o *sentido*.

Essas são coisas diferentes, e a segunda não se reduz à primeira. Uma demonstração verificada em Lean pode ser um labirinto de dez mil linhas que ninguém consegue ler — formalmente impecável e humanamente opaca. Transformá-la numa ideia que se possa segurar na cabeça, ensinar num quadro, generalizar para outro problema: isso é a etapa de exposição, e é criação, não transcrição.

Quanto a publicar e canonizar — decidir o que **importa**, quais perguntas valem a pena, o que merece entrar no cânone e o que é curiosidade passageira —, isso é julgamento de valor, e julgamento de valor pressupõe uma comunidade com uma história, um gosto e um senso de direção. Foi o consenso que emergiu do simpósio de Stanford em maio, reunindo três medalhistas Fields e pesquisadores da OpenAI e da DeepMind: as ferramentas já reformulam *como* a matemática é feita, mas definir os conceitos certos, entender por que uma prova funciona e decidir quais perguntas importam continuam sendo tarefas humanas.

## Da escassez à abundância

Há uma frase de Tao que, para mim, é a chave de tudo. Estamos saindo de uma era de **escassez de demonstrações** e entrando numa era de **abundância de demonstrações**.

Vale pensar no que isso muda, porque não é pouco. Durante toda a história da matemática, a demonstração foi o recurso escasso. Um problema difícil podia esperar décadas por uma única prova, e essa prova era um acontecimento. Toda a sociologia da área — o prestígio, a autoria, a estrutura dos periódicos — foi construída em torno dessa escassez.

O que acontece quando o rascunho deixa de ser o caro? Quando gerar uma demonstração candidata fica barato, e o custo se desloca inteiramente para conferir, entender, organizar e decidir o que vale?

Muda o lugar onde o trabalho humano é mais precioso. Se antes o gargalo era ter a ideia, agora, cada vez mais, o gargalo é dar sentido a uma enxurrada de ideias. O matemático do futuro próximo talvez se pareça menos com um explorador solitário abrindo uma trilha e mais com um editor exigente diante de material em excesso — separando o que é profundo do que é meramente correto, o que ilumina do que apenas se verifica.

Não acho isso diminuidor. Pelo contrário. As três etapas que sobram para nós — entender, comunicar, decidir o que importa — são precisamente as mais difíceis de terceirizar, porque são as que dependem de consciência, de gosto e de uma noção de propósito. São a parte da matemática que sempre foi, no melhor sentido, humana.

## Uma nota pessoal

Escrevo isto como alguém que trabalha com equações dispersivas — boa colocação, decaimento, dinâmica de longo prazo. Já usei essas ferramentas para conferir uma conta que levaria uma tarde, para testar se uma desigualdade era plausível antes de investir dias nela, para reorganizar um argumento emperrado. Elas são úteis de um jeito concreto e cotidiano.

Mas a pergunta que abre uma pesquisa — *por que este fenômeno acontece? o que este obstáculo está tentando me dizer?* — essa continua sendo minha, e das minhas conversas com colegas e alunos. A máquina responde muito bem a perguntas bem postas. Fazer a pergunta certa, na ordem certa, ainda é o trabalho.

Foi o que Tao mostrou ao vivo esta semana, ao não aceitar um milagre e insistir em entendê-lo. E é, no fim, o que este blog vem tentando registrar em cada um dos textos desta série: não a máquina resolvendo problemas, mas o pensamento humano em ação — usando uma ferramenta nova, e permanecendo, ele próprio, o centro.

> *A IA já é forte na geração e avança na verificação. As etapas restantes — expor, publicar, canonizar — ainda dependem fortemente do julgamento e do trabalho humanos. Estamos passando de uma era de escassez de demonstrações para uma era de abundância. E ainda há muito a fazer até que a IA sirva de fato como uma ferramenta que potencialize — e não substitua — o trabalho de matemáticos e cientistas.*
>
> — a partir da palestra de Terence Tao, *Mathematics in the Age of AI*, ICM 2026.

## Referências

1. T. Tao, *Mathematics in the Age of AI*, palestra pública, Congresso Internacional de Matemáticos (ICM), Filadélfia, 24 de julho de 2026.
2. *AI will be top of mind at ICM, math's biggest conference*, Simons Foundation, maio de 2026.
3. *Future of Mathematics Symposium*, Stanford, 1–2 de maio de 2026.
4. GPT-5.6 Sol High, *Evidence that AI systems can produce genuinely novel and valuable work*, compilação de casos, 2026.
5. T. Tao, *A digestion of the Jacobian conjecture counterexample*, What's new, 21 de julho de 2026.
