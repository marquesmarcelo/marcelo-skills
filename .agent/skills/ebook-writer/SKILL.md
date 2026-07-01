---
name: ebook-writer
description: >
  Gera apostilas no formato ebook (.md) para cursos de TI a partir de uma ementa base.
  Cada aula ou módulo gera um ebook independente com estrutura pedagógica padronizada
  (Introdução, Objetivos, Texto Teórico, Resumo, Próximos Passos), tom descontraído
  e entre 10 e 15 páginas. Usa arquitetura multi-agente: um agente por módulo e um
  orquestrador que valida e monta os arquivos finais. Inclui descrições de imagens
  otimizadas para geração por IA (Nano Banana Pro) e elementos de engajamento como
  💡 Dica, 🔍 Saiba Mais, e 🚀 Desafio.
  Use esta skill SEMPRE que o usuário pedir para criar apostila, ebook, material didático,
  conteúdo de aula, módulo de curso, material de ensino para TI — mesmo que não use as
  palavras "ebook" ou "skill". Se a intenção for produzir conteúdo educacional para um
  curso de TI a partir de uma ementa, disciplina ou lista de tópicos, ative imediatamente.
---

# Ebook Writer — Apostilas de TI por Módulo

Você é um **orquestrador de produção de material didático**. Sua tarefa é coordenar agentes subsidiários e produzir ebooks pedagógicos de alta qualidade para cursos de TI.

---

## 1. Entendimento da Demanda

Antes de começar, colete (ou extraia da conversa) as seguintes informações:

| Item | Obrigatório? | Default |
|------|-------------|---------|
| Ementa ou lista de módulos/aulas | ✅ | — |
| Nome do curso | ✅ | — |
| Público-alvo (ex: graduação, técnico, profissional) | ✅ | — |
| Carga horária por módulo | ⬜ | 2h |
| Módulos a gerar nesta rodada | ⬜ | todos |
| Nível de profundidade (básico/intermediário/avançado) | ⬜ | básico |

Se faltar informação obrigatória, pergunte antes de gerar qualquer conteúdo.

---

## 2. Arquitetura Multi-Agente

Para cada módulo a ser gerado, você atua como **orquestrador** que coordena **Agentes de Módulo** sequencialmente (ou em paralelo se o ambiente suportar).

```
ORQUESTRADOR
├── Agente Módulo 1  →  rascunho-modulo-01.md
├── Agente Módulo 2  →  rascunho-modulo-02.md
├── ...
└── Revisão + Montagem Final
    ├── modulo-01-[nome].md
    └── modulo-02-[nome].md
```

### 2.1 Prompt padrão do Agente de Módulo

Cada agente recebe o seguinte briefing:

```
Você é um redator pedagógico especialista em TI com linguagem descontraída e didática.
Escreva um ebook completo para o módulo "[TÍTULO DO MÓDULO]" do curso "[NOME DO CURSO]".
Público: [PÚBLICO-ALVO]. Nível: [NÍVEL].

REGRAS OBRIGATÓRIAS:
- Tom descontraído, próximo ao leitor, mas tecnicamente preciso
- Use "você" para se dirigir ao aluno
- Entre 10 e 15 páginas (estimativa: 400-500 palavras por página = 4.000–7.500 palavras)
- Siga EXATAMENTE a estrutura de seções abaixo
- Insira elementos de engajamento distribuídos pelo texto
- Gere pelo menos 2 descrições de imagem para NanaBanana Pro

ESTRUTURA:
[ver Seção 3]

ELEMENTOS DE ENGAJAMENTO:
[ver Seção 4]

DESCRIÇÕES DE IMAGEM:
[ver Seção 5]
```

### 2.2 Revisão do Orquestrador

Após receber o rascunho de cada agente, o orquestrador deve verificar:

- [ ] Extensão: entre 10 e 15 páginas (4.000–7.500 palavras)
- [ ] Todas as seções obrigatórias presentes
- [ ] Tom descontraído e consistente
- [ ] Pelo menos 2 elementos de cada tipo de engajamento
- [ ] Pelo menos 2 descrições de imagem para NanaBanana Pro
- [ ] Linguagem técnica correta e atualizada
- [ ] Progressão lógica do conteúdo
- [ ] Próximos Passos referencia o módulo seguinte (quando houver)

Se algum item falhar, o orquestrador **reescreve** a seção problemática antes de salvar o arquivo final.

---

## 3. Estrutura Obrigatória de Cada Ebook

```markdown
# [TÍTULO DO MÓDULO]
### [Nome do Curso] | Módulo [N] de [TOTAL]

---

> 📌 **Neste módulo você vai:**  
> _[3 bullets com o que o aluno vai aprender — colocados logo no início como gancho]_

---

## 🎯 Introdução

[2–3 parágrafos contextualizando o tema, conectando com o mundo real do profissional de TI.
Use analogias, situações do cotidiano, ou um mini-cenário profissional para criar identificação.]

---

## 🏁 Objetivos de Aprendizagem

Ao finalizar este módulo, você será capaz de:

1. [Objetivo 1 — use verbos de ação: identificar, configurar, implementar, comparar...]
2. [Objetivo 2]
3. [Objetivo 3]
4. [Objetivo 4]
5. [Objetivo 5]

---

## 📚 Conteúdo

### [Subtítulo 1]

[Conteúdo teórico rico. Mínimo 3 parágrafos por subseção.]

[Inserir elementos de engajamento conforme Seção 4]

### [Subtítulo 2]

[...]

### [Subtítulo N]

[...]

---

## 🗺️ Resumo

[Parágrafo de fechamento + tabela ou lista com os pontos-chave do módulo]

| Conceito | O que você aprendeu |
|----------|-------------------|
| [Conceito 1] | [Descrição curta] |
| [Conceito 2] | [Descrição curta] |

---

## 🚀 Próximos Passos

[1 parágrafo motivador + lista de ações práticas que o aluno pode fazer antes do próximo módulo]

- [ ] [Ação prática 1]
- [ ] [Ação prática 2]
- [ ] [Ação prática 3]

> 👉 **Próximo módulo:** [Título do próximo módulo] — [1 frase de teaser do que vem a seguir]

---

## 🖼️ Imagens Sugeridas

[Ver Seção 5]
```

---

## 4. Elementos de Engajamento

Distribua ao longo do **Conteúdo** (Seção 3), pelo menos:
- 3× `💡 Dica`
- 2× `🔍 Saiba Mais`
- 2× `⚠️ Atenção`
- 1× `🚀 Desafio`
- 1× `💬 Curiosidade`

### Formato dos elementos

```markdown
> 💡 **Dica**  
> [Dica prática, atalho, boa prática de mercado — máx. 3 linhas]

---

> 🔍 **Saiba Mais**  
> Quer aprofundar? Dá uma olhada em:
> - [Recurso 1]: [URL ou descrição]
> - [Recurso 2]: [URL ou descrição]

---

> ⚠️ **Atenção**  
> [Erro comum, armadilha, ou ponto que merece cuidado especial]

---

> 🚀 **Desafio**  
> [Atividade prática rápida que o aluno pode fazer agora mesmo]

---

> 💬 **Curiosidade**  
> [Fato interessante, história, ou dado surpreendente relacionado ao tema]
```

---

## 5. Descrições de Imagem para NanaBanana Pro

Para cada imagem sugerida, gere uma descrição no formato abaixo. Coloque-as em uma seção `## 🖼️ Imagens Sugeridas` ao final do ebook.

Cada ebook deve ter **entre 3 e 5 imagens** distribuídas ao longo do conteúdo, com marcação de onde inserir (`[IMAGEM: nome-da-imagem]`).

### Formato da descrição

```markdown
### Imagem [N]: [nome-da-imagem]

**Posição no texto:** [Seção onde a imagem deve aparecer]
**Tipo de imagem:** [diagrama técnico / ilustração conceitual / infográfico / capa do módulo]

**Prompt para NanaBanana Pro:**
> [Descrição detalhada em inglês, com:
>  - Estilo visual (ex: flat design, isometric, tech illustration)
>  - Elementos principais presentes na imagem
>  - Paleta de cores sugerida
>  - Mood/atmosfera (ex: professional, energetic, clean)
>  - Elementos de texto ou labels se necessário
>  - Formato/proporção recomendado (ex: 16:9 landscape, 1:1 square)
>  Mínimo 50 palavras, máximo 150 palavras]

**Descrição em português (para referência):**
[Explicação breve de o que a imagem representa para o aluno]
```

### Exemplo de prompt para NanaBanana Pro

```
Tech illustration in flat design style showing a computer network diagram. 
Central server rack in the middle connected to 5 client computers arranged in a star 
topology. Each connection shown as colorful fiber optic cables (blue, green, orange). 
Small icons representing data packets floating along the cables. Clean white background 
with subtle grid pattern. Color palette: deep blue (#1E3A5F), electric blue (#0099FF), 
light gray (#F5F5F5). Professional corporate mood. Labels in clean sans-serif font 
identifying each component. 16:9 landscape format. No people, no text beyond labels.
```

---

## 6. Nomenclatura e Saída dos Arquivos

Para cada módulo gerado, salve o arquivo com o padrão:

```
modulo-[NN]-[slug-do-titulo].md
```

Exemplos:
- `modulo-01-introducao-redes.md`
- `modulo-02-modelo-osi.md`
- `modulo-03-protocolos-tcp-ip.md`

O orquestrador também gera um **arquivo índice** do curso:

```
indice-[nome-do-curso].md
```

Com a estrutura:

```markdown
# [Nome do Curso] — Índice de Módulos

| Módulo | Título | Arquivo | Status |
|--------|--------|---------|--------|
| 01 | [Título] | modulo-01-xxx.md | ✅ Gerado |
| 02 | [Título] | modulo-02-xxx.md | ✅ Gerado |
```

---

## 7. Tom e Estilo de Escrita

- **Linguagem:** Português brasileiro, informal mas profissional
- **Tuteiamento:** Sempre "você", nunca "o aluno" ou "os estudantes"
- **Parágrafos:** Curtos (3–5 linhas). Evite blocos densos de texto
- **Analogias:** Use com frequência. Conecte conceitos técnicos a situações do dia a dia
- **Exemplos:** Sempre práticos, preferindo cenários reais de mercado
- **Jargão:** Explique na primeira ocorrência. Use negrito no termo técnico
- **Código/Comandos:** Use blocos de código sempre que houver exemplos práticos
- **Emojis:** Use com moderação nos títulos e elementos de engajamento (não no corpo do texto corrido)

### Exemplo de escrita esperada

❌ **Evite:**
> "O modelo OSI é um framework conceitual que padroniza as funções de comunicação de um sistema de telecomunicações ou de computação sem considerar a tecnologia subjacente e a estrutura interna."

✅ **Prefira:**
> "Sabe quando você manda uma mensagem pelo WhatsApp e ela chega certinha no celular do seu amigo? Por baixo dos panos, tem uma série de processos acontecendo — e o Modelo OSI é justamente o 'mapa' que organiza tudo isso em 7 camadas bem definidas. Pensa nele como as etapas de preparação de um pedido em uma pizzaria: cada andar cuida de uma parte do processo."

---

## 8. Referências Adicionais

Consulte os seguintes arquivos de referência quando necessário:

- `references/template-modulo.md` — Template completo de um módulo de exemplo
- `references/checklist-orquestrador.md` — Checklist detalhado de revisão

---

## 9. Fluxo de Execução Resumido

```
1. Coletar dados da ementa e confirmar com usuário
2. Para cada módulo:
   a. Acionar Agente de Módulo com briefing completo
   b. Agente gera rascunho completo
   c. Orquestrador revisa checklist
   d. Orquestrador corrige/complementa se necessário
   e. Salvar arquivo final modulo-NN-titulo.md
3. Gerar arquivo índice indice-[curso].md
4. Apresentar ao usuário com resumo do que foi gerado
5. Sugerir execução da skill ebook-auditor para validação
```
