# Characters

Before we get into biological data, we first need to be able to give the computer knowledge of what an alphabet, or even a character is. Computers can only understand numbers, so how do we tell it we want alphabet characters? One way to do that is to choose a number for each character in some systematic way. One method could be instead of ABC we save 123 if we're using the location in the alphabet as our integer. Since we know the alphabet, we can store numbers and still know what the numbers are supposed to say, and convert back and forth between numbers and characters.

Most commonly, this is done with [bytes](https://en.wikipedia.org/wiki/Byte). When your internet company's talking about speeds, megabits are different from megabytes (8 bits to a byte)! Each byte most commonly represents a character like A or T, but instead of A or T, it's a number. Since each number represents a character, we can write a word as a vector of numbers. In our first example of 'ABC', it would just be `vec![1,2,3]`.

In practice, 'A' isn't stored as 1, but as '65' in the [ASCII alphabet](https://en.wikipedia.org/wiki/ASCII) and '41' in [UTF-8](https://en.wikipedia.org/wiki/UTF-8). This is to be useful to users and computers around the world; UTF-8 has a ton of stuff, even [emojis](https://unicode.org/emoji/charts/full-emoji-list.html)!

## References 

I really enjoyed Stanford's [bits and bytes](https://web.stanford.edu/class/cs101/bits-bytes.html) section!

