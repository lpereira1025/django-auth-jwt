<h1>Django Auth Project</h1>
Este projeto é uma aplicação de autenticação utilizando Django e Django REST Framework.

<h2>Funcionalidades</h2>
<li>Registro de usuários</li>
<li>Login de usuários</li>
<li>Logout de usuários</li>
<li>Visualização de perfil de usuário</li>
<li>Autenticação baseada em JWT</li>
  
<h2>Tecnologias Utilizadas</h2>
<li>Python 3.12</li>
<li>Django 3.1.3</li>
<li>Django REST Framework</li>
<li>MySQL</li>
  
<h2>Pré-requisitos</h2>
<li>Python 3.12</li>
<li>MySQL</li>
  
<h2>Configuração do Ambiente</h2>
<li>Passo 1: Clonar o repositório</li>
<li>Passo 2: Criar e ativar um ambiente virtual: python -m venv venv</li>
<li>Passo 3: Instalar as dependências</li>
  
<h3>Atualizando o pip</h3>
Você pode precisar atualizar o pip antes de instalar as dependências. Se você encontrar problemas de permissão ao atualizar pip no Windows, siga as instruções abaixo.
<h3>Método 1: Executar como administrador</h3>
Abra o Prompt de Comando ou PowerShell como administrador (clique com o botão direito e selecione "Executar como administrador").
Execute o comando:
python.exe -m pip install --upgrade pip

<h3>Método 2: Usar a opção --user</h3>
Execute o comando no seu terminal atual:
python.exe -m pip install --upgrade pip --user
Instalando as dependências do projeto<br/>
pip install -r requirements.txt
<li>Passo 4: Configurar o banco de dados</li>
Atualize as configurações do banco de dados no arquivo auth/settings.py para corresponder às suas credenciais MySQL:

python
Copiar código
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'yt_django_auth',
        'USER': 'root',
        'PASSWORD': 'rootroot'
    }
}
<li>Passo 5: Aplicar as migrações do banco de dados</li>
python manage.py migrate
<li>Passo 6: Criar um superusuário</li>
python manage.py createsuperuser
<li>Passo 7: Executar o servidor de desenvolvimento</li>
python manage.py runserver
A aplicação estará disponível em http://127.0.0.1:8000.

<h2>Endpoints da API</h2>
<li>POST /api/register: Registrar um novo usuário
<li>POST /api/login: Fazer login de um usuário
<li>GET /api/user: Visualizar informações do usuário autenticado
<li>POST /api/logout: Fazer logout de um usuário
