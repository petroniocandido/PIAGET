# Módulo de Raciocício

- Serve como camada de isolamento e interface com os LLMs e a infraestrutura de inferência. O objetivo é padronizar as interações com o LLM.
- Atividades de Inferência: Raciocício/Explanação, Síntese, Tomada de Decisão, Embedding

- Interface: Prompt, Parâmetros -> Servidor Inferência -> Resposta

- Atividades
  - Conexão com o Servidor de Inferência
  - Parâmetros de Inferência
  - Tratamento Básico da Saída

- Interface Pública
  - Generate(prompt, limit) -> Text
  - Summarize(prompt, limit) -> Text
  - Embedding(prompt) -> Vector
  - Decide(prompt, options) -> Option
  - ExtractTopics(prompt) -> List[Text]
