# João Alexandre – Perfil Profissional

Sou engenheiro e cientista de dados, com mais de 10 anos de experiência em liderança de projetos, gestão de processos, modelagem de dados e integração de sistemas.

Atualmente participo do programa **AWS Cloud Data Engineering Scholarship**, promovido pela Compass UOL, e do curso de **Pós-graduação em Engenharia e Ciência de Dados** pela UNIESP/PB. Estou aprofundando conhecimentos em **ETL**, bancos de dados, **Python**, visualização de dados e serviços em nuvem (AWS).
>
## 🎓 Formação Acadêmica
- Pós-graduação em Engenharia e Ciência de Dados (em andamento) – UNIESP
- Pós-graduação em Engenharia de Dados
- Pós-graduação em Controladoria
- Pós-graduação em Análise de Sistemas
- Pós-graduação em Gestão Financeira

---

## 🛠 Habilidades Técnicas
- **SQL** (SQLite, PostgreSQL, SQL Server)
- **Python** (Pandas, NumPy, Matplotlib)
- **Power BI**
- **Git** e **GitHub**
- **Modelagem de Dados**
- **Integração de Sistemas**
- Fundamentos de **AWS** (S3, EC2, RDS – em aprendizado)

---

## 📂 Projetos e Evidências
Este repositório contém a estrutura completa dos sprints realizados no programa AWS Cloud Data Engineering, com todos os exercícios, desafios e apresentações organizados por pasta:

```
engenharia-dados/
├── imagens/                  # Recursos visuais
├── sprint-1/                 # Exercícios e desafio da Sprint 1
├── sprint-2/                 # Exercícios e desafio da Sprint 2
└── README.md                 # (Este arquivo – perfil profissional)
```

Cada sprint possui um `README.md` com descrição detalhada da estrutura, evidências dos exercícios (`.png`), scripts em Python (`.py`) e arquivos de apoio (`.csv`, `.txt`).

---

## 📍 Localização
📌 João Pessoa – PB, Brasil

---

## 🚀 Objetivo Profissional
Transformar dados em soluções inteligentes para tomada de decisão, combinando experiência em processos com conhecimento técnico em ciência de dados e nuvem. Estou em aprendizado constante e pronto para novos desafios.

---

# 📊 Projeto: Clustering — Student Performance (K-Means & Hierárquico)

## 1. Sobre
Implementação de **clustering** (aprendizado não supervisionado) usando o dataset **Student Performance** (UCI/Kaggle).  
O objetivo é segmentar estudantes com base em atributos acadêmicos e demográficos, utilizando **K-Means** e **Clustering Hierárquico (Ward)**.

---

## 2. Estrutura
```
.
├── clustering_student_performance.ipynb   # Notebook completo e parametrizado
├── clustering_student_performance_cli.py  # Script Python com interface de linha de comando
├── outputs_clustering_student/            # Resultados gerados (CSV + PNG)
│   ├── dataset_com_clusters_kmeans.csv
│   ├── dataset_com_clusters_hier.csv
│   ├── perfil_clusters_kmeans.csv
│   ├── perfil_clusters_hier.csv
│   ├── elbow_wcss.png
│   ├── silhouette_k.png
│   ├── dendrograma_ward.png
│   ├── pca_kmeans.png
│   └── pca_hierarquico.png
```

---

## 3. Como usar

### 3.1 Notebook
1. Coloque seu dataset (`student-mat.csv` ou `student-por.csv`) na mesma pasta do notebook **ou** altere o caminho na primeira célula:
```python
DATA_PATH = r'student-mat.csv'
```
2. Execute célula a célula no Jupyter.
3. Os resultados serão gravados em `outputs_clustering_student/`.

### 3.2 Script CLI
```bash
# Dataset Matemática (separador ;)
python clustering_student_performance_cli.py --data-path "C:\caminho\student-mat.csv"

# Dataset Português
python clustering_student_performance_cli.py --data-path "C:\caminho\student-por.csv" --save-dir outputs_por

# CSV com outro separador
python clustering_student_performance_cli.py --data-path "C:\...\meuarquivo.csv" --sep ","
```

**Parâmetros principais:**
- `--data-path`: caminho do CSV local (**obrigatório**)
- `--sep`: separador do CSV (default: `;`)
- `--save-dir`: pasta de saída (default: `outputs_clustering_student_cli`)
- `--max-k`: maior k testado no K-Means (default: `8`)
- `--sample-dendro`: nº máximo de amostras no dendrograma (default: `400`)

---

## 4. Resultados
- **`dataset_com_clusters_kmeans.csv`**: dataset com ID de cluster K-Means
- **`dataset_com_clusters_hier.csv`**: dataset com ID de cluster hierárquico
- **`perfil_clusters_*.csv`**: estatísticas por cluster (`G1`, `G2`, `absences`, `failures`, `studytime`)
- **Gráficos**:
  - `elbow_wcss.png` — curva Elbow para WCSS
  - `silhouette_k.png` — Silhouette médio por k
  - `dendrograma_ward.png` — dendrograma hierárquico
  - `pca_kmeans.png` — projeção PCA colorida por cluster K-Means
  - `pca_hierarquico.png` — projeção PCA colorida por cluster hierárquico

---

## 5. Observações
- Pré-processamento inclui **one-hot encoding** para variáveis categóricas e **normalização z-score**.
- Melhor número de clusters (k) é escolhido pelo maior **Silhouette médio**.
- O dendrograma é amostrado para manter a legibilidade.
>>>>>>> 6d03213 (docs: unifica perfil profissional e README do projeto de clustering)
