# Commands

Bioinformaticians use a lot of R, Python, and shell scripting to get what they want done. These tools are really good at working with text and sequencing data, and have been around before Rust was even born! For the command line scripting sections of bioinformatics workflows we can easily use the same code in Rust. In the following sections we'll translate some of the most common operations directly from a script. 

*Warning* *Warning* *Warning*

The command line scripts we write are based on the operating system we're using. Windows Powershell has different commands from the Linux command line, which is different from the Mac terminal! It follows that our Rust program translation will also need to be run on a specific operating system. This is in contrast to all our code up to this point, which can be compiled and run all on mainstream operating systems. In the following examples, we're going to write commands for Linux. Enough with the long-winded explanations, let's write some code!

