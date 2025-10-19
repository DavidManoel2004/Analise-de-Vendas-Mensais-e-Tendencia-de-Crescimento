# Projeto Solo I: Análise de Vendas Mensais e Tendência de Crescimento

* David Manoel da Silva | Analista de Dados Júnior
* Habilidades: Python (Pandas), Análise de Séries Temporais, Cálculo de Variação Percentual.
## 2. O Desafio: Entender o Desempenho

* **Problema de Negócio:** Precisamos saber se as vendas estão crescendo mês a mês e, em caso positivo, a **velocidade** desse crescimento.
* **Pergunta Chave:** Qual foi o crescimento percentual mês a mês e qual mês teve o maior pico de vendas?
* **Ação:** Transformar dados de vendas diárias em uma Série Temporal Mensal.
## 3. Ação Técnica: Agregação e Transformação

A conversão da granularidade diária para mensal foi feita com `groupby()` no período ('M').

| Etapa | Código | Habilidade |
| :--- | :--- | :--- |
| **1. Agregação** | `dados.groupby(dados['date'].dt.to_period('M'))['value'].sum()` | Agrupar por Mês |
| **2. Variação** | `.pct_change()` | Calcular variação percentual |

* O `.dt.to_period('M')` foi crucial para consolidar as vendas diárias em **Vendas Mensais**.
## 4. O Insight Estratégico

* A análise revelou que as vendas apresentaram uma **tendência geral de crescimento**.
* O maior destaque foi o mês de **Abril**, que registrou um pico de crescimento de **+15.5%** em relação a Março.
* O pior desempenho foi registrado em **Agosto**, com uma queda de **-2.1%**.

**Recomendação:** Estudar as ações de marketing e vendas realizadas no mês de **Abril** para replicar o sucesso e investigar a causa da queda em **Agosto**.
## 5. Conclusão e Próximos Passos

O projeto demonstrou proficiência em:
* Manipulação de datas (`datetime`).
* Agregação de dados (`groupby`).
* Criação de métricas de negócio (`pct_change`).

**Próximo Projeto:** Análise de Correlação entre Desmatamento e Índice Educacional.

| **LinkedIn** | [David Manoel] |
