# Print Numbers

Let's print something!

```
fn main(){
    println!("42")
}
```
[playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=85ae37adbe96892255eab588c99912fe)

Well that was pretty easy, we didn't even need the semicolon because we end the main function after printing. Now instead of printing directly, let's try printing something in a variable.

```
fn main(){
    // Make a variable x that holds 1
    let x = 1;

    println!("{}", x)

}
```

Now that we have a variable, `println!` takes two parts, the first is formatting the print, while the second part is the variable to print. the quotes surround everything that will be printed, in our case, `{}` which is always the input variable. So we have stated to print only the variable. We probably want to other things than just deal with numbers though, so let's try to 
