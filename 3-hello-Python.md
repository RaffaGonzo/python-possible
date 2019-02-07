## Basics

1. To start, add your Virtual Environment folder to your text editor. So, in Atom, go to File --> Add Project Folder, and choose your Virtual Environment. This is where you'll build your project, and it also holds your Python installation and all your dependencies (like libraries). 

2. In that folder, create a new file called `hello.py` and put this in it:

```python
print("Hello Python, nice to meet you.")
```

3. Run this script in your editor (in Atom, `COMMAND i`). 

You should see "Hello Python, nice to meet you." printed on the screen.

### Expressions

An "expression" is a set of instructions for the computer to execute. Python will read or evaluate your expressions and return a result. For example you can add numbers.

4. Add these numbers and print the results: 

```python
print(1+1)
print(10/2)
print(100 * 6.2 - 70/3.5)
```
You can also test to see how different expressions relate to each other. 

`==` tests for equality  
`<` less than  
`>` greater than  
`<=` less than or equal  
`>=` greater than or equal  

```python
print(1 == 1)
print(1 == 2)
print(1 < 2)
print(5 * 20 >= 100/13)
```
All of these expressions will evaluate to either a `True` or a `False`

5. Try evaluating a few of your own expressions. Check if 1 == 2, etc.  

## Python is sort of like a monster calculator. 
It's great at working with data. So, that's where we'll start. 

### Variables

You can store the value of expressions inside named variables using the `=` symbol. Notice that you don't need any semi-colons. Hooray. 

```python
x = 2
y = 5
z = x + y
print(x * 100)
print(z)
```

6. Store your name as a variable and print it. 
7. Add the ages of everyone at your table and print the total. 

#### Types

Values stored in variables (all values actually) have different "types" or categories. 
For example, 1 is an integer, 1.5 is a float, and "hello" is a string.

You can see what type a value is is by using the `type` function:

```python
print(type(1))
```

Some important types are:

```python			# DATA_TYPE
a_number = 1 			# an integer
another_number = 5.1 		# a float
some_string = "Hello!" 		# a string
some_boolean = True 		# a boolean (notice the capitalization)
a_list = ["a bunch", "of", "stuff", a_number, some_string, 9, True] # list
a_2d_list = [['list'],['of', 'lists']]
a_dictionary = {"key1": 10, "key2": "a string"} # a dictionary {key:value_pairs} # dictionary
```

In Python you do not need to declare variable types, or even that you are declaring a variable, you simply type a name, the equals sign, and then a value or expression.

8. Create a new variable of each type. For example:
```python			# DATA_TYPE
people_at_table = 4	        # an integer
sandwiches_I_ate = 1.5 		# a float
best_friend = "Abbas" 		# a string
is_raining = False 		# a boolean (notice the capitalization)

print(people_at_table)
```

9. Create a list. This is a lot like an array in JavaScript.

```
colors = ["blue", "pink", "turquoise", "sand"]
dark_blue = [10, 27, 56]
random_info = [people_at_table, sandwiches_I_ate, best_friend, is_raining]
```

10. Print some stuff from the list.
```
print(colors[2])
print(dark_blue[0])
print(random_info[-1])
```
Did you notice that you can check the last element in the list by scrolling around from the back with -1? Yup! That's awesome. 

### Strings

Strings are a variable type that stores text. To create a string, surround some text within quotation marks. It doesn't matter if you use single or double quotes as long as you are consistent.

11. Create a string with someone's name. 

```python
first_name = "Cardi"
last_name = 'B'

print(first_name)
print(last_name)
```
If you add two or more strings together, Python will combine a new string for you.

12. Add those strings: 

```python
first_name = "Cardi"
last_name = 'B'

print(first_name + last_name)

print(first_name + " " + last_name)
```
Notice that you can add a space by putting quotes around an empty space. 

-----
#### Speaking of space, let's get rid of all the code you wrote so far. Highlight everything in your file and delete it. From now on, delete each code snippet before typing a new one. That way you don't get a million lines of repetitive code.

#### Also, in case you haven't noticed, Python code is a lot closer to English than other languages you might have used. Instead of copying and pasting, you should be typing your code out by hand. It's a better way! 

Moving on... 

-----

Each character in a string is indexed numerically, and can access individual characters using `[]` square brackets. 

13. Print the first and second letters of your person's name: 

```python
name = "Cardi B"
first_letter = name[0]
print(first_letter)

second_letter = name[1]
print(second_letter)
```

The character index begins with the number 0. If you wish to access the last character, you use `-1`. The second to last, `-2` and so on.

14. Get the last letter of your person's name: 

```python
name = "Cardi B"
last_letter = name[-1]
print(last_letter)
```

You can also get a range of characters in a string by entering a starting and ending index in your square brackets:

15. Get the first three letters of your person's name (feel free to use a different person if you're getting bored): 

```python
name = "Cardi B"
first_three_letters = name[0:3]
print(first_three_letters)
```

To get the total length of a string, use the `len()` function.

16. Try it. How long is a word you're curious about?

```python
print(len("California"))
```

You can also determine if a string exists within another string with the `in` keyword.

17. Check to see if a word is inside a song lyric (obviously this will become more powerful when you aren't writing the lyric out by hand, but be patient with this learning process):

```# python
sentence = "I do what I like, I do, I do"
print("do" in sentence)
print("boss" in sentence)
```

you can reverse the list order, (or string or some other itterable).

18. here check it out

```python
my_list = list(range(5)) # everything is an object so you can do this! (almost always)
print(my_list)
my_list = my_list[::-1] # casual variable reset
print(my_list)

#### String methods

Python has a lot of powerful tools for messing with text. We are going to spend time here, so let's dive into what we can do with strings. 

18. Make a string uppercase:

```python
sentence = "Now here's a little story I've got to tell About three bad brothers you know so well!"
uppercase = sentence.upper()
print(uppercase)
```

19. Choose a lyric that you want to play with and do these things to it: 

```python
sentence = "   I STILL SEE YOUR SHADOWS IN MY ROOM   "

# make it uppercase
lowercase_sentence = sentence.lower()

# make it title case
titlecase_sentence = sentence.title()

# remove white space at the start and end
stripped = sentence.strip()

# replace one set of characters with another
less_poetic_sentence = sentence.replace("SHADOWS", "SWEATSHIRT")
```
20. Print those results if you haven't already: 

```
print(lowercase_sentence)
print(titlecase_sentence)
print(stripped)
print(less_poetic_sentence)
```

Here's a full list of things you can do to strings: [https://docs.python.org/3.7/library/stdtypes.html#string-methods](https://docs.python.org/3.7/library/stdtypes.html#string-methods)

### Lists

A list is a numerically ordered collection of values, also known as an array.

21. Make an empty list: 

```python
# make an empty list
dreams = []
```

22. Add something to the list: 

```
# add something to our list with the "append" method
dreams.append("flying dream") # the list will now look like this: ["flying dream"]
```

23. Add more things to the list: 

```
# add some more stuff
dreams.append("forgot something")
dreams.append("saw a friend from a long time ago")
dreams.append(100)
dreams.append("whatever")
```

24. Print that to make sure it looks right: 
```
print(dreams)
# ['flying dream', 'forgot something', 'saw a friend from a long time ago', 100, 'whatever']
```

25. Do all this stuff to your list: 
```
# get the length of a list
len(dreams)

# you can access individual items in the list by referrring to their index value
print dreams[0] # prints "flying dream"
print dreams[2] # prints "saw a friend from a long time ago"

# use negative numbers to start at the back
print dreams[-1] # prints whatever - the last item

# you can access part of a list with a ":"
print(dreams[1:4])
```

You can iterate through every value in a list with the `for` keyword:

```python
for item in my_list:
	print(item)
```
A normal for loop in JavaScript looks something like this:

```javascript
for (var i = 0; i < 3; i++) {
    print(i); 
  }
```  
  
In Python, it has a different structure, but it does the same thing:

```python
for x in range(0, 3):
  print(x)

```    
# fun fact
you dont have to print everything if your in the python terminal! Whatever the function returns will show up if you don't set it to a variable.

### Reading files

To open a file in Python, use the `open()` keyword function. The function takes two arguments. The first is the name of the file to open, and the second is a flag that states if we are opening the file with the intent of *reading* to it (use "r"), or *writing* to it (use "w").

Once we have opened a file, we use the `read` function to grab it's contents and return then as a string.

In this example, we open a file and store its contents in a string. We then uppercase the entire file and print it to the screen.

```python
content = open("frozen_lyrics.txt", "r").read() # these are quotes bc they go to the cmd
loud_frozen = content.upper()
print(loud_frozen)
```

You can also store a file as a list of lines using `readlines()` instead of `read()`

This example prints the first 5 characters of a text file.

```python
all_lines = open("frozen_lyrics.txt", "r").readlines()
for line in all_lines:
	print(line[0:5])
```

