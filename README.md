# Getting Started With Ruby on Rails

## Installation
In progress...

## Let's Get To It!

Install Gems
```bash
bundle install
```
Check out available routes:
```bash
bundle exec rake -T
```
## Migrations

Create users migration file.
```bash
rails generate migration CreateUsers
```

In DB/MIGRATE FOLDER
```ruby
class CreateUsers < ActiveRecord::Migration
  def change
    create_table users do |t|
      t.string :first_name
      t.string :last_name
      t.integer :email

      t.timestamps
    end
  end
end
```

Create User's model

```bash
be rake generate:model NAME=Users
```
In the **app** folder
```ruby
class User < ActiveRecord::Base
  has_many
end
```

CREATE & MAKE THE TABLE OR ELSE NOTHING WILL SAVE!

```bash
bundle exec rake db:drop
bundle exec rake db:create
bundle exec rake db:migrate
bundle exec rake db:seed 
# (if you have a database)
be shotgun
```
In the browser navigate to: localhost:9393


If you wanna check out what's in the database

```bash
bundle exec rake console
Link.connection
Link
```
