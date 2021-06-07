# Ready Set Go

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
    println!("{:?}", thing);
}
```
[playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=a4a47924ba912573476de3d42841c2b9)

We also have to change directory to the home folder and type `cargo build bioinfo`, in addition to also running the program with `./target/debug/bioinfo`. What does all of this mean? Don't worry, we'll break it down in the next section.

Why is it so much longer in Rust? Well there are a few things here that we're doing.