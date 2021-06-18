# Biological Sequencing Data

In this chapter, we're going to start working with biological data, finally! We're going to focus on genetic sequencing data here because a large portion of bioinformatics is focused on this type of data.

DNA is classically notated as having the four bases ACTG, whereas RNA ACUG. In sequencing data, we also commonly have N, where we're unsure of what base goes there but we think there's something there. 

```
fn main(){
    let dna = b"ACTG".to_vec();
    let rna = b"ACUG".to_vec();
}
```