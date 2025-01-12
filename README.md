# Copy-From-File Script

A simple script to copy content from a file, specifying a starting and an ending line.



## Requirements

1. Root privileges.
2. ```sed``` and ```xclip``` (and git if you want to clone the repo).

	The ```sed``` package is commonly pre-installed in the Linux distros.

	But ```xclip``` is not a package included by default.

	
#### Install ```sed``` and ```xclip```:
	
In Debian-based:

```
sudo apt install sed xclip
```	

With pacman (arch-based):

```
sudo pacman -S sed xclip
```

For Fedora:
	
```
sudo dnf install sed xclip
```


Now, if you have ```sed``` and ```xclip``` you can install the script.



## Installation

Clone the repo and set up the script:


```
git clone https://github.com/FabrizioJordan/copyFromFile.git && cd copyFromFile
```


```
chmod +x copyFromFile && cp copyFromFile /usr/local/bin
```
	


But if you want a shorter command, you can create a alias like ```cpff``` or ```cpFromFile```.

Or you can run this command:


```
sudo cp copyFromFile /usr/local/bin/cpff
```


## Usage


### How this script works?

Its easy. You only need to pass three arguments.

1. The starting line.

2. The ending line.

3. The file name.


### Examples of use

This examples shows how this script can be used easilly:


This example copies the content from the line 10 to line 30 in ```file.txt``` file.

```
copyFromFile 10 30 file.txt
```

If you created an alias, you can use it in the same way:

```
cpff 10 30 file.txt
```
## Uninstallation

During installation, the script is copied to /usr/local/bin. If you wish to uninstall it, follow these steps:

To remove the script:

```
find /home/ -type f -name "copyFromFile" -exec rm {} \; && sudo find /usr/ -type f -name "copyFromFile" -exec rm {} \;
```

If you renamed the script during installation (e.g., to cpff):

```
find /home/ -type f -name "cpff" -exec rm {} \; && sudo find /usr/ -type f -name "cpff" -exec rm {} \;
```
