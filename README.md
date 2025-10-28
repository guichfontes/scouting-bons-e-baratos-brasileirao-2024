# ⚽ Análise de Jogadores "Bons e Baratos" do Brasileirão 2024

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-Completed-success)

Este repositório contém o **notebook original (.ipynb)** e as **bases de dados (.xlsx)** utilizados na análise estatística e exploratória de jogadores do **Campeonato Brasileiro 2024**, com o objetivo de **identificar atletas de alto desempenho e baixo custo de mercado** — os chamados *bons e baratos*.

Utilizando [ScraperFC](https://scraperfc.readthedocs.io/en/latest/), os dados foram coletados do [FBref](https://fbref.com) (métricas de desempenho) e [Transfermarkt](https://www.transfermarkt.com.br) (valores de mercado), e analisados com técnicas de **aprendizado não supervisionado (DBSCAN, IForest, LOF, One-Class SVM)** e **métricas customizadas de performance**.

---

## 🧠 Objetivo do Projeto

Encontrar **outliers positivos** — jogadores que:
- Apresentam **alta performance estatística** nas métricas específicas de sua posição;
- Possuem **baixo valor de mercado** ou **alto custo-benefício**.

A metodologia permite auxiliar o **scouting de clubes** e **análises de contratação baseadas em dados**.

---

> Todos os arquivos `.xlsx` e o notebook `.ipynb` estão na **raiz do projeto** para facilitar a execução direta no Jupyter Notebook ou Google Colab.

---

## ⚙️ Tecnologias Utilizadas

| Categoria | Ferramenta |
|------------|-------------|
| Linguagem | Python 3.10+ |
| Análise e Machine Learning | Pandas, NumPy, Scikit-Learn, SciPy |
| Visualização | Matplotlib, Plotly Express, Seaborn |
| Ambiente | Google Colab |
| Dados | FBref e Transfermarkt |

---

## 📊 Metodologia

1. **Coleta de Dados**
   - FBref (dados técnicos por posição);
   - Transfermarkt (valores de mercado em euros).

2. **Pré-processamento**
   - Padronização de colunas;
   - Normalização (`MinMaxScaler`);
   - Combinação de métricas entre performance e custo.

3. **Análise Estatística**
   - Correlação entre variáveis;
   - PCA (redução de dimensionalidade);
   - Clustering com DBSCAN, Isolation Forest, Local Outlier Factor e One-Class SVM;
   - Análise de ruído.

4. **Métrica de Performance Personalizada**
   - Pesos ajustados conforme posição (FW, MF, DF, GK);
   - Cálculo de *score híbrido* (performance × custo-benefício).

5. **Identificação de Outliers Positivos**
   - Jogadores com **alto score individual** e **baixo valor de mercado**;
   - Visualização e interpretação manual por posição.

---

## 💡 Resultados

A análise identificou jogadores subvalorizados que se destacaram estatisticamente no Brasileirão 2024.  
O trabalho serviu de base para o **dashboard interativo de scouting** publicado em:

👉 [Dashboard de Bons e Baratos — Streamlit](https://github.com/guichfontes/dashboard-scouting-2024)

---

## 👤 Autor

**Guilherme Fontes**  
🎓 Universidade Federal da Bahia (UFBA)
📧 guilhermefontes@ufba.br
