# Heroku MyApp

```sh
# Logar no Heroku
heroku login

# Instalar a gem do rails
gem install rails --no-document

# Criar uma nova aplicação chamada heroku-myapp
rails new heroku-myapp --database=postgresql --skip-action-cable --skit-turbo-links

# Acessar a aplicação criada
cd heroku-myapp

# Criar o banco de dados
rails db:create

# Importar a gem do postgresql
gem 'pg'

# Instalar todas as gems pendentes
bundle install

# Copiar as configurações de outro projeto
cp ../rails-react-learning/config/database.yml config/database.yml
cp ../rails-react-learning/.env .
cp ../rails-react-learning/docker-compose.yml .
cp ../rails-react-learning/Procfile.dev .

# Criar um novo controlador chamado welcome
rails generate controller welcome

# Conteúdo do controlador welcome
<h2>Hello World</h2>
<p>
  The time is now: <%= Time.now %>
</p>

# Configurando a rota
root 'welcome#index'

# Inicializando o projeto
docker-compose up --build
overmind start

# Configurando o _config/environments/production.rb_
config.public_file_server.enabled = ENV['RAILS_SERVE_STATIC_FILES'].present?

if ENV["RAILS_LOG_TO_STDOUT"].present?
  logger           = ActiveSupport::Logger.new(STDOUT)
  logger.formatter = config.log_formatter
  config.logger = ActiveSupport::TaggedLogging.new(logger)
end

# Commitando o projeto
git init

git add .

git commit -m "init"

# Criando um novo dyno no Heroku
heroku create

# Configurando o dyno
git config --list | grep heroku

# Push no Heroku
git push heroku master

# Atualizando o banco
heroku run rake db:migrate

# Escala a aplicação
heroku ps:scale web=1

# Mostra a escala
heroku ps

# Inicia a aplicação
heroku open
```
