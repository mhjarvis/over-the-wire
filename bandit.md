# How to Connect
Connect via port 2220 using the bandit0 username at path bandit.labs.overthewire.org, as follows:

    ssh -p 2220 bandit0@bandit.labs.overthewire.org

### Bandit 0
Username and password are given as bandit0.

### Bandit 1
Using the ```cat``` command will concatenate files and print on the standard output. The ```ls``` command will list directory contents. ```man ls``` will provide access to the manpage where there are several important OPTIONS available. While not needed here, the following will be important:

    -a, --all           //does not ignore entries with .
    -l                  //use a long listing format
    -al                 //combine both OPTIONS

passwd: boJ9jbbUNNfktd78OOpsqOltutMc3MY1

### Bandit 2
Specify the full location of the file, as follows:

    cat ./-

username: bandit2
<br/>
passwd: CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

### Bandit 3
Surround string with quotes:

    cat 'spaces in this filenam'

username: bandit3
<br/>
passwd: UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

### Bandit 4
The file is hidden. Find the name of the hidden file and read it.

    ls -A               //-a shows all files
    cat .hidden

username: bandit4
<br/>
passwd: pIwrPrtPN36QITSp3EQaw936yaFoFgAB

### Bandit 5
The file is stored in the only human-readable file in the 'inhere' folder. 

    file -- *
    cat ./-file07

username: bandit5
<br/>
passwd: koReBOKuIDDepwhWk7jZC0RTdopnAYKh

### Bandit 6
The file is human-readable, 1033 bytes, not executable. The ```find``` command by itself will find and print ever directory/file from the starting point. For this example, there is one file that meets the size requirement of 1033 bytes.

    find -size 1033c
    cat ./inhere/maybehere07/.file2

username: bandit6
<br/>
passwd: DXjZPULLxYr17uwoI01bNLQbtFemEgo7

### Bandit 

username: bandit7
<br/>
passwd: HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 

### Bandit 

username: bandit

passwd: 