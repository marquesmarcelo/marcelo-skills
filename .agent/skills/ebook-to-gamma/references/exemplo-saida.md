# Instruções para Geração no Gamma.app
## Módulo: Introdução a Redes de Computadores

---

## ⚙️ Configurações Iniciais do Gamma

Antes de colar o prompt, configure o Gamma com os seguintes parâmetros:

| Parâmetro | Valor | Onde configurar |
|-----------|-------|----------------|
| **Formato** | Presentation | Seletor de tipo ao criar |
| **Proporção** | 16:9 | Card Options → Dimensions |
| **Tema** | Carbon | Theme selector |
| **Modo de texto** | Generate | Text Mode |
| **Quantidade de texto** | Medium | Text Options → Amount |
| **Audiência** | University students and IT professionals | Text Options → Audience |
| **Tom** | Educational, conversational | Text Options → Tone |
| **Fonte de imagens** | AI Generated | Image Options → Source |
| **Estilo de imagem** | Illustration | Image Options → Style Preset |
| **Idioma** | pt | Text Options → Language |

> 🎨 **Por que Carbon:** O tema escuro com acentos em azul elétrico transmite credibilidade técnica e reduz fadiga visual em aulas longas sobre infraestrutura de TI — ideal para um módulo introdutório de redes.

---

## 📋 Prompt Principal

Cole o texto abaixo integralmente no campo de input do Gamma ao criar uma nova apresentação:

---

**Título:** Introdução a Redes de Computadores

**Audiência:** Estudantes de graduação em cursos de TI e profissionais iniciando na área de infraestrutura

**Objetivo geral:** Ao final desta apresentação, o aluno será capaz de identificar os tipos de rede, reconhecer os componentes básicos de uma infraestrutura de rede e compreender a importância das redes para o trabalho em TI.

Crie uma apresentação profissional e didática com os seguintes slides, nesta ordem exata:

---

**SLIDE 1 — CAPA**
Título principal: "Introdução a Redes de Computadores"
Subtítulo: "Fundamentos de Infraestrutura de TI | Módulo 01"
Elemento visual: imagem de fundo com datacenter ou rede de cabos iluminados em azul, tom cinematográfico e profissional
Layout: título centralizado com destaque máximo, fundo escuro, tipografia bold

---

**SLIDE 2 — AGENDA**
Título: "O que veremos hoje"
Formato: lista numerada com ícones
Itens:
1. O que é uma rede de computadores
2. Tipos de rede: PAN, LAN, MAN e WAN
3. Componentes essenciais de uma rede
4. Com fio vs. Wi-Fi: quando usar cada um
5. Por que redes importam para sua carreira em TI

---

**SLIDE 3 — OBJETIVOS**
Título: "Ao final deste módulo, você vai conseguir:"
Formato: lista com ícones de check em verde
Itens:
- Definir o conceito de rede de computadores com suas próprias palavras
- Identificar os tipos de rede e seus casos de uso reais
- Descrever os componentes básicos: hosts, switches, roteadores e APs
- Distinguir redes com fio e sem fio e escolher a certa para cada cenário
- Relacionar redes com a infraestrutura de TI de empresas reais

---

**SLIDE 4 — O QUE É UMA REDE?**
Título: "Redes: a espinha dorsal da TI"
Conteúdo principal:
- Rede = dois ou mais dispositivos que trocam dados entre si
- Inclui computadores, servidores, celulares, impressoras, câmeras
- Objetivo: compartilhar recursos e informações com eficiência
- Base de TUDO em TI: cloud, segurança, DevOps, desenvolvimento
Exemplo: "Como o WhatsApp entrega sua mensagem em frações de segundo"
Elemento visual sugerido: diagrama de rede simples com dispositivos conectados
Layout: imagem à direita, bullets à esquerda

---

**SLIDE 5 — TIPOS DE REDE**
Título: "Qual rede é essa?"
Formato: 4 cards lado a lado (um por tipo)
Card 1 — PAN: Personal, Bluetooth/smartwatch, alcance de metros
Card 2 — LAN: Local, escritório/casa, rápida e barata
Card 3 — MAN: Metropolitana, cidade inteira, operadoras
Card 4 — WAN: Global, a própria internet, conecta continentes
Elemento visual sugerido: mapa de abrangência crescente em círculos concêntricos
Layout: grid de 4 colunas com ícone + título + descrição curta

---

**SLIDE 6 — COMPONENTES ESSENCIAIS**
Título: "Quem é quem em uma rede?"
Formato: dois painéis — lista à esquerda, diagrama à direita
Itens:
- **Hosts:** os dispositivos finais (computadores, servidores, celulares)
- **Switch:** "corretor de imóveis" — entrega dados para o destinatário certo
- **Roteador:** "carteiro internacional" — conecta redes diferentes
- **Access Point:** transmissor Wi-Fi separado do roteador em redes maiores
- **Cabeamento:** estradas físicas para os dados (par trançado, fibra óptica)
Elemento visual sugerido: diagrama de rede com labels identificando cada componente
Layout: imagem à direita ocupando 40% do slide

---

**SLIDE 7 — DESTAQUE: NÃO CONFUNDA!**
Formato: slide de alerta / callout visual
Título: "⚠️ Cuidado com esse erro clássico"
Conteúdo: Hub vs. Switch — O hub gritava para todos. O switch é inteligente.
Subtexto: Hubs são obsoletos. Em infraestruturas modernas, sempre use switch.
Elemento visual: comparação lado a lado (hub X vermelho vs switch ✓ verde)
Layout: fundo com cor de alerta (amarelo ou âmbar), tipografia bold central

---

**SLIDE 8 — COM FIO VS. WI-FI**
Título: "Cabo ou Wi-Fi: depende do contexto"
Formato: tabela comparativa
Colunas: Critério | Ethernet (Com Fio) | Wi-Fi (Sem Fio)
Linhas:
- Velocidade | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐
- Latência | ⭐⭐⭐⭐⭐ | ⭐⭐⭐
- Mobilidade | ❌ | ⭐⭐⭐⭐⭐
- Segurança | ⭐⭐⭐⭐⭐ | ⭐⭐⭐
- Custo instalação | Médio/Alto | Baixo
Dica abaixo da tabela: Servidores e estações fixas → sempre cabo. Reuniões e dispositivos móveis → Wi-Fi.
Layout: tabela centralizada com zebra-striping

---

**SLIDE 9 — REDES NA SUA CARREIRA**
Título: "Redes estão em todo lugar na TI"
Formato: grid de 4 cards com ícones de área
Card 1 — Dev: APIs, bancos remotos, microsserviços — tudo é rede
Card 2 — DevOps/SRE: firewalls, VPNs, load balancers, monitoramento
Card 3 — Segurança: 90% dos ataques entram pela rede
Card 4 — Cloud: toda nuvem é, no fundo, uma rede gigantesca
Elemento visual sugerido: mapa mental com "Rede" no centro e áreas irradiando
Layout: 2x2 grid de cards coloridos com ícone + título + 1 linha

---

**SLIDE 10 — RESUMO**
Título: "O que ficou?"
Formato: tabela de dois painéis
Coluna 1 — Conceito | Coluna 2 — Definição curta
- Rede de computadores | Dispositivos interconectados que trocam dados
- PAN | Rede pessoal, alcance de metros (Bluetooth)
- LAN | Rede local: escritório, casa
- MAN | Rede metropolitana: cidade inteira
- WAN | Rede ampla: a internet global
- Switch | Entrega dados para o destinatário certo na LAN
- Roteador | Conecta redes diferentes (LAN ↔ WAN)
Layout: tabela limpa com cabeçalho colorido

---

**SLIDE 11 — PRÓXIMOS PASSOS**
Título: "Por onde continuar?"
Formato: lista de ações com checkboxes visuais
Itens:
- ☐ Trace o mapa de rede da sua casa ou trabalho
- ☐ Execute `ipconfig` (Windows) ou `ifconfig` (Linux) e anote seu IP e gateway
- ☐ Pesquise o modelo do seu roteador e descubra quantas funções ele acumula
- ☐ Assista "How the Internet Works in 5 Minutes" no YouTube
Rodapé: "Próximo módulo: Modelo OSI e TCP/IP — a anatomia da comunicação em rede"
Layout: bullets grandes com checkbox visual, fundo levemente diferente do restante

[FIM DO PROMPT]

---

## 🖼️ Instruções de Imagem para o Gamma

Configure o modelo de imagem como **dall-e-3** e o style preset como **illustration** para todos os slides de conteúdo. Para o slide de capa, use **photorealistic**.

| Slide | Prompt de Imagem Sugerido (colar no campo de imagem do Gamma) |
|-------|---------------------------------------------------------------|
| Capa (Slide 1) | Photorealistic cinematic shot of a modern server room with illuminated ethernet cables in blue and white lights, slight motion blur on foreground cables suggesting data flow, dark background, dramatic lighting, 16:9 landscape, professional tech atmosphere, no people, no text |
| O que é uma Rede (Slide 4) | Flat design illustration showing a central hub icon connected to 5 diverse devices: desktop, laptop, smartphone, printer, and smart TV. Clean colorful connection lines with small packet icons floating along them. White background, electric blue and coral accents, 16:9 landscape, no text |
| Tipos de Rede (Slide 5) | Clean isometric infographic showing 4 concentric coverage rings from smallest to largest: a person (purple), a building (blue), a city skyline (teal), a globe (green). Each ring labeled and color-coded. Minimal white background, 1:1 square |
| Componentes (Slide 6) | Technical flat illustration of a complete office network: server rack, switch, router, access point, and 3 connected devices, each labeled with clean callout arrows. Deep blue and white color scheme, 16:9 landscape, no background clutter |
| Hub vs Switch (Slide 7) | Split comparison illustration. Left side (red, labeled "Hub"): broadcast arrows going to ALL devices indiscriminately. Right side (green, labeled "Switch"): single precise arrow to one specific device. Bold flat design, high contrast, 16:9 |
| Com Fio vs Wi-Fi (Slide 8) | Flat design split-screen. Left: desktop with ethernet cable, lock icon, lightning speed indicator. Right: laptop and phone with wifi signal waves, mobility arrows. Blue for wired, purple for wireless. Clean white background, 16:9 |
| Carreira (Slide 9) | Flat design mind map with "Network" in glowing center node, 4 branches to colored icons: code brackets (Dev), gear+server (DevOps), shield (Security), cloud (Cloud). Dark background with neon accent colors, tech atmosphere, 16:9 |

---

## 🔧 Ajustes Pós-Geração Recomendados

Após o Gamma gerar a apresentação:

1. **Slide 5 (Tipos de Rede):** Se o Gamma gerar como lista em vez de 4 cards, clique no card → "Change layout" → "4 columns"
2. **Slide 7 (Alerta):** Mude manualmente a cor de fundo do card para âmbar/amarelo via "Card background color" para dar destaque
3. **Slide 8 (Tabela):** Verifique se a tabela renderizou com zebra-striping; se não, selecione a tabela → "Format" → ativar "Alternate row colors"
4. **Slide 11 (Próximos Passos):** Adicione o link real do próximo módulo como hyperlink no rodapé
5. **Geral:** Revise se o tema Carbon está ativo em todos os cards (alguns podem ter sofrido override automático)

---

## 📤 Export Recomendado

| Uso | Formato | Como exportar |
|-----|---------|--------------|
| Aula presencial com projetor | `.pptx` | Share → Export → PowerPoint |
| Aula online / LMS | Link público + embed | Share → Publish → Copy embed code |
| Material de apoio impresso | `.pdf` | Share → Export → PDF |
| Thumbnail para divulgação | `.png` (Slide 1) | Share → Export → PNG |
