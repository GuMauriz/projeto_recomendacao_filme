# 🎬 Sistema de Recomendação de Filmes

Este projeto é um sistema de recomendação de filmes desenvolvido em Python. O objetivo principal é simular o funcionamento de plataformas de streaming, como a Netflix, sugerindo novos títulos semelhantes para o usuário logo após ele finalizar a visualização de uma obra.

## 🚀 Como Funciona?

O motor de recomendação deste sistema baseia-se na **Semelhança de Cossenos (Cosine Similarity)**. Ele calcula a distância e similaridade entre os filmes utilizando uma abordagem baseada em Processamento de Linguagem Natural (NLP). 

O fluxo de processamento dos dados ocorre da seguinte maneira:
1. **Unificação de Dados:** O algoritmo agrupa as principais informações categóricas e descritivas de cada filme (sinopse, elenco/atores, diretor, produtor, gêneros, etc.) em uma única coluna chamada `"tags"`.
2. **Pré-processamento (NLP):** É aplicada a técnica de *Stemming* (redução das palavras ao seu radical) para padronizar os termos e evitar redundâncias.
3. **Vetorização:** As tags textuais são transformadas em vetores numéricos.
4. **Recomendação:** A semelhança de cossenos compara o ângulo entre esses vetores; quanto mais próximos, mais semelhantes são os filmes. O algoritmo então devolve os títulos com a maior correspondência.

## 🛠️ Tecnologias Utilizadas

- **Python** (Linguagem principal)
- **Pandas & NumPy** (Manipulação e estruturação dos dados)
- **Scikit-Learn** (Vetorização dos dados e cálculo da Semelhança de Cossenos)
- **NLTK** (Processamento de Linguagem Natural e Stemming)

## 🔮 Melhorias Futuras

O modelo atual apresenta ótimos resultados ao capturar o contexto, a temática e a equipe técnica envolvida nos filmes. Contudo, ele considera **somente vetores construídos a partir de variáveis categóricas e textuais**.

Para refinar ainda mais as sugestões e criar um sistema de recomendação mais robusto e completo, as próximas atualizações deverão incluir:
- **Implementação de Variáveis Numéricas:** Combinar a atual análise de NLP com dados quantitativos da base, passando a considerar o peso de atributos como:
  - Ano de lançamento
  - Tempo de duração
  - Popularidade
  - Avaliação/Nota da obra