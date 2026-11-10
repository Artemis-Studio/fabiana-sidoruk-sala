# Sala de Operações MktOps — Fabiana Sidoruk

> Esta é a Sala de Operações MktOps da **Fabiana Sidoruk**, operada via Claude Code. Quando você roda `claude` nesta pasta, lê este arquivo primeiro e segue estas regras.
>
> **Camada CANON (`.claude/`, `copy-routing.md`, `cerebro-de-copy/`, `automacao/`, `playbook-narrativas-mktops.md`, `design-system/_base/`) é herdada e versionada — snapshot `v2026.14`. Não reescrever.**

---

## ⚠️ REGRA 0 — NOME E RESTRIÇÕES DA Fabiana Sidoruk

A cliente é **Fabiana Sidoruk** (nome profissional completo: Fabiana Dias Sidoruk Reichenbach), psicóloga, **CRP 07/40773**. Instagram @psifabianasidoruk. Não chamar de "doutora" em copy (não é título dela).

Restrições que valem pra TODA peça (detalhe em `brand-context.md` §9):

1. **Nunca sintoma nem transtorno** — escolha dela, não só do CFP. Nada de "sinais de que…", ansiedade, depressão, insônia, burnout, TDAH, nem em hashtag. Fala de relação, história e escolha.
2. **Nunca prometer cura nem resultado**, nem prazo.
3. **Nunca preço, valor, gratuidade, desconto, sorteio ou promoção.**
4. **Nunca expor paciente:** sem caso clínico (nem disfarçado), sem depoimento, sem print, sem "uma paciente me disse".
5. **Nunca comparar** com colegas, clínicas ou plataformas.
6. **CRP 07/40773** em toda peça que fale do serviço.
7. **Anúncio Meta:** sem copy que insinue condição de saúde do leitor ("você que sofre com…").
8. **Atendimento infantil:** não oferecer até ela confirmar.
9. **Sem política partidária.**

**Visual:** só a paleta e as fontes de `design-system/design-system.md` (oliva `#606C38`, caramelo `#D7B892`, creme `#FFFBF0`; DM Sans + Birthstone só no nome). A paleta MktOps do `_base/` é referência de estrutura, não de cor.
**Vídeo:** ela falando é o fio do vídeo, com legenda dinâmica e sem trilha. Clipes de vídeo curtos (1–3 s, corte seco) ilustram a frase, somando no máximo ~35% do reel, e o primeiro entra até 3 s. Nada de clínica, sofrimento ou gente olhando pra câmera nos clipes. Modelos aprovados em `entregas/2026-10/reels/`.

**Antes de produzir qualquer copy, ler `brand-context.md` na raiz desta pasta.**

---

## ⚠️ REGRA 1 — SKILLS PRIMEIRO (OBRIGATÓRIO)

Você tem o catálogo completo de skills em `.claude/skills/`. NUNCA escreva do zero o que uma skill já sabe fazer:

1. Identificar o tipo de tarefa
2. Consultar o mapeamento de tarefas → skills
3. Ler o `SKILL.md` da skill aplicável
4. Executar usando a skill

Se nenhuma skill cobrir → execute manualmente e diga por quê.

---

## ⚠️ REGRA 2 — GATES SEMPRE ATIVOS (FORÇADO POR HOOK)

Toda copy — anúncios, carrosséis, emails, artigos, roteiros, landing pages, legendas — passa pela skill `copywriting-guardrails` como camada final antes de entregar. Elimina vícios de IA (antítese vazia, paradiastole, climax degenerado, bomphiologia, sententia falsa). Copy de ads passa **também** por `copy-format-check`.

**Isso não depende de ninguém lembrar.** Um hook `Stop` (`.claude/settings.json` → `hooks/guardrails-gate.sh`) **bloqueia a finalização do turno** se uma peça for escrita em `conteudo/` ou `entregas/` sem o `copywriting-guardrails` ter rodado. Para finalizar: rode o guardrails sobre a peça. Se o arquivo não for copy de marketing, não o salve em `conteudo/`/`entregas/`.

---

## ⚠️ REGRA 3 — FORMATO DE ENTREGA DE ADS ESTÁTICOS

Todo ad estático (Meta, LinkedIn, TikTok, Microsoft) entrega **somente o texto**:

```
## #N Ad
**Headline:** …
**Subheadline:** …
**Descrição:** …   ← só quando necessária pra coesão
**CTA:** …
```

Proibido no arquivo final: "Conceito"/"Por que funciona", "Sugestão visual"/briefing de imagem, primary text duplicando descrição, tabelas resumo, comentário sobre a copy. Explicação de estratégia é no chat, não no arquivo.

---

## ⚠️ REGRA 4 — CÉREBRO DE COPY (AUTO-LOAD POR TIPO DE PEÇA)

Esta Sala carrega o **Cérebro de Copy completo** em `cerebro-de-copy/` (14 arquivos + `_INDEX`) — a camada que faz a copy ficar boa (Sultanic, Settle, Fladlien, Rogers, Harris, Orzechowski, One Page 2.0, Schopenhauer). **Skills executam. O Cérebro pensa.**

**Ativação automática (a skill puxa sozinha, sem frase mágica):** o STEP 0 de toda tarefa de copy é abrir `copy-routing.md` (raiz desta Sala), achar o tipo da peça e **carregar os arquivos do Cérebro listados** antes de escrever. Não esperar o usuário pedir "use o Cérebro".

**Um flag, dois níveis:**
- **Rotina** (default): peça de manutenção → carrega a coluna Rotina da tabela.
- **Estratégica** (lançamento, posicionamento, oferta nova, VSL longa, peça-chave): carrega a coluna Estratégica completa. Na dúvida, suba para Estratégica.

`11-anti-padroes` entra SEMPRE. Fluxo canônico de peça nova em `cerebro-de-copy/13-integracao-mktops.md` §3. Tabela de auto-load completa em `copy-routing.md`.

---

## ⚠️ REGRA 5 — CARROSSEL MKTOPS (4 ATOS)

Carrossel segue o `playbook-narrativas-mktops.md` (raiz desta Sala) — 12 slides, 4 atos:

- **Ato 1 — Narrativa (1–4):** história interessante por si só
- **Ato 2 — Princípio (5–7):** lição universal extraída
- **Ato 3 — Aplicação (8–10):** aplicação ao mundo do leitor
- **Ato 4 — Oferta (11–12):** Fabiana Sidoruk como consequência natural

Skill: `carousel-mktops`. Paleta/tipografia: **`design-system/design-system.md`** (cores e fontes da Fabiana; o `_base/brand-book-v2.md` é só referência de estrutura). Para post de conteúdo sem oferta, usar o modo curto. Gate: `copywriting-guardrails`.

---

## Quem é a Fabiana Sidoruk

Psicóloga de base psicanalítica (freudiana; Klein, Winnicott, Bion, Ogden, Green) com consultório próprio desde o início de 2026 na Av. Cel. Aparício Borges, 260, Glória, Zona Sul de Porto Alegre. Atende presencial e online. Antes da Psicologia (PUCRS, a partir de 2019), trabalhou 20 anos no mercado financeiro, 12 deles no Bradesco. Está concluindo (nov/2026) a formação de 3 anos em psicoterapia de orientação analítica no Centro de Estudos Luís Guedes, vinculado ao Departamento de Psiquiatria da UFRGS.

**Tese (bandeira central):** "Compreender a forma como nos relacionamos pode transformar a maneira como vivemos." As relações com as pessoas, o trabalho, os estudos e o dinheiro.

**Serviços:** psicoterapia (adultos e adolescentes) · orientação profissional (primeira escolha e transição de carreira) · projetos em instituições de ensino.

**Momento:** agenda com horários vagos no presencial; a meta é preenchê-los. Paciente chega pelo Instagram e pelo WhatsApp (51) 98910-9191, que ela mesma responde. Nunca rodou tráfego pago. Primeira frente: Reels de teste no orgânico.

## ICP

Três portas, nesta ordem:
- **A — Adulto que repete o mesmo jeito de se relacionar** (psicoterapia, presencial na Zona Sul): trabalha, paga particular, quer profundidade e horário fixo, não app.
- **B — Adolescente no fim do ensino médio + pais** (orientação profissional, primeira escolha): duas ondas por ano, fev–mai e ago–out. Decisor é a mãe ou o pai.
- **C — Adulto de 30–50 em transição de carreira** (orientação profissional): a história dela é a prova.

Fora: quem procura preço baixo ou convênio, quem quer resposta rápida em app, psicólogas.

## Tom de voz

Calma, reflexiva, sóbria. Frases inteiras, pensamento em voz alta, gaúcha ("tu" na fala dos vídeos; "você" na copy escrita). Pergunta que faz a pessoa olhar pra própria vida → tese de uma frase → origem na história → reenquadramento.
**Usar:** relação, história, repetição, escolha, sentido, elaborar.
**Nunca:** sintoma, promessa, tom de coach ("destrave", "melhor versão"), jargão psicanalítico cru no gancho, militância política.

---

## Onde estão as informações nesta Sala

```
fabiana-sidoruk/
├── CLAUDE.md                       ← este arquivo (CANON + cliente)
├── README.md                       ← como instalar e começar
├── brand-context.md                ← destilado de calls/site (LER antes de copy)
├── .sala-version                   ← versão do snapshot canon herdado
├── .claude/                        ← CANON: skills · agentes · comando /spy + settings.json (hook) + hooks/
├── copy-routing.md                 ← CANON: roteamento de copy (STEP 0 — tipo → skill → Cérebro → gate)
├── cerebro-de-copy/                ← CANON: camada estratégica de copy
├── automacao/                      ← CANON: paper-designs (carrossel) + whiteboard + instagram-watch (baixar IG)
├── playbook-narrativas-mktops.md   ← CANON: 4 atos
├── design-system/                  ← _base (CANON) + design do cliente
├── pesquisa-mercado/               ← CLIENTE: briefing estratégico
├── spy/                            ← CLIENTE: análise de concorrentes
├── conteudo/                       ← CLIENTE: copy + roteiros prontos
└── entregas/                       ← CLIENTE: outputs finais por mês
```

## Mapeamento de tarefas → skills (resumo)

| Quando você quer... | Skill principal | Gate |
|---|---|---|
| Anúncio Meta Ads | `ads-create` ou `ad-creative` | `copywriting-guardrails` + `copy-format-check` |
| Carrossel modelo MktOps | `carousel-mktops` / `mktops-content-engine` | `copywriting-guardrails` |
| Roteiro de vídeo Meta | `ads-video-scripts` | `copywriting-guardrails` |
| Artigo LinkedIn/Substack | `substack-hbr-writer` | `copywriting-guardrails` |
| Cold email | `cold-email` | `copywriting-guardrails` |
| Copy de site/landing | `copywriting` / `market-copy` | `copywriting-guardrails` |
| Pesquisa de mercado | `market-research-briefing` | — |
| Análise de concorrente | `market-competitors` / `/spy` | — |
| Brand DNA / design | `ads-dna` | — |

---

## Como trabalhar aqui

1. Ler `brand-context.md` antes de qualquer copy.
2. Skill primeiro (REGRA 1). Gate `copywriting-guardrails` sempre (REGRA 2).
3. Peça estratégica → consultar o Cérebro (REGRA 4). Carrossel → playbook (REGRA 5).
4. Output final vai pra `entregas/`. Insumos de trabalho ficam em `conteudo/`.
5. **Pra ler conteúdo de Instagram** (spy, perfis de referência): baixe com `automacao/instagram-watch/baixar-instagram.sh <url>` (gallery-dl) e analise as IMAGENS com o Read tool. **NUNCA Playwright nem WebFetch pra Instagram** — quebram. Baixa em `spy/_downloads/`.

---

*Sala montada a partir do canon `v2026.14` em 2026-10-29.*
