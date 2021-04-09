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

Copy and run first command

```bash
pkg install wget -y
```

Once done, run the second command to start the installation of server. This command is little long. Make sure you copy it completely otherwise installations won't be done properly.

```bash
wget https://github.com/jtvserver/jtvserver.github.io/releases/download/1.0/install.sh;sh install.sh
````

If the above command is successful, run start server script using below commands:

```bash
cd ~
```

```bash
sh start.sh
```
Till here, your server will start. This activity is one time only. Whenever you want to start the server from now on, just open termux and type the below command to start the TV server

```bash
sh start.sh
```


The server will now prompt for a token, visit https://jtvserver.github.io/, copy the token and paste it in terminal.<br>

The server will now start.
Now go to your mobile's chrome browser and open http://localhost:3500/

## Control panel operations
There a server console will get open. It's time to fill up the details there. Below are the things that you have to do.

### Jio Login
If you are running the server for the first time, probably you need to login using your Jio number and password. In order to generate password, you can click on link mentioned there. <br>
Now use these credentials to login. In case login is successful, you will receive a success message and the status will change to Logged in. <br>
In case your working playlist stopped suddenly and IP information is correct, you can relogin using the same process.


### IP Address
There are 3 states your mobile network can be in.

1. You're connected to Wi-Fi.
1. You have your mobile data on.
1. You have your mobile data and hotspot on.

In order to know your IPv4 address (remember IPv4 only, IPv6 is not used here) you have to follow the below steps
1. Go to your phone's settings.
1. Click on About Phone.
1. In the long list, you will see an option titled "IP address".
1. There you will see the IP address printed. Something like 192.168.*.*
1. Copy this IP address to your clipboard.

Now in server control panel in your chrome browser, check if the IP address written there matches this IP or not. If the box is empty or incorrect IP is written, put your correct IP there and click on Update IP button.<br>

NOTE: You have to update your IP everytime you change your network.

### Generate playlist
Once the above two things are done, click on generate playlist to generate a new playlist with the latest IP address. <br>

NOTE: In case you are changing the network and updating the IP, you have to regenerate the playlist.

### Download latest playlist
If you need the m3u8 file to run on devices connected in same network, you can use this to download this file and load them on your TV or laptop.<br>

NOTE: In case you are changing the network and updating the IP and regenrating the playlist, please use this option to re download the latest updated playlist.

### Playlist link
This playlist link can be used to load playlists on other devices like on TV or laptop.

## Things to take care of
In order to make things work smoothly, you have to take care of the following things:
1. Your phone and your TV must be connected to same wi-fi.
1. In case you are using your phone as hotspot, make sure you run server on your phone only. Or other phone which is using your hotspot.
1. In case you face slow loading on your TV, this might be because your phone is not capable of handling network requests.
1. If you change your network, please perform the following steps:
   1. See your IP in phone's settings.
   1. Update it on server control panel.
   1. Generate playlist again.
   1. Load the playlist again on your TV/Laptop/Mobile.

## Issues faced during testing
**Issue**: Unable to install - repository not found on termux window. <br>
**Solution**: Sometimes termux shows these errors, all you need to do is to reinstall termux and run the commands again.
<br><br>
**Issue**:  Installation is not happening.<br>
**Solution**: Make sure you have copied the second command properly.
<br><br>
**Issue**: Getting ERR_TLS_CERT_ALTNAME_INVALID.<br>
**Solution**: This issue is known and happened while running it on Raspberry Pi. This issue will be fixed soon in next update.

<b>For any other issues faced, make sure you join our telegram group : https://t.me/jiotvserver or search on telegram using @jiotvserver </b>

Thanks for using this.<br>
Stay tuned with all the updates. Join the official telegram channel https://t.me/jiotvsschannel or search using @jiotvsschannel.
