# Introdução a Redes de Computadores
### Fundamentos de Infraestrutura de TI | Módulo 01 de 08

---

> 📌 **Neste módulo você vai:**  
> - Entender o que são redes de computadores e por que elas importam no dia a dia
> - Conhecer os principais tipos de rede (LAN, MAN, WAN) e quando cada uma é usada
> - Descobrir como os dispositivos se comunicam e por que isso é a base de tudo em TI

---

## 🎯 Introdução

Você já parou pra pensar no que acontece nos bastidores quando você manda aquela figurinha no WhatsApp? Parece simples do seu lado — aperta o botão, a figurinha vai. Mas por baixo dos panos, acontece uma dança incrível de dados viajando por cabos, sinais sem fio, roteadores e protocolos que trabalham juntos em frações de segundo.

Redes de computadores são exatamente isso: a infraestrutura invisível que conecta dispositivos e permite que a informação flua de um ponto a outro. E aqui vai um spoiler: **tudo que você vai aprender ao longo desse curso depende desse conceito fundamental**. Sem redes, não tem cloud, não tem segurança, não tem DevOps. É a fundação da casa.

Neste módulo, a gente vai dar aquela primeira olhada geral no universo das redes — sem medo, sem formalidade excessiva, e com bastante exemplo do mundo real. Bora lá?

---

## 🏁 Objetivos de Aprendizagem

Ao finalizar este módulo, você será capaz de:

1. **Definir** o conceito de rede de computadores com suas próprias palavras
2. **Identificar** os principais tipos de rede (LAN, MAN, WAN, PAN) e seus casos de uso
3. **Descrever** os componentes básicos de uma rede (hosts, switches, roteadores, cabos)
4. **Distinguir** redes com fio e sem fio e suas vantagens em diferentes cenários
5. **Relacionar** o conceito de rede com a infraestrutura de TI de empresas reais

---

## 📚 Conteúdo

### O que é uma Rede de Computadores?

De forma bem direta: uma **rede de computadores** é um conjunto de dois ou mais dispositivos interconectados que conseguem trocar dados entre si. Esses dispositivos podem ser computadores, celulares, impressoras, câmeras de segurança, servidores — qualquer coisa que consiga se comunicar digitalmente.

A ideia central é simples: em vez de cada dispositivo viver numa ilha, eles se conectam para compartilhar recursos. Precisa imprimir? Não precisa de uma impressora por pessoa — uma na rede atende a todos. Precisa acessar um arquivo? Ele pode estar num servidor central, acessível por qualquer máquina autorizada.

[IMAGEM: diagrama-rede-basica]

> 💬 **Curiosidade**  
> A primeira rede de computadores do mundo foi a **ARPANET**, criada em 1969 pelo Departamento de Defesa dos EUA. O primeiro "login" da história? Travou no meio. O sistema só conseguiu enviar as letras "L" e "O" antes de cair. Ironicamente, mandou "LO" — que em inglês pode ser lido como "hello" (olá). Um acidente histórico que virou lenda! 😄

---

### Tipos de Rede: Qual é Qual?

O tamanho importa — pelo menos quando falamos de redes. A classificação mais comum leva em conta a **abrangência geográfica**:

#### PAN — Personal Area Network

A menor de todas. É a rede que se forma ao redor de você mesmo — tipo quando você conecta o fone Bluetooth no celular ou sincroniza o smartwatch. Alcance de poucos metros.

#### LAN — Local Area Network

A queridinha das empresas e casas. Cobre um ambiente físico limitado: um escritório, um andar de prédio, uma residência. É rápida, relativamente barata e fácil de gerenciar. Quando você conecta o notebook no Wi-Fi de casa, está numa LAN.

> 💡 **Dica**  
> Na prática profissional, quando alguém fala "a rede caiu", quase sempre está se referindo a problemas na LAN — seja no switch, no roteador local ou no ponto de acesso Wi-Fi. Saber diagnosticar a LAN é habilidade essencial de qualquer profissional de TI.

#### MAN — Metropolitan Area Network

Cobre uma cidade ou região metropolitana. Menos comum no dia a dia, mas muito usada por operadoras de telecom para interligar bairros ou diferentes unidades de uma mesma empresa espalhadas pela cidade.

#### WAN — Wide Area Network

A internet é o exemplo mais famoso de WAN. Cobre países, continentes, o planeta inteiro. A sua conexão doméstica com a internet é, na prática, sua LAN se conectando à WAN global através do seu provedor de internet (ISP).

[IMAGEM: comparacao-tipos-rede]

> 🔍 **Saiba Mais**  
> Quer ver um mapa em tempo real do tráfego da internet global?
> - **Akamai Real-Time Web Monitor**: https://www.akamai.com/us/en/resources/visualizing-akamai/real-time-web-monitor.jsp
> - **Internet Exchange Maps**: https://www.internetexchangemap.com — mostra onde as redes do mundo se encontram fisicamente

---

### Componentes de uma Rede

Uma rede não é só cabo e Wi-Fi. Ela tem uma série de componentes com papéis bem definidos:

**Hosts (Dispositivos Finais)**  
São os "moradores" da rede — computadores, servidores, smartphones, impressoras. Qualquer dispositivo que gera ou consome dados.

**Switch**  
O "corretor de imóveis" da rede local. Ele sabe o endereço de cada dispositivo conectado a ele e garante que os dados cheguem no destinatário certo, sem ficar gritando pra todo mundo.

> ⚠️ **Atenção**  
> Não confunda **switch** com **hub** (que é um equipamento antigo e obsoleto). O hub enviava os dados para TODOS os dispositivos da rede — péssimo para performance e segurança. O switch é inteligente: manda só para quem precisa receber. Hubs não são mais usados em infraestruturas modernas.

**Roteador (Router)**  
O "carteiro internacional". Enquanto o switch cuida do tráfego local, o roteador é responsável por encaminhar os dados entre redes diferentes — por exemplo, da sua LAN para a internet (WAN).

**Access Point (AP)**  
O transmissor de Wi-Fi. Em redes maiores, é separado do roteador. Em casa, o seu "roteador Wi-Fi" normalmente já tem tudo integrado: roteador + switch + access point num só equipamento.

**Cabeamento e Meios Físicos**  
Os "estradas" por onde os dados trafegam. Podem ser cabos de par trançado (o famoso cabo de rede), fibra óptica (para longas distâncias ou altíssimas velocidades) ou ondas de rádio (Wi-Fi, Bluetooth, 4G/5G).

> 🚀 **Desafio**  
> Trace o mapa da rede onde você está agora. Quantos dispositivos estão conectados? Tem switch ou só roteador? O Wi-Fi e o cabo compartilham o mesmo roteador? Desenhe num papel mesmo — isso vai fixar os conceitos muito melhor do que só ler!

---

### Redes com Fio vs. Sem Fio

A batalha clássica da TI moderna: cabo ou Wi-Fi?

A resposta honesta é: **depende do contexto**. Cada um tem seus pontos fortes:

| Critério | Com Fio (Ethernet) | Sem Fio (Wi-Fi) |
|----------|-------------------|-----------------|
| Velocidade | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| Latência | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ |
| Mobilidade | ❌ | ⭐⭐⭐⭐⭐ |
| Segurança | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ |
| Custo de instalação | Médio/Alto | Baixo |
| Interferências | Mínima | Moderada |

[IMAGEM: cabeamento-vs-wifi]

> 💡 **Dica**  
> Em ambientes críticos (data centers, servidores, estações de trabalho fixas), **sempre prefira cabo**. O Wi-Fi é ótimo para mobilidade, mas não para confiabilidade em sistemas que precisam de disponibilidade máxima. Muitos problemas de "rede instável" em empresas são simplesmente causados por servidores conectados via Wi-Fi.

---

### Por que Redes Importam para Você Profissionalmente?

Independente de qual área de TI você escolha, redes estão em todo lugar:

- **Desenvolvedor?** Seus sistemas vão se comunicar via API, banco de dados remoto, microsserviços — tudo rede.
- **DevOps/SRE?** Você vai configurar firewalls, load balancers, VPNs e monitorar latência.
- **Segurança?** 90% dos ataques entram pela rede. Entender o que trafega é obrigação.
- **Cloud?** Toda nuvem é, na essência, uma infraestrutura de rede gigantesca.

> 🔍 **Saiba Mais**  
> Quer uma visão geral de como as grandes empresas pensam em rede?
> - **Cisco Networking Academy** (gratuito): https://www.netacad.com — cursos introdutórios excelentes
> - **Livro gratuito**: "Computer Networking: A Top-Down Approach" — Kurose & Ross (tem versão em PDF disponível em bibliotecas universitárias)

---

## 🗺️ Resumo

Chegamos ao fim do Módulo 01! Você deu o primeiro passo em direção a entender a infraestrutura que sustenta praticamente tudo na TI moderna. Aqui está o que a gente cobriu:

| Conceito | O que você aprendeu |
|----------|-------------------|
| Rede de computadores | Conjunto de dispositivos interconectados que trocam dados |
| Tipos de rede | PAN (pessoal), LAN (local), MAN (metropolitana), WAN (ampla) |
| Componentes | Hosts, switches, roteadores, access points, cabos |
| Com fio vs. sem fio | Cada um tem vantagens — contexto define a escolha |
| Relevância profissional | Redes estão presentes em todas as especialidades de TI |

---

## 🚀 Próximos Passos

Você já tem a visão geral. Agora é hora de fixar e se preparar para o que vem a seguir!

- [ ] Trace o mapa da rede da sua casa ou trabalho (tipo de rede, equipamentos, conexões)
- [ ] Acesse o terminal do seu computador e rode o comando `ipconfig` (Windows) ou `ifconfig` (Linux/Mac) — anote seu IP, máscara e gateway
- [ ] Pesquise o modelo do roteador que você usa e descubra: ele é só roteador, ou tem switch e AP integrados?
- [ ] Assista o vídeo "How the Internet Works in 5 Minutes" no YouTube — é um clássico e vai reforçar tudo que vimos aqui

> 👉 **Próximo módulo:** Modelo OSI e TCP/IP — a gente vai descer para as entranhas da comunicação em rede e entender por que os dados chegam no lugar certo (quase sempre 😄)

---

## 🖼️ Imagens Sugeridas

### Imagem 1: diagrama-rede-basica

**Posição no texto:** Seção "O que é uma Rede de Computadores?"  
**Tipo de imagem:** Diagrama técnico / ilustração conceitual

**Prompt para NanaBanana Pro:**
> Flat design tech illustration showing a simple computer network diagram. Central office building icon connected to 4 different devices: a desktop computer, a laptop, a smartphone, and a printer, all connected by clean lines representing network cables. Small data packet icons (colorful squares) floating along the connection lines to represent data transfer. Minimalist white background with very subtle light blue grid. Color palette: deep navy blue (#1A2B4A), bright electric blue (#0077FF), coral accent (#FF5A5F), light gray (#F8F9FA). Clean sans-serif labels identifying each device. Professional and friendly atmosphere. 16:9 landscape format. No people.

**Descrição em português:** Diagrama básico mostrando como dispositivos diferentes se conectam numa rede local simples.

---

### Imagem 2: comparacao-tipos-rede

**Posição no texto:** Seção "Tipos de Rede: Qual é Qual?"  
**Tipo de imagem:** Infográfico

**Prompt para NanaBanana Pro:**
> Clean infographic in isometric flat design style showing four concentric network coverage zones from smallest to largest. Innermost zone: a person with phone and smartwatch (PAN, labeled "PAN - Personal"). Second zone: a house/office building (LAN, labeled "LAN - Local"). Third zone: a city skyline silhouette (MAN, labeled "MAN - Metropolitan"). Outermost zone: a globe with satellite (WAN, labeled "WAN - Wide"). Each zone has a distinct color: purple for PAN, blue for LAN, teal for MAN, green for WAN. Arrows showing the scale increase. Clean white background. Bold sans-serif typography for labels. 1:1 square format suitable for content illustration.

**Descrição em português:** Infográfico visual mostrando a abrangência geográfica crescente dos tipos de rede, do PAN ao WAN.

---

### Imagem 3: cabeamento-vs-wifi

**Posição no texto:** Seção "Redes com Fio vs. Sem Fio"  
**Tipo de imagem:** Ilustração comparativa

**Prompt para NanaBanana Pro:**
> Split-screen flat design illustration comparing wired and wireless networks. Left side (labeled "Ethernet — Wired"): a server rack connected to a desktop computer via a clean ethernet cable, showing lightning bolt speed icon and lock security icon. Right side (labeled "Wi-Fi — Wireless"): the same setup but with wireless signal waves instead of cable, with a laptop and smartphone, showing mobility arrows. Both sides use the same color palette but with a subtle dividing line in the center. Style: modern tech illustration, flat with subtle shadows. Colors: blue (#0066CC) for wired side, purple (#6B35CC) for wireless side. White background. 16:9 landscape format.

**Descrição em português:** Comparação visual lado a lado entre rede cabeada e Wi-Fi, destacando os pontos fortes de cada uma.
