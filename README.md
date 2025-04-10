# MVP - Engenharia de Dados:

# 📊 Análise dos Beneficiários do Auxílio Brasil - Janeiro de 2023

## 🎯 Objetivo do Projeto

Este projeto tem como objetivo explorar, limpar, modelar e analisar os dados de beneficiários do programa Auxílio Brasil no mês de janeiro de 2023, respondendo às seguintes perguntas de negócio:

- Qual o valor médio do benefício por estado (UF)?
- Quais municípios receberam os maiores valores totais de benefício?
- Existe correlação entre o número de famílias beneficiadas e o valor total distribuído?

---

## 🗂 Fonte de Dados

- **Fonte oficial**: [Portal da Transparência](https://portaldatransparencia.gov.br)
- **Link direto**: [CSV via GitHub](https://github.com/tleal92/engenharia-dados-clima-rj/blob/main/202301_AuxilioBrasil.csv)
- **Formato**: CSV (separado por ponto e vírgula, codificação Latin-1)

---

## 🛠 Tecnologias Utilizadas

- Python 3.10
- Pandas
- Matplotlib / Seaborn
- Google Colab / Databricks
- Delta Lake (parquet)
- Git / GitHub

---

## ⚙️ Etapas do Projeto

1. **Coleta**  
   - Os dados foram baixados automaticamente a partir do repositório GitHub.

2. **Tratamento e Limpeza**  
   - Remoção de colunas desnecessárias e valores nulos.
   - Conversão de formatos numéricos e datas.

3. **Modelagem em Esquema Estrela**  
   - Fato: pagamentos
   - Dimensões: município, UF, mês

4. **Carga**  
   - Dados tratados salvos em formato Parquet.

5. **Análise**  
   - Cálculo de estatísticas descritivas.
   - Visualizações: gráfico de barras, heatmaps e ranking de municípios.

6. **Autoavaliação**  
   - Todos os objetivos traçados foram alcançados com sucesso.

7. **Capricho**  
   - Projeto bem organizado, comentado e com evidências visuais anexadas.





