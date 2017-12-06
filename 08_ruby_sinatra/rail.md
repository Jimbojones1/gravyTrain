# Rails commands

### starting a new rails app

1. `rails new intro_app_api --api -d postgresql`

### Makind a database

1. `rails db:create`

`rail dbconsole`
- opens up the console to interact with database

### Migration to create table

- CreateTodos is the table name, this creates a migration in the db folder under migrate
add the columns that you want on the table
1. `rails generate migration CreateTodos`


### Migrate the table and create them in sql

1.  `rails db migrate`


### Run migration to add a foregin key column to a table('todos')

1. `rails g migration AddUserIdToTodos`


```
class AddUserIdToTodos < ActiveRecord::Migration
  def change
    add_column :todos, :user_id, :integer
  end
end

```

- Then run `rails db:migrate`

- Don't forget to set up active record migrations




### Routes

`open config/routes.rb`

- if you add the line resources :songs`, (songs is name of enpoint) will create five JSON RESTFUL routes

- Then Run `rails routes`


