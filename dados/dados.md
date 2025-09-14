# Módulo de Dados

Alguns pontos principais precisam ser definidos aqui:

a) Tecnologia de Banco de Dados 
b) Entidades
  - Usuários
    - id
    - LDAP name
    - e-mail
    - perfil
  - Perfis
    - id
    - Nome
  - Recursos
    - id
    - Recurso
  - Permissões
    - Recurso
    - Perfil
    - Permissão
  - Logs
    - timestamp
    - usuário
    - nível
    - descrição
  - Feedbacks
    - id
    - timestamp
    - usuário
    - texto

- Interface Pública
  - GetUserById(id)
  - GetUsers(filter)
  - GetLogs(filter)
  - GetFeedbacks(filter)
  - WriteFeedback(user, content)
  - WriteLog(log)
  - WriteUser(user)

