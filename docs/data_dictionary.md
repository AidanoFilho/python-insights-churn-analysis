# 📘 Dicionário de Dados — Python Insights

Este documento descreve as colunas utilizadas no projeto **Python Insights — Análise de Cancelamento de Clientes (Churn)**, incluindo o dataset de entrada e o principal output gerado pela simulação de cenários.

---

## 1. Dataset de Entrada — `cancelamentos.csv`

Base de dados fictícia utilizada para identificar padrões de comportamento associados ao cancelamento de clientes.

### 📄 Descrição das Colunas

| Coluna | Tipo | Descrição |
|------|------|----------|
| CustomerID | Numérico | Identificador único do cliente |
| idade | Numérico | Idade do cliente |
| sexo | String | Sexo do cliente (`Male`, `Female`) |
| tempo_como_cliente | Numérico | Tempo de relacionamento do cliente com a empresa (em meses) |
| frequencia_uso | Numérico | Frequência de uso do serviço |
| ligacoes_callcenter | Numérico | Quantidade de ligações realizadas ao call center |
| dias_atraso | Numérico | Número de dias de atraso em pagamentos |
| assinatura | String | Tipo de plano contratado (`Basic`, `Standard`, `Premium`) |
| duracao_contrato | String | Duração do contrato (`Monthly`, `Annual`,`Quarterly`) |
| total_gasto | Numérico | Valor total monetário gasto pelo cliente |
| meses_ultima_interacao | Numérico | Meses desde a última interação do cliente com a empresa |
| cancelou | Numérico (0/1) | Indicador de cancelamento (`1` = Sim, `0` = Não) |

### 📌 Observações
- A base contém valores numéricos armazenados como `float` por simplicidade do dataset.
- A coluna `CustomerID` é removida durante a análise por não agregar valor explicativo ao churn.
- O dataset é fictício e tem fins educacionais e de portfólio.

---

## 2. Dataset de Saída — `Potencial_taxa_cancelamento.xlsx`

Arquivo gerado após a **simulação de cenários**, que avalia o impacto potencial da aplicação de diferentes ações de retenção na taxa de cancelamento.

### 📄 Descrição das Colunas

| Coluna | Tipo | Descrição |
|------|------|----------|
| Condição Contrato | String | Indica se a empresa está atuando ou não sobre clientes com contrato mensal  |
| Condição CallCenter | String |Indica se a empresa está atuando ou não sobre clientes com alto volume de ligações ao call center |
| Condição Atraso | String |Indica se a empresa está atuando ou não sobre clientes com alto atraso de pagamento. |
| Taxa Cancelamento | Percentual | Taxa média de cancelamento observada no cenário simulado |

#### 🔎 Detalhamento das Condições da Simulação

##### 1️⃣ Condição Contrato

- **ATIVADO**
  - Considera apenas clientes que **não possuem contrato mensal**
  - Simula ações como:
    - migração para plano anual ou trimestral
    - incentivos financeiros
    - bloqueio de churn em contratos mensais

- **DESATIVADO**
  - Não há atuação sobre o tipo de contrato
  - Todos os clientes entram na análise

---

##### 2️⃣ Condição CallCenter

- **ATIVADO**
  - Considera apenas clientes com **até 4 ligações** ao call center
  - Simulações como:
    - encaminhamento para time especializado
    - resolução definitiva no primeiro contato
    - acompanhamento ativo do cliente

- **DESATIVADO**
  - Não há atuação sobre esse fator
  - Clientes com qualquer número de ligações entram no cenário

---

##### 3️⃣ Condição Atraso

- **ATIVADO**
  - Considera apenas clientes com **até 20 dias de atraso**
  - Simula ações como:
    - negociação antecipada
    - contato preventivo
    - flexibilização de pagamento

- **DESATIVADO**
  - Não há atuação sobre atraso
  - Clientes com qualquer nível de atraso entram no cenário


### 📌 Interpretação
- Cada linha representa um **cenário diferente**, combinando filtros ativados ou desativados.
- A **menor taxa de cancelamento** indica o cenário com maior potencial de retenção.
- O arquivo serve como apoio à tomada de decisão estratégica.

---

## 🧠 Considerações Finais

- Os resultados representam **simulações baseadas em dados históricos**, não previsões.
- O objetivo do arquivo é comparar cenários relativos, e não estimar valores absolutos futuros.
- A análise pode ser expandida para modelos preditivos de churn em etapas futuras.
