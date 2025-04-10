# MVP - Engenharia de Dados: Análise Climática no Rio de Janeiro (Jan/2024)

## Objetivo do Projeto
Este projeto tem como objetivo construir um pipeline de dados completo, utilizando tecnologias na nuvem, para buscar, coletar, modelar, carregar e analisar dados climáticos da cidade do Rio de Janeiro, com foco no mês de janeiro de 2024. As principais perguntas de negócio que motivaram este trabalho foram:

1. Quais foram as temperaturas médias diárias no Rio de Janeiro durante o mês de janeiro de 2024?
2. Houve episódios de alta ou baixa precipitação? Em quais dias?
3. É possível identificar padrões meteorológicos relevantes ao longo do mês?

---

## Coleta dos Dados
Os dados utilizados neste projeto foram obtidos por meio da API do INMET (Instituto Nacional de Meteorologia), referente às observações meteorológicas horárias na estação de referência do Rio de Janeiro, no período de 01 a 31 de janeiro de 2024. Os dados foram persistidos na nuvem utilizando a plataforma **Databricks**.

Formato dos dados coletados: `.csv`

---

## Modelagem dos Dados
O modelo utilizado foi um **Esquema Estrela** com os seguintes componentes:

### Tabela Fato
- **fato_clima**:
  - id_data (chave primária)
  - temperatura_media
  - precipitacao_total

### Tabelas Dimensão
- **dim_tempo**:
  - id_data
  - dia
  - mes
  - ano
  - dia_semana

### Catálogo de Dados
| Coluna                  | Tipo     | Descrição                                     |
|------------------------|----------|-------------------------------------------------|
| temperatura_media      | float    | Temperatura média diária em graus Celsius      |
| precipitacao_total     | float    | Total de precipitação do dia em milímetros   |
| dia                    | inteiro  | Dia do mês                                     |
| mes                    | inteiro  | Mês de referência                             |
| ano                    | inteiro  | Ano de referência                              |
| dia_semana             | texto    | Nome do dia da semana                          |

---

## Carga dos Dados
O processo de ETL foi realizado em Databricks com os seguintes passos:

- Extração via API (código em Python)
- Transformação: limpeza de dados, agregados diários e formatação
- Carga em tabela no formato Delta Table no Data Lake

Todos os scripts estão disponíveis neste repositório.

---

## Análise

### a. Qualidade dos Dados
- Dados sem valores nulos
- Datas e formatos padronizados
- Faixas de temperatura e precipitação coerentes com o clima da região

### b. Respostas e Gráficos
- [x] Gráfico de Temperatura Média Diária
- [x] Gráfico de Precipitação Diária
- Padrões como queda de temperatura após chuvas foram observados

Evidências disponíveis na pasta `/evidencias` com screenshots e outputs.

---

## Autoavaliação
- O objetivo foi completamente atingido.
- Todas as perguntas foram respondidas com base em evidências técnicas.
- Pipeline funcional e bem documentado.
- Possível melhoria futura: incluir dados de mais meses para comparação sazonal.

---

## Capricho
- Gráficos gerados com Matplotlib
- Scripts comentados e organizados
- Documentação clara no README
- Repositório estruturado com pastas:
  - `/src`: código-fonte
  - `/data`: arquivos de dados
  - `/evidencias`: screenshots e gráficos
  - `/notebooks`: notebooks utilizados

---

## Licença
Dados públicos coletados da API INMET. Uso educacional.


