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

* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?* I see all the projects in my project explorer.

rsabaric.github.io      wats3010-adv-markup    wats3010-css             wats3010-hello-world           wats3010-product-page  wats3020-sandwich-machine
wats1030-intro-to-unix  wats3010-basic-markup  wats3010-embedded-media  wats3010-intro-to-bootstrap-4  wats3020-mad-libs

* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?* I am getting a note that says command not found for options.

total 4.0Ktotal 4.0K
drwxr-xr-x 13 user root  321 Jul  4 01:11 .
drwxr-xr-x 22 root root  295 Jul  6 20:07 ..
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

/home/user

* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*

bash: /home/user: Is a directory

* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?* Just one file. 2015_special_stuff.demo

* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?* cd
* Press the up arrow on your keyboard. *What just happened?* it changed to cd
* Press the up arrow a few more times. *What do you see?* I see everything I had just entered previously. 
* Run the `history` command. *What do you see?* 
    1  ls
    2  cd wats1030-intro-to-unix/challenge_files/
    3  ls
    4  cd
    5  history

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

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?* I found many files. In fact too many to count. I could barely capture all of them. Here is just a small sample of what I was able to copy and paste. It seems the main file names are credit_cards2.txt and credit_cards.txt with many variations as the small sample below. 

credit_cards2.txt:201493327821934
credit_cards2.txt:2100180073746880
credit_cards2.txt:30331841165601
credit_cards2.txt:201456362059785
credit_cards2.txt:1800160500781424
credit_cards2.txt:2100167177143932
credit_cards2.txt:201440321910544
credit_cards2.txt:201493256525142
credit_cards.txt:Last updated: 01-15-2015
credit_cards.txt:6011648902145507
credit_cards.txt:6011541522810495
credit_cards.txt:201489234446831
credit_cards.txt:2100183923553803
credit_cards.txt:6011480509444137
credit_cards.txt:6011525210032934
credit_cards.txt:601115084631471


* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?* I am just seeing a string of numbers. Each time I press the space bar, the --More-- changes it's precentage. The last update was Last updated: 01-15-2015.

* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?* ./tmp/modi_laboriosam.txt

* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*

I found two files. Britt-Erdman.user:O'Harachester, WA 37261
Lissie-Strosin.user:Jewessfurt, WA 00816-7241

* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*

serial-numbers/eaque_molestiae.txt:Ut est maiores quia autem. Nisi modi Waldo sed corporis sit explicabo ut est. Et est placeat ea sunt sunt consectetur sunt incid
unt. Explicabo vel esse blanditiis dolorem culpa non quia.
### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?* It seems I am still in seeing the challenge_files folder.

* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.* All the file names simply appear very quickly with ls -alh, but when I enter ls-alh | more I see a little box at the bottom that says more. When I hit the space bar, I can scroll through the names much better. 

* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:* This list seems like the longest one I have seen yet. I see that the word user is highlighted, but that is how Codenvy seemed to recognize my name too. Here is just a small sample.

user@f92bb33e72bb:/projects/wats1030-intro-to-unix/challenge_files$ ps aux | grep user
user         1  0.0  0.0   4500   644 ?        Ss   22:22   0:00 /bin/sh -c tail -f /dev/null
user        28  0.0  0.0   6036   624 ?        S    22:22   0:00 tail -f /dev/null
user        30  0.0  0.0   4508   752 ?        Ss   22:22   0:00 /bin/sh -c trap '[ -z "$(jobs -p)" ] || kill $(jobs -p); [ -e /tmp/docker-exec-214792.pid ] && rm
/tmp/docker-exec-214792.pid' EXIT; echo $$>/tmp/docker-exec-214792.pid; # # Copyright (c) 2012-2017 Red Hat, Inc. # All rights reserved. This program and the accom
panying materials # are made available under the terms of the Eclipse Public License v1.0 # which accompanies this distribution, and is available at # http://www.e
clipse.org/legal/epl-v10.html # # Contributors: #   Red Hat, Inc. - initial API and implementation #   is_current_user_root() {     test "$(id -u)" = 0 }  is_curre
nt_user_sudoer() {     sudo -n true > /dev/null 2>&1 }  set_sudo_command() {     if is_current_user_sudoer && ! is_current_user_root; then SUDO="sudo -E"; else uns
et SUDO; fi }  set_sudo_command unset PACKAGES command -v tar >/dev/null 2>&1 || { PACKAGES=${PACKAGES}" tar"; } CURL_INSTALLED=false WGET_INSTALLED=false command
-v curl >/dev/null 2>&1 && CURL_INSTALLED=true command -v wget >/dev/null 2>&1 && WGET_INSTALLED=true  # no curl, no wget, install curl if [ ${CURL_INSTALLED} = fa
lse ] && [ ${WGET_INSTALLED} = false ]; then   PACKAGES=${PACKAGES}" curl";   CURL_INSTALLED=true fi  CHE_DIR=$HOME/che LOCAL_AGENT_BINARIES_URI='/mnt/che/exec-age
nt/exec-agent-${PREFIX}.tar.gz' DOWNLOAD_AGENT_BINARIES_URI='${WORKSPACE_MASTER_URI}/agent-binaries/${PREFIX}/exec/exec-agent-${PREFIX}.tar.gz' TARGET_AGENT_BINARI
ES_URI='file://${CHE_DIR}/exec-agent-${PREFIX}.tar.gz'  if [ -f /etc/centos-release ]; then     FILE="/etc/centos-release"     LINUX_TYPE=$(cat $FILE | awk '{print
 $1}')  elif [ -f /etc/redhat-release ]; then     FILE="/etc/redhat-release"     LINUX_TYPE=$(cat $FILE | cut -c 1-8)  else     FILE="/etc/os-release"     LINUX_TY
