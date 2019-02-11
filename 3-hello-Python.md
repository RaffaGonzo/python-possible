## Basics

1. To start, cd to the folder where you have your virtual environment, and activate it:

```
your_env\Scripts\activate
```
This makes sure that you're running the version of python that you've created for this project. 

2. Create a new file called `hello.py` and put this in it:

```python
print("Hello Python, nice to meet you.")
```

3. Run this script in your editor (in Atom, `COMMAND i`), or via the command line `python hello.py`. 

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
It's great at working with data. So, that's where we'll focus. 

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

```python
a_number = 1 				# an integer
another_number = 5.1 		# a float
some_string = "Hello!" 		# a string
some_boolean = True 		# a boolean (notice the capitalization)
a_list = ["a bunch", "of", "stuff", a_number, some_string]
a_dictionary = {"key1": 10, "key2": "a string"} # a dictionary (key/value pairs)
```

In Python you do not need to declare variable types, or even that you are declaring a variable, you simply type a name, the equals sign, and then a value or expression.

8. Create a new variable of each type. For example:
```python
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

```python
sentence = "I do what I like, I do, I do"
print("do" in sentence)
print("boss" in sentence)
```

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


### Reading files

To open a file in Python, use the `open()` keyword function. The function takes two arguments. The first is the name of the file to open, and the second is a flag that states if we are opening the file with the intent of *reading* to it (use "r"), or *writing* to it (use "w").

Once we have opened a file, we use the `read` function to grab it's contents and return then as a string.

In this example, we open a file and store its contents in a string. We then uppercase the entire file and print it to the screen.

```python
content = open("frozen_lyrics.txt", "r").read()
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

## Day 1 Beyond the Basics


We’ll grab Kafka’s Metamorphosis from gutenberg
https://www.gutenberg.org/cache/epub/5200/pg5200.txt

Save it to a file next to our python script

We’ll read the text file and store it as a variable
In our python script:

    
    text = open("kafka.txt").read() # the name of the file, relative to where the script is
    
    print(text) # Outputs: the entire text
    
    

Now we can do stuff with it


    
    print(text.upper())
    


To read every single lines, Instead of read() we use readlines()

    
    text = open("kafka.txt").readlines()
    # text is now a list of string items, with each line from the file
    

Now we can iterate over the lines


    
    for line in text:
      print(line) #Outputs each line
      

The problem, it’s putting a space in between each line.
This is because there’s an extra character after a line break, called a newline character
We can get rid of that with strip()


    
    for line in text:
      line = line.strip()
      print(line) # Outputs each line without whitespace or extra line breaks
      


Each of the lines is a string, so we can print parts of each line


    
    for line in text:
      line = line.strip()
      print(line[0:4])
    
    # Output is the first four characters of each line
    

Or do fun stuff like replacing


    
    for line in text:
      line = line.strip()
      print(line.replace('e', 'eeeeeee'))
      



## Processing text

We’re gonna use a function called split() to break downs a string according to a delimiter character.
You can use split() to return a string as a list separated by a character
You can use join() to join a list back into a string

    
    for line in text:
      line = line.strip()
      words = line.split(" ") # Separates the lines by an empty space, getting a list of words
      
      print(words[0]) # Outputs the first word of each sentence
      
      # Chain it all together!
      print(words[0].center(30, '~').upper())
      


We can use the **random** methods to do interesting stuff

Sometimes you have to tell python to add **modules** with the **import** keyword to add functionality you need. Here we’ll import the [random module](https://docs.python.org/3.5/library/random.html). 

- Use the documentation to find what you can do with a module
- Make sure you’re seeing the documentation of the python version you’re using (e.g. 3.5)
    # Import the module
    import random
    
    text = open("kafka.txt").readlines()
    
    for line in text:
      line = line.strip()
      words = line.split(" ")
      
      random_word = random.choice(words)  #Get a random item from the word list
      
      random.shuffle(words) # Randomizes the order of the items in the list
    


We use the join() method to join the randomized word list in to a string

    
    
    for line in text:
      line = line.strip()
      words = line.split(" ")
      random.shuffle(words)
      
      new_line = " ".join(words) # Joins each element in the list by sticking the space character in between the words, outputs a string
      


We can sort with sorted()


    
    for line in text:
      line = line.strip()
      words = line.split(" ")
      random.shuffle(words)
      
      words = sorted(words) # Sort the words list alphabetically
      
      new_line = " ".join(words)
      


Final script

    # Import the module
    import random
    
    text = open("kafka.txt").readlines()
    for line in text:
      line = line.strip()
      words = line.split(" ")
      random.shuffle(words)
      words = sorted(words)
      new_line = " ".join(words)
      print(new_line)


## List comprehension

Make a new file comps.py


We can make a list of upper case’d items

    names = ["Trotsky", "Marx", "Lenin", "Engels"]
    
    uppercase_names = []
    for name in names:
      uppercase_names.append(name.upper())
    
    

There’s a handier way of doing this in python, called **list comprehension.**
This does the same thing as the example above

    names = ["Trotsky", "Marx", "Lenin", "Engels"]
    
    uppercase_names = [name.upper() for name in names]
    

It’s saying: for every value in the list **names** temporarily store it as a variable **name**, make that upper case and store it in a new list called **uppercase_names**


    
    names = [name.replace('r', 'arrrrr') for name in names]
    

We can filter too, by adding **if statements** inside too:

    
    names = [name for name in names if name[0] == "l"]
    # returns elements inside of the list whose first letter is l
    


We can add this filtering technique to the words in our previous example

    import random
    
    text = open("kafka.txt").readlines()
    for line in text:
      line = line.strip()
      words = line.split(" ")
    
      words = [word for word in words if word.startswith("a")]
    
      new_line = " ".join(words)
        
      print(new_line)
      # prints all the words that start with a  

OR more:

      words = [word for word in words if len(word) > 5
      # all the words that have 5 or more characters in them


      words = [word for word in words if word.endswith("ing")]
      # all the words that end in ing



# Creative Assignment 

Transform a non-poetic text into a poetic text. Take something that exists, do something that transforms it.

- start with any text that's interesting to you: something you're reading in another class, a work of literature, a political speech, music, poetry, twitter, restaurant menu, etc. 

- up to you to determine what’s poetic

- explore word counts if you're interested


Read some file, or if the text is short you can just put that text directly into python as a variable.

If you don’t know what to do try sorting, randomizing, replacing, deleting things. By taking something that exists and using these methods we can reformat it and rework it. You can use whatever is at your disposal. You’re not bound by command line or python, so you can take the output of that text and you’re welcome to format it into something interesting, put it into p5, whatever you want to do.

* If you’re more advanced, you can start to get into using third party libraries to analyze text. Look at [TextBlob](https://textblob.readthedocs.io/en/dev/) and [spaCy](https://github.com/aparrish/rwet/blob/master/nlp-concepts-with-spacy.ipynb). 

* If you’re feeling ambitious, make this program so that it can deal with any text. Make this poetic operation so it can work with any text that you feed it.

# Kinda Mathy assignment
Ever heard of the fibonacci sequence? It's (0, 1, 1, 2, 3, 5, 8, 13, 21...) the way to predict the next number in the pattern is to add the previous two number together. Try to write a program to predict the Nth number in the sequence.

How long does it take to get the 11th number, what about the 24th, or 35th? 

Try and write a faster version of the algorithm. (hint: dictionaries are your friend!)

