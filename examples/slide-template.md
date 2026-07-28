# Slide Template — Apresentações

> 3 níveis tipográficos máx por slide. Diagrama conceitual (ilustração) + métrica destaque. Fonte: DESIGN.md, PRINCIPLES.md, Ilustrações.

---

## Estrutura por Slide

| Nível | Token | Uso | Exemplo |
|-------|-------|-----|---------|
| **Título** | `type.h1` / `type.h2` (Sentient Bold/Medium) | 1 por slide, topo | "Reframing: do briefing à métrica" |
| **Corpo** | `type.body-lg` (Switzer Regular) | Máx 3 bullets curtos | "Briefing: 'criar promoção'" → "Pergunta: como gerar engajamento recorrente?" |
| **Métrica** | `type.metric-display` (Trench Slab SemiBold + Brasa) | 1 número âncora por slide | **+1048%** (72 → 827) |

**Nunca mais que 3 níveis por slide.** Espaço generoso ao redor do dado.

---

## Layouts Padrão

### 1. Slide de Abertura / Seção
```
┌─────────────────────────────────────┐
│                                     │
│        [TÍTULO H1/H2]               │
│        Sentient Bold/Medium         │
│                                     │
│        [Ilustração tema §6]         │
│        (ex: Bifurcação, Antes/Depois)│
│                                     │
└─────────────────────────────────────┘
```

### 2. Slide de Método / Processo
```
┌─────────────────────────────────────┐
│  [TÍTULO H2]                        │
├─────────────────────────────────────┤
│  ● Briefing recebido                │
│  ● Pergunta feita                   │  ← Switzer Body Large
│  ● Decisão tomada                   │
│  ● Resultado: +1048%                │  ← Trench Slab + Brasa
└─────────────────────────────────────┘
```

### 3. Slide de Métrica / Prova
```
┌─────────────────────────────────────┐
│                                     │
│        +1048%                       │  ← Trench Slab 64px, Brasa
│        (72 → 827 por rodada)        │  ← Switzer Caption
│                                     │
│        [Ilustração: Gráfico como    │
│         Prova — barras + baseline]  │
│                                     │
└─────────────────────────────────────┘
```

### 4. Slide de Transição / Reflexão
```
┌─────────────────────────────────────┐
│                                     │
│    "O padrão não é sorte —          │
│     é método: questionar o          │
│     briefing antes de executar"     │  ← Switzer Body Large, centralizado
│                                     │
└─────────────────────────────────────┘
```

---

## Regras de Composição

| Regra | Spec |
|-------|------|
| **Grid** | 12-col desktop, margens 80px / gutter 24px (tokens.spacing.grid) |
| **Espaço negativo** | Mín 30% área livre — não encha o slide |
| **Ilustração** | 1 por slide máx, tema mapeado (Ilustrações §6), flat, 1 acento Brasa OU Bronze |
| **Tipografia** | Apenas 3 níveis: Título → Corpo → Métrica |
| **Cor** | 60% neutro / 30% Tinta / ≤10% Brasa (Bronze 1× opcional) |
| **Dark mode** | Brasa = ação primária; Tinta = fundo. Testar contraste projetor. |

---

## Temas de Ilustração por Conteúdo

| Conteúdo | Tema (Ilustrações §4) | Acento |
|----------|----------------------|--------|
| Reframing / Decisão | Bifurcação | Brasa no ramo escolhido |
| Baseline / Métrica | Antes/Depois em Espelho | Neutro (antes) + Brasa (depois) |
| Documentação / Infra | Camadas/Estratos, Torre de Camadas | Tinta |
| IA / RAG | Circuito de Conhecimento | Tinta |
| Trajetória / Domínios | Trilha de Domínios | Bronze (segmento final) |
| Filtro Ético | Peneira de Valores / Escudo de Linhas | Tinta |
| Ciclo Produto | Ciclo Fechado | Brasa no nó final (entrega) |

---

## Checklist Pré-Apresentação

- [ ] Máx 3 níveis tipográficos por slide
- [ ] Métrica tem baseline → resultado (Trench Slab + Brasa)
- [ ] Ilustração explica mecanismo, não decora
- [ ] Brasa ≤ 10% área do slide
- [ ] Fonte: Sentient/Switzer/Trench Slab via Fontshare CDN ou self-host
- [ ] Testado em projetor (contraste dark mode)
- [ ] `prefers-reduced-motion` respeitado (sem auto-animation)

---

## Referências Cruzadas

| Spec | Arquivo |
|------|---------|
| Tokens tipo/cor/spacing | DESIGN.md, TOKENS.md |
| Princípios densidade/hierarquia | PRINCIPLES.md §4, §7 |
| Ilustrações temas/biblioteca | Ilustrações §4, §5, §6 |
| Motion (se animado) | PRINCIPLES.md §10, motion.json |
| Voz de Marca (copy) | BRAND.md §3 |
