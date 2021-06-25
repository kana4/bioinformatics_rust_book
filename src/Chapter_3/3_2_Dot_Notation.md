# Dot Notation

In Rust and a few other programming languages, we can use [dot notation](https://en.wikipedia.org/wiki/Property_(programming)#Dot_notation).
Dot notation is used when we have a thing and we want to do something with it. In pseudo programming English if I wanted to say: 

"cut apple"

With dot notation it would look something like: 

`apple.cut();`

where we have an apple and we want to cut it. Let's use dot notation with a vector!

```
fn main(){
    
    // Make a vector holding the numbers 1,2,3,4

    let vector = vec![1,2,3,4];

    // Use dot notation with len(), a function to get the length of a vector

    let length_of_vector = vector.len();

    // Print the value stored in length_of_vector, which is the length of the vector

    println!("{}",length_of_vector)

}
```

[playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=270b25fb22fee3383a695eff2bb33e3f)

Congrats! We've not only used our first dot notation, our first function! It doesn't seem like it now, but `len()` is a workhorse for Rust programmers of all levels.

![Margaret Hamilton](../img/Margaret_Hamilton.jpg)

*[Margaret Hamilton](https://en.wikipedia.org/wiki/Margaret_Hamilton_(software_engineer)) and software for Apollo. Thanks to early researchers, the world runs on computers! Credits: Wikipedia*