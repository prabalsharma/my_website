# Git and GitHub: Configuration  
[.bashrc](http://www.joshstaiger.org/archives/2005/07/bash_profile_vs.html) | [Settings the PS1](http://www.tldp.org/HOWTO/Bash-Prompt-HOWTO/setps.html) |  
Global and Local settings allow us to customize particular
repositories.  

List all settings  
```bash
git config --list
```  
To view your global settings for many tools can be found in your system's home directory. The following commands in a bash terminal will perform the same thing.   
```bash
vim ~/.gitconfig
vim $HOME/.gitconfig
```  
Dotfiles are files beginning with a dot (.), which are 'hidden files' and are generally used for customizing settings.  
  
We use terminal a lot when developing. Bash (the Bourne Again Shell) is a shell we use in the
terminal, and a [scripting language](http://www.ibm.com/developerworks/library/l-bash/) (like Ruby). There are [alternative shells](http://www.interworx.com/community/alternative-shells-for-linux/), such as zsh, ksh.  
  
Mac OS X runs its Terminal.app a little differently from most other GUI
terminals, and a [recommended
setting](http://www.joshstaiger.org/archives/2005/07/bash_profile_vs.html) for your .bash_profile is to add
the following  
```bash
if [ -f ~/.bashrc ]; then
   source ~/.bashrc
fi
```  
This script is pretty easy to undertand, and basically says "If there is
a file in the home directory .bashrc, then use it as the source."  
  
There are some intended [differences between .bashrc and
.bash_profile](http://superuser.com/questions/183870/difference-between-bashrc-and-bash-profile),
however for the scope of this course, we will only be using the .bashrc
file for setting alsiases, setting up our default editors, and system
output colors, etc.  
  
## Setting the PS1  
We can customize the command prompt in Bash using PS1="something". To
see the current code behind your prompt, try `echo $PS1`.  
  
You can make your command prompt look different for the current session
with `PS1="Hello: "`. We can set up our command line to give more
[meaningful
information](http://www.thegeekstuff.com/2008/09/bash-shell-ps1-10-examples-to-make-your-linux-prompt-like-angelina-jolie/). For example, if we wish to show the current git branch we are on, and its status, we can use a script like this. 

