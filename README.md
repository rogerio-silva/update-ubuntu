# Update ubuntu shell script.
## update-ubuntu

This is a simple shell script that updates the Ubuntu system. 

It is a simple script that runs the following commands:
```bash
sudo apt update
sudo apt upgrade
snap refresh
```

Optionally, it can also run the following commands:
```bash
sudo apt dist-upgrade
sudo apt autoremove
sudo apt autoclean
```

The command sintax is:
```bash 
update-ubuntu [options]
```
[options] are:
- -d: run the dist-upgrade command.
- -a: run the autoremove command.
- -c: run the autoclean command.
- -h: show the help message.
- -V: show the verbose version.

To run the script, the user is asked for the 'sudo' password only once, and it is stored for 15 minutes.

## Installation
Clone and access the repository:
```bash
git clone git@github.com:rogerio-silva/update-ubuntu.git
cd update-ubuntu
```

Make the script executable and move it to the bin directory:
```bash
chmod +x update-ubuntu.sh
mv update-ubuntu /usr/local/bin/update-ubuntu
```

Ensure that the script is in the bin directory:
```bash
which update-ubuntu
``` 

Ensure that the `\usr\local\bin` directory is in the PATH:
```bash
echo $PATH
```

If not, add the following line to the `.bashrc` file:
```bash
export PATH=$PATH:/usr/local/bin
```

    