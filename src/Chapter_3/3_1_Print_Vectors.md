# Printing Vectors and Debug Mode

If you look closely, we didn't print the vector just yet, for that we need something called `debug`!

Debug is something new if you're coming from other languages like R or Python, and it's something that we don't really need to know how it works, so we'll just leave it at: *We neeeeeeed it!* At least for vectors.

```
fn main(){
    let thing_of_things = vec![1,2,3,4];
    println!("{:?}",thing_of_things)
}
```

[playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=b94f6fadd0cb4b684b29f22803547f0d)

Can you spot the debug notation? It's the `:?` inside the `{}`! Rust is super smart, if we didn't have the debug and just wrote `println!("{}",thing_of_things)` like in our prior examples, we'd get an error like this:

`the trait std::fmt::Display is not implemented`

But we'd also get this:

`in format strings you may be able to use {:?} (or {:#?} for pretty-print) instead`

The first option is exactly what we needed, which leads us to the golden rule: figure out the output Rust gives us. Rust is pretty smart, it'll probably give us some useful clues (and in this case the exact fix) to what to do if we get an error! It's a safe troubleshooting default if we get an error when printing to try add in the `:?`.