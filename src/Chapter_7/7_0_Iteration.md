# Iteration

While there are loops (no pun intended) in all languages, Rust has many other powerful methods that make our life so much easier, but may also be a little confusing at first.

Instead of writing a `for` loop every time we want to do something per element, we can use a dot notation version, or an `iterator`. 

```
fn main(){

    let vector = vec![1,2,3,4];

    let sum: u64 = vector.iter().sum();

    println!("{}", sum);
}
```

[playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=cfc0e98847143188b295c895ea1b2466)

This looks pretty confusing at first, but if we break it down into parts it gets a lot easier.

First we make a vector within our `main` function.

Next, we make a variable `sum` that holds our sum.

Now here's the magic. We know we want to do something for each element of the vector. We could write out to the computer `for each element add to the variable sum`. This is closer to the English version of what we want the computer to do, but we don't need to do everything manually!

We can 'iterate' through each element with the `iter()` functionality. In regular english, the same as "Cut the apple" would be translated as `apple.cut()`, we can say "iterate through each element in the vector" with `vector.iter()`. 

Keeping with our translation, we can say "iterate through the vector and give me the sum" with `vector.iter().sum()`. 

As we learned in section 5.3, [integer overflow](../Chapter_5_5_3_Integer_Overflow.md) occurs if our sum is over 255, so our final bit of code is to the left of the equal sign ([left hand side](https://en.wikipedia.org/wiki/Sides_of_an_equation), or lhs), indicating to return our `sum` as a `u64`, which has a lot larger max limit. This is translated as `let sum: u64` or specifically, let `sum` be a `u64` and not any other integer type.

Translation done!

