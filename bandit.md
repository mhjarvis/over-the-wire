# How to Connect
Connect via port 2220 using the bandit0 username at path bandit.labs.overthewire.org, as follows:

    ssh -p 2220 bandit0@bandit.labs.overthewire.org

### Bandit Level 0 => Level 1
Username: bandit0</br>
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
Username: bandit3</br>
Password: UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

Solution:

    cat inhere/.hidden

### Bandit Level 4 => 5
Username: bandit4</br>
Password: pIwrPrtPN36QITSp3EQaw936yaFoFgAB

The ```file``` command helps determine file type. Using grep and piping can help filter out only those 'human-readable' files (ASCII). 

Solution:

    cd inhere
    file ./* | grep ASCII
    cat ./-file07

### Bandit Level 5 => 6
Username: bandit5</br>
Password: koReBOKuIDDepwhWk7jZC0RTdopnAYKh

The ```find``` command will search fo rfiles in a dierctory hierarchy. The following OPTIONS will be helpful: 

    -executable         //matches files which are executable
    -size n             //files uses 'n' units of space, rounding up
    -type c             //file is of type 'c'

The '!' exclamation point also means 'not'. 

Solution:

    find -type f -size 1033c ! -executable
    cat ./inhere/maybehere07/.file2

### Bandit Level 6 => 7
Username: bandit6</br>
Password: DXjZPULLxYr17uwoI01bNLQbtFemEgo7

The following OPTIONS will be helpful with the ```find ``` command:

    -group gname            //file belongs to group gname (numeric group ID allowed)
    -user uname             //file is owned by user uname (numberic user ID allowed)
    -size n                 //file uses 'n' units of space, rounding up

The following is used to help filter out information ```2>/dev/null``` does.

    > file                  //redirects stdout to file
    1> file                 //redirects stdout to file
    2> file                 //redirects stderr to file

Solution:

    cd /                    //go to root directory
    find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
    cat /var/lib/dpkg/info/bandit7.password

### Bandit Level 7 => 8
username: bandit7</br>
passwd: HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

```grep``` will print lines matching a pattern. ```grep [OPTIONS] PATTERN [FILE...]```.

Solution:

    grep millionth data.txt

### Bandit Level 8 => 9
Username: bandit8</br>
Password: cvX2JJa4CFALtqS87jk27qwqGhBM9plV

The ```sort``` command sorts lines of text files and is used as ```sort [OPTION]... [FILE]...```. The ```uniq``` command allow you to report or omit repeated lines.

Solution:

    sort data.txt | uniq -u

### Bandit Level 9 => 10
Username: bandit9
Password: UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

The ```strings``` command will print the sequences of printable characters in files. Used in conjunction with ```grep```, results can be filtered further.

Solution:

    strings -d data.txt | grep ==

### Bandit Level 10 => 11
Username: bandit10
Password: truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

The ```base64``` command will encode/decode data and print to standard output. Use in the form ```base64 [OPTION]... [FILE]```.

    base64 -d data.txt

### Bandit Level 11 => 12
Username: bandit11
Password: IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

The ```tr``` command will translate or delete characters using ```tr [OPTION]... SET [SET2]```. Piping will be required for both  lower-case and upper-case letters.

    tr '[a-z]' '[n-za-m]'           //input will be translated to the matching position
                                    //in the output set
                                    //'a' becomes 'n', 'b' becomes 'o'

Solution:

    cat data.txt | tr '[a-z]' '[n-za-m]' | tr '[A-Z]' '[N-ZA-M]'

### Bandit Level 12 => 13
Username: bandit12
Password: 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu

