# Onboarding
Welcome to the PhD program!
Here are a few resources that you will hopefully find useful.
Note, most of the help guides are geared towards Linux.

* TODO: add links to learning modules

# Table of Contents
1. [General Info](#general-info)
2. [High Performance Computing](#hpc)
3. [Linux](#linux)
   1. [Linux Basics](#linux-basics)
   2. [Git Repository](#git-repo)
   3. [Installing Linux on Windows (WSL)](#wsl)

# General Info<a name="general-info"></a>
 * Cranfield's interal website with general information is
   [intranet.cranfield.ac.uk](intranet.cranfield.ac.uk)
 * [Printing](https://cranfield-cces.github.io/printing)
<!---  * add link to comp hardware -->
  * [PowerPoint Templates](https://intranet.cranfield.ac.uk/CranfieldBrand/Pages/PowerPoint-templates.aspx)

# High Performance Computing<a name="hpc"></a>
Cranfield's supercomputer for researchers is Delta.
Before accessing it you will need to fill and submit this
  [form](https://intranet.cranfield.ac.uk/it/Documents3/DeltaApplication.pdf)
  to IT.
The official documentation can be found
  [here](https://intranet.cranfield.ac.uk/it/Documents3/Getting%20Started%20With%20HPC.pdf).


You can access the filesystem by using a GUI with
[WinSCP](https://intranet.cranfield.ac.uk/it/Documents3/WindowsHPCSCP.pdf),
 [mobaXterm](https://intranet.cranfield.ac.uk/it/Documents3/WindowsMobaXterm.pdf),
 or from the command line using `ssh`.


Hint: stick this command, where s000000 is your student number, in a
  [bash script](https://github.com/Cranfield-CCES/cranfield-cces.github.io/blob/master/delta.sh)
  to make accessing the system easier.
``` bash
ssh -t s000000@hpcgate.cranfield.ac.uk ssh s000000@delta.central.cranfield.ac.uk
```

Use `module load [package name]` or `ml [package name]` to load the software you want to use.
Type `ml` to list the loaded packages.
The module system is nice because it allows you to easily load and manage the software you want to use.



# Linux
Linux is used on HPC systems and by many scientists, it is very useful to get comfortable with it.
Luckily Linux has been integrated into Windows, there is no more need to dual boot.

## Linux Basics<a name="linux-basics"></a>
 * [A Quick Guide to Get Started with the Linux Command Line](https://www.makeuseof.com/tag/using-linux-with-wayland/) or [UNIX Tutorial for Beginners](http://www.ee.surrey.ac.uk/Teaching/Unix/)
     * Make sure you understand `mv`, `cp`, `cd`, `mkdir`, and `wget`.
     * Note: `cd -` takes you to previous directory
 * [Compiling and Running a Program](https://cranfield-cces.github.io/compile)
 * Install packages using [sudo apt](https://codeburst.io/a-beginners-guide-to-using-apt-get-commands-in-linux-ubuntu-d5f102a56fc4)
   (note: that this will not work on Delta, only systems where you have `sudo` privileges)
   or a [tarball](https://linuxize.com/post/how-to-extract-unzip-tar-gz-file/).
   The tarballs will probably use [cmake](https://preshing.com/20170511/how-to-build-a-cmake-based-project/#running-cmake-from-the-command-line)
   or [configure, make, make install](https://thoughtbot.com/blog/the-magic-behind-configure-make-make-install).
 * [Environment Modules](http://www.admin-magazine.com/HPC/Articles/Environment-Modules): these are used on Delta.
   Note that instead of typing `module load` you can just use `ml`.
 * [Makefiles](https://makefiletutorial.com/)
 * [Installing Latex](https://linuxconfig.org/how-to-install-latex-on-ubuntu-18-04-bionic-beaver-linux)
 * [Running Bash Scripts as Executables](https://www.cyberciti.biz/faq/run-execute-sh-shell-script/)
 * Tab Complition: Note, when typing in the command line, if you hit `tab` it will try to auto-complete.
   If there are multiple items it can complete to, hitting `tab` twice will list all of them.
 * [Turn off beeping](https://www.tldp.org/HOWTO/Visual-Bell-8.html) in Linux


## Git Repository<a name="git-repo"></a>
 * Understand how to use Git with this [Hello World](https://guides.github.com/activities/hello-world/)

## Accessing Linux from Windows<a name="wsl"></a>
 1. [Install](https://docs.microsoft.com/en-us/windows/wsl/install-win10) Windows Subsystem Linux (WSL).
    This will give you access to the Command Line Interface (CLI) of a Linux Distro.
    Ubuntu is the most used and probably the best tested, it's the one I would recommend.
 2. [Install](https://code.visualstudio.com/download) Visual Studio Code
 3. Open WSL and enter `code .` or `code fileToEdit.cpp`.
    This will open VS Code that is integrated with WSL, allowing you to use the Linux CLI from inside VS Code.
 4. [Install](https://sourceforge.net/projects/xming/) Xming and add `export DISPLAY=:0` to your `.bashrc` file.
    Here is more info about [.bashrc](https://www.maketecheasier.com/what-is-bashrc/).
 5. It is helpful to [learn Emacs](http://ergoemacs.org/emacs/emacs_basics.html) or [learn Vim](https://danielmiessler.com/study/vim/).
    Both are text editors that can be used from the command line.
    It's a great thing when you figure out how to do everything using your keyboard, it takes so long to reach out and use the mouse ;)
    You can get extension is VS Code that will allow you to use key-bindings for either of these.
    I prefer Emacs, it is crazy powerful, but just an fyi there is a never ending battle between Emacs people and Vim people.
    You should learn a bit of both since each ones key binding show-up all over the place.

### WSL Miscellaneous
 * Access to C drive from WSL, in this case user Bill Murray is accessing his Download directory:
 ```
 /mnt/c/Users/BillMurray/Downloads/
 ```
 * [An In-depth tutorial about Linux development on Windows with WSL and VS Code](https://devblogs.microsoft.com/commandline/an-in-depth-tutorial-on-linux-development-on-windows-with-wsl-and-visual-studio-code/)
