# For Loops

We now know that vectors are made of smaller pieces of data; what if we wanted to do something for each part (element) of our vector?

Each language has multiple ways to do something for each element of our vector. In any language, we could write a `for` or a `while` loop:

```
# Python

vector = [1,2,3,4]
for element in vector:
    print(element)

```

```
# R

vector = c(1,2,3,4)
for (element in 1:length(vector)) {
    print(element)
}

```


```
// Rust

fn main(){
    let vector = vec![1,2,3,4];
    for element in vector {
        println!("{}", element);
    }
}

```

[playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=5eac305bb88b46f33e9ba4d264f3d349)
