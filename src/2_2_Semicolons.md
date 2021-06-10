# Semicolons

What's the point of the semicolons? Aren't we just typing a new thing we want to do on a new line anyway? In Python and R, we continue what we're doing by going to a new line.

In Rust, semicolons separate the steps of a function. This means we could just type everything on one line separated by semicolons, even though this would look kind of weird. Going to a new line isn't necessary, but makes it look nicer like in Python and R.

In Rust, the whole binary is run like a single function, thus the main function structure. This means that if we don't have a semicolon, we'll return whatever we get from the non-semicolon line, the main function will end, and so will our program. If we want to return something from a function, we don't need to type `return`, we just leave out a semicolon!

