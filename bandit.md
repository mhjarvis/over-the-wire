# How to Connect
Connect via port 2220 using the bandit0 username at path bandit.labs.overthewire.org, as follows:

    ssh -p 2220 bandit0@bandit.labs.overthewire.org

### Bandit Level 0 => Level 1
Username: bandit0
Password: bandit0

The ```cat``` command will concatenate files and print on the standard output. The ```ls``` command will list directory contents. ```man ls``` will provide access to the manpage where there are several important OPTIONS available. While not needed here, the following OPTIONS are important to know when using the ```ls``` command:

    -a, --all           //does not ignore entries with .
    -l                  //use a long listing format
    -al                 //combine both OPTIONS

Solution: 

    cat readme

### Bandit Level 1 => Level 2
Username: bandit1</br>
Password: boJ9jbbUNNfktd78OOpsqOltutMc3MY1

The ```pwd``` command prints the location of the current directory. Attempting to use ```cat -``` will not do much since the '-' character is a special character for providing argumets. The prefix ```./``` should solve the problem as it clarify that the file is in the current directory.

Solution:

    cat ./-

### Bandit Level 2 => Level 3
Username: bandit2</br>
Password: CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

The command ```cat``` alone will not work, as each blank space creates a new argument. Using quotations or escaping the spaces will reference the words as one file name.

Solution:

    cat "spaces in this filename"






### Bandit Level 3 => 4
username: bandit3</br>
passwd: UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

Using the ```-a, -l``` OPTIONS with ls should show the hidden filename. From there, using ```cat``` should work.

### Bandit Level 4 => 5
username: bandit4</br>
passwd: pIwrPrtPN36QITSp3EQaw936yaFoFgAB

The password is in the only human-readable file in the inhere directory. The ```file``` command will be easiest way to go about finding which file contains the password. 

### Bandit Level 5 => 6
username: bandit5</br>
passwd: koReBOKuIDDepwhWk7jZC0RTdopnAYKh

The ```find``` command will be most useful in this instance. The following OPTIONS will be helpful: 

    -executable         //matches files which are executable
    -size n             //files uses 'n' units of space, rounding up
    -type c             //file is of type 'c'

Remember that the '!' exclamation point also means 'not'. 

### Bandit Level 6 => 7
username: bandit6</br>
passwd: DXjZPULLxYr17uwoI01bNLQbtFemEgo7

The password is saved somewhere on the server and has several new properties. Again, the ```find``` command is one way to find the file that matches all the properties. The following OPTIONS will be helpful to lookup:

    -group gname            //file belongs to group gname (numeric group ID allowed)
    -user uname             //file is owned by user uname (numberic user ID allowed)
    -size n                 //file uses 'n' units of space, rounding up

While this will be enough to find the password, there will be a lot of extra information that would be nice to filter out. In this case it is worthwhile understanding what ```2>/dev/null``` does.

    > file                  //redirects stdout to file
    1> file                 //redirects stdout to file
    2> file                 //redirects stderr to file

### Bandit Level 7 => 8
username: bandit7</br>
passwd: HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

    grep millionth data.txt

### Bandit Level 8 => 9
username: bandit8</br>
passwd: cvX2JJa4CFALtqS87jk27qwqGhBM9plV