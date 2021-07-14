# Comparing Printing Strings


In [interpreted](https://en.wikipedia.org/wiki/Interpreter_(computing)) languages, doing things is really short and succinct. Let's go with a classic: printing "Hello World!".
In Python: 

`thing = "Hello World!"`

`print(thing)`

In R:

`thing = "Hello World!"`

`print(thing)`

And in Rust:

```
fn main(){

    let thing="Hello World!";

    println!("{}", thing);
    
}
```

[playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=b7a9925991302bdd3802fa2a25c89d0e)

Why is it so much longer in Rust? With great power comes having to be specific! Let's break it down based on what we learned so far.

We're building a binary, which is why we have the main function, `fn main(){}`. 

Inside the main function, we create a variable `thing` that stores `"Hello World!"` We put the `thing` variable into `println!`, where `"{}"` is just our variable, and the second input is the actual variable to be printed. We could also print something more fun like:

`Our variable contains: Hello World!` 

by typing:

`println!("Our variable contains: {}", thing);`
