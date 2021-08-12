# Counting Bases

    // println!("{:?}", boolean_vector.into_iter().all(|u| u==true));

Now that we know about iteration, let's use it to count the number of bases in a 

```
use std::cmp::Ordering;
use std::collections::BTreeMap;

fn main() {
        let btree: BTreeMap<Ordering, u64> = BTreeMap::new();
        let test = vec![1,2,3,4];
        let target = 3;
        test.iter().for_each(|u| match u.cmp(&target) {
                    Ordering::Less => println!("less"),
                    Ordering::Equal => println!("equal"),
                    Ordering::Greater => println!("greater"),
                })
}

```