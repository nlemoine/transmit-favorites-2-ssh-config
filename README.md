# Transmit favorites to SSH config

This little tool is born because I was bored to keep both my SSH config file and Transmit favorites in sync, filling twice the same informations over and over. 

This script converts all your [Transmit](https://panic.com/transmit/) SFTP favorites into an SSH config file. 

## Usage

Download the script, give it execution rights and execute. 

```
curl -O https://raw.githubusercontent.com/nlemoine/transmit-favorites-2-ssh-config/master/transmit-to-sshconfig.py
chmod +x transmit-to-sshconfig.py
./transmit-to-sshconfig.py
```

**Warning! This will overwrite your existing SSH config file.**

## Notes

Only SFTP favorites are added to the SSH config file. 

HostNames are slugified and formatted to play nice with the excellent [Shuttle](http://fitztrev.github.io/shuttle/) app. 

In Transmit, let's say you have:

- Company folder
	- Server 1
	- Server 2
- Personal folder
	- Server 1
	- Server 2

These favorites will be converted to these HostNames:

- company-folder/server-1
- company-folder/server-2
- personal-folder/server-1
- personal-folder/server-2

And will appear as shown above in [Shuttle](http://fitztrev.github.io/shuttle/): 

![Transmit SFTP favorites SSH config](http://benkey.free.fr/transmit-to-sshconfig.png)
