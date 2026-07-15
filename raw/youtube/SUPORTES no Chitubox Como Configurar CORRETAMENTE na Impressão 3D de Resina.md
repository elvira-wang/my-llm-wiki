---
title: "SUPORTES no Chitubox Como Configurar CORRETAMENTE na Impressão 3D de Resina"
source: "https://www.youtube.com/watch?v=udmS9AVx-wg"
author:
  - "[[Dr. Celso Adami | Odontologia Digital]]"
published: 2026-03-10
created: 2026-07-14
description: "A impressão 3D em resina se tornou uma das tecnologias mais importantes dentro do fluxo digital moderno. Hoje ela está presente em diversas áreas, como odontologia digital, engenharia, design de produ"
tags:
  - "videos"
---
![](https://www.youtube.com/watch?v=udmS9AVx-wg)

A impressão 3D em resina se tornou uma das tecnologias mais importantes dentro do fluxo digital moderno. Hoje ela está presente em diversas áreas, como odontologia digital, engenharia, design de produtos, prototipagem rápida e fabricação de peças técnicas de alta precisão. No entanto, apesar da evolução das impressoras e dos materiais, ainda existe um ponto crítico que continua gerando dúvidas para muitos usuários: \*\*a configuração correta dos suportes de impressão\*\*.  
  
Em impressoras 3D que utilizam tecnologias como \*\*LCD, DLP ou SLA\*\*, o objeto não é construído simplesmente apoiado sobre a mesa. A peça é formada camada por camada enquanto é puxada para cima do tanque de resina. Isso significa que, durante a impressão, muitas regiões do modelo ficam literalmente suspensas no ar até que novas camadas sejam adicionadas. É exatamente nesse momento que entram os \*\*suportes de impressão\*\*, estruturas fundamentais para garantir a estabilidade da peça durante todo o processo.  
  
Sem suportes adequados, a impressão pode apresentar diversos problemas, como deformações, falhas estruturais, deslocamento de camadas, perda de detalhes ou até mesmo a completa falha da peça. Muitas vezes o usuário acredita que o problema está na resina, na impressora ou nos parâmetros de exposição, quando na realidade a causa está simplesmente em uma estratégia incorreta de suportes.  
  
Neste vídeo eu explico de forma detalhada \*\*como funciona a aba de suportes do Chitubox\*\*, um dos softwares de slicing mais utilizados no mundo para impressão 3D em resina. O Chitubox é amplamente utilizado por usuários de diversas impressoras, incluindo marcas como Elegoo, Anycubic, Phrozen e muitas outras, sendo um dos programas mais populares para preparar arquivos antes da impressão.  
  
Durante o vídeo nós analisamos a interface da aba \*\*SUPPORTS\*\*, entendendo exatamente o que cada ferramenta faz e como cada configuração influencia no resultado final da impressão. Muitas pessoas utilizam apenas o botão de \*\*Auto Supports\*\*, deixando o software gerar automaticamente todos os suportes necessários. Embora isso possa funcionar em algumas situações, confiar apenas na automação nem sempre gera o melhor resultado.  
  
Entender a lógica estrutural dos suportes é essencial para quem deseja obter impressões consistentes e de alta qualidade. Neste vídeo eu explico as diferenças entre os perfis \*\*Light, Medium e Heavy\*\*, mostrando em quais situações cada tipo de suporte deve ser utilizado e como esses perfis alteram a resistência estrutural das hastes de sustentação.  
  
Também discutimos parâmetros importantes como \*\*diâmetro da ponta de contato, espessura do pilar, densidade de suportes, base estrutural e distribuição estratégica dos suportes na peça\*\*. Cada um desses fatores tem impacto direto na estabilidade da impressão, na facilidade de remoção dos suportes após a impressão e na qualidade superficial final da peça.  
  
Outro conceito importante que abordamos é o das chamadas \*\*ilhas de impressão\*\*, que são regiões do modelo que aparecem antes de terem qualquer suporte estrutural abaixo delas. Essas ilhas são uma das principais causas de falhas na impressão 3D em resina, e identificar esses pontos no modelo é fundamental para garantir uma impressão bem-sucedida.  
  
Ao compreender melhor o funcionamento da aba de suportes do Chitubox, você passa a ter muito mais controle sobre o processo de fabricação digital. Isso permite não apenas reduzir falhas de impressão, mas também otimizar o uso de resina, diminuir o tempo de pós-processamento e melhorar a qualidade final das peças produzidas.  
  
Esse conhecimento é especialmente importante para quem trabalha com \*\*odontologia digital\*\*, onde a precisão dimensional e a integridade estrutural das peças são essenciais para aplicações clínicas. Modelos odontológicos, guias cirúrgicos para implantes, provisórios, placas oclusais e dispositivos personalizados dependem diretamente de um fluxo de impressão confiável e previsível.  
  
Neste vídeo eu mostro exemplos práticos e explico de forma clara e objetiva \*\*como interpretar as configurações da aba de suportes do Chitubox\*\*, ajudando você a entender não apenas como usar o software, mas principalmente a lógica por trás da construção das estruturas de suporte.  
  
Se você trabalha com impressão 3D em resina ou deseja aprimorar seu conhecimento sobre preparação de arquivos para impressão, este vídeo vai ajudar a entender um dos pontos mais importantes de todo o fluxo digital.  
  
Se esse tipo de conteúdo sobre \*\*impressão 3D, odontologia digital, scanners intraorais, softwares CAD/CAM e tecnologia aplicada à odontologia\*\* é interessante para você, aproveite para se inscrever no canal e acompanhar os próximos vídeos.

## Transcript

**0:00** · Se a tua impressão falha do nada, ou se o suporte fica impossível de remover e marca tudo, o problema quase sempre não é a resina, é a configuração do suporte.

**0:09** · Hoje eu vou te explicar item por item o centro de configuração de suporte do Chitubox, uma ferramenta que é nova. Eu não sei, mas eu acho que a última atualização ele não tinha ainda essa ferramenta e eu achei ela fantástica. As pessoas às vezes reclamam dessa nova versão do Chitubox, mas é porque não conseguem visualizar a grande vantagem e as novas opções de funções que o software nos traz. No final, você vai entender exatamente o que mexer para ganhar segurança sem estragar a peça.

**0:38** · Fica até o final desse vídeo que eu vou te explicar tudo como você tem que fazer para trabalhar e controlar a colocação dos seus suportes nas suas peças.

**0:46** · \[música\] Para a gente entender um pouquinho sobre como funciona a questão dos suportes, o que que os suportes, quais são as funções que os suportes têm na hora das impressões que a gente vai fazer.

**0:58** · Existem três funções que os suportes têm na hora que a gente vai colocar as nossas peças para imprimir. A primeira é segurar as ilhas. Quando uma impressão começa, a gente não pode começar essa impressão no ar. A gente precisa que um suporte, ele comece aquela impressão para que a peça seja impressa. Então a gente precisa o suporte \[música\] segurar para que a gente comece a impressão. Então segurar as ilhas de impressão.

**1:23** · A outra função é vencer as forças do peel force. É quando a peça, a nossa mesa entra e sai do nosso tanque, há uma força e essa força pode fazer com que essa peça se desgrude. Então os, as nossas, os nossos suportes, eles seguram essa peça para que ela não caia. E também controlar a vibração ou torque no momento de pressão.

**1:47** · Em peças muito altas e finas, a gente vai evitar o efeito banana ou efeito de curvatura que essas peças possam \[música\] ter e também fazer com que a gente não tenha micro trincas.

**2:01** · Suporte não é só segurar, ele precisa aguentar tração, deslocamento e evitar erros no no início da impressão das ilhas e ainda também estabilizar a peça durante toda a impressão. E por que que é esse suporte, se eles eles existem leves, médios e pesados? Os leves ou light, eles marcam menos, mas eles podem fazer as peças falharem. Os middle, os médios, suportes médios, eles dão um equilíbrio e eles vão ser utilizados na maioria dos casos.

**2:29** · E os suportes heavy, os suportes pesados, \[música\] eles dão uma máxima segurança, mas eles marcam mais e a gente precisa mais força para remover. Light, middle e heavy não são qualidades, são os perfis de força e impacto e a gente pode escolher conforme o risco que a gente tenha para cada área na peça. Bom, pessoal, agora vou mostrar para vocês aqui na tela do computador essa configuração de suporte nova que a gente tem aqui no Studio Box, que é fantástico. \[música\] Então, como é que a gente vai chegar para a gente poder configurar?

**2:57** · Eu vou aqui na aba de suporte e a gente clica então no centro de suporte e a mágica acontece. Tudo está aqui na nossa tela. Todas as funções que a gente pode configurar, que são inúmeras.

**3:13** · Então, eu acho que essa nova atualização ela nos trouxe muitos recursos. Claro que a gente podia mudar várias coisas, mas aqui a gente pode configurar e deixar já estabelecido eh as funções que a gente quer para as nossas impressões do do dia a dia.

**3:27** · Eh umas coisas que são importantes para a gente entender sobre a impressão \[música\] ou suportes, né, sobre os suportes da impressão 3D. Vou mostrar aqui para vocês. Aqui em cima, né, essa parte de cima a gente chama de topo.

**3:38** · Topo é onde o nosso suporte encosta na peça de impressão. A parte inferior, que seria o pé ou a plataforma, a parte principal, que seria a parte do meio do nosso suporte, a parte da jangada, que a gente traduz como jangada, mas seria a base onde ele encosta ou raft, né? A gente fala inglês no raft, que seria a parte onde ele fica encostado na mesa de impressão. E a gente tem também, entre um suporte e outro, uma coisa que a gente chama de \[música\] contraventamento cruzado ou barras entre os suportes.

**4:09** · Então, para a gente conseguir falar sobre tudo isso que eu quero explicar para vocês, a gente tem que entender. Então, seria a base, o raft ou a jangada, a a parte do principal, que seria o suporte em si, a parte do topo e a parte do pé da plataforma, que é seria o que a gente pode configurar. Então, é muito interessante a gente entender tudo isso para poder ver o que que a gente pode mudar. Aqui em cima, então, na tela do computador, a gente consegue ver que a gente poderia mudar as nossas configurações \[música\] para basic, advanced ou pro.

**4:39** · Isso são programas que a gente pode modificar e ele nos facilita. Tanto o advanced quanto o pro, eles são pagos. Então, se isso é interessante para a gente ter as vantagens que o advanced \[música\] e o pro nos trazem, então a gente acaba pagando. Quando a gente faz muita impressão, isso é muito legal e tudo que facilita o dia a dia vale a pena o investimento. Então, essa parte ela define o nível de profundidade que a gente quer acessar \[música\] no nosso software. Então, aqui eu tô trabalhando com o basic, né?

**5:07** · Então, eu tô aqui na aba de suporte e a gente consegue modificar isso tudo aqui. Logo abaixo, a gente tem, então, o tipo de suporte, que como eu falei antes, light, mirror ou heavy. E se a gente for diferenciar, no modo basic, eu não consigo, então, mexer nos parâmetros internos. E é ideal para iniciantes, para quem faz impressões simples e para quem precisa de um fluxo rápido. No advanced, a gente pode editar o diâmetro de contato, a profundidade, o pilar, a base e o ângulo.

**5:38** · E é o modo que a maioria dos profissionais deveriam usar. Aqui a gente consegue ajustar para modelo, ajustar para guia e ajustar para provisórios. Então nos facilita muito. E aqui a gente tem a aba do pró, onde a gente tem um controle total. A gente pode editar a estrutura interna do pilar, parâmetros de reforço, \[música\] a densidade estrutural e tem um algoritmo mais refinado. É praticamente

**6:03** · um modo engenharia para a gente gerar suportes. É excelente para quem quer padronizar os protocolos do laboratório, fazer peças mais difíceis, mas que tenha alguma padrão mais crítico e que é uma máxima previsibilidade. E por que que eu vou marcar light, mirror ou heavy ou marcar todos ao mesmo tempo? É que isso, o Chitubox permite usar múltiplos tipos de suporte na mesma peça. E ele separa os suportes por função estrutural.

**6:30** · Os suportes lights, eles tem pequeno diâmetro, ele tem uma pequena profundidade, mas eles fazem que a gente tenha menos marcações nas peças.

**6:39** · \[música\] Ele é usado para peças delicadas, para bordas e para pequenos detalhes. O mirror, ele é um intermediário, ele equilibra entre força e a marca. E ele é para uso geral. É muito comum para modelos odontológicos e para peças médias. E o heavy, ele é um suporte estrutural. Ele tem maior diâmetro, mais resistência \[música\] e ele é usado para base e sustentação principal de peças grandes. Ele é dedicado para peças iniciais de impressão, para áreas de grande peso e para estruturas altas.

**7:10** · E quando que a gente usa os três juntos? Quando a gente precisa de uma estrutura forte na base, um suporte intermediário no corpo e mais delicado nas áreas finas. E o algoritmo software já mistura automaticamente conforme a necessidade. Isso vai aumentar segurança, eficiência \[música\] e vai reduzir marcas desnecessárias. E para que que servem esses três pontinhos do lado de cada função? Os três pontinhos são um menu de configuração individual daquele tipo de suporte.

**7:36** · Ali a gente pode editar os parâmetros específicos, alterar o diâmetro, alterar a profundidade, ajustar a base e salvar como preset, dando a possibilidade da gente duplicar a configuração e resetar o pro padrão. Ou seja, cada tipo, light, middle ou heavy, pode ter um perfil totalmente diferente. A gente pode, por exemplo, criar um light específico pra guia cirúrgico, um middle específico pra modelo e um heavy reforçado pra bases mais longas. Isso vai transformar o Shofu Box num sistema modular de engenharia.

**8:09** · Bom, agora a gente vai mostrar todas as funções que a gente tem aqui. Vamos começar pela função de topo. Se a gente olhar aqui, a gente tem um olhinho que a gente pode \[música\] deixar ele aberto ou fechado. Quando eu deixo ele aberto, essa função vai estar \[música\] ativa. Então, se eu configurei a função, ela vai tá ativa. E se eu coloquei o olhinho, ele vai utilizar uma a função que já era pré-estabelecida do software.

**8:36** · Então, a gente utiliza ele aberto ou fechado conforme a necessidade que a gente quer. Depois disso, cada função, quando eu quero entender, \[música\] então, dentro da função topo, eu tenho várias botões que eu posso alterar. E cada um deles, se eu colocar em cima, ele vai me dar o que que é. Então, escolha a forma do segmento de suporte que entra em contato com o modelo. Nesse caso, eu posso escolher como é que esse segmento vai entrar em contato com o modelo. Então, vamos lá.

**9:01** · Explicando a forma de contato. Ele define o tipo de ponta que toca na peça, mais pontual ou mais distribuída. \[música\] E a regra é que quanto maior a área de contato, mais segura, porém mais marca.

**9:14** · E na forma de contato, eu posso escolher nenhum ou posso escolher esfera. Então, se eu colocar a esfera, a gente a gente consegue ver aqui no lado, ele já mostra, da forma de contato do nosso suporte com a peça vai ser com uma esfera. Isso é legal porque a gente consegue soltar esse suporte mais \[música\] facilmente. Então, a gente pode escolher isso. Além disso, o diâmetro do contato.

**9:36** · Isso aí é o tamanho que ele vai entrar dentro da nossa peça. Então, quanto mais a gente aumentar, mais segura, mas vai marcar mais. E se eu diminuir um pouquinho, ele vai marcar menos, mas pode soltar da peça, dependendo se ele não tiver muito em contato. Então, a gente tem que medir quanto mais eu quero segurar a peça e quanto menos eu quero marcar. O diâmetro de contato é o botão do medo. Se você vive tendo falha em ponta de cúspide, de borda fina ou peça mais alta, é bom subir o diâmetro de contato e salvar.

**10:08** · A outra função que a gente tem é a profundidade de contato.

**10:12** · Profundidade de contato é o quanto a ponta entra e se fixa na peça. Aumentar cola mais e reduz a soltura. Diminuir facilita o acabamento e a remoção. A dica é: se tá quebrando suporte na remoção, muitas vezes é profundidade alta mais um diâmetro alto. O outro botão que a gente tem aqui é a forma de conexão. E a forma de conexão é a transição do topo pro corpo. Esse cone tende a distribuir melhor a força e reduzir a quebra no pescoço. E a gente pode modificar ele pra pirâmide ou skate.

**10:45** · Isso a gente pode deixar pré-configurado. A outra função é o diâmetro superior da parte de suporte médio, que é como que ele vai entrar na nossa peça. É a espessura do pescoço logo embaixo do contato. Aumentar dá menos quebra de suporte e diminuir traz menos marcas e uma menor rigidez. A outra função aqui é o diâmetro inferior.

**11:07** · Ele continua a transição do cone pro corpo. E aumentar deixa o suporte mais robusto. E se a gente diminuir, ele fica mais flexível, daí ele pode vibrar. A outra função é o comprimento do segmento. Ele define o tamanho dos gominho dos segmentos da estrutura. Se eu fizer ele maior, ele vai ter menos conexões, então mais rápido, às vezes mais instável. E se ele for menor, mais conexões, mais rígido, a gente tem mais controle. Então a gente vê que na função de topo eu consigo ajustar como que esse suporte vai encostar na minha peça.

**11:38** · Isso é uma coisa muito importante. A gente pode modificar e já deixar isso salvo. A próxima função que a gente tem seria a função do principal. E a função principal é a rigidez desse nosso suporte. E a próxima aba é a forma da secção transversal. Aqui no nossa tela ele tá como cilindro, que é o padrão, que ele é previsível e forte. Mas eu poderia modificar ele pra prisma ou pra cubo. Então normalmente a gente trabalha com cilindro.

**12:06** · A segunda função é o diâmetro superior \[música\] da parte do suporte de suporte médio. Isso mostra na verdade a espessura do corpo lá em cima.

**12:17** · Se a gente sobe ele aguenta mais força e melhora essa estabilidade. E se a gente desce tem menos material e menos marca indireta, mas pode falhar. O outro botão que a gente tem aqui seria o diâmetro inferior, que seria a base do corpo de suporte, mais perto do pé. Se a gente sobe ele fica um poste, fica muito firme. E se a gente desce ele pode balançar, especialmente em peças mais pesadas e mais altas. O último botão que a gente tem aqui no principal seria o ângulo entre o topo e o meio. E ele controla a geometria e a transição, como o suporte abre no topo do corpo.

**12:50** · Em geral ângulos mais agressivos eles dão rigidez, mas eles podem criar pontos de tensão. Se você tem suporte quebrando no meio do caminho, o corpo precisa ficar mais robusto. Não adianta só aumentar a ponta. A próxima aba que eu vou mostrar pra vocês seria a parte inferior do nosso suporte. E a primeira aba é a forma de contato da plataforma. E a forma de contato da plataforma é o pé do suporte. Skate, como que ele tá aqui, ele tende a aumentar a área de adesão com menos concentração de tensão.

**13:21** · Eu posso modificar essa aba com skate, cone, cubo, cilindro, prisma ou não deixar nenhuma base nessa minha impressão. A outra aba seria do diâmetro de contato. E esse diâmetro de contato, ele nos dá o tamanho da base de contato na plataforma. Quanto maior, gruda mais, mas é mais difícil de remover, usa mais resina. E quanto menor, ele pode \[música\] soltar da mesa. A outra aba seria a grossura. E essa grossura seria a espessura do nosso pé. Quanto maior, menor a chance de soltar.

**13:53** · Quanto maior, mais fácil de remover. A outra aba seria o support bottom boss height. Seria o que na verdade? É o diâmetro do pé, ou seja, o reforço que a gente tem na base entre o nosso rail e o início do nosso suporte. E se a gente tiver uma base com mais diâmetro, essa base fica mais forte. O último botão que a gente tem na parte inferior seria o support bottom boss diameter. Seria na verdade o diâmetro desse reforço. Mais diâmetro, a base fica mais forte.

**14:26** · A próxima aba seria as configurações de jangada ou de rail, né? Então, quais são as funções que a gente tem aqui? A primeira função seria adicione automaticamente a jangada. É importante que a gente deixe ele ligado. Ele \[música\] cria o raft automaticamente. Depois disso, eu tenho a altura da elevação do modelo. Isso seria o lift do modelo, que tem acima da base, ou espaço para drenagem e o suporte. E quanto maior, melhor a drenagem e menos sucção.

**14:57** · Mas a gente vai precisar utilizar mais suporte, mais tempo. E quanto menor, mais compacto, mas pode prender a resina e aumentar a sucção. E a outra função aqui das nossas configurações seria a forma, seria o tipo de jangada.

**15:13** · \[música\] Então, o tipo de raft, né? Aqui você escolhe o estilo e quando for usar. Se Se clicar aqui, eu posso colocar ele como skate, como grade cruzada, grade hexagonal, fundo conectado ou estojo de proteção. Lembrando que isso são traduções que a gente tem do inglês. Então, às vezes na tradução para o português, ele não fica com o nome muito adequado, mas a gente consegue entender.

**15:38** · Se a gente colocar aqui e modificar, a gente consegue ver certinho como que isso funciona, como é que é essa base. A outra aba que a gente tem aqui seria do suporte confortável, que seria na verdade como que a gente faz para remover sem arrancar nenhum pedaço da nossa peça. Esse bloco é para equilibrar segurança com uma remoção mais limpa. E a primeira aba que a gente tem aqui seria o comprimento máximo do pequeno pilar, seria da parte interna.

**16:04** · Quando a gente tem peças circulares, a gente vai utilizar suportes para que a gente consiga imprimir essa parte interna.

**16:15** · Aqui do lado a gente pode modificar para vocês entenderem a partir desses suportes que seria que a gente traduz como pilar pequeno. Mas seria basicamente os suportes que não vem lá da nossa mesa de impressão. Como que a gente configura? O comprimento máximo do pilar pequeno, ele limita até onde esse pilar aparece antes de virar uma estrutura normal. A segunda aba seria do diâmetro, então é \[música\] a espessura desse pilar pequeno, quanto maior mais firme, mas menos confortável para remover.

**16:46** · E quanto menor é mais fácil de remover, mas a gente corre mais riscos para que essa peça imprima. Isso é muito importante a gente entender e vai ser muito relacionada com o over hang que a gente tem.

**16:59** · \[música\] Dependendo do de como que essa peça vai sendo construída, se eu tiver um cilindro, por exemplo, ele aceita até 60, 70 graus tranquilamente desse over hang. Então, não haveria uma necessidade de a gente colocar esses suportes internos. Mas eu Eu aí muita gente utilizando só suportes automáticos e isso vai acabar colocando, porque eles têm pré-configurações para provavelmente um over hang de 45.

**17:25** · Então, isso é uma questão que a gente deve entender para poder não marcar tanto as peças e que não tenhamos erros nas nossas impressões. A outra aba que a gente configura aqui seria a profundidade superior, que seria o encaixe então desse desse suporte na nossa peça. A outra configuração que a gente pode fazer seria a profundidade da extremidade inferior. Então, eu posso configurar tanto a parte superior quanto a inferior da nossa peça. A outra aba seria a forma de contato.

**17:52** · Eu posso ter um contato como nenhum contato ou de esfera, igual eu tenho lá dos suportes comuns que vem lá da nossa base e o diâmetro de contato. Então, tudo isso, né, no suporte confortável, eu posso configurar aqueles pequenos suportes que não vem lá da nossa base e que são colocados às vezes na peça para a gente poder imprimir. Para a gente explicar um pouquinho melhor isso, que tipos de contato que a gente tem no modelo? Eles podem ser nenhum, esférico, cônico ou plano, dependendo da versão que a gente utiliza do Chitubox.

**18:23** · Isso altera a ponta. Então, se a gente for pensar, quando o contato é como se fosse uma esfera, ele tem menos marca e é mais fácil da gente remover. E quando ele for plano, ele vai acabar grudando e quando a gente remover, a gente pode deixar um pouco desse suporte na peça ou acabar removendo uma parte, arrancando uma parte dessa peça. Às vezes é difícil da gente entender esse ponto de contato, mas é basicamente isso. Eu gosto muito desses contatos esféricos. Eles nos facilitam muito na hora de remover e não deixam essas marcas.

**18:51** · E a última aba desse nosso suporte confortável seria o diâmetro de contato. Então, é o tamanho da ponta que encosta no nosso modelo.

**19:00** · Ele pode ser de 0,6, que é o padrão médio, mas a gente pode, se a gente quiser, \[música\] alterar para mais ou para menos. Aqui ele já vem configurado com 0,5, mas \[roncando\] isso é de a gente fazer os testes na hora da impressão e ver qual fica melhor para as nossas peças e para qual resina que a gente vai utilizar. Na outra aba que a gente tem seria o contraventamento cruzado. Que nome estranho esse? Seria na verdade como que os suportes eles podem \[música\] entre eles se ajudar e a gente pode criar como se fosse pontes entre um suporte e outro. E quais as abas que a gente tem?

**19:31** · E na primeira aba a gente tem o bracing ou bracing cruzado automático. A gente É interessante que a gente deixe ele ligado. Que daí a gente pode em áreas com necessidade ele unir um suporte outro.

**19:45** · Ele não nos atrapalha como ele entra na nossa peça, mas ele reforça esse \[música\] suporte para que eles estejam juntos. A outra aba seria do diâmetro da estrutura cruzada. E isso aí ele mostra o quê? Ele mostra a espessura dessas barras. Quanto maior, mais estabilidade a gente vai ter entre esses suportes. A próxima aba seria da altura de partida cruzada. E isso mostra o quê? Que a partir de que altura ela começa a colocar as nossas travessas. Se nós vamos começar desde o início da impressão ou mais alto.

**20:13** · A outra aba seria o mínimo espaçamento cruzado e ele é da distância mínima vertical entre essas travessas.

**20:23** · \[música\] Próxima aba que é parecido com isso seria o máximo espaçamento cruzado. Então ele nos mostra a distância máxima horizontal para decidir onde travar. E para essa aba de contraventamento cruzado é importante a gente entender. Peça alta e fina sem contraventamento é a receita para vibração e vai fazer com que a gente tenha uma falha por fadiga.

**20:44** · Travessa é como se fosse um cinto de segurança. \[música\] A gente vai subindo os nossos suportes, se eles forem muito finos, eles podem ter alguma movimentação. E se a gente colocar essas ligações cruzadas entre suportes, a gente vai ter uma maior facilidade e uma menor chance de a gente poder ter alguma movimentação nessa peça. A próxima aba que a gente tem aqui seria a aba de configuração manual e essa parte controla como o suporte se comporta quando você coloca ele manualmente.

**21:12** · E a primeira aba seria do contraventamento bidimensional e ela cria reforços diagonais entre os pilares de suporte.

**21:21** · Isso faz com que a gente aumente a estabilidade, vai reduzir a vibração e vai diminuir o risco de falha em peças mais altas. E como eu falei, ela é muito útil para peças altas, próteses longas e e guias muito extensos. A outra aba seria do anexo automático, ele permite que o Toolbox crie conexões automáticas entre os suportes próximos, que reduz essa flexão e ele distribui melhor as forças de peel force. E os suportes \[música\] podem ficar isolados. E se isso acontecer, essas peças elas podem ter problemas na hora da nossa impressão.

**21:50** · A outra aba seria o raio de fixação e esse raio de fixação ele define que raio que a gente vai ter na nossa base de suporte do modelo. Maior raio, mais estabilidade, mas marca mais. E menor o raio, menos marca, mas a gente vai ter menos resistência. A próxima aba seria o ângulo de fixação, que ele vai definir o ângulo com que o suporte encosta no modelo. Mais inclinado tem melhor distribuição de força e menos pontos de tensão concentrados na nossa peça.

**22:19** · Então muitas vezes a gente vai fazer uma angulação para que a gente tenha menos força e essa peça imprima mais facilmente e tenha uma estabilidade maior de impressão. A próxima aba que a gente tem seria de configuração aprimorada. A gente vê que várias dessas nossas botões, eles vão só estar disponíveis. Então aqui em cima eu não falei, mas a gente tá no modo advanced.

**22:45** · Então tudo que que não tem nada, ele é do modo basic. Tudo que tá com azinho do lado é advanced e tudo que tá no P é no modo pro. Então essa configuração aprimorada que a gente tem só tá disponível no modo pro. E aqui, a primeira aba que a gente tem nessa configuração aprimorada seria o máximo deslocamento do ponto de contato. E o que que ele faz? Ele permite que o software, ele mova ligeiramente o ponto de contato automaticamente. Então, ele melhora o posicionamento e ele evita pontos muito próximos. E se a gente colocar muito alto, ele pode alterar a área crítica da peça.

**23:17** · Isso faz com que a gente tenha menos erros na nossa impressão, porque automaticamente ele se modela para que a gente tenha ajustes perfeitos na hora de imprimir. A outra aba seria a mínima altura efetiva desse suporte, funciona da mesma forma que a aba anterior, mas na parte inferior. E a última aba seria o espaçamento do modelo. E ele nos mostra a distância mínima entre os suportes. Menor valor, mais densidade, mais estabilidade. Maior valor, menos suportes e menos marcas.

**23:45** · A próxima aba seria da configuração automática e a gente tem aqui o máximo ângulo superior, então ele vai mostrar exatamente o ângulo que a gente tem para colocar na peça. Isso é crucial. Ele \[música\] define que a inclinação máxima que o software considera como auto suportável. Mas eu vou dar um exemplo, 45° seria o padrão. 30° seria quando a gente tem mais suportes e 60° seria quando a gente tem menos suportes.

**24:14** · E em odontologia, no que a gente faz aqui, a gente trabalha normalmente entre 40 e 45. Isso aí já é bastante seguro para as nossas impressões. E a próxima aba seria o espaçamento do ponto de contato, que seria a distância entre os pontos automáticos. Menor valor, ele dá mais suportes e mais segurança. E maior valor, ele traz uma impressão mais limpa, com menos riscos.

**24:38** · A próxima aba seria o espaçamento principal do nosso pilar e ele é a distância entre os pilares verticais \[música\] principais.

**24:48** · Isso controla a densidade e a estrutura geral dessa nossa impressão. A próxima aba seria suporte, ele nos traduz como suporte em cálice. Ele \[música\] cria um suporte dentro da cavidade interna. Ele é muito útil para coroas, guias e peças ocas. A próxima aba seria melhorar o suporte automático. A gente pode colocar ele como nenhum, reforço independente, reforço triangular ou reforço global. E ele ativa o refinamento do algoritmo.

**25:18** · Ele ajusta o posicionamento, evita sobreposições e corrige falhas estruturais. O exemplo que aparece aqui é quadrado, mas a gente pode colocar ele como quadrado ou circular. E na verdade o suporte quadrado ele tem uma maior distribuição regular na peça. Ele tem uma boa previsibilidade. Normalmente a gente acaba utilizando como padrão esse suporte quadrado. A próxima aba seria o modo de contato de limite, que a gente pode colocar como tangente de aresta ou centro de coincidência. E ele define como o software trata regiões de borda.

**25:52** · Ele evita colocar esses suportes em umas áreas muito finas ou margens bem delicadas. É importante, principalmente quando tem margens de preparo ou bordas muito fininhas. A próxima aba seria a aba do regular. Essa parte controla as regras básicas que o Chitubox usa para gerar e organizar esses suportes. E a próxima aba seria o máximo deslocamento do ponto de contato. E o que que é? Ele define o quanto o software pode mover automaticamente esse ponto de contato para que a gente encontre uma área de melhor fixação.

**26:21** · Na prática, quando o algoritmo identifica uma área que precisa de suporte, ele pode ajustar levemente esse ponto, deslocar \[música\] alguns milímetros, procurar uma área mais estruturalmente favorável e, por exemplo, se eu colocar 0 mm, o suporte vai exatamente onde o algoritmo detectou. Se eu colocar de 0,5 a 1, ele pode ajustar levemente para melhor retenção.

**26:45** · A gente tem que ter um cuidado um pouquinho, se deixar muito alto, a gente pode deslocar para a área estética, pode ir para uma margem do preparo, pode interferir numa área clínica. Em odontologia sempre eu recomendo valores baixos para manter mais a previsibilidade. A próxima aba seria a mínima altura efetiva do suporte. E o que que essa aba faz? Ela define a altura mínima que o suporte precisa ter para ser criado. Serve para quê? Para evitar que o suporte crie um micro suporte muito pequenininho e que seja inútil. E se for muito baixo, o Toolbox cria suportes muito curtos.

**27:17** · Eles podem nem funcionar, só aumentar as marcações da peça. E se for muito alto, ele ignora essas micro regularidades, cria suportes só estruturais. Isso ajuda muito em modelos de odontologia cheio de micro detalhes. O último botão dessa nossa aba de regular seria o espaçamento do modelo. E o que que seria esse espaçamento do modelo? Ele vai definir a distância mínima entre o suporte do modelo, controlando a densidade desse suporte, a quantidade final e a distribuição estrutural.

**27:46** · Se a gente diminuir muito, a gente cria mais suportes, tem mais segurança, mas cria mais marca. E além disso, mais consumo de resina. Se aumentar, menos suportes, a impressão fica mais limpa, mas tem mais risco de falha. Bom, pessoal, eu acho que eu consegui explicar todas as abas aqui no meu computador. Foi assim, ó, são são uma série de botões que eu posso configurar, que eu posso ajustar.

**28:11** · E a gente precisa, na verdade, fazer as impressões e testar. Tudo isso pode ser pré-configurado, pré-ajustado. A maioria das pessoas nem mexe nada nessas impressões, mas também a gente vê gente falando que tem erros. E muitas vezes eles não têm a menor ideia de onde está esse erro.

**28:28** · E configurar adequadamente esses suportes é extremamente importante para que a gente minimize esses problemas na hora de impressão. É muito comum, é muito comum a gente acabar tendo impressões que soltam da base, impressões que acabam soltando no meio dos suportes. É muito comum a gente acabar as peças e ter uma dificuldade extremamente grande de fazer um polimento e até desgastando a mais essa peça.

**28:54** · Na odontologia é muito importante a gente ter precisão, previsibilidade dessas impressões. \[música\] Quanto melhor essa nossa impressão for, mais fácil da gente trabalhar no pós-cura, mais fácil da gente conseguir não ter um trabalho de acabamento dessas nossas \[música\] peças. Então, isso tudo é importante a gente entender e cada vez mais que a gente puder modificar e aprender esses parâmetros, a gente vai fazer impressões melhores, mais lisas, mais delicadas e mais precisas.

**29:22** · Se você tem alguma dúvida, deixe nos comentários. É importante a gente trocar ideias, aprender. Não se esqueça de se inscrever no canal, deixar seu like, ativar as notificações. Todas as terças e quintas sobe um vídeo como esse no canal pra gente poder aprender tudo sobre odontologia digital. Até mais.

**29:44** · \[música\] \[música\]