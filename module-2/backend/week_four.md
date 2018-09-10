## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?

  * A cookie is a piece of data that is stored in a user's browser.

2. What’s the difference between a session and a cookie?

  * A cookie is stored in the user's browser while a session is stored on a server.

3. What’s a flash and when do you want to use flashes?

  * A flash is a message that lets a user know something, such as an item has been added to a cart or there was an error when setting up an account.

4. Why do people say “HTTP is stateless”?

  * HTTP is stateless because nothing persists. That's why cookies and sessions are necessary; so that data is stored in between visits.

5. What’s authentication? Explain.

  * Authentication how a website keeps track of different users. So when a person logs on to a website, they should see their own profile and info, rather than another user's.

6. What’s the difference between authentication and authorization?

  * Authentication is how a website keeps track of different users, while authorization is what allows different users to do different things. Like an admin is able to alter things that a normal user cannot.

7. What’s a before filter?

  * A before filter is a method that runs before actions in a controller.

8. How do we keep track of a user once they’ve logged in?

  * Through sessions

9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?

  * Being honest, I don't fully understand this at all.

10. At a high level, what tools can you use to implement authorization? How would you use them?

  * I think name spacing is one, and enums are another.

11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?

  * An enum allows you create an attribute and then assign different values to it. For instance, you can make different types of users by mapping different values to them. It has to be an integer, because you are basically creating an array where the different values correspond to their index in the array. For example, if you enums values are [default, admin], then the default role is 0, and the admin role is 1. You declare an enum in your model.

12. What are some strategies you can use to keep your views DRY?

  * You can use the application.html.erb file in layouts. This allows you to show things across all pages so that you do not have to write them over and over again.


### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  

  * holidays.map do |holiday|
      holiday[:holiday][:name]
    end.sort

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?

  * .delete("$").to_i


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
