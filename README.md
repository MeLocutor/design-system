# Design System — Rodrigo Melo

> Sistema operacional de marca e design para portfólio, LinkedIn, decks e documentos. Fonte de verdade para agentes de IA (Claude Code, Cursor) e humanos.

---

## Estrutura

```
/
├─ README.md              # Este arquivo
├─ DESIGN.md              # Arquivo raiz operacional (YAML tokens + regras compactas)
├─ BRAND.md               # Estratégia: arquétipo, voz, posicionamento, proposta, filtro
├─ TOKENS.md              # Referência plana: nome, valor, papel, quando usar/não usar
├─ COMPONENTS.md          # 6 componentes + 4 padrões de seção: anatomia, variantes, estados
├─ PRINCIPLES.md          # 6 princípios + termômetro→regras + motion + densidade
├─ tokens/
│  ├─ colors.json
│  ├─ typography.json
│  ├─ spacing.json
│  ├─ radius.json
│  └─ motion.json
├─ examples/
│  ├─ portfolio-home.html
│  ├─ case-page.html
│  ├─ linkedin-post.md
│  └─ slide-template.md
└─ assets/ (futuro)
   ├─ wordmark/*.svg
   ├─ icons/*.svg
   └─ illustrations/*.svg
```

---

## Como usar

### Agentes de IA (Claude Code, Cursor, etc.)
1. **Leia `DESIGN.md`** — tokens YAML + regras operacionais compactas
2. Consulte `TOKENS.md` para lookup plano de valores
3. Use `COMPONENTS.md` para anatomia exata de cada componente
4. Siga `PRINCIPLES.md` para decisões não cobertas por tokens

### Humanos (designers, devs, Rodrigo)
- `BRAND.md` — *por que* cada decisão existe (estratégia, arquétipo, voz)
- `TOKENS.md` — referência rápida de valores
- `examples/` — HTML/Markdown de referência visual
- `tokens/*.json` — import direto no Figma (variables), CSS-in-JS, Tailwind

---

## Arquivos principais

| Arquivo | Função |
|---------|--------|
| `DESIGN.md` | **Single source of truth para agentes** — tokens + contratos |
| `BRAND.md` | Camada estratégica (posicionamento, arquétipo, voz, DNA, filtro) |
| `TOKENS.md` | Documentação humana de todos os tokens |
| `COMPONENTS.md` | Anatomia, variantes, estados, a11y dos 6 componentes |
| `PRINCIPLES.md` | Princípios consolidados + regras derivadas do termômetro |

---

## Princípios (resumo)

1. **Estrutura antes de estética** — grid, tipo, espaço carregam significado
2. **Dado antes de adjetivo** — métricas (+1048%, -54%, +237%) = peso visual máximo
3. **Método visível** — briefing → pergunta → decisão → resultado (sempre)
4. **Acento é raro** — Brasa ≤10% área; Bronze 1×/página máx
5. **Silêncio funcional** — flat, motion mínimo, espaço negativo generoso
6. **Consistência sobre novidade** — reusar 18 ícones, 5–7 temas ilustração

**Regra de ouro:** *Traduzir, não esconder* — "iGaming → traduz para fintech/health", nunca anonimizar.

---

## Tokens essenciais (quick ref)

| Cat | Valores |
|-----|---------|
| **Cor** | Tinta `#1F2C3D` (~30%), Brasa `#C1502E` (≤10%), Bronze `#B08D57` (raro), Neutros quentes 50–900 (~60%) |
| **Tipo** | Sentient (wordmark/headlines), Switzer (body), Trench Slab (métricas only) |
| **Escala** | Display 56/36, H1 40/28, H2 32/24, H3 24/20, H4 20/18, Body 16/15, Caption 14/13, Métrica display 64/40, inline 28/22 |
| **Espaço** | Base 8px → 4,8,16,24,32,48,64,96,128,160 |
| **Grid** | 12col/24px/80mg (desk), 6col/16px (tab), 4col/16px/24mg (mob) |
| **Radius** | 2px (ícones), 4px (botões), 8px (cards) — **never pill** |
| **Motion** | 120ms / 150–200ms / 300–500ms, ease-out — no bounce/elastic/loop |

---

## Componentes

| Componente | Uso |
|------------|-----|
| `case_card` | Home (3) + /work (4) — ícone, H3, problema 1 linha, tag setor, métrica, link |
| `proof_strip` | Home + cases — até 4 métricas `·` separadas, linkáveis, sem ícone decorativo |
| `proof_block_testimonial` | Cases — quote Body Large, atribuição Caption, **sem foto**, sem placeholder |
| `post_cover` | LinkedIn — 1 ilustração hero (tema por categoria), título Sentient overlay |
| `about_section` | Única página narrativa — foto registro secundário, 3 blocos |
| `nav` | 5 itens fixos, sublinhado Brasa 2px só no ativo |

---

## Status

| Item | Status |
|------|--------|
| Tokens (YAML + JSON) | ✅ Completo |
| Componentes (anatomia/estados) | ✅ Definido em `COMPONENTS.md` |
| Princípios + regras derivadas | ✅ Em `PRINCIPLES.md` |
| Estratégia de marca | ✅ Em `BRAND.md` |
| Lockup wordmark (SVG) | ⏳ Pendente |
| Biblioteca Figma (ícones/ilustrações/variables) | ⏳ Pendente |
| Fotos reais (headshot + About) | ⏳ Pendente |
| Retrofit Framer publicado | ⏳ Pendente (maior gap) |
| Validação WCAG em produção | ⏳ Pendente |
| Reconciliação anonimização (Base Estratégica §9, BMY) | ⏳ Pendente |

---

## Decisões fechadas (não reabrir)

- Arquétipo: Sábio + Explorador (Mark & Pearson) — substitui versão junguiana
- Tipografia: Sentient / Switzer / Trench Slab (Fontshare, ITF Free)
- Paleta: Tinta 533 C, Brasa 1665 C, Bronze 4515 C, neutros H≈50°
- Movimento: Modernismo Editorial Sistemático (Swiss grid + base editorial)
- Proporção: 60% neutros / 30% Tinta / 10% Brasa (Bronze exceção)
- Dark mode: Brasa = ação primária; Tinta = fundo
- Brasa nunca toca foto de Rodrigo (conflito Inverno Profundo)
- "Traduzir, não esconder" substitui anonimização legada

---

## Licença

Uso pessoal/profissional de Rodrigo Melo. Fontes Fontshare (ITF Free). Ícones base Phosphor (MIT). Referências: Stripe, Are.na, Linear, Isotype, Paul Rand, Saul Bass — apenas estudo de princípio.