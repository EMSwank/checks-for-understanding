## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
A cookie is a small text file that's stored on the client side with information about the session on a server.
2. What’s the difference between a session and a cookie?
Sessions live on the server, where cookies live on the client/browser.
3. What’s a flash and when do you want to use flashes?
It's a small animated message. You'd want them to pop up to tell the user if there's a problem submitting a form or a confirmation something has been edited or deleted.
4. Why do people say “HTTP is stateless”?
Because http is just a protocol that exists in static text files. It doesn't do anything by itself.
5. What’s authentication? Explain.
Authentication is a process of determining the user's access level to a site.
6. What’s the difference between authentication and authorization?
Authentication is getting access, and authorization is the features a user is able to see/use based on their access level.
7. What’s a before filter?
It's a way to check if certain things like whether a user is an admin are present.
8. How do we keep track of a user once they’ve logged in?
This is kept in a session, so when a user accesses a site, the user's browser will send a key to the website that tells the website who you are and what access you have.
9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
Use a namespace to limit access to certain paths to certain user levels. Use nested resources to indicate that a resource is a "child" of another resources.
10. At a high level, what tools can you use to implement authorization? How would you use them?
Tools? There are gems like Devise. You would need to require the gem and read the docs to find out how to use it.
11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
An enum is a way to turn an attribute into an integer in a database. It lives in the model.
12. What are some strategies you can use to keep your views DRY? You can use partials and the application.html.erb files to have one place that will have templates for other pages within the app.


### Reviews Questions 
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}
]
```  
holidays = array.map {|holiday| holiday[:holiday][:name]}
print holidays.sort.reverse

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300? 
.to_i

### Self Assessment:
Choose One:

* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:

* I feel comfortable with the content presented this week
