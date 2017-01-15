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

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:*

Is a directory 

* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?*

LICENSE  README.md  challenge_files  nix_scavenger_hunt.md  n
ix_scavenger_hunt_stretch.md  

* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?*

total 36K                                                    
drwxrwxr-x  4 cabox cabox 4.0K Jan 13 04:06 .                
drwxr-xr-x 11 cabox cabox 4.0K Jan 13 04:06 ..               
drwxrwxr-x  8 cabox cabox 4.0K Jan 13 04:06 .git             
-rw-rw-r--  1 cabox cabox 1.1K Jan 13 04:06 LICENSE          
-rw-rw-r--  1 cabox cabox 2.7K Jan 13 04:06 README.md        
drwxrwxr-x  7 cabox cabox 4.0K Jan 13 04:06 challenge_files  
-rw-rw-r--  1 cabox cabox 5.5K Jan 13 04:06 nix_scavenger_hun
t.md                                                         
-rw-rw-r--  1 cabox cabox  317 Jan 13 04:06 nix_scavenger_hun
t_stretch.md 

* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://linux.die.net/man/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?*

ls command list the files and directories 
-a will show you ALL the files in the directory including hidden files
-l will give you a long listing
-h will show the size in "human readable format"


* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*

bin   etc       lib    mnt   root  srv  usr                  
boot  fastboot  lib64  opt   run   sys  var                  
dev   home      media  proc  sbin  tmp  

* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*

/


* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*

/home/cabox


* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?*

scooter-double-mamba.demo
cloaked-wookie.demo 
2015_special_stuff.demo 

* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*

/workspace 


* Press the up arrow on your keyboard. *What just happened?*

-The last command I typed appeared 

* Press the up arrow a few more times. *What do you see?*

-It goes through all the previos commands I entered 

* Run the `history` command. *What do you see?*

-a list numbering 1 through 80 appeared showing the history of all commands I have typed. 

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?*

-cabox


* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:*

-No other user shows up


* How long has your system been running? Use `uptime` to see, and *paste the result here:*

02:01:08 up 26 min,  5 users,  load average: 0.00, 0.00, 0.0
0   


* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*

-ps displays information about a selection of the active processes

* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?*

-shows tasks that are running and sleeping. currently there are 36 total tasks and 1 is running while the rest are sleeping. the task that is running is is the last one pid user: 2148 cabox.

### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?*

-2 files with the word credit in it 

* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?*

01-15-2015  

* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*

tmp/modi_laboriosam.txt 

* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*

Britt-Erdman.user:O'Harachester, WA 37261
Lissie-Strosin.user:Jewessfurt, WA 00816-7241

* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*

rial-numbers/eaque_molestiae.txt:Ut est maiores quia autem. Nisi modi Waldo sed corporis sit explicabo ut est. Et est placeat ea sunt sunt consectetur sunt incidunt. Explicabo vel esse blanditiis dolorem culpa non quia.



### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*

it shows files from top to bottom 

* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*

paginated format divided (content) into discrete page, otherwise it didnt change the content.

* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*

root       593  0.0  0.6  63876  3480 ?        Ss   16:07   0:00 sshd: cabox [priv]                                                                        
cabox      595  0.0  0.2  63876  1468 ?        S    16:07   0:00 sshd: cabox@pts/0                                                                         
cabox      596  0.0  0.6  19464  3404 pts/0    Ss   16:07   0:00 -bash                                                                                     
cabox      924  0.0  0.2  15520  1144 pts/0    R+   16:57   0:00 ps aux                                                                                    
cabox      925  0.0  0.1   8816   764 pts/0    S+   16:57   0:00 grep --color=auto cabox 

