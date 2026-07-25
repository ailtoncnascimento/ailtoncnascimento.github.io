---
title: "O mar cruzado e a equação que estudei no doutorado"
date: 2026-07-25 09:00:00 -0300
categories: [Matemática, Miscelânea]
tags: [kadomtsev-petviashvili, ondas, edp, doutorado]
math: true
image:
  path: /assets/img/kp-cover.png
  alt: Mar cruzado na Île de Ré, com a equação de Kadomtsev–Petviashvili.
description: Sobre um padrão perigoso de ondas oblíquas, a equação que o modela, e o hábito de procurá-lo toda vez que vou à praia.
---

Existe um padrão de ondas que, uma vez que você aprende a enxergar, não consegue mais deixar de procurar. Chama-se **mar cruzado** (*cross sea*), e acontece quando dois sistemas de ondas que viajam em ângulos oblíquos se encontram e se sobrepõem, formando aquele xadrez inconfundível na superfície da água.

A foto acima, tirada perto do farol de Phares des Baleines, na Île de Ré (França), é o exemplo mais famoso do fenômeno — e é bela justamente pela regularidade geométrica que emerge do aparente caos do mar.

É bela, mas é perigosa. O mar cruzado está associado a condições de navegação traiçoeiras: os dois trens de onda somam suas amplitudes de forma irregular, dificultam a leitura da superfície e podem gerar ondas anômalas. Boa parte dos naufrágios em certas condições de mar acontece exatamente nesses padrões.

## A matemática por trás

O que me fascina é que esse desenho na água tem uma equação — e é uma que conheço de perto. A interação dessas ondas oblíquas é modelada pela **equação de Kadomtsev–Petviashvili (KP)**:

$$
\partial_x\!\left(\partial_t u + u\,\partial_x u + \epsilon^{2}\,\partial_{xxx}u\right) + \lambda\,\partial_{yy}u = 0 .
$$

Ela é uma generalização bidimensional da célebre equação de Korteweg–de Vries (KdV), que descreve ondas propagando-se essencialmente numa direção. A KdV vive numa reta; a KP acrescenta a variável transversal $y$, e é justamente esse termo $\lambda\,\partial_{yy}u$ que permite descrever ondas que se cruzam em ângulo — a física do mar cruzado.

O sinal de $\lambda$ divide a equação em duas famílias com comportamentos bem distintos, a **KP-I** e a **KP-II**, conforme a tensão superficial seja forte ou fraca. Essa diferença de sinal, que parece um detalhe, muda completamente a estabilidade das ondas e a estrutura matemática do problema — é uma daquelas situações, comuns em EDPs dispersivas, em que trocar um sinal troca o universo inteiro.

## Uma lembrança de tese

A KP foi uma das equações que estudei no meu doutorado no IMPA. Trabalhei com propagação de regularidade para modelos dispersivos em duas dimensões, e a família KP estava no coração daquilo — entender como a suavidade de uma solução se espalha, ou se preserva, ao longo do tempo e do espaço.

Por isso tenho por essa equação um carinho que vai além do profissional. Ela é, para mim, um elo entre o quadro-negro e o mundo: a prova de que aqueles símbolos que manipulei por anos descrevem algo que se pode ver, tocar e — no caso do mar cruzado — respeitar.

Confesso o hábito: toda vez que vou à praia, fico procurando o padrão de ondas oblíquas se formando perto da arrebentação. 😍 É raro ver o xadrez perfeito da Île de Ré, mas versões modestas aparecem com frequência, quando a ondulação local encontra uma ondulação vinda de longe. Quando acontece, é difícil não sorrir — é a minha equação favorita, desenhada na água, de graça, só para quem sabe olhar.
