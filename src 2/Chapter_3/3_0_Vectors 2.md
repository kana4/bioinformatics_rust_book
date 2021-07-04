# Vectors

We made a string in the prior section, so let's make it's simpler cousin, the vector!

```
fn main(){
    let thing_of_things = vec![1,2,3,4];
}
```

What *is* a vector exactly? A [vector](https://doc.rust-lang.org/rust-by-example/std/vec.html) in Rust is a sequence of things, in our case the numbers 1,2,3,4 one after the other. This is also referred to as a [composite](https://en.wikipedia.org/wiki/Composite_data_type) type because a vector is made of multiple smaller things. We could also make the vector with the following:

```
fn main(){
    let thing1 = 1;
    let thing2 = 2;
    let thing3 = 3;
    let thing4 = 4;

    let thing_of_things = vec![thing1,thing2,thing3,thing4];
}
```