### Week 5 Questions

Re-pull from this repository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?

  * In the controller, write 'flash[:notice] = "Your message here."' in the method that you want.

2. Where is cart information/temporary information usually stored?

  * In the session

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?

  * We would not want to store the cart in our database because it would take up huge amounts of server space. We could also be potentially storing information that will never be used again, if a user adds something to the cart and then leaves.

4. What is the purpose of the asset pipeline?

  * To organize all of our styling stuff together

5. Why do we precompile our assets?

  * Because we can only send so much information at once. By precompiling, we can send more information.

6. What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```

  * stylesheet_link_tag = returns an HTML script that tells rails to pull from that file for styling
  * javascript_include_tag = returns an HTML script tag that points to a javascript file
  * image_tag = returns an HTMl tag that points to an image in the asset pipeline

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?

  * Elements of a great readme:
    1. Gem information
    2. Easy to read
    3. Instructions for the app

  * One benefit is that if you do the readme before you start the project, you have a guide of what you need to do and what the app is going to look like. Another benefit is that people who come to your app will understand what you are doing and will be able to use it more effectively.

8. What are the top four accessibility issues that we as developers should be aware of?

  * Sight
  * Motor
  * Hearing
  * Cognitive

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?

  * It's a callback
  * In the create action?                  

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```
  * Change the url

11. What is the difference between a scope and a class method?

  * I don't think we covered this is class and the documentation I can find is a bit confusing.

### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?

    * cart["48"] = 4

  12b. How would you increase the quantity of item 29?

    * cart["29"] += 1

  12c. How would you find out how many items your user is thinking about purchasing?  

    * cart.values.sum

13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?

    * Polymorphism is the ability of classes to inherit from a parent class. This allows the code to be dryer because methods that are applicable for multiple classes can be made just once and put into a parent class or super class.

    * An object's suitability is determined by the presence of certain methods and properties, rather than the type of the object itself. Basically if it walks like a duck and it quacks like a duck, it's a duck.

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?

  * string.delete!('()').gsub!(' ', '.')
    string.gsub('-','.')


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
