#  Análise de Churn – TelecomX

<p align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="38" alt="Python" />
    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" width="40" alt="Pandas" />
 
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/matplotlib/matplotlib-original.svg" width="40" alt="Matplotlib" />

  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original.svg" width="40" alt="Jupyter / Colab" />

 
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg" width="40" alt="NumPy" />
  
</p>


### Objetivo do Projeto

Analisar o **Churn (evasão de clientes)** da TelecomX para identificar padrões de cancelamento e apoiar **decisões estratégicas de retenção de clientes**.

---

## 📂 Dados

- **Fonte:** API pública (JSON)  
- **Total de registros:** 7.043 clientes  
- **Variável alvo:** Churn (Yes / No)

### Tipos de Variáveis
- **Categóricas:** gênero, contrato, forma de pagamento, serviços  
- **Numéricas:** tenure (tempo de contrato), MonthlyCharges, TotalCharges  

---

## 🔧 ETL e Tratamento de Dados

- Extração de dados via `requests` diretamente da API  
- Conversão dos dados para `pandas.DataFrame`  
- Ajuste de tipos numéricos (TotalCharges)  
- Remoção de valores ausentes  
- Padronização de variáveis categóricas  

---

## 📈 Análise Exploratória de Dados (EDA)

 🔹 Distribuição do Churn
- **26,5%** dos clientes cancelaram o serviço  
- **73,5%** permaneceram ativos  

---

 🔹 Churn por Variáveis Categóricas

**Contrato**
- Month-to-month(Mensal)→ **maior taxa de churn**
- One year/Two year(Anual)→ **churn significativamente menor**

**Forma de Pagamento**
- Electronic check → **maior evasão**
- Cartão de crédito e débito automático → **menor churn**

**Tipo de Internet**
- Fiber optic → **maior propensão ao cancelamento**
- DSL → **menor taxa de churn**

---

🔹 Churn por Variáveis Numéricas

**Tempo de Contrato (Tenure)**
- Clientes com menos de **12 meses** concentram a maior evasão  
- Quanto maior o tempo de contrato, **menor o churn**

**Gasto Mensal**
- Clientes com valores mensais mais altos apresentam **maior taxa de cancelamento**

**Gasto Total**
- Clientes que cancelam possuem **baixo TotalCharges**,(gasto total depende do tempo de permanência) indicando **churn precoce**

---

## 💡 Principais Insights

- O churn ocorre majoritariamente **nos primeiros meses de contrato**
- Contratos **mensais** representam o principal fator de risco
- A **forma de pagamento** influencia diretamente a evasão
- Clientes com **Fiber Optic** exigem maior atenção estratégica

---

## 🕵️‍♀️ Recomendações

- Incentivar a migração de contratos mensais para **planos anuais**
- Oferecer benefícios para **débito automático e cartão**
- Criar ações de retenção focadas nos **primeiros 6 meses**
- Revisar o **valor percebido** dos planos Fiber Optic
  
## 🔗 Notebook no Google Colab

O código completo da análise, incluindo tratamento de dados e visualizações, está disponível no Colab:

**https://colab.research.google.com/drive/1OfwmJ0lujaZQcomzL17vDa2J-cuV7k_h?usp=sharing**

---
## 📁 Estrutura do Projeto

```bash
telecomx-churn-analysis/
│
├── notebook/
│   └── churn_telecomx.ipynb
│
├── data/
│   └── TelecomX_Data.json
│
├── images/
│   └── churn_visualizations.png
│
└── README.md
```
---
#
<p align="center">
  © 2025
</p>
