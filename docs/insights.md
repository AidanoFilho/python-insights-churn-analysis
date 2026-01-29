# 🧠 Insights — Análise de Cancelamento de Clientes (Churn)

## 1. Contexto da Análise

Esta análise teve como objetivo identificar os principais fatores associados ao alto índice de cancelamento de clientes e simular cenários de atuação para apoiar decisões estratégicas de retenção.

A base de dados utilizada contém informações contratuais, comportamentais e operacionais dos clientes, incluindo status de cancelamento.

---

## 2. Principais Insights

### 🔹 Insight 1 — Contratos mensais apresentam maior risco de cancelamento

Clientes com contrato mensal possuem uma taxa de cancelamento significativamente superior quando comparados a contratos anuais ou trimestrais.

**Impacto no negócio:**  
A alta flexibilidade do contrato mensal facilita o churn.

**Ação recomendada:**  
Criar incentivos financeiros para migração de clientes para contratos de maior duração.

---

### 🔹 Insight 2 — Alto volume de ligações ao call center indica insatisfação

Clientes que realizaram mais de 4 ligações ao call center apresentam taxa de cancelamento elevada.

**Impacto no negócio:**  
Problemas recorrentes não resolvidos aumentam a frustração do cliente.

**Ação recomendada:**  
Encaminhar clientes com múltiplos contatos para um time especializado de retenção.

---

### 🔹 Insight 3 — Atrasos prolongados antecedem o cancelamento

Clientes com mais de 20 dias de atraso possuem maior probabilidade de cancelar.

**Impacto no negócio:**  
O atraso pode indicar dificuldade financeira ou insatisfação com o serviço.

**Ação recomendada:**  
Atuar preventivamente a partir de 15 dias de atraso, com abordagem consultiva.

---

## 3. Análise de Cenários (Simulação)

Foram simuladas todas as combinações possíveis de atuação sobre três frentes:
- Tipo de contrato
- Volume de ligações ao call center
- Dias de atraso

Os resultados indicam que a **redução mais significativa da taxa de cancelamento ocorre quando as três ações são aplicadas simultaneamente**.

---

## 4. Recomendações Prioritárias

1. Priorizar clientes com alto volume de ligações ao call center  
2. Incentivar a migração de contratos mensais para planos mais longos  
3. Atuar preventivamente em casos de atraso recorrente  

---

## 5. Limitações e Próximos Passos

- A base de dados é fictícia e representa um recorte estático no tempo  
- Não foram considerados fatores externos (preço, concorrência, satisfação)  

**Próximos passos sugeridos:**
- Criar modelo preditivo de churn
- Analisar comportamento ao longo do tempo
- Integrar dados de satisfação do cliente
