### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions

1.  How do we make flash messages display on a page?
    It's for UX, so the user sees a validation that whatever action the wanted to do actually happened.
2.  Where is cart information/temporary information usually stored?
    The session
3.  What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
    Anything we add to the database will increase the amount of items in the database and take up extra space. But, space is cheap, and sometimes you might want the user to be able log in from multiple devices and see their cart, and having cart info in the db will allow a user to log in from any device and still see their cart/wish list, etc...
4.  What is the purpose of the asset pipeline?
    To reduce the amount of time it takes to load a site.
5.  Why do we precompile our assets?
    So that we can send them all in one shot instead of everytime the page is accessed, and the browser can cache them until they see a new asset pipeline with a new fingerprint.
6.  What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %>
links to the stylesheet for the style of the link

<%= javascript_include_tag "application" %>
links to the java script for the tag

<%= image_tag "rails.png" %>
links to that image asset
```

7.  What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?

The readme should give basic information about what the project does, what gems and ruby/rails versions the project uses, the purpose of the project, how to use it, how to set it up, etc. Making sure that the readme is up-to-date is important because if anything has changed, the person using the code will be confused and stop using your app/gem/project, etc..

8.  What are the top four accessibility issues that we as developers should be aware of?
    Visual, Motor, Auditory, Cognitive, (and 5 seizure for epileptics?--that might be a subset of visual, but when I think of visual, I think of people who are visually impaired, like color blindness and blindness, rather than flishing screens causing a seizure.)
9.  `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
    It's a callback. We'd likely find before_save, if you find you're going to use callbacks, in the create method.

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```

scope :user, module: :user, as: :user do
resources :active
end

11. What is the difference between a scope and a class method?
    A scope changes the routes, and a class method is

### Review Questions:

12. Given the following hash:

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

12a. How would you add item with id of 48 with a quantity of 4?  
 cart["48"] = 4
12b. How would you increase the quantity of item 29?  
 cart[29] += 1
12c. How would you find out how many items your user is thinking about purchasing?  
 cart.values.sum

13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
    It has to do with having multiple model associations in one association. I'm fuzzy about how it relates to duck-typing.

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
    string.delete('( ').gsub!(/[()-]/, ".")

### Self Assessment:

Choose One:

- I was able to answer most questions independently, but utilized outside resources for a few

Choose One:

- I feel comfortable with the content presented this week
