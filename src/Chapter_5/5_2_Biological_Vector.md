# Biological Vector

In the previous section, we created a biological sequence and made it into a vector with `to_vec()`. 

We've created a vector of ACTG and that the vector doesn't hold characters, but bytes. Now that the computer has an idea of a biological sequence, we can start working with our biological data just like any other numeric vector! This includes things that we're more familiar with from math, and in this section we'll do something that we can only do once we've made our characters into numbers: find the sum! What's the sum of 'ACTG'? Let's find out!

```
fn main(){
    let dna = b"ACTG".to_vec();
    println!("{}", dna);
}
```

