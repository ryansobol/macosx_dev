#### [⇐ README](README.md) | [Next ⇒](2_homebrew.md)

## Configure the Terminal

Included in Mac OS X is the **Terminal**—an app that runs a Unix shell.

A **Unix shell** is a command line user interface between you and your computer's operating system. You're probably most familiar with the graphical user interface of an operating system. While that's technically a shell too, most developers think of the textual, command line interface when they hear to word _shell_. Mac OS X blends both the graphical and the command line interfaces beautifully which is why it's so popular among developers.

The first Unix shell was released in 1971. Decades later, developers continue to incorporate command line shells into their workflow because they're interactive and scriptable. In other words, the same commands that control an operating system from an interactive command line can be included in an executable script file. While a **script file** is simply a file that contains a sequence of commands, it's the crux of automating repetitive tasks and increasing developer productivity.

In this guide, you'll download and run script files to speed up the installation and configuration of your development environment.

### Discover the Terminal

Let's get our hands dirty and have some fun. :paw_prints:

First, use Spotlight to launch the Terminal app by pressing the `Command` + `Spacebar` keys at the same time, typing the word "terminal" into the search field, and then pressing the `Enter` key.

![](https://i.imgur.com/XQE36wU.jpg)

Once launched, you'll see something like this.

![](https://i.imgur.com/7d6GeeO.png)

Here's a quick break down of what you're seeing in the Terminal app.

| Component             | Description                            |
| --------------------- | -------------------------------------- |
| `Wed Jan 28 12:06:29` | Date of your last login                |
| `ttys008`             | Name of your last terminal session     |
| `photon`              | Name of your computer                  |
| `~` (home directory)  | Name of your working directory         |
| `ryansobol`           | Name of your user account              |
| `$`                   | Prompt symbol                          |

Go ahead and type `uname` which is a command that will display your operating system's Unix name. Any characters you type will appear after the `$` prompt symbol. After pressing the `Enter` key, you'll see something like this.

![](https://i.imgur.com/eGnT4NZ.png)

**TIP:** The two most common Unix operating systems are Darwin and Linux.

Here's what happened:

1. The shell told the Terminal to display a prompt.
1. The shell asked the Terminal to wait for you to type a command.
1. You then typed the word `uname` which appeared after the prompt.
1. You pressed the `Enter` key which triggered the shell to accept your input.
1. The shell searched for a program called `uname`.
1. Once found, the shell launched the `uname` program and handed it control over the Terminal.
1. While running, the `uname` program told the Terminal to display the word `Darwin`.
1. Once finished, the `uname` program exited and handed control of the Terminal back to the shell.
1. The shell told the Terminal to display another prompt.
1. Once displayed, the shell began waiting for your next command.

This is called a read-evaluate-print loop or **REPL** for short.

### Change the Terminal Profile

The default profile for the Terminal uses small, black text on a white background. Boring! Let's change that.

1. Download the [Tomorrow Night Eighties](https://raw.githubusercontent.com/ryansobol/sea-c17-ruby/master/class1/osx/Tomorrow%20Night%20Eighties.terminal) terminal profile by holding the `Option` key and left-clicking the link.
1. Navigate to the `Downloads` folder.
1. Install the profile by double-clicking the file.
1. You'll see an alert explaining the file "cannot be opened because it is from an unidentified developer". **Don't panic.**
1. Using Spotlight, open the `Security & Privacy` system preferences by pressing the `Command` + `Spacebar` keys at the same time, typing the word "security" into the search field, and then pressing the `Enter` key.
1. Navigate to the `General` tab and then click on the `Open Anyway` button. ![](https://i.imgur.com/lOh3GAH.png)
1. Press the `Command` + `Tab` keys at the same time to switch back to the Terminal app.
1. Navigate to the `Terminal > Preferences` menu item by pressing the `Command` + `,` keys at the same time.
1. In the preferences window, click the `Settings` Pane.
1. On the left side, scroll to the bottom, select the `Tommorrow Night Eighties` profile, and click the `Default` button. ![](https://i.imgur.com/g9l91K0.png)
1. Quit the Terminal app by pressing the `Command` + `Q` keys at the same time.
1. Relaunch the Terminal using Spotlight like before.

Now, every new Terminal window will look like this.

![](https://i.imgur.com/87bHvEF.png)


#### [⇐ README](README.md) | [Next ⇒](2_homebrew.md)
