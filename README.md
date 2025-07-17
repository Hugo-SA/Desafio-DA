# Análise de Letras de Músicas

Este repositório contém o código fonte e o relatório técnico do desafio de análise textual em uma base de letras de músicas. O projeto tem como objetivo principal realizar o pré-processamento, a análise de polaridade e a análise exploratória de dados (EDA) para compreender padrões linguísticos, emocionais e temporais das composições musicais.

## Descrição do Desafio

A tarefa consistiu em analisar uma base textual heterogênea, inicialmente composta por músicas, trechos de livros, discursos, entre outros. O foco foi filtrar e estruturar apenas as músicas, e posteriormente realizar uma análise de sentimentos (polaridade) das letras ao longo do tempo, considerando também aspectos como artistas, anos e popularidade (views).

" Neste processo de seleção, iremos realizar essas etapas utilizando uma base de dados textuais contendo letras
de músicas. A base contém o título da música, o autor, outros envolvidos, ano de produção, a letra da música e
outras informações. Essa base possui também alguns poemas e livros. Cada entrada pode ter quebras de linhas,
o que precisar de algum pré-processamento. Vale ressaltar que o arquivo é relativamente grande. Então
recomenda-se utilizar apenas trecho dele para testes de forma a não comprometer seu ritmo de programação.
Com essa base de dados, você deve:

(1) Explorar os dados: apresente análises numéricas e/ou gráficos para mostrar os dados que você possui,
como a base está dividida e quais relações você poderia explorar desses dados.

(2) Tratar a base: normalizar os dados, eliminar atributos que julguem irrelevantes e realizar outros ajustes
que julgar importantes.

(3) Realizar uma das tarefas abaixo:

a. Analisar a polaridade (negativo/neutro/positivo) das letras de música e a polaridade das musicas
de um dado artista foi mudando ao longo do tempo. Ainda, encontrar aqueles artistas que
tiveram uma variação mais relevante de polaridade ao longo do tempo. Verificar se há uma
relação entre a polaridade a música e a quantidade de views que a letra teve.

b. Predizer o gênero musical (rap/pop/etc) de uma música à partir da sua letra. Avaliar a qualidade
do processo de predição.

c. Gerar novas letras de música à partir do conteúdo desta base. Crie um modelo generativo que
vai receber o começo de uma letra e gerar o restante da música.

d. Verifique a rede de colaboração de artistas através de um grafo. Encontre comunidades de
colaboração neste grafo.

(4) Documente todo o processo.

2. Instruções adicionais

 Utilize as ferramentas, linguagens de programação, frameworks, etc, que desejar. Não estamos
interessados em uma ferramenta/linguagem específica. Contudo, tudo deve estar documentado.

 Se você não conseguiu completar todas as tarefas não tem problema! Mesmo não terminando tudo,
envie ainda assim o que você fez, descreva no relatório os obstáculos que teve. Nosso objetivo é avaliar
suas estratégias. Queremos discutir contigo as ideias que teve. Mostre até onde chegou e como chegou.

O formulário está dividido em duas seções, a primeira com os dados pessoais e a segunda com a resolução da
prova, conforme descrição abaixo:

 Arquivo 1 - Código fonte

 Arquivo 2 - Relatório informando como foi seu processo de análise/desenvolvimento, ferramentas que
usou, as ideias que teve para resolver cada um dos passos do projeto, experimentos com o modelo de
predição, etc. Seja detalhado e claro o suficiente para entendermos seu processo e, principalmente, as
conclusões que você chegou em cada tarefa.

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
