# Roteiro de Produção — Higgsfield
## Introdução a Redes de Computadores

---

## 🎬 Visão Geral da Produção

| Parâmetro | Valor |
|-----------|-------|
| **Modelo principal** | Cinema Studio Video 3.0 (`cinematic_studio_3_0`) |
| **Resolução** | 1080p |
| **Aspect ratio** | 16:9 |
| **Duração estimada** | ~4 minutos de vídeo final |
| **Total de cenas** | 9 cenas |
| **Voz (TTS)** | `Heitor (pt)` via Inworld TTS |
| **Estilo visual** | Cinematográfico técnico — azul profundo, iluminação dramática, ambientes de TI |

> 🎯 **Estratégia visual:** Cada conceito de rede é representado visualmente com metáforas do mundo físico — rodovias para dados, carteiros para roteadores, condomínios para redes locais — mantendo consistência cromática em azul elétrico e grafite ao longo de todo o vídeo.

---

## 🎙️ Configuração de Narração (Inworld TTS)

- **Modelo:** `inworld_text_to_speech`
- **Voz recomendada:** `Heitor (pt)` — masculina, profissional, clara, naturalidade brasileira
- **Alternativa feminina:** `Maitê (pt)` — calorosa, ideal para tom mais próximo e didático
- **Workflow:** Gere o áudio de cada cena individualmente → importe no editor de vídeo → sincronize com o vídeo gerado pelo Cinema Studio 3.0

---

## 🎞️ Roteiro Cena a Cena

---

### CENA 01 — Abertura: O Mundo Conectado
**Tipo:** Abertura
**Duração:** 6s
**Tópico do ebook:** Introdução geral

#### Prompt de Vídeo
```
Aerial cinematic shot slowly pulling back from a single glowing fiber optic cable
to reveal an entire global network of interconnected light threads spanning continents,
viewed from above like a living organism of light. The cables pulse with blue and
white data streams flowing in both directions. Background transitions from deep space
darkness to a subtle map of the Earth's surface. Camera begins extremely close on
one cable's glowing core, then smoothly dollies out over 6 seconds to reveal the
vast planetary network. Deep navy blue and electric blue color palette with bright
white highlight pulses. Atmosphere: awe-inspiring, epic, technological wonder.
Cinematic depth of field, lens flare on brightest nodes. No text, no people.
Cinematic quality, 1080p, 16:9 aspect ratio.
```

#### Configurações no Higgsfield
```
Modelo: cinematic_studio_3_0
Duração: 6s
Resolução: 1080p
Aspect ratio: 16:9
```

#### Narração (TTS — Inworld)
> "Cada vez que você manda uma mensagem, assiste a um vídeo ou faz uma videochamada, dados viajam por uma rede invisível que conecta bilhões de dispositivos ao redor do mundo. Neste módulo, você vai entender como essa rede funciona — do começo."

**Duração estimada da fala:** ~7s
**Ritmo:** moderado, com pausa após "mundo"

---

### CENA 02 — O Que é uma Rede?
**Tipo:** Conteúdo
**Duração:** 8s
**Tópico do ebook:** "O que é uma Rede de Computadores?"

#### Prompt de Vídeo
```
Smooth camera push-in toward a modern home office setup where a desktop computer,
laptop, smartphone, printer, and smart TV are all connected by glowing blue ethernet
cables and wifi signal arcs. Small luminous data packet cubes travel along the
connections in real time, each reaching its destination device. The room is warmly
lit from outside but the devices glow with cool blue digital light. Camera starts
at doorway level and slowly moves toward the central router on the desk, which
pulses like a heart sending signals outward. Clean, modern interior design.
Shallow depth of field on the router in the foreground. No text overlays, no UI.
Photorealistic style with cinematic color grading — deep blue shadows, warm
ambient fill. 1080p, 16:9.
```

#### Configurações no Higgsfield
```
Modelo: cinematic_studio_3_0
Duração: 8s
Resolução: 1080p
Aspect ratio: 16:9
```

#### Narração (TTS — Inworld)
> "Uma rede de computadores é qualquer conjunto de dispositivos conectados que conseguem trocar dados entre si. Pode ser o seu notebook e a impressora lá em casa, ou pode ser o data center de uma empresa conectando milhares de servidores. A lógica é sempre a mesma: dispositivos se comunicam para compartilhar informação."

**Duração estimada da fala:** ~10s
**Ritmo:** moderado

---

### CENA 03 — Analogia: O WhatsApp
**Tipo:** Exemplo / Analogia
**Duração:** 8s
**Tópico do ebook:** Analogia do WhatsApp

#### Prompt de Vídeo
```
Macro close-up of a smartphone screen showing an abstract message being sent,
represented as a glowing green bubble. The bubble lifts off the screen surface
and transforms into a stream of glowing data packets — tiny luminous cubes —
that travel through an abstract tunnel of fiber optic light, passing through
routers shown as glowing nodes, traversing underwater cables shown as giant
glowing pipes crossing a dark ocean floor, finally arriving at another
smartphone screen where a new message bubble materializes. The entire journey
shown in one continuous 8-second shot with smooth camera following the data
stream. Electric blue and green color palette. Dark background throughout.
Cinematic, sci-fi tech aesthetic. No text, no UI elements visible.
1080p, 16:9, cinematic quality.
```

#### Configurações no Higgsfield
```
Modelo: cinematic_studio_3_0
Duração: 8s
Resolução: 1080p
Aspect ratio: 16:9
```

#### Narração (TTS — Inworld)
> "Sabe quando você manda aquela figurinha no WhatsApp? Parece simples, mas por baixo dos panos seus dados atravessam roteadores, cabos de fibra óptica — às vezes cruzando oceanos inteiros — em frações de segundo. Tudo isso graças às redes."

**Duração estimada da fala:** ~8s
**Ritmo:** ágil no final

---

### CENA 04 — Tipos de Rede
**Tipo:** Conteúdo
**Duração:** 10s
**Tópico do ebook:** "Tipos de Rede: PAN, LAN, MAN, WAN"

#### Prompt de Vídeo
```
Elegant top-down isometric animation starting as a tight shot on a single person
wearing a smartwatch and earbuds — glowing purple connection arcs between devices
representing a PAN. Camera slowly zooms out to reveal the person inside an office
building where dozens of computers glow with blue LAN connections. Continue
zooming out to see the entire city block with fiber connections between buildings
in teal (MAN). Final pull-back to reveal the entire globe with satellite and
undersea cable connections in green (WAN). Each network layer appears with a
subtle color-coded glow as the camera reveals it — purple, blue, teal, green.
Smooth continuous camera movement, no cuts. Birds-eye perspective throughout.
Clean, minimal cityscapes. No text labels. Deep space background at final
zoom level. Cinematic quality, 1080p, 16:9.
```

#### Configurações no Higgsfield
```
Modelo: cinematic_studio_3_0
Duração: 10s
Resolução: 1080p
Aspect ratio: 16:9
```

#### Narração (TTS — Inworld)
> "As redes se classificam pela área que cobrem. A PAN é pessoal — cobre só você e seus dispositivos. A LAN é local — escritório, casa. A MAN cobre uma cidade inteira. E a WAN? É a internet — conecta o planeta. Cada uma com seu papel."

**Duração estimada da fala:** ~9s
**Ritmo:** moderado, com micro-pausa entre cada tipo

---

### CENA 05 — Componentes da Rede
**Tipo:** Conteúdo
**Duração:** 10s
**Tópico do ebook:** "Componentes de uma Rede"

#### Prompt de Vídeo
```
Cinematic slow orbit around a transparent isometric model of a modern network
infrastructure floating in dark space. The model shows: a server rack on the
left with blinking lights, connected via glowing cable to a central switch
(slightly elevated, shown as the "hub" of the scene), which connects to four
client computers and a printer arranged in a star pattern. A router sits at
the edge connecting to an external cloud symbol. Each component pulses softly
when "active". Camera performs a slow 180-degree orbit starting from the server
side and ending at the router, revealing the entire architecture. Electric blue
glow on all connection cables. Components are semi-transparent with internal
circuitry faintly visible. Dark dramatic background, slight fog effect.
No text overlays. Cinematic, tech-documentary style. 1080p, 16:9.
```

#### Configurações no Higgsfield
```
Modelo: cinematic_studio_3_0
Duração: 10s
Resolução: 1080p
Aspect ratio: 16:9
```

#### Narração (TTS — Inworld)
> "Toda rede tem personagens fixos. Os hosts são os dispositivos finais — computadores, servidores, celulares. O switch é o organizador local — ele sabe o endereço de cada um e entrega os dados certinho. O roteador conecta redes diferentes. E o access point distribui o Wi-Fi. Cada um no seu papel."

**Duração estimada da fala:** ~11s
**Ritmo:** pausado, um componente de cada vez

---

### CENA 06 — Destaque: Hub vs Switch
**Tipo:** Destaque / Alerta
**Duração:** 6s
**Tópico do ebook:** "⚠️ Atenção — Hub vs Switch"

#### Prompt de Vídeo
```
Split-screen cinematic shot divided by a vertical glowing dividing line.
LEFT SIDE (red-tinted, labeled with a warning glow): An old network hub
broadcasting identical signal beams chaotically to ALL connected devices
simultaneously — shown as red arrows scattering in all directions, causing
visual "noise" and interference. RIGHT SIDE (blue-tinted, clean): A modern
switch sending a single precise glowing blue beam directly to one specific
device, while others remain unlit and undisturbed. Camera slowly pushes in
toward the dividing line. The contrast between chaos and precision is the
visual story. No text. Dramatic red vs blue color war. Cinematic quality,
1080p, 16:9.
```

#### Configurações no Higgsfield
```
Modelo: cinematic_studio_3_0
Duração: 6s
Resolução: 1080p
Aspect ratio: 16:9
```

#### Narração (TTS — Inworld)
> "Um detalhe importante: não confunda switch com hub. O hub gritava para todo mundo ao mesmo tempo — péssimo para performance e segurança. O switch é inteligente: ele só manda o dado para quem precisa receber. Hoje, hubs não existem mais em redes modernas."

**Duração estimada da fala:** ~8s
**Ritmo:** ênfase em "inteligente"

---

### CENA 07 — Com Fio vs Wi-Fi
**Tipo:** Conteúdo comparativo
**Duração:** 8s
**Tópico do ebook:** "Redes com Fio vs. Sem Fio"

#### Prompt de Vídeo
```
Elegant split environment shot showing two sides of the same modern open-plan
office. LEFT HALF: A workstation with a server rack and desktop computer
connected by a thick ethernet cable. The connection glows solid blue —
stable, unwavering, with a "speed" indicator pulsing rapidly. A padlock
icon subtly floats above the connection. RIGHT HALF: Same office, but with
laptops and tablets floating at various angles, connected by wifi signal
arcs. The signals pulse intermittently, showing slight variations. A
person walks through the right half of the frame, carrying a tablet —
emphasizing mobility. Camera slowly slides from left to right, spending
equal time on each half. Warm corporate lighting, blue and purple split
color grade. No text. 1080p, 16:9, cinematic.
```

#### Configurações no Higgsfield
```
Modelo: cinematic_studio_3_0
Duração: 8s
Resolução: 1080p
Aspect ratio: 16:9
```

#### Narração (TTS — Inworld)
> "Com fio ou sem fio? A resposta é: depende. O cabo é mais rápido, mais estável e mais seguro — ideal para servidores e estações fixas. O Wi-Fi é mais prático para quem precisa de mobilidade. Na prática profissional, você vai usar os dois — cada um no lugar certo."

**Duração estimada da fala:** ~9s
**Ritmo:** moderado

---

### CENA 08 — Redes na Carreira de TI
**Tipo:** Conteúdo motivacional
**Duração:** 8s
**Tópico do ebook:** "Por que Redes Importam para Você Profissionalmente"

#### Prompt de Vídeo
```
Dynamic montage-style single continuous shot moving through four distinct tech
environments in sequence, each transitioning via a smooth camera push-through-a-wall
effect. Environment 1 (Dev): Programmer at multiple monitors with floating code
and API connection diagrams. Environment 2 (DevOps): Server room with rack lights
blinking, network traffic visualization on wall screens. Environment 3 (Security):
Dark room with a hacker-style screen showing firewall rules and intrusion alerts,
then a security analyst calmly navigating them. Environment 4 (Cloud): Abstract
visualization of cloud infrastructure — floating server icons connected globally.
Throughout: consistent electric blue tones, professional cinematic lighting.
Camera never stops moving. No text, faces blurred or not visible. 1080p, 16:9.
```

#### Configurações no Higgsfield
```
Modelo: cinematic_studio_3_0
Duração: 8s
Resolução: 1080p
Aspect ratio: 16:9
```

#### Narração (TTS — Inworld)
> "Não importa qual área de TI você escolha — redes vão estar lá. Desenvolvedor? Seus sistemas se comunicam por rede. DevOps? Você vai configurar firewalls e VPNs. Segurança? Noventa por cento dos ataques entram pela rede. Cloud? Cloud é rede em escala global. Entender redes não é opcional — é fundação."

**Duração estimada da fala:** ~11s
**Ritmo:** ágil, impactante, com ênfase em "não é opcional"

---

### CENA 09 — Encerramento e Próximos Passos
**Tipo:** Encerramento
**Duração:** 6s
**Tópico do ebook:** Próximos Passos

#### Prompt de Vídeo
```
Pull-back shot starting close on a single glowing network node — a small sphere
of electric light — then slowly expanding to reveal it as part of a beautiful
constellation of interconnected nodes forming a perfect network pattern in dark
space. As the camera pulls back, new nodes light up one by one, expanding the
network organically until it fills the frame. The pattern suggests growth and
potential. Warm golden light begins bleeding into the electric blue as the shot
ends — suggesting a new beginning. No text. Inspirational, hopeful, expansive.
Slow elegant camera movement. Deep space background. 1080p, 16:9, cinematic.
```

#### Configurações no Higgsfield
```
Modelo: cinematic_studio_3_0
Duração: 6s
Resolução: 1080p
Aspect ratio: 16:9
```

#### Narração (TTS — Inworld)
> "Você acaba de dar o primeiro passo no universo das redes. No próximo módulo, vamos descer um nível: o Modelo OSI e o TCP/IP — a gramática que toda rede fala. Até lá, experimente: abra o terminal, rode um ipconfig ou ifconfig e veja sua rede de perto."

**Duração estimada da fala:** ~9s
**Ritmo:** moderado, encerramento tranquilo

---

## 📋 Roteiro Completo de Narração

Textos consolidados para gerar todos os áudios no Inworld TTS (`Heitor (pt)`):

**Cena 01 — Abertura:**
> "Cada vez que você manda uma mensagem, assiste a um vídeo ou faz uma videochamada, dados viajam por uma rede invisível que conecta bilhões de dispositivos ao redor do mundo. Neste módulo, você vai entender como essa rede funciona — do começo."

**Cena 02 — O que é uma Rede:**
> "Uma rede de computadores é qualquer conjunto de dispositivos conectados que conseguem trocar dados entre si. Pode ser o seu notebook e a impressora lá em casa, ou pode ser o data center de uma empresa conectando milhares de servidores. A lógica é sempre a mesma: dispositivos se comunicam para compartilhar informação."

**Cena 03 — Analogia WhatsApp:**
> "Sabe quando você manda aquela figurinha no WhatsApp? Parece simples, mas por baixo dos panos seus dados atravessam roteadores, cabos de fibra óptica — às vezes cruzando oceanos inteiros — em frações de segundo. Tudo isso graças às redes."

**Cena 04 — Tipos de Rede:**
> "As redes se classificam pela área que cobrem. A PAN é pessoal — cobre só você e seus dispositivos. A LAN é local — escritório, casa. A MAN cobre uma cidade inteira. E a WAN? É a internet — conecta o planeta. Cada uma com seu papel."

**Cena 05 — Componentes:**
> "Toda rede tem personagens fixos. Os hosts são os dispositivos finais — computadores, servidores, celulares. O switch é o organizador local — ele sabe o endereço de cada um e entrega os dados certinho. O roteador conecta redes diferentes. E o access point distribui o Wi-Fi. Cada um no seu papel."

**Cena 06 — Hub vs Switch:**
> "Um detalhe importante: não confunda switch com hub. O hub gritava para todo mundo ao mesmo tempo — péssimo para performance e segurança. O switch é inteligente: ele só manda o dado para quem precisa receber. Hoje, hubs não existem mais em redes modernas."

**Cena 07 — Com Fio vs Wi-Fi:**
> "Com fio ou sem fio? A resposta é: depende. O cabo é mais rápido, mais estável e mais seguro — ideal para servidores e estações fixas. O Wi-Fi é mais prático para quem precisa de mobilidade. Na prática profissional, você vai usar os dois — cada um no lugar certo."

**Cena 08 — Carreira:**
> "Não importa qual área de TI você escolha — redes vão estar lá. Desenvolvedor? Seus sistemas se comunicam por rede. DevOps? Você vai configurar firewalls e VPNs. Segurança? Noventa por cento dos ataques entram pela rede. Cloud? Cloud é rede em escala global. Entender redes não é opcional — é fundação."

**Cena 09 — Encerramento:**
> "Você acaba de dar o primeiro passo no universo das redes. No próximo módulo, vamos descer um nível: o Modelo OSI e o TCP/IP — a gramática que toda rede fala. Até lá, experimente: abra o terminal, rode um ipconfig ou ifconfig e veja sua rede de perto."

---

## 🔧 Workflow de Produção Recomendado

### Passo 1 — Gerar áudios de narração
1. Acesse Higgsfield → Generate Audio → **Inworld TTS**
2. Cole cada texto do roteiro acima
3. Voz: `Heitor (pt)`
4. Gere e baixe cada arquivo (9 arquivos de áudio)

### Passo 2 — Gerar os vídeos
1. Acesse Higgsfield → Generate Video → **Cinema Studio Video 3.0**
2. Cole o prompt de cada cena
3. Configurações: 1080p, 16:9, duração conforme roteiro
4. Gere cena por cena (9 vídeos)

### Passo 3 — Edição final
1. Importe os 9 vídeos e 9 áudios em CapCut ou DaVinci Resolve
2. Ordene na sequência (Cenas 01 → 09)
3. Sincronize narração com imagem — ajuste cortes onde necessário
4. Duração total esperada: ~4–4,5 minutos

### Passo 4 — Música de fundo (opcional)
Use **Sonilo Music** no Higgsfield:
- **Prompt:** `Ambient electronic background music for educational tech video. Subtle, professional, not distracting. Soft synthesizers, gentle rhythm, modern corporate tone. No vocals.`
- **Duração:** 270s (4,5 minutos)
- **Mix:** -15dB para não cobrir a voz
