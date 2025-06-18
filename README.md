# Projeto de Clusterização: Análise de Leads do Quiz Casal Próspero

![Preview da Análise](quarto/capa.png)

### ➡️ Análise Completa e Detalhada no Meu Portfólio:
[Acesse a página completa do projeto aqui](https://ferreiragabrielw.github.io/portfolio-gabriel/projetos/DataScience/1AnaliseMarketingCasalProspero/AnaliseMarketingCasalProspero.html)

---

## Sobre o Projeto

Este projeto de **Ciência de Dados** foca na análise e segmentação de leads coletados através de um quiz interativo para casais que planejam seu casamento. O objetivo principal é utilizar técnicas de **aprendizado não supervisionado (clusterização)** para identificar grupos distintos de casais com base em suas respostas, permitindo a criação de estratégias de marketing mais eficazes e personalizadas.

## Tecnologias e Processo

* **Ferramentas**: Python (Pandas, Scikit-learn, Matplotlib, Seaborn), Quarto (para relatórios dinâmicos), Jupyter Notebook.
* **Pipeline de Análise (E2E)**:
    * **Coleta e Preparação de Dados**: Unificação e padronização de leads de três fontes CSV (`df1`, `df2`, `df3`), limpeza e tratamento de valores ausentes;
    * **Análise de Correlação Categórica**: Utilização do **Cramér’s V** para analisar a associação entre as perguntas do quiz, garantindo a ausência de multicolinearidade.
    * **Pré-processamento para Clusterização**: Aplicação de **One-Hot Encoding (OHE)** com `drop_first=True` para transformar respostas categóricas em numéricas, reduzindo dimensionalidade (8 para 24 features).
    * **Redução de Dimensionalidade**: Uso de **PCA (Análise de Componentes Principais)** para reduzir as 24 features para 17 componentes principais, preservando 90.31% da variância total e otimizando o desempenho do modelo.
    * **Clusterização**: Aplicação do algoritmo **KMeans** com K=3 (definido por Método do Cotovelo e Silhouette Score), resultando em três grupos distintos de casais.
* **Insights Chave (Clusterização)**:
    * **Grupo 1 (234 leads)**: Foco em casamento íntimo/simples, capazes de investir em algo modesto, mas ainda com pouca organização inicial.
    * **Grupo 2 (206 leads)**: Sonham com cerimônia encantadora, mas se sentem perdidas com organização e capacidade financeira.
    * **Grupo 3 (55 leads)**: Altíssima clareza, comprometimento e organização, com boa capacidade de investimento e busca por otimização.

## Conteúdo do Repositório

* `data/`: Contém os datasets brutos (`leads_funil-casamento_df1.csv`, `_df2.csv`, `_df3.csv`) e o dataset tratado (`df_gf_tratado.csv`).
* `notebooks/`: Inclui o **Jupyter Notebook (`.ipynb`)** com o código completo do pipeline de análise, desde a limpeza de dados até a clusterização e interpretação.
* `quarto/`: Inclui o arquivo-fonte `.qmd` da análise e sua versão `html` renderizada.
* `README.md`: Este documento.
* `LICENSE`: Licença do projeto (MIT License).

## Como Visualizar a Análise Completa

* **Online (HTML)**: Faça o download do arquivo `AnaliseMarketingCasalProspero.html` da pasta `quarto/` e abra-o em seu navegador para ver o relatório completo.
* **Jupyter Notebook**: Visualize o Jupyter Notebook diretamente no GitHub ou faça o download do arquivo `.ipynb` da pasta `notebooks/` e abra-o em seu ambiente Jupyter para explorar o código interativamente.
* **Localmente (Quarto)**:
    1.  Faça o download do arquivo `AnaliseMarketingCasalProspero.qmd` da pasta `quarto/`.
    2.  Certifique-se de ter o Quarto e Python com as bibliotecas necessárias instalados.
    3.  Abra o `.qmd` em um editor compatível (VS Code com extensão Quarto) e compile-o.

---

### Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
