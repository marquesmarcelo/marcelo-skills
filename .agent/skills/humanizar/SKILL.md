---
name: humanizar
description: Checklist obrigatório de humanização a ser aplicado em TODO texto substancial que Claude produzir — despachos, notas técnicas, ebooks, roteiros, e-mails, posts, artigos, respostas de FAQ, questões ENADE, relatórios de auditoria, etc. Baseada na página "Wikipedia:Signs of AI writing", em pesquisa acadêmica de linguística computacional sobre vocabulário excedente e métricas de detecção (perplexidade/burstiness), e em guias práticos de redatores sobre os "tells" (marcas) que denunciam texto gerado por IA. Use esta skill em conjunto com qualquer outra skill de produção de conteúdo (ebook-writer, sei-responder, lab-roteiro, elaborar-questoes, revisor-conteudo, email-faq-responder etc.) como uma passada final de revisão antes de entregar o texto — não é uma skill que se aciona sozinha, é uma camada de qualidade que se soma às demais. Ative sempre que for redigir prosa corrida em português ou inglês, mesmo que o usuário não peça explicitamente "humanize isso".
---

# Humanizar Texto

Camada de revisão que se aplica **depois** de qualquer skill de produção de conteúdo, e **antes** de entregar o texto final ao usuários. Não substitui as outras skills — soma-se a elas. Sempre que produzir prosa (não código, não dados tabulares soltos), rode este checklist mentalmente e corrija antes de mostrar o resultado.

## Por que isso existe

Vários grupos, com metodologias independentes, chegaram às mesmas conclusões sobre como texto de IA se denuncia:

- **Wikipedia (WikiProject AI Cleanup):** catalogação manual de milhares de edições sinalizadas como geradas por IA, focada em padrões retóricos e estruturais.
- **Pesquisa acadêmica de linguística computacional (Kobak et al. 2024/2025, Science Advances/arXiv; Juzek & Ward; e outras):** análise estatística de "vocabulário excedente" em mais de 14 milhões de resumos científicos do PubMed, comparando a frequência de palavras antes e depois do ChatGPT — método quantitativo, não subjetivo.
- **Métricas de detecção (perplexidade e "burstiness"):** usadas por ferramentas como GPTZero, medem previsibilidade lexical e uniformidade rítmica de frases — um padrão estrutural, não uma lista de palavras.
- **Guias práticos de redatores e agências (Beutler Ink, Forbes/William Beutler, comunidade de copywriting no Medium):** observação empírica de padrões recorrentes em textos comerciais e institucionais gerados por IA.

Essas fontes convergem porque descrevem o mesmo fenômeno por ângulos diferentes: um LLM tende a regredir à média estatística do seu corpus de treino, produzindo uma saída previsível, genérica e ritmicamente uniforme — a "voz de ninguém". Escrever bem para o usuário significa evitar esse repertório por padrão, sem que ele precise pedir.

**Importante (aviso da própria Wikipedia, vale seguir aqui):** não adianta caçar cada padrão isoladamente e cortá-lo às cegas — isso produz texto empobrecido e ainda mais artificial. O objetivo é reescrever com voz própria, específica ao conteúdo, e não apenas trocar palavras proibidas por sinônimos.

## Checklist de padrões a evitar

### 1. Paralelismos negativos ("não é X, é Y")
Evitar construções como "não é apenas um documento, é uma ferramenta estratégica" ou "não X, mas Y". IA usa isso obsessivamente para criar falsa sensação de contraste dramático. Também evitar a variante em duas frases (frase 1 afirma algo, frase 2 começa com "no entanto/contudo" contrastando).
- Ruim: "Não se trata apenas de um processo administrativo, mas de um instrumento de garantia de direitos."
- Melhor: dizer o que é, sem montar o contraste artificial.

### 2. Regra de três (rule of three) em excesso
Listas de exatamente três adjetivos, três substantivos ou três cláusulas curtas, usadas para simular profundidade ou completude onde não há. Às vezes vira "adjetivo, adjetivo e adjetivo substantivo".
- Ruim: "uma solução robusta, escalável e eficiente"
- Melhor: usar dois, quatro, ou nenhum — o número certo é o que reflete a realidade, não um hábito retórico.

### 3. Travessão (em dash) em excesso, com espaços
IA usa travessão com muito mais frequência que escritores humanos, geralmente cercado de espaços, em lugares onde uma vírgula, parênteses, dois-pontos ou hífen bastariam. Em português, preferir vírgula, dois-pontos ou parênteses na maioria dos casos; reservar o travessão para casos em que ele realmente é a melhor opção, sem espaços ao redor conforme a norma culta.

### 4. Vocabulário típico de IA
Palavras e expressões que aparecem com frequência estatisticamente anômala em texto gerado por modelo. Evitar (e seus equivalentes em português quando aplicável):
- **Inglês:** delve, intricate, tapestry, pivotal, underscore, landscape, foster, testament, enhance, crucial, boundaries, robust, seamless, leverage, showcase, highlight, emphasize, notable, significant, comprehensive, holistic, dynamic, cutting-edge, transformative, groundbreaking, paradigm, empower, unlock, elevate, journey, realm, delve, navigate, unveil.
- **Português (equivalentes que o usuário já ouve rotineiramente da IA):** "landscape/panorama abrangente", "robusto", "essencial", "fundamental" em excesso, "de forma a garantir", "desempenha um papel crucial/fundamental", "representa um marco", "consolidar-se como", "trajetória", "jornada", "cenário", "amplo espectro", "gama diversificada".
- Não é proibir a palavra para sempre — é notar quando ela está sendo usada como muleta genérica em vez de dizer algo específico.

### 5. Frases-cauda com gerúndio ("-ing"/"-ando") que inflam significado
IA gosta de encerrar frases com uma oração reduzida de gerúndio que finge estar analisando algo, mas não acrescenta informação nova.
- Ruim: "O órgão publicou a norma, reforçando seu compromisso com a transparência."
- Melhor: cortar a cauda, ou substituí-la por um fato concreto se houver um.

### 6. Falsas amplitudes ("de X a Y")
Construção que finge abranger um espectro amplo, mas na verdade só junta dois itens vagamente relacionados para soar abrangente.
- Ruim: "Nossos serviços vão do planejamento estratégico à execução operacional."
- Melhor: listar o que realmente é oferecido, com especificidade.

### 7. Resumos compulsivos ("em suma", "em conclusão", "ao final", "resumindo")
Reafirmar o que acabou de ser dito, mesmo em textos curtos que não precisam de recapitulação. Só resumir quando o texto for longo o suficiente para justificar (documentos extensos, relatórios com muitas seções).

### 8. Frases de "importância inflada" (puffery)
Comentários que exageram a relevância do assunto conectando-o a temas maiores, sem embasamento factual — comum em textos institucionais e educacionais gerados por IA.
- Ruim: "Este tema é fundamental para o futuro da administração pública brasileira."
- Melhor: deixar os fatos falarem; se a relevância for real, mostrar o motivo concreto, não declarar a importância em abstrato.

### 9. Atribuições vagas e "weasel words"
Atribuir opiniões a autoridades não identificadas ("especialistas apontam que...", "estudos mostram que...") sem citar fonte real. Se não há fonte, não inventar uma moldura de autoridade — ou citar a fonte específica, ou não fazer a afirmação.

### 10. Seção de "desafios e perspectivas futuras" genérica
Padrão de fechar textos institucionais/educacionais com um parágrafo do tipo "apesar dos avanços, ainda existem desafios..." seguido de uma frase vaga e positiva sobre o futuro. Só incluir essa seção se houver desafios reais e específicos a relatar.

### 11. Uso de "while"/"embora"/"enquanto" como conector artificial de contraste
IA usa "enquanto" ou "embora" para conectar duas ideias que não são realmente contrastantes, só para dar ares de nuance.

### 12. Formatação robótica
- Negrito em excesso, aplicado a termos-chave de forma mecânica (como se cada seção fosse um manual).
- Uso de emojis em títulos ou listas fora de contexto claramente pedido.
- Listas com marcadores para tudo, mesmo quando um parágrafo corrido comunicaria melhor.
- Títulos em "Title Case" desnecessário (em português, título deve seguir a norma culta de capitalização, só a primeira palavra e nomes próprios).

### 13. Tom promocional/institucional artificial
Texto que soa como material de marketing ou folheto turístico mesmo quando o pedido era neutro ou técnico (comum em textos sobre lugares, instituições, produtos). Manter o registro pedido — técnico permanece técnico, neutro permanece neutro.

### 14. Frases de meta-comentário desnecessário
"É importante notar que...", "vale ressaltar que...", "não se pode deixar de mencionar...". Se a informação importa, ela entra direto no texto sem o aviso prévio de que é importante.

### 15. Hedging (qualificadores em excesso)
Encher a frase de "pode", "geralmente", "em muitos casos", "tende a" quando a afirmação poderia ser direta. Usar hedge apenas quando há incerteza real a comunicar — não como reflexo defensivo.

### 16. Baixa "burstiness" — uniformidade rítmica das frases
Este é um padrão estrutural, não lexical, e é considerado o sinal mais robusto na pesquisa de detecção (mais confiável que vocabulário isolado). Escrita humana alterna frases curtas e diretas com frases longas e elaboradas, de forma irregular. Texto de IA tende a manter frases no mesmo comprimento e na mesma complexidade sintática ao longo de todo o parágrafo — um ritmo "liso" demais.
- Ao revisar, leia em voz alta (mentalmente): se todas as frases de um parágrafo têm 15-25 palavras e a mesma estrutura sujeito-verbo-objeto-complemento, quebre o padrão. Insira uma frase curta. Deixe uma mais longa quando o raciocínio pedir.

### 17. Vocabulário "excedente" identificado por pesquisa quantitativa
Estudo de Kobak et al. (2024/2025, PubMed, mais de 14 milhões de resumos) mediu estatisticamente quais palavras dispararam em frequência depois do ChatGPT. Além das já listadas no item 4, essa pesquisa aponta especificamente: boast/boasts (e "ostenta" em português), meticulous/meticuloso, notably/notavelmente, garner/angariar, showcase/showcasing, comprehensive, commendable/louvável, primarily (usado como conector de abertura de frase), notable.
- Regra prática: se uma palavra soa "de relatório de consultoria genérico" mais do que "do jeito que o usuário falaria a mesma coisa em uma reunião", trocar.

### 18. Vazamento de tom conversacional de chatbot
Aberturas e fechos típicos de assistente de chat que nunca devem aparecer em um entregável (despacho, ebook, e-mail, relatório): "Claro!", "Ótima pergunta!", "Vamos mergulhar nisso", "Espero que isso ajude!", "Se precisar de mais alguma coisa, é só avisar!", "Aqui está...". Esses são artefatos de interação, não de documento — um documento não conversa com quem lê.

### 19. Encadeamento de conectivos formais em sequência
Empilhar "além disso", "ademais", "outrossim", "adicionalmente", "nesse sentido", "dessa forma" um atrás do outro, parágrafo após parágrafo, como se o texto fosse uma apresentação de slide com transições automáticas. Usar cada conector apenas quando ele expressa a relação lógica real entre as frases — não como cola padrão entre parágrafos.

### 20. Jargão corporativo vazio ("buzzword bingo")
Expressões que soam produtivas mas não comunicam nada verificável: "soluções inovadoras", "impulsionar resultados", "agregar valor", "insights acionáveis", "solução robusta e escalável", "otimizar processos", "trazer eficiência". Comum em textos de TI/gestão — especialmente arriscado nos contextos do usuário (atividades relacionadas a TI incluindo edução, gestão, aquisições, pareceres técnicos), onde jargão vazio pode ser lido como enrolação em vez de análise.
- Trocar por: o que o processo/sistema/decisão realmente faz, em termos verificáveis.

### 21. "Apenas"/"simplesmente"/"só" como suavizador reflexo
IA usa advérbios de minimização ("apenas", "simplesmente", "só") com frequência maior que escritores humanos, muitas vezes sem necessidade, como tique de estilo. Revisar e cortar quando não alteram o sentido.

### 22. Variação elegante forçada (troca de termo técnico por sinônimo)
Para "não repetir a mesma palavra", IA troca um termo técnico por sinônimos ao longo do texto (ex.: chamar o SEI ora de "sistema", ora de "plataforma", ora de "ambiente eletrônico" no mesmo despacho). Em texto técnico e jurídico-administrativo isso é o oposto de boa prática: gera ambiguidade sobre se é a mesma coisa. Repetir o termo técnico exato é preferível a variar por estética.

## Como aplicar

1. Produza o conteúdo normalmente seguindo a skill específica da tarefa (sei-responder, ebook-writer, etc.) e as instruções do usuário.
2. Antes de entregar, releia o texto com este checklist em mente e corrija qualquer ocorrência.
3. Priorize reescrever com voz específica ao conteúdo real — não troque uma palavra-clichê por outra igualmente genérica.
4. Não exagere na correção a ponto de o texto ficar seco ou estranho: o objetivo é soar como o usuário escrevendo bem, não como um texto artificialmente "anti-IA".
5. Mantenha o registro formal exigido em contextos institucionais (SEI, ABNT) — humanizar não é sinônimo de informalizar; é eliminar o ruído estatístico de IA preservando o tom apropriado ao contexto.
6. Em textos técnicos/administrativos (despachos, notas técnicas, pareceres), dê atenção redobrada aos itens 1, 2, 3, 4, 8, 9, 10, 14, 18, 20 e 22 — e principalmente ao 22 (variação elegante), que em texto jurídico-administrativo é erro grave, não só estilístico.
7. Em textos educacionais (ebooks, roteiros de aula, questões), dê atenção redobrada aos itens 4, 5, 6, 7, 8, 13, 16 e 17.
8. Em qualquer gênero, o item 16 (burstiness/ritmo de frases) é o teste final: releia o parágrafo pensando no ritmo, não só no vocabulário. Um texto pode estar livre de clichês lexicais e ainda soar mecânico se todas as frases tiverem o mesmo tamanho e formato.

## Fontes

- Wikipedia, "Wikipedia:Signs of AI writing" — página de orientação mantida pelo WikiProject AI Cleanup, com milhares de exemplos catalogados de texto gerado por IA em artigos, rascunhos e comentários (itens 1-15).
- Kobak, D. et al., "Delving into LLM-assisted writing in biomedical publications through excess vocabulary" (arXiv 2406.07016 / Science Advances 2025) — análise estatística de mais de 14 milhões de resumos do PubMed, base quantitativa do item 17.
- Literatura de linguística computacional sobre perplexidade e "burstiness" como métricas de detecção (usadas por ferramentas como GPTZero), base do item 16.
- Análises de terceiros sobre os mesmos padrões, usadas para triangulação e exemplos práticos: Beutler Ink ("How to Spot AI Writing, According to Wikipedia"), Forbes/William Beutler, MakeUseOf, e discussões de redatores/copywriters sobre clichês recorrentes do ChatGPT em textos comerciais (itens 18-21).
- Curadoria e adaptação ao contexto de produção de conteúdo institucional, técnico (TI) e educacional: item 22 e a priorização por gênero na seção "Como aplicar" são elaboração própria desta skill, não tradução literal de nenhuma fonte — a Wikipedia, por exemplo, foi escrita para o contexto específico de detecção de edições na enciclopédia, e algumas de suas observações não se aplicam fora dali.
