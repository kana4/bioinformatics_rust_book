# Binary VS Library

When we get a program, we click it, it'll open, and we'll be able to do stuff. We'll have to choose the program based on our operating system.

The program we're downloading is a binary: a bunch of operating system-specific operations amalgamated together so the computer can do the things we want it to in (hopefully) an efficient manner. You may have heard this word before on Windows as the .exe file type ('executable' by the system) or .dmg for Mac or just plain no file extension in Ubuntu or Linux.

![Executable Gif](./img/binary_vs_library.gif)

In Rust, binaries always have a main function, written `fn main(){}`. This main function is the head honcho of all things in our binary. Everything that will actually be done is in the main function, with other functions, definitions, etc. being sourced from everywhere else. We build binaries by typing `cargo build --bin` (more on that in the next section).

The other kind of thing we make in Rust is a library. While we also build a library with `cargo build --lib`, a library does not have a program that we can just run like what we would imagine. This is because a library's purpose is to be a bunch of small, reusable pieces of code that we can use to make an executable, but aren't really useful to our users. As an analogy, a library is like a tool shed and the binary a house that the user lives in.


Side Note: my terminal is one of the options in Mac, if you want to customize yours go here!
