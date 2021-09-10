# Short Circuit Logic

A function that ends early on a specific situation is `short circuiting`. This can save a ton of time and speeds up our code!

In a common instance, we're doing something in a loop, and if a specific situation happens, we could stop the loop early. One example could be that we're searching through the word `hello` letter by letter and want to stop when we find an `l`. In pseudocode:

```
for letter in word
    if 'l' return 1
    else return 0
```

In our normal code above, we would return:

`00110`

Our code went through every letter, even if we hit an `l` at the third letter! If we want to write code that stops at the first `l`, we could write something like:

which would return `001`
