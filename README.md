# Share and Enjoy
**ashfile** - Creates a Bash script, makes it executable, and opens it

</br>

## Disclaimer
I am still learning, proceed with a moderate measure of caution.

</br>

## Setup - Create a custom bin directory
The following code creates a hidden directory in your home directory and adds it to the PATH.

_BE WARNED_

Any executables you put in this directory will be accessible anywhere in your machine. Before naming a new executable, take a moment and make sure the name isn't being used by another program. You will also have a `.bashrc` file now, anything you add to this will be run when you log-in, try adding `echo "Hello, Dave. You're looking well today."` to it.

#### Bash
```sh
echo -e "\nBEGIN\n"
cd ~ #go to your home directory
mkdir .my_bin #create hidden bin directory
cd .my_bin #go to new bin directory
export PATH=$PATH:$(pwd) #add bin to PATH for current session
echo "export PATH=\$PATH:$(pwd)" >> ../.bashrc #adds bin to PATH for future sessions
echo \#\!/bin/bash >> my_first_bash_script #create a new bash script
echo "" >> my_first_bash_script #add new line to new bash script
chmod a+x my_first_bash_script #make new bash script executable by all users
if [ -e $(pwd)"/my_first_bash_script" ]; then echo -e "\nSUCCESS\n";\
ls -lgG; else echo -e "\nFAILED\n"; fi #list the contents of .my_bin in long format #Checks if directory and file were created
```

</br>

</br>

</br>

---

#### Created by Arik Rosenthal
#### If you'd like to contribute to one of the projects, feel free to contact me [@aDENTinTIME](http://twitter.com/aDENTinTIME)
