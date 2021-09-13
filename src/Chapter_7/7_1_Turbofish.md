# Turbofish

```
fn main(){
    let vector = vec![1,2,3,4];

    let sum = vector.iter().sum::<u64>();

    println!("{}", sum);
}
```

[playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=bcc6dac13b035b705ca17ee8fdd9fe2e)

The last part of our code is one of the coolest parts of Rust: the [Turbofish](https://turbo.fish) (yes, that's it's actual name). Remember that if we just summed directly, if the sum was bigger than 256, we would get an `integer overflow` ([section 5_3](../Chapter_5/5_3_Integer_Overflow.md)). We fixed this by making `sum` able to hold bigger numbers (an unsigned 64-bit integer vs 8-bit) With turbofish, we can say "Give me back an unsigned 64-bit integer at the end" with `::<u64>`. Turbofish goes between the name of the function and the parenthesis, so `sum()` would be `sum::<>()`.

Our final English-Rust translations would be:
"Iterate through the vector and sum the elements, and hey, turbofish, don't forget to give me back a u64 please"
`vector.iter().sum::<u64>()`. 

Thanks [turbofish](https://turbo.fish)!

## ::<> 
### ::<> 
#### ::<> 
##### ::<>

