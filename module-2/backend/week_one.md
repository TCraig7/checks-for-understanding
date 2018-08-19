## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.

  * PUT - Update
  * POST - Create
  * GET - Read
  * DELETE - Delete
  * PATCH - Update

2. What is Sinatra?

  * Sinatra is a ruby web application framework

3. What is MVC?

  * MVC stands for Model, View, Controller, and is a design pattern.

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?

  * Readability
  * Makes it so most websites use the same thing, which makes data manipulation easier

5. What types of variables are accessible in our view templates without explicitly passing them?

  * Not sure

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = '1'
    erb :index, :locals => { :name => 'Mr. Ed' }
  end
  ```

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

  * See above

8. What's the purpose of ERB?

  * To allow us to use Ruby but have it output html.

9. Why do I need a development AND test database?

  * Because you don't want to test your new code in the development db and end up breaking stuff, and then have to fix it while people are trying to use it, or it ends up crashing your whole website and no one can use it.

10. What is CRUD and why is it important?

  * Create, Read, Update, and Delete. It is important because these are the major ways in which we interact with a resource.

11. What does HTTP stand for?

  * Hypertext Transfer Protocol

12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?

  * <% %> and <%= %>. The way without the equal sign will just run the ruby code, while the way with the equal sign will print the code out to the website or resource.

13. What's an ORM? What does it do?

  * Object Relational Mapping. It wraps our data in Ruby objects to make them easier to manipulate.

14. What's the most commonly used ORM in ruby (Sinatra & Rails)?

  * ActiveRecord

15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

  * GET '/' - to view the dashboard
  * GET '/restaurants' - to view the restaurants
  * GET '/restaurants/new' - to create a new restaurant
  * POST '/restaurants' - to save the new restaurant
  * GET '/restaurants/:id' - to show one restaurant
  * GET '/restaurant/:id/edit' - to got to the edit page for the restaurant with the corresponding ID
  * PUT '/restaurant/:id' - to update the task
  * DELETE '/restaurant/:id' - to delete the restaurant

16. What's a migration?

  * A migration is what makes changes to a database. So for instance, to create a new column in a table.

17. When you create a migration, does it automatically modify your database?

  * You have to run rake db:migrate in order to modify the database.

18. How does a model relate to a database?

  * A model gives the database some requirements for the database. So for instance, whether the model belongs to any other model, or whether anything is required in order to be valid.

19. What is the difference between `#new` and `#create`?

  * Not sure

20. Given a table named `animals`, What is the SQL query that will return all info from that table?
    `id     name        number_of_legs
    -----   ------      --------------
      1     panda       4
      2     giraffe     4
      3     whale       0
      4     bird        2
    `
    * SELECT * FROM animals;

21. Using the same table, What is the SQL query that will return only the animals that has 4 legs?

  * SELECT * FROM animals
    WHERE number_of_legs=4;

### Review Questions:  
22. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  

  * require '../films.csv'
  * require 'csv'

  * CSV.foreach('../films.csv, headers: true, header_converters: symbol') do |film|...

23. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```
How would I add 'granola bar' to things you should have when hiking?

  * activities[hiking][supplies] = 'granola bar'

24. What are the 4 Principles of OOP? Give a one sentence explanation of each.

 * Don't Repeat Yourself (DRY) - Write your code in a way that allows for it to be reused in other places.
 * Single use Responsibility Principle (SRP) - Make your classes, methods, etc. be responsible for one thing.
 * Classes fewer than 80 lines and methods fewer than 7 lines - Kind of self explanatory.
 * Can't remember this one

### Self Assessment:
Choose One: (erase the others)
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel overwhelmed by the content presented this week
