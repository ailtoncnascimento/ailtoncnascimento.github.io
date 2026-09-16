---
title: "Navier–Stokes (III): o que significa ser matemático na era da IA"
date: 2026-09-16 08:00:00 -0300
categories: [Miscelânea, Matemática]
tags: [inteligência artificial, Navier-Stokes, Terence Tao, Medalha Fields, EMS, filosofia da matemática, ética na ciência, futuro da matemática]
math: true
---

> **Terceiro e último da série.** O [primeiro](/posts/navier-stokes-i-anatomia-de-um-problema-do-milenio/) tratou do problema e do que foi provado; o [segundo](/posts/navier-stokes-ii-a-controversia-contada-pelos-documentos/), da disputa de prioridade. Este trata da pergunta que sobrou: se as máquinas vão nos substituir, e o que é, afinal, ser matemático.

Na semana que se seguiu ao anúncio de 8 de setembro, aconteceu uma coisa que eu não me lembro de ter visto antes. A comunidade matemática — que tipicamente discute suas crises em corredores de congresso e listas de e-mail fechadas — se organizou **em público**, e em três documentos.

No dia 10, a **Sociedade Matemática Europeia** publicou uma nota assinada por seu presidente e três dirigentes. Em algum momento daqueles dias, **vinte e cinco medalhistas Fields** — de Pierre Deligne, premiado em 1978, a Yu Deng, premiado este ano — assinaram uma declaração conjunta com um título que não deixa dúvida sobre o tom: *A Severe Misalignment of AI in Mathematics*. E no dia 12, o blog de Terence Tao publicou um ensaio de dois filósofos da matemática propondo uma reformulação inteira da pergunta.

São documentos diferentes, com autores diferentes e ênfases diferentes. Mas convergem de um modo que vale examinar, porque nenhum deles diz o que a manchete diria. Nenhum deles pergunta se a máquina vai vencer o matemático.

## Antes do anúncio: problemas como recurso não renovável

Convém começar por um texto anterior a tudo isso. Em **2 de setembro**, seis dias antes do anúncio da OpenAI, Tao escreveu em sua conta no Mathstodon uma reflexão que, relida agora, parece premonitória.

O ponto de partida é uma observação de economia intelectual. Problemas em aberto podem ser gerados aos milhares — mas, nas palavras dele, *"a esmagadora maioria desses problemas não vale a atenção que se lhes daria: eles não demonstram nenhuma propensão particular a revelar novas percepções ou conexões com outras questões."* Bons problemas — os que funcionam como farol, os que ao serem atacados obrigam a inventar uma teoria — são **escassos**. E são escassos de um modo específico: uma vez respondidos, não voltam.

Daí a formulação que me parece a mais forte de todo o debate: responder a uma pergunta *"pode acarretar custos irreversíveis"*, e os problemas em aberto são, por isso, algo parecido com um **recurso não renovável**. A analogia é com o *spoiler*: saber o final diminui permanentemente o valor de assistir.

E então a imagem que circulou o mundo, publicada no mesmo dia: a mineração automatizada e indiscriminada de problemas em aberto em busca de soluções *"é como usar escavadeiras para tirar tesouros de um sítio arqueológico, destruindo o contexto histórico que dava a esses tesouros boa parte do seu significado."*

Note que o objeto da crítica não é a inteligência artificial. É o **modo** de usá-la: indiscriminado, automatizado, orientado a extração. Em outra ocasião Tao usou uma imagem mais suave e igualmente precisa — ferramentas de IA como pegar um helicóptero até o sítio da escavação: você chega, mas perde todos os benefícios da jornada.

Há ainda um diagnóstico estrutural, de abril, que explica por que a comunidade foi pega despreparada: a matemática está passando de um regime de **escassez de demonstrações** para um de **abundância de demonstrações**, e nem sua cultura nem sua infraestrutura se adaptaram a isso. Nossos periódicos, nossos pareceres, nossos critérios de contratação e promoção, nossos seminários — tudo foi desenhado para um mundo em que provar um teorema difícil era raro e caro. Esse mundo acabou de mudar, e as instituições não mudaram junto.

## A EMS: o problema não é o crédito, é o acesso

A nota da Sociedade Matemática Europeia, de **10 de setembro**, assinada por Jan Philip Solovej, Victoria Gould, Helge Holden e Adam Skalski, faz duas coisas.

A primeira é de justiça histórica, e ecoa o que já vimos nos textos anteriores: o trabalho *"não surge do vácuo"*. A nota nomeia **Diego Córdoba, Luis Martínez-Zoroa, Fan Zheng, Levent Alpöge e Tristan Buckmaster**, e acrescenta o progresso de décadas de matemáticos no mundo inteiro. Registra também, com sobriedade, que *"questões de autoria e crédito no novo mundo da matemática produzida por interação humano-máquina precisarão ser resolvidas"*.

A segunda é a que me parece mais aguda, e quase não foi noticiada. A EMS aponta que **o modelo usado é interno à OpenAI e não é acessível de forma geral** — e classifica isso como *"um problema sério que a comunidade matemática precisa enfrentar"*, invocando explicitamente os compromissos com ciência aberta e igualdade de oportunidades.

Vale entender por que isso é grave, e não apenas inconveniente.

A matemática é, entre as ciências, aquela cuja pretensão de verdade repousa inteiramente na **verificabilidade por qualquer um**. Não há laboratório caro, não há amostra que só um grupo possui, não há equipamento sob patente. Um argumento matemático é público por construção: quem discorda pode pegar papel e refazê-lo. É por isso que a matemática funciona sem hierarquia de autoridade — a autoridade é o argumento.

Um resultado produzido por um sistema fechado rompe isso em dois lugares. Não se pode reproduzir o processo que gerou a demonstração, o que já é ruim. E, como vimos no texto anterior, não se pode nem sequer auditar se ele usou o trabalho não publicado de terceiros, o que é pior. Some-se a isso a desigualdade de acesso — um departamento em Teresina, em Madri ou em Bucareste não dispõe de dez mil agentes rodando por 88 horas — e o que se tem não é uma ferramenta nova, é uma **assimetria nova**.

## Vinte e cinco Medalhas Fields

A declaração conjunta é o documento mais duro dos três, e seu título é a tese: existe um **desalinhamento severo** entre os objetivos das empresas de IA e os da comunidade matemática.

O texto abre reconhecendo o fato sem minimizá-lo: nos últimos meses as capacidades matemáticas dos modelos melhoraram dramaticamente, *"a ponto de poderem resolver grandes problemas em aberto em muitos campos da matemática"*. Ninguém ali está negando o que aconteceu. A crítica é outra: *"o esforço das empresas de IA para resolver problemas matemáticos como um teste de desempenho é prejudicial à ciência da matemática e à comunidade matemática."*

O argumento central está numa passagem que vale citar com cuidado:

> "Problemas famosos frequentemente serviram como marcos e faróis contra os quais se pode medir uma compreensão aprimorada dessa paisagem. Resolver um desses problemas foi sempre um sinal certo de novas percepções e métodos interessantes, que então seriam estudados por uma comunidade de matemáticos, através de um processo longo e árduo de palestras, discussões, simplificações. Ao final desse processo, idealmente se encontrará uma apresentação em livro-texto dos resultados, adequada para qualquer estudante de pós-graduação ou mesmo de graduação."

Está tudo aí. O problema famoso nunca foi o objetivo — foi o **instrumento de medida**. Resolver Fermat importou porque produziu as curvas modulares e a teoria de deformações de Galois, não porque uma igualdade passou a ter um selo de "verdadeira". E o ciclo só se completa quando o resultado atravessa o processo lento — palestras, discussões, simplificações — que termina com um estudante de mestrado conseguindo aprendê-lo.

Daí a frase que resume a preocupação, e que é a mesma de Tao em outras palavras: *"resolver problemas é apenas uma ferramenta e um substituto para alcançar o objetivo primário, que é a compreensão conceitual e o discernimento. Esquecer isso no mundo da IA pode voltar a ferramenta contra o objetivo primário. De fato, a produção em massa, num ritmo cada vez mais acelerado, de afirmações 'verdadeiro/falso' poderia destruir terreno fértil em vez de insuflar vida em novas ideias."*

E há uma passagem que me tocou particularmente, porque é sobre o ofício e não sobre a tecnologia:

> "A comunidade matemática funciona, de muitas maneiras, como uma versão em miniatura da humanidade. […] **Os recursos mais preciosos da nossa profissão são os estudantes e as ideias**, e é a eles que dedicamos o maior cuidado. Sentimo-nos responsáveis por deixá-los crescer até seu pleno potencial, até que possam viver uma vida própria no mundo matemático."

Quem orienta sabe exatamente do que se trata. O problema que damos a um aluno de mestrado quase nunca é escolhido por ser importante — é escolhido por ser **formativo**, por obrigá-lo a aprender uma técnica, a ler certa literatura, a errar de um jeito específico e produtivo. Se esses problemas passam a ser resolvidos em minutos por um sistema, o que se perde não é o resultado. É a formação.

A declaração fecha ampliando o escopo, e aqui ela deixa de ser sobre matemática: em muitos campos, anos de treinamento serviram não apenas para produzir uma resposta final, mas para desenvolver compreensão e a capacidade de formular novas perguntas. Quando o sistema passa a produzir diretamente o resultado desse trabalho, esses dois objetivos **deixam de estar alinhados**. A pergunta, dizem os signatários, é de toda a sociedade: como garantir que, ao mudar o modo como o trabalho é feito, não se perca de vista aquilo que o trabalho pretendia alcançar.

## Resposta certificada não é solução

O terceiro documento é um ensaio dos filósofos **Silvia De Toffoli e Eamon Duede**, publicado como texto convidado no blog de Tao em 12 de setembro, sob o título *After Math*. Ele faz a distinção conceitual que faltava ao debate.

Existem, argumentam, **duas noções de demonstração**. Há a demonstração **lógica**: uma cadeia verificável por procedimento mecânico, e é exatamente isso que uma formalização em Lean certifica. E há a demonstração **inteligível**: aquela que revela *por que* algo é verdadeiro, que pode ser lida, ensinada, generalizada, adaptada a outro problema. As duas coisas não são a mesma, e a segunda não se segue da primeira.

O que a OpenAI entregou, na leitura deles, é **uma resposta** — mas *"não está claro que tenham entregue uma solução frutífera"*. Falta *"uma demonstração inteligível que matemáticos humanos possam entender e usar para fazer avançar os objetivos da matemática"*. A verificação formal isolada, dizem, produz *"obstáculos em vez de inspiração"*.

E aqui é preciso observar uma coisa que raramente se nota: **a melhor evidência dessa tese veio dos próprios autores do resultado humano**. Como vimos no texto anterior, Alpöge e Buckmaster tiveram sua demonstração certificada em Lean no dia 22 de agosto — e passaram as **três semanas seguintes** trabalhando sem parar para entender o que tinham. Buckmaster descreve a primeira versão como a demonstração mais horrenda que já leu, e o texto final sobre Euler como *AI slop*, pedindo desculpas por ele. Não é retórica de crítico externo. É o relato de quem estava lá.

O ensaio recusa também a premissa implícita de todo o debate: a de que *"a matemática é apenas sobre resolver problemas"*. Ela é também desenvolver teorias e técnicas, formar comunidades, treinar as próximas gerações, produzir trabalho esteticamente valioso, entender conexões entre campos. Reconhecer isso, insistem, **não é mudar as regras do jogo depois de perder** — é reconhecer que a matemática é um *jogo infinito*, sem condição determinada de vitória.

## A escolha

O que leva à formulação que é, a meu ver, a melhor coisa escrita sobre o assunto até agora, e que vale reproduzir por inteiro:

> A IA apresenta à matemática não um fim, mas uma **escolha** sobre o que a prática matemática deve se tornar. Se o sucesso matemático passar a ser identificado de forma muito estreita com a produção de respostas certificadas, a matemática corre o risco de se adaptar precisamente àquelas características que são mais fáceis de mensurar e automatizar.
>
> Se, em vez disso, os matemáticos tratarem a IA como uma tecnologia para impulsionar seus propósitos históricos e essencialmente humanos, a tecnologia poderá contribuir para um florescimento e enriquecimento acelerado da disciplina. A questão importante, portanto, não é se a IA derrotará os matemáticos, mas **a quais fins matemáticos queremos que a IA sirva**.

Repare no mecanismo que está sendo descrito, porque ele é o oposto de uma ameaça externa. Não é a máquina que estreita a matemática — somos nós, se deixarmos que a métrica mais fácil de medir vire a definição de sucesso. É o velho problema de Goodhart aplicado a uma ciência inteira: quando uma medida vira meta, deixa de ser boa medida. Contratar, promover e financiar por contagem de problemas resolvidos sempre foi uma aproximação grosseira; funcionava porque resolver era caro. Se resolver ficar barato e a métrica não mudar, a profissão vai se reorganizar em torno daquilo que a métrica premia — e o que ela premia é justamente a parte automatizável.

O corolário é otimista, e eu concordo com ele: o que sobra para os humanos **não são as sobras**. Ao contrário — é uma oportunidade de esclarecer qual é a verdadeira essência da matemática. Somos forçados a nos perguntar de novo o que realmente buscamos quando fazemos matemática.

## O telescópio

Tao, em entrevista, formula a mesma ideia pelo lado construtivo, e acrescenta uma previsão concreta sobre o que vai mudar no ofício.

A IA, diz ele, vai mudar o que os matemáticos fazem, mas não os tornará desnecessários. Ela pode aproximar a matemática das **ciências naturais**: descobre-se algo primeiro, e depois se tenta entender por que funciona. Quem trabalha com EDP reconhece o movimento — é o que já acontece quando uma simulação numérica revela um comportamento que levará anos para ser demonstrado. A diferença é de escala, e ela agora vale para o teorema, não só para o experimento.

O ponto seguinte é o que mais me interessa profissionalmente. Uma IA pode dar uma resposta sem deixar claras as ideias por trás dela. E mesmo uma demonstração **correta** pode ser tão longa ou complexa que nos diz pouco além de que a resposta está certa. Saber que algo é verdadeiro e compreendê-lo bem são coisas diferentes — e só a segunda se transmite, se generaliza, se ensina.

Donde a descrição do trabalho que resta, que não é pouco: **encontrar explicações mais simples, criar conexões, fazer boas perguntas**. À medida que a IA nos fornecer mais resultados, dar sentido a eles pode se tornar uma parte maior da matemática, não menor. E a imagem final:

> Vejo a IA como um novo tipo de telescópio. Ela nos ajuda a ver mais longe, mas ainda temos que entender o que vemos.

A analogia é exata, e é generosa com a máquina sem ser ingênua. O telescópio de Galileu não tornou os astrônomos obsoletos — tornou possível uma astronomia que não existia, e exigiu uma geração inteira para descobrir o que fazer com aquilo que ele mostrava. Ninguém confundiu ver Júpiter com entender Júpiter.

Há, no entanto, um alerta de Tao que precisa vir junto, e que é o mais político de tudo o que ele escreveu: *"se não fizermos essas perguntas nós mesmos, elas serão respondidas por nós por uma empresa de tecnologia, ou decididas por incentivos financeiros."*

## Três perguntas que eu não sei responder

Chego ao ponto em que devo parar de citar gente competente e dizer o que eu mesmo penso. E o que eu penso, honestamente, é que **queremos saber qual é o futuro da matemática em cinco anos sem entender direito o presente**. Deixo três perguntas, nenhuma retórica.

**Primeira.** O número de submissões ao arXiv cresceu muito e diversos problemas estão caindo. Mas há muitos outros que não caíram. Foi porque ninguém tentou, ou porque são mais difíceis para os modelos? E nós — os que trabalhamos nessas questões ainda de pé — temos alguma chance com elas? Elas vão continuar de pé com a próxima geração de modelos? Não sei. E o desconfortável é que não tenho nem como estimar.

**Segunda.** Ao que tudo indica há um esforço em curso, da ordem de centenas de milhões de dólares, para resolver mais problemas do milênio. O que caiu era o mais bem compreendido, aquele para o qual existia uma estratégia plausível que já havia funcionado em outras EDPs — como mostrei no [primeiro texto](/posts/navier-stokes-i-anatomia-de-um-problema-do-milenio/), a escada estava montada e numerada. Os outros não caíram. Por quê? E se caírem amanhã, isso significa triunfo da força bruta, ou outra coisa? A resposta muda completamente o que devemos concluir.

**Terceira.** A afirmação de que "a IA não sabe propor problemas novos, estratégias diferentes ou teorias novas" é defendida com base em quê? Temos experimentos nessa direção? Eu a ouço repetida com muita confiança em corredores, inclusive por mim, e desconfio que ela seja mais consoladora do que fundamentada. Se for verdadeira, é o argumento mais importante do nosso lado, e merecia evidência melhor do que a nossa impressão.

É muito importante que essas perguntas possam ser exploradas e resolvidas de forma **sistemática**. E aqui vale dizer uma coisa com todas as letras: **as empresas de IA são empresas, não parceiras de investigação científica.** Não deveríamos planejar nosso futuro apenas com as informações parciais que elas nos passam — é exatamente esse o ponto que a EMS levantou ao apontar que o modelo é fechado, e é exatamente o que Tao quer dizer ao avisar que, se não fizermos as perguntas, alguém as responderá por nós.

Há medidas que terão de ser tomadas agora. Mas parece-me que, em meio a tantas incertezas, deveríamos estar mais preocupados em **preservar valores** do que em repensar a infraestrutura da profissão. Infraestrutura se reconstrói; a cadeia de transmissão entre um orientador e um aluno, não — e é dela que a declaração dos vinte e cinco fala quando diz que os recursos mais preciosos da profissão são os estudantes e as ideias.

Então: os matemáticos serão substituídos por máquinas?

Acho que a pergunta está mal-posta, e os três documentos desta semana explicam por quê. A matemática nunca foi a produção de sentenças verdadeiras. Se fosse, um gerador de teoremas aleatórios verificados em Lean já teria nos aposentado há uma década — ele produz verdades às toneladas, e nenhuma interessa a ninguém. A matemática é o que uma comunidade humana faz com essas sentenças: organiza, simplifica, conecta, ensina, e a partir daí pergunta a próxima coisa.

Nada disso está automatizado. Muito disso talvez nunca esteja, porque depende de julgar o que **vale a pena** — e valer a pena é um juízo sobre fins, não sobre fatos. O que mudou é que a parte mecânica do nosso trabalho ficou barata, e isso nos obriga a ser explícitos sobre a parte que não era mecânica e que nós mesmos raramente soubemos nomear.

Talvez seja esse o saldo. Fomos obrigados, por uma máquina, a explicar por que fazemos isto.

## Conclusão pessoal: *Erbarme dich*

Termino saindo da matemática, porque o limite de que quero falar não é matemático.

Abaixo está Magdalena Kožená cantando *Erbarme dich, mein Gott* — a ária nº 39 da **Paixão segundo São Mateus**, BWV 244, de Johann Sebastian Bach. Ouça antes de prosseguir. São sete minutos, e eles fazem diferença para o que vem depois.

{% include embed/youtube.html id='DQUYZHKnn58' %}

_Magdalena Kožená, contralto. Bach, *Matthäus-Passion* BWV 244, nº 39._

A ária ocorre logo depois de Pedro negar Jesus três vezes. É uma expressão de arrependimento e um clamor por piedade e perdão — *Erbarme dich, mein Gott*, "tem piedade de mim, meu Deus", canta a voz, sobre um violino solo que soluça junto com ela e que é, em boa parte, o outro personagem da cena.

Mas ela é bem mais do que isso. É também um pungente grito por misericórdia de uma humanidade miserável atolada na dor.

Quando a ouvimos, não é apenas uma belíssima melodia que ouvimos, mas **um significado que captamos** — que expressa uma experiência humana complexa e profunda: a consciência da nossa condição de dor e sofrimento, e a esperança de redenção pela intercessão do amor divino.

Poderia uma IA tê-la composto?

A melodia, sem dúvida. Mas seria apenas uma colherada de mel sonoro, incapaz de veicular qualquer significado que a transforme em arte. O significado, esse, é fruto de uma **intenção significativa originária na consciência de Bach**, revestida em música que ouvimos e decodificamos de volta em significado. A ária só existe como diálogo entre humanos; a beleza sonora, por si só, é apenas o meio.

Por isso, a meu ver, uma IA não poderia nunca a ter composto: não sendo humana, ela é incapaz de produzir significados. E mesmo que um dia inventássemos uma IA capaz de consciência doadora de significado, esse significado seria mera paródia — porque não expressaria genuínas experiências humanas.

Porque a arte é mergulho na vivência humana, a arte só pode ser produzida por humanos.

## "E você consegue?"

Junto a essa paixão outra, o cinema — e uma cena que virou emblema do assunto antes mesmo de o assunto existir.

Em *Eu, Robô* (2004), inspirado na coleção de contos de Isaac Asimov de 1950, o detetive Del Spooner tenta diminuir o robô Sonny lembrando-lhe que ele é apenas uma máquina, incapaz de criar, sentir ou compreender a complexidade da existência humana:

> — Um robô consegue escrever uma sinfonia? Um robô consegue transformar uma tela numa obra-prima?

E Sonny faz uma pergunta de três palavras:

> — **E você consegue?**

É nesse instante que a discussão deixa de ser sobre inteligência artificial e passa a ser sobre nós.

Gostamos de acreditar que somos diferentes das máquinas porque sentimos, sonhamos e criamos. Mas quantas dessas capacidades realmente exercemos? A maioria das pessoas acorda no mesmo horário, segue a mesma rotina, repete os mesmos pensamentos, reage aos mesmos estímulos, e vive anos sem questionar se está escolhendo o próprio caminho ou apenas executando um programa escrito por hábitos, medos e expectativas alheias.

Sonny foi criado para obedecer. O homem, para escolher. Mas muitos abrem mão dessa liberdade e passam a viver no piloto automático, presos a padrões que nunca decidiram construir.

Talvez a maior diferença entre um robô e um ser humano não seja a capacidade de pensar. Seja a **coragem de questionar**. Porque uma máquina executa comandos; já um ser humano consciente é capaz de interromper o ciclo, desafiar as próprias certezas e decidir quem deseja se tornar.

E aqui as duas metades deste texto se encontram, o que eu não havia previsto quando comecei a escrevê-lo. A declaração dos vinte e cinco medalhistas Fields diz que o objetivo primário da matemática é a compreensão, e que resolver problemas é apenas o instrumento. O ensaio dos filósofos distingue a demonstração que certifica da demonstração que **explica**. Tao diz que saber que algo é verdadeiro e compreendê-lo bem são coisas diferentes. Todos estão dizendo, em vocabulário técnico, o que a ária diz sem vocabulário nenhum: que a forma correta, sozinha, não significa nada. Que o que importa é o sentido, e que sentido é coisa que se dá e se recebe entre pessoas.

Uma demonstração de cem páginas verificada em Lean e uma melodia perfeitamente bem formada têm exatamente o mesmo problema, se ninguém compreender por que são como são. São ambas verdadeiras. Nenhuma das duas, por si só, é arte nem é matemática.

No fim, a pergunta de Sonny continua ecoando. Não basta nascer humano: é preciso viver como um. E talvez seja esse o presente inesperado que as máquinas nos trazem — a urgência de descobrirmos como ser humanos, verdadeiramente.

## Referências e leituras

**Documentos da comunidade**

- *A Severe Misalignment of AI in Mathematics*. Declaração conjunta assinada por 25 medalhistas Fields — entre eles Artur Avila, Pierre Deligne, Maxim Kontsevich, Peter Scholze, Terence Tao, Maryna Viazovska e Cédric Villani. [mathandai.org](https://mathandai.org/).
- European Mathematical Society. [*EMS statement on recent Navier–Stokes announcement*](https://euromathsoc.org/news/ems-statement-on-recent-navier-stokes-announcement-225), 10 set. 2026. Assinada por J. P. Solovej, V. Gould, H. Holden e A. Skalski.
- American Mathematical Society. [*Statement on the Navier–Stokes announcement*](https://www.ams.org/news?news_id=7686), set. 2026.

**Ensaios e entrevistas**

- De Toffoli, S.; Duede, E. [*After Math*](https://terrytao.wordpress.com/2026/09/12/after-math/). Texto convidado no blog *What's new*, de T. Tao, 12 set. 2026.
- Tao, T. [Fio no Mathstodon sobre problemas em aberto como recurso não renovável](https://mathstodon.xyz/@tao/117237320796901560), 2 set. 2026.
- Tao, T. *'The job description is changing': mathematician Terence Tao on the rise of AI*. **Nature**, 2026. [Link](https://www.nature.com/articles/d41586-026-01246-9).
- [*Terence Tao on AI in mathematics (and beyond)*](https://teorth.github.io/tao-web/ai-views.html) — compilação de posicionamentos públicos, com datas e fontes.

**Música e cinema**

- Bach, J. S. *Matthäus-Passion*, BWV 244 (1727), nº 39, ária para contralto e violino solo: *Erbarme dich, mein Gott*. Interpretação de [Magdalena Kožená](https://youtu.be/DQUYZHKnn58).
- *Eu, Robô* (*I, Robot*), dir. Alex Proyas, 2004 — inspirado na coleção de contos homônima de Isaac Asimov (1950). [A cena](https://www.instagram.com/reels/DbTBbBHhV2I/).

**Nesta série**

- [Navier–Stokes (I): anatomia de um problema do milênio](/posts/navier-stokes-i-anatomia-de-um-problema-do-milenio/), 14 set. 2026.
- [Navier–Stokes (II): a controvérsia, contada pelos documentos](/posts/navier-stokes-ii-a-controversia-contada-pelos-documentos/), 15 set. 2026.
