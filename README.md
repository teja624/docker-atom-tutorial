# Docker-Atom Tutorial
How to use Atom and Docker for Containerised fun.

### Why Atom?
Atom is one of the best text editors out there. It's cross-platform, modern, approachable, yet hackable. Also, Atom comes with a very large number of packages to customise your editor exactly as you want it, all installable from the GUI.

### Why Docker?
Docker is the world’s leading software container platform. Download a container with your favourite software preinstalled and start coding in seconds.

### Why Atom and Docker?
There's a package in Docker for pretty much everything, including an in-window terminal. This is beyond useful when creating Docker containers.

## Show me.
Ok, no need to get aggresive. I'll need something from you first ... Go to these two links and download + install both Docker and Atom:

Docker: https://docs.docker.com/engine/installation/
Atom: https://atom.io

### Atom + platformio-ide-terminal package
The most important Atom package to install is platformio-ide-terminal. It'll give you a terminal in your editor. Install it first by going to Atom's Preferences, select Install +, and search for 'platformio'. Here's a screenshot:

![alt text](https://github.com/dformoso/docker-atom-tutorial/blob/master/platformio.png)

## In-window Terminal
After you've installed the platformio-ide-terminal package, you'll now have a '+' button at the bottom-left corner of your screen. Click on it to open a terminal window.

The magic starts with a very simple shortcut. Command+Enter on the Mac. I'll send the current line (or selection) from the text editor and run it in the terminal. This is great for scriptingless scriting.

It's simple, but magical in time-savings. Look at the magic in this screenshot. All commands were run from the text editor into the terminal by pressing Command+Enter three times.

![alt text](https://github.com/dformoso/docker-atom-tutorial/blob/master/atom.png)

Let's try running some Docker commands from out text editor by pressing Command+Enter. I'll leave you with one more screenshot, before moving to simply posting the commands here. You can do the copy/pasting.

![alt text](https://github.com/dformoso/docker-atom-tutorial/blob/master/docker.png)

## Docker Commands
There are many Docker commands available, so I'm going to focus only on the minimum to get you going on simple environments. If you want all the commands available, go here: https://docs.docker.com/engine/reference/commandline/docker/#child-commands

### Environment Info
```shell
# Print Docker Version
docker --version
# Print Docker Images (To be used to create Containers)
docker images
# Print Containers
docker ps -a
```


