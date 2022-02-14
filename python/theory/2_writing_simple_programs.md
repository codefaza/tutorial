# Writing Simple Programs

## The Software Development Process

**Formulate Requirements** Figure out exactly what the problem to be solved is. Try to understand as much
as possible about it. Until you really know what the problem is, you cannot begin to solve it.

**Determine Specifications** Describe exactly what your program will do. At this point, you should not worry
about how your program will work, but rather with deciding exactly what it will accomplish. For
simple programs this involves carefully describing what the inputs and outputs of the program will be
and how they relate to each other.

**Create a Design** Formulate the overall structure of the program. This is where the how of the program gets
worked out. The main task is to design the algorithm(s) that will meet the specifications.

**Implement the Design** Translate the design into a computer language and put it into the computer. In this
book, we will be implementing our algorithms as Python programs.

**Test/Debug the Program** Try out your program and see if it works as expected. If there are any errors (often
called bugs), then you should go back and fix them. The process of locating and fixing errors is called
debugging a program.

**Maintain the Program** Continue developing the program in response to the needs of your users. Most
programs are never really finished; they keep evolving over years of use.

## Example Program: Temperature Converter

Let’s go through the steps of the software development process with a simple real-world example. Suzie
Programmer has a problem. Suzie is an American computer science student spending a year studying in
Europe. She has no problems with language, as she is fluent in many languages (including Python). Her
problem is that she has a hard time figuring out the temperature in the morning so that she knows how to
dress for the day. Suzie listens to the weather report each morning, but the temperatures are given in degrees
Celsius, and she is used to Fahrenheit.

1. Suzie begins with the requirements of her problem. In this case, the problem is pretty clear: the radio an-
nouncer gives temperatures in degrees Celsius, but Suzie only comprehends temperatures that are in degrees Fahrenheit. That’s the crux of the problem.

2. Next, Suzie considers the specifications of a program that might help her out. What should the input
be? She decides that her program will allow her to type in the temperature in degrees Celsius. And the
output? The program will display the temperature converted into degrees Fahrenheit. Now she needs to
specify the exact relationship of the output to the input. Suzie does some quick figuring to derive the formula. That seems an adequate specification.

3. Suzie is now ready to design an algorithm for her problem. She immediately realizes that this is a simple
algorithm that follows a standard pattern: Input, Process, Output (IPO). Her program will prompt the user
for some input information (the Celsius temperature), process it to convert to a Fahrenheit temperature, and
then output the result by displaying it on the computer screen.

4. Suzie could write her algorithm down in a computer language. However, the precision of writing it out
formally tends to stifle the creative process of developing the algorithm. Instead, she writes her algorithm
using pseudocode. Pseudocode is just precise English that describes what a program does. It is meant to
communicate algorithms without all the extra mental overhead of getting the details right in any particular
programming language.

Here is Suzie’s completed algorithm:
```
Input the temperature in degrees Celsius (call it celsius)
Calculate fahrenheit as 9/5 celsius + 32
Output fahrenheit
```
5. The next step is to translate this design into a Python program. This is straightforward, as each line of the
algorithm turns into a corresponding line of Python code.

```
# convert.py
# A program to convert Celsius temps to Fahrenheit
# by: Suzie Programmer
def main():
celsius = input("What is the Celsius temperature? ")
fahrenheit = 9.0 / 5.0 * celsius + 32
print "The temperature is", fahrenheit, "degrees Fahrenheit."
main()
```

6. After completing her program, Suzie tests it to see how well it works. She uses some inputs for which
she knows the correct answers. Here is the output from two of her tests.
```
What is the Celsius temperature? 0
The temperature is 32.0 degrees fahrenheit.
What is the Celsius temperature? 100
The temperature is 212.0 degrees fahrenheit.
```
You can see that Suzie used the values of 0 and 100 to test her program. It looks pretty good, and she is
satisfied with her solution. Apparently, no debugging is necessary.

## Elements of Programs

1. **Names** You have already seen that names are an important part of programming. We give names to modules (e.g., convert) and to the functions within modules(e.g., main). Variables are used to give names to values (e.g.,
celsius and fahrenheit). Technically, all these names are called identifiers. Python has some rules
about how identifiers are formed. Every identifier must begin with a letter or underscore (the “ ” character)
which may be followed by any sequence of letters, digits, or underscores. This implies that a single identifier
cannot contain any spaces.

2. **Expressions** 
Programs manipulate data. The fragments of code that produce or calculate new data values are called
expressions. So far our program examples have dealt mostly with numbers, so I’ll use numeric data to
illustrate expressions.

You should have little trouble constructing complex expressions in your own programs. Do keep in mind that only the round parentheses are allowed in expressions, but you can nest them if necessary to create expressions like this.
```
((x1 - x2) / 2*n) + (spam / k**3)
```
If you are reading carefully, you may be curious why, in her temperature conversion program, Suzie
Programmer chose to write 9.0/5.0 rather than 9/5. Both of these are legal expressions, but they give
different results. This mystery will be discussed in Chapter 3. If you can’t stand the wait, try them out for
yourself and see if you can figure out what’s going on.

3. **Output Statements** Now that you have the basic building blocks, identifier and expression, you are ready for a more complete description of various Python statements. You already know that you can display information on the screen
using Python’s print statement. But what exactly can be printed? Python, like all programming languages,
has a precise set of rulesfor the syntax (form) and semantics (meaning) of each statement. Computerscientists
have developed sophisticated notations called meta-languages for describing programming languages. In this
book we will rely on a simple template notation to illustrate the syntax of statements. Here are the possible forms of the print statement:
```
print <expr>
```
4. **Assignment Statements** 
One of the most important kinds of statements in Python is the assignment statement. We’ve already seen a number of these in our previous examples. The basic assignment statement has this form:
```
<variable> = <expr>
```
Here variable is an identifier and expr is an expression. The semantics of the assignment is that the expression on the right side is evaluated to produce a value, which is then associated with the variable named on the left side.

5. **Assigning Input** The purpose of an input statement is to get some information from the user of a program and store it into a
variable. Some programming languages have a special statement to do this. In Python, input is accomplished
using an assignment statement combined with a special expression called input. This template shows the
standard form.
```
<variable> = input(<prompt>)
```

6. **Simultaneous Assignment** There is an alternative form of the assignment statement that allows us to calculate several values all at the same time. It looks like this:
```
<var>, <var>, ..., <var> = <expr>, <expr>, ..., <expr>
```
This is called simultaneous assignment. Semantically, this tells Python to evaluate all the expressions on
the right-hand side and then assign these values to the corresponding variables named on the left-hand side.
Here’s an example.
```
sum, diff = x+y, x-y
```

7. **Definite Loops** You already know that programmers use loopsto execute a sequence ofstatementsseveral times in succession. The simplest kind of loop is called a definite loop. This is a loop that will execute a definite number of times. That is, at the point in the program when the loop begins, Python knows how many times to go around
(or iterate) the body of the loop. For example, the Chaos program from Chapter 1 used a loop that always
executed exactly ten times.
```
for i in range(10):
x = 3.9 * x * (1 - x)
print x
```
This particular loop pattern is called a counted loop, and it is built using a Python for statement. Before
considering this example in detail, let’s take a look at what for loops are all about.

A Python for loop has this general form.
```
for <var> in <sequence>:
<body>
```
The body of the loop can be any sequence of Python statements. The start and end of the body is indicated
by its indentation under the loop heading (the for <var> in <sequence>: part).
Now, let’s go back to the example which began this section (from chaos.py) Look again at the loop
heading:
```
for i in range(10):
```
Comparing this to the template for the for loop shows that the last portion, range(10) must be some kind
of sequence. Let’s see what the Python interpreter tells us.
```
>>> range(10)
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```
Do you see what is happening here? The range function is a built-in Python command that simply produces
a list of numbers. The loop using range(10) is exactly equivalent to one using a list of 10 numbers.
```
for i in [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]:
```
In general, range(<expr>) will produce a list of numbers that starts with 0 and goes up to, but not
including, the value of <expr>. If you think about it, you will see that the value of the expression determines
the number of items in the resulting list. In chaos.py we did not even care what values the loop index
variable used (since the value of i was not referred to anywhere in the loop body). We just needed a list of
length 10 to make the body execute 10 times.







