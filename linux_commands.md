---


---

<h1 id="commands">Commands</h1>
<p>More commands here : <a href="https://www.geeksforgeeks.org/linux-commands/">GeeksForGeeks Linux Commands</a></p>
<h2 id="basic-commands-">Basic Commands :</h2>
<ul>
<li><code>pwd</code> - It gives us the absolute path, which means the path that starts from the root. The root is the base of the Linux file system. It is denoted by a forward slash( / ).</li>
<li><code>ls</code> - to know what files are in the directory you are in.</li>
<li><code>cd</code> - change directory.  <code>cd ..</code> go to previous directory. <code>cd</code> go to root directory.</li>
<li><code>mkdir</code> - make new directory.</li>
<li><code>rmdir</code> - remove directory. But can remove only an empty directory.</li>
<li><code>rm</code> - used to delete files and directories. <code>rm</code> removes directory and all the files it contains. Use <code>rm -r</code> to remove only the directory.</li>
<li><code>touch</code> - to create a new file. Do mention file extension in name.</li>
<li><code>man</code> - shows manual page for the specific command like <code>man cd</code> shows manula for cd command.</li>
<li><code>--help</code> - add <code>--help</code> after a command to know more about the command.</li>
<li><code>cp</code> - use to copy files through command line. <code>cp &lt;file path&gt; &lt;location where to copy&gt;</code>.</li>
<li><code>mv</code> - use to move files through command line. it is also used to rename files. aka <code>mv &lt;old name&gt; &lt;new name&gt;</code></li>
<li><code>locate</code> - to locate any file in linux system.</li>
</ul>
<h2 id="intermediate-commands-">Intermediate commands :</h2>
<ul>
<li><code>echo</code> - to move some data, usually text into a file. For example, if you want to create a new text file or add to an already made text file, you just need to type in, “<strong>echo hello, my name is alok &gt;&gt; new.txt</strong>”. You do not need to separate the spaces by using the backward slash here, because we put in two triangular brackets when we finish what we need to write.</li>
<li><code>cat</code> - to display the contents of a file. It is usually used to easily view programs.</li>
<li><code>nano</code>,<code>vi</code>,<code>jed</code> - <strong>ano</strong> and <strong>vi</strong> are already installed text editors in the Linux command line. The <strong>nano</strong> command is a good text editor that denotes keywords with color and can recognize most languages. And <strong>vi</strong> is simpler than <strong>nano</strong>. You can create a new file or modify a file using this editor. For example, if you need to make a new file named <strong>"check.txt</strong>", you can create it by using the command “<strong>nano check.txt</strong>”. You can save your files after editing by using the sequence Ctrl+X, then Y (or N for no). In my experience, using <strong>nano</strong> for HTML editing doesn’t seem as good, because of its color, so I recommend <strong>jed</strong> text editor.</li>
<li><code>sudo</code> - <strong>sudo</strong> stands for “SuperUser Do”. So, if you want any command to be done with administrative or root privileges, you can use the <strong>sudo</strong> command.</li>
<li><code>df</code> - to see the available disk space in each of the partitions in your system. You can just type in <strong>df</strong> in the command line and you can see each mounted partition and their used/available space in % and in KBs. If you want it shown in megabytes, you can use the command “<strong>df -m</strong>”.</li>
<li><code>du</code> - to know the disk usage of a file in your system. If you want to know the disk usage for a particular folder or file in Linux, you can type in the command <strong>df</strong> and the name of the folder or file. You can also use the command “<strong>ls -lah</strong>” to view the file sizes of all the files in a folder.</li>
<li><code>tar</code> - to work with tarballs (or files compressed in a tarball archive) in the Linux command line. It has a long list of uses. It can be used to compress and uncompress different types of tar archives like <strong>.tar, .tar.gz, .tar.bz2</strong>,etc. It works on the basis of the arguments given to it. For example, “<strong>tar -cvf</strong>” for creating a <strong>.tar</strong> archive, -<strong>xvf</strong> to untar a tar archive, -<strong>tvf</strong> to list the contents of the archive, etc. Since it is a wide topic, here are some <a href="http://www.tecmint.com/18-tar-command-examples-in-linux/">tar commands example</a>.</li>
<li><code>zip</code>,<code>unzip</code> - Use <strong>zip</strong> to compress files into a zip archive, and <strong>unzip</strong> to extract files from a zip archive.</li>
<li><code>uname</code> - Use <strong>uname</strong> to show the information about the system your Linux distro is running. Using the command “<strong>uname -a</strong>” prints most of the information about the system. This prints the kernel release date, version, processor type, etc.</li>
<li><code>apt-get</code>  - Use <strong>apt</strong> to work with packages in the Linux command line. Use <strong>apt-get</strong> to install packages. This requires root privileges, so use the <strong>sudo</strong> command with it. For example, if you want to install the text editor <strong>jed</strong> (as I mentioned earlier), we can type in the command “<strong>sudo apt-get install jed</strong>”. Similarly, any packages can be installed like this. It is good to update your repository each time you try to install a new package. You can do that by typing “<strong>sudo apt-get update</strong>”. You can upgrade the system by typing “<strong>sudo apt-get upgrade</strong>”. We can also upgrade the distro by typing “<strong>sudo apt-get dist-upgrade</strong>”. The command “<strong>apt-cache search</strong>” is used to search for a package. If you want to search for one, you can type in “<strong>apt-cache search jed</strong>”(this doesn’t require root).</li>
<li><code>chmod</code> - Use <strong>chmod</strong> to make a file executable and to change the permissions granted to it in Linux. Imagine you have a python code named <strong><a href="http://numbers.py">numbers.py</a></strong> in your computer. You’ll need to run “<strong>python <a href="http://numbers.py">numbers.py</a></strong>” every time you need to run it. Instead of that, when you make it executable, you’ll just need to run “<strong><a href="http://numbers.py">numbers.py</a></strong>” in the terminal to run the file. To make a file executable, you can use the command “<strong>chmod +x <a href="http://numbers.py">numbers.py</a></strong>” in this case. You can use “<strong>chmod 755 <a href="http://numbers.py">numbers.py</a></strong>” to give it root permissions or “<strong>sudo chmod +x <a href="http://numbers.py">numbers.py</a></strong>” for root executable. Here is some more <a href="http://www.computerhope.com/unix/uchmod.htm">information about the chmod command</a>.</li>
<li><code>hostname</code> - Use <strong>hostname</strong> to know your name in your host or network. Basically, it displays your hostname and IP address. Just typing “<strong>hostname</strong>” gives the output. Typing in “<strong>hostname -I</strong>” gives you your IP address in your network.</li>
<li><code>ping</code>  -to check your connection to a server.</li>
</ul>
<h3 id="tricks-">TRICKS :</h3>
<ul>
<li>
<p>You can use the  <strong>clear</strong>  command to clear the terminal if it gets filled up with too many commands.</p>
</li>
<li>
<p><strong>TAB</strong>  can be used to fill up in terminal. For example, You just need to type “<strong>cd Doc</strong>” and then  <strong>TAB</strong>  and the terminal fills the rest up and makes it “<strong>cd Documents</strong>”.</p>
</li>
<li>
<p><strong>Ctrl+C</strong>  can be used to stop any command in terminal safely. If it doesn’t stop with that, then  <strong>Ctrl+Z</strong>  can be used to force stop it.</p>
</li>
<li>
<p>You can exit from the terminal by using the  <strong>exit</strong>  command.</p>
</li>
<li>
<p>You can power off or reboot the computer by using the command  <strong>sudo halt</strong>  and  <strong>sudo reboot</strong>.</p>
</li>
</ul>

