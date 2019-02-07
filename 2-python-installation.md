# Python Installation and Creating a Virtual Environment 

There are two versions of Python, Python 2 and Python 3. For this class we will be using Python 3, which you will need to install on your computer. 

## Windows
Follow [this guide](https://docs.python-guide.org/starting/install3/win/).
If you have trouble, install [Anaconda](https://www.anaconda.com/distribution/#windows)


## Mac
### Install Homebrew
Homebrew is what's called a package manager. It allows you to install software via the command line.

Visit [Homebrew's website](https://brew.sh/) and follow the instructions there, or just copy and paste the following into your terminal:

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### Install Python 3

Once Homebrew is done, you can use it to install Python and a number of other extremely useful command line tools.

```bash
brew install python3
```

NOTE: If you think you may already have Python installed, you can run this command to check:

```bash
python --version
```

## Create a Virtual Environment for your Python Project

One of the great things about Python is that it's modular. There's a basic template, Python 2.7 or 3, which you installed, and then there are lots of other pieces that you can add when you need them. These pieces are called packages or dependencies. They're like code libraries that bring you extra functionality and you can install them a la carte. Python stays relatively lightweight and you install what you need. 

The problem with this system is that sometimes the packages conflict with one another. You might have code that you wrote 2 years ago that uses Python 2.7 and code that you wrote yesterday that uses Python 3. If you try to run your 2.7 code in 3, it breaks. 

Ugg. 

The solution is to create a special folder on your hard drive for each Python project. This folder is called a **Virtual Environment**

Your virtual environment contains an isolated copy of Python and the packages that you need for your project. Each project should have its own virtual environment. 

#### If you prefer watching videos to reading instructions, you can follow [this tutorial](https://www.youtube.com/watch?v=nnhjvHYRsmM) to set up virtual environments. 

#### If you prefer following written instructions, read on:

1. Install virtualenv. Virtualenv is a tool to create isolated Python environments. It basically creates a folder that's a copy of your Python installation, with everything you need inside. Then you build your Python project inside that folder. 

You install virtualenv via the command line, with this simple line of code: 

```bash
pip install virtualenv
```
If that gives you an error, make sure you have pip installed (pip is Python's package manager). 

```bash
pip --version
```
2. Test your installation of virtualenv:

```bash
virtualenv --version
```
If that gives you some number (e.g. 16.3.0), that means that you have the software installed. Good job. 

3. cd to your Documents (or Desktop, if you prefer to store your work there), and make a folder to hold the projects that you will do in this class. I'm going to call mine pythonland, but you feel free to come up with a better name. 

```bash
cd Documents
mkdir pythonland
cd pythonland
```
4. Inside pythonland (or your project folder), create a virtual environment, aka a copy of your python installation. I'll call mine first_env. Again, call yours what you want. 
If you don't give it a name and just type virtualenv, it will copy all the python files into the current directory (i.e. pythonland). 

```bash
virtualenv first_env
```
Okay. Now you should see a folder called first_env (or whatever you called yours) that holds a lot of Python files. I hope it worked!

## Activate Your Virtual Environment

Okay. You made a copy of your entire python installation in an isolated environment so you can add different modular pieces to it that conflict with one another. 

The last thing you need to do is activate that environment, AKA turn it on, so you're no longer coding in your defaul installation of python, but you're coding in your special isolated virtual environment. 

5. Navigate to the folder holding your virtual environment:
```
cd Documents/pythonland
```
Type the name of your virtual environment, followed by \Scripts\activate: 
```
first_env\Scripts\activate
```
The computer will run a script to activate your environment and now you should see the name of your virtual environment at the front of your command prompt like this:
```
(first_env) C:\Users\student\Documents\pythonland>
```
Now all the python code you run will use the special installation that you created in that space. When you want to deactivate it, just type `deactivate`
```
(first_env) C:\Users\student\Documents\pythonland>deactivate
```

## Run Python from the command line

Python is a command line application, just like `cat`, `grep` and `sort`.

To execute Python code you run the python command with a text file as an argument.

To start, let's make a simple program that prints a message on the terminal. To do this we will use the print command.

cd to the folder that will hold your python work for this class: 

```bash
cd Documents/pythonland
```

Use the `cat >` or `type nul >` command to create a new file called hello.py put this in it:

```python
cat > hello.py

print("Hello Python, nice to meet you.")
```
`Control D` to save your new file and get back to your $ prompt. 

```
type nul > hello.py
echo print("Hello Python, nice to meet you.") > hello.py
```

Navigate (`cd`) to the directory where the file is saved, and then type:

```
python hello.py
```
You should see "Hello Python, nice to meet you." printed on the screen.

Now add some math to hello.py. Use `cat >>` or `echo >>` to add to the hello.py file

```python
cat >> hello.py

print(1+1)
print(10/2)
print(100 * 6.2 - 70/3.5)
```
```
echo print(1+1) >> hello.py
```

And run the file again:
```
python hello.py
```
Hopefully you see your hello python message and the answers to your math problems.

Editing a text file and running it through the command line is a perfectly good way to use Python, but it would be nice to edit and run these scripts inside your text editor. Keep going to learn how... 


## Add a script extension to your favorite text editor or install an IDE 

Unlike JavaScript, which runs when you load your website into a browser, a python script needs to be told "go". You can install an extension in your editor that will let you run your python code. Or you can use an IDE (integrated development environment), which will usually have something like a play button to run your code. 


* Atom  
  * Install [script](https://atom.io/packages/script)
  * You might also want a Python autocomplete package. [Here's a good one](https://atom.io/packages/autocomplete-python). 
  * While you're installing stuff in Atom, you might play around with themes to color the text and background. I like Atom-Material [syntax](https://atom.io/themes/atom-material-syntax) and [UI](https://atom.io/themes/atom-material-ui). 

* [Visual Studio Code](https://code.visualstudio.com/)
  * Install the [Python Extension for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-python.python), which essentially makes your text editor into an IDE (I think). 
  * or install [CodeRunner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)

* [PyCharm](https://www.jetbrains.com/pycharm/) is a nice IDE. The free community version is good. 

* another is [Anaconda](https://www.anaconda.com/distribution/) which is great for maniging virtual environments, projects jupyter notebooks and more!

Once you have your development environment set up, add your project folder to your editor or IDE (in Atom, go to File --> Add Project Folder). 

Open your hello.py file in the editor. You should see the code that you typed via the command line. Now run the code in your editor or IDE. If you're using the Script package in Atom, you run with `COMMAND i`. 
You should see your output in a console in the bottom of the editor. 

### Congratulations. Take a break. You deserve it. 
