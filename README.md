#Installing Node and npm

## Objectives

1. Install Node v5.x and npm 2.x via the website installer
1. Install Node via n, nvm or nave (optional)
1. Install Node and npm with brew (optional, Mac OS X users only)
1. Configure npm so you get the ownership (optional)
1. Check Node and npm installations and the versions

## Introduction

Hopefully you're excited about Node by now. But before we can go any further, we need to install it on our system. 

There are a few ways to install Node and npm. Our recommendation is to use one-click installer. Sometimes you might work on projects which require different versions of Node and/or npm. We'll cover how to switch between them too. In this case use `n`, `nave` or `nvm`. 

For the very advanced developers, there are a few recipes like installing from the source code or taking ownership. If you are total beginner, stick with one-click installer or n/nave/nvm.


## Instructions

1. Install Node with one of the methods listed below
2. Install npm
3. Check that you have the latest versions of Node and npm
4. Install testing dependencies with `npm install`
5. Run tests to check for versions with `npm test`


## Installing with Homebrew

If you already have Homebrew (`brew`) installed, straightforwardly run:

```
brew install node
```

This command will install the latest brewed versions of both Node.js and npm.

## Installing with apt/yum/etc.

Installing Node.js with the package manager of your choice should look essentially like the above installation with Homebrew. Note that on Debian-based systems, you'll need to `sudo apt-get install node.js`, because a `node` package other than Node.js already exists in apt.

## Checking the Installation

To test your installations, run these commands in your Terminal app (command line `cmd.exe` in Windows):

```bash
node -v
npm -v
```

As of this writing (8 July 2016), you should have Node.js v6.3.0 and npm v3.10.x ("x" will be a number but it seems like it'll change imminently). Alternatively, run the tests for this lessons with `npm test`.

## Changing versions

As you work with different Node.js projects, you'll find that you need to change versions from time to time. There are many version managers available for Node.js, such as [nvm](https://github.com/creationix/nvm), or even virtual environment managers like [nave](https://github.com/isaacs/nave).

We prefer to use [n](https://github.com/visionmedia/n). To get started, simply run

```
npm install -g n
```

This installs `n` globally on your system.

With `n` installed, switching to a new version is as simple as running

```
n 6.2.0
```

Where "6.2.0" could be any version that you need. Use `n --help` to explore your options and learn how to use it!

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/node-install-lab' title='node-install-lab'>node-install-lab</a> on Learn.co and start learning to code for free.</p>

