# Recuperação de senha
  **Requisitos Funcionais**
  - O usuário deve poder recuperar sua senha informando o seu email;
  - O usuário deve receber um email com instruções de recuperação de senha;
  - O usuário deve poder restar seu senha;

  **Requisitos Não Funcionais**
  - Utilizar Mailtrap para envio de emails em ambiente de desenvolvimento;
  - Utilizar Amazon SES para envios em produção;
  - O envio de e-maisl deve acontecer em segundo plano (background job - fila);

  **Regras de Negócio**
  - O link enviado por email para resetar a senha, deve expirar em 2h;
  - O usuário precisa confirmar a nova senha ao reseta-lá;


# Atualização do perfil
  **Requisitos Funcionais**
  - O usuário deve poder atualizar seu perfil: nome, email e senha;

  **Requisitos Não Funcionais**

  **Regras de Negócio**
  - O usuário não pode alterar seu email para um email já cadastrado por outro usuário;
  - Para atualizar sua senha, o usuário deve informar a senha antiga;
  - Para atualizar sua senha, o usuário deve confirmar a nova senha;


# Painel do prestador
  **Requisitos Funcionais**
  - O usuário deve poder listar todos os seus agendamentos de um dia específico;
  - O prestador deve receber uma notificação sempre que houver um novo agendamento;
  - O prestador deve poder visualizar todas as notificações não lidas;

  **Requisitos Não Funcionais**
  - Os agendamentos do presdor no dia devem ser armazenados em cache;
  - As notificações do prestador devem ser armazenads em MongoDB;
  - As notificações do prestador devem ser enviadas em tempo real utilizando Socket.io;

  **Regras de Negócio**
  - A notificação deve ter um status de lida ou não lida para controle do prestador;


# Agendamento de serviços
  **Requisitos Funcionais**
  - O usuário deve poder listar todos os prestadores de serviços;
  - O usuário deve poder listar os dias de um mês com os horários disponíveis de um prestador;
  - O usuário deve poder listar os horários disponíveis em um dia específico de um prestador;
  - O usuário deve poder realizar um novo agendamento com um prestador;

  **Requisitos Não Funcionais**
  - A listagem de prestadores devem ser armazenadas em cache;

  **Regras de Negócio**
  - Cada agendamento deve durar uma hora;
  - Os agendamentos devem estar disponíveis entre as 8h às 18h;
  - O usuário não pode agendar um horário já ocupado;
  - O usuário não pode agendar em um horário que já passou;
  - O usuário não pode agendar um horário consigo mesmo;'


