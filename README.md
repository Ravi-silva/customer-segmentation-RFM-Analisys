# Segmentação de Clientes utilizando Análise RFM

## Visão Geral do Projeto

Este projeto realiza uma segmentação de clientes utilizando a metodologia **RFM (Recência, Frequência e Valor Monetário)** aplicada a dados transacionais de consumo. O objetivo é identificar padrões de comportamento dos clientes e apoiar a tomada de decisão estratégica em áreas como retenção, marketing e gestão de relacionamento com clientes.

A partir da preparação dos dados, análise exploratória e construção de métricas RFM, foi possível identificar grupos distintos de clientes com diferentes níveis de engajamento e contribuição para o faturamento.

O resultado final fornece uma estrutura de segmentação que pode ser utilizada para orientar estratégias de CRM, campanhas de retenção e priorização de clientes de maior valor.

---

# Descrição dos Dados

A base utilizada contém informações transacionais e cadastrais de clientes, incluindo variáveis como:

- Identificador do cliente
- Valor das compras
- Frequência de compras
- Data da última compra
- Categoria de produto
- Informações demográficas do cliente

A partir dessas variáveis foram construídos os indicadores fundamentais da análise RFM:

- **Recência (R):** número de dias desde a última compra do cliente  
- **Frequência (F):** quantidade de compras realizadas pelo cliente  
- **Monetário (M):** valor total gasto pelo cliente  

---

# Metodologia

O projeto foi estruturado em um pipeline analítico composto pelas seguintes etapas.

---

## 1. Limpeza e Preparação dos Dados

A primeira etapa consistiu na preparação e validação dos dados, incluindo:

- Identificação e tratamento de valores nulos em variáveis críticas
- Detecção e tratamento de outliers utilizando o método **IQR (Interquartile Range)**
- Padronização de tipos de dados
- Validação da consistência da base

Essa etapa garante que as análises posteriores sejam realizadas sobre dados confiáveis.

---

## 2. Engenharia de Variáveis

Foram criadas variáveis adicionais para enriquecer a análise do comportamento de consumo, incluindo:

- Estimativa de gasto mensal
- Ticket médio por cliente
- Métricas derivadas de recência, frequência e valor monetário

Essas variáveis permitem capturar tanto **nível de atividade quanto contribuição econômica dos clientes**.

---

## 3. Cálculo dos Scores RFM

Os clientes foram classificados utilizando **quintis (1 a 5)** para cada dimensão do modelo RFM:

- **Score de Recência:** clientes que compraram mais recentemente recebem notas mais altas
- **Score de Frequência:** clientes com maior número de compras recebem notas mais altas
- **Score Monetário:** clientes com maior valor gasto recebem notas mais altas

O **RFM Score final** foi construído a partir da combinação desses três indicadores.

Para facilitar a visualização da segmentação foi criada também a métrica:

**MF Score = (F Score + M Score) / 2**

Essa métrica permite construir uma matriz de análise baseada em **Recência × Valor**.

---

## 4. Segmentação de Clientes

A partir dos scores RFM, os clientes foram classificados em segmentos comportamentais:

- Campeões
- Clientes Leais
- Potenciais Clientes Leais
- Clientes em Risco
- Precisam de Atenção
- Prestes a Dormir
- Hibernando
- Perdidos
- Promissores
- Clientes Recentes
- Não Pode Perdê-los

Cada segmento representa um estágio diferente do ciclo de vida do cliente.

---

## 5. Análise dos Segmentos

Para cada segmento foram calculadas métricas como:

- Quantidade de clientes
- Percentual da base
- Recência média
- Frequência média
- Valor monetário médio
- Receita total gerada
- Ticket médio

Essas métricas permitem entender quais grupos concentram **maior valor financeiro e maior representatividade na base de clientes**.

Além disso, foram desenvolvidas visualizações para facilitar a interpretação dos resultados, incluindo:

- Matriz de segmentação RFM
- Distribuição de clientes por segmento
- Receita gerada por segmento

---

# Principais Resultados

A análise revelou três grandes grupos comportamentais dentro da base de clientes.

## Segmentos de Maior Impacto

Os segmentos **Clientes Leais**, **Em Risco** e **Potenciais Clientes Leais** concentram a maior parte dos clientes e da receita.

Esse grupo representa o núcleo do negócio e possui grande impacto financeiro. Estratégias de retenção e relacionamento devem ser priorizadas nesses clientes.

---

## Segmentos Intermediários

Os segmentos **Perdidos**, **Prestes a Dormir**, **Hibernando** e **Precisam de Atenção** apresentam níveis intermediários de engajamento.

Esses clientes demonstram redução na atividade recente e podem ser alvo de campanhas de reativação.

---

## Segmentos Estratégicos de Nicho

Os segmentos **Campeões**, **Não Pode Perdê-los**, **Clientes Recentes** e **Promissores** possuem menor volume, mas alto valor estratégico.

- Campeões representam clientes altamente engajados
- Não Pode Perdê-los possuem alto valor histórico
- Clientes Recentes e Promissores apresentam potencial de crescimento

---

# Tecnologias Utilizadas

Este projeto foi desenvolvido utilizando as seguintes ferramentas:

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Estrutura do Projeto


projeto-rfm-segmentacao/
│
├── data/ # Dados brutos e/ou dados tratados utilizados no projeto
│
├── notebooks/ # Notebook principal contendo toda a análise
│ └── analise_segmentacao_rfm.ipynb
│
├── outputs/ # Arquivos gerados durante a análise
│ ├── rfm_final_with_segment.csv
│ ├── segment_stats.csv
│ └── rfm_exec_log.txt
│
├── README.md # Documentação do projeto
│
└── requirements.txt # Dependências do projeto (opcional)

---

# Conclusão

Este projeto demonstra como a metodologia RFM pode ser utilizada para transformar dados transacionais em insights estratégicos sobre comportamento de clientes.

Por meio da preparação dos dados, engenharia de variáveis e segmentação comportamental, foi possível identificar padrões de consumo, avaliar a contribuição financeira de cada grupo de clientes e estruturar uma base analítica para estratégias de retenção e relacionamento.

A abordagem apresentada pode ser aplicada em diferentes contextos de negócio que buscam compreender melhor sua base de clientes e orientar decisões com base em dados.
