# Counting Bases
 
Now that we know about iteration, let's use it to count the number of bases in a vector!

```
use std::collections::BTreeMap;

fn main() {
        let mut btree: BTreeMap<u8, u64> = BTreeMap::new();
        let vector = vec![b'A',b'A',b'G',b'G',b'C',b'T'];
        vector.iter().for_each(|u| match u {
                    b'A' => {let count = btree.entry(b'A').or_insert(0); *count +=1},
                    b'G' => {let count = btree.entry(b'G').or_insert(0); *count +=1},
                    b'C' => {let count = btree.entry(b'C').or_insert(0); *count +=1},
                    b'T' => {let count = btree.entry(b'T').or_insert(0); *count +=1},
                    _ => {}
                });
        println!("{:?}", btree);
        
        // A is 65, G is 67, C is 71, T is 84 
        // Prints {65: 2, 67: 1, 71: 2, 84: 1}
}
```

[playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=cb787faa4be4335add1339bf5ea1f40e)