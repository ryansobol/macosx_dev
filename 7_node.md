#### [⇐ Previous](6_git.md) | [Next ⇒](8_surge.md)

## Install Node

Using Homebrew, you can also install [Node](https://nodejs.org/), an open-source, cross-platform runtime system for developing applications in JavaScript. In other words, it runs JavaScript outside the browser.

To get started, run the following command.

```
brew install node
```

Once it finishes, run the following command.

```
node -v
```

And you'll see something like this.

![](https://i.imgur.com/s6yEpP9.png)


### Discover the Node Shell

The interactive **Node shell** provides a read-evaluate-print loop (REPL) for JavaScript programs.

To get started, launch the Node shell by running the following command.

```
node
```

And you'll see something like this.

![](https://i.imgur.com/tSVXigd.png)

After the prompt `>`, you can type a line of JavaScript code and then press the `Enter` key to run it. For example, type and run the following JavaScript program.

```
1 + 2
```

And you'll see something like this.

![](https://i.imgur.com/ZO8fIEw.png)

The Node shell is a great tool for learning and experimenting with JavaScript.

Play around with JavaScript on your own. When you're done, type `.exit` and press the `Enter` key to quit the Node shell.


### Discover the Node Interpreter

Given a JavaScript program stored in a file, the **Node interpreter** reads it, evaluates it, and then quits.

Unlike the Node shell, the Node interpreter is _not_ interactive. In other words, the Node interpreter won't automatically print the result of each line or loop waiting for you to give it more input. It just reads and evaluates a JavaScript program file.

Despite these deficiencies, you'll use the Node interpreter more frequently. Let's try it out.

First, open a new JavaScript program file in Atom.

```
atom ~/Desktop/test.js
```

**TIP:** JavaScript program files end with a `.js` extension.

Then type the following program into the file.

```
1 + 2;
```

Save the file and run the program using the Node interpreter.

```
node ~/Desktop/test.js
```

Weird, nothing happened. Remember, the Node interpreter won't print anything unless told. Jerk! :triumph:

Change the program so it reads like this.

```
console.log(1 + 2);
```

Save the file and re-run the program.

```
node ~/Desktop/test.js
```

And you'll something like this.

![](https://i.imgur.com/13wlgTe.png)

Play around with JavaScript on your own. When you're done, remove the `test.js` file by running the following command.

```
rm ~/Desktop/test.js
```


#### [⇐ Previous](6_git.md) | [Next ⇒](8_surge.md)
