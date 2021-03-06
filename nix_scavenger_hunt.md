# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. 

*Paste the output of the `pwd` command here:*

```
/home/cabox/workspace 
```

* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. 

*What directories and files do you see when you run `ls`?*

```
LICENSE  README.md  challenge_files  nix_scavenger_hunt.md  nix_scavenger_hunt_
stretch.md 
```

* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. 

*How are the results different when you use the `-alh` options?*
It includes a lot more information about the files such as last date modified and size.

```
total 36K                                                                      
drwxrwxr-x  4 cabox cabox 4.0K Jan 11 11:01 .                                  
drwxr-xr-x 10 cabox cabox 4.0K Jan 11 13:18 ..                                 
drwxrwxr-x  8 cabox cabox 4.0K Jan 11 11:01 .git                               
-rw-rw-r--  1 cabox cabox 1.1K Jan 11 11:01 LICENSE                            
-rw-rw-r--  1 cabox cabox 2.7K Jan 11 11:01 README.md                          
drwxrwxr-x  7 cabox cabox 4.0K Jan 11 11:01 challenge_files                    
-rw-rw-r--  1 cabox cabox 5.5K Jan 11 11:01 nix_scavenger_hunt.md              
-rw-rw-r--  1 cabox cabox  317 Jan 11 11:01 nix_scavenger_hunt_stretch.md  
```


* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://linux.die.net/man/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. 

*Write down what those options do?*
a:do not ignore entries starting with .
l:use a long listing format
h:with -l, print sizes in human readable format 


* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. 

*What files and directories do you see listed?*

```
bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  sbin  selin
ux  srv  sys  tmp  usr  var   
```

* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) 

*Then run `pwd` and paste the output here:*

```
/ 
```


* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. 

Use `cd` to move to `~`. *Run `pwd` and paste the response here:*

```
/home/cabox 
```



* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. 

*How many files do you find?*
I found 3 files.


* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*

```
/home/cabox/workspace  
```


* Press the up arrow on your keyboard. 

*What just happened?*
It shows the last command I typed


* Press the up arrow a few more times. 

*What do you see?*
It continues to scroll through previously typed commands in reverse order.

* Run the `history` command. 

*What do you see?*
All previously typed commands in order.

### Observing the System

* Discover what account you are logged into using the `whoami` command. 

*What username are you currently using?*
cabox

* Discover who else is on your system with the `who` command. *Are any other users using your system? 
There are no other users using my system.

If so, list them here:*

* How long has your system been running? Use `uptime` to see, and *paste the result here:* 
The system has been running for 2 hours, 31 minutes.


* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) 

*How do you interpret what you see here?*
It's showing me all the processes that are happening on the computer I'm connected to. I'm using CodeAnywhere, and it shows that there are other people using CodeAnywhere on this computer at the same time.


* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) 

*How do you interpret what you see here?*
It's showing all kinds of stats for the computer, and it's changing, so it's showing me an up to date record of these stats.

### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. 

*How many files did you find?*
I found 2 files.

* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) 

*What is the date in the file you have viewed?*
The date in the file is: 1-15-2015

* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. 

*Where is that file located?*

```
./tmp
```


* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state).

*How many files did you find?*
I found 2 files.


* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. 

*Paste the result showing the file and line where the word "Waldo" shows up.*

```
challenge_files/serial-numbers/eaque_molestiae.txt:Ut est maiores quia autem. Ni
si modi Waldo sed corporis sit explicabo ut est. Et est placeat ea sunt sunt con
sectetur sunt incidunt. Explicabo vel esse blanditiis dolorem culpa non quia. 
```

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. 

*What do you see in the `files.txt` file?*
I see all the file names that were pushed into the file.


* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. 

*Describe what you see when you run `ls -alh | more`.*
It shows me only one page of the list at a time.

* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. 

*Paste the list of processes that reference your username here:*

```
root      2532  0.0  0.6  69184  3492 ?        Ss   Jan11   0:00 sshd: cabox [priv]                                                                             
cabox     2536  0.0  0.2  69184  1476 ?        S    Jan11   0:00 sshd: cabox@pts/1                                                                              
cabox     2537  0.0  0.6  12916  3232 pts/1    Ss+  Jan11   0:00 -bash          
root      3372  0.0  0.6  69184  3488 ?        Ss   Jan11   0:00 sshd: cabox [priv]                                                                             
root      3374  0.0  0.6  69184  3488 ?        Ss   Jan11   0:00 sshd: cabox [priv]                                                                             
cabox     3376  0.0  0.2  69184  1476 ?        S    Jan11   0:00 sshd: cabox@pts/0                                                                              
cabox     3377  0.0  0.2  69340  1488 ?        S    Jan11   0:00 sshd: cabox@pts/2                                                                              
cabox     3378  0.0  0.6  12916  3228 pts/0    Ss+  Jan11   0:00 -bash          
cabox     3466  0.0  0.6  12916  3252 pts/2    Ss   Jan11   0:00 -bash          
root      3811  0.0  0.6  69184  3452 ?        Ss   00:36   0:00 sshd: cabox [priv]                                                                             
cabox     3813  0.0  0.3  69340  1604 ?        S    00:36   0:00 sshd: cabox@notty                                                                              
cabox     3814  0.0  0.4  57828  2300 ?        Ss   00:36   0:00 /usr/libexec/op
enssh/sftp-server                                                               
cabox     4014  0.0  0.2  13372  1064 pts/2    R+   00:41   0:00 ps aux         
cabox     4015  0.0  0.1   6384   680 pts/2    S+   00:41   0:00 grep cabox    
```
