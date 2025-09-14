# Módulo de Memória

- Esse módulo é responsável por Interface com Banco de Dados para recuperação 
- Armazenar as threads de conversações com usuários
- Sintetizar as threads longas, mantendo o contexto coeso, simples e objetivo
- Estabelecer parâmetros como:
  - Janela de Memória/Esquecimento em relação ao tempo
  - Janela de Memória/Esquecimento em relação ao comprimento máximo

- Interface Pública
  - NewThread(user) -> Cria uma nova conversação
  - List(user) -> Retorna a lista de conversações do usuário
  - Get (user, thread, limit=None) -> Retorna as mensagens de uma conversação do usuário
  - Store(user, thread, messages) -> Armazena novas mensagens em uma conversação do usuário
  - Summary(user, thread, limit) -> Sintetiza uma conversação do usuário

- Invoca o módulo de Inferência para Síntese, limitado ao tamanho T
