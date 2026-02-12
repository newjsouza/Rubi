# 📉 Relatório de Performance - 11/02/2026

## Resumo do Dia
**Data:** 11 de Fevereiro de 2026  
**Apostas realizadas:** 6  
**Acertos:** 3  
**Erros:** 3  
**Void:** 0  
**Lucro/Prejuízo do dia:** **-3.5 unidades**  
**ROI do Dia:** **-26,9%**  

> Relatório referente à análise oficial APEX ML v5.0 Rubi do dia 11/02/2026. Resultados confirmados em fontes estatísticas e de placares ao vivo.[cite:33][cite:37][cite:35][cite:48][cite:52][cite:46]

---

## 🧾 Tabela de Resultados

| Jogo | Mercado | Odd ref. | Stake | Resultado | Lucro/Prejuízo |
|------|---------|----------|-------|-----------|----------------|
| Aston Villa vs Brighton (Premier League) | Aston Villa vence (1X2) | 1.95 | 1.5u | ✅ (1-0 Aston Villa) | **+1.4u** |
| Manchester City vs Fulham (Premier League) | Manchester City vence (1X2) | 1.33 | 3.0u | ✅ (3-0 City) | **+1.0u** |
| Crystal Palace vs Burnley (Premier League) | Crystal Palace vence (1X2) | 1.50 | 2.0u | ❌ (2-3 Burnley) | **-2.0u** |
| Sunderland vs Liverpool (Premier League) | Liverpool vence (1X2) | 1.70 | 1.5u | ✅ (0-1 Liverpool) | **+1.1u** |
| Celtic vs Livingston (Scottish Premiership) – **NAP** | Celtic -2 handicap asiático | 1.63 | 4.0u | ❌ (2-1 Celtic, linha não coberta) | **-4.0u** |
| Athletic Club vs Real Sociedad (Copa del Rey) | BTTS – Ambas marcam (Sim) | 1.95 | 1.0u | ❌ (0-1 Real Sociedad) | **-1.0u** |

**Exposição total:** 13.0u  
**Lucro líquido:** **-3.5u**  

---

## 🧠 Análise de Erros, Acertos e Variância

### 1. Panorama do dia (3/6 acertos, impacto do NAP em red)
- Portfólio com 6 entradas, todas em ligas/copa de elite europeia, mantendo foco em mercados principais (1X2 e handicap asiático, mais um BTTS).
- O dia termina **negativo em -3.5u**, com acerto em 3 favoritos bem mapeados (Villa, City, Liverpool), mas com peso forte do red no **NAP (Celtic -2)** e do erro em Crystal Palace.
- Em termos de gestão de risco, a **exposição total em 13u** permaneceu dentro do teto diário de 15u da v5.0, com concentração maior nas teses consideradas de maior edge pré-jogo (especialmente Celtic).

### 2. Celtic -2 handicap asiático vs Livingston – NAP perdido, padrão parcialmente validado ❌
- **O que o modelo esperava:** domínio amplo do Celtic em casa contra a lanterna em crise profunda, com cenário típico de vitória por 2 ou mais gols e alta probabilidade de cobertura de linha estendida.[cite:52]
- **O que aconteceu em campo:**  
  - Jogo terminou 2-1, com Celtic massacrando em volume (nove defesas do goleiro de Livingston, posse alta e pressão constante), mas falhando em transformar superioridade em goleada.[cite:52]
  - Livingston ainda encontra um gol em pênalti, forçando o Celtic a buscar vitória dramática já nos acréscimos.
- **Diagnóstico APEX:**  
  - Do ponto de vista estrutural, **a leitura mandante muito superior x lanterna foi correta**: posse, xG e volume confirmam o favoritismo.  
  - O erro não foi na direção (vitória do Celtic), mas na **agressividade da linha (-2)** em contexto em que o adversário tende a jogar 90 minutos em modo sobrevivência.  
  - Classificação: **misto de variância com ajuste metodológico** – o padrão favorito em casa segue válido, mas os dados reforçam que, em alguns cenários de lanterna ultra-retrancado, o sistema deve ponderar com mais carinho linhas como -1.5 ou até 1X2 simples em vez de carregar stake máxima em -2.

### 3. Crystal Palace vs Burnley – favorito em casa punido por colapso psicológico ❌
- **Leitura pré-jogo:** Palace em boa sequência, Burnley em crise profunda e com uma das piores defesas da liga; vitória simples do mandante parecia padrão clássico de favorito em casa contra time em desespero.[cite:32][cite:35]
- **O que o jogo mostrou:**  
  - Palace abre 2-0 e confirma exatamente o script previsto até os 33 minutos.  
  - Em sete minutos, Burnley marca três vezes, vira ainda no primeiro tempo e segura o 3-2 até o fim, mesmo sendo pressionado na etapa final.[cite:32][cite:35]
- **Diagnóstico APEX:**  
  - **Camadas 1–6 (dados, padrão, causalidade)** estavam razoavelmente alinhadas (diferença de qualidade, momento e fragilidade defensiva de Burnley).  
  - O ponto negligenciado foi a **Camada 7–8 (Interpretação/Crítica)**: um time tão desesperado por quebrar sequência de 16 jogos sem vitória tende a adotar comportamento extremamente agressivo/caótico quando atrás no placar – e isso aumenta a volatilidade do placar final.  
  - Erro classificado como **erro parcial de leitura psicológica e de variância alta não devidamente precificada**, razão pela qual a confiança alta em Palace deve ser revisitada em futuros cenários similares.

### 4. BTTS Athletic Club vs Real Sociedad – padrão de gols quebra num 0-1 clássico de copa ❌
- **Tese pré-jogo:** derby basco com histórico recente forte de BTTS para ambos os lados, duas equipes em fase ofensiva boa e contexto de semifinal de Copa do Rei que normalmente produz gols para os dois lados.[cite:53][cite:56]
- **Realidade em campo:** jogo muito equilibrado, chances para ambos, mas apenas a Real Sociedad converte, vencendo por 1-0 fora de casa.[cite:46]
- **Diagnóstico APEX:**  
  - Padrão BTTS em derbis não foi desmentido estruturalmente (houve volume razoável para os dois), mas **o roteiro específico de 0-1 faz parte do intervalo natural de variância** desse tipo de aposta.  
  - Não há evidência forte de falha metodológica aqui; é um red classificado como **variância dentro do esperado** para um mercado com confiança apenas MÉDIA.

### 5. Greens confirmam robustez dos padrões principais ✅
- **Aston Villa vs Brighton – vitória mandante em odd próxima de 2.00**  
  - Villa vence 1-0 em jogo duro, decidindo em gol contra tardio, mas confirmando narrativa de mandante mais sólido enfrentando adversário em queda, especialmente em termos de resultados e confiança.[cite:33][cite:36][cite:39]
- **Manchester City vs Fulham – favorito absoluto em casa**  
  - City vence 3-0 com controle total, repetindo padrão de mandante de elite que transforma domínio em placar confortável contra equipe de meio de tabela e defesa vulnerável.[cite:31][cite:37][cite:34]
- **Sunderland vs Liverpool – favorito técnico fora, mas com variância controlada**  
  - Liverpool vence 1-0 fora, encerrando invencibilidade longa do Sunderland em casa, num roteiro que confirma a tese de diferença técnica e necessidade competitiva dos Reds.[cite:42][cite:48][cite:51]

### 6. Erro vs Variância – classificação do dia
- **Celtic -2 handicap (NAP):**  
  - Domínio amplo, mas margem final curta (2-1) contra retranca máxima.  
  - Classificação: **variância + ajuste fino de linha** – padrão macro segue válido, mas o sistema deve ser mais conservador na escolha entre -1.5, -2 e -2.5 em alguns contextos.
- **Crystal Palace 1X2 vs Burnley:**  
  - Queda brusca após 2-0, colapso psicológico e Burnley jogando pela vida.  
  - Classificação: **erro parcial de Camadas 7–8 (Interpretação/Crítica)** ao não dar peso suficiente ao fator desespero do azarão.  
- **BTTS Athletic–Real Sociedad:**  
  - Derby equilibrado com chances, mas que cai na cauda da distribuição (apenas 0-1).  
  - Classificação: **variância aceitável em mercado de confiança MÉDIA**.

---

## 💼 Atualização de Banca

* **Banca inicial (dia):** 115.9u  
* **Resultado (dia):** -3.5u  
* **Banca final (dia):** **112.4u**  
* **Status mensal aproximado:** banca ainda em torno de **+12–13%** sobre a banca inicial de 100u, dentro da curva alvo de longo prazo (+20–25% ao ano), apesar da sequência recente de dias puxados com NAPs de alta responsabilidade.

---

*Relatório gerado automaticamente pelo sistema APEX ML v5.0 Rubi, mantendo honestidade radical sobre reds, variância e possíveis ajustes metodológicos.*
