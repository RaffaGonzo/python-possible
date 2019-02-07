#  - The Command Line -

The command line is a text-based interface for interacting with your computer. From the command line you can launch programs, view files, and manipulate your file system by making, moving, and copying files and directories. You can think of it as the Finder in Mac, without the graphic interface, but much more powerful.

## Setup

On a Mac you can access the command line by opening up the `Terminal` application, located in `/Applications/Utilities/Terminal`

On Windows, you can access the command line by typing `Win r`.
You should then check which version of Windows you're running by typing `winver` (stands for windows version) and push enter. 
The commands listed here work for most versions, but Windows does vary slightly version by version, so look things up if they don't work. 

On Windows 10, you have the option to set up the Windows Subsystem for Linux, which allows you to run Ubuntu (a Linux distribution) from within your current Windows 10 installation.  [Follow this guide to do so](https://tutorials.ubuntu.com/tutorial/tutorial-ubuntu-on-windows).


## The Prompt

When you open up your terminal application you'll see something like this:

```bash
LizzysComputer:~ lizzy$
```

This is called the "prompt". By default (on a Mac) it shows the name of the computer, the directory that you are currently in, your username, and then a $ sign.

On Windows, it looks similar. It shows the path and the user, follwed by `>`

```
C:\\Users\student>
```

The basic use of the command line is: 1) you type a command, 2) you hit return, and 3) some output of the command is printed to the screen.

## Basic Navigation & File Operations

Make the computer say hi to you. 

```
echo hi
```
No, actually make the computer say hi. (Make sure your speakers are on for this one). This one doesn't work natively on Windows, sorry. 

```
say hi your name! how are you doing today? 

```

There some [other voices available (but they are limited)](https://gohgarry.wordpress.com/2010/01/16/fun-with-mac-say-command/). May need to enable them at System Preferences --> Accessibility --> Speech. Specify them like this: 

```
say -v Karen hello

```
Okay. Enough of that. 
Navigate to a directory (aka folder) on your computer. You may have done this before. (cd stands for change directory).

```
cd [drag and drop your folder here or type the path] 
```
# The ```/[directory name]/``` that you see is how the computer knows where one directory name starts and ends. Stringing them together lets you map out the path you want the computer to follow. This notation is also used inside most programming lanquages.

List contents of current directory 

MAC:
```
ls 
```
# and if you want to see: hidden files and directorys add ```-a``` or the the permissions on the file ```-l```

WINDOWS:
```
dir
```

Show name of current directory and full path. 
###### Path means the route that your computer will take to reach a particular file. To the computer, this is a "string" of text that it will follow to find your file. 
###### Fun fact: pwd stands for print working directory and will return the full path to it.

MAC
```
pwd
```
WINDOWS: plain old `cd` will print your working directory. 

Go back one

```
cd ..
```
# this is technically another directory so you could for example ```cd ../[some directory]```

MAC
If you type `cd` without a folder name after, it takes you back to your home folder and if you type `cd /` it takes you to the root directory.
```
cd
```
WINDOWS
If you type `cd\` without a folder name after, it takes you back to your home folder.
```
cd\
```

Now go to desktop

```
cd Desktop
```


**`mkdir`** stands for "make directory". In this context, director = folder. Type `mkdir` and then a name to make a folder. For example, make a folder called "cool_project":

```bash
mkdir cool_project
```

Get yourself into cool_project:
```bash
cd desktop/cool_project
```

on MAC
**`cat`** stands for "concatenate" and it shows you the contents of a file. 
```bash
cat frozenlyrics.txt
```
on WINDOWS
**`type`** shows you the contents of a file. 
```bash
type frozenlyrics.txt
```

Maybe you don't have a file called frozenlyrics.txt inside your cool_project folder. Don't worry. 

on MAC
You can use **`cat >`** to make one. Call it whatever you want. 
```
cat > frozenlyrics.txt
```
When you push enter this time, you don't go back to the prompt. You get a cursor. You can now add text to your file.
Type some song lyrics that you like, or write down what you ate for breakfast.

```
The snow glows white on the mountain tonight
Not a footprint to be seen
A kingdom of isolation,
And it looks like I'm the queen.

I didn't get to eat breakfast today :(
```
Now get out of there and save your file. 

```
CONTROL D. 
```

on WINDOWS
You can use **`type nul >`** to make a new file. Call it whatever you want. 
```
type nul > frozenlyrics.txt
```
Use the echo command and save it to your text file:
```
echo The snow glows white on the mountain tonight > frozenlyrics.txt
```

Check to see if your file is there. 

Mac: Open your file using the default application
```
open FILENAME
```
Windows: `cd` into your folder and type your filename. Push `ENTER`.

Open the current directory in the Finder (mac only)
(the ```.``` means "here")

```
open .
```

Print the contents of a file to the screen
MAC
```
cat FILENAME
```
WINDOWS
```
type FILENAME
```

Say the contents of the file (Mac only)

```
cat frozenlyrics.txt | say -v Karen
```

Maybe you just remembered some more lyrics that you need to add. `cat >>` (mac) or `echo >>` (windows) will append or add text to the end of your file.
MAC
```
cat >>frozenlyrics.txt

The wind is howling like this swirling storm inside
Couldn't keep it in, heaven knows I've tried
```
WINDOWS
```
echo The wind is howling like this swirling storm inside >> frozenlyrics.txt
```

Move your file around: On Mac **`mv`** stands for "move". On Windows it's just `move`. It lets you move files and folders. 
```
mv frozenlyrics.txt Documents\frozenlyrics.txt
```
```
move frozenlyrics.txt Documents\frozenlyrics.txt
```

On Mac, `mv` can also rename a file int the same folder: 

```bash
mv frozenlyrics.txt Frozen_Lyrics.txt
```
On Windows, use `ren` to rename:
```
ren frozenlyrics.txt Frozen_Lyrics.txt
```

On Mac, **`cp`** stands for "copy". On Windows, `copy` is "copy". It lets you duplicate files. Make a copy of your file. 

```bash
cp Frozen_Lyrics.txt Frozen_Lyrics2.txt
```
```bash
copy Frozen_Lyrics.txt Frozen_Lyrics2.txt
```

MAC: **`touch`** will make a new empty file. 

```bash
touch nothinginhere.txt
```
WINDOWS: You already did that. It's **`type nul`**

**`sort`** sorts a file alphabetically by line and prints the output to the screen

```bash
sort names.txt

sort LucidDreams.txt
```
Do you like that? Maybe you want to save it to a new file. `>` will create a file if it does not already exist, or overwrite one if it does. You can use `>>` instead to append to a file. 

```bash
sort LucidDreams.txt > remixedLucidDreams.txt

```

SEARCH A FILE
MAC: **`grep`** searches each line of a file for some input, and prints those lines to the screen. For example, the following searches for all lines in LucidDreams containing the word "heart".

```bash
grep "search term" FILENAME

grep heart LucidDreams.txt
```
WINDOWS: **`findstr`** searches each line of a file for some input, and prints those lines to the screen. For example, the following searches for all lines in LucidDreams containing the word "heart".

```bash
findstr "search term" FILENAME

findstr heart LucidDreams.txt
```

You may really need to hear this out loud (mac only): 

```
grep "search term" FILENAME | say -v Voice

grep "heart" LucidDreams.txt | say -v Ralph
```

Unix has a very powerful concept called "pipes" which allow us to chain commands together, effectively feeding the output of one command into the input of another. To do so, we use the `|` symbol.

Extract all lines of Lucid Dreams containing "heart", then sort them.

```bash
grep heart LucidDreams.txt | sort -u
```

The `|` here means "take the output of the grep command and send it to sort -u". You can use as many pipes as you desire, and combine this technique with the output redirection.

Extract all lines of Lucid Dreams containing "heart", then sort them, then save to a new file called "remixed_dreams.txt"

```bash
grep heart LucidDreams.txt | sort -u > remixed_dreams.txt
```

Is it becoming too much??
On Mac **`rm`** stands for "remove". It lets you delete files:

```bash
rm bad_selfie.jpg
```
On Windows it's **`del`**
```
del bad_selfie.jpg
```

Please note, `rm` and `del` will **not** ask for confirmation, and will not move files to the trash. It'll just delete them immediately, so be careful.


**`more`** is like `cat` but will paginate the output if it is larger than the size of your terminal window:

```bash
more mobydick.txt
```
(now use the up and down arrows to go up or down by a line, the space to go down by a page and `q` to exit if needed)

**`file`** provides basic info about a file (mac only):

```bash
file mysteryfile.what
```

## Command Line Options and Getting Help

Most commands have extra options that you can input when you run the command.  They are usually preceded by either one or two dashes (`-` or `--`). 

The structure of a typical command looks like this:

```bash
command_name [options] arguments
```

("arguments" refers to the file or files your are running the command with)

For example, the `sort` command outputs in ascending order by default, but you can have it use reverse order with the `-r` option on Mac or `/r` on Windows, like so:

```bash
sort -r LucidDreams.txt
```
```bash
sort /r LucidDreams.txt
```

You can also tell `sort` to only output unique lines (ie, to remove any duplicate lines) with the `-u` option (mac only):

```bash
sort -u LucidDreams.txt
```

Finally you can combine options:

```bash
sort -u -r LucidDreams.txt
```
Mac has more built-in sort options. You can see what Windows does [here](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/sort)

Sometimes, options have parameters. For example, the `cut` command cuts out portions of each line of a file. To use it you must specify a delimiter character with the `-d` option and field number to extract with the `-f` option.  To get the first word of every line in Lucid Dreams I might enter:

```bash
cut -d " " -f 1 LucidDreams.txt
```

To see all the options and view a manual for any command, on Mac: use the `man` tool (short for "manual"), on Windows, `help`.
Use the arrow keys to navigate, and `q` to exit.
```bash
man cut
```
`cut` doesn't exist in the Windows command line, so let's look at `find`
```bash
man cut
```

## The Structure of the Filesytem

Everything on your computer is either a file or a folder, and these files and folders are organized hierarchically, like a tree. At the very bottom of the tree is the "root folder", indicated by a single forward slash, like so `/`. Here's a basic example of directory structure:

```
/
	Users/
  		lizzy/
   			Desktop/
	  			sunshine.jpg
	  			lovewilltearyouapart.txt
	 		Documents/
	 		Downloads/			
		Guest/
	Applications/
	Volumes/
```

Each file and folder has a unique location on the filesystem. This location is called a "path". You can reference files and folders either by their **relative** path, or by their **absolute** or **full** path. In the previous examples I have been using the relative path - that is, I have been referencing files relative to where I currently am. **A path is absolute if it begins with a `/`**

For example the absolute path to `lovewilltearyouapart.txt` in the above filesystem is `/Users/lizzy/Desktop/lovewilltearyouapart.txt`. I can look inside the contents of this file, from any working directory, with this command:

```bash
more /Users/lizzy/Desktop/lovewilltearyouapart.txt
```

On Mac, there are a few shortcuts for dealing paths as well.

`.` (single dot) or './' (single dot with slash) means the current folder that I am in.

`..` (two dots) or `../` (two dots with slash) means the parent folder. For example, if am in my Desktop folder and I want to list the contents of my Downloads folder I could type:
MAC
```bash
ls ../Downloads/
``` 

## Wildcards

On Mac, it's also possible to reference multiple files using the `*` character in combination with other characters. This can be really useful in a lot of situations.

For example, can list all files that begin with the word "the" like so:

```bash
ls the*
```

List all jpg images:

```bash
ls *.jpg
```

Make a folder called `images` and move all jpeg images into it:

```bash
mkdir images
mv *.jpg images/
```


## Tips

It can take a while to get used to the command line, but there are a few tips and trick that make it much easier to use.

* Use the up and down arrows to view a history of the commands you have entered. 
* Hit the tab key to autocomplete commands and file paths
* Type `open` and then a filename to open the file in its default program
* Drag a folder or file onto the terminal to fill in its absolute path
* Type ctrl-a to move your cursor to the beginning of the line, and ctrl-e to the end

## Further fun

There are lots of programs that you can run through the command line interface, so feel free to explore and try things out.

There's a software called youtube-gl that allows you to download any video from youtube.You can use that in combination with a command line video editor called ffmpeg to do some really cool stuff. [Here's a tutorial to get you started with that.](https://github.com/antiboredom/automating-video-itp/blob/master/FFMPEG.md)

Congratulations on your new knowledge. Remember, it's just the beginning. If you want to explore more of what the command line can do, [here is a good, thorough tutorial](https://www.learnenough.com/command-line-tutorial/basics). 
