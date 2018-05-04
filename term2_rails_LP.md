## MVC and Rails Architecture the hard way
- Understand MVC (just with classes) without introducing to rails framework
- Create rails app using rails new myFirstApp -> understand the architecture and folder structure
- Create a game app, start with routes /games
- Create the controller with static content and instance variable , and view displaying static content and then the model to add multiple elements to the game apart from just title
- Understand database in console window
- Connect Model to view and controller and update the index method.


# Introduce CRUD system.
- Introduce route /games/new and then view , controller to create the games
- Access /games/id  -> to show a particular game
- Access /games/edit/id -> to edit a particular game
- Access /games/destroy -> to delete a particular game



## Challenge: Work on the rails get started page in the [rails guide ](http://guides.rubyonrails.org/getting_started.html)

#  Forms in detail

```
  <form accept-charset="UTF-8" action="/clients" method="post">
    <input type="text" name="client[name]" value="Acme" />
    <input type="text" name="client[phone]" value="12345" />
    <input type="text" name="client[address][postcode]" value="12345" />
    <input type="text" name="client[address][city]" value="Carrot City" />
  </form>
```

```
  def create
    @client = Client.new(params[:client])   
            # note: here params[:client], :client is an object containing the data filled out in the form
    if @client.save
      redirect_to @client
    else
      # This line overrides the default rendering behavior, which
      # would have been to render the "create" view.
      render "new"
    end
  end
```
- Form validation, and rendering back same form if the validation fails
[Action View form helpers](http://guides.rubyonrails.org/form_helpers.html)



## Rails Back Bone
- [Action controller](http://guides.rubyonrails.org/action_controller_overview.html)
- [Action View](http://guides.rubyonrails.org/action_view_overview.html)
- [Active record](http://guides.rubyonrails.org/active_record_basics.html)
- [Rails Routing](http://guides.rubyonrails.org/routing.html)

## Build an Instagram App

- Authentication
- Create home page
- profile page
- upload picture
- like and comment
- followers


## Generic content for other applications:
- Geocoder
- mailgun/sendgrid
- Stripe payments system

## [Cart creation guide](/agile-web-development-with-rails.pdf)

## Hackathon

## Final Project
