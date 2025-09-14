# Módulo de Conhecimento

O módulo de conhecimento possui dois sub-módulos:

1. Base de Conhecimento
   - Consulta por similaridade ou metadados à base de conhecimento e ao Grafo de Conhecimento, que contém os relacionamentos ontológicos entre as entidades/tópicos

2. Ingestor de Conhecimento
  - Pré-processamento de documentos, extração de tópicos, vetorização e inserção na Base de Conhecimentos

Dois pontos principais precisam ser definidos aqui:

a) Tecnologia de Banco de Dados Vetorial
  - Tecnologias sob inspeção: PGVec, Weaviate

b) Tipo de Embedding
  - Vetores Densos (Single Vector, Multi Vector) e Vetores Esparsos (BM25)

c) Tipo de Recuperação
  - Reuperação em 1 passo ou 2 passos (Rerank)

d) Grafo de Conhecimento ?

e) Campos de Metadados
  - Documento
  - URL
  - Datetime
  - Tipo

f) Lista de palavras especiais associadas à um nível de alarme (PROIBIDO, RISCO, )

- Interfaces
  - Query(prompt, metadata, k) -> Document
  - Store(document, metadata)
  - Topics(filter)
