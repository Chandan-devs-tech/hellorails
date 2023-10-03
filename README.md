# README

I have done this exercise following these steps :
- Install rails :
```
gem install rails
```
- For checking the version of your rails :
```
rails --version
```
- Create a new app called 'hellorails'.
```
rails new hellorails --database=postgresql
```
- Initialize your project with Git.
```
git init
```
- Make sure that your project has Postgres database set up.
  - Configure the config/database.yml file :
```
default: &default
  adapter: postgresql
  encoding: unicode
  pool: <%= ENV.fetch("RAILS_MAX_THREADS") { 5 } %>
  username: postgres
  password: postgre1990
  host: localhost
development:
  <<: *default
  database: hellorails_development
test:
  <<: *default
  database: hellorails_test
production:
  <<: *default
  database: hellorails_production
```
  - gem install pg
  - check the GemFile to have `gem "pg", "~> 1.1"`
  - bundle install
  - `rails db:create`
  - `rails db:migrate`
- Run rails server and visit http://localhost:3000/ in your browser!
`rails server`
For Play with your first Rails website :
- `rails generate controller Pages hello`
- Open the file `app/views/pages/hello.html.erb` and add an `h1` element saying `Hello world`.
- Open http://localhost:3000/pages/hello in your browser. You should see your "Hello world" message.
- In `config/routes.rb` replace get `pages#hello` with root `pages#hello`
- Revisit http://localhost:3000/ and see your changes in action. Now your `Hello world` page should be displayed as the main page.