# Docker-Atom Tutorial
How to use Atom and Docker for Containerised fun.

### Why Atom?
Atom is one of the best text editors out there. It's cross-platform, modern, approachable, yet hackable. Also, Atom comes with a very large number of packages to customise your editor exactly as you want it, all installable from the GUI.

### Why Docker?
Docker is the world’s leading software container platform. Download a container with your favourite software preinstalled and start coding in seconds.

### Why Atom and Docker?
There's a package in Docker for pretty much everything, including an in-window terminal. This is beyond useful when creating Docker containers.

## Show me.
Alright, take it easy. I'll need something from you first ... Go to these two links and download + install both Docker and Atom:

Docker: https://docs.docker.com/engine/installation/
Atom: https://atom.io

### Atom + platformio-ide-terminal package
The most important Atom package to install is platformio-ide-terminal. It'll give you a terminal in your editor. Install it first by going to Atom's Preferences, select Install +, and search for 'platformio'. Here's a screenshot:

![alt text](https://github.com/dformoso/docker-atom-tutorial/blob/master/platformio.png)

## In-window Terminal
After you've installed the platformio-ide-terminal package, you'll now have a '+' button at the bottom-left corner of your screen. Click on it to open a terminal window.

The magic starts with a very simple shortcut. Command+Enter on the Mac. I'll send the current line (or selection) from the text editor and run it in the terminal. This is great for scriptingless scriting.

It's simple, but fucking magical. It can save you so much time. Look at this screenshot. All commands were run from the text editor into the terminal by pressing Command+Enter three times.

![alt text](https://github.com/dformoso/docker-atom-tutorial/blob/master/atom.png)

Let's try running some Docker commands from out text editor by pressing Command+Enter. I'll leave you with one more screenshot, before moving to simply posting the commands here. You can do the copy/pasting.

![alt text](https://github.com/dformoso/docker-atom-tutorial/blob/master/dockercom.png)

## Docker Commands
There are many Docker commands available, so I'm going to focus only on the minimum to get you going on simple environments. If you want all the commands available, go here: https://docs.docker.com/engine/reference/commandline/docker/#child-commands

### Environment Info
Let's start with a few easy commands. 
The following will print your Docker Version, the Images available (might not have any yet), and the Containers running (might not have any yet).

```shell
# Print Docker Version
docker --version
# Print Docker Images (To be used to create Containers)
docker images
# Print Docker Containers
docker ps -a
# List Docker Networks
docker network ls
```
### Downloading your first Docker instance
There are hundreds of Docker instances ready to be downloaded with thousands of built in apps. A great place to look for available images is Docker Hub https://hub.docker.com, and also here in Github, there's loads on Github.

To download and run your docker instance, you'll need to run a 'docker run' command. When you run the command, Docker will go and download the image for you. The image might have for following components:

- OS (The whole point of Docker is that it can work without installing an OS, but on the Mac it does download the OS)
- Application (NGINX, MySQL, any many, many, many others)
- Additional OS or App Config.

A complete environment? Yes. Sounds to good to be true right? It does. Let's pick an application and test it out: Nginx.

Nginx (pronounced "engine-x") is an open source reverse proxy server for HTTP, HTTPS, SMTP, POP3, and IMAP protocols, as well as a load balancer, HTTP cache, and a web server (origin server). It's a great choice because it's a web server that immediately gives us a Web front-end to go to verify it all installed correctly.

To install NGINX on Debian, and get it ready for use, we could type the following command:

```shell
docker run -itd \
    --restart always \
    --name my-nginx \
    --hostname splunk_hf_ds \
    --volume "/tmp/:/tmp/" \
    -p 8080:80 \
  nginx:latest
```

Now go to http://localhost:8080 and you should see the Nginx Welcome screen. 
Yeah, that just happened.

### Accessing your instance
How can we get onto our Docker instance shell?

[TO BE CONTINUED]
