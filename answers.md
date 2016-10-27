# Q0: Why is this error being thrown?

There is no Pokemon model in the application yet. This needs to be initalized.

# Q1: How are the random Pokemon appearing? What is the common factor between all the possible Pokemon that appear? *

The random Pokemon are appearing because we seeded the database with the Pokemon that
we created in seed.rb. Whenever the homepage is refreshed, one of the four Pokemon that we seeded into the database in the seed.rb file will appear.

# Question 2a: What does the following line do "<%= button_to "Throw a Pokeball!", capture_path(id: @pokemon), :class => "button medium", :method => :patch %>"? Be specific about what "capture_path(id: @pokemon)" is doing. If you're having trouble, look at the Help section in the README.
This line generates the "Throw a PokeBall!" button on the homepage. This button submits to the URL
created by "capture_path(id: @pokemon)" which maps to the ID of the Pokemon captured as the URL path. It also specifies the method argument, and in this case we want the PATCH operation as we are updating the trainer's profile with this captured Pokemon.

# Question 3: What would you name your own Pokemon?

RubyRailsMon


# Question 4: What did you pass into the redirect_to? If it is a path, what did that path need? If it is not a path, why is it okay not to have a path here?

I wanted to redirect the webpage back to the trainer's profile page at the end of the damage method, so I had redirect_to the "trainer_path" using the current_trainer.id as the parameter and this will redirect the webpage back to the trainer profile after hitting the damage button and updating the database of Pokemons accordingly. 

# Question 5: Explain how putting this line "flash[:error] = @pokemon.errors.full_messages.to_sentence" shows error messages on your form.

This line for erroring is put in an if/else clause, more specifically, in the case where the Pokemon cannot save to the database. This will now show the "@pokemon.errors.full_messages.to_sentence" error when we fail to create a Pokemon. 

# Give us feedback on the project and decal below!
Really enjoyed this project it was fun!

# Extra credit: Link your Heroku deployed app
