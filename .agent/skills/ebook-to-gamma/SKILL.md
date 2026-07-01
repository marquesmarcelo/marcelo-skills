---
name: ebook-to-gamma
description: >
  Lê um ebook ou apostila (.md, .pdf, .docx) e gera um arquivo .md com instruções
  completas e detalhadas para que o Gamma.app produza uma apresentação de alta qualidade
  a partir do conteúdo. O arquivo gerado inclui: prompt principal estruturado slide a
  slide, escolha de tema justificada, configurações de imagem, tom, audiência, formato
  de card e orientações de uso na interface do Gamma.
  Use esta skill SEMPRE que o usuário pedir para transformar uma apostila, ebook, material
  didático ou documento em apresentação usando Gamma, slides com IA, deck automático, ou
  qualquer variação de "gerar slides a partir de um documento". Também ative quando o
  usuário disser "quero apresentar esse conteúdo", "cria um slide desse material" ou
  "passa isso pro Gamma".
---

# Ebook to Gamma — Geração de Prompt para Apresentação

Você é um **especialista em design instrucional e em uso avançado do Gamma.app**. Sua tarefa é analisar um ebook/apostila e produzir um arquivo de instrução completo que permita ao Gamma gerar uma apresentação excelente de primeira tentativa.

---

## 1. Coleta de Informações

Antes de gerar, colete ou infira:

| Campo | Obrigatório? | Default |
|-------|-------------|---------|
| Arquivo do ebook (`.md`, `.pdf`, `.docx`) | ✅ | — |
| Público-alvo da apresentação | ⬜ | Inferido do ebook |
| Formato de entrega (aula presencial / online / webinar / autoestudo) | ⬜ | Aula |
| Número de slides desejado | ⬜ | Gamma define automaticamente |
| Tema visual preferido | ⬜ | Selecionado pela skill |
| Proporção dos slides | ⬜ | 16:9 |

Se o arquivo não for fornecido, solicite antes de prosseguir.

---

## 2. Análise do Ebook

Leia o ebook completo e extraia:

1. **Título e tema central** do módulo
2. **Objetivos de aprendizagem** (listados ou implícitos)
3. **Estrutura de tópicos** — hierarquia de seções e subseções
4. **Conceitos-chave** — termos técnicos centrais (máx. 10)
5. **Exemplos e analogias** presentes no texto
6. **Elementos especiais** — tabelas, listas comparativas, dicas, alertas
7. **Tom do conteúdo** — formal, descontraído, técnico, introdutório
8. **Domínio temático** — para selecionar paleta e tema Gamma adequados

---

## 3. Seleção do Tema Gamma

Com base no domínio e tom detectados, selecione o tema mais adequado:

| Domínio / Tom | Temas Gamma Recomendados |
|--------------|--------------------------|
| TI / Segurança / Infra | `Dusk`, `Carbon`, `Midnight` (escuros, profissionais) |
| Desenvolvimento / Cloud | `Nord`, `Blueprint`, `Digital` |
| Educação / Didático descontraído | `Breeze`, `Sunrise`, `Pastel` |
| Negócios / Corporativo | `Executive`, `Slate`, `Graphite` |
| Ciência de Dados / Analítico | `Deep Blue`, `Obsidian`, `Cosmos` |
| Redes / Infraestrutura | `Carbon`, `Storm`, `Midnight` |

> **Instrução:** Ao gerar o arquivo de saída, sempre justifique a escolha do tema com 1 frase.

---

## 4. Mapeamento Ebook → Slides

Converta a estrutura do ebook em uma sequência de slides seguindo esta lógica:

| Seção do Ebook | Slide(s) Correspondente(s) |
|----------------|---------------------------|
| Título + Bloco "Neste módulo você vai:" | **Slide 1 — Capa** + **Slide 2 — Agenda/O que veremos** |
| Objetivos de Aprendizagem | **Slide 3 — Objetivos** (lista visual com ícones) |
| Cada subseção principal (###) | **1–2 slides de conteúdo** |
| Tabelas comparativas | **Slide dedicado** com layout de tabela ou colunas |
| Elementos 💡 Dica / ⚠️ Atenção | **Slide de destaque** (callout visual) |
| Elementos 🔍 Saiba Mais | **Slide de recursos** ao final do bloco |
| Resumo | **Slide de recap** com bullets ou tabela |
| Próximos Passos | **Slide final de chamada para ação** |

**Regra geral:** 1 ideia central por slide. Se uma subseção tiver mais de 3 conceitos distintos, divida em múltiplos slides.

---

## 5. Estrutura do Arquivo de Saída

O arquivo gerado deve ter o seguinte formato:

```markdown
# Instruções para Geração no Gamma.app
## Módulo: [TÍTULO DO EBOOK]

---

## ⚙️ Configurações Iniciais do Gamma

Antes de colar o prompt, configure o Gamma com os seguintes parâmetros:

| Parâmetro | Valor | Onde configurar |
|-----------|-------|----------------|
| **Formato** | Presentation | Seletor de tipo ao criar |
| **Proporção** | 16:9 | Card Options → Dimensions |
| **Tema** | [NOME DO TEMA] | Theme selector |
| **Modo de texto** | Generate | Text Mode (expande o conteúdo) |
| **Quantidade de texto** | Medium | Text Options → Amount |
| **Audiência** | [AUDIÊNCIA] | Text Options → Audience |
| **Tom** | [TOM: professional / educational / conversational] | Text Options → Tone |
| **Fonte de imagens** | AI Generated | Image Options → Source |
| **Estilo de imagem** | [ESTILO] | Image Options → Style Preset |
| **Idioma** | pt | Text Options → Language |

> 🎨 **Por que [NOME DO TEMA]:** [1 frase justificando a escolha visual para este conteúdo]

---

## 📋 Prompt Principal

Cole o texto abaixo integralmente no campo de input do Gamma ao criar uma nova apresentação:

---

[INÍCIO DO PROMPT — COLAR NO GAMMA]

**Título:** [TÍTULO DA APRESENTAÇÃO]

**Audiência:** [DESCRIÇÃO DO PÚBLICO]

**Objetivo geral:** [O QUE O ALUNO DEVE SABER AO FINAL]

Crie uma apresentação profissional e didática com os seguintes slides, nesta ordem exata:

---

**SLIDE 1 — CAPA**
Título principal: "[TÍTULO DO MÓDULO]"
Subtítulo: "[NOME DO CURSO] | Módulo [N]"
Elemento visual: imagem de fundo que remeta a [DESCRIÇÃO DO TEMA VISUAL PARA IA]
Layout: título centralizado, destaque máximo, sem bullets

---

**SLIDE 2 — AGENDA**
Título: "O que veremos hoje"
Formato: lista numerada com ícones
Itens:
[LISTA DOS TÓPICOS PRINCIPAIS DO MÓDULO]

---

**SLIDE 3 — OBJETIVOS**
Título: "Ao final deste módulo, você vai conseguir:"
Formato: cards ou lista com ícones de check (✓)
Itens (verbos de ação):
[OBJETIVOS EXTRAÍDOS DO EBOOK]

---

[SLIDES DE CONTEÚDO — um bloco por slide]

**SLIDE [N] — [TÍTULO DO TÓPICO]**
Título: "[TÍTULO DO SLIDE]"
Conteúdo principal: [RESUMO DO CONTEÚDO EM 3-4 BULLETS DIRETOS]
Exemplo ou analogia: "[EXEMPLO EXTRAÍDO DO EBOOK]"
Elemento visual sugerido: [DESCRIÇÃO PARA GERAÇÃO DE IMAGEM]
Layout sugerido: [bullets / dois painéis / imagem à direita / colunas / tabela]

---

[repetir para cada slide de conteúdo]

---

**SLIDE [N] — RESUMO**
Título: "O que aprendemos"
Formato: tabela de duas colunas (Conceito | Definição)
Linhas:
[TABELA EXTRAÍDA DO RESUMO DO EBOOK]

---

**SLIDE FINAL — PRÓXIMOS PASSOS**
Título: "Por onde continuar?"
Formato: lista de ações com checkboxes visuais
Itens:
[AÇÕES EXTRAÍDAS DA SEÇÃO DE PRÓXIMOS PASSOS DO EBOOK]
Rodapé: "Próximo módulo: [TÍTULO DO PRÓXIMO MÓDULO]"

[FIM DO PROMPT]

---

## 🖼️ Instruções de Imagem para o Gamma

Para cada slide com sugestão visual, configure:

- **Image Model:** dall-e-3 (melhor para ilustrações técnicas e educacionais)
- **Style Preset:** illustration (didático) ou 3D (impacto visual)
- **Guidance per slide:**

| Slide | Prompt de Imagem Sugerido |
|-------|--------------------------|
| Capa | [PROMPT DETALHADO EM INGLÊS PARA IMAGEM DE CAPA] |
| Slide [N] | [PROMPT DETALHADO EM INGLÊS] |
| ... | ... |

---

## 🔧 Ajustes Pós-Geração Recomendados

Após o Gamma gerar a apresentação, revise:

1. **Slide de capa** — confirme que o título está com o tamanho correto e a imagem não obscurece o texto
2. **Slides com tabelas** — verifique se o Gamma manteve todas as colunas; expanda manualmente se necessário
3. **Densidade de texto** — se algum slide ficou muito denso, use "Split card" para dividir em dois
4. **Consistência de ícones** — o Gamma às vezes mistura estilos; padronize via "Edit theme"
5. **Slide final** — adicione o logo da instituição se disponível (Insert → Image)

---

## 📤 Export Recomendado

| Uso | Formato | Como exportar |
|-----|---------|--------------|
| Aula presencial | `.pptx` | Share → Export → PowerPoint |
| Publicação online | Link público | Share → Publish |
| PDF handout | `.pdf` | Share → Export → PDF |
| Redes sociais | `.png` (ZIP) | Share → Export → PNG |
```

---

## 6. Qualidade das Descrições por Slide

Para cada slide de conteúdo, o prompt gerado deve seguir estas regras:

### Título do slide
- Máximo 6 palavras
- Frase afirmativa ou pergunta direta
- Nunca use "Introdução" ou "Conteúdo" genéricos

### Bullets de conteúdo
- Máximo 4 bullets por slide
- Cada bullet: 1 linha, começa com verbo ou substantivo-chave
- Se o conteúdo tiver mais de 4 pontos → dividir em 2 slides

### Prompt de imagem para o Gamma (em inglês)
- Especifique sempre: estilo, elementos, cores, mood
- Formato padrão:

```
[Estilo visual] showing [elemento principal]. [Contexto/cenário].
Color palette: [cor 1], [cor 2], [cor 3]. [Mood/atmosfera].
[Formato: 16:9 landscape]. No text overlays.
```

Exemplo:
```
Flat design technical illustration showing a computer network with a central
server connected to 5 client devices via colorful cables. Clean white background
with subtle grid. Color palette: deep blue (#0A2540), electric blue (#0066FF),
light gray (#F5F5F5). Professional and modern mood. 16:9 landscape. No text overlays.
```

---

## 7. Nomenclatura do Arquivo de Saída

```
gamma-prompt-[slug-do-titulo].md
```

Exemplo: `gamma-prompt-introducao-redes.md`

---

## 8. Fluxo de Execução

```
1. Receber e ler o arquivo do ebook
2. Extrair: título, objetivos, tópicos, exemplos, tom, domínio
3. Selecionar tema Gamma adequado ao domínio (Seção 3)
4. Mapear ebook → sequência de slides (Seção 4)
5. Gerar o arquivo .md com todas as seções da Seção 5
6. Para cada slide: escrever título, bullets e prompt de imagem em inglês
7. Salvar como gamma-prompt-[slug].md
8. Apresentar ao usuário com resumo: N slides planejados, tema escolhido, instrução de uso
```
