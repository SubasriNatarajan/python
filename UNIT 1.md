![N|Solid](https://github.com/SubasriNatarajan/python/blob/main/Unit%20-%202%20Word%20Art.png?raw=true)

## **UNIT I - ALGORITHMIC PROBLEM SOLVING**

*Algorithms, building blocks of algorithms (statements, state, control flow, functions), notation (pseudo code, flow chart, programming language), algorithmic problem solving, simple strategies for developing algorithms (iteration, recursion).* 

***Illustrative problems:*** *find minimum in a list, insert a card in a list of sorted cards, Guess an integer number in a range, Towers of Hanoi.*

[Illustrative Problem Solutions](https://github.com/Professor-Sathish/GE_8151-unit-programs/tree/master/MD%20FILES)- find minimum in a list, insert a card in a list of sorted cards, Guess an integer number in a range, Towers of Hanoi

[Memcode flashcards](https://www.memcode.com/courses/2283)- 20+ flashcards to review the contents of this unit. Space repetition of the flashcards will help in retaining the content and perform better in exams."

#  TABLE OF CONTENTS

[1.1. ALGORITHMS](https://github.com/SubasriNatarajan/python/blob/main/UNIT%201.md#11algorithms)

[1.2. BUILDING BLOCKS OF ALGORITHM](https://github.com/SubasriNatarajan/python/blob/main/UNIT%201.md#12building-blocks-of-algorithms)

[1.3. NOTATION OF ALGORITHM](https://github.com/SubasriNatarajan/python/blob/main/UNIT%201.md#13notations)

[1.4. ALGORITHMIC PROBLEM SOLVING](https://github.com/SubasriNatarajan/python/blob/main/UNIT%201.md#14algorithmic-problem-solving)

[1.5. SIMPLE STRATEGIES FOR DEVELOPING ALGORITHM](https://github.com/SubasriNatarajan/python/blob/main/UNIT%201.md#15simple-strategies-for-developing-algorithm)

### INTRODUCTION 
A program is a set of instructions that tells the computer how to solve a particular problem. Various program design tools like algorithms, pseudocodes and flowcharts are used to design the blueprint of the solution (or the program to be written). 
Computer programming goes a step further in problem solving process. Programming means writing computer programs. While programming, the programmers take an algorithm and code the instructions in a particular programming language so that it can be executed by a computer. These days, there are many programming languages available in the market. The programmer can choose any language depending on his expertise and the problem domain
### 1.1.ALGORITHMS
*In computing, we focus on the type of problems categorically known as **algorithmic problems**, where their solutions are expressible in the form of algorithms. The term ‘***algorithm***’ was derived from the name of Mohammed al-Khwarizmi, a Persian mathematician in the nineth century (Al-Khwarizmi → Algorism (in Latin) → Algorithm).
- The typical meaning of an algorithm *is a formally defined procedure for performing some calculation*. If a procedure is formally defined, then it must be implemented using some formal language, and such languages are known as programming languages. The algorithm gives the logic of the program, that is, a step-by-step description of how to arrive at a solution.
- In general terms, ***an algorithm provides a blueprint to writing a program to solve a particular problem. It is considered to be an effective procedure for solving a problem in a finite number of steps.*** That is, a well defined algorithm always provides an answer, and is guaranteed to terminate. Algorithms are mainly used to achieve software reuse. 

**_Real Life Example_**
**_Procedure to cook Bread Toast_**

_Step 1 : Grab a loaf of bread_

_Step 2 : Get a pan and place it on the stove let it heat_

_Step 3 : Pour some oil on the pan and wait for oil to be heated_

_Step 4 : Put a slice on the pan and roast until it become brown in shade_

_Step 5 : Turn the slice and roast until it become brown in shade_

_Step 5 : Get the toasted bread from the pan and serve it on a plate with anything or nothing._

_The above procedure that explains “how to make a bread toast” and what are all the requirements before we start the procedures. We can code this procedure or algorithm in any programming language of your choice and simulate as results on the computer display. Else we can feed this procedure to the robot with proper instructions and we make the robot to do the bread toast for us._

**_Example :_**

**Algorithm for adding two numbers:**

_Step 1 : Get the 2 numbers from the user as input._

_Step 2 : Perform addition of those 2 numbers._

_Step 3 : Store the answer for display._

_Step 4 : Display the stored value to the user._

***Why We need Algorithm***
Three reasons for using algorithms are efficiency, abstraction and reusability.

**_Efficiency_**: Certain types of problems, like sorting, occur often in computing. Efficient algorithms must be used to solve such problems considering the time and cost factor involved in each algorithm.

**_Abstraction_**: Algorithms provide a level of abstraction in solving problems because many seemingly complicated problems can be distilled into simpler ones for which well known algorithms exist. Once we see a more complicated problem in a simpler light, we can think of the simpler problem as just an abstraction of the more complicated one. For example, imagine trying to find the shortest way to route a packet between two gateways in an internet. Once we realize that this problem is just a variation of the more general shortest path problem, we can solve it using the generalised approach.

**_Reusability_**: Algorithms are often reusable in many different situations. Since many well-known algorithms are the generalizations of more complicated ones, and since many complicated problems can be distilled into simpler ones, an efficient means of solving certain simpler problems potentially lets us solve many complicated problems.

### 1.1.1 Characteristics of Algorithm

• Precision: The instructions should be written in a precise manner. 

• Uniqueness: The outputs of each step should be unambiguous, i.e., they should be unique and only depend on the input and the output of the preceding steps.

• Finiteness: Not even a single instruction must be repeated infinitely.

• Effectiveness: The algorithm should designed in such a way that it should be the most effective among many different ways to solve a problem. 

• Input: The algorithm must receive an input. 

• Output: After the algorithm gets terminated, the desired result must be obtained.

• Generality: The algorithm can be applied to various set of inputs

### 1.2.BUILDING BLOCKS OF ALGORITHMS

As algorithm is a part of the blue-print or plan for the computer program. An algorithm is constructed using following blocks.

• Statements

• States

• Control flow

• Function

**i) Statements**

Statements are simple sentences written in algorithm for specific purpose. Statements may consists of assignment statements, input/output statements, comment statements.

Example:

• Read the value of ‘a’ //This is input statement

• Calculate c=a+b //This is assignment statement

• Print the value of c // This is output statement

• Comment statements are given after // symbol, which is used to tell the purpose of the line.

**ii) States**

An algorithm is deterministic automation for accomplishing a goal which, given an initial state, will terminate in a defined end-state.

An algorithm will definitely have start state and end state.

**iii) Control Flow**

Control flow which is also stated as flow of control, determines what section of code is to run in program at a given time. There are three types of flows, they are

1. Sequential control flow

2. Selection or Conditional control flow

3. Looping or repetition control flow

**Sequential control flow:**

The name suggests the sequential control structure is used to perform the action one after another. Only one step is executed once. The logic is top to bottom approach.

**Example**

**Description:** To find the sum of two numbers.

1. Start
2. Read the value of ‘a’
3. Read the value of ‘b’
4. Calculate sum=a+b
5. Print the sum of two number
6. Stop

**Selection or Conditional control flow**

Selection flow allows the program to make choice between two alternate paths based on condition. It is also called as decision structure

**Basic structure:**

**IF**CONDITION is **TRUE** then

perform some action

**ELSE IF** CONDITION is **FALSE** then

perform some action

The conditional control flow is explained with the example of finding greatest of two numbers.

**Example**

**Description:** finding the greater number

1. Start
2. Read a
3. Read b
4. If a>b then
- 4.1. Print a is greater else
- 4.2. Print b is greater
5. Stop

**Repetition control flow**

Repetition control flow means that one or more steps are performed repeatedly until some condition is reached. This logic is used for producing loops in program logic when one one more instructions may need to be executed several times or depending on condition.

**Basic Structure:**

Repeat until CONDITION is true

Statements

**Example**

**Description:** to print the values from 1 to n

1. Start
2. Read the value of ‘n’
3. Initialize i as 1
4. Repeat step 
- 4.1 until i< n
- 4.2. Print i
5. Stop

**Function**

A function is a block of organized, reusable code that is used to perform a single, related action. Function is also named as methods, sub-routines.

**Elements of functions:**
1. Name for declaration of function
2. Body consisting local declaration and statements
3. Formal parameter
4. Optional result type.

**Basic Syntax**

function\_name(parameters)

function statements

end function

Algorithm for addition of two numbers using function

**Main function()**

Step 1: Start

Step 2: Call the function add()

Step 3: Stop

**sub function add()**

Step 1: Functionstart

Step 2: Geta,bValues

Step 3: add c=a+b

Step 4: Printc

Step 5: Return

### 1.3.NOTATIONS

**FLOWCHART**
Flow chart is defined as graphical representation of the logic for problem solving. The purpose of flowchart is making the logic of the program clear in a visual representation.

![](https://github.com/SubasriNatarajan/python/blob/main/001.jpeg?raw=true)

**Rules for drawing a flowchart**

- The flowchart should be clear, neat and easy to follow.

![](https://github.com/SubasriNatarajan/python/blob/main/002.jpeg?raw=true)

- The flowchart must have a logical start and finish.\Only one flow line should come out from a process symbol.
- Only one flow line should enter a decision symbol. However, two or three flow lines may leave the decision symbol.

![](https://github.com/SubasriNatarajan/python/blob/main/003.png?raw=true)

- Only one flow line is used with a terminal symbol.

![](https://github.com/SubasriNatarajan/python/blob/main/004.jpeg?raw=true)

- Within standard symbols, write briefly and precisely.
- Intersection of flow lines should be avoided.

**Advantages of flowchart:**

1. **Communication: -** Flowcharts are better way of communicating the logic of a system to all concerned.
1. **Effective analysis: -** With the help of flowchart, problem can be analyzed in more effective way.
1. **Proper	documentation:	-** Program	flowcharts	serve	as	agoodprogram documentation, which is needed for various purposes.
1. **Efficient Coding: -** The flowcharts act as a guide or blueprint during the systems analysis and program development phase.
1. **Proper Debugging: -** The flowchart helps in debugging process.
1. **Efficient Program Maintenance: -** The maintenance of operating program becomes easy with the help of flowchart. It helps the programmer to put efforts more efficiently on that part.

**Disadvantages of flow chart:**

1. **Complex logic: -** Sometimes, the program logic is quite complicated. In that case, flowchart becomes complex and clumsy.
1. **Alterations and Modifications: -** If alterations are required the flowchart may require re-drawing completely.
1. **Reproduction: -** As the flowchart symbols cannot be typed, reproduction of flowchart becomes a problem.
1. **Cost:** For large application the time and cost of flowchart drawing becomes costly.

**EXAMPLES:**

**Draw the flowchart to find the largest number between A and B**

![](https://github.com/SubasriNatarajan/python/blob/main/005.png?raw=true)

**Find the area of circle of radius r.**

![](https://github.com/SubasriNatarajan/python/blob/main/006.png?raw=true)


**Convert temperature Fahrenheit to Celsius.**

![](https://github.com/SubasriNatarajan/python/blob/main/007.png?raw=true)

**Flowchart for the problem of printing even numbers between 0 and 99**

![](https://github.com/SubasriNatarajan/python/blob/main/008.png?raw=true)

**PSEUDOCODE**

- Pseudo code consists of short, readable and formally styled English languages used for explain an algorithm.
- It does not include details like variable declaration, subroutines.
- It is easier to understand for the programmer or non-programmer to understand the general working of the program, because it is not based on any programming language.
- It gives us the sketch of the program before actual coding. 
- Pseudo code can’t be compiled and executed and not machine readable.
- There is no standard syntax for pseudo code.

**Guidelines for writing pseudo code:**

- Write one statement per line
- Capitalize initial keyword
- Indent to hierarchy
- End multiline structure
- Keep statements language independent

**Common keywords used in pseudocode**

The following gives common keywords used in pseudocodes.

- **//:** This keyword used to represent a comment.
- **BEGIN, END:** Begin is the first statement and end are the last statement.
- **INPUT, GET, READ:** The keyword is used to inputting data.
- **COMPUTE, CALCULATE:** used for calculation of the result of the given expression.
- **ADD, SUBTRACT, INITIALIZE:** used for addition, subtraction and initialization.
- **OUTPUT, PRINT, DISPLAY:** It is used to display the output of the program.
- **IF, ELSE, ENDIF:** used to make decision.
- **WHILE, ENDWHILE:** used for iterative statements.
- **FOR, ENDFOR:** Another iterative incremented/decremented tested automatically.

**Syntax for if else:**
```sh
IF (condition)THEN 
    statement
    ... 
ELSE
     statement
     ...
ENDIF
```
**Example: Greatest of two numbers**
```sh 
BEGIN READ a,b
IF (a>b) THEN
DISPLAY a is greater 
ELSE
DISPLAY b is greater 
END IF
END
```
**Syntax for For:**
```sh
FOR( start-value to end-value) DO
statement
... 
ENDFOR
```
**Example: Print n natural numbers**
```sh 
BEGIN GET n
INITIALIZE i=1 
FOR (i<=n) DO 
PRINT i
i=i+1 
ENDFOR
END
```
**Syntax for While:**
```sh
WHILE (condition) DO 
statement
...
ENDWHILE
```
**Example: Print n natural numbers**
```sh 
BEGIN GET n
INITIALIZE i=1 
WHILE(i<=n) DO
PRINT i
i=i+1 
ENDWHILE
END
```
**Advantages:**

- Pseudo is independent of any language; it can be used by most programmers.
- It is easy to translate pseudo code into a programming language and easily modifiable.
- Converting a pseudo code to programming language is very easy as compared with converting a flowchart to programming language.

**Disadvantages:**

- It does not provide visual representation of the program’s logic.
- There are no accepted standards for writing pseudo codes.
- It cannot be compiled nor executed.
- For a beginner, it is more difficult to follow the logic or write pseudo code as compared to flowchart.

**EXAMPLES:**         

**Addition of two numbers:** 
```console
BEGIN
GET a,b
ADD c=a+b
PRINT c 
END
```
**Calculate sum and average for n numbers:**
```console
BEGIN
INITIALIZE sum=0, i=1
READ n
FOR i <=n, then
COMPUTE sum = sum +i
CALCULATE i=i+1
END FOR
COMPUTE avg = sum/n
PRINT sum, avg
END
```
**Calculate area of circle:**
```console
BEGIN
READ radius, r
INITIALIZE pi=3.14
CALCULATE Area=pi \* r \*r
PRINT Area
END
```
**Read Number  n and print the integers counting upto n:**
```console
BEGIN
READ n
INITIALIZE i to 1
FOR i <= n, then
DISPLAY i
INCREMENT i
END FOR
END
```
**To determine a student whether successful or fail.**
```console
BEGIN
READ student’s grade
IF student's grade is greater than or equal to 50
Print “passed”
ELSE
Print “failed”
END
```
|**Algorithm**|**Flowchart**|**Pseudo code**|
| :-: | :-: | :-: |
|An algorithm is a sequence of instructions used to solve a problem|It is a graphical representation of algorithm|It is a language representation of algorithm.|
|User needs knowledge to write algorithm.|not need knowledge of program to draw or understand flowchart|Not need knowledge of program language to understand or write a pseudo code.|

**PROGRAMMING LANGUAGE**

A programming language is a set of symbols and rules for instructing a computerto perform specific tasks. The programmers have to follow all the specified rules before writing program using programming language. The user has to communicate with the computer using language which it can understand.

**Types of programming language**

- Machine language
- Assembly language
- High level language

**Machine language:**

The computer can understand only machine language which uses 0’s and 1’s. In machine language the different instructions are formed by taking differentcombinations of 0’s and 1’s.

**Advantages:** 

**Translation free:**

Machine language is the only language which the computer understands. For executing any program written in any programming language, the conversion to machine language is necessary. The program written in machine language can be executed directly on computer. In this case any conversion process is not required. 

**High speed**

The machine language program is translation free. Since the conversion time is saved, the execution of machine language program is extremely fast.

**Disadvantage:**

- It is hard to find errors in a program written in the machine language.
- Writing program in machine language is a time-consuming process. 

**Machine dependent:**

According to architecture used, the computer differs from each other. So, machine language differs from computer to computer. So, a program developed for a particular type of computer may not run-on other type of computer. 

**Assembly language:**

- To overcome the issues in programming language and make the programming process easier, an assembly language is developed which is logically equivalent to machine language but it is easier for people to read, write and understand.
- Assembly language is symbolic representation of machine language. Assembly languages are symbolic programming language that uses symbolic notation to represent machine language instructions. They are called low level language because they are so closely related to the machines.

Ex: ADD a, b

**Assembler:**

Assembler is the program which translates assembly language instruction in to a machine language.

**Advantage:**

- Easy to understand and use.
- It is easy to locate and correct errors.

**Disadvantage** 

**Machine dependent**

The assembly language program which can be executed on the machine depends on the architecture of that computer.

**Hard to learn**

It is machine dependent, so the programmer should have the hardware knowledge to create applications using assembly language.

**Less efficient**

- Execution time of assembly language program is more than machine language program.
- Because assembler is needed to convert from assembly language to machine language.

**High level language**

High level language contains English words and symbols. The specified rules are to be followed while writing program in high level language. The interpreter or compilers are used for converting these programs in to machine readable form.

**Translating high level language to machine language**

The programs that translate high level language in to machine language are called interpreter or compiler.

**Compiler**

A compiler is a program which translates the source code written in a high-level language in to object code which is in machine language program. Compiler reads the whole program written in high level language and translates it to machine language. If any error is found it display error message on the screen.

**Interpreter**

Interpreter translates the high-level language program in line-by-line manner. The interpreter translates a high-level language statement in a source program to a machinecode and executes it immediately before translating the next statement. When an error is found the execution of the program is halted and error message is displayed on the screen.

**Advantages** 

**Readability**

High level language is closer to natural language so they are easier to learn and understand

**Machine independent**

High level language program has the advantage of being portable between machines.

**Easy debugging**

Easy to find and correct error in high level language

**Disadvantages**

**Less efficient**

The translation process increases the execution time of the program. Programs in high level language require more memory and take more execution time to execute.

**High Level Languages are divided into following categories:**

- Interpreted programming languages
- Functional programming languages
- Compiled programming languages
- Procedural programming languages
- Scripting programming language
- Markup programming language
- Concurrent programming language
- Object oriented programming language

**Interpreted Programming Languages:**

An interpreted language is a programming language for which most of its implementation executes instructions directly, without previously compiling a program into machine language instructions. The interpreter executes the program directly translating each statement into a sequence of one or more subroutines already compiled into machine code.

**Examples: Pascal, Python**

**Functional programming language:**

Functional programming language defines every computation as a mathematical evaluation. They focus on the programming languages are bound to mathematical calculations

**Examples: Clean, Haskell**

**Compiled Programming language:**

A compiled programming is a programming language whose implementation are typically compilers and not interpreters. It will produce a machine code from source code.

**Examples:C, C++, C#, JAVA**

**Procedural programming language:**

Procedural (imperative) programming implies specifying the steps that the programs should take to reach to an intended state.A procedure is a group of statements that can be referred through a procedure call. Procedures help in the reuse of code. Procedural programming makes the programs structured and easily traceable for program flow.

**Examples: Hyper talk, MATLAB**

**Scripting language:**

Scripting language are programming languages that control an application. Scripts can execute independent of any other application. They are mostly embedded in the application that they control and are used to automate frequently executed tasks like communicating with external program.

**Examples: Apple script, VB script**

**Markup languages:**

A markup language is an artificial language that uses annotations to text that define hoe the text is to be displayed.

**Examples: HTML, XML**

**Concurrent programming language:**

Concurrent programming is a computer programming technique that provides for the execution of operation concurrently, either with in a single computer or across a number of systems.

**Examples: Joule, Limbo**


**Object oriented programming language:**

Object oriented programming is a programming paradigm based on the concept of objects which may contain data in the form of procedures often known as methods.

**Examples: Lava, Moto**

### 1.4.ALGORITHMIC PROBLEM SOLVING

- Algorithms are solutions to problems. They are not solutions themselves. They just list specific instructions that need to be performed for getting the solution. In computer science, emphasis is laid on writing a good and effective algorithm and this emphasis makes computer science distinct from other disciplines. For example, computer science is distinct from theoretical mathematics because those practitioners are typically satisfied with just proving the existence of a solution to a problem but in computer science, the problem is not solved until the algorithm is used to implement the solution. 
- We will now discuss about the sequence of steps one must typically follow for designing an effective algorithm.
![N|Solid](https://github.com/SubasriNatarajan/python/blob/main/Algorithmic.jpeg?raw=true)

1. Understanding the problem
2. Determining the capabilities of the computational device
3. Exact/approximate solution
4. Select the appropriate data structure
5. Algorithm design techniques
6. Methods of specifying an algorithm
7. Proving an algorithms correctness
8. Analysing the performance of an algorithm
> Understanding the problem 
- The problem given should be clearly and completely understood. It is compared with earlier problems that have already been solved to check if it is similar to them and a known
algorithm exists. If the algorithm is available, it is used otherwise a new one has to be developed.
> Determining the capabilities of the computational device 
- After understanding the problem, the capabilities of the computing device should be known. For this, the type of the architecture, speed and
memory availability of the device are noted.
> Exact/approximate solution 
- The next step is to develop the algorithm. The algorithm must compute correct output for all possible and legitimate inputs. This solution can be an exact solution or an approximate solution. For example, you can only have an approximate solution in case of finding square root of number or finding the solutions of nonlinear equations.
> Select the appropriate data structure 
- A data type is a well-defined collection of data with a welldefined set of operations on it. A data structure is basically a group of data elements that are put together
under one name, and which defines a particular way of storing and organizing data in a computer so that it can be used efficiently. The elementary data structures are as follows.
- List: Allows fast access of data.
- Sets: Treats data as elements of a set. Allows application of operations such as intersection, union, and
equivalence.
- Dictionaries: Allows data to be stored as a key-value pair.

> Algorithm design techniques 
- Developing an algorithm is an art which may never be fully automated. By mastering the design techniques, it will become easier for you to develop new and useful algorithms.
Examples of algorithm design techniques include dynamic programming.
> Methods of specifying an algorithm 
- An algorithm is just a sequence of steps or instructions that can be used to implement a solution. After writing the algorithm, it is specified either using a natural language or with the help of pseudocode and flowcharts. We will read about them in the next section. 
> Proving algorithms correctness 
- Writing an algorithm is not just enough. You need to prove that it computes solutions for all the possible valid inputs. This process is often referred to as algorithm validation. Algorithm validation ensures that the algorithm will work correctly irrespective of the programming language in which it will be implemented.
> Analysing the performance of algorithms 
- When an algorithm is executed, it uses the computer’s resources like the Central Processing Unit (CPU) to perform its operation and to hold the program and data respectively. An algorithm is analysed to measure its performance in terms of CPU time and memory space required to execute that algorithm. This is a challenging task and is often used to compare different algorithms for a particular problem. The result of the comparison helps us to choose the best solution from all possible solutions. Analysis of the algorithm also helps us to determine whether the algorithm will be able to meet any efficiency constraint that exits or not. 

### 1.5.SIMPLE STRATEGIES FOR DEVELOPING ALGORITHM

### 1.5.1 Iteration
_________________

In computational mathematics, an iterative method is a mathematical procedure that generates a sequence of improving approximate solutions for a class of problems, in which the n-th approximation is derived from the previous ones. A specific implementation of an iterative method, including the termination criteria, is an algorithm of the iterative method. An iterative method is called convergent if the corresponding sequence converges for given initial approximations.

### For Example

### To find power of a number

Step 1: Get a base number
Step 2: Get a power
Step 3: Initialize result value with number and pow with power
Step 4: Start with pow as 1
Step 5: Multiply result and number then increase pow by one
Step 6: Repeat Step 5 Until pow reaches value of power
Step 7: Break the loop and display the result
Step 8: End

### In pseudocode:

### TASK: To Find Power of a number
```sh
READ number
READ Power
Initialize result with number and pow with Power
WHILE pow < Power:
result = result * number
Increase pow by 1
End Loop
PRINT result
End
```

### 1.5.2 Recursion
_________________

- A recursive algorithm is an algorithm which calls itself with "smaller (or simpler)" input values, and which obtains the result for the current input by applying simple operations to the returned value for the smaller (or simpler) input. More generally if a problem can be solved utilizing solutions to smaller versions of the same problem, and the smaller versions reduce to easily solvable cases, then one can use a recursive algorithm to solve that problem. For example, the elements of a recursively defined set, or the value of a recursively defined function can be obtained by a recursive algorithm.

- If a set or a function is defined recursively, then a recursive algorithm to compute its members or values mirrors the definition. Initial steps of the recursive algorithm correspond to the basis clause of the recursive definition and they identify the basis elements. They are then followed by steps corresponding to the inductive clause, which reduce the computation for an element of one generation to that of elements of the immediately preceding generation.

- In general, recursive computer programs require more memory and computation compared with iterative algorithms, but they are simpler and for many cases a natural way of thinking about the problem.

### For Example 

### To find power of a number

Step 1: Get a base number 
Step 2: Get a power
Step 3: Send a number and power to routine
Step 4: In routine Compare power with 1
Step 5: If it is equal to 1 then return number
Step 6: Else Compute the same routine (Step 4 and 5) with a same number and  reduced power by 1
Step 7: display the result
Step 8: End

## In pseudocode:

### TASK: To Find Power of a number
```sh
READ number
READ Power
result = FIND_POWER number and power
FIND_POWER number and power:
IF power = 1:
ELSE
result = FIND_POWER number and power -1
RETURN result
End FIND_POWER
PRINT result
End
End TASK
```








