# Database

Rails 6 has introduced inserting bulk record by
using `insert_all`. The example can be seen in this [post](https://blog.saeloun.com/2019/11/26/rails-6-insert-all.html#insert_all-and-insert_all).

Rails 6 also introduce `upsert_all` which is can update the existing record or create a new record if the record does not exist in the database. See [this](https://blog.saeloun.com/2019/11/26/rails-6-insert-all.html#upsert_all) example.

---
To combine two object relation use merge method, eg `first_name_relation.merge(last_name_relation)` or or method, eg `first_name_relation.or(last_name_relation)`. 