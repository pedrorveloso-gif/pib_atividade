# 📊 Detecção de Outliers no PIB dos Municípios Brasileiros

Este projeto foi desenvolvido como parte da disciplina **Técnicas de Pesquisa e Análise de Dados II (TPADII/CDN)** da UFPB.  
O objetivo é identificar **municípios brasileiros com Produto Interno Bruto (PIB) atípico**, tanto em valores totais quanto em PIB per capita, utilizando métodos estatísticos e de machine learning.

---

## 🚀 Objetivos
- Realizar a **preparação dos dados** socioeconômicos do IBGE.  
- Aplicar técnicas estatísticas (IQR e Z-Score) para detectar outliers.  
- Testar métodos avançados de machine learning (Isolation Forest e Local Outlier Factor).  
- Comparar os resultados entre os diferentes métodos.  
- Interpretar os contextos socioeconômicos dos municípios detectados.  
- Discutir como esses outliers podem distorcer a média nacional e impactar **políticas públicas**.

---

## 📂 Estrutura do Projeto
- `pib01.ipynb` → Notebook principal com todo o código, análises e visualizações.  
- `Exercicio_02_Outliers.pdf` → Enunciado da atividade.  
- Saídas gráficas: histogramas, boxplots, heatmaps e comparativos de métodos.

---

## 🛠️ Metodologia

### 1. Preparação dos dados
- Renomeação e padronização de colunas.  
- Criação da variável `PIB_total` a partir de `PIB_per_capita × População`.  
- Ajuste de unidades (PIB em R$ mil, conforme IBGE).  

### 2. Análise Exploratória
- Estatísticas descritivas (`describe`).  
- Histogramas e boxplots para visualizar distribuição e valores extremos.  

### 3. Métodos de detecção de outliers
- **IQR (Interquartile Range)** → identifica valores fora do intervalo Q1 ± 1.5×IQR.  
- **Z-Score** → valores com |Z| > 3 foram considerados outliers.  
- **Isolation Forest** → modelo baseado em árvores que isola anomalias.  
- **Local Outlier Factor (LOF)** → avalia densidade local comparada aos vizinhos.  

### 4. Comparação entre métodos
- Criação de uma tabela com flags de cada município em cada método.  
- Gráficos de barras (número de métodos) e heatmap comparativo.  

---

## 🔎 Principais Resultados

- **Municípios mais consistentes como outliers (3 métodos):**  
  - **Maricá (RJ)** – royalties do petróleo.  
  - **Canaã dos Carajás (PA)** – polo de mineração.  
  - **Paulínia (SP)** – polo petroquímico.  

- **Municípios relevantes em 2 métodos:**  
  - **Saquarema (RJ)** – turismo + petróleo.  
  - **Catas Altas (MG)** – mineração, população muito pequena.  

- **Exemplo adicional:**  
  - **Barueri (SP)** – polo empresarial e financeiro (Alphaville).  

---

## 📈 Visualizações
- Histogramas e boxplots do **PIB total** e **PIB per capita**.  
- Heatmap com a presença dos municípios em cada método.  
- Gráfico de barras destacando quantos métodos classificaram cada município como outlier.  

---

## 📝 Análise Crítica
Os resultados mostram que municípios com atividades específicas, como **mineração, petróleo ou polos industriais**, se destacam e são detectados como outliers por diversos métodos.  

Esses municípios não representam a realidade nacional: seu PIB elevado é fruto de **atividades concentradas em poucos setores**, não de uma economia diversificada.  
Assim, eles **distorcem indicadores agregados** como a média do PIB per capita do Brasil.  

➡️ Para políticas públicas, recomenda-se o uso de medidas mais robustas, como **mediana ou percentis**, além de análises regionais, para evitar que poucos municípios ricos encubram a realidade da maioria.

---

## 📚 Tecnologias Utilizadas
- Python (pandas, numpy, matplotlib, seaborn).  
- scikit-learn (Isolation Forest, Local Outlier Factor).  
- Jupyter Notebook.  

---

## 👨‍💻 Autor
- Desenvolvido por **[Seu Nome]**, aluno do curso de **Ciência de Dados para Negócios (UFPB)**.  
