# Documentação Backend - Backian

1. Descrição do Módulo
O módulo de Autenticação de Usuários da loja de roupas é responsável por gerenciar o processo de autenticação e autorização dentro do sistema de vendas online. Ele assegura que apenas usuários autenticados e autorizados possam acessar suas contas, visualizar pedidos, e realizar compras de forma segura. Além disso, gerencia as sessões dos usuários para garantir uma experiência contínua e protegida.

2. Lista de Requisitos
2.1 Requisitos Funcionais
2.1.1 Cadastro de Usuário
O sistema deve permitir que novos usuários se cadastrem com dados básicos (nome, e-mail, senha) para criar uma conta na loja.
Cada e-mail deve ser único para garantir que não haja duplicidade de contas.

2.1.2 Login de Usuário
Permitir que os clientes façam login com e-mail e senha para acessar suas contas e histórico de compras.
O sistema deve gerar um token de sessão válido por um período configurável para manter o cliente logado durante a navegação na loja.

2.1.3 Recuperação de Senha
Disponibilizar uma funcionalidade para que os clientes recuperem suas senhas por meio de um e-mail de recuperação.

2.1.4 Autorização de Acesso
O sistema deve permitir o acesso a recursos específicos com base nos papéis dos usuários (ex: administrador, cliente comum).

2.1.5 Logout
Permitir que os clientes se desloguem e invalidem seu token de sessão, protegendo suas informações pessoais.

2.2 Requisitos Não Funcionais
2.2.1 Performance
O módulo deve responder a requisições de autenticação em menos de 200ms para garantir uma experiência de compra rápida e fluida.

2.2.2 Segurança
As senhas dos clientes devem ser armazenadas de forma segura utilizando técnicas de hashing e salting.
O módulo deve seguir as melhores práticas de segurança, incluindo proteção contra ataques como SQL injection e brute force, para garantir a segurança dos dados dos clientes.

2.2.3 Escalabilidade
Deve suportar pelo menos 1000 requisições simultâneas, especialmente durante períodos de alta demanda, como promoções e datas comemorativas.

2.2.4 Compatibilidade
O módulo deve ser compatível com os principais navegadores e dispositivos móveis, garantindo que os clientes possam acessar a loja de qualquer plataforma.

3. Regras de Negócio
3.1 Política de Senha
A senha dos clientes deve ter pelo menos 8 caracteres, incluindo uma letra maiúscula, uma minúscula e um número, garantindo a segurança das contas.

3.2 Verificação de E-mail
O e-mail deve ser verificado após o cadastro para ativar a conta e permitir que o cliente acesse funcionalidades como compras e acompanhamento de pedidos.

4. Requisitos de Usuário
Como cliente, quero ser capaz de me cadastrar na loja para fazer compras e acompanhar meus pedidos.
Como cliente, desejo poder recuperar minha senha caso a esqueça, para não perder o acesso à minha conta.
Como cliente, quero poder me deslogar para garantir que minha conta fique protegida.

5. Requisitos de Sistema
O sistema deve armazenar dados de autenticação dos clientes em um banco de dados seguro e eficiente.

6. Análise de Viabilidade
6.1 Tecnologias Disponíveis
Linguagens de Programação: JavaScript, Python (Django)
Frameworks: Express.js, Django
Banco de Dados: MySQL

6.2 Justificativas de Escolha
Linguagem e Framework: Express.js foi escolhido pela sua alta performance e escalabilidade, essenciais para uma loja online. MySQL foi selecionado para garantir a integridade e segurança dos dados dos clientes.

7. Priorização de Requisitos
7.1 Técnica MoSCoW
Must Have (Deve Ter):

Cadastro de Usuário
Login de Usuário
Autorização de Acesso

Should Have (Deveria Ter):

Recuperação de Senha
Logout
Could Have (Poderia Ter):

Performance (importante para uma experiência de compra satisfatória)
Won’t Have (Não Terá):

Funcionalidades na fase inicial, como suporte a múltiplos fatores de autenticação.

7.2 Critérios de Prioridade
Valor de Negócio: Funcionalidades básicas de autenticação são cruciais para o funcionamento da loja online e têm alta prioridade.

Urgência: A recuperação de senha é importante, mas pode ser implementada após a funcionalidade principal.

Risco e Custo: Implementações relacionadas à segurança são críticas e devem ser bem priorizadas para minimizar riscos e proteger os dados dos clientes.

