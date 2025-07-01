# Análise de Letras de Músicas

Este repositório contém o código fonte e o relatório técnico do desafio de análise textual em uma base de letras de músicas. O projeto tem como objetivo principal realizar o pré-processamento, a análise de polaridade e a análise exploratória de dados (EDA) para compreender padrões linguísticos, emocionais e temporais das composições musicais.

## Descrição do Desafio

A tarefa consistiu em analisar uma base textual heterogênea, inicialmente composta por músicas, trechos de livros, discursos, entre outros. O foco foi filtrar e estruturar apenas as músicas, e posteriormente realizar uma análise de sentimentos (polaridade) das letras ao longo do tempo, considerando também aspectos como artistas, anos e popularidade (views).

## Principais Etapas

- **Pré-processamento:**  
  Limpeza da base, remoção de registros irrelevantes (como livros/discursos), identificação e recuperação de músicas originalmente classificadas como 'misc', e tratamento de duplicidades.
- **Análise Exploratória (EDA):**  
  Visualização das principais características da base, como distribuição por artista, ano, idioma e views.
- **Limpeza dos dados:**  
  Padronização das letras, remoção de anotações estruturais e preparação dos dados para análise de sentimentos.
- **Análise de Polaridade:**  
  Utilização do VADER Sentiment Analyzer para calcular scores de sentimento e classificar cada música em positiva, neutra ou negativa.
- **Visualizações:**  
  Geração de gráficos para ilustrar padrões de polaridade por artista, por período, e relação entre sentimento e popularidade.

## Estrutura do Repositório

- `codigoFonte.py` — código fonte com todas as etapas do processamento, análise e visualização.
- `Relatorio Técnico.pdf` — relatório detalhado descrevendo desafios, decisões técnicas, métodos e resultados obtidos.
- (Opcional) `analise_sample_musicas_Versionfinal__.ipynb` — notebook com células interativas, gráficos e outputs para visualização passo a passo.

## Principais Resultados

- Recuperação eficaz de músicas legítimas originalmente classificadas como 'misc'.
- Análise automatizada da polaridade das letras, permitindo identificar tendências emocionais em diferentes artistas e períodos.
- Observação de que não há relação direta entre a polaridade do sentimento da letra e a quantidade de views das músicas.
- Ferramenta modular e reprodutível para futuras análises, classificação automática ou geração de letras musicais.

## Como utilizar

1. **Requisitos:**  
   - Python 3.x  
   - Bibliotecas: `pandas`, `matplotlib`, `seaborn`, `vaderSentiment`, `re`

2. **Execução:**  
   - Certifique-se de que o arquivo de dados (CSV/ZIP) possua as mesmas colunas utilizadas neste projeto:
      `title`, `artist`, `year`, `lyrics`, `language`, `tag`, `views`, `id`, `language_cld3`, `language_ft`  
       *(As colunas `id`, `language_cld3` e `language_ft` são descartadas no início do processamento.)*
   - Ajuste o caminho do dataset no arquivo `.py` conforme sua máquina.
   - Execute o script `codigoFonte.py` em seu ambiente Python.
   - (Opcional) Abra o notebook `.ipynb` para uma experiência interativa.

4. **Saídas:**  
   - Gráficos e prints com os principais resultados da análise.
   - Relatório técnico para consulta detalhada.

## Autor

Hugo de Souza Almeida  
Desafio de Análise Textual - 2025

---

Fique à vontade para abrir issues ou sugerir melhorias!
