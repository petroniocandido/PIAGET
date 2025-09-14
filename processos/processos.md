# Módulo de Processos

Esse módula implementa a estrutura e dinâmica dos Agentes, implementando os fluxos de lógica e conectando todos os processos de Engenharia de Prompt, Engenharia de Contexto, Recuperação, Chamada de Ferramentas e Interface com o usuário.

1. Recebe uma requisição da Interface com o Usuário contendo um prompt
2. Invoca o módulo de Ferramentas, para receber informações contextuais e do usuário
3. Invoca o módulo de Mémoria, para receber um sumário da conversação (se existir)
4. Invoca o módulo de Conhecimento, para enriquecer o prompt com conhecimento especializado
5. Constrói o prompt inicial
6. Loop de Construção da Saída
   1. Invoca o módulo de Inferência para Geração com os padrões Chain-Of-Thought e Self-Consistency, recebendo uma lista com k respostas
   2. Invoca o módulo de Inferência para Decisão entre a lista com k respostas
   3. Verifica se há invocação para Ferramentas. Se houver Invoca o módulo de Ferramentas e agrega a resposta ao prompt
   4. Invoca o módulo de Inferência para Geração final
   5. Invoca o módulo de Inferência para Avaliação de Confiança e Completude
      1. Se a saída for SIM, termina o loop de Construção da Saída
      2. Se a saída for NÃO, volta ao início do loop de Construção da Saída
11. Invoca o módulo de Mémoria, para armazenar a rodada atual da conversação (prompt + saída)
12. Envia resposta para a Interface

- Considerar avaliar uma classificação de sentimento no prompt do usuário

- Interface Pública|
  - Query(usuario, thread, prompt)
