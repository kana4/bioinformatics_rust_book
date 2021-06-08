# Print

I'll just come out and say it: in other interpreted languages, it's really simple to do things. Let's go with the classic, printing "Hello World!".

Python: 
```
thing = "Hello World!"
print(thing)
```

R:
```
thing = "Hello World!"
print(thing)
```

And comparatively in Rust:
```
fn main(){
    let thing="Hello World!".to_string();
    println!("{}", thing);
}
```
[playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=a4a47924ba912573476de3d42841c2b9)


Why is it so much longer in Rust? With great power comes having to be specific! Let's break it down.

We're building a binary, which is why we have the main function, `fn main(){}`. 

Inside the main function, we create a variable `thing` that stores `"Hello World!"` just like in the other languages. Unlike the other languages though, we have to actually state that the `"Hello World!"` is a [string](https://en.wikipedia.org/wiki/String_(computer_science))! 

The final part of our code prints what we want. We put the `thing` variable into a function to print what's in the variable, where the first input to `println!`, `"{}"` is just our variable, and the second input is the actual variable to be printed. As an example, we could print:

`Our variable contains: Hello World!` 

by typing:

`println!("Our variable contains: {}", thing);`