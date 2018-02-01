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

* TERMINAL
rails generate migration CreateUsers

* DB/MIGRATE FOLDER
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

* Terminal
be rake generate:model NAME=Users

*APP FOLDER*
class User < ActiveRecord::Base
  has_many
end

*Terminal - CREATE & MAKE THE TABLE OR ELSE NOTHING WILL SAVE!
bundle exec rake db:drop
bundle exec rake db:create
bundle exec rake db:migrate
bundle exec rake db:seed (if you have a database)
be shotgun
*in chrome: localhost:9393

*Terminal - if you wanna check out what's in the DB
bundle exec rake console
Link.connection
Link
