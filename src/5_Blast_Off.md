# Setup

![Introduction Rust Playground](./img/intro_playground.gif)

Side Note: my terminal is one of the options in Mac, if you want to customize yours go here!


Hello world! Well, not quite yet, we need to install prerequisites (but it's not that hard, we promise!). Throughout the book, we'll also give shortcuts and tools that *really* help speed things up.

There are a few things on our *TODO* list and we refer you to the original sources as these will give you better instructions than we can:

[Install and Configure Rust](https://www.rust-lang.org/tools/install)

[Install VSCode](https://www.rust-lang.org/tools/install) 


<ul>First, create a new folder in the place you want to have your work</ul>
<ul>Open VSCode and File>>Open your folder</ul>

Run `Cargo init`

Our workspace should look something like this

// fn n50(numbers: &[usize], nb_bases_total: usize) -> usize {
//     let mut acc = 0;
//     for val in numbers.iter() {
//         acc += *val;
//         if acc > nb_bases_total / 2 {
//             return *val;
//         }
//     }

//     numbers[numbers.len() - 1]
// }