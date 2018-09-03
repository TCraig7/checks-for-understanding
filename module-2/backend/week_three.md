## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?

  * rails new name_of_project

2. What do Models generally inherit from in rails?

  * ApplicationRecord

3. What do Controllers generally inherit from in a rails project?

  * ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

  * resources :horse, only: [:show]

5. What rake task is useful when looking at routes, and what information does it give you?

  * rails routes - it gives you all of the routes available to you for each model

6. What is an example of a route helper? When would you use them?

  * horse_path(horse) - You would use them when you want to link to another route. For instance, the example I gave would allow a user to go to the horse show page to view a single horse.

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

  * A path helper returns the corresponding controller. In the case of horse_path(horse), this equates to /horses/1. A url helper returns the same path prefixed with the current host, port and path prefix.

8. What are strong params and why are they necessary?

  * Strong params are a private method that allows rails to control what type of things can come in for a controller. This is necessary because you don't want someone to be able to just enter any information into something. This could cause issues such as a database dropping.

9. What role does `form_for` play in helping us create our forms?

  * Form_for tells

10. How does `form_for` know where to submit the user's input?

  * Based on the model given to it. So in the example form below, we gave it @horse, and so it knows from that model.

11. Create a form using a `form_for` helper to create a new `Horse`.

  *  <%= form_for @horse do |f| %>

        <%= f.label :name %>

        <%= f.text_field :name %>

        <%= f.label :breed %>

        <%= f.text_field :breed %>

        <%= f.label :color %>

        <%= f.text_field :color %>

        <%= f.submit %>

      <% end %>

12. Why do we want to validate our models?

  * We want to validate our models because then we know what is required in order to make a new instance of something (such as :name or :age). This allows us to control how objects are made.

13. What are the steps of the DNS lookup?

  1. Starts at the browser/OS
  2. Goes to the local DNS server
  3. Which points to the root server
  4. Which goes to the top level DNS server
  5. Which directs to the authoritative DNS server
  6. Back to the browser/OS

### Review Questions
14. Within a feature test and given the following HTML, write the code necessary to target the following section and check the person's name?

  `<section id="personal-info">
    <h3><%= @person.name%></h3>
   </section>
  `

  * within(#personal-info) do
      expect(page).to have_content("Dave")
    end

15. How would you call the method `prance` from within the method `move` on a `Horse` instance?

  * def move

      prance
      
    end

16. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?

  * true: furniture[:table][:height]
  * 3: furniture[:purchased]

17. What is inheritance?
  * Inheritance is when a class has access to its parent class's methods. So if a horse class is created and inherits from animal, it will have access to the animal methods as well as its own.

### Self Assessment:
Choose One:

* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:

* I feel comfortable with the content presented this week
