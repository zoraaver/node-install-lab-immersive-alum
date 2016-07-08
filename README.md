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

## One-Click Installers (Recommended)

First, let's go to <http://nodejs.org> and download a one-click installer for your Operation System. Choose version 5.1.0. The differences between stable and long-term support (LTS) is that LTS is for enterprises.

Don't choose binaries or source code unless you know what to do with them or your OS is not present (i.e., not Windows or Mac). The installers come with Node Package Manager (npm or NPM) — important tool for managing dependencies. No need to install npm separately, but you might want to downgrade to v2.14.15 because v3.x is slower.

Note: for older Mac OS X machines, you can pick 32-bit versions.

If there's no installer for your OS, you can get source code and compile it yourself (look for the installing from a tar file section in this file). The One-Click installer options will work for most of developers. If you need other installation recipes, proceed with this text. Otherwise, run `npm test` to test the versions. You will see pass or not.

Note: If you need to downgrade or upgrade Node, you can use one-click installer for that version. However, if you do it often enough (maybe you have 2 projects which require different versions) n/nave/nvm is a better option (covered below).


## Checking the Installation

To test your installations, run these commands in your Terminal app (command line `cmd.exe` in Windows):

```bash
node -v
npm -v
```

As of this writing (8 July 2016), you should have Node.js v6.3.0 and npm v3.10.x ("x" will be a number but it seems like it'll change imminently). Alternatively, run the tests for this lessons with `npm test`.


## Installing with HomeBrew

If you already have HomeBrew (`brew`) installed, straightforwardly run:

```
brew install node
```

This command will install the latest brewed versions of both Node.js and npm.

## Multi-version Setup with Nave

If you plan to run multiple versions of Node to be able to quickly switch between them, you should use [nave](https://github.com/isaacs/nave) which is a virtual environment for Node.

Make a folder:

```bash
mkdir ~/.nave
cd ~/.nave
```

Downloading Nave and setting the link to PATH'ed folder:

```
wget http://github.com/isaacs/nave/raw/master/nave.sh
sudo ln -s $PWD/nave.sh /usr/local/bin/nave
```

This is an example of switching to Node version 5.1.0 in a virtual environment with Nave:

```
nave use 5.1.0
```

To use NPM in this particular virtual environment, someone needs to use:

```
curl https://npmjs.org/install.sh | sh
```

After which it's possible to install something via NPM:

```
npm install express
```

And exit virtual environment with:

```
exit
```

More approaches to install Node and NPM in [gist](https://gist.github.com/isaacs/579814).


## Multi-version Setup with NVM

Another options to Nave is NVM — Node Version Manager ([GitHub](https://github.com/creationix/nvm)). You can install NVM with:

```
curl https://raw.github.com/creationix/nvm/master/install.sh | sh
```

or

```
wget -qO- https://raw.github.com/creationix/nvm/master/install.sh | sh
```

And after that, harness NVM's `install` to install version 5.1.0 of Node:

```
nvm install 5.1.0
```

To switch that 5.1 version of node, simply apply the `use` command, e.g.,

```
nvm use 5.1.0
```

## Alternative Multi-Version Systems

Alternatives to Nave and NVM include:

* [neco](https://github.com/kuno/neco)
* [n](https://github.com/visionmedia/n)



<p data-visibility='hidden'>View <a href='https://learn.co/lessons/node-install-lab' title='node-install-lab'>node-install-lab</a> on Learn.co and start learning to code for free.</p>

