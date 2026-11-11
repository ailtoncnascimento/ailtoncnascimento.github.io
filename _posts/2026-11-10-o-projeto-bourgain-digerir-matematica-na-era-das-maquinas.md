---
title: "O Projeto Bourgain: digerir matemática na era das máquinas"
date: 2026-11-10 09:00:00 -0300
categories: [Miscelânea, Matemática]
tags: [Jean Bourgain, Projeto Bourgain, espaços de Bourgain, equações dispersivas, continuação única, Zakharov-Kuznetsov, KdV, Schrödinger, inteligência artificial, futuro da matemática]
math: true
description: "Um projeto comunitário quer entender, por completo, os mais de quinhentos artigos de Jean Bourgain. Numa época em que máquinas produzem demonstrações em série, digerir matemática talvez seja a tarefa mais humana que nos resta. Dois exemplos da minha área mostram como contribuir."
---

> **Continuação da série sobre matemática e inteligência artificial.** O texto anterior, [Dia 6 de outubro de 2026: o dia que mudou a matemática para sempre](/posts/dia-6-de-outubro-de-2026-o-dia-que-mudou-a-matematica/), terminava com mais perguntas do que respostas. Este é sobre uma das respostas que a comunidade começou a dar. A série inteira, desde o [contraexemplo da Conjectura Jacobiana](/posts/conjectura-jacobiana-contraexemplo-ia/) e o [diagrama de Tao no ICM](/posts/matematica-na-era-da-ia/), está reunida na [Miscelânea](/miscelanea/).

No texto sobre o dia 6 de outubro, abri com uma frase de Jacob Tsimerman, Medalha Fields deste ano: em breve teremos demonstrações que ninguém compreende. Passei as semanas seguintes pensando nela, e me ocorreu uma coisa que deveria ter sido óbvia desde o começo. Para quem trabalha com equações dispersivas, demonstrações que quase ninguém compreende não são novidade nenhuma. Nós convivemos com elas há mais de trinta anos. Elas têm até um autor: **Jean Bourgain**.

Treze dias depois do 6 de outubro, apareceu no blog de Terence Tao um texto convidado anunciando o **Projeto Bourgain** ([*The Bourgain Project*](https://terrytao.wordpress.com/2026/10/19/the-bourgain-project/), 19 out. 2026). Ele foi assinado por três matemáticos: Lukas Liehr, Mitchell Taylor e meu amigo **João Pedro Ramos**, do IMPA. A proposta é simples de enunciar e enorme de executar: entender, por completo, cada um dos mais de quinhentos artigos de Bourgain, e escrever esse entendimento de modo que um matemático em início de carreira consiga acompanhar.

Confesso que eu já tinha lido sobre o projeto, mas não tinha percebido que o João era um dos seus protagonistas. Isso mudou na sexta-feira, 6 de novembro. Eu estava na plateia da palestra plenária que ele deu no [7º Workshop em Equações Dispersivas Não Lineares](https://impa.br/evento/7th-workshop-on-nonlinear-dispersive-equations/), no IMPA, um encontro internacional que celebrou também os 65 anos de **Felipe Linares**, meu orientador de doutorado. O lugar não poderia ser mais apropriado: o auditório estava cheio de gente que vive, todos os dias, das ideias de Bourgain.

Foi uma palestra marcante, e para mim emblemática. O João revisitou os grandes momentos da obra de Bourgain e depois apresentou o projeto como um esforço comunitário, aberto a todos. Mas o tema central da fala foi a inteligência artificial. Ao fundo, o tempo todo, estava a pergunta que tem ocupado esta série: o que significa fazer matemática numa época em que as máquinas também a fazem? Saí do auditório com a certeza de que tinha testemunhado um daqueles momentos em que uma comunidade começa a responder, em voz alta, a uma pergunta que até então só fazia em voz baixa.

A minha leitura do que vi, e que é minha, é esta: num momento em que as máquinas passaram a *produzir* demonstrações em escala industrial, um grupo de matemáticos decidiu dedicar-se a *digerir* demonstrações. Este texto é sobre essa diferença. Vou contar o que é o projeto, como contribuir com ele e mostrar dois exemplos concretos, ambos da minha área, do que significa digerir Bourgain.

## Quem foi Jean Bourgain

Muitos leitores desta Miscelânea talvez nunca tenham ouvido falar de Bourgain, e isso diz mais sobre a distância entre a matemática e o grande público do que sobre ele. Vale contar um pouco da sua história, seguindo o [obituário oficial](https://www.ias.edu/news/press-releases/2019/jean-bourgain-obituary) publicado pelo Instituto de Estudos Avançados de Princeton (IAS).

Jean Bourgain nasceu em 1954, em Ostende, uma cidade à beira-mar na Bélgica. Fez o doutorado em Bruxelas, aos 23 anos, e em pouco tempo passou a ser disputado pelas melhores instituições do mundo: deu aulas nos Estados Unidos, na França, em Israel. Em 1994 chegou ao IAS, em Princeton, a casa onde trabalharam Einstein e von Neumann, e ali ficou até o fim da vida.

O que mais impressiona em Bourgain é a abrangência. A maioria dos grandes matemáticos deixa sua marca numa área, às vezes em duas. Bourgain resolveu problemas célebres em meia dúzia delas, de campos que estudam o infinito e a forma dos espaços até a teoria dos números, que estuda os inteiros, e chegou a contribuir para a ciência da computação e a probabilidade. Já no fim da vida, com dois colegas, resolveu um problema sobre somas de potências de inteiros que estava em aberto havia mais de oitenta anos. E, na área em que eu trabalho, a das equações que descrevem ondas, ele criou as ferramentas que todos nós usamos até hoje. Escreveu mais de quinhentos artigos, com mais de cento e trinta coautores.

Os prêmios acompanharam a obra. O mais conhecido é a **Medalha Fields**, que recebeu em 1994 e que costuma ser chamada de "Nobel da matemática". Vieram depois o Prêmio Shaw, o Prêmio Crafoord (dividido com Terence Tao), o Breakthrough Prize e, em 2018, um prêmio da Sociedade Americana de Matemática pelo conjunto da obra, em cuja citação foi chamado de gigante da análise matemática. O governo belga chegou a lhe conceder o título de barão. No obituário, Peter Sarnak, seu colega em Princeton, diz que o brilho analítico de Bourgain não tinha igual.

Bourgain morreu em 22 de dezembro de 2018, aos 64 anos, na Bélgica, depois de uma longa luta contra o câncer. Deixou a esposa, a matemática Mei-Chu Chang, e o filho, Eric.

Além da obra, Bourgain deixou um estilo. Escrevia de um jeito muito particular, e os seus artigos são famosos pela concisão. A página do projeto diz, com delicadeza, que eles eram muitas vezes escritos de uma só vez, deixando ao leitor a tarefa de preencher os detalhes. Quem já tentou ler um deles sabe o que isso quer dizer na prática: uma estimativa que ocupa uma linha pode custar uma semana de trabalho; uma frase como "o mesmo argumento se aplica em dimensões mais altas" pode custar uma tese de doutorado. Nos comentários do anúncio no blog de Tao, alguém lembrou, com humor, que o MathOverflow está cheio de perguntas do tipo "estou tentando entender um passo técnico de um artigo de Bourgain".

Até Terence Tao passou por isso. No texto que escreveu quando Bourgain morreu, em dezembro de 2018, Tao conta que, como aluno de doutorado em Princeton, passou meses tentando entender o artigo de Bourgain de 1991 sobre os problemas de restrição e de Kakeya, publicado na *GAFA*, e que foi o artigo mais difícil que já tinha lido. Só conseguiu decifrá-lo com a ajuda de Elias Stein e de Tom Wolff. E aí a sua opinião sobre o artigo se inverteu. Passou a ver as ferramentas "básicas" de Bourgain, como a decomposição diádica e o princípio da incerteza, como atalhos, e com elas a leitura dos artigos seguintes ficou muito mais rápida. Boa parte dos primeiros trabalhos de Tao consistiu em melhorar resultados de Bourgain. Uma digestão, portanto, e das mais bem-sucedidas da história recente da análise.

Tao conta ainda, no mesmo texto, como nasceu o único artigo que escreveu com Bourgain. Por volta de 2002, mencionou a ele um problema do tipo soma-produto em corpos finitos. Bourgain achou primeiro que haveria uma demonstração fácil por análise de Fourier, depois admitiu que o problema era mais interessante do que parecia. Meses depois, Tao recebeu por fax uma demonstração manuscrita de duas páginas. Daí saiu o artigo de Bourgain, Katz e Tao sobre estimativas soma-produto em corpos finitos. O fax original se perdeu.

Há uma ironia que me parece importante. Bourgain foi, por décadas, o caso mais extremo de um fenômeno que hoje nos assusta: resultados corretos, profundos, cujas demonstrações estavam escritas, publicadas e, no entanto, eram compreendidas por pouquíssimas pessoas. A comunidade não entrou em pânico. Fez outra coisa: passou décadas digerindo. E dessa digestão nasceram áreas inteiras. A minha é uma delas.

## O que é o Projeto Bourgain

O projeto vive em [bourgain-pedia.com](https://bourgain-pedia.com/), que se descreve como uma enciclopédia expositiva e expandida da obra de Bourgain. Os objetivos declarados são sete, e vale resumi-los:

1. Entender toda a obra de Bourgain, por completo, e apresentá-la de modo que qualquer matemático em atividade possa acompanhar.
2. Encontrar maneiras melhores de apresentar matemática do que o PDF, sozinho.
3. Experimentar palestras mais envolventes, com vídeos e animações.
4. Identificar padrões e ferramentas recorrentes na obra, e mapear as áreas em que ele trabalhou e as conexões entre elas.
5. Entender o impacto dessa obra sobre outros matemáticos.
6. Construir uma comunidade, em que matemáticos se juntem para escrever exposições dos artigos mais influentes das suas áreas.
7. Estimular outros projetos coletivos, relacionados ou não a este.

O site se organiza em poucas seções. Em [*All articles*](https://bourgain-pedia.com/articles.html) está a bibliografia completa de Bourgain, com referência, contagem de citações e link para cada artigo. Em [*Expositions*](https://bourgain-pedia.com/digested.html) ficam as exposições já escritas, que podem vir acompanhadas de vídeos, formalizações, animações e repositórios. Em [*Bourgain's collaborators*](https://bourgain-pedia.com/collaborators.html) estão todos os seus coautores, organizados de várias maneiras, inclusive num mapa. Há ainda uma página de links, uma página [*About*](https://bourgain-pedia.com/about.html) com as políticas do projeto e a página [*Contribute*](https://bourgain-pedia.com/contribute.html), de que falarei adiante.

Os mantenedores são os três autores do anúncio: Mitchell A. Taylor (Oxford e Toronto), João Pedro Ramos (IMPA) e Lukas Liehr (Bar-Ilan). O projeto se apresenta como complementar ao prêmio [*Paper of the Future*](https://amathr.org/prizes/paper-of-the-future-prize/) e à nova revista [*Mathematical Discourse*](https://www.mathematicaldiscourse.org/), duas outras iniciativas preocupadas com a forma como a matemática é escrita e transmitida.

Três políticas me chamaram a atenção, porque dialogam diretamente com tudo o que discutimos nesta série.

- **Exatidão.** Uma exposição deve ser correta e completa, dentro da boa-fé. Se um passo do artigo original não puder ser verificado, a exposição deve dizer isso com todas as letras, em vez de passar por cima. Erros encontrados no original devem ser registrados, com tato, e se possível corrigidos.
- **Uso de IA.** A única exigência é a transparência: quem usar ferramentas de IA deve declarar. O próprio site, aliás, registra nos agradecimentos que foi construído com a ajuda de um modelo de linguagem.
- **Formalização.** O projeto incentiva formalizações em Lean ou em outros assistentes de prova, e os mantenedores se dizem à vontade para discutir como apresentá-las.

Repare na combinação. O projeto não proíbe as máquinas nem as idolatra. Pede que se diga quando foram usadas, e põe no centro algo que nenhuma verificação automática entrega sozinha: a exigência de que *alguém entenda* e de que o entendimento fique escrito. No texto sobre o 6 de outubro, escrevi que verificado não é verdadeiro, e verdadeiro não é compreendido. O Projeto Bourgain é uma aposta inteira na terceira palavra.

## Primeiro exemplo: os espaços de Bourgain, digeridos

Para mostrar o que é uma boa digestão, escolhi um texto que nunca foi escrito para o Projeto Bourgain, mas que poderia ter sido. Trata-se de *Fourier Restriction Norm Method*, um projeto de pós-graduação escrito em 2018 por **Andreia Chapouto**, então aluna da escola de pós-graduação MIGSAA, em Edimburgo, sob a orientação de Tadahiro Oh e Oana Pocovnicu. São quarenta e poucas páginas que destrincham uma fatia dos dois artigos de Bourgain de 1993 que fundaram o chamado **método da norma de restrição de Fourier**. Para quem trabalha com equações dispersivas, esses artigos são o equivalente a uma certidão de nascimento.

### O problema

Considere uma equação de evolução do tipo

$$
\partial_t u = \mathcal{L}u + \mathcal{N}(u), \qquad u(0)=u_0,
$$

em que $\mathcal{L}$ é um operador diferencial com coeficientes constantes e $\mathcal{N}$ é uma não linearidade. Os dois exemplos centrais são a equação de Schrödinger não linear (NLS) e a de Korteweg–de Vries (KdV), em que

$$
\mathcal{L} = i\,\partial_x^2 \quad (\text{NLS}), \qquad \mathcal{L} = -\partial_x^3 \quad (\text{KdV}).
$$

Aplicando a transformada de Fourier na variável espacial, $\mathcal{L}$ vira multiplicação por $i\,h(n)$, em que $h$ é a **relação de dispersão**: $h(n)=-n^2$ para NLS e $h(n)=n^3$ para KdV. O problema linear se resolve explicitamente, e o não linear se escreve pela fórmula de Duhamel,

$$
u(t) = e^{t\mathcal{L}}u_0 + \int_0^t e^{(t-t')\mathcal{L}}\,\mathcal{N}(u(t'))\,dt'.
$$

A estratégia é tratar o lado direito como uma aplicação $\Gamma_{u_0}$ e mostrar que ela é uma contração num espaço conveniente. Toda a dificuldade está na palavra "conveniente".

Na reta real, a resposta clássica são as **estimativas de Strichartz**, que exploram o fato de que ondas de frequências diferentes viajam com velocidades diferentes e, portanto, se espalham: a solução decai no tempo. No toro $\mathbb{T}=\mathbb{R}/2\pi\mathbb{Z}$, isso falha. As ondas não têm para onde ir. Dão a volta e reencontram-se. Era preciso outra ideia.

### A ideia de Bourgain

A ideia é olhar para a solução linear no espaço de Fourier em **espaço e tempo**. Se $u$ resolve $\partial_t u = \mathcal{L}u$, a transformada de Fourier espaço-temporal de $u$ vive inteiramente sobre a curva característica

$$
\{(\tau,n)\in\mathbb{R}\times\mathbb{Z} : \tau = h(n)\}.
$$

Para NLS, a parábola $\tau=-n^2$; para KdV, a cúbica $\tau=n^3$. A aposta de Bourgain é que, para tempos curtos, a solução não linear não deve se afastar muito dessa curva: sua transformada deve se concentrar numa vizinhança dela. A figura que Chapouto reproduz do livro de Tao mostra isso com clareza: à esquerda, a cúbica fina da solução linear de KdV; à direita, uma faixa engordada em torno dela, onde vive a solução não linear.

Os **espaços de Bourgain** $X^{s,b}$ são feitos sob medida para medir essa proximidade. A norma é

$$
\lVert u \rVert_{X^{s,b}} = \Big\lVert \langle n\rangle^{s}\,\langle \tau - h(n)\rangle^{b}\,\widehat{u}(\tau,n) \Big\rVert_{\ell^2_n L^2_\tau}
= \big\lVert e^{-t\mathcal{L}}u \big\rVert_{H^b_t H^s_x},
$$

com $\langle x\rangle = (1+x^2)^{1/2}$. O peso $\langle n\rangle^s$ mede regularidade em espaço, como num espaço de Sobolev comum. O peso $\langle \tau-h(n)\rangle^b$ é a novidade: ele penaliza a parte de $u$ que mora longe da curva característica. A segunda igualdade traduz isso: a norma $X^{s,b}$ é a norma de Sobolev da solução depois de "desfazermos" a evolução linear.

### As peças do argumento

O texto de Chapouto separa o método em peças, e a digestão está justamente nessa separação.

**Inclusão em funções contínuas.** Se $b>\tfrac12$, então $X^{s,b}\subset C_tH^s_x$. É a imersão de Sobolev em uma dimensão, aplicada à variável temporal. É o que garante que o ponto fixo seja uma solução honesta.

**Estimativas lineares.** Com $\eta$ uma função de corte suave no tempo,

$$
\lVert \eta(t)\,e^{t\mathcal{L}}u_0 \rVert_{X^{s,b}} \lesssim \lVert u_0\rVert_{H^s}, \qquad
\Big\lVert \eta(t)\int_0^t e^{(t-t')\mathcal{L}}F(t')\,dt' \Big\rVert_{X^{s,b}} \lesssim \lVert F\rVert_{X^{s,b-1}}, \quad b>\tfrac12.
$$

A segunda diz que integrar no tempo faz ganhar exatamente uma derivada temporal: $F$ está em $X^{s,b-1}$, e a integral, em $X^{s,b}$. O corte $\eta$ é obrigatório: sem ele, a solução linear não está em $X^{s,b}$, porque sua norma no tempo é tomada sobre a reta inteira.

**Localização no tempo.** Para $-\tfrac12 < b' \le b < \tfrac12$ e $0<T<1$,

$$
\lVert \eta(t/T)\,u \rVert_{X^{s,b'}} \lesssim T^{\,b-b'}\,\lVert u\rVert_{X^{s,b}}.
$$

É daqui que sai a potência positiva de $T$ que faz a aplicação $\Gamma_{u_0}$ contrair para tempos pequenos. Note a restrição $b<\tfrac12$: para usá-la, as estimativas não lineares precisam "chegar" num espaço com $b$ estritamente menor que $\tfrac12$, deixando uma folga.

**Princípio de transferência.** Uma estimativa multilinear válida para soluções lineares $e^{t\mathcal{L}}f$ com dados em $H^s$ se transfere automaticamente para funções em $X^{s,b}$, com $b>\tfrac12$. A razão é que toda função de $X^{s,b}$ é uma superposição de soluções lineares moduladas no tempo.

Com isso, o problema de boa colocação local fica reduzido a uma única tarefa: **provar estimativas não lineares**. Todo o resto é maquinaria geral.

### A estimativa $L^4$ e a aritmética escondida

A estimativa decisiva para NLS cúbica, provada por Bourgain em 1993, é

$$
\lVert u \rVert_{L^4_{t,x}(\mathbb{R}\times\mathbb{T})} \lesssim \lVert u\rVert_{X^{0,3/8}}.
$$

Por que $3/8$? Chapouto oferece uma heurística que eu adoraria ter lido quando era aluno. A imersão de Sobolev em duas variáveis $(t,x)$ dá $X^{1/4,1/4}\subset L^4_{t,x}$: um quarto de derivada em espaço e um quarto em tempo. Mas, na equação de Schrödinger, duas derivadas em espaço "valem" uma derivada em tempo. Transferindo o quarto de derivada espacial para o tempo, ele vira um oitavo, e o total fica $\tfrac14+\tfrac18=\tfrac38$. E $\tfrac38<\tfrac12$: é a folga de que a localização no tempo precisa.

A demonstração, que Chapouto apresenta seguindo um argumento de Nikolay Tzvetkov, decompõe $u$ em pedaços diádicos segundo a distância à parábola e reduz tudo a um **problema de contagem**. Fixados $n=n_1+n_2$ e $\tau$, quantos inteiros $n_1,n_2$ satisfazem $\tau = -n_1^2-n_2^2 + O(K)$? A identidade elementar

$$
(n_1-n_2)^2 = 2(n_1^2+n_2^2) - (n_1+n_2)^2 = -2\tau - n^2 + O(K)
$$

mostra que $(n_1-n_2)^2$ está preso num intervalo de comprimento $O(K)$. Logo $n_1-n_2$ assume no máximo $O(K^{1/2})$ valores. Uma estimativa de análise harmônica virou uma pergunta de teoria dos números sobre pontos inteiros perto de uma parábola. Daí o título do artigo de Bourgain, que fala em fenômenos de restrição da transformada de Fourier a certos subconjuntos de reticulados.

Com a estimativa $L^4$ na mão, uma desigualdade de Hölder e um argumento de dualidade dão a estimativa trilinear

$$
\lVert u_1u_2u_3 \rVert_{X^{0,-1/2+\varepsilon}} \lesssim \prod_{j=1}^3 \lVert u_j\rVert_{X^{0,1/2-\delta}}, \qquad 0<\varepsilon,\delta\le\tfrac18,
$$

e daí, com as peças lineares, a **boa colocação local de NLS cúbica em $L^2(\mathbb{T})$**. Para a não linearidade quíntica, o caminho passa por uma estimativa $L^6$ com uma perda $N^{0+}$, que vem de contar divisores de inteiros de tamanho $N^2$. A conclusão é a boa colocação em $H^\varepsilon(\mathbb{T})$ para todo $\varepsilon>0$, e não em $L^2$. A perda da função divisor, que cresce mais devagar que qualquer potência mas não fica limitada, aparece intacta no expoente de regularidade.

### KdV: a ressonância e os contraexemplos

Para KdV, a peça central é a **estimativa bilinear** de Kenig, Ponce e Vega (1996). O segredo está numa identidade algébrica: se $n=n_1+n_2$, então

$$
n^3 - n_1^3 - n_2^3 = 3\,n\,n_1\,n_2.
$$

Consequência: entre as três distâncias à cúbica, $\langle\tau-n^3\rangle$, $\langle\tau_1-n_1^3\rangle$ e $\langle\tau_2-n_2^3\rangle$, a maior é pelo menos da ordem de $\lvert n\,n_1n_2\rvert$. É esse ganho que paga a derivada da não linearidade $u\,\partial_xu$. Daí sai a boa colocação local de KdV periódica em $H^s(\mathbb{T})$ para $s\ge-\tfrac12$, abaixo de $L^2$.

O que mais aprecio no texto de Chapouto, e que considero a marca de uma digestão de verdade, é a seção de **contraexemplos**. Ela mostra, com funções concretas, que cada hipótese da estimativa bilinear é necessária:

- sem a condição de média nula, a estimativa falha para todos $s,b$, porque quando $n_1=0$ ou $n_2=0$ o produto $n\,n_1n_2$ se anula e o ganho desaparece;
- se a estimativa vale, então necessariamente $b=\tfrac12$, o que força a troca de $X^{s,b}$ pelos espaços $Y^s$, que acrescentam uma componente $\ell^2_nL^1_\tau$ para recuperar a continuidade no tempo;
- se a estimativa vale, então $s\ge-\tfrac12$.

Um artigo de pesquisa prova que algo funciona. Uma boa digestão mostra também *por que* não poderia funcionar de outro jeito. Na linguagem do Projeto Bourgain, um texto como o de Chapouto é quase uma exposição pronta de uma parte dos artigos de 1993: preenche passos, oferece heurísticas, testa os limites com exemplos e acompanha a literatura posterior, de Kenig–Ponce–Vega a Colliander, Keel, Staffilani, Takaoka e Tao.

## Como contribuir

A página [*Contribute*](https://bourgain-pedia.com/contribute) descreve o processo, que é deliberadamente simples.

1. **Escolha um artigo** na lista de artigos de Bourgain que está na própria página. Ao lado de cada um, há um botão para indicar que você quer trabalhar nele, pedindo nome, e-mail, instituição e se você procura colaboradores. Seu nome passa a aparecer junto ao artigo, e quem tiver interesse no mesmo texto pode procurá-lo. A lista pode ser filtrada entre artigos ainda livres, em andamento e já expostos.
2. **Escreva a exposição.** A orientação é apresentar o artigo do jeito que você gostaria de lê-lo. Pode-se seguir o argumento de Bourgain, propor casos-teste mais simples, incluir várias demonstrações com ideias diferentes ou explorar generalizações e perguntas posteriores.
3. **Envie por e-mail** aos mantenedores (o endereço está na página *About*): o código-fonte `.tex` expandido e o PDF compilado, com o título e o ano do artigo, seu nome como deve aparecer, repositórios ou vídeos que você tenha criado e uma nota dizendo se e como usou IA.
4. **A exposição é publicada** na seção *Expositions*. Ela continua pertencendo aos seus autores, sob a licença que eles escolherem.
5. **Outras contribuições** também são bem-vindas: comentários, histórias sobre Bourgain, conexões entre trabalhos, esclarecimentos sobre a sua caixa de ferramentas, ajuda para mapear a influência da obra.

Para encontrar parceiros, há um [canal no Zulip](https://bourgain.zulipchat.com). Exposições múltiplas do mesmo artigo e exposições em grupo são explicitamente incentivadas.

Penso, em particular, nos nossos programas de pós-graduação. Um seminário de doutorado que passe um semestre lendo um artigo de Bourgain, linha por linha, produz exatamente o tipo de texto que o projeto procura. E produz, de quebra, a melhor formação que conheço: ninguém aprende tanto sobre uma técnica quanto quem teve de explicar por que cada passo de uma demonstração famosa é verdadeiro.

## Segundo exemplo: um parágrafo de 1997 e uma tese de 2025

O segundo exemplo é mais próximo de casa, e é dele que me orgulho.

### A pergunta

Em 1997, Bourgain publicou no *International Mathematics Research Notices* um artigo curto, de onze páginas, intitulado *On the compactness of the support of solutions of dispersive equations*. A pergunta é uma versão fraca do que se chama **propriedade de continuação única** (UCP):

> Se uma solução suave de uma equação dispersiva tem suporte compacto durante um intervalo de tempo não trivial, ela é necessariamente nula?

A intuição física é clara: uma equação dispersiva espalha instantaneamente qualquer perturbação localizada. Uma solução que permanecesse confinada numa caixa seria uma onda que não dispersa. A pergunta é provar isso para equações *não lineares*, em que a não linearidade poderia, em princípio, compensar a dispersão.

A história do problema é longa. Saut e Scheurer (1987) usaram estimativas de Carleman para uma classe de equações dispersivas; Zhang (1992) tratou KdV e mKdV por espalhamento inverso. Bourgain introduziu, em 1997, um método inteiramente diferente, baseado em **análise complexa**, simples o bastante para se adaptar a muitos modelos. O artigo contém uma observação, um daqueles parágrafos à Bourgain, segundo a qual o método se estende a modelos dispersivos não lineares em outras dimensões. A demonstração dessa extensão, em dimensão arbitrária, não estava lá.

### O método, em dois tempos

No caso **linear**, o argumento é bonito e curto. Se $u(t)$ tem suporte num cubo $[-B,B]^n$, o teorema de Paley–Wiener diz que $\widehat{u}(t)$ se estende a uma função inteira em $\mathbb{C}^n$ com crescimento no máximo exponencial, da ordem de $e^{B\lvert\sigma\rvert}$ na direção imaginária $\sigma$. Por outro lado, a evolução linear multiplica $\widehat{u}$ por $e^{it\,p(\lambda)}$, em que $p$ é o símbolo da equação. Para a equação de Zakharov–Kuznetsov,

$$
\partial_t u + \partial_{x_1}\Delta u + u\,\partial_{x_1}u = 0, \qquad x\in\mathbb{R}^n,
$$

o símbolo é $p(\lambda)=\lambda_1\lvert\lambda\rvert^2$, um polinômio cúbico. Na direção complexa, $e^{it\,p(\lambda+i\sigma)}$ cresce como a exponencial de um polinômio cúbico, rápido demais para ser compatível com o crescimento de Paley–Wiener. A única saída é $\widehat{u}\equiv0$.

No caso **não linear**, a solução é vista como uma perturbação da linear, pela fórmula de Duhamel. Para que a perturbação seja pequena, é preciso escolher bem o ponto $\lambda$ em que se olha. É aqui que entra o lema-chave da página 440 do artigo de Bourgain. Defina

$$
u^{\ast}(\lambda) = \sup_{t\in I}\,\big\lvert \widehat{u}(t)(\lambda)\big\rvert.
$$

Em uma dimensão, toma-se $m(\lambda)=\sup_{\lvert\lambda'\rvert\ge\lvert\lambda\rvert}u^{\ast}(\lambda')$, que é monótona em $\lvert\lambda\rvert$. O lema afirma que, se a solução não é identicamente nula, existem frequências $\lambda$ arbitrariamente grandes em que valem, ao mesmo tempo,

$$
m(\lambda) > e^{-\lvert\lambda\rvert/Q} \qquad\text{e}\qquad m(\lambda) > c\,(m\ast m)(\lambda).
$$

A primeira condição diz que $\widehat{u}$ não é exponencialmente pequena ali; a segunda diz que a não linearidade, que no lado de Fourier é uma convolução, não domina a parte linear. Nesses pontos, o termo não linear de Duhamel é controlado pelo linear, e o argumento linear volta a funcionar.

### Onde está a dificuldade

Em dimensão maior, o lema deixa de ser rotina por uma razão concreta, que os autores identificaram com precisão: a função $m$, que em dimensão $n$ precisa ser redefinida (veja abaixo), **deixa de ser monótona** no tamanho $\lvert\lambda\rvert$. Em uma dimensão, a monotonia permite um argumento de "primeiro ponto de falha": se o lema falhasse, haveria um menor raio em que uma cota exponencial deixa de valer, e a monotonia propaga a informação para todas as frequências maiores. Em $\mathbb{R}^n$, "maior" deixa de ter um sentido único.

Foi isso que **Dieme P. da Silva**, hoje na UEMASUL, em Imperatriz, resolveu na sua tese de doutorado no Departamento de Matemática da UFPI, em trabalho com meus colegas **Roger P. de Moura** e **Gleison N. Santos**. O artigo, publicado neste ano no *Journal of Mathematical Analysis and Applications* e em acesso aberto, é *On the unique continuation and stabilization for the $n$-dimensional Zakharov–Kuznetsov equation*. Os autores afirmam que, até onde sabem, é o primeiro artigo em que o lema da página 440 de Bourgain é demonstrado em dimensões $n\ge2$.

A solução é elegante. Em vez de comparar frequências pelo tamanho, compara-se coordenada a coordenada. Com a norma do máximo, $\lvert x\rvert=\max_j\lvert x_j\rvert$, define-se

$$
A_\lambda = \{\lambda'\in\mathbb{R}^n : \lvert\lambda'_j\rvert\ge\lvert\lambda_j\rvert \ \text{para todo } j\}, \qquad m(\lambda)=\sup_{\lambda'\in A_\lambda}u^{\ast}(\lambda').
$$

Com a ordem parcial $\lambda\preceq\tilde\lambda$ quando $\lvert\lambda_j\rvert\le\lvert\tilde\lambda_j\rvert$ para todo $j$, a função $m$ é monótona *para essa ordem*: $\lambda\preceq\tilde\lambda$ implica $m(\tilde\lambda)\le m(\lambda)$. E, para qualquer conjunto de índices $J$, o vetor $\lambda_J$, que conserva só as coordenadas de $\lambda$ indexadas por $J$, satisfaz $\lambda_J\preceq\lambda$, logo $m(\lambda)\le m(\lambda_J)$.

Essa última observação é o pulo do gato. Suponha, por absurdo, que o lema falhe a partir de algum raio. Os autores mostram que, então,

$$
m(\lambda) < \frac{2B_1}{1+\lvert\lambda\rvert^{2n}}\,e^{-\lvert\lambda\rvert/(2(\lambda_0+Q))} \qquad\text{para todo } \lambda\in\mathbb{R}^n.
$$

Se essa cota falhasse em algum ponto, haveria um menor raio $\delta$ em que ela falha. Um ponto $\lambda$ de raio $\delta$ tem alguma coordenada de módulo $\delta$; projetando sobre ela, obtém-se um vetor sobre um eixo, digamos $\delta e_1$, com $m$ pelo menos tão grande. O problema $n$-dimensional fica reduzido a um ponto sobre um eixo, onde ele se comporta como em uma dimensão. A integral de convolução $(m\ast m)(\delta e_1)$ é então separada numa região em que as duas frequências têm raio menor que $\delta$, onde a cota já vale, e no complementar, onde a escolha do ponto extremal dá $m\le m(\delta e_1)$. A primeira parte contribui no máximo com metade da cota; a segunda, com no máximo metade de $m(\delta e_1)$. Somando, $m(\delta e_1)$ fica abaixo da cota, o que contradiz a escolha de $\delta$. O outro caso, em que falha a primeira das duas desigualdades do lema, é mais simples. A cota exponencial, por sua vez, torna $u(t)$ analítica numa faixa complexa, o que é incompatível com suporte compacto, a menos que $u\equiv0$.

O resto da demonstração segue o roteiro de Bourgain, com as adaptações de dimensão: escolhe-se $\lambda$ com $\lambda_1\lambda_k>0$ e um deslocamento imaginário $\sigma$ pequeno, de sinal escolhido para que os fatores $e^{s\,\mathrm{Im}\,p(\lambda+i\sigma)}$ decaiam no intervalo de integração, e estimam-se separadamente a parte linear, o termo não linear em $\lambda$ e o erro de deslocar para $\lambda+i\sigma$. O resultado final é o

> **Teorema** (da Silva, de Moura e Santos, 2026). Seja $u$ uma solução suave de $\partial_tu+\partial_{x_1}\Delta u+\gamma\,u\,\partial_{x_1}u=0$ em $\mathbb{R}^n$, com $\gamma\ge0$, definida num intervalo não degenerado $I=[-T,T]$. Se, para algum $B>0$, o suporte de $u(t)$ está contido no cubo $[-B,B]^n$ para todo $t\in I$, então $u\equiv0$.

### A aplicação: a energia que se dissipa

Um teorema de continuação única raramente é um fim em si. Neste caso, ele é a peça que faltava num problema de **estabilização**. Considere a equação de Zakharov–Kuznetsov num cubo $\Omega=(0,L)^n$, com condições de fronteira adequadas e um termo de amortecimento localizado $a(x)u$, com $a\ge0$ e $a\ge a_0>0$ fora de um compacto $\Gamma$. A energia

$$
E(u(t)) = \frac12\int_\Omega u^2\,dx
$$

decresce ao longo do fluxo. A pergunta é se ela vai a zero, e com que velocidade. A resposta dos autores é que o decaimento é **exponencial**: para dados com $\lVert u_0\rVert_{L^2(\Omega)}\le R$, existe $\delta=\delta(R)>0$ com

$$
E(u(t)) \le C\,E(u(0))\,e^{-\delta t}, \qquad t\ge0.
$$

A demonstração passa por uma desigualdade de observabilidade, provada por um argumento de compacidade e unicidade: supõe-se que ela falha, extrai-se uma sequência normalizada, passa-se ao limite e obtém-se uma solução que se anula onde o amortecimento atua. Estendida por zero ao espaço todo, ela tem suporte compacto, e é aí que entra a continuação única: a solução limite é nula, o que contradiz a normalização. Uma versão anisotrópica da desigualdade de Gagliardo–Nirenberg cuida das estimativas em dimensão alta.

Aqui entra uma nota pessoal. Em 2022, Roger, Gleison e eu publicamos um artigo sobre estabilização para equações de Kadomtsev–Petviashvili de ordem alta e de Zakharov–Kuznetsov em duas dimensões, no *Evolution Equations and Control Theory*. Lá deixamos registrada, numa observação, uma restrição que não sabíamos como remover. O artigo de Dieme, Roger e Gleison diz, também numa observação, que seus resultados dão resposta completa àquela. Poucas coisas são tão gratificantes quanto ver uma pergunta que deixamos para trás ser fechada por um doutorando do próprio departamento.

### Por que isto é uma contribuição modelo

Olhe para o que esse trabalho fez, com os olhos do Projeto Bourgain. Pegou uma frase de Bourgain, do tipo que um leitor apressado aceita sem pensar, e perguntou: *isso é verdade, exatamente, e por quê?* Encontrou o ponto em que o argumento de uma dimensão quebra, a perda de monotonia. Inventou o conserto, a ordem coordenada a coordenada. E escreveu tudo. É exatamente o que a política de exatidão do projeto pede: quando um passo não pode ser verificado, dizer isso com clareza; e, quando possível, completá-lo.

Uma exposição do artigo de 1997 para o Projeto Bourgain poderia ter três camadas: o argumento linear via Paley–Wiener, que cabe numa página; o lema da página 440 em uma dimensão, com todos os detalhes; e, como apêndice, a versão $n$-dimensional, com o caso da ZK como exemplo trabalhado. O núcleo combinatório do lema, a redução ao eixo, me parece até um bom candidato a formalização em Lean, que é outra das formas de contribuição que o projeto acolhe.

Quase trinta anos separam o parágrafo de Bourgain da tese de Dieme. Não acho que seja um atraso. É o tempo normal da digestão.

## Digerir, numa época de abundância

Volto ao começo. No texto sobre o 6 de outubro, a pergunta que me incomodava era: o que é o trabalho de um matemático quando uma máquina escreve, numa noite, centenas de manuscritos?

O Projeto Bourgain sugere uma resposta que não depende de vencer as máquinas na produção, uma competição que provavelmente já perdemos. Ela consiste em lembrar que a matemática nunca foi só a produção de enunciados verdadeiros. Os artigos de Bourgain estiveram corretos desde 1993. Mas os espaços $X^{s,b}$ só se tornaram parte do patrimônio comum quando dezenas de pessoas os desmontaram, peça por peça, e os remontaram em textos como o de Andreia Chapouto. O lema da página 440 só virou um teorema em $\mathbb{R}^n$ quando alguém, em Teresina, levou a sério uma frase e a transformou numa tese.

Se em breve tivermos demonstrações que ninguém compreende, como previu Tsimerman, alguém vai ter de compreendê-las. Esse trabalho tem nome, tem método e, agora, tem um lugar para ser feito em comunidade. A obra de Bourgain é um ótimo campo de treino: são mais de quinhentos artigos à espera, escritos por um ser humano que pensava mais depressa do que escrevia.

Aos alunos e colegas que me leem daqui do Piauí: escolham um artigo. Há Bourgain para todas as áreas.

## Referências e leituras

**O projeto**

- The Bourgain Project. [bourgain-pedia.com](https://bourgain-pedia.com/); páginas [*About*](https://bourgain-pedia.com/about.html) (objetivos, mantenedores e políticas) e [*Contribute*](https://bourgain-pedia.com/contribute) (como enviar uma exposição). Canal no [Zulip](https://bourgain.zulipchat.com).
- Liehr, L.; Ramos, J. P.; Taylor, M. [*The Bourgain Project*](https://terrytao.wordpress.com/2026/10/19/the-bourgain-project/). Texto convidado no blog *What's new*, de T. Tao, 19 out. 2026.
- [*Paper of the Future Prize*](https://amathr.org/prizes/paper-of-the-future-prize/) e a revista [*Mathematical Discourse*](https://www.mathematicaldiscourse.org/), iniciativas citadas pelo projeto como complementares.

- Ramos, J. P. *The Bourgain Project*. Palestra plenária no [7º Workshop em Equações Dispersivas Não Lineares](https://impa.br/evento/7th-workshop-on-nonlinear-dispersive-equations/), IMPA, Rio de Janeiro, 6 nov. 2026.

**Sobre Bourgain**

- Institute for Advanced Study. [*Jean Bourgain, pioneering mathematician, dies at 64*](https://www.ias.edu/news/press-releases/2019/jean-bourgain-obituary). Nota oficial de falecimento.
- Tao, T. [*Jean Bourgain*](https://terrytao.wordpress.com/2018/12/29/jean-bourgain/). Blog *What's new*, 29 dez. 2018.
- Bourgain, J. *Besicovitch type maximal operators and applications to Fourier analysis*. **Geometric and Functional Analysis**, v. 1, n. 2, p. 147–187, 1991.
- Bourgain, J.; Katz, N.; Tao, T. *A sum-product estimate in finite fields, and applications*. **Geometric and Functional Analysis**, v. 14, n. 1, p. 27–57, 2004.

**Espaços de Bourgain e o método da norma de restrição de Fourier**

- Bourgain, J. *Fourier transform restriction phenomena for certain lattice subsets and applications to nonlinear evolution equations. I. Schrödinger equations*. **Geometric and Functional Analysis**, v. 3, n. 2, p. 107–156, 1993.
- Bourgain, J. *Fourier transform restriction phenomena for certain lattice subsets and applications to nonlinear evolution equations. II. The KdV-equation*. **Geometric and Functional Analysis**, v. 3, n. 3, p. 209–262, 1993.
- Chapouto, A. *Fourier Restriction Norm Method*. MIGSAA Extended Project, orientação de T. Oh e O. Pocovnicu, Edimburgo, 2018. Cap. 2 (estimativas lineares, localização no tempo, transferência), cap. 3 (Strichartz $L^4$ e $L^6$, NLS cúbica e quíntica) e cap. 4 (estimativa bilinear e contraexemplos para KdV).
- Kenig, C. E.; Ponce, G.; Vega, L. *A bilinear estimate with applications to the KdV equation*. **Journal of the American Mathematical Society**, v. 9, n. 2, p. 573–603, 1996.
- Colliander, J.; Keel, M.; Staffilani, G.; Takaoka, H.; Tao, T. *Sharp global well-posedness for KdV and modified KdV on $\mathbb{R}$ and $\mathbb{T}$*. **Journal of the American Mathematical Society**, v. 16, n. 3, p. 705–749, 2003.
- Colliander, J.; Keel, M.; Staffilani, G.; Takaoka, H.; Tao, T. [*Multilinear estimates for periodic KdV equations, and applications*](https://arxiv.org/abs/math/0110049). arXiv:math/0110049.
- Tao, T. *Nonlinear Dispersive Equations: Local and Global Analysis*. CBMS Regional Conference Series in Mathematics, v. 106. American Mathematical Society, 2006. Seção 2.6 (espaços $X^{s,b}$).

**Continuação única e estabilização**

- Bourgain, J. *On the compactness of the support of solutions of dispersive equations*. **International Mathematics Research Notices**, n. 9, p. 437–447, 1997. O lema-chave está na p. 440.
- da Silva, D. P.; de Moura, R. P.; Santos, G. N. [*On the unique continuation and stabilization for the $n$-dimensional Zakharov–Kuznetsov equation*](https://doi.org/10.1016/j.jmaa.2026.130413). **Journal of Mathematical Analysis and Applications**, v. 558, artigo 130413, 2026. Acesso aberto (CC BY). Seção 2 (Proposição 2.7, o lema de Bourgain em dimensão $n$, e Teorema 1.1) e Seção 3 (estabilização).
- de Moura, R. P.; Nascimento, A. C.; Santos, G. N. *On the stabilization for the high-order Kadomtsev–Petviashvili and the Zakharov–Kuznetsov equations with localized damping*. **Evolution Equations and Control Theory**, v. 11, n. 3, p. 711–727, 2022.
- Panthee, M. *A note on the unique continuation property for Zakharov–Kuznetsov equation*. **Nonlinear Analysis**, v. 59, p. 425–438, 2004.
- Saut, J.-C.; Scheurer, B. *Unique continuation for some evolution equations*. **Journal of Differential Equations**, v. 66, p. 118–139, 1987.
- Zhang, B. Y. *Unique continuation for the Korteweg–de Vries equation*. **SIAM Journal on Mathematical Analysis**, v. 23, p. 55–71, 1992.

**Nesta série** (todos os textos estão na [Miscelânea](/miscelanea/))

- [Da escassez à abundância: a matemática na era da IA](/posts/matematica-na-era-da-ia/), 25 jul. 2026.
- [O mar cruzado e a equação que estudei no doutorado](/posts/mar-cruzado-equacao-kp/), 25 jul. 2026.
- [Navier–Stokes (III): o que significa ser matemático na era da IA](/posts/navier-stokes-iii-o-que-significa-ser-matematico-na-era-da-ia/), 16 set. 2026.
- [Dia 6 de outubro de 2026: o dia que mudou a matemática para sempre](/posts/dia-6-de-outubro-de-2026-o-dia-que-mudou-a-matematica/), 15 out. 2026.
