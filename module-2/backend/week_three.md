## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
rails new _project_name_ -T -d='postgresql'
2. What do Models generally inherit from in rails?
ApplicationRecord
3. What do Controllers generally inherit from in a rails project?
ApplicationController
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
resources horse, only: :show
5. What rake task is useful when looking at routes, and what information does it give you?
rake routes - Give you all available routes to call
6. What is an example of a route helper? When would you use them?
'/user/:id' You use them to tell which controller to use.
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
8. What are strong params and why are they necessary?
They sanitize the incoming data so as to guard against an SQL injection attack
9. What role does `form_for` play in helping us create our forms?
It automatically generates the forms with the proper verbs and paths
10. How does `form_for` know where to submit the user's input?
    It uses the route helpers to know where to use the verb to post
11. Create a form using a `form_for` helper to create a new `Horse`. 
      <%= form_for :horse do |f| %>
        <%= f.text_field :name %>
        <%= f.submit %>
      <% end %>
12. Why do we want to validate our models?
    To make sure there're hooked up right (rails is seeing it), and to dictate what fields are required.
13. What are the steps of the DNS lookup?
    The OS sends a request to the DNS server and receives back an IP address which then gets used to send the HTTP request to the server. The server receives the request, the processes it, and finally responds back to the client.

### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?
    Horse.move.prance
    
15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3? 
true :  furniture[:puchased]
3 :  furniture[:table][:height]
16. What is inheritance?
  When a class and its class methods are connected to another clas.

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
<<<<Somewhere in here>>>>
* I feel overwhelmed by the content presented this week

Sometimes I feel like I don't know what I know, but then it turns out I do. Sometimes not. It's confusing at times...
