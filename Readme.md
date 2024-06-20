Introdução
Este é o README do projeto de API web Agenda APP, desenvolvido para a disciplina
Programação para Web. A API é uma ferramenta para organizar suas atividades que tem para realizar podendo fazer uma 
lista de atividades, criando, editando, exlcuindo e consultando para facilitar nas tarefas diarias ou semanais.
Funcionalidades
● [Funcionalidade 1]: criação de usuário
● [Funcionalidade 2]: login de usuário com autenticação
● [Funcionalidade 3]: CRUD de tarefa

Requisitos
● [Requisito 1]: Criacao de um ambiente virtual
● [Requisito 2]: instalar o requirements.txt
● [Requisito 3]: iniciar o Uvicorn

Instalação
● Requisitos pré-requisitos:[Requisito 1]
1- Abra seu terminal powershell e digite esses comandos se estiver no windows:
2- para criar: python -m venv nome_do_ambiente
3- Para Ativar: nome_do_ambiente/Scripts/Activate.ps1
4- Caso der erro rode esse politicas de grupo do usuario local rode esse depois ativa:
5- nome_do_ambiente/Scripts/Activate.ps1
MAC- Ja no Mac e um pouco diferente:
6- para criar: python -m venv nome_do_ambiente
7- Para Ativar: source nome_do_ambiente/bin/activate
● Requisitos pré-requisitos:[Requisito 2]
1- pip install -r requirements.txt
● Requisitos pré-requisitos:[Requisito 3]
1- no ambiente virtual digite: uvicorn main:app --reload
2- depois abra o link no navegador asicionando uma "/"
3- pronto sua aplicacao estara rodando

Uso da API
Auth.py
O arquivo auth.py contém a lógica de autenticação de um aplicativo usando FastAPI. Aqui estão os principais pontos:
●	Importações e Configurações: O código importa várias bibliotecas necessárias para o roteamento, autenticação e criptografia de senhas. Também define uma chave secreta e um algoritmo para JWT (Token Web JSON).
●	Modelos de Usuário: Utiliza modelos para a estrutura de dados dos usuários, incluindo funções para criar e verificar hash de senhas.
●	Roteador e Rotas: Define um roteador para autenticação com rotas específicas para login, logout e registro de usuários.
●	Funções de Autenticação:
○	authenticate_user: Verifica se o usuário existe e se a senha está correta.
○	get_password_hash e verify_password: Funções para criar e verificar a hash das senhas.
●	Rotas Detalhadas:
○	/auth/login: Autentica o usuário e retorna uma resposta HTML com o resultado.
○	/auth/logout: Faz o logout do usuário, limpando o cookie.
○	/auth/register: Rota para registrar um novo usuário, garantindo que as informações sejam válidas e as senhas coincidam.
Todos.py
O arquivo todos.py define a lógica para um sistema de gerenciamento de tarefas (To-Dos) utilizando FastAPI. Aqui estão os detalhes importantes:
●	Roteamento e Dependências: Este módulo usa APIRouter para definir rotas relacionadas a tarefas (To-Dos). Ele também depende de um sistema de autenticação definido em auth.py para identificar o usuário atual.
●	Modelos de Dados: Utiliza modelos de dados para representar tarefas, que são armazenadas e gerenciadas em um banco de dados SQL.
●	Rotas Definidas:
○	/todos/: Lista todas as tarefas do usuário autenticado.
○	/todos/add-todo: Formulário para adicionar uma nova tarefa.
○	/todos/add-todo: POST para criar uma nova tarefa com detalhes como título, descrição e prioridade.
○	/todos/edit-todo/{todo_id}: Formulário para editar uma tarefa e POST para submeter as alterações.
○	/todos/delete/{todo_id}: Deleta uma tarefa específica.
○	/todos/complete/{todo_id}: Altera o estado de uma tarefa para completa ou incompleta.

Contribuição
● [Contribuidor 1]: José Mário Bernardes da Silva
● [Contribuidor 2]: Bruna Suda Moreira
GIT: https://github.com/JoseMarioBernardes/Projetoweb
