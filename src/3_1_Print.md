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
    let thing=b"Hello World!".to_string()
    Println!("{}", thing);
}
```

We also have to change directory to the home folder and type `cargo build bioinfo`, in addition to also running the program with `./target/debug/bioinfo`. What does all of this mean? Don't worry, we'll break it down in the next section.

Why is it so much longer in Rust? In low-level languages, it was (and sort of still is) actually quite a feat to get to the first step where the computer says those two words back to you. I'm not sure, but this may have played a role in the choice of words.
