# Fabiana Sidoruk — Design System

> Fonte da verdade visual da Sala. Toda peça (capa de reel, carrossel, story, legenda de vídeo, Google Perfil da Empresa) sai daqui. **Nenhuma cor que não esteja neste arquivo entra numa peça.**
>
> **Como foi montado (27/10/2026):** a paleta e as fontes foram lidas direto do código do site no ar (fabianasidoruk.com.br, variáveis `--brand`, `--cream`, `--terracotta` etc.). O monograma e a assinatura foram recortados dos carrosséis que ela já publica. O feed hoje mistura três estilos; este arquivo escolhe um e aposenta os outros dois.
>
> **Guia visual:** abra `design-system/guia-visual.html` no navegador. **Tokens prontos para HTML:** `design-system/tokens.css`.

---

## 1. Logo e assinatura

Arquivos em `design-system/logo/`:

| Arquivo | O que é | Quando usar |
|---|---|---|
| `assinatura-fabiana-referencia.png` | Monograma FS caramelo + "Fabiana Sidoruk" em script oliva + "PSICÓLOGA" | Referência da assinatura completa. Último slide do carrossel, capa do Google |
| `monograma-fs-referencia.png` | Monograma FS em traço branco sobre caramelo | Referência do símbolo. Topo do carrossel, avatar, marca d'água |

Regras:
- Os dois arquivos são **recortes de post** (200–540 px). Servem como referência, não pra impressão. **Pedir à Fabiana o arquivo original do logo** (PNG transparente ou SVG) — quem fez o site ou a agência de vídeo deve ter.
- Até chegar o original, a assinatura em peça nova é montada em texto: "Fabiana Sidoruk" em **Birthstone** (a mesma script do site) + "PSICÓLOGA · CRP 07/40773" em DM Sans 500 caixa alta.
- O monograma vai **pequeno** (máx. 64 px num slide de 1080). Ele assina, não decora.
- **CRP em toda peça** que fale do serviço (exigência ética da profissão).

## 2. Paleta

| Token | Hex | Origem | Uso |
|---|---|---|---|
| `--oliva` | `#606C38` | site (`--brand`) | Cor da marca. Títulos em fundo claro, slide escuro, botão |
| `--caramelo` | `#D7B892` | site (`--brand-soft`) | Monograma, faixa de destaque, fundo de slide de pausa |
| `--creme` | `#FFFBF0` | site (`--cream`) | Fundo principal de peça clara |
| `--creme-2` | `#F5EFE0` | site (`--cream-alt`) | Cartão dentro do fundo creme, slide alternado |
| `--terracota` | `#C97A63` | site (`--terracotta`) | Detalhe pequeno: fio, ícone, marcador. Nunca texto corrido |
| `--terracota-escuro` | `#A65A4D` | site (`--terracotta-dark`) | Palavra de destaque em texto sobre creme |
| `--tinta` | `#2C2C2C` | site (`--ink`) | Texto corrido; fundo da caixa de legenda |
| `--cinza` | `#5B5B5B` | site (`--muted-foreground`) | Texto de apoio, fonte, rodapé |
| `--branco` | `#FFFFFF` | — | Texto sobre foto escurecida e sobre oliva |

Combinações aprovadas (contraste WCAG):
- `--tinta` sobre `--creme` (13,5:1) → corpo de texto.
- `--oliva` sobre `--creme` (5,5:1) ou `--creme-2` (4,9:1) → título e corpo.
- `--creme`/`--branco` sobre `--oliva` (5,5–5,7:1) → qualquer texto.
- `--tinta` sobre `--caramelo` (7,4:1) → qualquer texto.
- `--terracota-escuro` sobre `--creme` (4,8:1) → palavra de destaque.

**Proibido (contraste reprovado):**
- **Branco sobre caramelo (1,9:1).** É o carrossel nude que ela posta hoje: o texto quase some. Sobre caramelo, o texto é `--tinta`.
- Oliva sobre caramelo (3,0:1) e terracota sobre creme (3,1:1) → só pra elemento gráfico, nunca texto.
- Verde do WhatsApp (`#25D366`) fora do botão do site. Preto puro, branco puro como fundo, degradê, azul, vermelho.

## 3. Tipografia

| Papel | Fonte | Peso | Estilo |
|---|---|---|---|
| Assinatura (nome) | Birthstone | 400 | Só no nome "Fabiana Sidoruk". **Nunca em título ou frase** |
| Título de capa e de slide | DM Sans | 600 | Normal, caixa normal, entrelinha 1.1, tracking −0,02em |
| Corpo | DM Sans | 400 | 34–40 px no slide 1080, entrelinha 1.4 |
| Label / CRP / numeração | DM Sans | 500 | Caixa alta, tracking +0,14em, 22–26 px |
| Legenda de vídeo | DM Sans | 600 | Branco, 1–4 palavras por vez, sem caixa de fundo |

**Destaque é cor, não itálico.** A palavra que importa vai em `--terracota-escuro` (fundo claro) ou `--caramelo` (fundo oliva/foto). O título em serifada pesada itálica dos carrosséis antigos sai.

O site usa Birthstone nos títulos (h1/h2) e isso fica difícil de ler em frase longa. Nas peças de rede social ela fica restrita ao nome. Sugestão pro site, quando for mexido: títulos em DM Sans 600, Birthstone só no logo.

## 4. Aplicação em peças

### Capa de reel (1080×1920, área segura 1080×1350 no centro)
- Rosto dela no consultório, plano médio-fechado, sempre no mesmo ponto da sala (fundo de sofá verde ou estante).
- Título de **até 6 palavras**, DM Sans 600 branco, 84–96 px, centralizado na altura do peito. Sombra suave `0 2px 24px rgba(44,44,44,.35)`.
- Sem selo, sem moldura, sem filtro de cor. A série reconhecível vem de repetir enquadramento e posição do título (modelo Lívia Oliveira).

### Legenda de vídeo (queimada)
- DM Sans 600, branco, 1–4 palavras por vez, centro-baixo (≈ 62% da altura), sem caixa.
- Palavra-chave da frase pode entrar em `--caramelo`. Uma por frase, no máximo.
- Nada de b-roll, trilha ou filtro por padrão (ver `spy/MODELAGEM-REFERENCIAS.md` §3).

### Carrossel (1080×1350) — dois modelos, só estes dois
**A. Frase sobre foto** (modelo Yasmin Martins)
- Foto real em tela cheia (consultório, livros, janela, Porto Alegre), escurecida com `rgba(44,44,44,.5)` (abaixo disso o caramelo some em foto clara).
- Uma frase por slide, DM Sans 600 branco, 64–72 px, alinhada à esquerda.
- Palavra de destaque em `--caramelo`.
- Monograma FS pequeno no topo; assinatura em texto no rodapé.
- Pra série com frase-gatilho repetida (mesma abertura em todo slide, foto diferente).

**B. Texto em fundo chapado** (conteúdo explicativo)
- Fundo `--creme`, slides alternados em `--creme-2`; slide de virada em `--oliva` com texto `--creme`.
- Título DM Sans 600 `--oliva` 64 px; corpo DM Sans 400 `--tinta` 36 px.
- Fio de 4 px em `--terracota` acima do título como marcador de slide.
- Capa sempre com foto dela (modelo A) — o rosto para o scroll; o miolo é modelo B.

Margem: 80 px nas laterais, 96 px em cima e embaixo. Rodapé de todo slide: `@psifabianasidoruk` em label `--cinza`.

### Story (1080×1920)
Mesmo modelo B do carrossel, com respiro de 250 px em cima e embaixo (interface do Instagram).

### Google Perfil da Empresa
Foto do consultório e dela em atendimento simulado, sem texto por cima. Post semanal reaproveita a capa do reel.

## 5. Tom visual

**Usar:** fotos reais do consultório (sofá verde-sálvia, madeira clara, janela com luz natural, estante de livros), ela olhando pra câmera, Porto Alegre como paisagem. Luz quente e natural. Muito respiro.

**Evitar:**
- Ícone de cérebro, quebra-cabeça, mão segurando coração, silhueta triste, pessoa com mão na cabeça — imagem de sofrimento/sintoma vai contra a linha dela.
- Banco de imagem genérico.
- Foto de paciente, de sessão real, de qualquer pessoa identificável sem autorização.
- Filtro laranja/sépia e trocas de ângulo dos vídeos antigos.
- Os três estilos atuais misturados no mesmo grid.

---
*Base estrutural: Brand Book MktOps v2.0 · Canon v2026.14 · 2026-10-27*
