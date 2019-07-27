---
layout: post
title: The Linux Filesystem
date: 2019-06-05 16:15
author: ajulusthoughts
comments: true
categories: [/, Ajulu's Thoughts, bin, boot, dev, etc, filesystem, home, lib, linux, linux commands, linux filesystem, linux laptop, Linux mint, linux terminal, lost+found, misc, mnt, net, proc, root, sbin, TECH &amp; CYBERSECURITY, the filesystem for linux, tmp, usr, var]
---
<!-- wp:paragraph -->
<p> This tutorial will help you get up to speed on the Linux filesystem.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>DIFFERENCES IN THE LINUX AND WINDOWS FILESYSTEM</h3>
<!-- /wp:heading -->

<!-- wp:image {"align":"center","id":1836} -->
<div class="wp-block-image"><figure class="aligncenter"><img src="https://ajulusthoughts.files.wordpress.com/2019/06/windows-file-structure_orig.jpg" alt="" class="wp-image-1836" /><figcaption>WINDOWS FILESYSTEM</figcaption></figure></div>
<!-- /wp:image -->

<!-- wp:spacer -->
<div style="height:100px;" aria-hidden="true" class="wp-block-spacer"></div>
<!-- /wp:spacer -->

<!-- wp:image {"align":"center","id":1837} -->
<div class="wp-block-image"><figure class="aligncenter"><img src="https://ajulusthoughts.files.wordpress.com/2019/06/linux-file-structure_orig.png" alt="" class="wp-image-1837" /><figcaption>LINUX FILESYSTEM</figcaption></figure></div>
<!-- /wp:image -->

<!-- wp:heading {"level":3} -->
<h3>Structure</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>It makes sense to explore the Linux filesystem from a terminal 
window, not because the author is a grumpy old man and resents new kids 
and their pretty graphical tools -- although there is some truth to that
 --&nbsp;but because a terminal, despite being text-only, has better tools to
 show the map of Linux's directory tree.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In fact, that is the name of the first tool you'll install to help you on the way: <em>tree</em>. If you are using Ubuntu or Debian, you can do:</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">sudo apt install tree
</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>On Red Hat or Fedora, do:</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">sudo dnf install tree
</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>For SUSE/openSUSE use <code>zypper</code>:</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">sudo zypper install tree
</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>For Arch-like distros (Manjaro, Antergos, etc.) use:</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">sudo pacman -S tree
</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>... and so on.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Once installed, stay in your terminal window and run <em>tree</em> like this:</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">tree /
</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p><code>The /</code> in the instruction above refers to the <em>root</em> directory. The root directory is the one from which all other directories branch off from. When you run <code>tree</code> and tell it to start with <em>/</em>,  you will see the whole directory tree, all directories and all the  sub directories in the whole system, with all their files, fly by.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>If you have been using your system for some time, this may take a  while, because, even if you haven't generated many files yourself, a  Linux system and its apps are always logging, caching, and storing  temporal files. The number of entries in the file system can grow quite  quickly.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Don't feel overwhelmed, though. Instead, try this:</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">tree -L 1 /
</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>And you should see what is shown in Figure 1.</p>
<!-- /wp:paragraph -->

<!-- wp:image -->
<figure class="wp-block-image"><img src="https://www.linux.com/sites/lcom/files/styles/rendered_file/public/f01_tree01.png?itok=aGKzzC0C" alt="tree" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>The instruction above can be translated as "<em>show me only the 1st Level of the directory tree starting at / (root)</em>". The <em><code>-L</code> </em>option tells <code>tree</code> how many levels down you want to see.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Most Linux distributions will show you the same or a very similar 
layout to what you can see in the image above. This means that even if 
you feel confused now, master this, and you will have a handle on most, 
if not all, Linux installations in the whole wide world.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>To get you started on the road to mastery, let's look at what each 
directory is used for. While we go through each, you can peek at their 
contents using <em>ls</em>.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>Directories</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>From top to bottom, the directories you are seeing are as follows.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4><em>/bin</em></h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><em>/bin</em> is the directory that contains <em>bin</em>aries, that is, some of the applications and programs you can run. You will find the <em>ls</em>
 program mentioned above in this directory, as well as other basic tools
 for making and removing files and directories, moving them around, and 
so on. There are more <em>bin</em> directories in other parts of the file system tree, but we'll be talking about those in a minute.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4><em>/boot</em>&nbsp;</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The <em>/boot</em> directory contains files required for starting your system. Do I have to say this? Okay, I'll say it: <strong>DO NOT TOUCH!</strong>.
 If you mess up one of the files in here, you may not be able to run 
your Linux and it is a pain to repair.&nbsp;On the other hand, don't worry 
too much about destroying your system by accident: you have to have 
superuser privileges to do that.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4><em>/dev</em></h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><em>/dev</em> contains <em>dev</em>ice files. Many of these are generated
 at boot time or even on the fly. For example, if you plug in a new 
webcam or a USB pendrive into your machine, a new device entry will 
automagically pop up here.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4><em>/etc</em>&nbsp;</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><em>/etc</em> is the directory where names start to get confusing. <em>/etc</em>
 gets its name from the earliest Unixes and it was literally "et cetera"
 because it was the dumping ground for system files administrators were 
not sure where else to put.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Nowadays, it would be more appropriate to say that <em>etc</em> stands 
for "Everything to configure,"&nbsp;as it contains most, if not all 
system-wide configuration files. For example, the files that contain the
 name of your system, the users and their passwords, the names of 
machines on your network and when and where the partitions on your hard 
disks should be mounted are all in here. Again, if you are new to Linux,
 it may be best if you don't touch too much in here until you have a 
better understanding of how things work.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4><em>/home</em></h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><em>/home</em> is where you will find your users' personal directories. In my case, under <em>/home</em> there are two directories: <em>/home/paul</em>, which contains all my stuff; and <em>/home/guest</em>, in case anybody needs to borrow my computer.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4><em>/lib</em></h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><em>/lib</em> is where <em>lib</em>raries live. Libraries are files 
containing code that your applications can use. They contain snippets of
 code that applications use to draw windows on your desktop, control 
peripherals, or send files to your hard disk.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>There are more <em>lib</em> directories scattered around the file system, but this one, the one hanging directly off of <em>/</em>
 is special in that, among other things, it contains the all-important 
kernel modules. The kernel modules are drivers that make things like 
your video card, sound card, WiFi, printer, and so on, work.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4><em>/media</em>&nbsp;</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The <em>/media</em> directory is where external storage will be 
automatically mounted when you plug it in and try to access it. As 
opposed to most of the other items on this list, <em>/media</em> does not 
hail back to 1970s, mainly because inserting and detecting storage 
(pendrives, USB hard disks, SD cards, external SSDs, etc) on the fly, 
while a computer is running, is a relatively new thing.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4><em>/mnt</em>&nbsp;</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The&nbsp;<em>/mnt</em>&nbsp;directory, however,&nbsp;is a bit of remnant from days 
gone by. This is where you would manually mount storage devices or 
partitions. It is not used very often nowadays.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>&nbsp;<em>/opt</em>&nbsp;</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The <em>/opt</em> directory is often where software you compile (that 
is, you build yourself from source code and do not install from your 
distribution repositories) sometimes lands. Applications will end up in 
the <em>/opt/bin</em> directory and libraries in the <em>/opt/lib</em> directory.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>A slight digression: another place where applications and libraries end up in is <em>/usr/local</em>, When software gets installed here, there will also be <em>/usr/local/bin</em> and <em>/usr/local/lib</em>
 directories. What determines which software goes where is how the 
developers have configured the files that control the compilation and 
installation process.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4><em>/proc</em></h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><em>/proc</em>, like <em>/dev</em> is a virtual directory. It contains 
information about your computer, such as information about your CPU and 
the kernel your Linux system is running. As with <em>/dev</em>, the files and directories are generated when your computer starts, or on the fly, as your system is running and things change.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4><em>/root</em>&nbsp;</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><em>/root</em> is the home directory of the superuser (also known as 
the "Administrator") of the system. It is separate from the rest of the 
users' home directories BECAUSE YOU ARE NOT MEANT TO TOUCH IT. Keep your
 own stuff in you own directories, people.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4><em>/run</em></h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><em>/run</em> is another new directory. System processes use it to 
store temporary data for their own nefarious reasons. This is another 
one of those DO NOT TOUCH folders.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4><em>/sbin</em></h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><em>/sbin</em> is similar to <em>/bin</em>, but it contains applications that only the superuser (hence the initial <em>s</em>) will need. You can use these applications with the <code>sudo</code> command that temporarily concedes you superuser powers on many distributions. <em>/sbin</em>
 typically contains tools that can install stuff, delete stuff and 
format stuff. As you can imagine, some of these instructions are lethal 
if you use them improperly, so handle with care.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4><em>/usr</em>&nbsp;</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The <em>/usr</em> directory was where users' home directories were originally kept back in the early days of UNIX. However, now <em>/home</em> is where users kept their stuff as we saw above. These days,&nbsp;<em>/usr</em>
 contains a mish-mash of directories which in turn contain applications,
 libraries, documentation, wallpapers, icons and a long list of other 
stuff that need to be shared by applications and services.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>You will also find <em>bin</em>, <em>sbin</em> and <em>lib</em> directories in <em>/usr</em>. What is the difference with their root-hanging cousins? Not much nowadays. Originally, the <em>/bin</em> directory (hanging off of root) would contain very basic commands, like <code>ls</code>, <code>mv</code> and <code>rm</code>;
 the kind of commands that would come pre-installed in all UNIX/Linux 
installations, the bare minimum to run and maintain a system. <em>/usr/bin</em>
 on the other hand would contain stuff the users would install and run 
to use the system as a work station, things like word processors, web 
browsers, and other apps.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>But many modern Linux distributions just put everything into <em>/usr/bin</em> and have <em>/bin</em> point to <em>/usr/bin</em> just in case erasing it completely would break something. So, while Debian, Ubuntu and Mint still keep <em>/bin</em> and <em>/usr/bin</em> (and <em>/sbin</em> and <em>/usr/sbin</em>) separate; others, like Arch and its derivatives just have one "real" directory for binaries, <em>/usr/bin</em>, and the rest or <em>*bin</em>s are "fake" directories that point to <em>/usr/bin</em>.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4><em>/srv</em></h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The <em>/srv</em> directory contains data for servers. If you are 
running a web server from your Linux box, your HTML files for your sites
 would go into <em>/srv/http</em> (or <em>/srv/www</em>). If you were running an FTP server, your files would go into <em>/srv/ftp</em>.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4><em>/sys</em></h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><em>/sys</em> is another virtual directory like <em>/proc</em> and <em>/dev</em> and also contains information from devices connected to your computer.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In some cases you can also manipulate those devices. I can, for 
example, change the brightness of the screen of my laptop by modifying 
the value stored in the <em>/sys/devices/pci0000:00/0000:00:02.0/drm/card1/card1-eDP-1/intel_backlight/brightness</em>
 file (on your machine you will probably have a different file). But to 
do that you have to become superuser. The reason for that is, as with so
 many other virtual directories, messing with the contents and files in <em>/sys</em> can be dangerous and you can trash your system. DO NOT TOUCH until you are sure you know what you are doing.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4><em>/tmp</em></h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><em>/tmp</em> contains temporary files, usually placed there by 
applications that you&nbsp;are running. The files and directories often (not 
always) contain data that an&nbsp;application doesn't need right now, but may
 need later on.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>You can also use<em> /tmp </em>to store your own temporary files --<em> /tmp</em> is one of the&nbsp;few directories hanging off / that you can actually interact with without&nbsp;becoming superuser.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4><em>/var</em></h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><em>/var</em> was originally given its name because its contents was deemed <em>variable</em>,
 in that it changed frequently. Today it is a bit of a misnomer because 
there are many other directories that also contain data that changes 
frequently, especially the virtual directories we saw above.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Be that as it may, <em>/var</em> contains things like logs in the <em>/var/log</em>
 subdirectories. Logs are files that register events that happen on the 
system. If something fails in the kernel, it will be logged in a file in
 <em>/var/log</em>; if someone tries to break into your computer from outside, your firewall will also log the attempt here. It also contains <em>spools</em>
 for tasks. These "tasks" can be the jobs you send to a shared printer 
when you have to wait because another user is printing a long document, 
or mail that is waiting to be delivered to users on the system.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Your system may have some more directories we haven't mentioned above. In the screenshot, for example, there is a <em>/snap</em> directory. That's because the shot was captured on an Ubuntu system. Ubuntu has recently incorporated <a href="https://www.ubuntu.com/desktop/snappy" target="_blank" rel="noreferrer noopener">snap</a> packages as a way of distributing software. The <em>/snap</em> directory contains all the files and the software installed from snaps.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>Digging Deeper</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>That is the root directory covered, but many of the sub directories  lead to their own set of files and sub directories. Figure 2 gives you an  overall idea of what the basic file system tree looks like (the image  is kindly supplied under a CC By-SA license by Paul Gardner) and <a rel="noreferrer noopener" href="https://en.wikipedia.org/wiki/Unix_filesystem#Conventional_directory_layout" target="_blank">Wikipedia has a break down with a summary of what each directory is used for</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:image -->
<figure class="wp-block-image"><img src="https://www.linux.com/sites/lcom/files/styles/rendered_file/public/standard-unix-filesystem-hierarchy.png?itok=CVqmyk6P" alt="filesystem" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>To explore the filesystem yourself, use the <code>cd</code> command:</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">cd 
</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>will take you to the directory of your choice (<em>cd</em> stands for <em>change directory</em>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>If you get confused,</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">pwd</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>will always tell you where you (<em>pwd</em> stands for <em>print working directory</em>). Also,</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">cd
</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>with no options or parameters, will take you back to your own home directory, where things are safe and cosy.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Finally,</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">cd ..
</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>will take you up one level, getting you one level closer to the <em>/</em> root directory. If you are in <em>/usr/share/wallpapers</em> and run <code>cd ..</code>, you will move up to <em>/usr/share</em>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>To see what a directory contains, use</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">ls 
</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>or simply</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">ls
</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>to list the contents of the directory you are in right now.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>And, of course, you always have <code>tree</code> to get an overview of what lays within a directory. Try it on <em>/usr/share</em> -- there is a lot of interesting stuff in there.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>Conclusion</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Although there are minor differences between Linux distributions, the
 layout for their filesystems are mercifully similar. So much so that 
you could say:&nbsp;once you know one, you know them all. And the best way to
 know the filesystem is to explore it. So go forth with <code>tree</code>, <code>ls</code>, and <code>cd</code> into uncharted territory.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>You cannot damage your filesystem just by looking at it, so move from  one directory to another and take a look around. Soon you'll discover  that the Linux filesystem and how it is laid out really makes a lot of  sense, and you will intuitively know where to find apps, documentation,  and other resources.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Keep in mind that the Linux file system is a&nbsp;<em>logical</em>&nbsp;system,  rather than a physical one. Different folders in the system may be on  different partitions on the disk, or even on different disks altogether,  but&nbsp;<em>logically</em>&nbsp;everything is still in the same location. The  best way to grasp this concept is to simply use Linux as your daily  driver, as the best way to learn is through immersion. Ubuntu or Linux  Mint are probably the best choices for this task. After using the Linux  file system for a while,&nbsp;eventually&nbsp;everything will click you’ll  understand what’s going on.<br></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Go check out my previous post on Linux Terminal Commands here: <a href="https://ajulusthoughts.wordpress.com/2019/05/30/basic-linux-commands/">https://ajulusthoughts.wordpress.com/2019/05/30/basic-linux-commands/</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Source: <a href="https://linux.com">Linux.com</a></strong></p>
<!-- /wp:paragraph -->
