# Módulo de Memória

- Esse módulo é responsável por Interface com Banco de Dados para recuperação 
- Armazenar as threads de conversações com usuários
- Sintetizar as threads longas, mantendo o contexto coeso, simples e objetivo
- Estabelecer parâmetros como:
  - Janela de Memória/Esquecimento em relação ao tempo
  - Janela de Memória/Esquecimento em relação ao comprimento máximo

- Invoca o módulo de Inferência para Síntese, limitado ao tamanho T
