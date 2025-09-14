# Módulo de Processos

Esse módula implementa a estrutura e dinâmica dos Agentes, implementando os fluxos de lógica e conectando todos os processos de Engenharia de Prompt, Engenharia de Contexto, Recuperação, Chamada de Ferramentas e Interface com o usuário.

- Recebe uma requisição da Interface com o Usuário contendo um prompt
- Invoca o módulo de Ferramentas, para receber informações contextuais
- Invoca o módulo de Mémoria, para receber um sumário da conversação (se existir)
- Invoca o módulo de Conhecimento, para enriquecer o prompt com conhecimento especializado
- Constrói o prompt
- Invoca o módulo de Inferência para Geração com os padrões Chain-Of-Thought e Self-Consistency, recebendo uma lista com k respostas
- Invoca o módulo de Inferência para Decisão entre a lista com k respostas
- Verifica se há invocação para Ferramentas. Se houver Invoca o módulo de Ferramentas e agrega a resposta ao prompt
- Invoca o módulo de Inferência para Geração final
- Envia resposta para a Interface

