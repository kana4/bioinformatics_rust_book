# Count Compare

We can also count other things, let's compare how many elements are greater, equal, and less than a target number!

```
use std::cmp::Ordering;
use std::collections::BTreeMap;

fn main() {
        let mut btree: BTreeMap<Ordering, u64> = BTreeMap::new();
        let vector = vec![1,2,3,4];
        let target = 3;
        vector.iter().for_each(|u| match u.cmp(&target) {
            Ordering::Less => {let count = btree.entry(Ordering::Less).or_insert(0); *count +=1},
            Ordering::Equal => {let count = btree.entry(Ordering::Equal).or_insert(0); *count +=1},
            Ordering::Greater => {let count = btree.entry(Ordering::Greater).or_insert(0); *count +=1},
            });
        println!("{:?}", btree);
        // prints {Less: 2, Equal: 1, Greater: 1}
}
```

[playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=316586d21b388764eafdca7c117ccf44)