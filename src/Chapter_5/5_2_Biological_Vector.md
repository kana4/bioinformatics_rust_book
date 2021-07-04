# Biological Vector

In the previous section, we created a biological sequence and made it into a vector with `to_vec()`. 

We've created a vector of ACTG and that the vector doesn't hold characters, but bytes. Now that the computer has an idea of a biological sequence, we can start working with our biological data just like any other numeric vector! This includes things that we're more familiar with from math, and in this section we'll do something that we can only do once we've made our characters into numbers: find the sum! What's the sum of 'ACTG'? Let's find out!

```
fn main(){
    let dna = b"ACTG".to_vec();
    let mut sum = 0;
    for base in dna {
        sum += base;
    }
    println!("{}", sum);
}
```

//TODO playground

## Background: 



//TODO link to mutable variable. 

//TODO link to += notation.

//TODO link for loops.

// index 
Mutable variables are variables that can change. Normally in Rust when we write `let` the variable cannot change, `mut` let's the program know that it should expect this variable to change. 

+= is shorthand notation for adding to a variable similar to the following pseudocode example:
```
x += y is the same as:
x = x + y
```

In short, it means set our first variable on the left hand side [lhs]() to itself plus something.


How to make for loops in Rust. Our for loop here takes the vector and for each element (`base`) adds to our variable `sum`.

