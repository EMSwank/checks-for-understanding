## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
ActiveRecord is Rails' ORM. It abstracts away many of the database queries and allows you to call items from the db in a simple way, using objects.

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
.find, .group, .new, .create, .save

We get these methods from inheriting from the ActiveRecord::Base class.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
team = Team.find(4)
team.name

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
team = Team.find(4)
team.owner.name

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
teacher has_many students
students belong_to teacher

create_table "students", force: :cascade do |t|
    t.string "name"
    t.integer "teacher_id"
    t.datetime "created_at", null: false
    t.datetime "updated_at", null: false
  end

create_table "Teacher", force: :cascade do |t|
    t.string "name"
    t.string "school"
    t.datetime "created_at", null: false
    t.datetime "updated_at", null: false
  end

6. Define foreign key, primary key, and schema.
foreign key = the column in a table that represents the primary key to another table in the database.
primary key = usually the incremented id of a row in a table that represents the unique id of information in a row.
schema = the layout/design of a table

7. Describe the relationship between a foreign key on one table and a primary key on another table.
the foreign key on one table is the reference/primary key for another table.

8. What are the parts of an HTTP response?
status code, headers, body.

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?

### Self Assessment:
Choose One:
* I was able to answer all questions independently.

Choose One:
* I feel comfortable with the content presented this week
