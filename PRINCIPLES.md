# PRINCIPLES.md — Princípios Consolidados e Regras Derivadas

> 6 princípios norteadores + regras derivadas do Termômetro + motion principles + "traduzir não esconder" + densidade + estrutura vs acento. Fonte: DESIGN.md principles YAML + vault (Termômetro Atributos, Movimento Estético, Design System card).

---

## 1. Seis Princípios Norteadores (ordem de prioridade)

| # | Princípio | Regra operacional |
|---|-----------|-------------------|
| 1 | **Estrutura antes de estética** | Grid, hierarquia tipográfica e espaçamento carregam o significado. Cor e ilustração = reforço, nunca mensagem principal. |
| 2 | **Dado antes de adjetivo** | Métricas (+1048%, -54%, +237%) recebem tratamento visual mais forte (Trench Slab + Brasa). Nada compete com métrica em peso visual. |
| 3 | **Método visível** | Todo case/post/slide segue: briefing → pergunta → decisão → resultado. Repetição do padrão = prova de repetibilidade. |
| 4 | **Acento é raro** | Brasa ≤ 10% área qualquer composição. Bronze = uso raríssimo (1×/página máx). Se acento aparece demais, perde função de destaque. |
| 5 | **Silêncio funcional** | Espaço negativo generoso (mín 30%), flat quase absoluto, motion mínimo. Sistema nunca "chama atenção para si". |
| 6 | **Consistência sobre novidade** | Reusar mesmos 18 ícones e 5–7 temas de ilustração. Não inventar metáfora visual nova a cada peça. Sistema > criatividade pontual. |

---

## 2. Tradução do Arquétipo em Decisão de Sistema

| Camada | Visual | Comportamental |
|--------|--------|----------------|
| **Sábio (primário)** | Serifa humanista (Sentient), Tinta ~30%, grid rígido, flat absoluto, geometria estável, sem ornamento | Didático, direto, sem hype. "Eu explico o caminho, não só a chegada." |
| **Explorador (secundário)** | Brasa único acento quente, Trench Slab peso "ação" só em métricas, 1 elemento assimétrico/ilustração | Investigativo, curioso. Pergunta "me ajuda a entender" vs "isso está errado". |
| **Fora da Lei (filtro)** | **Nunca** como estilo visual (nada de "rebeldia" gráfica) | Aparece como *ausência*: iGaming nunca mostrado visualmente; nenhuma peça usa linguagem disrupção/choque. Filtro ético: recusa produtos que exploram vulnerabilidade. |

---

## 3. Termômetro de Atributos → Regras Concretas

Fonte: `Termômetro de Atributos Visuais — Marca Pessoal Rodrigo Melo` (20 pares numerados).

| Atributo (posição) | Regra de sistema |
|--------------------|------------------|
| Minimalista = 15/100 | Máx 3 elementos visuais distintos/composição (ilustração, ícone, texto). Se precisar 4º → cortar um dos 3. |
| Séria = 30/100 | Sorriso "dentes" nunca no registro primário; meio-sorriso só no About (registro secundário). |
| Técnica = 22/100 (vs Intuitiva) | Toda métrica **sempre** com baseline (nunca número solto sem "de X para Y"). |
| Racional = 22/100 (vs Emocional) | Motion e cor **nunca** comunicam emoção — só hierarquia (feita por peso/posição, não "efeito bonito"). |
| Delicada↔Robusta = 75/100 (robusta) | Traço nunca fino a ponto de sumir em impressão P&B ou tela pequena. Testar 100% zoom antes de aprovar. |
| Rebelde↔Disciplinada = 72/100 (disciplinada) | Nenhuma peça usa linguagem "quebrar regra" ou "disruptivo" — nem visual nem textual. |
| Conservadora↔Inovadora = 68/100 (inovadora) | Camada IA (Circuito-Nó, Rede-e-Nó) pode aparecer mais que em marca puramente conservadora — é diferencial raro. |
| Geométrica↔Orgânica = 25/100 (geométrica) | 1 concessão orgânica/ilustração = teto, não padrão. Maioria peças = 100% geométrica. |
| Humana↔Tecnológica = 55/100 (tech) | Equilíbrio: diagrama conceitual (tech) + foto registro secundário com meio-sorriso (humano) no About. |

---

## 4. Hierarquia Visual (ordem de peso)

1. **Métrica display** — Trench Slab 64/40px + Brasa (proof strip, case anchor)
2. **Display/H1** — Sentient Bold 56/36px / 40/28px (hero, case title)
3. **Métrica inline** — Trench Slab 28/22px + Brasa (dentro de card/parágrafo)
4. **H2/H3** — Sentient 32/24px / 24/20px (seções, card title)
5. **H4** — Switzer Medium 20/18px (block labels)
6. **Body Large** — Switzer 18/16px (lede, opening paragraph)
7. **Body** — Switzer 16/15px (corpo padrão)
8. **Caption/Small** — Switzer 14/13px (metadata, tags, timestamps)
9. **Neutro 500+** — ícones, bordas, placeholders (função estrutural, não destaque)

**Regra:** Nada no nível 3–9 pode competir visualmente com nível 1–2.

---

## 5. Proporção de Cor por Contexto

| Contexto | Neutros | Tinta | Brasa | Bronze |
|----------|---------|-------|-------|--------|
| Site / portfólio | 60% | 30% | ≤10% | 1×/página opcional |
| Post LinkedIn (imagem) | 55–65% | 25–35% | ≤10% | Raro |
| Slides/apresentação | 60–70% | 25–30% | ≤10% (só número destaque) | Raro |
| Documento/PDF | Predomina neutro + Tinta headers | — | Só callout/métrica | Não recomendado |
| UI produto (futuro) | 60% | 30% | ≤10% (CTA/estado) | N/A |

**Hard rule:** Brasa > 10% → revert. No exceptions.

**Dark mode inversion:** Brasa = primary action; Tinta = background/structure.

**Brasa nunca toca foto de Rodrigo** (roupa, fundo, luz) — conflito Inverno Profundo.

---

## 6. Prova vs. Estética

| Princípio | Implementação |
|-----------|---------------|
| **Número = prova** | Métricas = Trench Slab + Brasa (peso máximo). Baseline → resultado sempre. |
| **Estrutura = prova** | Grid, tipo, espaço = significado. Ilustração = diagrama explicativo, não décor. |
| **Ícone = notação** | Line icon 1.5–2px, flat, sem fill/duotone. Comunica categoria, não "conquista". |
| **Foto = presença** | Headshot = credibilidade. About = conexão. Nunca "lifestyle stock". |
| **Motion = revelação** | Reveal hierarchy (estrutura primeiro, acento por último). Nunca entretenimento. |

---

## 7. Regras de Densidade por Contexto

| Contexto | Densidade | Especificação |
|----------|-----------|---------------|
| Site/portfólio | Baixa (generosa) | Mín 30% espaço negativo/seção. Editorial density, não app density. |
| LinkedIn post/carrossel | Média-alta | Mobile-first. 1–3 linhas/parágrafo (Voz de Marca). |
| Slides | Baixa | Máx 1 ideia/slide. Espaço generoso ao redor do dado. |
| PDF/documento longo | Média | Margens 2–2.5cm. Headers seguem scale tipográfica do sistema. |

---

## 8. Estrutura vs. Acento (Regra de Decisão)

| Dúvida | Teste | Decisão |
|--------|-------|---------|
| "Adiciono cor aqui?" | É métrica/CTA/active link? | Sim → Brasa. Não → Neutro ou Tinta. |
| "Uso Bronze?" | É 1 elemento "prova/conquista" na página? | Sim → Bronze (1× máx). Não → não use. |
| "Adiciono ilustração?" | Explica mecanismo (antes→depois, causa→efeito)? | Sim → 1 ilustração tema mapeado. Não → não use. |
| "Adiciono ícone?" | Reforça categoria/estrutura? | Sim → 1 icon neutro/Tinta. Não → não use. |
| "Arredondo botão?" | Pill? | **Nunca.** md (4px) only. |
| "Adiciono sombra?" | Card interativo? | Sim → `card_shadow` only. Não → flat. |
| "Animo isso?" | Reveal hierarchy on scroll/interaction? | Sim → ease-out, stagger. Não → sem motion. |

---

## 9. Regra "Traduzir, Não Esconder"

**Origem:** Tensão resolvida entre docs legados (Base Estratégica §9, BMY = "anonimizar") e execução real (LinkedIn, Portfolio Sitemap = nomear setor + traduzir métrica).

**Regra vigente:**
- Nome da empresa **pode** aparecer
- Setor de origem **nomeia**: "iGaming"
- Métrica **traduz** para destino: "→ traduz para fintech/health"
- **Nunca** linguagem que promova/normalize produto de apostas em si
- Ver: `BRAND.md §1.2` tensão #1, `Voz de Marca §8` zona de risco iGaming

---

## 10. Motion Principles (extendidos a página)

| Elemento | Duração | Easing | Regra |
|----------|---------|--------|-------|
| Icon/button hover | 120–150ms | ease-out | Fade opacity (0.8→1) ou scale sutil (1→1.05). Never rotate/bounce. |
| Button color change | 150ms | ease-out | Ajuste L em OKLCH (mesmo H/C). Never hue swap. |
| Illustration reveal (scroll) | 300–500ms/layer, stagger 60–80ms | ease-out | Estrutura primeiro, acento Brasa por último. |
| Section reveal (scroll) | 300ms | ease-out | Fade + translate 8px. Max. |
| Page transition | 200ms | ease-out | Fade simples. No wipe/slide/zoom dramático. |

**Forbidden (sistema):** Auto-loop sem interação, rotação contínua, bounce/elastic/spring, path-draw decorativo (Lottie consumer), qualquer motion sem ação do usuário.

---

## 11. Acessibilidade Baseline (não negociável)

| Regra | Spec |
|-------|------|
| Contraste texto | AA mínimo (AAA preferido) — todas pares semânticos em `TOKENS.md` |
| Contraste ícone/gráfico | ≥3:1 (WCAG non-text) |
| Focus-visible | Outline 2px Brasa offset 2px — **sempre** |
| Color + ícone/texto | Estados (success/error) **nunca** só cor — sempre ícone (✓/✕) ou label |
| Motion | Respeita `prefers-reduced-motion` — desliga stagger/reveal |
| Touch target | Mín 24×24px área ativa (ícone visual pode ser 16px) |

---

## 12. Checklist de Decisão (para qualquer nova peça)

Antes de aprovar qualquer entrega visual:

- [ ] Segue 6 princípios? (Estrutura, Dado, Método, Acento raro, Silêncio, Consistência)
- [ ] Brasa ≤ 10%? Bronze ≤ 1×?
- [ ] Métrica tem baseline → resultado? Trench Slab + Brasa?
- [ ] Tipografia: Sentient/Switzer/Trench Slab nos papéis certos?
- [ ] Espaçamento: só valores da scale 8px?
- [ ] Radius: 2/4/8px only, never pill?
- [ ] Flat? Só `card_shadow` em card interativo?
- [ ] Motion: ease-out, reveal hierarchy, no auto-loop?
- [ ] "Traduzir, não esconder" aplicado? (setor nomeado, métrica traduzida)
- [ ] A11y baseline passa? (contraste, focus, color+icon, reduced-motion)

---

## 13. Referências Cruzadas

| Princípio | DESIGN.md | BRAND.md | TOKENS.md | COMPONENTS.md |
|-----------|-----------|----------|-----------|---------------|
| 6 princípios | YAML `principles` | — | — | — |
| Termômetro→regras | — | — | — | — |
| Hierarquia visual | — | — | `typography.scale` | component anatomy |
| Proporção cor | YAML `proportion` | §5 | `color.proportion` | component constraints |
| Prova vs estética | §1, §7 | §3, §4 | — | metric treatment |
| Densidade | §4 | — | `spacing.density` | section patterns |
| Estrutura vs acento | §2, §6 | §2 | `color.usage` | component rules |
| Traduzir não esconder | §2, §8 | §1.2, §8 | — | sector tag |
| Motion | YAML `motion` | — | `motion` | component states |
| A11y baseline | — | — | `WCAG` | component a11y |

---

## 14. Pendências

- TODO: Validar regra "máx 3 elementos visuais" em peças reais (Home, Case, LinkedIn)
- Pending validation: Motion stagger 60–80ms feels right no Framer?
- Needs human review: Regra "Brasa nunca toca foto" — confirmar com ensaio fotográfico real
- Needs human review: Densidade "mín 30% espaço negativo" — testar em mobile 375px