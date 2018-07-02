## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
GET -- get info from server/site,
POST -- create a new record,
PUT -- updates info in a record,
PATCH -- updates entire record
DELETE -- removes a record

2. What is Sinatra?
a light-weight webserver framework for ruby

4. What is MVC?
stands for Model, View, Controller. It's a design pattern that helps encapsulate responsibilities for software.

5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
For more universal compatibility on the web.

6. What types of variables are accessible in our view templates without explicitly passing them?
instance variables

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
name = 'Mr. Ed'

9. What's the purpose of ERB?
So you can run ruby code in html

10. Why do I need a development AND test database?
The development db is there to have data to populate while building the web app. the test database is used by the test suite to park test-data temporarily while the tests run.

11. What is CRUD and why is it important?
Create, Read, Update, Delete. CRUD is the essential pattern of most websites such as blogs to social media sites.

12. What does HTTP stand for? 
Hypertext Transfer Protocol.

13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
Not sure what is being asked here, but here's a guess: <%Foo.bar%>, <%= Foo.bar %>  The first one executes the code in the background, where the second one (with the equals sign), prints whatever the code executes to the screen.
14. What's an ORM?
Object-relational mapping--it turns db entries into objects so that Ruby (in this case) can exercise code on it.

15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
ActiveRecord

16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

17. What's a migration?
A migration creates the table heading for the database.

18. When you create a migration, does it automatically modify your database?
No. You have to run the rake db:migrate command.

19. How does a model relate to a database?
The model is what relates to the database through ActiveRecord.

20. What is the difference between `#new` and `#create`?
"#new" creates a new instance of an object, "#create" creates an instance adds an object that saves to the db.

### Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?
after requiring CSV and the model file, 
CSV.foreach('films.csv', headers: true, header_converters: :symbol) do |film|
  Film.create(id: film[:id], title: film[:title], description: film[:description])
end 
22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone'],
  brunch: {cost: $35, supplies: ['mimosa flutes'],
  antiquing: {cost: $200, supplies: ['list of antique stores'] 
}
```
How would I add 'granola bar' to things you should have when hiking?
activities[:hiking][:supplies] << 'granola bar'

23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
Encapsulation, Data abstraction, polymorphism, inheritance

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel comfortable with the content presented this week