

## What big endian looks like from u64

```
use core::ops::Range;

fn main(){
    let x: u64 = 3;
    let y = x.to_be_bytes();
    println!("{:?}", y);
    
    // 
} 
```

[playground]()