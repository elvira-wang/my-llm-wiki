---
title: "SUPORTE MAGIC do Chitubox EXPLICADO Como o Software Cria os Suportes da Impressão 3D"
source: "https://www.youtube.com/watch?v=sMR-pvOA8Nk"
author:
  - "[[Dr. Celso Adami | Odontologia Digital]]"
published: 2026-03-12
created: 2026-07-14
description: "Neste vídeo nós entramos profundamente em uma das ferramentas mais interessantes — e também mais mal compreendidas — do **Chitubox: a aba Support Magic**.Muita gente acredita que o Support Magic é a"
tags:
  - "videos"
---
![](https://www.youtube.com/watch?v=sMR-pvOA8Nk)

Neste vídeo nós entramos profundamente em uma das ferramentas mais interessantes — e também mais mal compreendidas — do \*\*Chitubox: a aba Support Magic\*\*.  
  
Muita gente acredita que o Support Magic é apenas um botão automático que cria suportes de forma aleatória. Mas a realidade é completamente diferente. O que existe ali é um \*\*sistema automatizado baseado em estratégia estrutural\*\*, onde você pode ensinar o software a construir a arquitetura de sustentação da peça de forma organizada e inteligente.  
  
Quando entendemos como essa ferramenta funciona, deixamos de usar apenas o modo automático e passamos a \*\*programar o comportamento estrutural da impressão 3D\*\*.  
  
Neste vídeo eu explico de forma clara e didática como funciona toda a lógica por trás do \*\*Support Magic no Chitubox\*\*, mostrando como o software analisa a geometria da peça, identifica regiões críticas e distribui suportes automaticamente com base em critérios técnicos.  
  
O sistema é capaz de:  
  
• Detectar \*\*overhangs e ângulos críticos\*\*  
• Identificar regiões que começam no ar  
• Distribuir suportes automaticamente  
• Aplicar diferentes estratégias estruturais  
• Refinar a estrutura em múltiplas etapas  
  
Mas o ponto mais importante é entender que o Support Magic não trabalha apenas com um único cálculo. Ele funciona através de \*\*etapas sequenciais chamadas de passos\*\*.  
  
Cada passo representa uma fase da estratégia de geração de suportes. O software executa essas etapas em sequência, analisando a peça repetidamente e refinando a estrutura a cada nova análise.  
  
Ou seja, não é repetição — é \*\*engenharia estrutural aplicada à impressão 3D\*\*.  
  
No vídeo você vai entender:  
  
• O que é exatamente a tela \*\*Support Magic\*\*  
• Por que existem \*\*Passo 1, Passo 2, Passo 3 e Passo 4\*\*  
• Como o software executa essas fases em sequência  
• Por que peças complexas podem exigir múltiplos passos  
• Como cada etapa refina a estrutura da impressão  
  
Também explico as diferenças entre os modos:  
  
\*\*Basic, Advanced e Pro\*\*  
  
Esses modos não mudam o conceito do Magic Support, mas alteram o nível de controle que o usuário tem sobre o algoritmo.  
  
• \*\*Basic\*\* – modo simplificado para fluxo rápido  
• \*\*Advanced\*\* – controle técnico intermediário  
• \*\*Pro\*\* – nível máximo de engenharia estrutural  
  
Além disso, abordamos em detalhes os três parâmetros principais que existem dentro de cada passo:  
  
\*\*1️⃣ Parâmetro de suporte\*\*  
Define a resistência estrutural da etapa.  
  
Light  
Middle  
Heavy  
  
\*\*2️⃣ Modo de detecção automática\*\*  
Define como o software identifica áreas críticas.  
  
Normal  
+Saliência  
Mesa  
  
\*\*3️⃣ Tipo de suporte automático\*\*  
Define a arquitetura estrutural do suporte.  
  
Filial  
Articulação  
Adaptativo  
Vertical  
Pilar pequeno  
  
Cada um desses modos possui uma função estrutural específica e altera completamente o comportamento da geração automática de suportes.  
  
Também falamos sobre as \*\*configurações globais da ferramenta\*\*, incluindo:  
  
• Tipo de jangada (raft)  
• Espessura da base estrutural  
• Contraventamento cruzado  
• Mesclagem de suportes  
  
Essas opções influenciam diretamente a \*\*estabilidade da impressão, consumo de resina e facilidade de remoção dos suportes\*\*.  
  
Para quem trabalha com \*\*impressão 3D em resina na odontologia digital\*\*, entender esse sistema faz muita diferença. Guias cirúrgicos, modelos odontológicos, provisórios e peças técnicas possuem geometrias complexas que exigem uma estratégia estrutural bem definida.  
  
Neste vídeo você vai perceber que o Support Magic não é simplesmente um recurso automático — ele é um \*\*sistema de engenharia automatizada aplicado à impressão 3D\*\*.  
  
Quando entendemos a lógica por trás dessa ferramenta, deixamos de apertar botões aleatórios e passamos a \*\*controlar o comportamento da impressão com muito mais previsibilidade\*\*.  
  
Se você trabalha com \*\*Chitubox, impressão 3D em resina, odontologia digital, guias cirúrgicos ou prototipagem técnica\*\*, este vídeo vai ajudar a compreender melhor como o software pensa e como utilizar essa ferramenta de forma mais estratégica.  
  
No final do vídeo você também verá exemplos práticos de estratégias de geração de suportes que podem ser aplicadas em \*\*modelos odontológicos, guias cirúrgicos e peças complexas impressas em resina\*\*.  
  
Entender suportes é entender a base estrutural da impressão.  
  
E quando você entende a estrutura, você controla o resultado.

## Transcript

**0:00** · Muito bem, pessoal. Eu fiz um vídeo explicando sobre o centro de suporte, que é uma aba nova que a gente tem. E lá nessa aba nova eu vou entrar aqui no meu shutobox para mostrar para vocês centro de suporte. E a gente explicou sobre a aba suporte. Agora a gente tem uma outra aba aqui que se chama suporte \[música\] mé, que são outras configurações que a gente tem que fazer.

**0:23** · Aqui não é simplesmente um botão de automático. Aqui a gente tá programando a estratégia estrutural da pressão. E esse suporte médico, ele é um sistema automatizado, inteligente, que ele detecta os overhangs, ele analisa ângulos críticos, ele distribui esses suportes automaticamente, ele aplica densidade de forma estratégica, ele é mais rápido, a gente consegue repetir mais facilmente, mas menos preciso do

**0:48** · que o suporte manual em casos que são críticos. odontologia, especialmente para guias cirúrgicos e provisórios mais delicados, eu ainda prefiro usar o modelo tradicional que eu tenho mais controle, mas entender o médico é entender como o software pensa. E o que que é essa tela do suporte médic? A tela é um gerador automático em múltiplas etapas. \[música\] Ele é diferente do botão automático simples. Aqui a gente cria uma estratégia em camadas. Ele define a ordem de aplicação, ele define o tipo estrutural. Ele vai controlar como que o algoritmo identifica áreas críticas.

**1:18** · E falando em outras palavras pra gente entender, a gente tá ensinando o software como construir estrutura. E se a gente olhar aqui, eu vou pra tela do computador, vou mostrar para vocês aqui como funciona no suporte médic. A gente tem passos nessa aba de menos e nessa aba de mais, a gente aumenta ou diminui o número de passos que eu quero trabalhar. As configurações globais que a gente tem, elas ficam na direita, que é o tipo de base. Então, o tipo da jangada, o tipo de raft, skate, grade cruzada, hexagonal e a grossura disso.

**1:49** · E também o contratravamento cruzado. E a gente pode também mesclar suportes, a gente pode ativar ou desativar. Eu diria pr vocês deixarem ativados aqui esses botões. E o software ele executa exatamente na ordem que a gente falou, passo a passo. E se você entender isso, o Mic suport ele vai deixar de parecer uma repetição, ele vai fazer configurações passo a passo como uma estratégia, vai organizar isso de uma forma bem clara. E por que que esses passo a passo parecem iguais?

**2:20** · Porque estruturalmente eles têm os mesmos três campos, \[música\] que seria o parâmetro de suporte, o modo de detecção e o tipo estrutural. Mas eles não fazem a mesma coisa, eles executam em sequência. Cada passo é uma camada de decisão. E o que que muda de um passo pro outro? Seria a ordem. O Mic funciona assim, ele executa o passo um, depois o passo dois, depois o três e assim por diante.

**2:46** · Cada passo atua sobre o que ainda não foi resolvido no passo anterior, fazendo uma analogia simples. O passo um seria a fundação, o passo dois, a estrutura principal, o passo três, um reforço secundário e o passo quatro, como se fosse um acabamento. \[música\] Eles parecem todos iguais. Todos usam o concreto, mas tem funções diferentes. E como que o software pensa? No passo um, ele analisa toda a peça, ele coloca suportes conforme aquela estratégia.

**3:13** · No passo dois, ele vai analisar novamente, mas agora ele vai ignorar o que já foi resolvido. Ele procura áreas que ainda precisam de suporte. E o passo três faz o mesmo, vai refinando passo a passo. E por que que a gente tem que ter 1, 2, 5, 10 passos? Porque a gente pode querer diferentes níveis de refidamento. Passo um é simples e rápido. Então eu vou dar como exemplo. Eu vou usar o passo um como middle mais normal, mais adaptativo. Vai resolver 80% das peças.

**3:44** · Ele é rápido, ele tem pouco processamento, mas ele fica menos refinado. Se eu tiver dois passos, ele tem uma estratégia básica profissional.

**3:52** · Passo um, por exemplo, eu coloco como Rev saliência. Ele \[música\] segura essas áreas críticas. O passo dois, middle e normal. Ele vai distribuir a sustentação geral, mais segurança, melhor distribuição. E se eu tiver, por exemplo, cinco passos ou mais, é nível engenharia. Você pode separar ilhas iniciais, overrang agressivo, áreas verticais, bordas finas, reforço estrutural e uma finalização estética.

**4:17** · Quanto mais espaços eu tiver, mais controle, mais refinamento, mas eu vou demorar mais tempo de cálculo e a gente vai ter mais trabalho e vai ser mais complexo a gente configurar. E o conceito mais importante disso, os passos não são repetição, eles são camadas estratégicas. O médico funciona assim: identificação, estrutura e refinamento, depois acabamento. E você pode parar em qualquer etapa. Na prática da odontologia, modelo simples, um ou dois passos resolvem. Guia cirúrgicos, três passos seria o ideal.

**4:47** · Peças complexas ou inclinadas, três a quatro passos fazem uma diferença real. Agora eu vou explicar aqui no meu computador como funciona. Dentro de cada passo, a gente tem parâmetro de suporte, modo do suporte automático e tipo de suporte automático. Eu vou explicar um por um. A primeira aba que aparece aqui seria o parâmetro do suporte. A gente pode colocar ele como light, mirror ou have.

**5:12** · Esse campo ele vai definir qual perfil estrutural tá sendo usado naquela fase.

**5:16** · Não, não significa qualidade, significa a resistência estrutural. No pesado é pilares mais grossos, maior diâmetro, mais retenção, vai marcar mais. Indicado para peças muito pesadas. Peças médias vão equilibrar força e marca e o light seria mais fino, marca menos, peças mais leves e mais fácil de remover os suportes. Esse campo ele responde a pergunta: qual força estrutural seria aplicada nessa etapa. A outra aba que a gente tem seria o modo de suporte automático.

**5:46** · Ele vai se dividir em normal, mesa ou saliência. Esse campo, ele vai definir como o algoritmo identifica onde coloca cada suporte. Ele não altera o tipo de suporte, ele altera o critério de detecção geométrica. No modo normal, o software analisa o ângulo \[música\] crítico do overhang, áreas que começam no ar e geometrias inclinadas além do limite definido. É o que analisa padrão baseado em inclinação, indicado para modelos mais simples e peças com poucas saliências.

**6:15** · No modo saliência, além de análise por ângulo, ele também procura pontas projetadas, bordas finas, regiões mais estreitas e \[música\] áreas que saltam para fora. Ele é o modo mais agressivo, ideal para geometrias mais complexas, peças muito detalhadas, ele aumenta a proteção estrutural. E no modo mesa, ele muda completamente a lógica. O modo mesa prioriza a conexão estrutural com a plataforma de pressão.

**6:40** · Ele força suportes que descem direto até a mesa, dá preferência para trajetórias \[música\] mais verticais e ele vai evitar suportes inclinados excessivamente. Vai priorizar a estabilidade global da peça, ou seja, ele pensa primeiro na fixação à base. E quanto que a gente tem que usar esse suporte \[música\] de mesa?

**7:00** · Peças muito altas, peças com centro de mesa deslocado, impressões pesadas e quando já teve falha por descolamento, ele reduz o risco de ter um torque lateral, um descolamento inicial e uma vibração estrutural. Você pode falar sim: normal, analisa inclinação, saliência procura pontas agressivas, mesa pensa em fixação com base na impressora. Se pensarmos assim, fica muito claro qual temos que utilizar.

**7:29** · A próxima aba seria o tipo de suporte automático, que na verdade ele é como o suporte vai ser desenhado estruturalmente. Esse campo ele vai definir a geometria e o comportamento estrutural na verdade do suporte que vai ser gerado automaticamente naquele passo. Ele não vai definir onde o suporte nasce, ele vai definir como ele será construído. Ele vai responder a pergunta: qual será o desenho estrutural do nosso suporte? E se a gente clicar aqui, ele vai dividir em filial, articulação, adaptativo, vertical ou pilar pequeno.

**8:00** · Filial é o modo que cria suportes ramificados. E o que que acontece aqui nesse tipo de suporte? É um suporte que nasce da base. Ele pode se dividir em ramificações menores e vários pontos podem ser sustentados por uma mesma coluna. É como uma árvore estrutural. E qual a vantagem disso? Ele vai reduzir o número total de pilares, vai economizar material, vai dar uma estrutura mais orgânica para esse suporte e vai ter uma boa distribuição de força.

**8:25** · Mas também ele pode concentrar uma tensão na coluna principal e se ele falhar na base, ele pode comprometer vários pontos. É indicado para peças médias, modelos inclinados e quando se quer otimizar o consumo da resina. No modo articulação, o suporte cria conexões intermediárias articuladas. Ele pode criar pontos de junção entre esses suportes, vai permitir pequenas angulações, vai distribuir as tensões em múltiplos pontos e ele é uma estrutura com nós estruturais.

**8:54** · E a vantagem é que ele tem uma excelente distribuição de tensão, vai trazer menor risco de torque lateral, vai trazer uma boa estabilidade nas geometrias mais complexas, mas também traz mais complexidade estrutural, pode ser mais difícil de remover e vai ser indicado para peças muito curvas. estruturas orgânicas, impressões inclinadas mais complexas. E o modo adaptativo seria um modo inteligente e dinâmico.

**9:21** · Esse suporte ele ajusta o ângulo automaticamente, ajusta o comprimento, ele pode inclinar e pode mudar a trajetória. Ele vai tentar reduzir a altura desnecessária, um torque lateral e um consumo excessivo de resina. A vantagem é que traz uma melhor distribuição da força, menos alavanca, uma estrutura mais eficiente e é o modo mais equilibrado entre todos eles.

**9:50** · \[música\] Ideal para guias cirúrgicos, modelos inclinados e impressões mais técnicas. O modo vertical, ele tem suportes que descem reta até a base, sem adaptação dinâmica. É uma estrutura bem simples. Quais são as vantagens? Ele é previsível, é fácil de entender, fácil de remover, mas traz como desvantagens que ele pode criar pilares muito longos

**10:12** · e pode nos trazer mais torque lateral na hora da impressão e pode consumir mais resina quando a gente tiver peças inclinadas. indicado para peças mais simples, modelos pouco inclinados e um fluxo mais rápido. E a última aba que a gente tem é o pilar pequeno, que ele cria colunas mais finas que nos trazem um menor diâmetro, uma estrutura mais delicada, menos consumo. E as vantagens são: menor marcação, melhor acabamento, ideal para detalhes, mas traz como desvantagem uma menor resistência e pode falhar em em peças com pesos excessivos.

**10:46** · indicado para áreas estéticas, bordas e finalização estrutural. Para resumir tudo que eu falei na odontologia, como é que a gente pode trabalhar modelos odontológicos? Passo um, mirror normal e adaptativo. Passo dois, light normal e vertical. em guias cirúrgicos. Passo um, Revaliência e adaptativo. Passo dois, mirror normal e adaptativo. E passo três, light normal e pilar pequeno.

**11:17** · Quando a gente entende isso tudo, a gente deixa de apertar os botões automaticamente. A gente começa a projetar uma estrutura pra nossa impressão. O médico enganando a gente, ele não é mágica, ele é engenharia automatizada. E quando você entende dessa engenharia, você controla o resultado. E aí, pessoal, consegui explicar direitinho uma forma de você gerar seus suportes de um modo mais simples, mais prático e com menos erros.

**11:46** · Eu acredito que o Shitbox nos trouxe o suporte automático pra gente poder configurar nossos suportes passo a passo, problema a problema. Isso é fantástico. Às vezes a gente quer colocar suportes mais pesados e a gente erra em partes mais finas da peça.

**12:02** · Ou a gente quer colocar suportes muito finos e as peças acabam desgrudando. que aqui a gente consegue adaptar pedaço ou parte da nossa peça por parte, utilizando suportes, utilizando formas de desse suporte entrar na nossa peça, fazendo tudo isso de uma forma muito personalizada, mas já deixando isso pré-configurado no nosso software. Eu acredito que isso é uma grande atualização, é uma forma da gente pensar.

**12:34** · Claro que a gente tem que entender tudo isso para poder trabalhar com o centro de configuração desses suportes, mas isso com o tempo vai ser mais fácil, ser mais simples e vai levar a gente a muito menos erros nas nossas impressões. Se você tem algum comentário quanto a isso, alguma dúvida, se você já tinha visto esse central de suporte, não tinha entendido, deixe lá nos comentários. Eu espero que a gente possa aprender juntos e cada vez mais trazer a odontologia digital \[música\] pro nosso consultório, pra nossa clínica, pro nosso laboratório.

**13:04** · Deixe seu like, não se esqueça de se inscrever no canal, ative as notificações para trazer vídeos todas as terças e quintas aqui no nosso canal. Até \[música\] mais.

**13:19** · \[música\] เฮ