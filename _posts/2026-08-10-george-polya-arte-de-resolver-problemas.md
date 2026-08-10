---
title: "George Pólya: o mestre da arte de resolver problemas"
date: 2026-08-10 10:00:00 -0300
categories: [Matemática, Miscelânea]
tags: [george polya, história da matemática, resolução de problemas, educação matemática]
math: true
description: "Retrato do matemático húngaro que ensinou o mundo a pensar — com uma anedota sobre von Neumann e um problema elegante de seu livro de Stanford."
---

Há matemáticos que ficam para a história pelos teoremas que provaram. **George Pólya** (1887--1985) ficou por algo mais raro e, à sua maneira, mais difícil: ensinou o mundo a *pensar*. Foi o grande teórico da arte de resolver problemas --- e o autor de um livro que já vendeu mais de um milhão de exemplares e é estudado até hoje por matemáticos, professores e até pesquisadores de inteligência artificial.

A pedido de um colega do Departamento, dedico este texto a ele.

## O húngaro que atravessou o século

Pólya nasceu em Budapeste em 1887, filho de judeus húngaros. Doutorou-se em 1912 sob a orientação de Lipót Fejér, e foi professor na lendária **ETH de Zurique** de 1914 a 1940. Com a ascensão do nazismo na Europa, emigrou para os Estados Unidos, onde se tornou professor em **Stanford** de 1940 a 1953, permanecendo ativo por décadas.

Sua produção matemática pura foi vasta e profunda: contribuições fundamentais em combinatória (o *Teorema de Enumeração de Pólya* leva seu nome), teoria dos números, análise numérica, probabilidade (foi ele quem cunhou o termo *passeio aleatório*, e provou o célebre teorema sobre recorrência e transiência em dimensões distintas). Fez parte, informalmente, do grupo de brilhantes cientistas húngaros da mesma geração que os americanos apelidaram de "**Os Marcianos**", tamanha era a sua genialidade --- grupo que incluía justamente um de seus alunos mais famosos em Zurique.

## A anedota de von Neumann

Esse aluno era **John von Neumann**, talvez a inteligência mais fulgurante do século XX. Pólya gostava de contar uma história sobre ele que se tornou lendária entre matemáticos. Em suas próprias palavras (traduzo livremente):

> Havia um seminário para alunos avançados em Zurique que eu lecionava, e von Neumann estava na turma. Cheguei a um certo teorema e disse que ele não estava demonstrado e que poderia ser difícil. Von Neumann não disse nada, mas depois de cinco minutos levantou a mão. Quando lhe dei a palavra, foi ao quadro-negro e escreveu a demonstração. Depois disso, fiquei com medo de von Neumann.

A anedota é deliciosa por vários motivos. Mostra a rapidez sobre-humana de von Neumann, é claro. Mas mostra também a grandeza de Pólya: um professor consagrado, sem qualquer vaidade, contando com humor uma cena em que um estudante o superou. É o retrato de um homem para quem a matemática importava mais do que o ego --- e para quem o brilho de um aluno era motivo de espanto admirado, não de ressentimento.

## Guiado pela intuição física

Pólya tinha uma visão profunda sobre como as descobertas realmente acontecem --- muito antes de a demonstração rigorosa ser escrita. Comentando a descoberta do cálculo integral por Arquimedes, ele observou:

> Acontece que uma das maiores descobertas de todos os tempos foi guiada pela intuição física.

Essa frase resume uma tese central do seu pensamento: a matemática não nasce pronta e rigorosa. Ela nasce do palpite, da analogia, da intuição --- inclusive da intuição *física*, do senso concreto de como as coisas se equilibram, fluem, se acumulam. Arquimedes "pesava" figuras geométricas na imaginação, como se fossem objetos numa balança, para descobrir suas áreas e volumes; só *depois* vinha a prova rigorosa. Para Pólya, ensinar matemática sem ensinar esse lado do palpite e da descoberta era mostrar apenas metade da disciplina --- e a metade menos viva.

## Um problema elegante do livro de Stanford

Pólya acreditava que se aprende a resolver problemas... resolvendo problemas. O exemplar que trago aqui, de número 63.2, vem de uma fonte com uma história curiosa: o **exame competitivo de matemática de Stanford**, que Pólya ajudou a criar em 1946 e que aplicou por anos a estudantes secundaristas talentosos. As questões desse exame foram depois reunidas com dicas e soluções no volume *The Stanford Mathematics Problem Book: With Hints and Solutions*, organizado por Pólya e Jeremy Kilpatrick, reeditado pela Dover em 2009 e ainda hoje uma referência para quem quer treinar o raciocínio.

O charme dessas questões --- e é aqui que se reconhece a marca de Pólya --- é que elas testam *originalidade e percepção*, não competência rotineira: pedem para conjecturar e verificar fatos, descobrir que hipóteses plausíveis podem ser falsas, e reconhecer "pistas falsas" (*red herrings*), aquelas relações óbvias nos dados que se revelam irrelevantes para a solução. O problema abaixo ilustra perfeitamente uma dessas virtudes: a de que um mesmo fato pode ter demonstrações de sabores completamente diferentes.

**O problema.** Mostre que a expressão

$$
n^2\,(n^2-1)\,(n^2-4)
$$

é divisível por $360$ para todo $n = 1, 2, 3, \ldots$

Divisível por $360$ significa: não importa qual inteiro positivo você coloque no lugar de $n$, o resultado é sempre um múltiplo de $360$. Para $n=3$, por exemplo, temos $9\cdot 8\cdot 5 = 360$ --- exatamente $360$. Para $n=4$: $16\cdot 15 \cdot 12 = 2880 = 8\times 360$. Sempre fecha. Por quê?

### Primeira solução: cinco inteiros em fila

O primeiro truque é reorganizar a expressão. Usando que $n^2-1 = (n-1)(n+1)$ e $n^2-4 = (n-2)(n+2)$, podemos reescrever tudo como

$$
n^2\,(n^2-1)\,(n^2-4) = n\cdot\big[(n-2)(n-1)\,n\,(n+1)(n+2)\big].
$$

Repare no que está dentro dos colchetes: é o produto de **cinco inteiros consecutivos**, $\;n-2,\ n-1,\ n,\ n+1,\ n+2$. Esse é o coração da solução.

Agora, a estratégia é fatorar o número $360$ e caçar cada pedaço:

$$
360 = 2^3 \cdot 3^2 \cdot 5 = 8 \cdot 9 \cdot 5.
$$

Basta mostrar que a expressão é divisível por $8$, por $9$ e por $5$ separadamente --- pois esses três números não têm fatores em comum, e então o produto deles, $360$, também divide a expressão. Vamos a cada um, usando o produto de cinco consecutivos:

- **Divisível por 5.** Entre quaisquer cinco inteiros consecutivos, um deles é obrigatoriamente múltiplo de $5$ (os múltiplos de $5$ aparecem de cinco em cinco). Logo $5$ divide o produto.

- **Divisível por 8.** Entre cinco consecutivos há pelo menos dois números pares, e um deles é múltiplo de $4$. Um múltiplo de $4$ vezes outro par já fornece o fator $4\times 2 = 8$. Logo $8$ divide o produto.

- **Divisível por 9.** Aqui entra o fator extra de $n$ que ficou fora dos colchetes. Se $n$ é múltiplo de $3$, então $n^2$ é múltiplo de $9$, e pronto. Se $n$ *não* é múltiplo de $3$, então, entre os cinco consecutivos, há dois múltiplos de $3$ (por exemplo $n-2$ e $n+1$, ou $n-1$ e $n+2$), e $3\times 3 = 9$ divide o produto.

Como a expressão é divisível por $5$, por $8$ e por $9$, e esses fatores nada compartilham, ela é divisível pelo produto $360$. $\blacksquare$

Essa é a solução "com as mãos": direta, concreta, verificando fator por fator. Funciona, mas exige atenção a vários casos.

### Segunda solução: a mágica dos coeficientes binomiais

A segunda solução é curtíssima e, para meu gosto, de uma beleza superior --- porque troca todo o trabalho de casos por uma única observação estrutural. Ela repousa sobre um fato que talvez pareça surpreendente:

> **Todo coeficiente binomial é um número inteiro.**

Lembre que o coeficiente binomial $\binom{m}{6} = \dfrac{m(m-1)(m-2)(m-3)(m-4)(m-5)}{6!}$ conta de quantas maneiras se escolhem $6$ objetos entre $m$. Como é uma *contagem*, o resultado é forçosamente um inteiro --- por mais que a fórmula tenha um $6! = 720$ no denominador. Essa é a arma secreta.

A ideia é mostrar que $\dfrac{n^2(n^2-1)(n^2-4)}{360}$ é sempre inteiro, escrevendo-o como uma **soma de coeficientes binomiais**. O passo engenhoso é notar que o fator solto $2n$ pode ser escrito como $(n+3) + (n-3)$. Com isso,

$$
\frac{n^2(n^2-1)(n^2-4)}{360}
= \frac{\big[(n+3)+(n-3)\big]\,(n+2)(n+1)\,n\,(n-1)(n-2)}{6!}
= \binom{n+3}{6} + \binom{n+2}{6}.
$$

E aqui a demonstração simplesmente *termina*. O lado direito é uma soma de dois coeficientes binomiais; cada um é um inteiro; a soma de inteiros é um inteiro. Portanto o lado esquerdo é inteiro --- ou seja, $360$ divide a expressão. Fim. $\blacksquare$

Não há casos, não há caça a fatores $2$, $3$ e $5$. Uma única identidade algébrica, seguida da observação de que binomiais contam coisas e portanto são inteiros, e o problema se dissolve. É o tipo de argumento que faz um matemático sorrir --- e é exatamente o que Pólya queria que aprendêssemos a enxergar: que por trás de uma conta aparentemente árida pode morar uma estrutura simples e luminosa, se soubermos procurá-la.

> **Para quem quiser conferir a identidade.** Multiplicando o numerador por $(n+3)+(n-3) = 2n$ e lembrando que $6! = 720 = 2\times 360$, o fator $2$ cancela com o $360$ e produz exatamente $6!$ no denominador. Verifiquei numericamente que $\binom{n+3}{6}+\binom{n+2}{6}$ coincide com o valor de $n^2(n^2-1)(n^2-4)/360$ para todos os $n$ testados.
{: .prompt-tip }

## *How to Solve It*: o livro que ensinou a pensar

Toda a filosofia de Pólya está condensada num livro pequeno e imortal: ***How to Solve It*** (1945), traduzido para dezenas de línguas --- incluindo o português, sob o título *A Arte de Resolver Problemas*.

O livro propõe um método em quatro fases, hoje conhecido por qualquer professor de matemática do mundo:

1. **Compreender o problema.** O que se pede? Quais são os dados? Qual a condição?
2. **Elaborar um plano.** Já vi um problema parecido? Existe um problema mais simples relacionado? Posso usar uma analogia?
3. **Executar o plano.** Levar adiante os passos, verificando cada um.
4. **Examinar a solução (o "retrospecto").** O resultado faz sentido? Há outro caminho? O que aprendi que serve para o futuro?

Parece simples --- e é justamente essa a genialidade. Pólya destilou o que os grandes solucionadores fazem intuitivamente num roteiro que qualquer pessoa pode seguir e praticar. Suas máximas viraram provérbios da matemática: *"se você não consegue resolver um problema, então existe um problema mais fácil que você consegue: encontre-o"*; ou *"o melhor das ideias é prejudicado pela aceitação acrítica e floresce sob o exame crítico"*.

A influência do livro é imensa e transbordou a sala de aula. Ele é objeto de incontáveis monografias, dissertações e teses em educação matemática. Inspirou gerações de professores a ensinar *processo*, não apenas resultado. E, numa reviravolta que Pólya certamente apreciaria, seu método heurístico influenciou até a pesquisa em **inteligência artificial** --- os primeiros programas que tentavam "resolver problemas" de forma geral se inspiraram diretamente nas fases que ele descreveu.

## Um legado que permanece

George Pólya faleceu em 1985, aos 97 anos, em Palo Alto. Deixou teoremas com seu nome, é verdade. Mas seu maior legado não é um teorema: é uma *atitude* diante do desconhecido. A convicção de que resolver problemas é uma arte que se pode aprender e ensinar; de que a intuição e o palpite têm dignidade matemática; de que por trás de toda demonstração rigorosa há uma história de tentativa, analogia e descoberta que merece ser contada.

Num tempo em que máquinas começam a gerar demonstrações, a mensagem de Pólya fica, se possível, ainda mais atual. Porque ele nunca reduziu a matemática a produzir provas. Para ele, o que importava era *entender* --- e o entendimento, esse, continua sendo a mais humana das artes.

Como ele mesmo escreveu, num conselho que carrego para dentro de cada sala de aula:

> Nada é mais importante do que ver as fontes da invenção que são, na minha opinião, mais interessantes do que as próprias invenções.

## Referências

- PÓLYA, George. *How to Solve It: A New Aspect of Mathematical Method*. Princeton: Princeton University Press, 1945. (Edição em português: *A Arte de Resolver Problemas*, Interciência.)
- PÓLYA, George; KILPATRICK, Jeremy. *The Stanford Mathematics Problem Book: With Hints and Solutions*. Nova York: Dover Publications, 2009. (Problema 63.2.)
- PÓLYA, George. *Mathematical Discovery: On Understanding, Learning, and Teaching Problem Solving*. Nova York: Wiley, 1962.
- A anedota sobre von Neumann e as citações de Pólya são reproduzidas em coletâneas como o Wikiquote e registros biográficos do autor.
