# Check Sequence, Version 2.0

Super sharp readers will see that in the previous section, even though we checked that each element was the same as the first element, our program didn't give us a direct answer to whether or not our sequence was a homopolymer. Let's do that now!

Instead of creating a vector of trues and falses, we're going to have a single boolean that we update every time we check an element. We're going to use a [boolean operator](https://doc.rust-lang.org/reference/types/boolean.html): `&`.

Using 'and' on our booleans, our answer at the end will only return `true` if all our element checks are `true`.

*Note: the `&` is used in Rust is also used to designate references, and this use is much, much more common!*

At the end, we return the boolean and answer our question: is the sequence a homopolymer?

```
fn main(){

    let vector = b"AAAAA".to_vec();
    
    let first_element = vector[0];
        
    let mut boolean = true;

    // For each element, true or false: is the same as the first element    
    for element in vector {
        boolean = boolean & (first_element == element);
    }

    println!("Is our sequence a homopolymer? {:?}", boolean);

    // prints true
}
```

[playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=e6c7c5bb976fed2f87ecc9edd50206d2)

For the speed junkies, a question arises: couldn't we stop if we found a `false` and save time? Yep! This is called [short circuiting](./Index/Short_Circuit.md), and a lot of Rust functions are built with this in mind!

*Background:*

[boolean operation: &](https://doc.rust-lang.org/reference/types/boolean.html)

*Note:* There's always more than one way to do things, can you think of other ways to test whether a sequence is a homopolymer?
