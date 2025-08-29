# 📊 Detecção de Outliers no PIB dos Municípios (Parte 1)

Este projeto faz parte da disciplina **Análise de Dados I (TPADII/CDN)** da UFPB.  
Essa é a primeira parte de uma atividade com o objetivo de identificar **municípios brasileiros com Produto Interno Bruto (PIB) atípico**, tanto em valores totais quanto em PIB per capita, utilizando métodos estatísticos simples (IQR e Z-Score).  

---

## 🚀 Objetivos
- Realizar a **preparação dos dados** (PIB, população, PIB per capita).  
- Aplicar **Análise Exploratória de Dados (AED)** com estatísticas e gráficos.  
- Detectar outliers com **IQR** e **Z-Score**.  
- Montar comparativos entre os métodos.  
- Visualizar os resultados em **histogramas, boxplots e gráficos comparativos**.  

---

## 📂 Estrutura do Projeto
- `pib01.ipynb` → Notebook principal com código, análises e gráficos.  
- `Exercicio_02_Outliers.pdf` → Enunciado da atividade.  

---

## 🛠️ Metodologia

### 1. Preparação dos Dados
- Carregamento da base de PIB municipal.  
- Criação da coluna `PIB_total` a partir de:  

  \[
  PIB\_total = PIB\_per\_capita \times População
  \]

- Ajustes para manter consistência de unidades (PIB em reais ou em mil reais).  

### 2. Análise Exploratória
- Estatísticas descritivas com `.describe()`.  
- **Histogramas** para observar a distribuição das variáveis.  
- **Boxplots** para destacar assimetria e possíveis outliers.  

### 3. Métodos de Detecção de Outliers
- **IQR (Interquartile Range):**  
  - Valores fora do intervalo \([Q1 - 1.5 \times IQR, Q3 + 1.5 \times IQR]\) são outliers.  

- **Z-Score:**  
  - Valores com \(|Z| > 3\) foram considerados outliers.  

### 4. Comparação dos Métodos
- Criação de uma tabela comparativa com flags para cada município:  
  - `Outlier_IQR_PC`, `Outlier_IQR_Total`, `Outlier_Z_PC`, `Outlier_Z_Total`.  
- Visualizações adicionais:  
  - **Gráfico de barras** → número de métodos que detectaram cada município.  
  - **Heatmap**

