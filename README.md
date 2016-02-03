#### [⇐ Previous](8_surge.md) | [Next ⇒](1_terminal.md)

## Mac OS X for Web Development

This guide will help you setup a web development environment on [Mac OS X 10.11 El Capitan](https://www.apple.com/osx/) and above. By the end, your computer will be configured with the same state-of-the-art tools used by professional web developers. While this guide is mostly compatible with older versions of Mac OS X, follow along as best you can while Googling any problems that arise.

By the end of this guide, your development machine should have the following software installed and configured.

1. [Terminal](1_terminal.md)
1. [Homebrew](2_homebrew.md)
1. [Chrome](3_chrome.md)
1. [Fish](4_fish.md)
1. [Atom](5_atom.md)
1. [Git](6_git.md)
1. [Node](7_node.md)
1. [Surge](8_surge.md)

After you've finished setting up your development environment, you'll be able to complete the following tasks.

1. Create a tiny web page with a text editor
1. Test the web page in a browser
1. Commit the web page to a repository
1. Deploy the web page to a production environment

Additionally, this guide assumes your computer is up to the task of coding.

- Is virus and malware free
- Uses the latest, stable, updated version of its operating system
- Has a functioning screen, keyboard, and trackpad
- Has plenty of free hard drive space and memory
- Can reliably connect to wireless networks

### What's an environment and why is it important?

In software, an **environment** is the place where an application is executed. An application's environment includes things like an operating system and a runtime system. Although web applications are often executed on many different environments, each with their own purpose, two environments are essential—production and development.

A **production environment** is a server, or collection of servers, that live somewhere on the Internet and is responsible for serving the web application to the public. When you visit https://duckduckgo.com/ in the browser, for example, you're making a request to a web application's production environment. Production environments are carefully configured and designed to process user requests as quickly as possible.

A **development environment** is a machine, like your laptop, that's used to create, test, commit, and deploy code to the production environment. For consistency, it's important that a development environment use the same technologies as its production counterpart. However, unlike production, a development environment is all about increasing developer productivity. As you can imagine, being able to create a development environment is a crucial skill for every developer.

### How do you create a development environment?

There are four essential tasks that web developers do on a daily basis.

1. Create code as efficiently as possible
1. Test code to ensure it works as expected
1. Commit code to a repository once it's correct
1. Deploy code to a production environment

In an ideal world, developers would learn and use a single, monolithic tool to accomplish all these tasks. In practice, this ideal turns out to be problematic for developers. Picture a scenario where a significantly better way of creating code is discovered that would dramatically improve your productivity. With a monolithic tool, you're at the mercy of the tool's creators to release a new version that incorporates the new and improved technique. In some cases, that can take a very long time if it ever happens at all.

That's why many developers prefer a development environment composed of multiple specialized tools rather than one monolithic tool. This approach is called the **Unix philosophy** and it emphasizes using simple, short, clear, modular, and extensible tools that can be easily maintained and repurposed by developers other than its creators. Though each tool has it's own learning curve, any one of them is easily replaceable when the need arises.

The following guide will help you install and configure a development environment so you can complete the essential tasks of a web developer using tools that adhere to the Unix philosophy. Let's get started.

#### [⇐ Previous](8_surge.md) | [Next ⇒](1_terminal.md)
