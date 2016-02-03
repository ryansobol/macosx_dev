#### [⇐ Previous](7_node.md) | [README ⇒](README.md)

## Install Surge

Now, you'll deploy a tiny web page with [Surge](https://nodejs.org/), a static web publishing platform for front-end developers. To deploy to Surge, you'll use a command line program that's installed via [npm](https://www.npmjs.com/), a package manager for JavaScript software that comes with Node.

To get started, run the following command.

`npm install -g surge`

Once it finishes, run the following command.

`surge -V`

**TIP:** Notice the flag uses a capital `V`.

And you'll see something like this.

![](https://i.imgur.com/vRRoJau.png)


### Start a new project

If you don't have one, make a `Projects` directory to hold all of your upcoming projects.

```
mkdir ~/Projects
```

Then change into the directory.

```
cd ~/Projects
```

Now make a `GITHUB-USERNAME.surge.sh` project directory replacing `GITHUB-USERNAME` with your actual GitHub username.

```
mkdir wcrusher.surge.sh
```

And change into the directory.

```
cd wcrusher.surge.sh
```

You should see something like this.

![](https://i.imgur.com/PDDFaMu.png)

**TIP:** The full name of your working directory is `~/Projects/wcrusher.surge.sh`. To save prompt space, Fish abbreviates it. This is especially handy for **deeply nested** directories.

Next, initialize a new Git repository in this directory.

```
git init
```

And you should see something like this.

![](https://i.imgur.com/p6Xw9eq.png)

As the message suggests, an empty Git repository was initialized in your working directory. Notice the prompt changed too. You'll see this fancy prompt whenever your current working directory contains a Git repository.

Here's a quick break down of what you're seeing.

| Component                | Description                                   |
|--------------------------|-----------------------------------------------|
| `~/P/wcrusher.surge.sh`  | Abbreviated name of your working directory    |
| `master`                 | Name of your repository's current branch      |
| `✔`                      | Prompt symbol indicating a clean staging area |

Anything typed will appear after the green `✔` prompt symbol.


### Create a tiny web page

Now that the project's directory contains a Git repository, let's create a tiny web page.

To get started, run the following command.

```
touch index.html
```

Noticed a red `✖` has replaced your prompt symbol. It indicates your staging area is dirty. :worried:

![](https://i.imgur.com/jdcHS8p.png)

To find out why, open the project directory in Atom.

```
atom .
```

**TIP:** The period `.` represents the current working directory.

It looks like there's a new, empty `index.html` file inside our project directory. As you can see, a Git repository's staging area becomes dirty whenever a new file is created.

![](https://i.imgur.com/5wqLRFE.png)

Go ahead and type the following HTML code into the `index.html` file and save it.

```html
<h1>Hello world</h1>
```

It should look like this when you're finished.

![](https://i.imgur.com/F26QSWr.png)


### Test your tiny web page

To test your tiny web page, you'll need to open it with your browser. An easy way to open a web page from the Terminal is to run the following command.

`open index.html`

And your default browser should open the file.

![](https://i.imgur.com/8XUgHOh.png)


### Commit your tiny web page

With your tiny web page working as expected, it's ready to be committed into your Git repository.

First, add the `index.html` file to your repository's staging area.

```
git add index.html
```

And then commit the changes, with a message, to your repository.

```
git commit -m 'Add a tiny web page'
```

The green `✔` prompt symbol is back, indicating your staging area is clean. Phew! :relieved:

![](https://i.imgur.com/QE3ks9b.png)


### Prepare your tiny web page for deployment

You're almost ready to deploy your tiny web page to Surge. However, Surge will ask you for a desired domain name each time you deploy. To prevent this, you can save your a domain name to a `CNAME` file so you don’t have to type it every time you deploy.

To add a `CNAME` file to the project directory, run the following command.

```
touch CNAME
```

Noticed a red `✖` is back, indicating your staging area is dirty.

Back in Atom, open the `CNAME` file and type in `GITHUB-USERNAME.surge.sh` replacing `GITHUB-USERNAME` with your actual GitHub username. Save the file and it should look something like this.

![](https://i.imgur.com/BRuK4kA.png)

Now, add the `CNAME` file to your repository's staging area.

```
git add CNAME
```

And then commit the changes, with a message, to your repository.

```
git commit -m 'Add a CNAME'
```

The green `✔` prompt symbol is back, indicating your staging area is clean.

![](https://i.imgur.com/AMzOTd3.png)

### Deploy your tiny web page

You're finally ready to deploy your tiny web page to Surge!

To get started, run the following command.

```
surge
```

You'll be asked for three pieces of information.

1. An email address
1. A password
1. A project path

Since you're probably creating a new Surge account, type in your email address and a unique, secure password. Be careful when you type in a password as the characters will **not** show up on the screen for security purposes.

When asked about the project path, just press the `Enter` key to use the current working directory. When you're finished, it should look something like this.

![](https://i.imgur.com/rh2I4gE.png)

Before moving on, **please write down your account credentials**. If you don't currently use a password manager, now is a great time to invest in one. As a professional web developer, you're going to be responsible for hundreds, if not thousands, of passwords throughout your career.

There are many password managers on the market. I use and whole-heartedly recommend [1Password](https://agilebits.com/onepassword) because its user-friendly interface makes it easy to generate and access all my account credentials on all my devices. More importantly, I trust the company behind 1Password to employ the best security practices available. While it's not a free application, there is a 30-day free trial. And if you become a satisfied customer, you can use the `MacPowerUsers` coupon code to take 20% off the price.

After having written down your Surge account credentials somewhere, open your deployed tiny web page in a browser by running the following command.

```
open http://wcrusher.surge.sh
```

**TIP:** Don't forget to use your tiny web page's domain name.

You should see something like this.

![](https://i.imgur.com/3koEnB4.png)

Bravo! :tada:


### Congratulations!

You've successfully setup a web development environment on Mac OS X and have completed these development tasks.

1. Created a tiny web page with a text editor
1. Tested the web page in a browser
1. Committed the web page to a repository
1. Deployed the web page to a production environment

Now that you've finished this guide, it's time to celebrate with a frosty beverage. :beers:


#### [⇐ Previous](7_node.md) | [README ⇒](README.md)
