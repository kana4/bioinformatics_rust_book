# Endianness

## What big endian looks like from u64

```
use core::ops::Range;

fn main(){
    let x: u64 = 3;
    let y = x.to_be_bytes();
    println!("{:?}", y);
    
    // prints
} 
```

[playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=74327ba36eba7ac9f7bc45be23968379)