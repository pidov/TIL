+++
date = "2016-11-06T00:25:46+02:00"
title = "Document reference"
weight = 5
+++

#### How to create a reference to another document and populate it with data

First create the proper schema and define the reference.
The value of `ref` is the name of the **model** that you're going to refer to.

```js
var personSchema = new Schema({
  name: String,
  books: [{
    type: Schema.Types.ObjectId,
    ref: 'Book'
  }]
});

var bookSchema = new Schema({
  title: String
});

var Person = mongoose.model('Person', personSchema);
var Book = mongoose.model('Book', bookSchema);
```

Creating a person with favorite book reference.

```js
var whiteFang = new Book({
  title: "White Fang"
});

whiteFang.save(function(err, book) {
  // Handle errors and save the id for reference. Let's assume that the id is "asd98123jg0aasdlfk9"
});

var john = new Person({
  name: "John",
  books: [
    "asd98123jg0aasdlfk9" // Id of the book that we want. Must be a valid ObjectId format
  ]
});

john.save();
```

Populating the books array when requesting john:

```js
Person.findOne({name: "John"})
	.populate('books')
	.exec(function(err, person) {
	  if (err) return handleError(err);
	  console.log(person.books) // prints [{"_id": "asd98123jg0aasdlfk9", "title": "White Fang"}];
	})

```
