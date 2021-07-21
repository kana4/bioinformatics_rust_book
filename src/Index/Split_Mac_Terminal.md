# Split-View Custom Mac Terminal

Prior to this, I used to have a ton of terminals open all the time and it started to be a hassle. Multiplying the usefulness of our terminal window is as easy as typing a few commands!

You'll need [homebrew](https://brew.sh) if you don't have it already. Simply copy/paste `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"` into a terminal will do the trick. After complete, use homebrew to install the program tmux by typing `brew install tmux` into the terminal. Start tmux in the terminal by typing `tmux` in the terminal. We've started a new tmux session.

Use the tmux shortcuts to create a split screen. By default, the shortcut to talk to tmux is `(cntrl + b)` together. Clicking these, letting go and clicking the next key will give us what we want. Clicking too slowly between `cntrl+b` and our other target key will not give us the desired outcome.

Get a split terminal either with `(control+b)` *then* `(shift + ')` or `(control+b)` *then* `(shift + 5)`. Navigate between the terminals with `(control+b)` *then* `(arrow_key)`.

And *voila*! We have a split terminal and can navigate between them.

Some useful shortcuts:

`(control+c)` to cancel whatever the terminal is doing. `(control+a)` and `(control+e)` to skip to beginning and end of a line. Of course on mac, can't go without `(command+c)` and `(command+v)`: copy and paste. `(control+u)` clears a line, or we can just clear everything in the terminal by typing the command `clear`.


Bonus: I <3 custom terminals!

Open a terminal and go to Terminal>preferences>profiles to choose your profile or create a custom one. Currently I like the 'novel' template and cyberpunk colors!

![Custom Terminal]()