## rails generic commands
- rails new projectName  - creates a new rails project with a bunch of folders and files

- rails s : runs the server on port 3000

- rails g controller game page : creates a game_controller.rb in  controller and page method also page.html.erb in the views folder

- rails g model Game name:string price:integer - create a Game model and database file which contains games table


## Note: migrate files created in the db folder is just a reference to the rails application, unless you generate a schema, the sqlite database is not aware of what table was created.hence you run the command below

- rails db:migrate : creates a copy/blueprint for sqlite database

- rails c - similar to irb playaround with the database in console window


## commands to be run in the console:
## CRUD system: Create, Read , Update and Delete

- How to Create or add elements to database

``Game.create(name: "Mario", price:100)``

- List all the items in the database
``Game.all``

- Read elements from the database
``first_game = Game.first``

``last_game = Game.last``

``find_game_by_id = Game.find(3)``  - finds the third game in the db

``find_by_key = Game.find_by(name: "Mario")``  - lists the first item in the db matching the search

``filter_by_key = Game.where(name: "Mario") `` //lists all items matching the search

## Note the difference between find_by and where methods

- Update elements from database

`` first_game = Game.first
first_game.update(name: "Ruine Escape")``

- Delete elements from database
`` find_game_id = Game.find(3)
find_game_id.destroy``
