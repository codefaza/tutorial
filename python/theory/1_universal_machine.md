## Universal Machine:

A **modern computer** might be defined as “a machine that stores and manipulates information under the con-
trol of a changeable program.”

A **computer program** is a detailed, step-by-step set of instructions telling a computer exactly what to do.

The fundamental question of computer science is simply: **What can be computed?** Computer scientists use numerous techniques of investigation to answer this question. The three main ones are design, analysis, and experimentation.

One way to demonstrate that a particular problem can be solved is to actually design a solution. That is,
we develop a step-by-step process for achieving the desired result. Computer scientists call this an **algorithm**.
That’s a fancy word that basically means “recipe.” The design of algorithms is one of the most important
facets of computer science.

In fact, programmers often refer to their programs as **computer code**, and the process of writing an algorithm
in a programming language is called **coding**.

Python, C++, Java, Perl, Scheme, or BASIC.All of the languages mentioned above are examples of **high-level** computer languages. Although they are
precise, they are designed to be used and understood by humans. Strictly speaking, computer hardware can
only understand very **low-level** language known as machine language.

## First Python Program

Let’s illustrate the use of a module file by writing and running a complete program. Our program will
illustrate a mathematical concept known as chaos. Here is the program as we would type it into Idle or some
other editor and save in a module file:

```
# File: chaos.py
# A simple program illustrating chaotic behavior.
def main():
print "This program illustrates a chaotic function"
x = input("Enter a number between 0 and 1: ")
for i in range(10):
x = 3.9 * x * (1 - x)
print x
main()
```
This file should be saved with with the name chaos.py. The .py extension indicates that this is a
Python module. You can see that this particular example contains lines to define a new function called main.
(Programs are often placed in a function called main.) The last line of the file is the command to invoke
this function.

One method that should always work is to start the Python interpreter and then import the file. Here is
how that looks.

```
>>> import chaos
This program illustrates a chaotic function
```
Typing the first line import chaos tells the Python interpreter to load the chaos module from the file
chaos.py into main memory. Notice that I did not include the .py extension on the import line; Python
assumes the module will have a .py extension.

As Python imports the module file, each line executes. It’s just as if we had typed them one-by-one at the
interactive Python prompt. The def in the module causes Python to create the main function. When Python
encounters the last line of the module, the main function is invoked, thus running our program.

When you first import a module file in this way, Python creates a companion file with a .pyc extension.
In this example, Python creates another file on the disk called chaos.pyc. This is an intermediate file used
by the Python interpreter. Technically, Python uses a hybrid compiling/interpreting process. The Python
source in the module file is compiled into more primitive instructions called byte code. This byte code (the
.pyc) file is then interpreted. Having a .pyc file available makes importing a module faster the second time
around. However, you may delete the byte code files if you wish to save disk space; Python will automatically
re-create them as needed.

A module only needsto be imported into a session once. After the module has been loaded, we can run the
program again by asking Python to execute the main command. We do this by using a special dot notation.
Typing chaos.main() tells Python to invoke the main function in the chaos module.

## Inside a Python Program

The first two lines of the program start with the # character:

```
# File: chaos.py
# A simple program illustrating chaotic behavior.
```

These lines are called comments. They are intended for human readers of the program and are ignored by
Python. The Python interpreter always skips any text from the pound sign (#) through the end of a line.

The next line of the program begins the definition of a function called main.
```
def main():
```
The first line inside of main is really the beginning of our program.
```
print "This program illustrates a chaotic function"
```
This line causes Python to print a message introducing the program when it runs.
Take a look at the next line of the program.
```
x = input("Enter a number between 0 and 1: ")
```
Here x is an example of a variable. A variable is used to give a name to a value so that we can refer to it at
other points in the program. The entire line is an input statement. When Python gets to this statement, it
displays the quoted message Enter a number between 0 and 1: and then pauses, waiting for the
user to type something on the keyboard and press the <Enter> key. The value that the user types is then
stored as the variable x. In the first example shown above, the user entered .25, which becomes the value of
x.

The next statement is an example of a loop.
```
for i in range(10):
```
A loop is a device that tells Python to do the same thing over and over again. This particular loop says to
do something 10 times. The lines indented underneath the loop heading are the statements that are done 10
times. These form the body of the loop.
```
x = 3.9 * x * (1 - x)
print x
```
The effect of the loop is exactly the same as if we had written the body of the loop 10 times:
```
x = 3.9 * x * (1 - x)
print x
x = 3.9 * x * (1 - x)
print x
x = 3.9 * x * (1 - x)
print x
x = 3.9 * x * (1 - x)
print x
x = 3.9 * x * (1 - x)
print x
x = 3.9 * x * (1 - x)
print x
x = 3.9 * x * (1 - x)
print x
x = 3.9 * x * (1 - x)
print x
x = 3.9 * x * (1 - x)
print x
x = 3.9 * x * (1 - x)
print x
```
But what exactly do these statements do? The first one performs a calculation.
```
x = 3.9 * x * (1 - x)
```
This is called an assignment statement.

The second line in the loop body is a type of statement we have encountered before, a print statement.
```
print x
```
When Python executes this statement the current value of x is displayed on the screen. So, the first number
of output is 0.73125.

Remember the loop executes 10 times. After printing the value of x, the two statements of the loop are
executed again.
```
x = 3.9 * x * (1 - x)
print x
```

