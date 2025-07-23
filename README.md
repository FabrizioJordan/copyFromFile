# Copy-From-File Script

A simple script to copy content from a file, specifying a starting and an ending line.



## Requirements

1. Root privileges.
2. ```sed``` and ```xclip``` (and ```git``` if you want to clone the repo).

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
chmod +x copyFromFile && sudo cp copyFromFile /usr/local/bin
```
	

But if you want a shorter command, you can create a alias like ```cpff``` or ```cpFromFile```.

Or you can run this command (to create a Symlink):


```
sudo ln -s /usr/local/bin/copyFromFile /usr/local/bin/cpff
```


## How to update

Update is so easy

Now you have two options

Using an argument with the command ->
Like this:
```
copyFromFile --update
```

From the terminal ->
Only run this command:

```
git clone https://github.com/FabrizioJordan/copyFromFile.git && cd copyFromFile && sudo cp copyFromFile /usr/local/bin/copyFromFile && cd .. && rm -f copyFromFile
```


## Usage


### How this script works?

Its easy. You only need to pass three arguments.

1. The starting line.

2. The ending line.

3. The file name.

But you have two arguments:

1. `-a | --all`
    
	With this argument only pass the file.

2. `-o | --one-line`
    
	This argument needs the line to copy and the file.


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


The next example copies all of the content from the ```file.txt``` file.

```
copyFromFile --all file.txt
```


Finally, the `--one-line` argument, this argument copies only one line from the file and is easy to use.
```
copyFromFile --one-line [Line] [File]
```

Example:

```
copyFromFile --one-line 5 file.txt
```

### All arguments

`-h | --help`: Shows the help menu

`-u | --update`: Updates the program

`-v | --version`: Shows the actual version of the program

`-a | --all`: Copies all of the content from the file

`-o | --one-line`: Copies only one line from the file

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
