# Copy-From-File Script

A script to copy content from a file.
The script copy from the starting line to the ending line.


### How this script works?

Its easy. You only need to pass three arguments.

The first argument is the line start.

The second argement is the line end.

And the third argument is the file.


## Requirements

1. Be root.
2. sed and xclip (and git).

	The sed package is normal in the Linux distros.

	But xclip is not a package installed normally by default.
	
### Install sed and xclip:
	
In Debian-based:

```
sudo apt install sed xclip
```	

With pacman (arch-based):

```
sudo pacman -S sed xclip
```

In Fedora:
	
```
sudo dnf install sed xclip
```


Now, if you have sed and xclip you can install this script.


## Installation

```
git clone https://github.com/FabrizioJordan/copyFromFile.git && cd copyFromFile
```

```
chmod +x copyFromFile && cp copyFromFile /usr/local/bin
```
	
