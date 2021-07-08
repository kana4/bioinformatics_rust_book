# Check Sequence

Calculating the sum of a sequence is pretty cool, but probably isn't very useful to us in a direct sense. Let's do something with a little more direct application: checking if our sequence is a [homopolymer](https://www.merriam-webster.com/dictionary/homopolymer)!

There's a few steps we're going to do here:

<ul> Store the first element of our sequence in a variable to compare to the other elements </ul>
<ul> Create a separate vector where each element is a boolean true/false. Rust gives us a really nice macro (vec![]) to make an empty vector. </ul>
<ul> For each element in our sequence, check if the element is the same as the first element and push the result into our boolean vector. </ul>
<ul> Print our boolean vector to see our results! </ul>

```
fn main(){

    let vector = b"AAAAA".to_vec();
    
    let first_element = vector[0];
        
    let mut boolean_vector: Vec<bool> = vec![];

    // For each element, true or false: is the same as the first element    
    for element in vector {
        boolean_vector.push(first_element == element)
    }

    println!("{:?}", boolean_vector);

}
```

[playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=1bf1cb00cdfce69f3765253711c55c55)

*Note:* There's always more than one way to do things, can you think of other ways to test whether a sequence is a homopolymer?
