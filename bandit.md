# How to Connect
Connect via port 2220 using the bandit0 username at path bandit.labs.overthewire.org, as follows:

    ssh -p 2220 bandit0@bandit.labs.overthewire.org

### Bandit Level 0 => Level 1
Username and password are given as bandit0.

Using the ```cat``` command will concatenate files and print on the standard output. The ```ls``` command will list directory contents. ```man ls``` will provide access to the manpage where there are several important OPTIONS available. While not needed here, the following will be important:

    -a, --all           //does not ignore entries with .
    -l                  //use a long listing format
    -al                 //combine both OPTIONS

### Bandit Level 1 => Level 2
username: bandit1</br>
passwd: boJ9jbbUNNfktd78OOpsqOltutMc3MY1

Using the ```pwd``` command we get the location of our current directory. Attempting to use ```cat -``` will not do much since the '-' character is a special character for providing argumets. The prefix ```./``` should solve the problem as it clarify that the file is in the current directory.

### Bandit Level 2 => Level 3
username: bandit2</br>
passwd: CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

The password is stored in a file with spaces in the filename. Again, ```cat``` alone will not work, as each blankspace creates a new argument. Using quotations or escaping the spaces will work at reading the file. 

### Bandit Level 3 => 4
username: bandit3</br>
passwd: UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

Using the ```-a, -l``` OPTIONS with ls should show the hidden filename. From there, using ```cat``` should work.

### Bandit Level 4 => 5
username: bandit4</br>
passwd: pIwrPrtPN36QITSp3EQaw936yaFoFgAB

The password is in the only human-readable file in the inhere directory. The ```file``` command will be easiest way to go about finding which file contains the password. 

### Bandit Level 5 => 6
username: bandit5
passwd: koReBOKuIDDepwhWk7jZC0RTdopnAYKh

The ```find``` command will be most useful in this instance. The following OPTIONS will be helpful: 

    -executable         //matches files which are executable
    -size n             //files uses 'n' units of space, rounding up
    -type c             //file is of type 'c'

Remember that the '!' exclamation point also means 'not'. 

### Bandit Level 6 => 7
username: bandit6
passwd: DXjZPULLxYr17uwoI01bNLQbtFemEgo7
