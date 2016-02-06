#### [⇐ Previous](4_fish.md) | [Next ⇒](6_git.md)

## Install and Configure Atom

Now it's time to install [Atom](https://atom.io/), a hackable text editor for the 21st century.

To get started, [download Atom](https://atom.io/download/mac), unzip the archive file, and drag the app icon into your `/Applications` folder.

Once installed, use Spotlight to launch Atom by pressing the `Command` + `Spacebar` keys at the same time, typing the word "atom" into the search field, and then pressing the `Enter` key.

![](https://i.imgur.com/fuVq4T5.jpg)

Close all the open tabs by pressing the `Command` + `W` keys at the same time.

Next, navigate to the `Atom > Preferences` menu item by pressing the `Command` + `,` keys at the same time.

Under the **Settings** tab, change the following:

| Name                               | Value              |
|------------------------------------|--------------------|
| Font Family                        | Menlo              |
| Font Size                          | 18                 |
| Show Indent Guide                  | :white_check_mark: |
| Soft Wrap                          | :white_check_mark: |
| Soft Wrap At Preferred Line Length | :white_check_mark: |

Under the **Install** tab, install the following:

| Name                           | Type    |
|--------------------------------|---------|
| file-icons                     | Package |
| language-fish-shell            | Package |
| tomorrow-night-eighties-syntax | Theme   |

Under the **Themes** tab, choose the following:

| Name                           | Type         |
|--------------------------------|--------------|
| Tomorrow Night Eighties        | Syntax Theme |

When you're done, close the preferences tab by pressing the `Command` + `W` keys  at the same time.

### Install the Shell Commands

You'll find it insanely useful to open files and directories into Atom from the Terminal.

To get started, select the `Atom > Install Shell Commands` menu item.

To verify Atom is wired up correctly, run the following command.

```
atom ~/.config/fish/config.fish
```

And Fish's startup file will open in Atom like this.

![](https://i.imgur.com/efTSZJR.png)


### Discover the `EDITOR` environment variable

Like most shells, Fish allows you to control the values of **environment variables**, which are a collection of key-value pairs that can affect the way running programs behave. It's common to set environment variables when a new shell starts so they're available throughout the entire duration of the shell's session.

Many command line programs look up specific environment variables and use their values as implicit input. For example, Git uses the `EDITOR` environment variable to open your preferred text editor when you forget to include a commit message. Environment variables like `EDITOR` can be set in a shell's startup file. While Fish's startup file is handy, add the following.

```
# Atom
set -x EDITOR 'atom -w'
```

**TIP:** Environment variables, like `EDITOR`, must be written in all capital letters.

Save the file and you'll see something like this.

![](https://i.imgur.com/0k7KvdD.png)

Now, relaunch the Terminal and verify these settings with the following command.

```
echo $EDITOR
```

**TIP:** When reading the value of an environment variable, it must be prefixed with a dollar sign `$`.

And you'll see something like this.

![](https://i.imgur.com/TAXG4JV.png)


### Discover the `PATH` environment variable

Like most shells, Fish relies on the `PATH` environment variable to specify a list of directories where commands can be found. Fortunately, the `PATH` environment variable's value is automatically set whenever you start a new shell session. :tropical_drink:

To see the value of the `PATH` environment variable, run the following command.

```
echo $PATH
```

**TIP:** When reading the value of an environment variable, it must be prefixed with a dollar sign `$`.

And you'll see something like this.

![](https://i.imgur.com/9oOQq4F.png)

When you type a command that _doesn't_ include a slash `/` character, these `PATH` directories are searched one after another. Once an executable file that matches the command is found, the searching stops and the matched file is executed.

If no matching executable file is found, the shell will display an error like this.

![](https://i.imgur.com/zbktAR4.png)

In addition to the error message, both the command and the prompt's working directory turned red. Fish is communicating two distinct things here.

1. The command you're thinking about executing doesn't exist.
2. The last executed command failed for some reason.

Don't worry, the prompt's working directory will turn blue again once a command is successfully executed.

![](https://i.imgur.com/EtkLPyT.png)

By the way, notice the `/usr/local/bin` directory is listed first. This means it has priority over the other searchable directories. This is important because Homebrew installs commands to the `/usr/local/bin` directory while Apple pre-installs commands to the other searchable directories. In other words, the shell will prefer Homebrew-installed commands over the Apple-installed ones.

Believe it or not, this is a very useful feature because Apple doesn't update its commands very often. In upcoming sections, you'll use Homebrew to install newer versions of pre-installed commands.

When you want to know where a command lives, you can look it up using the `which` command.

```
which echo
```

And you'll see something like this.

![](https://i.imgur.com/5xgj2DQ.png)


#### [⇐ Previous](4_fish.md) | [Next ⇒](6_git.md)
