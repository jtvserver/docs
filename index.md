# J-TV self server

## Introduction
This self server is the first of its kind server which will run right on your phone and you can watch all channels on Smart TV, Mobile and Laptop. It will let you generate all the personal playlists.

## Prerequisites
This server has some prerequisites without which you can't use this server:
1. An android phone. IOS may work but I haven't tested.
1. Jio number with subscription as you need to login.
1. Your phone and your TV or Laptop must be connected to the same wifi. In case you are watching on your phone, then this is not required.
1. Little brain as the process is little complicated. [Come on. You are setting up a server afterall]

## Let's get started
Go to play store and download Termux application.
Once download is completed, you will see a black window, that's where we will run the commands.

Copy and run first command:
```bash
pkg install wget -y
```
Once done, run the second command to start the installation of server:
```wget https://github.com/jtvserver/jtvserver.github.io/releases/download/1.0/install.sh;sh install.sh````

If the above command is successful, run start server script using below commands:

```bash
cd ~
```

```bash
sh start.sh
```

The server will now prompt for a token, visit https://jtvserver.github.io/, copy the token and paste it in terminal.
The server will now start.
Now go to your mobile's chrome browser and open http://localhost:3500/

