# Iteration

While there are loops (no pun intended) in all languages, Rust has many other powerful methods that make our life so much easier, but may also be a little confusing at first.

Instead of writing a `for` loop every time we want to do something per element, we can use a dot notation version, or an `iterator`. 

```
// Rust

fn main(){
    let vector = vec![1,2,3,4];
    let sum = vector.iter().sum::<u64>();
    println!("{}", sum);
}
```

[playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=bcc6dac13b035b705ca17ee8fdd9fe2e)

This looks super confusing at first, but if we break it down into parts it gets a lot easier.

First we make a vector within our `main` function.

Next, we make a variable `sum` that holds our sum.

Now here's the magic. We know we want to do something for each element of the vector. We could write out to the computer `for each element add to the variable sum`. This is closer to the English version of what we want the computer to do, but we don't need to do everything manually!

We can 'iterate' through each element with the `iter()` functionality. In regular english, the same as "Cut the apple" would be translated as `apple.cut()`, we can say "iterate through each element in the vector" with `vector.iter()`. 

Finally, keeping with our translation, we can say "iterate through the vector and give me the sum" with `vector.iter().sum()`. Super cool, right?

The last part of our code is one of the coolest parts of Rust: the [Turbofish](https://turbo.fish) (yes, that's it's actual name). Remember that if we just summed directly, if the sum was bigger than 256, we would get an `integer overflow` ([section 5_3](../Chapter_5/5_3_Integer_Overflow.md)). We fixed this by making `sum` able to hold bigger numbers (an unsigned 64-bit integer vs 8-bit) With turbofish, we can say "Give me back an unsigned 64-bit integer at the end" with `::<u64>`. Turbofish goes between the name of the function and the parenthesis, so `sum()` would be `sum::<>()`.

Our final English-Rust translations would be:
"Iterate through the vector and sum the elements, and hey, turbofish, don't forget to give me back a u64 please"
`vector.iter().sum::<u64>()`. 

Thanks turbofish!