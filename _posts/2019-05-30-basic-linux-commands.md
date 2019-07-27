---
layout: post
title: Basic Linux Commands
date: 2019-05-30 18:04
author: ajulusthoughts
comments: true
categories: [Ajulu's Thoughts, command, command line, commands, linux, linux command line, linux commands, linux terminal, TECH &amp; CYBERSECURITY, terminal, terminal commands]
---
<!-- wp:heading -->
<h2><strong><span style="text-decoration:underline;">Terminal Navigation Commands</span></strong></h2>
<!-- /wp:heading -->

<!-- wp:paragraph {"dropCap":true} -->
<p class="has-drop-cap">Before you can really make full use of the terminal, you’ll need to know how to navigate it. Two things are true of the Linux command line: one, there are thousands of possible commands  you can use at any given time, and two, you’ll only end up using a  fraction of them. Despite the power offered, most of us just repeat the  same commands over and over again. A lot of people still see Linux as a difficult operating system used  only by hardcore geeks who have a bazillion commands memorized, but  that’s simply not true. If you can learn the most-used commands, you’ll  have a perfectly fine time in Linux — even as a total newbie. </p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li><strong>&amp;&amp;</strong> — This one is so basic that it’s not  even technically a command. If you ever want to run multiple commands in  sequential order, just stick this in between each one. For example, <code>[command1] &amp;&amp; [command2]</code> will first run [command1] then immediately follow it with [command2]. You can chain as many commands as you want.</li><li><strong>!</strong> — Repeats a recently used command. Best to use it in conjunction with the <code>history</code> command. You can use <code>!n</code> to repeat the n-th command in history. You can also use <code>!-n</code> to repeat the command that happened n commands ago.</li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/cd.html" target="_blank">cd</a></strong> — Changes the current terminal directory.</li><li><strong>clear</strong> — Clears the terminal screen.</li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/history.html" target="_blank">history</a></strong>  — Displays a list of all recently used commands. You can also cycle  through recently used commands by pressing the Up and Down arrow keys in  the terminal.</li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/ls.html" target="_blank">ls</a></strong>  — Displays a list of all files in the current terminal directory. You  can modify it with parameters to specify some other directory or to  change the format of the list.</li><li><strong>man –</strong> There’s a running gag in the Linux community that <em>man</em> is the only command you need to know. It stands for <em>manual</em>, and it will give you detailed information on commands and aspects of Linux.</li><li><strong>reboot –</strong> Immediately stops all running processes, shuts down the system, then reboots.</li><li><strong>shutdown –</strong>  Stops all running processes and shuts down the system. Parameters can  be specified to issue a delayed shutdown or a shutdown at a particular  time.</li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/man.html" target="_blank">man</a></strong>  — Displays a help page (from the manual) based on your search query.  Very useful for learning how to use a command you don’t recognize or  when you forget the parameters for an infrequently used command. If  you’re ever confused, turn to man.</li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/pwd.html" target="_blank">pwd</a></strong> — Displays the current terminal directory as an absolute path.</li><li><strong>whatis</strong> — Displays brief descriptions of command line programs. Think of it like a simplified version of <code>man</code> when you aren’t sure what a command does but don’t need the full manual on how to use it.</li></ul>
<!-- /wp:list -->

<!-- wp:heading -->
<h2><strong><span style="text-decoration:underline;">File Management Commands</span></strong></h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Most Linux distros come with a graphical desktop environment, and no matter which desktop environment you choose to use,  you’ll be able to browse and manage files in the same way you would on  Windows or Mac — but for complex tasks, it’s often easier and faster to  use the command line.</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/cat.html" target="_blank">cat</a></strong>  — When used on a single text file, it will display the contents of that  file. When used on two or more text files, it will display all of their  contents in sequential order. Use the redirection operator (“<strong>&gt;</strong>“) to combine multiple text files into one text file.</li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/chmod.html" target="_blank">chmod</a>/<a rel="noreferrer noopener" href="http://ss64.com/bash/chown.html" target="_blank">chown</a></strong> — The <code>chmod</code> command changes the read, write, and execute permissions of a file while the <code>chown</code> command changes the user and/or user group that owns a file.</li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/cp.html" target="_blank">cp</a></strong>  — Makes a copy of a file. By default, the copy appears in the current  terminal directory, but you can also specify the destination directory  as well.</li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/find.html" target="_blank">find</a></strong>  — Searches a specific directory (or your entire system) to find files  that match a given set of criteria. There are dozens of options,  including filename, filetype, filesize, permissions, owners, date  created, date modified, etc.</li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/grep.html" target="_blank">grep</a></strong>  — Searches a specific file or set of files to see if a given string of  text exists, and if it does, tells you where the text exists in those  files. This command is extremely flexible (e.g. use  wildcards to search all files of a given type) and particularly useful  for programmers (to find specific lines of code). </li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/locate.html" target="_blank">locate</a></strong>  — Searches the entire system for files or directories that match the  search query, then outputs the absolute paths for each match. By  default, it only searches in directories for which you have permissions.  This is the simplest and fastest way to find a file. </li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/mkdir.html" target="_blank">mkdir</a>/<a rel="noreferrer noopener" href="http://ss64.com/bash/rmdir.html" target="_blank">rmdir</a></strong>  — Creates or deletes a directory, by default in the current terminal  directory but a target directory can be specified as well. When  deleting, the directory must be completely empty. </li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/mv.html" target="_blank">mv</a></strong>  — Moves a file from one directory to another, and you can specify a  different name for the file in the target directory. You can use this  command to rename a file by moving it to the same directory but with a  different filename. </li><li><strong>nano/emacs/vim</strong> — The three main terminal text  editors that exist on nearly all Linux systems, ordered by increasing  complexity. Newbies should stick to <code>nano</code> as both <code>emacs</code> and <code>vim</code> are wildly complex (and wildly powerful). </li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/rename.html" target="_blank">rename</a></strong>  — Changes the name of a file or a set of files. Comes with a lot of  interesting parameters, allowing you to automatically rename a bunch of  files according to a pattern. </li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/rm.html" target="_blank">rm</a></strong>  — Removes files. With a certain parameter, it can be used to wipe the  entire contents of a specified directory. It can also be used to delete  several files that all match a certain filename pattern.</li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/touch.html" target="_blank">touch</a></strong> — Changes the date accessed or date modified of the given file to right now.</li><li><strong>wget</strong> — Downloads the file or page at the given web URL.</li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/zip.html" target="_blank">zip</a>/<a rel="noreferrer noopener" href="http://ss64.com/bash/gzip.html" target="_blank">gzip</a>/<a rel="noreferrer noopener" href="http://ss64.com/bash/tar.html" target="_blank">tar</a></strong> — Various formats for compressing and decompressing file archives.</li><li><strong>ftp / sftp –</strong> Connects to a remote FTP server in order to download multiple files.</li><li><strong>wget –</strong> Downloads files from the Internet at the specified URL to your system.</li></ul>
<!-- /wp:list -->

<!-- wp:heading -->
<h2><strong><span style="text-decoration:underline;">System Management Commands</span></strong></h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Again,
 most Linux distros provide a graphical way to manage your system 
settings, but you may find it easier (and perhaps even more informative)
 to use these time-tested commands instead. Indeed, these commands tend 
to offer a lot more power in terms of what you can do.</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li><strong>apt</strong> — While <code>apt</code> isn’t a command in itself, there are three commands that you must know to make full use of APT: <code>add-apt-repository</code> (for locating third-party packages), <code>apt-get</code> (for actually installing packages), and <code>apt-cache</code> (for searching your repositories). <ul><li>If your distro doesn’t use APT, it may use YUM, RPM, or some other alternative. Look into their equivalent commands. </li><li> <strong>yum –</strong>  Yellowdog  Updater, Modified. An open source package manager used to  easily  install software packages from repositories. Available on   RPM-compatible Linux distributions. </li></ul></li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/bg.html" target="_blank">bg</a>/<a rel="noreferrer noopener" href="http://ss64.com/bash/fg.html" target="_blank">fg</a></strong> — Sends a foreground job to run in the background or a background job to run in the foreground. For more on jobs, see the <code>jobs</code> command.</li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/df.html" target="_blank">df</a></strong> — Displays how much space is used and free on your system.</li><li><strong>free</strong> — Displays how much RAM is used and free on your system.</li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/ip.html" target="_blank">ip</a></strong> —  Displays useful network details such as your IP address, network  interfaces, bandwidth usage, and more. Can also be used to configure  network-related settings.</li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/jobs.html" target="_blank">jobs</a></strong> — Displays all current jobs and their statuses. A job is just a representation of a running process or group of processes.</li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/kill.html" target="_blank">kill</a>/<a rel="noreferrer noopener" href="http://ss64.com/bash/killall.html" target="_blank">killall</a></strong> — You can use <code>kill</code> to end a process according to its process ID (often used in conjunction with the <code>ps</code> command) whereas you can use <code>killall</code> to end all processes whose names match your query.</li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/mount.html" target="_blank">mount</a>/umount</strong>  — Attaches and detaches a separate filesystem to your system’s main  filesystem. Mostly used to make external devices, like hard drives or  USB drives, interactable with your computer. <strong><a rel="noreferrer noopener" href="http://ss64.com/bash/ps.html" target="_blank">ps</a></strong>  — Displays a list of currently running processes. By default, it only  lists processes started under your current user, but parameters exist to  find and filter all kinds of processes. </li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/sudo.html" target="_blank">sudo</a>/gksudo</strong> — Prepending <code>sudo</code> allows you to run any command as superuser (e.g. <code>sudo [command1]</code>). If you want to run a graphical program with superuser privileges, use <code>gksudo</code> followed by the executable file for the program. </li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/top.html" target="_blank">top</a></strong> — Displays a list of currently running processes, sorted by how much CPU each processes uses. Unlike <code>ps</code>, this command regularly updates in real-time. Basically a terminal equivalent to Task Manager. </li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/uname.html" target="_blank">uname</a></strong>  — Displays core system information depending on the parameters you use,  such as kernel name and version, machine hardware, and operating  system. </li><li><strong>uptime</strong> — Displays time elapsed since last boot. </li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/whereis.html" target="_blank">whereis</a></strong> — Finds the location of the executable file for a given program. </li><li><strong><a rel="noreferrer noopener" href="http://ss64.com/bash/whoami.html" target="_blank">whoami</a></strong> — Displays the current user name. Comes in handy when you’re switching between users with the <code>su</code> command and you lose track of who you are at the moment.</li><li><strong>date –</strong> Prints out the current system date and time. Specified parameters can change the format of the output.</li><li><strong>hostname –</strong> Displays the name of the current host system.</li><li><strong>ps –</strong> Displays information about all of the processes currently running on the system.</li><li><strong>quota –</strong>  Displays disk limits and current disk usage for a specified user.  Useful when there are multiple users assigned to a particular system.</li></ul>
<!-- /wp:list -->

<!-- wp:heading {"level":3} -->
<h3>Important information about the Linux terminal</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>There is not a single Linux distribution, as far as we know, that  doesn't have a terminal of some kind. On the contrary, there are a few  distributions that don't have a GUI by default, and everything is done  on the command line.<br>To open a terminal quickly from the GUI, the shortcut <strong>Ctrl+Alt+T</strong> will work on most distributions and desktop environments.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>This is the&nbsp;basic anatomy of most Linux commands:</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">[sudo] <strong>command</strong> [optional switch] [file or directory path]</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>Using<strong> sudo</strong>&nbsp;will run any command with administrative 
rights. Most Linux commands that have to deal with system files and 
installation/uninstallation of programs demand sudo.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>The linux commands are&nbsp;case-sensitive</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>It is important to remember that everything written in the terminal  is case-sensitive. When the command is "sudo", neither "Sudo", "SUDO",  nor "sUdO" will work.<br>Most Linux commands are lowercase, but there are capitalized switches, such as "chown -R".<br>The file and directory names are also case-sensitive. "File1" and  "file1" are different files, even if they are in the same directory.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>Beware of spaces</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Spacing is equally important. "chown-R" will only return an error. If  we want to create/access/delete a file or directory that has a space in  the filename, we can either put the whole filename inside quotation  marks......or "escape" the space using the backslash "\".<br>If we did neither, the particular mkdir command, which creates  directories, would create two directories, "Folder" and "Name". Other  Linux commands would just fail.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>Finding previous Linux commands</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Pressing the Up keyboard key will cycle through the last Linux  commands we successfully used, in order. No failed commands will show  here.<br>We can also use the <strong>history</strong> command to see all the Linux commands we have ever used on the terminal.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>The invisible password</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>When we are asked for our password, e.g. after we used "sudo", as we  type the password nothing will show on screen, no stars or dots or  anything. We just type the password and press Enter.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>Use Tab to autocomplete</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The Tab button on the keyboard is a huge time saver on Linux  commands, as it will automatically fill in the names of files and  directories.<br>If we want to delete a file named "whydidIgivethisfilesuchalongname",  we just need to type "rm w" and pressing Tab will automatically  complete the rest of the filename.<br>If there are more than files that begin with the same letters, e.g.  "whydidIgivethisfilesuchalongname" and "whydidIeatsomuch", pressing Tab  on "rm w" will autocomplete the common "whydidI".<br>We then need to type an additional character - "g" or "e", in the  example - and press again Tab for the auto completion to resume.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>Copying and pasting Linux commands</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>To copy or paste on the terminal, Ctrl+C and Ctrl+V won't work.<br>Instead, we must use Ctrl+Shift+C and Ctrl+Shift+V. Or we can right click and use the commands from the context menu.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>Wildcards</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>While using Linux commands, the characters "?" and "*" are wildcards.<br>"?" will replace any single character. So, if we have two files names  test1file and test2file, we can delete them both with "rm test?file".  But this won't delete test12file.<br>"*" will replace any string of characters. "rm test*file" will delete  test1file, test12file, testBLABLABLAfile. It will also delete any other  filename that begins with "test-" and ends in "-file", including  testfile.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>It is obvious that we must be extremely careful when combining  deletion commands with wildcards. "rm *" will delete every file in the  current directory, and it won't use Trash.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>What to do with commands that return too many results</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>If we run "ls" on a directory with 1,000 files, or we use "locate 
*.png" on a disk with lots of png pictures, we will get too many 
results.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In this case, we can use a&nbsp;pipe with the vertical bar "<strong>|</strong>" symbol (accessible with "Shift + \" ) and <strong>more</strong> or <strong>less</strong>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>With <strong>locate *.png&nbsp;| more&nbsp;</strong>we will get the results page by page, and we can reveal the next pages by pressing space. We quit by pressing "q".</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>With <strong>locate *.png | less </strong>we will still get the first page of results, but navigate up and down with the arrow keys. Again, we quit with "q".</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>Directory access shortcuts</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>When we want to navigate to a particular directory or access a 
specific file, it's handy to keep in mind the following shortcuts.</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li><strong>"~"</strong>&nbsp;represents our personal /home directory, e.g. <strong>cd ~ </strong>and <strong>cd ~/Documents</strong></li><li><strong>".."</strong> represents the parent directory, i.e.
 the directory that contains the one we currently are. If we are at 
/home/test/public and type <strong>cd ..&nbsp;</strong>it will take us to /home/test/</li><li>We can also use the full path to change to a particular directory, e.g.&nbsp;<strong>cd /home/test/public/</strong>. The Tab button can help us every step of the way to autocomplete the directories.</li></ul>
<!-- /wp:list -->

<!-- wp:heading -->
<h2><strong><span style="text-decoration:underline;">See Which Commands You Use the Most</span></strong></h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>How
 do your own Linux terminal habits reflect these commands? If you want a
 definitive answer, it’s actually quite simple to see your personal 
most-used commands, and we can see what they are by using one of the 
commands mentioned above:</p>
<!-- /wp:paragraph -->

<!-- wp:syntaxhighlighter/code -->
<pre class="wp-block-syntaxhighlighter-code brush: plain; notranslate">history | awk '{print $2}' | sort | uniq -c | sort -rn | head -10</pre>
<!-- /wp:syntaxhighlighter/code -->

<!-- wp:paragraph -->
<p>The pipe character (“<strong>|</strong>“)
 takes the output of the command on its left and uses it as input for 
the command on its right. This is basically a chain of commands that 
one-by-one manipulate the output of the <code>history</code> command to count how many times each command is used, then sorts the list, then limits it to the top 10.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Pretty nifty, but loses accuracy every time you clear your Bash cache.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Anyway that's all for today guys. Have a wonderful day.</p>
<!-- /wp:paragraph -->
