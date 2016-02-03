#### [⇐ Previous](3_chrome.md) | [Next ⇒](5_atom.md)

## Install and Configure Fish

Using Homebrew, you can now install [Fish](https://fishshell.com/), a smart and user-friendly command line shell. Remember, a shell is simply the user interface between you and your computer's operating system.

There are many command line shells availabe to choose from, each with their own strengths. Since it's easy to switch back and forth at any time, I recommend you give Fish a try.

To get started, run the following command.

```
brew install fish
```

Run the following command to let your computer know it's safe to use Fish as your default shell.

```
echo '/usr/local/bin/fish' | sudo tee -a /etc/shells
```

**TIP:** This will require your account password which **will not** appear on the screen as you type.

Finally, run this command to make Fish your default shell.

```
chsh -s /usr/local/bin/fish
```

**TIP:** This will also require your account password which **will not** appear on the screen as you type.

Now, quit the Terminal app by pressing the `Command` + `Q` keys at the same time. Then relaunch your Terminal using Spotlight and you'll see something like this.

![](https://i.imgur.com/h2qvEez.png)

Welcome to Fish! :tropical_fish:


### Improve the prompt

The prompt is the visual cornerstone of any shell, so let's change it to be both functional and glamorous. :nail_care:

To download and install a better prompt, run the following command.

```
curl -fsSL https://git.io/vgqFU | ruby
```

To verify the new prompt is installed correctly, relaunch the Terminal. You'll see something like this.

![](https://imgur.com/kBsLiZK.png)

Here's a quick break down of what you're seeing.

| Component             | Description                            |
| --------------------- | -------------------------------------- |
| `Wed Jan 28 08:53:47` | Date of your last login                |
| `ttys006`             | Name of your last terminal session     |
| `~` (home directory)  | Name of your working directory         |
| `$`                   | Prompt symbol                          |


### Update the auto-completions

Fish's auto-completions enhance the user experience of most command line tools.

To update fish's completions, run the following command.

```
fish_update_completions
```

And you'll see something like this.

![](https://i.imgur.com/NOS48CL.png)

To try out auto-completions, start typing the following command.

```
brew in
```

And press the `Tab` key and you'll see something like this.

![](https://i.imgur.com/NNP06MA.png)

Finish typing the following command and press the `Enter` key.

```
brew info fish
```

And you'll see something like this.

![](https://i.imgur.com/ShGjo1s.png)


### Leverage your history

Fish keeps a record of every command you've ever run. You can use that history to your advantage.

Start by typing the following command one more time.

```
brew in
```

This time you'll see an auto-suggestion based on the most recent matching command.

![](https://i.imgur.com/yrOuJX9.png)

To use the auto-suggestion, press the right arrow ➡ key and hit the `Enter` key.

![](https://i.imgur.com/DbaBTi7.png)

**TIP:** Use the up arrow ⬆ and the down arrow ⬇ keys to cycle through your entire history of commands.


#### [⇐ Previous](3_chrome.md) | [Next ⇒](5_atom.md)
