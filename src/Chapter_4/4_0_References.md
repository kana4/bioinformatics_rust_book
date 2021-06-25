# References


*!Difficult Section!*

References are one way to make code super efficient. The general idea is that we have some data and we want to reuse the data. In Python or R, we just have the data in a variable and that variable is copied over and over again whenever we want to use it. In most cases, we could have just made and stored the data once, and just referred to it other times.

In a more concrete example, Rust makes a book (our data), stores it on a shelf, and whenever someone wants some information from the book, we  let them know where the book is on the shelf rather than making a copy of the whole book. Making copies of a book in the real world is expensive; the same holds true in computation. On the other hand, our new method not only saves us the time of copying a whole book, but means we don't have to walk to the shelf ourselves, and lets us direct a revolving door of people that want books.

References are a new concept comparing to Python and R, let's see what it would look like in a code block

