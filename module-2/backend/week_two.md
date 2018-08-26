## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?

  * ActiveRecord is a way to work with relational databases. It allows you to access columns in tables via methods and also allows for CRUD functionality

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

  * You can call CRUD methods on Team. You have access to them via the controller.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

  * Team.where(id: 4).first.name

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

  * Team.where(id: 4).first.owner

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

  * Not sure if this is supposed to be a one to many or many to many... but if it's a one to many, then it would be a teacher has_many :students and a student belongs_to :teacher. If it's many to many, then it would be teacher has_many :students and student has_many :teachers.

6. Define foreign key, primary key, and schema.

  * A foreign key is the column on a table that links to the ID of another table. For instance, a teacher has many students, so the foreign key would be a teacher_id on the students table. A primary key is the ID for the table. So it would be the ID for students. A schema is the blueprint for making the tables.

7. Describe the relationship between a foreign key on one table and a primary key on another table.

  * A foreign key on one table is the primary key on another. So for instance, on a teachers table each teacher would have an ID, which would be the primary key. When it is linked to the students table, then the teachers table primary key would become a foreign key on the students table.

8. What are the parts of an HTTP response?

  * A status line, header fields, and a message body.

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
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel overwhelmed by the content presented this week
