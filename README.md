# 🌕 MoonBase Dashboard

Interface de gestão em tempo real dos sistemas vitais de uma base lunar habitada. Desenvolvido como projeto acadêmico, o dashboard centraliza monitoramento de energia, água, oxigênio e alimentos em um único painel responsivo.

---

## Visão geral

O MoonBase Dashboard simula o painel de controle de uma base lunar, exibindo o estado operacional de quatro sistemas críticos. A interface responde a três níveis de alerta — Estável, Instável e Crítico — alterando cores, dados e imagens em tempo real para refletir as condições da base.

---

## Estrutura do projeto

```
moonbase/
├── moonbase-dashboard.html   # Estrutura e interação
├── moonbase.css              # Estilos e responsivo
└── img/
    ├── Base_status_01_critico.png
    ├── Base_status_02_instavel.png
    ├── Base_status_03_estavel.png
    ├── power.svg
    ├── droplet.svg
    ├── wind.svg
    └── heart.png
```

---

## Sistemas monitorados

### ⚡ Energia
| Métrica principal | Métricas secundárias |
|---|---|
| Carga das baterias (%) | Geração solar (kWh) · Autonomia (dias) · Modo atual |

### 💧 Água
| Métrica principal | Métricas secundárias |
|---|---|
| Nível do reservatório (%) | Reciclagem (%) · Litros disponíveis · Qualidade · Dias de autonomia |

### 🌬 Oxigênio
| Métrica principal | Métricas secundárias |
|---|---|
| Concentração de O₂ (%) | Reserva (dias) · CO₂ atual (ppm) · Pressão (kPa) |

### 🌱 Alimentos
| Métrica principal | Métricas secundárias |
|---|---|
| Autonomia calórica (dias) | Consumo diário (kcal) · Produção da estufa (kg/sem) |

---

## Estados de alerta

Clique na imagem da base lunar no hero para alternar entre os três estados. Cada estado atualiza a imagem, as cores do sistema e todos os valores dos cards.

| Estado | Cor | Imagem |
|---|---|---|
| ✅ Estável | Azul `#4fc3f7` | `Base_status_03_estavel.png` |
| ⚠️ Instável | Amarelo `#f59e0b` | `Base_status_02_instavel.png` |
| 🚨 Crítico | Vermelho `#ef4444` | `Base_status_01_critico.png` |

A troca de estado afeta: imagem do hero, badge de status, ponto pulsante, barra de água, badges dos cards e todos os valores numéricos.

---

## Decisões visuais e de UX

**Dark mode** — reduz fadiga ocular em longos turnos de monitoramento e aumenta o contraste de alertas coloridos, seguindo a convenção de centros de controle de missão (NASA, ESA).

**Tipografia Geist Mono** — fontes monoespaciadas criam ritmo visual consistente em números dinâmicos, evitando que o layout se mova quando os valores mudam.

**Hierarquia em dois níveis** — métrica principal em destaque para leitura periférica; três métricas secundárias para contexto operacional. Princípio de *progressive disclosure*.

**Sistema de cores por estado** — azul / amarelo / vermelho mapeiam para o modelo mental universal de alerta. A cor se propaga por todos os elementos interativos simultaneamente.

**Barra de progresso na água** — o volume de reservatório é espacialmente intuitivo como barra, mais do que como número isolado.

**Gradiente radial nos cards** — `#111C31` (canto superior direito) → `#090F1A` (canto inferior esquerdo), criando profundidade sutil sem distrair dos dados.

---

## Tecnologias

- HTML5 semântico (`<section>`, `<main>`, `<article>`, `<header>`)
- CSS3 com custom properties (design tokens em `:root`)
- JavaScript vanilla — sem dependências externas
- [Geist Mono](https://fonts.google.com/specimen/Geist+Mono) via Google Fonts
- Bitcount Single via `@font-face` (pills de status)
- Imagem da base gerada com **Google Flow / Nano Banana 2**

---

## Como usar

1. Clone ou baixe o repositório
2. Coloque os arquivos de imagem na pasta `img/`
3. Abra `moonbase-dashboard.html` diretamente no navegador — sem servidor necessário

---

## Responsivo

| Breakpoint | Layout |
|---|---|
| `> 1024px` | Hero 50/50 · Cards em 4 colunas |
| `≤ 1024px` | Hero 50/50 · Cards em 2 colunas |
| `≤ 640px` | Hero empilhado · Cards em 1 coluna |

---

## Relação com ODS

**ODS 9 — Indústria, Inovação e Infraestrutura**
O dashboard responde às metas 9.1 e 9.4 ao prover monitoramento contínuo de infraestrutura crítica em ambiente extremo, permitindo decisões preventivas e garantindo resiliência operacional.

**ODS 6 — Água Potável e Saneamento**
O monitoramento da taxa de reciclagem hídrica reflete a lógica de economia circular de água — princípio central do ODS 6 aplicado a um contexto de escassez absoluta.

**ODS 13 — Ação Climática**
Tecnologias de gestão eficiente de recursos desenvolvidas para ambientes espaciais historicamente retornam para sistemas terrestres de energia e água em regiões com escassez.

---

## Créditos

Desenvolvido como projeto acadêmico de interface de gestão de sistemas críticos.
Imagens da base lunar geradas com Google Flow (modelo Nano Banana 2).
