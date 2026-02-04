# 🛡️ Gestão de Risco APEX-ML v5.0

## Sistema de Alocação e Proteção de Banca

---

## 💰 Estrutura de Banca

### **Definição de Unidades**

```yaml
Banca Total: 100 unidades (100u)
  
Exemplo financeiro:
  Banca R$ 10.000 → 1 unidade = R$ 100
  Banca R$ 5.000 → 1 unidade = R$ 50
  Banca R$ 1.000 → 1 unidade = R$ 10
  
Princípio:
  "Nunca aposte o que não pode perder."
  Banca = dinheiro separado exclusivamente para apostas.
```

### **Alocação por Confiança**

```yaml
Confiança 55-64% (BAIXA 🟡):
  Stake: 0.5-1 unidade
  % Banca: 0.5-1%
  Ação: EVITAR (só se value >20%)
  
Confiança 65-74% (MÉDIA 🟢):
  Stake: 1-2 unidades
  % Banca: 1-2%
  Ação: Stake padrão
  
Confiança 75-84% (ALTA 🔵):
  Stake: 2-4 unidades
  % Banca: 2-4%
  Ação: Stake aumentado
  
Confiança 85-90% (PREMIUM 🟣):
  Stake: 4-6 unidades
  % Banca: 4-6%
  Ação: Stake máximo
```

### **Limites de Exposição**

```yaml
LIMITE DIÁRIO:
  Máximo: 15 unidades (15% da banca)
  Exemplo: 6 apostas × 2.5u média = 15u
  
  Se atingir 15u:
    ✓ Parar de apostar no dia
    ✓ Aguardar resultados
    ✓ Recalcular banca para próximo dia
    
LIMITE SEMANAL:
  Máximo: 50 unidades (50% da banca)
  Exemplo: 20 apostas × 2.5u média = 50u
  
  Se atingir 50u:
    ✓ Parar apostas até domingo
    ✓ Revisar performance semanal
    ✓ Ajustar estratégia se necessário
    
LIMITE MENSAL:
  Máximo: 150 unidades (150% da banca)
  Rotatividade esperada: 1.5x
```

---

## 🎯 Estratégia de Stakes

### **Apostas Simples**

```python
def calcular_stake(confianca, value, banca):
    """
    Calcula stake dinâmico baseado em confiança e value
    """
    # Base stake por confiança
    if confianca >= 0.85:
        base_stake = 5.0  # 5 unidades (premium)
    elif confianca >= 0.75:
        base_stake = 3.0  # 3 unidades (alta)
    elif confianca >= 0.65:
        base_stake = 1.5  # 1.5 unidades (média)
    else:
        base_stake = 0.5  # 0.5 unidades (baixa)
    
    # Ajuste por value
    if value > 0.30:  # Value >30%
        multiplicador = 1.20
    elif value > 0.15:  # Value 15-30%
        multiplicador = 1.10
    elif value > 0.05:  # Value 5-15%
        multiplicador = 1.00
    else:  # Value <5%
        return 0  # Não apostar
    
    stake_final = base_stake * multiplicador
    
    # Limitar a 6% da banca
    stake_maximo = banca * 0.06
    
    return min(stake_final, stake_maximo)

# Exemplo
stake = calcular_stake(
    confianca=0.90,  # 90%
    value=0.55,      # 55%
    banca=100        # 100 unidades
)
# Resultado: 6.0 unidades (5.0 × 1.20 = 6.0)
```

### **Apostas Múltiplas**

```yaml
MÚLTIPLA SEGURA (2-3 seleções):
  Critérios:
    - Todas confiança ≥75%
    - Correlação <0.40
    - Odd total: 2.5-4.5
    
  Stake:
    Base: 2 unidades
    Ajuste value: +0.5u se todas value >15%
    Máximo: 2.5 unidades
    
MÚLTIPLA AGRESSIVA (4-5 seleções):
  Critérios:
    - Todas confiança ≥70%
    - Correlação <0.30
    - Odd total: 5.0-10.0
    
  Stake:
    Base: 0.5 unidades (especulativo)
    Ajuste value: +0.25u se todas value >20%
    Máximo: 1 unidade
    
NUNCA:
  ❌ Múltipla com 6+ seleções
  ❌ Stake >1u em múltipla agressiva
  ❌ Combinar mercados correlação >0.40
```

---

## 🚨 Sistema de Stop-Loss

### **Stop-Loss Diário**

```yaml
Regra:
  Se perder 6 unidades em 1 dia:
    ✓ PARAR imediatamente
    ✓ Não tentar "recuperar"
    ✓ Revisar decisões do dia
    ✓ Identificar erros
    ✓ Voltar apenas no dia seguinte
    
Exemplo:
  Aposta 1: -2u (derrota)
  Aposta 2: -2u (derrota)
  Aposta 3: -2u (derrota)
  TOTAL: -6u → STOP-LOSS ATIVADO
  
  ❌ NÃO faça aposta 4 para recuperar
  ✅ Documente, aprenda, recomece amanhã
```

### **Stop-Loss Semanal**

```yaml
Regra:
  Se perder 15 unidades em 1 semana:
    ✓ PARAR até domingo
    ✓ Fazer auditoria completa
    ✓ Revisar todos os padrões
    ✓ Identificar falhas sistemáticas
    ✓ Ajustar modelo se necessário
    
Ações:
  1. Listar TODAS as apostas da semana
  2. Categorizar erros:
     - Violação de veto
     - Má interpretação de contexto
     - Dados insuficientes
     - Variância estatística (azar)
  3. Documentar aprendizados
  4. Atualizar vetos se padrão mudou
```

### **Stop-Loss Mensal**

```yaml
Regra:
  Se perder 20% da banca em 1 mês:
    ✓ PARAR apostas por 1 semana
    ✓ Revisão filosófica completa
    ✓ Reavaliar se deve continuar
    ✓ Buscar mentoria/segunda opinião
    
Exemplo:
  Banca inicial: 100u
  Banca atual: 78u (-22u = -22%)
  
  Ação:
    → Pausar apostas por 7 dias
    → Revisar TODAS as 12 Camadas
    → Questionar TODAS as 12 Regras
    → Identificar falha filosófica
    
  Se falha for:
    - Metodológica → Ajustar processo
    - Emocional → Trabalhar disciplina
    - Dados → Melhorar fontes
    - Variância → Aceitar e continuar
```

---

## 📈 Sistema de Take-Profit

### **Meta de Lucro Mensal**

```yaml
Meta Conservadora: +10% ao mês
  Banca 100u → Meta 110u (+10u)
  Atingiu? → Sacar 50% do lucro (5u)
  Banca nova: 105u (crescimento sustentável)
  
Meta Agressiva: +20% ao mês
  Banca 100u → Meta 120u (+20u)
  Atingiu? → Sacar 60% do lucro (12u)
  Banca nova: 108u (proteção lucro)
  
Meta Premium: +30% ao mês
  Banca 100u → Meta 130u (+30u)
  Atingiu? → Sacar 70% do lucro (21u)
  Banca nova: 109u (realização)
```

### **Estratégia de Retirada**

```yaml
NUNCA:
  ❌ Sacar durante sequência negativa
  ❌ Sacar >80% do lucro (matar crescimento)
  ❌ Sacar capital inicial (preservar banca)
  
SEMPRE:
  ✅ Sacar após atingir meta mensal
  ✅ Manter capital + parte do lucro trabalhando
  ✅ Celebrar conquista (Regra 12 de Peterson)
```

---

## ⚖️ Balanceamento de Portfolio

### **Diversificação por Tipo de Aposta**

```yaml
Distribuição Semanal Ideal:
  
  Apostas Simples: 70% do volume
    - Handicap: 30%
    - BTTS: 20%
    - Corners: 10%
    - Cartões: 10%
    
  Múltiplas Seguras: 20% do volume
    - 2-3 seleções
    - Confiança alta
    
  Múltiplas Agressivas: 10% do volume
    - 4-5 seleções
    - Especulativo
    
Exemplo Semana:
  15 apostas simples × 2u = 30u (70%)
  4 múltiplas seguras × 2u = 8u (20%)
  2 múltiplas agressivas × 0.5u = 1u (10%)
  TOTAL: 39u exposição
```

### **Diversificação por Liga**

```yaml
NÃO concentrar >40% em 1 liga:
  
  ❌ Errado:
    Brasileirão: 60% apostas
    Outras: 40%
    
  ✅ Correto:
    Brasileirão: 35%
    Premier League: 20%
    La Liga: 15%
    Serie A: 10%
    Bundesliga: 10%
    Outras: 10%
    
Razão:
  - Ligas têm ciclos (rodadas fracas)
  - Diversificação reduz variância
  - Aprende padrões de múltiplas ligas
```

---

## 🔄 Recalibração de Banca

### **Ajuste Semanal**

```python
def recalibrar_banca(banca_inicial, resultado_semanal):
    """
    Recalcula banca após semana
    """
    banca_nova = banca_inicial + resultado_semanal
    
    if resultado_semanal > 0:  # Lucro
        # Saca parte do lucro
        saque = resultado_semanal * 0.50
        banca_nova -= saque
        print(f"Lucro: +{resultado_semanal}u")
        print(f"Saque: {saque}u (50%)")
        print(f"Nova banca: {banca_nova}u")
    else:  # Prejuízo
        print(f"Prejuízo: {resultado_semanal}u")
        print(f"Nova banca: {banca_nova}u")
        
        # Verifica stop-loss
        perda_percentual = abs(resultado_semanal) / banca_inicial
        if perda_percentual > 0.15:  # -15%
            print("⚠️ ALERTA: Stop-loss semanal ativado!")
            print("Revisar estratégia antes de continuar.")
    
    return banca_nova

# Exemplo Positivo
recalibrar_banca(100, +15)  
# Lucro: +15u
# Saque: 7.5u
# Nova banca: 107.5u

# Exemplo Negativo
recalibrar_banca(100, -18)
# Prejuízo: -18u
# Nova banca: 82u
# ⚠️ ALERTA: Stop-loss semanal ativado!
```

---

## 🎲 Gestão de Variância

### **Entendendo Variância**

```yaml
O que é:
  "Mesmo com 75% de acerto, você PODE perder 5 seguidas."
  "Não é falha do modelo, é matemática."
  
Probabilidades:
  Taxa 75% acerto:
    - Ganhar 5 seguidas: 23.7%
    - Perder 5 seguidas: 0.1%
    - Sequência 3V-2D: 26.4%
    - Sequência 4V-1D: 39.6%
    
Realidade:
  Em 100 apostas com 75% acerto:
    ✓ 75 vitórias
    ✗ 25 derrotas
    
  Mas NÃO distribuídas uniformemente:
    Possível: VVVDVVDVDVVVVVDDVVVDVVV...
    Improvável: VVVVDVVVVDVVVVDVVVVD... (perfeito)
```

### **Como Lidar**

```yaml
1. ACEITAR:
   "Variância é inevitável."
   "5 derrotas seguidas ≠ modelo quebrado."
   
2. DOCUMENTAR:
   "Registro permite distinguir erro de azar."
   
   Erro:
     - Violou veto
     - Dados insuficientes
     - Má interpretação
     
   Variância:
     - Seguiu processo corretamente
     - Desfecho improvável mas possível
     
3. NÃO ALTERAR:
   "Não mude modelo durante sequência negativa."
   "Mudanças devem vir de análise fria, não emoção."
   
4. CONFIAR NO LONGO PRAZO:
   "100 apostas > 10 apostas."
   "Ano completo > 1 mês ruim."
```

---

## 📊 Métricas de Saúde da Banca

### **Indicadores Mensais**

```yaml
ROI (Return on Investment):
  Cálculo: (Lucro Total / Total Apostado) × 100
  
  Meta: ≥20% ao mês
  Alerta: <10% → Revisar
  Crítico: <0% → Stop-loss ativado
  
Sharpe Ratio (Retorno ajustado ao risco):
  Cálculo: (ROI Médio - ROI Livre Risco) / Desvio Padrão
  
  Excelente: >1.5
  Bom: 1.0-1.5
  Ruim: <1.0
  
Drawdown Máximo:
  Definição: Maior queda de pico a vale
  
  Aceitável: ≤15%
  Preocupante: 15-20%
  Crítico: >20% → Pausa obrigatória
  
Win Rate:
  Taxa de Acerto
  
  Meta: ≥72%
  Aceitável: 68-72%
  Problemático: <68%
```

---

## 🎯 Checklist Pré-Aposta (Gestão de Risco)

```yaml
□ Stake calculado conforme confiança
□ Stake ≤6% da banca total
□ Exposição diária <15u
□ Exposição semanal <50u
□ Stop-loss diário não ativado (-6u)
□ Stop-loss semanal não ativado (-15u)
□ Stop-loss mensal não ativado (-20%)
□ Portfolio balanceado (não >40% em 1 liga)
□ Value confirmado (≥5%)
□ Múltipla: correlação <0.40
□ Decisão racional (não emocional)
□ Documentação preparada

SE TODOS ✅ → EXECUTAR APOSTA
SE QUALQUER ❌ → REVISAR OU DESCARTAR
```

---

**"Preservar capital > Ganhar muito. Sobreviver > Enriquecer rápido."**

*APEX-ML v5.0 (Rubi) - Fevereiro 2026*