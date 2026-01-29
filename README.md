# 📊 Python Insights — Análise de Cancelamento de Clientes (Churn)

Projeto de portfólio em **Python** focado em **análise exploratória de dados**, **geração de insights de negócio** e **simulação de cenários** para redução da taxa de cancelamento de clientes.

> **Autor:** Aidano da Silva Filho  
> **Stack:** Python • Pandas • Plotly • OpenPyXL  

---

## 🎯 Objetivo do Projeto

Identificar os principais fatores responsáveis pelo alto índice de cancelamento de clientes e simular cenários de atuação para apoiar decisões estratégicas de retenção.

---
## 📁 Estrutura do Projeto

```text
python-insights-churn-analysis/
├── README.md
├── LICENSE
├── requirements.txt
├── data/
│   └── cancelamentos.csv
├── src/
│   └── python_insights.py
├── outputs/
│   ├── Graficos/
│   │   └── *.png
│   └── Potencial_taxa_cancelamento.xlsx
├── docs/
│   ├── insights.md
│   └── data_dictionary.md
```
---


## 📂 Dados Utilizados

- **Arquivo:** `cancelamentos.csv`
- Base fictícia contendo informações de:
  - Tipo de contrato
  - Número de ligações ao call center
  - Dias de atraso
  - Status de cancelamento (churn)

---

## 🔍 Etapas da Análise

1. Limpeza e preparação dos dados
2. Análise exploratória de cancelamento
3. Geração de gráficos automáticos
4. Identificação de principais ofensores de churn
5. Simulação de cenários via tabela verdade (itertools)
6. Exportação de resultados para Excel formatado

---

## 🧠 Principais Insights

- Contratos mensais apresentam taxa de cancelamento significativamente maior
- Clientes com mais de 4 ligações ao call center têm alto risco de churn
- Atrasos superiores a 20 dias elevam drasticamente a taxa de cancelamento

---

## 📈 Simulação de Cenários

O projeto simula todas as combinações possíveis de atuação sobre:
- Tipo de contrato
- Volume de ligações
- Dias de atraso

📌 O melhor cenário ocorre quando as três ações são aplicadas simultaneamente.

---

## ▶️ Como Executar o Projeto

```bash
pip install -r requirements.txt
python src/python_insights.py
