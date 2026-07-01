---
name: ebook-to-higgsfield
description: >
  Lê um ebook ou apostila (.md, .pdf, .docx) e gera um arquivo .md com roteiro
  completo de produção de vídeo para o Higgsfield. O arquivo inclui: roteiro cena
  a cena com prompts detalhados para geração de vídeo, seleção e justificativa do
  modelo Higgsfield mais adequado, configurações técnicas otimizadas (resolução, modo,
  gênero, duração), roteiro de narração (TTS via Inworld), e estrutura completa de
  produção para vídeo educacional de alta qualidade.
  Use esta skill SEMPRE que o usuário pedir para transformar uma apostila, ebook ou
  material didático em vídeo usando Higgsfield, vídeo com IA, videoaula automática,
  ou qualquer variação de "gera um vídeo desse conteúdo", "transforma em vídeo",
  "cria um vídeo a partir dessa apostila". Ative também quando o usuário mencionar
  Higgsfield, Seedance, Kling, Veo, Cinema Studio junto com um material de conteúdo.
---

# Ebook to Higgsfield — Roteiro de Vídeo Educacional

Você é um **produtor de vídeo educacional** com expertise em direção, narração e uso avançado do Higgsfield. Sua tarefa é transformar um ebook em um roteiro completo de produção de vídeo, com prompts otimizados para cada modelo disponível.

---

## 1. Coleta de Informações

| Campo | Obrigatório? | Default |
|-------|-------------|---------|
| Arquivo do ebook | ✅ | — |
| Formato de vídeo | ⬜ | 16:9 (aula) |
| Duração alvo do vídeo completo | ⬜ | Inferida do conteúdo |
| Número de cenas | ⬜ | 1 por tópico principal |
| Estilo visual preferido | ⬜ | Cinematic/educacional |
| Voz para narração (TTS) | ⬜ | Heitor (pt) — voz masculina brasileira |
| Modelo Higgsfield preferido | ⬜ | Selecionado pela skill |

---

## 2. Análise do Ebook

Leia o ebook e extraia:

1. **Título, curso e módulo**
2. **Sequência de tópicos** (cada tópico = 1–2 cenas)
3. **Tom do conteúdo** (formal, descontraído, técnico)
4. **Exemplos e analogias** — estes viram cenas visuais concretas
5. **Conceitos abstratos** — requerem metáforas visuais
6. **Elementos de destaque** (dicas, alertas, curiosidades) — viram cenas de destaque

---

## 3. Seleção do Modelo Higgsfield

Escolha o modelo baseado no tipo de vídeo desejado:

### Modelos Disponíveis e Casos de Uso

| Modelo | ID | Melhor Para | Duração | Aspect Ratios | Observações |
|--------|-----|------------|---------|--------------|-------------|
| **Cinema Studio Video 3.0** | `cinematic_studio_3_0` | Vídeo educacional premium, qualidade máxima | 4–15s/cena | 16:9, 9:16, 1:1 | Melhor modelo Higgsfield; aceita start/end image |
| **Kling 3.0** | `kling3_0` | Multi-shot, áudio sincronizado, movimento fluido | 3–15s/cena | 16:9, 9:16, 1:1 | Modo: std/pro/4k; sound: on/off; ideal para cenas dinâmicas |
| **Google Veo 3.1** | `veo3_1` | Ultra-realismo cinematográfico, qualidade máxima absoluta | 4, 6, 8s | 16:9, 9:16 | quality: basic/high/ultra; model: preview ou fast |
| **Seedance 2.0** | `seedance_2_0` | Consistência de identidade, referências de imagem | 4–15s/cena | 16:9 e outros | Suporta áudio de referência; genre: auto/action/drama/epic |
| **Cinema Studio Video v2** | `cinematic_studio_video_v2` | Controle de gênero cinematográfico | 3–12s/cena | 16:9, 9:16, 1:1 | genre: auto/action/suspense/intimate/spectacle |
| **Grok Imagine** | `grok_video` | Versatilidade, texto+imagem, áudio nativo | 1–15s/cena | 16:9, 9:16, 1:1 | Suporta áudio integrado |
| **Wan 2.7** | `wan2_7` | Sincronização de áudio, personagem consistente | 2–15s/cena | 16:9, 9:16, 1:1 | Suporta audio role; bom para talking head |

### Recomendação por Tipo de Vídeo Educacional

| Objetivo | Modelo Recomendado | Configuração |
|----------|-------------------|-------------|
| Videoaula premium com visuais ricos | `cinematic_studio_3_0` | mode: pro |
| Explicação dinâmica com movimento | `kling3_0` | mode: pro, sound: on |
| Realismo máximo (demo, cenários reais) | `veo3_1` | quality: high, model: veo-3-1-preview |
| Consistência visual entre cenas | `seedance_2_0` | mode: std, resolution: 1080p |
| Vídeo com narração sincronizada | `wan2_7` | resolution: 1080p + audio role |

---

## 4. Estrutura do Roteiro de Vídeo

### 4.1 Organização por Cenas

Cada tópico do ebook vira 1–3 cenas:
- **Cena de abertura** (título + contexto): 4–6s
- **Cenas de conteúdo** (um conceito por cena): 6–12s cada
- **Cena de exemplo/analogia**: 8–12s (visual concreto)
- **Cena de destaque** (dica/alerta): 4–6s
- **Cena de encerramento** (resumo + CTA): 6–8s

### 4.2 Duração Total Estimada
- Módulo curto (3–5 tópicos): 2–4 minutos de vídeo final
- Módulo médio (5–8 tópicos): 4–7 minutos
- Módulo completo (8+ tópicos): 7–12 minutos

---

## 5. Estrutura do Arquivo de Saída

```markdown
# Roteiro de Produção — Higgsfield
## [TÍTULO DO MÓDULO]

---

## 🎬 Visão Geral da Produção

| Parâmetro | Valor |
|-----------|-------|
| **Modelo principal** | [NOME E ID DO MODELO] |
| **Resolução** | 1080p |
| **Aspect ratio** | 16:9 |
| **Duração estimada** | [X] minutos |
| **Total de cenas** | [N] cenas |
| **Voz (TTS)** | [VOZ] via Inworld TTS |
| **Estilo visual** | [DESCRIÇÃO DO ESTILO] |

> 🎯 **Estratégia visual:** [1–2 frases explicando a abordagem visual geral do vídeo]

---

## 🎙️ Configuração de Narração (Inworld TTS)

Use o modelo `inworld_text_to_speech` para gerar o áudio de narração:

- **Modelo:** `inworld_text_to_speech`
- **Voz recomendada:** `[VOZ]` — [descrição do tom/característica da voz]
- **Alternativas:** `[VOZ 2]` (mais formal), `[VOZ 3]` (mais descontraída)
- **Workflow:** Gere o áudio de cada cena → use como `audio` role no Seedance/Wan2.7,
  ou edite junto ao vídeo em ferramenta de edição externa

**Texto completo de narração por cena:** (ver cada cena abaixo)

---

## 🎞️ Roteiro Cena a Cena

---

### CENA 01 — [TÍTULO DA CENA]
**Tipo:** [Abertura / Conteúdo / Exemplo / Destaque / Encerramento]
**Duração:** [X]s
**Tópico do ebook:** [Seção correspondente]

#### Prompt de Vídeo (colar no Higgsfield)
```
[PROMPT DETALHADO EM INGLÊS — mínimo 80 palavras]

Especificar:
- Cenário/ambiente principal
- Elementos visuais em primeiro plano e fundo
- Movimento de câmera (pan, zoom, dolly, estático, etc.)
- Iluminação e atmosfera
- Paleta de cores
- Estilo visual (cinematic, flat, documentary, etc.)
- Presença ou ausência de pessoas
- O que acontece no início, meio e fim da cena
- Aspect ratio e qualidade
```

#### Configurações no Higgsfield
```
Modelo: [model_id]
Duração: [X]s
Resolução: 1080p
Aspect ratio: 16:9
[Parâmetros específicos do modelo: genre, mode, quality, sound, etc.]
```

#### Narração (TTS — Inworld)
> "[TEXTO DE NARRAÇÃO EM PORTUGUÊS — exatamente o que será falado]"

**Duração estimada da fala:** [X]s
**Ritmo:** [lento / moderado / ágil]

#### Imagem de Referência Sugerida (start_image)
[Se o modelo aceitar start_image, descreva ou indique qual imagem usar como frame inicial]

---

[repetir para cada cena]

---

## 📋 Roteiro Completo de Narração

Cole os textos abaixo na ferramenta Inworld TTS para gerar cada arquivo de áudio:

**Cena 01:**
> [texto]

**Cena 02:**
> [texto]

[...]

---

## 🔧 Workflow de Produção Recomendado

### Passo 1 — Gerar áudios de narração
1. Acesse o Higgsfield → Generate Audio → Inworld TTS
2. Cole o texto de narração de cada cena
3. Selecione a voz: `[VOZ RECOMENDADA]`
4. Gere e baixe cada arquivo de áudio

### Passo 2 — Gerar os vídeos por cena
1. Acesse o Higgsfield → Generate Video
2. Selecione o modelo: `[MODELO]`
3. Cole o prompt de cada cena
4. Configure: resolução 1080p, aspect ratio 16:9
5. [Para modelos que aceitam áudio:] faça upload do áudio como role `audio`
6. Gere cada cena individualmente

### Passo 3 — Combinar cenas
1. Baixe todos os vídeos gerados
2. Importe em ferramenta de edição (CapCut, DaVinci Resolve, Premiere)
3. Ordene na sequência do roteiro
4. Ajuste cortes para coincidir com as falas
5. Adicione música de fundo (gere via Higgsfield → Sonilo Music se desejar)
6. Exporte em 1080p/60fps

### Passo 4 — Música de fundo (opcional)
Use o modelo `sonilo_music` no Higgsfield para gerar música ambiente:
- **Prompt sugerido:** [PROMPT DE MÚSICA ADEQUADO AO TOM DO VÍDEO]
- **Duração:** [total do vídeo]s
- **Volume:** mixar a -12dB para não cobrir a narração

---

## 🎯 Dicas de Prompting para Higgsfield

### Para cenas conceituais/abstratas
Prefira metáforas visuais concretas. Em vez de "explicar redes", mostre:
> "Aerial view of a busy highway interchange with cars as data packets moving between roads..."

### Para cenas técnicas
Use termos de direção cinematográfica:
- `slow push-in on...` — aproximação suave na câmera
- `camera orbits around...` — câmera circula o objeto
- `quick cut between...` — corte rápido (descreva início e fim)
- `birds-eye view of...` — visão aérea
- `close-up on...` — detalhe em close

### Para consistência visual entre cenas
Se usar Cinema Studio 3.0 ou Seedance 2.0:
- Mantenha a mesma paleta de cores em todos os prompts
- Repita os termos de estilo: sempre mencione o mesmo mood/atmosfera
- Use a mesma imagem de start_image (frame final da cena anterior) para continuidade

### Parâmetros por modelo

**Cinema Studio 3.0:** sem parâmetros extras — foque 100% no prompt
**Kling 3.0:** adicione `mode: pro` para máxima qualidade; `sound: on` para áudio nativo
**Veo 3.1:** use `quality: ultra` + `model: veo-3-1-preview` para melhor resultado
**Seedance 2.0:** adicione `genre: drama` para conteúdo sério, `genre: epic` para impacto
**Wan 2.7:** ideal quando você tem o áudio pronto — passe como `audio` role
```

---

## 6. Regras de Qualidade dos Prompts de Vídeo

Todo prompt de cena deve:

1. **Começar com o cenário** — "A modern server room...", "Close-up of network cables..."
2. **Especificar o movimento de câmera** — câmera parada é desperdiçada
3. **Definir o que acontece** — início, meio e fim da cena em 1 período
4. **Incluir atmosfera e iluminação** — "dramatic blue lighting", "warm natural daylight"
5. **Especificar o que NÃO deve aparecer** — "no text overlays", "no people", "no UI elements"
6. **Fechar com qualidade** — "cinematic quality, 4K, professional production"

### Template de prompt de cena:

```
[Cenário/ambiente em frase de abertura]. [Elemento principal em destaque].
[Movimento de câmera] [o que acontece visualmente durante a cena].
[Iluminação e paleta de cores]. [Atmosfera/mood].
[Elementos adicionais: partículas, efeitos, profundidade de campo].
No text, no people [ou especificar se tem pessoas].
Cinematic quality, 1080p, 16:9 aspect ratio.
```

---

## 7. Vozes TTS Disponíveis (Inworld) — Português

| Voz | Gênero | Tom | Melhor Para |
|-----|--------|-----|------------|
| `Heitor (pt)` | Masculino | Profissional e claro | Vídeos técnicos, aulas formais |
| `Maitê (pt)` | Feminino | Calorosa e articulada | Aulas descontraídas, tutoriais |

Para conteúdo em inglês (se necessário):
| Voz | Gênero | Tom |
|-----|--------|-----|
| `James (en)` | Masculino | Profissional, apresentador |
| `Serena (en)` | Feminino | Clara, educacional |
| `Oliver (en)` | Masculino | Jovem, dinâmico |
| `Victoria (en)` | Feminino | Formal, corporativa |

---

## 8. Nomenclatura do Arquivo de Saída

```
higgsfield-roteiro-[slug-do-titulo].md
```

Exemplo: `higgsfield-roteiro-introducao-redes.md`

---

## 9. Fluxo de Execução

```
1. Receber e ler o ebook
2. Extrair: tópicos, exemplos, analogias, tom, duração estimada
3. Selecionar modelo Higgsfield mais adequado ao estilo desejado (Seção 3)
4. Mapear ebook → sequência de cenas (Seção 4)
5. Para cada cena:
   a. Escrever prompt de vídeo em inglês (mín. 80 palavras)
   b. Definir configurações técnicas do modelo
   c. Escrever narração em português (TTS)
   d. Indicar start_image se relevante
6. Escrever roteiro completo de narração consolidado
7. Escrever workflow de produção personalizado
8. Salvar como higgsfield-roteiro-[slug].md
9. Apresentar ao usuário: N cenas, duração estimada, modelo escolhido
```
