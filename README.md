# Análise Comparativa de Custos na Construção Civil (INCC vs IPCA)

## Visão Geral do Projeto
Este projeto consiste em uma ferramenta de engenharia de dados desenvolvida em Python para monitorar e comparar a evolução dos custos na construção civil em relação à inflação geral do país. O objetivo principal é responder a uma questão recorrente na gestão de obras: o descolamento entre o custo real de construir (medido pelo INCC-M) e o custo de vida médio (medido pelo IPCA).

Utilizando dados oficiais e públicos da API do Banco Central do Brasil, o script automatiza a extração, o tratamento e a visualização dessas séries temporais, permitindo uma análise fundamentada em dados sobre o impacto financeiro em projetos de longo prazo.

## Metodologia e Abordagem Técnica
A solução foi construída focando na integridade dos dados e na precisão matemática da engenharia de custos. O fluxo de trabalho consiste em três etapas principais:

1.  **Extração Automatizada:** O script conecta-se diretamente à base de dados do Banco Central (SGS), eliminando a necessidade de download manual de planilhas e garantindo que a análise esteja sempre atualizada com os dados mais recentes disponíveis.
2.  **Tratamento de Dados:** Foi implementada uma rotina de limpeza para adequar os formatos numéricos e de datas aos padrões computacionais. Mais importante, realizou-se a transformação das taxas mensais de inflação em índices acumulados (Juros Compostos), normalizados em Base 100. Isso permite a comparação visual direta da evolução dos preços a partir de uma data de corte definida (neste caso, o início de 2020).
3.  **Visualização de Dados:** A plotagem utiliza a biblioteca Matplotlib para gerar gráficos que destacam visualmente a área de divergência entre os dois índices, facilitando a interpretação rápida por gestores e engenheiros.

## Tecnologias Utilizadas
O projeto foi desenvolvido em Python 3, utilizando as bibliotecas Pandas para manipulação eficiente de séries temporais e Matplotlib para a geração dos gráficos analíticos. A escolha dessas ferramentas deve-se à sua robustez e padronização no mercado de Ciência de Dados e Engenharia.

## Estrutura do Repositório
* **analise_custos.ipynb:** Código fonte principal contendo as funções de coleta e tratamento.
* **requirements.txt:** Lista de dependências necessárias para a execução do projeto.
* **analise_incc_ipca.png:** Resultado visual gerado pela última execução do script.

## Como Executar o Projeto
Para replicar esta análise em seu ambiente local, certifique-se de ter o Python instalado. Baixe os arquivos deste repositório e instale as bibliotecas necessárias listadas no arquivo requirements.txt. Ao executar o script principal, o sistema processará os dados mais recentes do Banco Central e gerará um novo arquivo de imagem com o gráfico atualizado na mesma pasta.

## Potencial de Aplicação
Embora este script funcione de forma autônoma, sua lógica de extração e cálculo pode ser integrada a sistemas maiores de orçamentação (ERP) ou painéis de Business Intelligence (BI), servindo como um módulo de atualização automática de índices para reajuste de contratos e planejamento financeiro de obras.

---
**Autor:** Vitor Sousa
Estudante de Engenharia Civil - UFMG
