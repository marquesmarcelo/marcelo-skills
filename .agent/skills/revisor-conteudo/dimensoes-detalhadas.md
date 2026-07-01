# Dimensões detalhadas, exemplos calibrados e verificação ativa

Este arquivo aprofunda cada uma das 11 dimensões da auditoria. Consultá-lo quando houver dúvida sobre **como classificar** um achado, **como distinguir erro de escolha legítima** ou **como redigir** a justificativa.

## Índice

- [Como calibrar um achado](#como-calibrar-um-achado)
- [Playbook de verificação ativa (D5, D6, D7)](#playbook-de-verificação-ativa)
- [D1 — Duplicidade](#d1--duplicidade)
- [D2 — Incrementalidade e progressão](#d2--incrementalidade-e-progressão)
- [D3 — Profundidade e nível de aplicação](#d3--profundidade-e-nível-de-aplicação)
- [D4 — Viés, neutralidade e ética](#d4--viés-neutralidade-e-ética)
- [D5 — Erros conceituais e imprecisões](#d5--erros-conceituais-e-imprecisões)
- [D6 — Conteúdo desatualizado](#d6--conteúdo-desatualizado)
- [D7 — Integridade de links e referências](#d7--integridade-de-links-e-referências)
- [D8 — Acessibilidade e inclusividade](#d8--acessibilidade-e-inclusividade)
- [D9 — Alinhamento de objetivos](#d9--alinhamento-de-objetivos)
- [D10 — Densidade e carga cognitiva](#d10--densidade-e-carga-cognitiva)
- [D11 — Consistência de estilo e voz](#d11--consistência-de-estilo-e-voz)

---

## Como calibrar um achado

A diferença entre uma auditoria útil e uma auditoria irritante está na calibração. Antes de registrar qualquer achado, aplicar os três testes:

1. **Teste da evidência.** Existe um trecho literal que sustenta o achado? Se a única base é "impressão geral", não é achado — é opinião. Reformular até ancorar em evidência ou descartar.
2. **Teste do erro vs. estilo.** O que incomoda é objetivamente um problema (compromete aprendizado, contradiz fato, quebra alinhamento) ou apenas diferente de como *eu* faria? Preferência de estilo do auditor não é defeito do material. Na dúvida, rebaixar para "recomendação" e preservar a autonomia do autor.
3. **Teste da ação.** Consigo escrever uma sugestão concreta e aplicável? Se a sugestão sai vaga ("melhorar a clareza"), o achado ainda não está maduro — especificar o que mudar e como.

**Exemplo de achado bem calibrado:**
> Localização: Aula 3 / p.12 · Trecho: "O TCP é um protocolo sem conexão que garante entrega." · D5 · 🔴 Alta · Justificativa: contradição factual — o TCP é orientado à conexão (handshake de 3 vias); "sem conexão" descreve o UDP. Um estudante memorizará a definição invertida. · Sugestão: corrigir para "protocolo orientado à conexão que garante entrega ordenada e confiável" e, se útil, contrastar com o UDP em uma frase.

**Exemplo de achado fraco (NÃO registrar assim):**
> Trecho: (nenhum) · D11 · 🟡 · Justificativa: o texto poderia ser mais envolvente. · Sugestão: deixar mais interessante.

Por que é fraco: sem trecho (falha no teste 1), confunde gosto com defeito (teste 2) e a sugestão é inacionável (teste 3).

**Linguagem recomendada para justificativas:**
- Erro confirmado: "contradição factual", "definição tecnicamente incorreta", "objetivo declarado sem entrega correspondente".
- Suspeita: "possível imprecisão — recomenda-se verificação com especialista da área".
- Estilo/recomendação: "escolha legítima; como melhoria opcional, considerar…".

---

## Playbook de verificação ativa

Auditar conteúdo factual sem verificar é apenas suspeitar. Quando houver `web_search`/`web_fetch` disponíveis, **verificar de fato** antes de afirmar — isso transforma a auditoria de "achismo informado" em diagnóstico defensável. Regras:

- **D5 (erros conceituais):** quando um achado depende de um fato datável ou contestável (uma definição técnica, um número, uma atribuição de autoria), buscar a fonte primária antes de classificar como erro. Se a busca confirmar, gravidade 🔴 com a fonte na justificativa. Se não der para confirmar, manter como "possível imprecisão".
- **D6 (desatualização):** **nunca** afirmar que algo está desatualizado de memória. Confirmar por busca a versão/estado atual (versão estável de um framework, vigência de uma lei, dado estatístico mais recente) usando o ano corrente na query. Defasagem só vira achado depois de confirmada.
- **D7 (links):** para as URLs principais, tentar `web_fetch`. Classificar cada uma: Ativa / Inativa (erro confirmado) / Redirecionada / Inacessível (paywall ou login). Listar as não verificadas explicitamente como "não verificada" em vez de presumir.
- **Limites:** se a verificação for inviável (sem rede, volume alto), declarar isso no relatório — "links não verificados automaticamente" — em vez de fingir que foram. Honestidade sobre o método é parte da auditoria.

---

## D1 — Duplicidade

**O que procurar:** conceitos explicados do zero mais de uma vez, entre arquivos ou dentro do mesmo arquivo.

**Erro vs. escolha:** revisitar um conceito com aprofundamento novo (espiral curricular de Bruner) é virtude, não defeito. O problema é a reexplicação idêntica que não adiciona nada — desperdiça tempo e sinaliza descoordenação entre conteudistas.

**Achado típico:** "Os capítulos 2 e 5 definem 'normalização de banco de dados' do zero, com exemplos equivalentes e sem aprofundamento no segundo. Consolidar a explicação no cap. 2 e, no cap. 5, apenas referenciá-la e avançar para formas normais superiores."

---

## D2 — Incrementalidade e progressão

**O que procurar:** dependências de pré-requisito respeitadas; ausência de saltos e regressões.

- **Salto lógico:** tema avançado usa um conceito que nunca foi introduzido. Ex.: usar "herança múltipla" antes de definir "classe".
- **Regressão:** conteúdo elementar reaparece depois de material avançado, sem justificativa (revisão deliberada é justificativa válida; esquecimento estrutural não é).

**Achado típico:** "A Aula 4 aplica regressão logística antes de a Aula 6 introduzir o conceito de função de verossimilhança. Reordenar ou inserir uma ponte conceitual na Aula 4."

---

## D3 — Profundidade e nível de aplicação

**Referência:** Taxonomia de Bloom revisada. Para ensino superior, conteúdo central preso em *Lembrar/Compreender* é insuficiente; o material deve levar a *Aplicar, Analisar, Avaliar, Criar*.

**Como medir:** olhar os verbos dos objetivos e, sobretudo, o que as **atividades** exigem. Um material que só pede "defina" e "liste" não chega à aplicação, por mais denso que seja o texto.

**Achado típico:** "O módulo de segurança define os tipos de ataque (nível Compreender) mas nenhuma atividade pede que o estudante analise um log real ou proponha mitigação (Aplicar/Criar). Acrescentar um estudo de caso com tomada de decisão."

---

## D4 — Viés, neutralidade e ética

**O que procurar:** viés pessoal, político, cultural, de gênero ou comercial; opinião como fato; falta de diversidade em exemplos e personagens; apresentação unilateral de tema controverso.

**Erro vs. escolha:** uma posição assumida e sinalizada como tal ("defende-se aqui que…") é legítima. O problema é a opinião disfarçada de consenso científico, ou o exemplo que sempre coloca o mesmo grupo no papel subalterno.

**Achado típico:** "Os 7 estudos de caso usam exclusivamente nomes masculinos em cargos de liderança. Diversificar gênero e contexto regional para ampliar a representatividade sem alterar o conteúdo técnico."

---

## D5 — Erros conceituais e imprecisões

**O que procurar:** definições incorretas, teorias mal interpretadas, estatística distorcida, citações deturpadas.

**Regra de ouro:** sinalizar apenas com convicção razoável. Verificar ativamente quando possível (ver Playbook). Diante de dúvida real, registrar como "possível imprecisão — recomenda-se verificação" em vez de afirmar erro.

**Achado típico:** ver o exemplo bem calibrado em [Como calibrar um achado](#como-calibrar-um-achado).

---

## D6 — Conteúdo desatualizado

**Referência temporal:** 2026. **Nunca** afirmar desatualização sem confirmar por busca.

**O que procurar:** versões de software/frameworks/bibliotecas defasadas; legislação ou norma alterada; dados estatísticos antigos (em geral anteriores a ~2022); ferramentas descontinuadas ou renomeadas.

**Achado típico:** "O material instrui instalar a versão X de uma biblioteca como 'a mais recente'. A verificação indica que a série atual é Y, com mudanças relevantes de API. Atualizar o comando e revisar os exemplos afetados."

---

## D7 — Integridade de links e referências

**O que procurar:** URLs quebradas, instáveis, muito antigas ou que exigem assinatura/login sem aviso; referências bibliográficas incompletas ou desatualizadas.

**Procedimento:** listar todas as URLs; verificar as principais com `web_fetch`; classificar (Ativa / Inativa / Redirecionada / Inacessível / Não verificada). Sinalizar paywalls não anunciados, porque frustram o estudante no meio do estudo.

**Achado típico:** "Dos 9 links da apostila, 2 retornaram erro na verificação (p.8 e p.14) e 1 exige assinatura sem aviso (p.20). Substituir os inativos e sinalizar o conteúdo pago."

---

## D8 — Acessibilidade e inclusividade

**Referências:** WCAG 2.2, ABNT NBR 9050, LBI (Lei 13.146/2015), linguagem simples.

**O que procurar:** figuras/tabelas/infográficos sem descrição textual no corpo; linguagem rebuscada onde a simples bastaria; siglas não expandidas na primeira ocorrência; pressuposição de recursos inacessíveis (software pago, idioma estrangeiro sem tradução, hardware específico).

**Achado típico:** "As 12 figuras do capítulo não têm descrição textual; um estudante com deficiência visual usando leitor de tela perde todo o conteúdo visual. Acrescentar descrição objetiva sob cada figura."

---

## D9 — Alinhamento de objetivos

**Referência:** alinhamento construtivo (Biggs & Tang) — objetivo, conteúdo de ensino e atividade de avaliação precisam apontar para o mesmo lugar.

**O que procurar, em três cruzamentos:**
- Objetivo declarado → existe conteúdo que o ensina? (senão: **promessa sem entrega**)
- Conteúdo ensinado → existe objetivo que o ancora? (senão: **ensino sem rumo**)
- Objetivo/conteúdo → existe atividade que o **avalia**? (senão: **aprendizado não verificável**)
- Os verbos são mensuráveis (Bloom) ou vagos ("entender", "conhecer")?

**Achado típico:** "O objetivo 'avaliar arquiteturas de rede' (nível Avaliar) não tem atividade correspondente — os exercícios só pedem para identificar componentes (Lembrar). Incluir uma atividade de comparação crítica entre duas arquiteturas."

---

## D10 — Densidade e carga cognitiva

**Referências:** Carga Cognitiva (Sweller), Aprendizagem Multimídia (Mayer).

**O que procurar:** blocos de texto contínuo acima de ~400 palavras sem respiro (exemplo, bullet, imagem, exercício); conceito novo sem exemplo concreto logo em seguida; ausência de variação de formato; páginas que despejam muitos conceitos novos sem ancoragem no que o estudante já sabe.

**Achado típico:** "A seção 3.2 apresenta 6 conceitos novos em 2 páginas de texto corrido, sem exemplo nem pausa. Fragmentar em blocos com um exemplo por conceito e uma síntese visual ao final."

---

## D11 — Consistência de estilo e voz

**O que procurar:** variação brusca de tom entre arquivos (informal demais em um, hiperacadêmico em outro); o mesmo conceito chamado por nomes diferentes em pontos distintos; formatação e hierarquia visual inconsistentes.

**Erro vs. escolha:** variar o registro de propósito (um capítulo introdutório mais leve) é legítimo se intencional e coerente. O problema é a oscilação não intencional que denuncia múltiplos autores não harmonizados.

**Achado típico:** "O conceito é chamado de 'aprendizado de máquina' no cap. 1, 'machine learning' no cap. 3 e 'AM' no cap. 5, sem padronização. Definir um termo canônico e os sinônimos aceitos, e aplicar em toda a trilha."
