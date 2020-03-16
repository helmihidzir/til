# Database

1. Rails 6 has introduced inserting bulk record by
using `insert_all`. The example can be seen in this [post](https://blog.saeloun.com/2019/11/26/rails-6-insert-all.html#insert_all-and-insert_all).

2. Rails 6 also introduce `upsert_all` which is can update the existing record or create a new record if the record does not exist in the database. See [this](https://blog.saeloun.com/2019/11/26/rails-6-insert-all.html#upsert_all) example.

3. To combine two object relation use merge method, eg `first_name_relation.merge(last_name_relation)` or or method, eg `first_name_relation.or(last_name_relation)`. 
[Source](https://stackoverflow.com/questions/9540801/combine-two-activerecordrelation-objects)

4. How to join table? [source](https://stackoverflow.com/questions/680141/activerecord-querying-polymorphic-associations/680172#680172)
```
.joins("INNER JOIN forum_topics ON forum_topics.id = comments.commentable_id")
```

5. How to format as hash on pluck query? [source](https://stackoverflow.com/questions/36011306/ruby-on-rails-4-pluck-results-to-hash/36011522#36011522)
```
Person.pluck(:id, :name).map { |p| { id: p[0], name: p[1] } }
```

6. How to filter multiple attribute?
```
Transaction.where.not(purpose: %i[a f])
```