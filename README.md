# Imersão Dados com Python: Dashboard Interativo de Salários 🚀

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![Plotly](https://img.shields.io/badge/Plotly-239120?style=for-the-badge&logo=plotly&logoColor=white)](https://plotly.com/)
[![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://streamlit.io/)
[![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)](https://code.visualstudio.com/)
![Status do Projeto](https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen?style=for-the-badge)
---

### **Índice**
* [📝 Descrição do Projeto](#-descrição-do-projeto)
* [⚙️ Tecnologias Utilizadas](#-tecnologias-utilizadas)
* [📁 Estrutura do Projeto](#-estrutura-do-projeto)
* [🚀 Funcionalidades e Demonstração](#-funcionalidades-e-demonstração)
* [💻 Como Usar a Aplicação](#-como-usar-a-aplicação)
* [👥 Equipe do Projeto](#-equipe-do-projeto)
* [✅ Conclusão](#-conclusão)
* [📸 Prévia do Projeto](#-prévia-do-projeto)

---

### 📝 **Descrição do Projeto**
O **Dashboard Interativo de Salários** é um projeto de análise de dados desenvolvido durante a Imersão de Dados com Python da Alura. O objetivo é realizar a análise exploratória e o tratamento de uma base de dados sobre salários na área de tecnologia, culminando na construção e implantação de um dashboard interativo. Este projeto demonstra habilidades em manipulação de dados com Pandas, criação de visualizações interativas com Plotly e desenvolvimento de dashboards com Streamlit.

#### ⚙️ **Tecnologias Utilizadas**
-   **Python**: Linguagem de programação principal.
-   **Pandas**: Biblioteca para manipulação e análise de dados.
-   **NumPy**: Biblioteca para computação numérica, utilizada para lidar com valores nulos (`NaN`).
-   **Plotly**: Biblioteca para criação de visualizações e gráficos interativos, incluindo o mapa coroplético.
-   **Streamlit**: Framework para construir e implantar dashboards e aplicativos web.
-   **Visual Studio Code**: IDE (Ambiente de Desenvolvimento Integrado) utilizada no desenvolvimento.
-   **Jupyter Notebooks**: Ambiente para desenvolvimento e execução interativa do código.

#### 📁 **Estrutura do Projeto**
```
.
├── app.py
├── requirements.txt
├── dF/
├── dados/
├── .venv/
└── .gitignore
```
A estrutura do projeto é a seguinte:
-   `app.py`: O arquivo principal do dashboard, escrito em Streamlit.
-   `requirements.txt`: Lista todas as bibliotecas e dependências necessárias para o projeto.
-   `dF`: A base de dados ORIGINAL.
-   `dados`: A base de dados tratada, utilizada pelo dashboard.
-   `.venv/`: O ambiente virtual do projeto, que contém todas as bibliotecas instaladas.
-   `.gitignore`: Arquivo para ignorar arquivos e pastas que não devem ser enviados para o repositório, como `.venv`.

---

### 🚀 **Funcionalidades e Demonstração**
#### **Principais Funcionalidades**
* **Dashboard Interativo**: Interface para explorar os dados de salários.
* **Filtros Dinâmicos**: Permite filtrar os dados por diferentes categorias, como experiência e cargo.
* **Visualizações Gráficas**: Exibe salários médios, máximos e outras métricas em gráficos interativos.
* **Mapa Coroplético**: Permite visualizar a distribuição de salários por localização geográfica.

#### **Como funciona**
O projeto foi estruturado para realizar a análise exploratória e a visualização de uma base de dados de salários na área de tecnologia, com o objetivo de construir um dashboard interativo. O fluxo de trabalho técnico é o seguinte:

1.  **Coleta e Importação de Dados:** A base de dados é importada diretamente de um repositório no GitHub para um DataFrame, usando a biblioteca `pandas`.
    * A base de dados original é carregada com o comando `pd.read_csv()`, que aponta para o arquivo `salaries.csv`.

2.  **Análise e Preparação:**
    * **Inspeção Inicial:** O `DataFrame` é analisado para entender sua estrutura, tipos de dados e dimensões usando métodos como `.head()`, `.info()` e `.shape`.
    * **Tradução e Padronização:** Os nomes das colunas e os valores categóricos (como "SE" para Sênior, "FT" para Tempo Integral) são traduzidos e padronizados para o português, tornando a análise mais intuitiva.
    * **Tratamento de Nulos:** A presença de valores nulos na coluna `ano` é identificada e, para garantir a consistência, as linhas afetadas são removidas com o método `df.dropna()`. O tipo de dado da coluna `ano` é então convertido de `float` para `int`.

3.  **Análise e Visualização de Dados:**
    * **Distribuições Salariais:** Gráficos como `barplot` e `boxplot` do `seaborn` são gerados para visualizar a média e a distribuição dos salários em relação à senioridade.
    * **Exploração Gráfica:** Um histograma é usado para mostrar a frequência dos salários, enquanto gráficos de rosca (`pie` do `plotly`) são utilizados para analisar a proporção de tipos de trabalho (Remoto, Presencial e Híbrido).
    * **Visualização Geográfica:** Um mapa coroplético (`choropleth` do `plotly`) é criado para ilustrar o salário médio de Cientistas de Dados por país, permitindo uma análise espacial dos dados.

4.  **Exportação para o Dashboard:** Por fim, o `DataFrame` limpo e tratado é salvo em um novo arquivo `CSV`, que serve como a fonte de dados para o dashboard interativo construído com o `Streamlit`.

---

### 💻 **Como Usar a Aplicação**
Para executar este projeto localmente, siga os passos abaixo:

1.  **Instale o Python 3.x** em sua máquina.
2.  **Clone o repositório** do projeto.
    ```bash
    git clone https://github.com/amaro-netto/ImersaoAlura-DadosComPython.git
    ```
3.  **Abra a pasta** no VS Code ou terminal.
    ```bash
    cd [nome do seu-repositório]
    ```
4.  **Crie e ative um ambiente virtual** para o projeto:
    ```bash
    python -m venv venv
    # Windows: .\venv\Scripts\activate
    # macOS/Linux: source venv/bin/activate
    ```
5.  **Instale as dependências** a partir do arquivo `requirements.txt`:
    ```bash
    pip install -r requirements.txt
    ```
6.  Para rodar o dashboard localmente, use o comando no terminal:
    ```bash
    streamlit run app.py
    ```

---

### 👥 **Equipe do Projeto**
<a href="https://github.com/amaro-netto" title="Amaro Netto"><img width="180" src="https://github.com/user-attachments/assets/b7a3a1bf-304a-4974-b75f-1d620ad6ecf1"/></a>

---

### ✅ **Conclusão**
Este projeto foi uma experiência de aprendizado valiosa, demonstrando a aplicação de bibliotecas como Pandas, Plotly e Streamlit para análise e visualização de dados. A imersão permitiu aprofundar conhecimentos em tratamento de dados e na construção de dashboards interativos.

---

### 📸 **Prévia do Projeto**

<img width="1920" height="2068" alt="image" src="https://github.com/user-attachments/assets/8c6c5bee-5121-4035-a89b-a6840988531c" />


