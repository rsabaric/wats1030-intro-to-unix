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

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:* /projects

* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?* 

rsabaric.github.io      wats3010-adv-markup    wats3010-css             wats3010-hello-world           wats3010-product-page  wats3020-sandwich-machine
wats1030-intro-to-unix  wats3010-basic-markup  wats3010-embedded-media  wats3010-intro-to-bootstrap-4  wats3020-mad-libs

* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?* For the -alh options I am getting a note saying command not found. The ls -alh is below.

total 4.0K

drwxr-xr-x 13 user root  321 Jul  4 01:11 .
drwxr-xr-x 22 root root  295 Jul  5 18:10 ..
drwxr-xr-x  4 user root  109 Jun 26 18:07 rsabaric.github.io
drwxr-xr-x  5 user root  178 Jul  4 01:11 wats1030-intro-to-unix
drwxr-xr-x  4 user root  253 Apr 25 02:23 wats3010-adv-markup
drwxr-xr-x  4 user root  192 Apr 13 01:31 wats3010-basic-markup
drwxr-xr-x  5 user root  130 Apr 22 21:40 wats3010-css
drwxr-xr-x  7 user root  134 May  3 03:02 wats3010-embedded-media
drwxr-xr-x  4 user root   98 Apr  9 00:19 wats3010-hello-world
drwxr-xr-x 11 user root 4.0K May 16 01:06 wats3010-intro-to-bootstrap-4
drwxr-xr-x  8 user root  300 Jun  3 23:31 wats3010-product-page
drwxr-xr-x  6 user root  101 Jun 29 03:45 wats3020-mad-libs
drwxr-xr-x  7 user root  115 Jul  3 16:37 wats3020-sandwich-machine

* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://man.he.net/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?* 

The man ls displays the manual page for the item or program. The 'a' command displays all the of manual intro pages. The 'l" decompresses the files. Lastly, the 'h' command seems to show where a symlink points. 

* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*

bin  boot  dev  etc  home  lib  lib64  media  mnt  open-jdk-source-file-location  opt  proc  projects  root  run  sbin  srv  sys  tmp  usr  var

* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*

user@810583208b96:/projects$ cd
user@810583208b96:~$ pwd
/home/user
user@810583208b96:~$

* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*

/home/user

* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?* Just one file. 2015_special_stuff.demo

* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*
* Press the up arrow on your keyboard. *What just happened?* it changed to cd
* Press the up arrow a few more times. *What do you see?* I see everything I had just entered previously. 
* Run the `history` command. *What do you see?* 
    1  uptime
    2  ps aux
    3  top
    4  ls
    5  pwd
    6  cd wats 1030-intro-to-unix/challenge_files/
    7  cd wats1030-intro-to-unix/challenge_files/
    8  pwd
    9  ls
   10  cd
   11  cd up
   12  history

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?* I am only getting the result 'user'.

* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:* There is no one else listed.

* How long has your system been running? Use `uptime` to see, and *paste the result here:*  19:42:58 up 3 days, 11:36,  0 users,  load average: 0.42, 0.62, 0.91
* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?* I can't really tell what is happening her, but it seems like it is just showing me working through some projects. 
SER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
user         1  0.0  0.0   4500   640 ?        Ss   20:01   0:00 /bin/sh -c tail -f /dev/null
root        26  0.0  0.0  47000  2004 ?        S    20:01   0:00 sudo /usr/sbin/sshd -D
user        27  0.0  0.0   6036   628 ?        S    20:01   0:00 tail -f /dev/null
root        28  0.0  0.0  65512  3252 ?        S    20:01   0:00 /usr/sbin/sshd -D
user        32  0.0  0.0   4508   752 ?        Ss   20:01   0:00 /bin/sh -c trap '[ -z "$(jobs -p)" ] || kill $(jobs -p); [ -e /tmp/docker-exec-198020.pid ]
user        92  0.0  0.0  13128  7872 ?        Sl   20:01   0:00 /home/user/che/exec-agent/che-exec-agent -addr :4412 -cmd /bin/bash -path /[^/]+ -enable-aut
user       106  0.0  0.0   4508   748 ?        Ss   20:01   0:00 /bin/sh -c trap '[ -z "$(jobs -p)" ] || kill $(jobs -p); [ -e /tmp/docker-exec-198023.pid ]
user       167  0.0  0.0  14324  8024 ?        Sl   20:01   0:00 /home/user/che/terminal/che-websocket-terminal -addr :4411 -cmd /bin/bash -path /[^/]+ -enab
user       284  0.0  0.0   4508   752 ?        Ss   20:01   0:00 /bin/sh -c trap '[ -z "$(jobs -p)" ] || kill $(jobs -p); [ -e /tmp/docker-exec-198038.pid ]
user       344 16.0  1.3 5816484 411180 ?      Sl   20:01   0:40 /usr/lib/jvm/java-1.8.0-openjdk-amd64/bin/java -Djava.util.logging.config.file=/home/user/ch
user       473  0.0  0.0  21036  3312 pts/0    Ss   20:02   0:00 /bin/bash
user       504  0.0  0.0  36076  1644 pts/0    R+   20:06   0:00 ps aux
* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?* It seems like this is constantly changing. Even where I can't seem to copy it quickly enough. This shows some commands and run time. 

### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?* I found two files.

* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?* I am just seeing a string of numbers. Each time I press the space bar, the --More-- changes it's precentage.

* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*

I am getting the a note that there is no such file or directory.

* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*
* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*
* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*
* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*
