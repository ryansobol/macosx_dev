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

Like most shells, Fish relies on the `PATH` environment variable to specify a set of directories where other commands can be found.

To see the value of the `PATH` environment variable, run the following command.

```
echo $PATH
```

**TIP:** When reading the value of an environment variable, it must be prefixed with a dollar sign `$`.

And you'll see something like this.

![](https://i.imgur.com/9oOQq4F.png)

When you type a command that **doesn't** include a slash `/` character, these `PATH` directories are searched one after another. Once a file that matches the command is found, the searching stops and the corresponding file is run.

Notice the `/usr/local/bin` directory is listed before the following directories.

- `/usr/bin`
- `/bin`
- `/usr/sbin`
- `/sbin`

This means the `/usr/local/bin` directory has priority over all later searched directories.

Since Homebrew installs new commands to the `/usr/local/bin` directory, Homebrew-installed commands will be preferred over the pre-installed ones. In upcoming sections, you'll use Homebrew to install additional commands that override the pre-installed commands that come with Mac OS X.


#### [⇐ Previous](4_fish.md) | [Next ⇒](6_git.md)
