#### [⇐ Previous](5_atom.md) | [Next ⇒](7_node.md)

## Install and Configure Git

Using Homebrew, you can also install [Git](https://git-scm.com/), the version control system of choice among choosy developers. :neckbeard:

To get started, run the following command.

```
brew install git
```

Once it finishes, run the following command.

```
git --version
```

And you'll see something like this.

![](https://i.imgur.com/Gwx0LOn.png)

Like artists, programmers sign their work. Let's configure Git to sign your commits with your name and email address.

**WARNING:** Before running the following commands, replace `YOUR FULL NAME` and `YOUR EMAIL ADDRESS` with the name and email from [your GitHub account](https://github.com/settings/profile).

```
git config --global user.name 'YOUR FULL NAME'
git config --global user.email 'YOUR EMAIL ADDRESS'
```

Next, run this command to download and install some awesome Git colors, handy aliases for common Git subcommands, and extra Git configuration that'll make your life easier when connecting to GitHub from the command line.

```
curl -fsSL https://git.io/vgqFH | sh
```

We'll go over these later. For now, relish in your victory of making it this far in the setup guide. :tada:


#### [⇐ Previous](5_atom.md) | [Next ⇒](7_node.md)
