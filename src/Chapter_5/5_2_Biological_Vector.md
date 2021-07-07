# Biological Vector

In the previous section, we created a biological sequence and made it into a vector with `to_vec()`. 

We've created a vector of ACTG and that the vector doesn't hold characters, but bytes. Now that the computer has an idea of a biological sequence, we can start working with our biological data just like any other numeric vector! This includes things that we're more familiar with from math, and in this section we'll do something that we can only do once we've made our characters into numbers: find the sum! What's the sum of 'ACTG'? Let's find out!

```
fn main(){

    let dna = b"ACT".to_vec();

    let mut sum = 0;

    for base in dna {
        sum += base;
    }

    println!("{}", sum);

    // Prints 216
}
```

[Playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=343748b7922270bccc2ec0cfa84d245c)

## Links: 

The `mut` keyword: a [mutable](https://doc.rust-lang.org/rust-by-example/scope/borrow/mut.html) variable. 

`+=` notation: [Adding](https://doc.rust-lang.org/book/appendix-02-operators.html) to a variable.

`-=` notation: [Subtracting](https://doc.rust-lang.org/book/appendix-02-operators.html) to a variable.

Definitions from the Rust language appendix:

```
+= Arithmetic addition and assignment, AddAssign

-= Arithmetic subtraction and assignment, SubAssign
```

[Rust Operators](https://doc.rust-lang.org/book/appendix-02-operators.html)

Writing our first [For loop: Rust by Example](https://doc.rust-lang.org/rust-by-example/flow_control/for.html)


