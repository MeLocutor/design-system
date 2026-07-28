# COMPONENTS.md — Componentes e Padrões de Seção

> Anatomia, variantes, estados, restrições, a11y dos 6 componentes + 4 padrões de seção. Fonte: DESIGN.md §7 + vault (Portfolio Sitemap, Iconografia, Ilustrações, Direção Fotográfica).

---

## 1. case_card

**Propósito:** Preview de case na Home (3 cards) e grid /work (4 cards).

### Anatomia

| Slot | Spec | Token/Ref |
|------|------|-----------|
| Category icon | 24–48px, Tinta, 1 icon da biblioteca por categoria | `tokens.color.tinta`, `Iconografia` |
| Title | H3, Sentient Medium | `tokens.typography.scale.h3` |
| Problem | 1 line, Body, Switzer | `tokens.typography.scale.body` |
| Sector tag | "iGaming → traduz para fintech/health", Caption | `tokens.typography.scale.caption` |
| Metric anchor | Trench Slab SemiBold + Brasa | `tokens.typography.scale.metric_inline`, `tokens.color.brasa` |
| Link | "Ler case →", Body, Tinta underline hover | `tokens.typography.scale.body` |

### Variantes

| Variante | Contexto | Diferenças |
|----------|----------|------------|
| `home-preview` | Home, 3 cards, 1/3 width cada | Icon 48px, padding `space.4` |
| `work-grid` | /work, 4 cards lista/grid | Icon 24px, mais metadados (role, tags) |
| `case-hero` | Topo página de case | Versão expandida, sem link (já na página) |

### Estados

| Estado | Visual |
|--------|--------|
| Default | Border `neutral_200` (light) / `neutral_700` (dark) |
| Hover | Border → Brasa 1px, transition 200ms ease-out |
| Focus-visible | Outline 2px Brasa, offset 2px |

### Restrições

- 1 icon por card, sempre da tabela de categoria (Iconografia §5)
- Métrica **sempre** Trench Slab + Brasa
- Máx 1 elemento Brasa por card (o hover border conta)
- **Nunca** photo/screenshot thumbnail
- **Nunca** adjective-led title ("Incrível redesign...") — title = outcome-oriented

### Acessibilidade

- Link text "Ler case" + aria-label com título do case
- Contraste ícone/borda: ≥3:1
- Focus-visible visível em ambos temas

---

## 2. proof_strip

**Propósito:** Faixa de métricas na Home e páginas de case — prova social quantitativa.

### Anatomia

| Slot | Spec |
|------|------|
| Metric item | Trench Slab SemiBold + Brasa, inline, separadas por `·` (U+00B7) |
| Link | Cada métrica linkável ao case correspondente (underline hover) |

### Variantes

| Variante | Layout |
|----------|--------|
| `desktop` | Horizontal, 1 linha, até 4 métricas |
| `mobile` | Empilhado 2×2 ou 1×4, mesmo separador |

### Estados

| Estado | Visual |
|--------|--------|
| Default | Brasa, sem underline |
| Hover | Underline apenas a métrica (cor não muda — Brasa já é max destaque) |

### Restrições

- **Máx 4 métricas** — mais dilui "dado como prova"
- **Nunca** ícone decorativo ao lado do número (sistema vetou "ícone de conquista")
- Métrica **sempre** com baseline → resultado (ex: "72 → 827 (+1048%)")

### Acessibilidade

- Cada métrica = `<a>` com texto descritivo completo
- Contraste Brasa/surface: AA large text (métricas são large)

---

## 3. proof_block_testimonial

**Propósito:** Bloco de prova qualitativa dentro de página de case.

### Anatomia

| Slot | Spec |
|------|------|
| Quote | Body Large, aspas discretas (não decorativas) |
| Attribution | Caption, nome + cargo (anonimizado se necessário) |
| Photo | **Nenhuma** — mantém registro sóbrio |

### Variantes

- `metric-led` — métrica Trench Slab + Brasa + 1 linha contexto acima (ex: "Prioridade regulatória #1, segundo Gerente de Operações")
- `quote-led` — quote + atribuição (quando houver depoimento real)

### Estados

- Static only — sem interação

### Restrições

- **Não popular com placeholders/inventados** — nenhum depoimento real existe no vault ainda
- Componente existe para quando ativação de aliados (Hans, Murilo) gerar primeiro depoimento público

### Acessibilidade

- `<blockquote>` + `<cite>`
- Contraste quote/surface: AAA

---

## 4. post_cover

**Propósito:** Capa de post/carrossel LinkedIn.

### Anatomia

| Slot | Spec |
|------|------|
| Illustration hero | 1 ilustração, tema mapeado por categoria (Ilustrações §6) |
| Title overlay | Sentient, área segura terço superior/inferior, sem lettering dentro da ilustração |

### Variantes

| Formato | Dimensões | Uso |
|---------|-----------|-----|
| `single` | 1200×627px | Post único link preview |
| `carousel` | 1080×1350px/slide | Carrossel, mesma ilustração em zooms diferentes |

### Restrições

- 1 ilustração por post, tema fixo por categoria (Ilustrações §6)
- **Nunca** foto de estoque genérica
- **Nunca** 2 cores de acento (Brasa + Bronze) na mesma capa
- **Nunca** emoji/ícone "conquista" sobreposto ao número

### Acessibilidade

- Texto alternativo da ilustração = título do post
- Contraste overlay/surface: testar em 40px thumbnail

---

## 5. about_section

**Propósito:** Única página com registro narrativo pessoal (/about).

### Anatomia

| Slot | Spec |
|------|------|
| Photo | Registro secundário (Direção Fotográfica §11) — meio-sorriso genuíno |
| Block 1 | "Quem sou" — origem como posição, não trauma |
| Block 2 | "Como trabalho" — 3 linhas: Reframing / Documentação / IA |
| Block 3 | "Transição" — iGaming → fintech/health/SaaS, filtro ético |

### Restrições

- **Única** seção onde Voz de Marca permite tom "autêntico" mais aberto
- Limite: "posição, não trauma" (Voz §1 princípio 5)
- **Nunca** props de fandom explícitos (Funko, cosplay) como assunto da foto
- **Nunca** energia performática ("posada pra parecer espontânea")

### Acessibilidade

- Alt text da foto: "Rodrigo Melo, Product Designer"
- Estrutura heading: H2 "Sobre" → 3× H3

---

## 6. nav

**Propósito:** Navegação global fixa.

### Anatomia

| Slot | Spec |
|------|------|
| Items | 5 fixos: Home · Work · About · Contact · Résumé |
| Typography | Switzer Regular, Tinta |
| Active state | Underline Brasa 2px (único Brasa permitido na nav) |

### Estados

| Estado | Visual |
|--------|--------|
| Default | Tinta, sem underline |
| Hover | Color → Brasa (transition 150ms) |
| Active | Underline Brasa 2px |
| Focus-visible | Outline 2px Brasa offset 2px |

### Restrições

- **Máx 5 itens** — nunca mais
- **Máx 1 active accent** por vez (trivial, mas formalizado)
- **Nunca** dropdown/mega-menu — IA flat

### Acessibilidade

- `<nav aria-label="Principal">`
- Item ativo: `aria-current="page"`
- Focus order lógico

---

## 7. Padrões de Seção (Section Patterns)

Não são componentes reutilizáveis isolados, mas templates de composição usados em páginas.

### 7.1 Hero (Home + Case pages)

| Slot | Spec |
|------|------|
| Display | `type.display` (56/36), Sentient Bold |
| Subhead | `type.body_lg` (18/16), Switzer |
| CTA | 1 button primary, `type.h4` |
| **Max** | Display + Body Large + 1 CTA — **nada mais acima da dobra** |

### 7.2 Proof Strip Section

- Instância de `proof_strip` component + espaçamento `space.8` acima/abaixo
- Ver component spec

### 7.3 Case Grid

- Home: 3× `case_card` (home-preview), gap `space.4`, grid 3-col desktop
- /work: 4× `case_card` (work-grid), gap `space.4`, grid 2-col tablet / 1-col mobile

### 7.4 CTA / Contact Footer

| Slot | Spec |
|------|------|
| Email | `mailto:`, Switzer Body |
| LinkedIn | Link, Switzer Body |
| Résumé | Link PDF, Switzer Body |
| Invite line | 1 frase convite, Body, Tinta |
| **Nunca** | Formulário decorado |

---

## 8. Referências Cruzadas

| Componente | Vault source | DESIGN.md | TOKENS.md |
|------------|--------------|-----------|-----------|
| case_card | Portfolio Sitemap, Iconografia §5 | §7 table | color, type, spacing, radius |
| proof_strip | Portfolio Sitemap | §7 table | color, type |
| proof_block_testimonial | Portfolio Sitemap | §7 table | color, type |
| post_cover | Ilustrações §6, Portfolio Sitemap | §7 table | color, type, illustration themes |
| about_section | Portfolio Sitemap, Direção Fotográfica §11 | §7 table | color, type, photo |
| nav | Portfolio Sitemap | §7 table | color, type, spacing |

---

## 9. Validações Pendentes

- TODO: Produzir mockups reais dos 4 cases (Gamificação, Onboarding, RAG, Autoexclusão) com tokens
- TODO: Validar `proof_block_testimonial` quando houver depoimento real
- Pending validation: Legibilidade ícones 24px em mobile (testar 100% zoom)
- Pending validation: Contraste Brasa/surface no Framer publicado (não só tabela tokens)