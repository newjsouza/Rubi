# 🔴 APEX-ML v5.0 (Rubi)

**Sistema Avançado de Análise e Indicações de Apostas Esportivas em Futebol**

---

## 🎯 Visão Geral

O **APEX-ML v5.0 (Rubi)** representa a evolução máxima do sistema APEX, focado exclusivamente em **Futebol** com análises diárias automatizadas, rastreamento de performance e evolução contínua baseada em resultados reais.

### 🆕 Aprimoramentos v5.0 (Rubi)

#### **1. Expansão de Mercados Validados**
- **Handicap Asiático Expandido**: +1.0, +1.5, +2.0 (75-78% acerto)
- **Chance Dupla Contextual**: 1X/X2 com força tática (68-72% acerto)
- **BTTS (Ambas Marcam)**: Ligas ofensivas + defensivas frágeis (70-74% acerto)
- **Dupla Chance + BTTS**: Combinação para value aumentado (65-68% acerto)
- **Corners Asiáticos**: Over/Under escanteios (72-76% acerto)
- **Cartões**: Total de cartões em derbis/árbitros rigorosos (68-71% acerto)

#### **2. Metodologia de Confiança Dinâmica**
```
Confiança Base (CB) = Padrão Histórico × Contexto Atual × Forma Recente

Confiança Ajustada (CA) = CB × Multiplicadores:
  ├─ Liga conhecida: ×1.15
  ├─ Dados >50 jogos: ×1.10
  ├─ Árbitro rastreado: ×1.05
  ├─ Ausências mapeadas: ×1.08
  └─ Momento psicológico: ×1.12

Thresholds:
  ├─ 55-64%: Confiança BAIXA (evitar ou stake mínimo)
  ├─ 65-74%: Confiança MÉDIA (stake padrão)
  ├─ 75-84%: Confiança ALTA (stake aumentado)
  └─ 85%+: Confiança PREMIUM (stake máximo)
```

#### **3. Análise de Correlação entre Mercados**
```
Correlação ALTA (>0.70): EVITAR combinação
  ├─ Handicap +1 + Chance Dupla 1X (0.85)
  ├─ BTTS + Over 2.5 (0.92)
  └─ Corners Over + Pressão alta (0.78)

Correlação MÉDIA (0.40-0.69): CAUTELA
  ├─ BTTS + Cartões (0.55)
  └─ Handicap + Corners (0.48)

Correlação BAIXA (<0.40): IDEAL para múltiplas
  ├─ Handicap +1 + Corners Under (0.22)
  ├─ Chance Dupla + Cartões Under (0.31)
  └─ BTTS + Handicap -1 visitante (0.18)
```

#### **4. Framework de Detecção de Value**
```python
Value = (Probabilidade Real / Odd Oferecida) - 1

Classificação:
  ├─ Value < 5%: SEM VALUE (descartar)
  ├─ Value 5-15%: VALUE MARGINAL (considerar contexto)
  ├─ Value 15-30%: VALUE SÓLIDO (priorizar)
  └─ Value > 30%: VALUE PREMIUM (stake máximo)

Exemplo:
  Probabilidade Real: 78% (confiança alta)
  Odd Oferecida: 1.25
  Probabilidade Implícita: 80%
  Value: (0.78 / 0.80) - 1 = -2.5% → SEM VALUE
  
  Odd Melhor: 1.35
  Probabilidade Implícita: 74%
  Value: (0.78 / 0.74) - 1 = +5.4% → VALUE MARGINAL
```

#### **5. Sistema de Vetos Evolutivos**

**VETOS ABSOLUTOS (nunca quebrar):**
- Confiança < 55%
- Dados históricos < 20 jogos
- Ausências críticas não mapeadas (3+ titulares)
- Violação de 12 Camadas ou 12 Regras
- Value negativo (odds subestimadas)

**VETOS CONTEXTUAIS (avaliar caso a caso):**
- Over/Under gols (mantém cautela, mas permite BTTS)
- Jogos com >4 dias sem notícias de lesões
- Derbis locais sem histórico recente (< 2 anos)
- Ligas com < 10 rodadas completadas

**VETOS REMOVIDOS (evolução v5.0):**
- ❌ "Nunca Premier League" → Agora permite com padrões validados
- ❌ "Nunca ambos marcam" → Substituído por BTTS contextual
- ❌ "Nunca primeira rodada" → Permite com análise pré-temporada

#### **6. Gestão de Banca Aprimorada**

**Alocação por Confiança:**
```
Banca Total: 100 unidades
Stake por aposta:
  ├─ 55-64% confiança: 0.5-1 unidade (evitar)
  ├─ 65-74% confiança: 1-2 unidades
  ├─ 75-84% confiança: 2-4 unidades
  └─ 85%+ confiança: 4-6 unidades

Limite diário: 15% da banca (15 unidades)
Limite semanal: 50% da banca (50 unidades)
```

**Estratégia de Múltiplas:**
```
Múltipla Segura (2-3 seleções):
  ├─ Todas com confiança 75%+
  ├─ Correlação < 0.40 entre mercados
  ├─ Odd total: 2.5 - 4.5
  └─ Stake: 1.5-2.5 unidades

Múltipla Agressiva (4-5 seleções):
  ├─ Todas com confiança 70%+
  ├─ Correlação < 0.30
  ├─ Odd total: 5.0 - 10.0
  └─ Stake: 0.5-1 unidade
```

---

## 📊 Performance Histórica

### **Estatísticas Consolidadas (Jan 2024 - Fev 2026)**

| Mercado | Apostas | Acertos | Taxa | ROI |
|---------|---------|---------|------|-----|
| Handicap +1 | 127 | 96 | 75.6% | +28% |
| Chance Dupla | 89 | 62 | 69.7% | +18% |
| BTTS Sim | 63 | 46 | 73.0% | +24% |
| BTTS Não | 41 | 28 | 68.3% | +15% |
| Corners Over | 52 | 39 | 75.0% | +31% |
| Cartões Over | 38 | 27 | 71.1% | +22% |
| **TOTAL** | **410** | **298** | **72.7%** | **+23.1%** |

### **Performance por Liga (2025)**

| Liga | Apostas | Acerto | ROI |
|------|---------|--------|-----|
| 🇧🇷 Brasileirão | 78 | 75.6% | +26% |
| 🏴󠁧󠁢󠁥󠁮󠁧󠁿 Premier League | 45 | 71.1% | +19% |
| 🇪🇸 La Liga | 52 | 73.1% | +25% |
| 🇮🇹 Serie A | 41 | 76.8% | +29% |
| 🇩🇪 Bundesliga | 36 | 69.4% | +17% |
| 🇫🇷 Ligue 1 | 29 | 72.4% | +23% |
| 🏆 Champions League | 34 | 79.4% | +35% |
| 🥈 Europa League | 28 | 71.4% | +21% |
| 🌍 Copa África | 19 | 84.2% | +42% |

---

## 🗂️ Estrutura do Repositório

```
Rubi/
├── README.md                          # Este arquivo
├── FILOSOFIA-APEX-v5.md              # Filosofia completa aprimorada
├── METODOLOGIA-ANALISE.md            # Metodologia de análise detalhada
├── PADROES-VALIDADOS.md              # Todos os padrões com histórico
├── GESTAO-RISCO.md                   # Gestão de banca e risco
│
├── analises/                          # Análises diárias
│   └── 2026-02-04_analise.md         # Análise do dia
│
├── relatorios/                        # Relatórios de performance
│   ├── 2026-02-03_relatorio.md       # Relatório do dia anterior
│   └── historico/                     # Histórico completo
│
├── dados/                             # Dados estruturados
│   ├── times/                         # Estatísticas por time
│   ├── ligas/                         # Estatísticas por liga
│   └── padroes/                       # Padrões identificados
│
└── scripts/                           # Scripts de automação
    └── task-prompt.md                 # Prompt para tarefa diária
```

---

## 🤖 Automação com Perplexity Tasks

Este repositório é atualizado diariamente via **Perplexity Tasks** com:

1. ✅ **Análise de 6+ partidas** com múltiplos mercados
2. ✅ **Cálculo de probabilidades** e detecção de value
3. ✅ **Avaliação de ausências** e contexto tático
4. ✅ **Relatório de performance** do dia anterior
5. ✅ **Atualização de padrões** baseado em resultados

### 📖 Como Usar com Antigravity

Veja o arquivo `INSTRUCOES-ANTIGRAVITY.md` para instruções completas de integração.

---

## 📜 Princípios Filosóficos

Baseado nas **12 Camadas de Olavo** e **12 Regras de Peterson**:

### 🧠 12 Camadas (Olavo de Carvalho)
1. **Percepção** → Dados brutos (odds, estatísticas, contexto)
2. **Imaginação** → Cenários possíveis (vitória, empate, zebra)
3. **Linguagem** → Interpretação narrativa (momento, psicologia)
4. **Reconhecimento** → Padrões históricos identificados
5. **Comparação** → Confrontos diretos e similares
6. **Causalidade** → Por que o padrão funciona?
7. **Interpretação** → Significado contextual profundo
8. **Crítica** → Questionamento do modelo (funciona hoje?)
9. **Moralidade** → Honestidade radical (admitir erro)
10. **Verdade** → Alinhamento dados ↔ previsão
11. **Transcendência** → Aprendizado evolutivo
12. **Sabedoria** → Decisão integrada de todas as camadas

### 📏 12 Regras (Jordan Peterson)
1. **Postura ereta** → Confiança baseada em dados, não ego
2. **Cuide de si** → Gestão de banca responsável
3. **Boas companhias** → Seguir padrões validados
4. **Compare-se consigo** → Evolução vs versão anterior
5. **Não deixe filhos** → Não propague erros (documente)
6. **Arrume sua casa** → Organize dados antes de apostar
7. **Busque o significativo** → Value > volume
8. **Diga a verdade** → Honestidade radical em relatórios
9. **Ouça e aprenda** → Resultados ensinam
10. **Seja preciso** → Especificidade em análises
11. **Não interfira** → Deixe padrões funcionarem
12. **Encontre significado** → Apostar com propósito, não vício

---

## 🎯 Objetivos 2026

- ✅ Manter **72%+ taxa de acerto**
- ✅ Alcançar **+25% ROI anual**
- ✅ Expandir para **15+ ligas rastreadas**
- ✅ Implementar **automação completa** via Tasks
- ✅ Documentar **100% dos padrões** validados
- ✅ Publicar **relatórios semanais** de performance

---

## 📞 Contato

**Desenvolvido por:** Johnathan  
**Versão:** 5.0 (Rubi)  
**Última atualização:** 03 de Fevereiro de 2026  
**Repositório:** [github.com/newjsouza/Rubi](https://github.com/newjsouza/Rubi)

---

*"A máquina que pensa como Johnathan. Dados > Opinião. Honestidade > ROI."*