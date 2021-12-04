![N|Solid](https://github.com/SubasriNatarajan/python/blob/main/Word%20Art%20Unit%205.png?raw=true)
# UNIT - 5 FILES, MODULES, PACKAGES 

### OBJECTIVE
Files and exception: text files, reading and writing files, format operator; command line arguments, errors and exceptions, handling exceptions, modules, packages; Illustrative programs: word count, copy file.

[Illustrative Problem Solutions](https://github.com/kgashok/GE_8151-unit-programs/tree/master/mdfiles)

[Memcode flashcards](https://www.memcode.com/courses/2280)	- 40+ flashcards to review the contents of this unit. Space repetition of the flashcards will help in retaining the content and perform better in exams."

 #  TABLE OF CONTENTS
 
 [5.1.FILES](#51files)
 
 [5.2.TEXT FILE CHARACTERISTICS](#52text-file-characteristics)
 
 [5.3.READING AND WRITING FILES](#53reading-and-writing-text-files)

 [5.4.FORMAT OPERATOR](#54format-operator)
 
 [5.5.COMMAND LINE ARGUMENTS](#55command-line-arguments)
 
 [5.6.ERRORS AND EXCEPTIONS](#56errors-and-exceptions)
 
 [5.7.HANDLING EXCEPTIONS](#57-handling-exceptions)
 
 [5.8.MODULES](#58-modules)
 
 [5.9.PACKAGES](#59-packages)
### KEY TERMS
### File 
- A file is a container in a computer system for storing information. Files used in computers are similar in features to that of paper documents used in library and office files. In a computer operating system, files can be stored on optical drives, hard drives or other types of storage devices.
### Binary file 
- Binary file is a collection of bytes or a character stream. The data that is written into and read from binary file remain unchanged,+ with no separation between lines and no use of end-of-line characters and the interpretation of the files are left to the programmer.
### Text file 
- A text file is a stream of characters that can be processed sequentially and logically in the forward direction. The maximum number of characters in each line is limited to 255 characters.
### Sequential file access 
- In case of sequential file access, data is read from or written to a file in a sequential manner while the position indicator automatically gets adjusted by the stream I/O functions.
### Random file access 
- Random access means reading from or writing to any position in a file without reading or writing all the preceding data by controlling the position indicator
### Record 
- A record consists of a collection of data fields that conforms to a previously defined structure that can be stored on or retrieved from a file.
### Stream 
- The stream is a common, logical interface to the various devices that comprise the computer and is a logical interface to a file. Although files differ in form and capabilities, all streams are the same.
### File management 
- It basically means all operations related to creating, renaming, deleting, merging, reading, writing, etc. of any type of files.
### Path
- The path specifies the drive and/or directory (or folder) where the file is located. On PCs, the backslash character is used to separate directory names in a path. Some systems like Unix use the forward slash (/) as the directory separator.
# 5.1.FILES
### What are files? 
*A file is sequential stream of bytes ending with an end-of-file marker. As we know, at the time of execution, every program is executed in the main memory. Main memory is volatile and the data would be lost once the program is terminated. If we need the same data again, we have to store the data in a file on the disk. A file is sequential stream of bytes ending with an end-of-file marker*
- Storage of data in variables and arrays is temporary—such data is lost when a program terminates. Files are used for permanent retention of data. Computers store files on secondary storage devices, such as hard drives, CDs, DVDs and flash drives. In this chapter, we explain how data files are created, updated and processed by C programs. We consider both sequential-access and random-access file processing.
### File Extensions
- File extensions we can usually tell if a file is binary or text based on its file extension. This is because by convention the extension reflects the file format, but ultimately it is the file format that dictates whether the file data is binary or text.
### Types of Files
- Text files
- Data files
- Directory files
- Binary files
- Graphic files
### Common extensions that are binary file formats:
> Images: jpg, png, gif, bmp, tiff, psd, ...

> Videos: mp4, mkv, avi, mov, mpg, vob, ...

> Audio: mp3, aac, wav, flac, ogg, mka, wma, ...

> Documents: pdf, doc, xls, ppt, docx, odt, ...

> Archive: zip, rar, 7z, tar, iso, ...

> Database: mdb, accde, frm, sqlite, ...

> Executable: exe, dll, so, class, ...

### Common extensions that are text file formats:
> Web standards: html, xml, css, svg, json, ...

> Source code: c, cpp, h, cs, js, py, java, rb, pl, php, sh, ...

> Documents: txt, tex, markdown, asciidoc, rtf, ps, ...

> Configuration: ini, cfg, rc, reg, ...

> Tabular data: csv, tsv, ...
_________________
# 5.2.TEXT FILE CHARACTERISTICS
By convention, the data in every text file obeys a number of rules:
- The text looks readable to a human or at least moderately sane. Even if it contains a heavy proportion of punctuation symbols (like HTML, RTF, and other markup formats), there is some visible structure and it’s not seemingly random garbage.
- The data format is usually line-oriented. Each line could be a separate command, or a list of values could put each item on a different line, etc. The maximum number of characters in each line is usually a reasonable value like 100, not like 1000.
- The text looks readable to a human or at least moderately sane. Even if it contains a heavy proportion of punctuation symbols (like HTML, RTF, and other markup formats), there is some visible structure and it’s not seemingly random garbage.
### BINARY FILE CHARACTERISTICS
-	For most software that people use in their daily lives, the software consumes and produces binary files. Examples of such software include Microsoft Office, Adobe Photoshop, and various audio/video/media players. A typical computer user works with mostly binary files and very few text files.
-	A binary file always needs matching software to read or write it. For example, an MP3 file can be produced by a sound recorder or audio editor, and it can be played in a music player or audio editor. But an MP3 file cannot be played in an image viewer or database software.
-	Some binary formats are popular enough that a wide variety of programs can produce or consume it. Image formats like JPEG are the best example – not only can they be used in image viewers and editors, they can be viewed in web browsers, audio players (for album art), and document software (such as adding a picture into a Word doc).
### BASIC FILE OPERATIONS
> Creation of a new file

> Modification of data or file attributes

> Reading of data from the file

> Opening the file in order to make the contents available to other programs

> Writing data to the file

> Closing or terminating a file operation
_________________
# 5.3.READING AND WRITING TEXT FILES
open() returns a file object, and is most commonly used with two arguments: open(filename, mode).
```py
>>> f = open('workfile', 'w')
```
The first argument is a string containing the filename. The second argument is another string containing a few characters describing the way in which the file will be used. mode can be 'r' when the file will only be read, 'w' for only writing (an existing file with the same name will be erased), and 'a' opens the file for appending; any data written to the file is automatically added to the end. 'r+' opens the file for both reading and writing. The mode argument is optional; 'r' will be assumed if it’s omitted.

Normally, files are opened in text mode, that means, you read and write strings from and to the file, which are encoded in a specific encoding. If encoding is not specified, the default is platform dependent (see open()). 'b' appended to the mode opens the file in binary mode: now the data is read and written in the form of bytes objects. This mode should be used for all files that don’t contain text.

In text mode, the default when reading is to convert platform-specific line endings (\n on Unix, \r\n on Windows) to just \n. When writing in text mode, the default is to convert occurrences of \n back to platform-specific line endings. This behind-the-scenes modification to file data is fine for text files, but will corrupt binary data like that in JPEG or EXE files. Be very careful to use binary mode when reading and writing such files.
It is good practice to use the with keyword when dealing with file objects. The advantage is that the file is properly closed after its suite finishes, even if an exception is raised at some point. Using with is also much shorter than writing equivalent try-finally blocks:
```py
>>> with open('workfile') as f:
...     read_data = f.read()

>>> # We can check that the file has been automatically closed.
>>> f.closed
True
```
If you’re not using the with keyword, then you should call f.close() to close the file and immediately free up any system resources used by it.

>Warning: Calling f.write() without using the with keyword or calling f.close() might result in the arguments of f.write() not being completely written to the disk, even if the program exits successfully. 

After a file object is closed, either by a with statement or by calling f.close(), attempts to use the file object will automatically fail.
```py
>>> f.close()
>>> f.read()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: I/O operation on closed file.
```
# Methods of File Objects
The rest of the examples in this section will assume that a file object called f has already been created.

To read a file’s contents, call f.read(size), which reads some quantity of data and returns it as a string (in text mode) or bytes object (in binary mode). size is an optional numeric argument. When size is omitted or negative, the entire contents of the file will be read and returned; it’s your problem if the file is twice as large as your machine’s memory. Otherwise, at most size characters (in text mode) or size bytes (in binary mode) are read and returned. If the end of the file has been reached, f.read() will return an empty string ('').
```py
>>> f.read()
'This is the entire file.\n'
>>> f.read()
''
```
f.readline() reads a single line from the file; a newline character (\n) is left at the end of the string, and is only omitted on the last line of the file if the file doesn’t end in a newline. This makes the return value unambiguous; if f.readline() returns an empty string, the end of the file has been reached, while a blank line is represented by '\n', a string containing only a single newline.
```py
>>> f.readline()
'This is the first line of the file.\n'
>>> f.readline()
'Second line of the file\n'
>>> f.readline()
''
```
For reading lines from a file, you can loop over the file object. This is memory efficient, fast, and leads to simple code:
```py
>>> for line in f:
...     print(line, end='')
...
This is the first line of the file.
Second line of the file
```
If you want to read all the lines of a file in a list you can also use list(f) or f.readlines().
f.write(string) writes the contents of string to the file, returning the number of characters written.
```py
>>> f.write('This is a test\n')
15
```
Other types of objects need to be converted – either to a string (in text mode) or a bytes object (in binary mode) – before writing them:
```py
>>> value = ('the answer', 42)
>>> s = str(value)  # convert the tuple to string
>>> f.write(s)
18
```
f.tell() returns an integer giving the file object’s current position in the file represented as number of bytes from the beginning of the file when in binary mode and an opaque number when in text mode.

To change the file object’s position, use f.seek(offset, whence). The position is computed from adding offset to a reference point; the reference point is selected by the whence argument. A whence value of 0 measures from the beginning of the file, 1 uses the current file position, and 2 uses the end of the file as the reference point. whence can be omitted and defaults to 0, using the beginning of the file as the reference point.
```py
>>> f = open('workfile', 'rb+')
>>> f.write(b'0123456789abcdef')
16
>>> f.seek(5)      # Go to the 6th byte in the file
5
>>> f.read(1)
b'5'
>>> f.seek(-3, 2)  # Go to the 3rd byte before the end
13
>>> f.read(1)
b'd'
```
In text files (those opened without a b in the mode string), only seeks relative to the beginning of the file are allowed (the exception being seeking to the very file end with seek(0, 2)) and the only valid offset values are those returned from the f.tell(), or zero. Any other offset value produces undefined behaviour.

File objects have some additional methods, such as isatty() and truncate() which are less frequently used; consult the Library Reference for a complete guide to file objects.
### Types of File Modes
| File Mode  | Description  |
|---|---|
| r  | Opens a file for reading only. The file pointer is placed at the beginning of the file. This is the default mode.  |
| rb  | Opens a file for reading only in binary format. The file pointer is placed at the beginning of the file. This is the default mode.  |
| r+  | Opens a file for both reading and writing. The file pointer placed at the beginning of the file.  |
|  rb+ | Opens a file for both reading and writing in binary format. The file pointer placed at the beginning of the file.  |
| w  | Opens a file for writing only. Overwrites the file if the file exists. If the file does not exist, creates a new file for writing.  |
|  wb |  Opens a file for writing only in binary format. Overwrites the file if the file exists. If the file does not exist, creates a new file for writing. |
|  w+ | Opens a file for both writing and reading. Overwrites the existing file if the file exists. If the file does not exist, creates a new file for reading and writing.  |
| wb+  | Opens a file for both writing and reading in binary format. Overwrites the existing file if the file exists. If the file does not exist, creates a new file for reading and writing.  |
| a  | Opens a file for appending. The file pointer is at the end of the file if the file exists. That is, the file is in the append mode. If the file does not exist, it creates a new file for writing.  |
| ab  | Opens a file for appending in binary format. The file pointer is at the end of the file if the file exists. That is, the file is in the append mode. If the file does not exist, it creates a new file for writing.  |
| a+  |  Opens a file for both appending and reading. The file pointer is at the end of the file if the file exists. The file opens in the append mode. If the file does not exist, it creates a new file for reading and writing. |
|  ab+ |  Opens a file for both appending and reading in binary format. The file pointer is at the end of the file if the file exists. The file opens in the append mode. If the file does not exist, it creates a new file for reading and writing. |
### Difference between Append and Write Mode
-	Write (w) mode and Append (a) mode, while opening a file are almost the same. Both are used to write in a file. In both the modes, new file is created if it doesn’t exists already.
-	The only difference they have is, when you open a file in the write mode, the file is reset, resulting in deletion of any data already present in the file. While in append mode this will not happen. Append mode is used to append or add data to the existing data of file (if any). Hence, when you open a file in Append(a) mode, the cursor is positioned at the end of the present data in the file.
### File Methods
| File Methods  |  Description | Prototype  |
|---|---|---|
| close()  |  Closes the file |  fileobject.close() |
| flush() | Flushes the internal buffer  | 	fileobject.flush()    |
|  read() | Returns the file content  | data = fileobject.read()  |
| readable()  | Returns whether the file stream can be read or not  | boolean = fileobject.flush()  |
| readline()  | Returns one line from the file  | data = fileobject.readline()  |
| readlines()  | Returns a list of lines from the file  |  filelines = fileobject.read() |
| seek()  | Change the file position  |  filelines = fileobject.seek(offset) |
|  seekable() | Returns whether the file allows us to change the file position  |  bool = fileobject.seekable() |
| tell()  | Returns the current file position  |  position = fileobject.tell() |
| truncate()  | Resizes the file to a specified size  |  fileobject.truncate(size) |
| writeable()  | Returns whether the file can be written to or not  | bool = fileobject.writeable()  |
|  write() | Writes the specified string to the file  | fileobject.write(data)  |
| writelines()  | Writes a list of strings to the file  |  fileobject.writelines(listofstrings[]) |
_________________
# 5.4.FORMAT OPERATOR
str.format() is one of the string formatting methods in Python3, which allows multiple substitutions and value formatting. This method lets us concatenate elements within a string through positional formatting.
Types
-	Single Place Holder
-	Multiple Place Holder
-	Type Specification
>Note: The formatting operations described here exhibit a variety of quirks that lead to a number of common errors (such as failing to display tuples and dictionaries correctly). Using the newer formatted string literals, the str.format() interface, or template strings may help avoid these errors. Each of these alternatives provides their own trade-offs and benefits of simplicity, flexibility, and/or extensibility. 

String objects have one unique built-in operation: the % operator (modulo). This is also known as the string formatting or interpolation operator. Given format % values (where format is a string), % conversion specifications in format are replaced with zero or more elements of values. The effect is similar to using the sprintf() in the C language.

If format requires a single argument, values may be a single non-tuple object. 5 Otherwise, values must be a tuple with exactly the number of items specified by the format string, or a single mapping object (for example, a dictionary).

A conversion specifier contains two or more characters and has the following components, which must occur in this order:
1. The '%' character, which marks the start of the specifier.
2. Mapping key (optional), consisting of a parenthesised sequence of characters (for example, (somename)).
3. Conversion flags (optional), which affect the result of some conversion types.
4. Minimum field width (optional). If specified as an '*' (asterisk), the actual width is read from the next element of the tuple in values, and the object to convert comes after the minimum field width and optional precision.
5. Precision (optional), given as a '.' (dot) followed by the precision. If specified as '*' (an asterisk), the actual precision is read from the next element of the tuple in values, and the value to convert comes after the precision.
6. Length modifier (optional).
7. Conversion type.

When the right argument is a dictionary (or other mapping type), then the formats in the string must include a parenthesised mapping key into that dictionary inserted immediately after the '%' character. The mapping key selects the value to be formatted from the mapping. For example:
```py
>>> print('%(language)s has %(number)03d quote types.' %
      {'language': "Python", "number": 2})
```
In this case no * specifiers may occur in a format (since they require a sequential parameter list).

The conversion flag characters are:
| Flag | Meaning |
|---|---|
|'#'|The value conversion will use the “alternate form” (where defined below).|
|'0'|The conversion will be zero padded for numeric values.|
|'-'|The converted value is left adjusted (overrides the '0' conversion if both are given).|
|' '|(a space) A blank should be left before a positive number (or empty string) produced by a signed conversion.|
|'+'|A sign character ('+' or '-') will precede the conversion (overrides a “space” flag).|

A length modifier (h, l, or L) may be present, but is ignored as it is not necessary for Python – so e.g. %ld is identical to %d.

The conversion types are:
| Conversion | Meaning |
|---|---|
|'d'|Signed integer decimal.|
|'i'|Signed integer decimal.|
|'o'|Signed octal value.|
|'u'|Obsolete type – it is identical to 'd'.|
|'x'|Signed hexadecimal (lowercase).|
|'X'|Signed hexadecimal (uppercase).|
|'e'|Floating point exponential format (lowercase).|
|'E'|Floating point exponential format (uppercase).|
|'f'|Floating point decimal format.|
|'F'|Floating point decimal format.|
|'g'|Floating point format. Uses lowercase exponential format if exponent is less than -4 or not less than precision, decimal format otherwise.|
|'G'|Floating point format. Uses uppercase exponential format if exponent is less than -4 or not less than precision, decimal format otherwise.|
|'c'|Single character (accepts integer or single character string).|
|'r'|String (converts any Python object using repr()).|
|'s'|String (converts any Python object using str()).|
|'a'|String (converts any Python object using ascii()).|
|'%'|No argument is converted, results in a '%' character in the result.|
### Notes:
1. The alternate form causes a leading octal specifier ('0o') to be inserted before the first digit.
2. The alternate form causes a leading '0x' or '0X' (depending on whether the 'x' or 'X' format was used) to be inserted before the first digit.
3. The alternate form causes the result to always contain a decimal point, even if no digits follow it.
4. The precision determines the number of digits after the decimal point and defaults to 6.
5. The alternate form causes the result to always contain a decimal point, and trailing zeroes are not removed as they would otherwise be.
6. The precision determines the number of significant digits before and after the decimal point and defaults to 6.
7. If precision is N, the output is truncated to N characters.
_________________
# 5.5.COMMAND LINE ARGUMENTS
The arguments that are given after the name of the program in the command line shell of the operating system are known as Command Line Arguments. We can use sys.argv to get and process the command line arguments
The sys module provides functions and variables used to manipulate different parts of the Python runtime environment. This module provides access to some variables used or maintained by the interpreter and to functions that interact strongly with the interpreter.
Common utility scripts often need to process command line arguments. These arguments are stored in the sys module’s argv attribute as a list. For instance the following output results from running python demo.py one two three at the command line:
```py
>>> import sys
>>> print(sys.argv)
['demo.py', 'one', 'two', 'three']
```
The argparse module provides a more sophisticated mechanism to process command line arguments. The following script extracts one or more filenames and an optional number of lines to be displayed:
```py
import argparse
parser = argparse.ArgumentParser(prog = 'top',
    description = 'Show top lines from each file')
parser.add_argument('filenames', nargs='+')
parser.add_argument('-l', '--lines', type=int, default=10)
args = parser.parse_args()
print(args)
```
When run at the command line with python top.py --lines=5 alpha.txt beta.txt, the script sets args.lines to 5 and args.filenames to ['alpha.txt', 'beta.txt'].
_________________
# 5.6.ERRORS AND EXCEPTIONS
Even if a statement or expression is syntactically correct, it may cause an error when an attempt is made to execute it. Errors detected during execution are called exceptions and are not unconditionally fatal: you will soon learn how to handle them in Python programs. Most exceptions are not handled by programs, however, and result in error messages as shown here:
```py
>>> 10 * (1/0)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
>>> 4 + spam*3
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'spam' is not defined
>>> '2' + 2
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate str (not "int") to str
```
The last line of the error message indicates what happened. Exceptions come in different types, and the type is printed as part of the message: the types in the example are ZeroDivisionError, NameError and TypeError. The string printed as the exception type is the name of the built-in exception that occurred. This is true for all built-in exceptions, but need not be true for user-defined exceptions (although it is a useful convention). Standard exception names are built-in identifiers (not reserved keywords).

The rest of the line provides detail based on the type of exception and what caused it.

The preceding part of the error message shows the context where the exception occurred, in the form of a stack traceback. In general it contains a stack traceback listing source lines; however, it will not display lines read from standard input.

[Built-in Exceptions](https://docs.python.org/3/library/exceptions.html#bltin-exceptions) lists the built-in exceptions and their meanings.
### BUILD IN EXCEPTIONS
| Exception  | Cause of Error  |
|---|---|
| AssertionError  | Raised when an assert statement fails.  |
| AttributeError  |  Raised when attribute assignment or reference fails. |
|  EOFError |  Raised when the input() function hits end-of-file condition. |
|  FloatingPointError | Raised when a floating point operation fails.  |
| GeneratorExit  |  Raise when a generator's close() method is called. |
| ImportError  | Raised when the imported module is not found.  |
| IndexError  | Raised when the index of a sequence is out of range.  |
| KeyError  |  Raised when a key is not found in a dictionary. |
| KeyboardInterrupt  | Raised when the user hits the interrupt key (Ctrl+C or Delete).  |
| MemoryError  | Raised when an operation runs out of memory.  |
| NameError  |  Raised when a variable is not found in local or global scope. |
| NotImplementedError  |  Raised by abstract methods. |
| OSError  | Raised when system operation causes system related error.  |
| OverflowError  | Raised when the result of an arithmetic operation is too large to be represented.  |
|  ReferenceError | Raised when a weak reference proxy is used to access a garbage collected referent.  |
| RuntimeError  | Raised when an error does not fall under any other category.  |
| StopIteration  |  Raised by next() function to indicate that there is no further item to be returned by iterator. |
| SyntaxError  | Raised by parser when syntax error is encountered.  |
| IndentationError  | Raised when there is incorrect indentation.  |
|  TabError |  Raised when indentation consists of inconsistent tabs and spaces. |
|  SystemError |Raised when interpreter detects internal error.   |
|  SystemExit | Raised by sys.exit() function.  |
| TypeError  |  Raised when a function or operation is applied to an object of incorrect type. |
| UnboundLocalError  |  Raised when a reference is made to a local variable in a function or method, but no value has been bound to that variable. |
| UnicodeError  | Raised when a Unicode-related encoding or decoding error occurs.  |
|UnicodeEncodeError   |  Raised when a Unicode-related error occurs during encoding. |
|UnicodeDecodeError   | Raised when a Unicode-related error occurs during decoding.  |
| UnicodeTranslateError  |  Raised when a Unicode-related error occurs during translating. |
|  ValueError | Raised when a function gets an argument of correct type but improper value. |
| ZeroDivisionError  | Raised when the second operand of division or modulo operation is zero.  |
_________________
# 5.7. HANDLING EXCEPTIONS
It is possible to write programs that handle selected exceptions. Look at the following example, which asks the user for input until a valid integer has been entered, but allows the user to interrupt the program (using Control-C or whatever the operating system supports); note that a user-generated interruption is signalled by raising the KeyboardInterrupt exception.
```py
>>> while True:
...     try:
...         x = int(input("Please enter a number: "))
...         break
...     except ValueError:
...         print("Oops!  That was no valid number.  Try again...")
...
```
The try statement works as follows.
1. First, the try clause (the statement(s) between the try and except keywords) is executed.
2. If no exception occurs, the except clause is skipped and execution of the try statement is finished.
3. If an exception occurs during execution of the try clause, the rest of the clause is skipped. Then, if its type matches the exception named after the except keyword, the except clause is executed, and then execution continues after the try/except block.
4. If an exception occurs which does not match the exception named in the except clause, it is passed on to outer try statements; if no handler is found, it is an unhandled exception and execution stops with a message as shown above.

A try statement may have more than one except clause, to specify handlers for different exceptions. At most one handler will be executed. Handlers only handle exceptions that occur in the corresponding try clause, not in other handlers of the same try statement. An except clause may name multiple exceptions as a parenthesized tuple, for example:
```py
... except (RuntimeError, TypeError, NameError):
...     pass
```
A class in an except clause is compatible with an exception if it is the same class or a base class thereof (but not the other way around — an except clause listing a derived class is not compatible with a base class). For example, the following code will print B, C, D in that order:
```py
class B(Exception):
    pass

class C(B):
    pass

class D(C):
    pass

for cls in [B, C, D]:
    try:
        raise cls()
    except D:
        print("D")
    except C:
        print("C")
    except B:
        print("B")
```
Note that if the except clauses were reversed (with except B first), it would have printed B, B, B — the first matching except clause is triggered.

All exceptions inherit from BaseException, and so it can be used to serve as a wildcard. Use this with extreme caution, since it is easy to mask a real programming error in this way! It can also be used to print an error message and then re-raise the exception (allowing a caller to handle the exception as well):
```py
import sys

try:
    f = open('myfile.txt')
    s = f.readline()
    i = int(s.strip())
except OSError as err:
    print("OS error: {0}".format(err))
except ValueError:
    print("Could not convert data to an integer.")
except BaseException as err:
    print(f"Unexpected {err=}, {type(err)=}")
    raise
```
Alternatively the last except clause may omit the exception name(s), however the exception value must then be retrieved from sys.exc_info()[1].

The try … except statement has an optional else clause, which, when present, must follow all except clauses. It is useful for code that must be executed if the try clause does not raise an exception. For example:
```py
for arg in sys.argv[1:]:
    try:
        f = open(arg, 'r')
    except OSError:
        print('cannot open', arg)
    else:
        print(arg, 'has', len(f.readlines()), 'lines')
        f.close()
```
The use of the else clause is better than adding additional code to the try clause because it avoids accidentally catching an exception that wasn’t raised by the code being protected by the try … except statement.

When an exception occurs, it may have an associated value, also known as the exception’s argument. The presence and type of the argument depend on the exception type.

The except clause may specify a variable after the exception name. The variable is bound to an exception instance with the arguments stored in instance.args. For convenience, the exception instance defines __str__() so the arguments can be printed directly without having to reference .args. One may also instantiate an exception first before raising it and add any attributes to it as desired.
```py
>>> try:
...     raise Exception('spam', 'eggs')
... except Exception as inst:
...     print(type(inst))    # the exception instance
...     print(inst.args)     # arguments stored in .args
...     print(inst)          # __str__ allows args to be printed directly,
...                          # but may be overridden in exception subclasses
...     x, y = inst.args     # unpack args
...     print('x =', x)
...     print('y =', y)
...
<class 'Exception'>
('spam', 'eggs')
('spam', 'eggs')
x = spam
y = eggs
```
If an exception has arguments, they are printed as the last part (‘detail’) of the message for unhandled exceptions.

Exception handlers don’t just handle exceptions if they occur immediately in the try clause, but also if they occur inside functions that are called (even indirectly) in the try clause. For example:
```py
>>> def this_fails():
...     x = 1/0
...
>>> try:
...     this_fails()
... except ZeroDivisionError as err:
...     print('Handling run-time error:', err)
...
Handling run-time error: division by zero
```
# 5.8. MODULES
A module allows you to logically organize your Python code. Grouping related code into a module makes the code easier to understand and use. A module is a Python object with arbitrarily named attributes that you can bind and reference.
If you quit from the Python interpreter and enter it again, the definitions you have made (functions and variables) are lost. Therefore, if you want to write a somewhat longer program, you are better off using a text editor to prepare the input for the interpreter and running it with that file as input instead. This is known as creating a script. As your program gets longer, you may want to split it into several files for easier maintenance. You may also want to use a handy function that you’ve written in several programs without copying its definition into each program.

To support this, Python has a way to put definitions in a file and use them in a script or in an interactive instance of the interpreter. Such a file is called a module; definitions from a module can be imported into other modules or into the main module (the collection of variables that you have access to in a script executed at the top level and in calculator mode).

A module is a file containing Python definitions and statements. The file name is the module name with the suffix .py appended. Within a module, the module’s name (as a string) is available as the value of the global variable __name__. For instance, use your favorite text editor to create a file called fibo.py in the current directory with the following contents:
# Fibonacci numbers module
```py
def fib(n):    # write Fibonacci series up to n
    a, b = 0, 1
    while a < n:
        print(a, end=' ')
        a, b = b, a+b
    print()

def fib2(n):   # return Fibonacci series up to n
    result = []
    a, b = 0, 1
    while a < n:
        result.append(a)
        a, b = b, a+b
    return result
```
Now enter the Python interpreter and import this module with the following command:
```py
>>> import fibo
```
This does not enter the names of the functions defined in fibo directly in the current symbol table; it only enters the module name fibo there. Using the module name you can access the functions:
```py
>>> fibo.fib(1000)
0 1 1 2 3 5 8 13 21 34 55 89 144 233 377 610 987
>>> fibo.fib2(100)
[0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89]
>>> fibo.__name__
'fibo'
```
If you intend to use a function often you can assign it to a local name:
```py
>>> fib = fibo.fib
>>> fib(500)
0 1 1 2 3 5 8 13 21 34 55 89 144 233 377
```
# Standard Modules
Python comes with a library of standard modules, described in a separate document, the Python Library Reference (“Library Reference” hereafter). Some modules are built into the interpreter; these provide access to operations that are not part of the core of the language but are nevertheless built in, either for efficiency or to provide access to operating system primitives such as system calls. The set of such modules is a configuration option which also depends on the underlying platform. For example, the winreg module is only provided on Windows systems. One particular module deserves some attention: sys, which is built into every Python interpreter. The variables sys.ps1 and sys.ps2 define the strings used as primary and secondary prompts:
```py
>>> import sys
>>> sys.ps1
'>>> '
>>> sys.ps2
'... '
>>> sys.ps1 = 'C> '
C> print('Yuck!')
Yuck!
C>
```
These two variables are only defined if the interpreter is in interactive mode.

The variable sys.path is a list of strings that determines the interpreter’s search path for modules. It is initialized to a default path taken from the environment variable PYTHONPATH, or from a built-in default if PYTHONPATH is not set. You can modify it using standard list operations:
```py
>>> import sys
>>> sys.path.append('/ufs/guido/lib/python')
```
# 5.9. PACKAGES
Packages are a way of structuring Python’s module namespace by using “dotted module names”. For example, the module name A.B designates a submodule named B in a package named A. Just like the use of modules saves the authors of different modules from having to worry about each other’s global variable names, the use of dotted module names saves the authors of multi-module packages like NumPy or Pillow from having to worry about each other’s module names.

Suppose you want to design a collection of modules (a “package”) for the uniform handling of sound files and sound data. There are many different sound file formats (usually recognized by their extension, for example: .wav, .aiff, .au), so you may need to create and maintain a growing collection of modules for the conversion between the various file formats. There are also many different operations you might want to perform on sound data (such as mixing, adding echo, applying an equalizer function, creating an artificial stereo effect), so in addition you will be writing a never-ending stream of modules to perform these operations. Here’s a possible structure for your package (expressed in terms of a hierarchical filesystem):
```
sound/                          Top-level package
      __init__.py               Initialize the sound package
      formats/                  Subpackage for file format conversions
              __init__.py
              wavread.py
              wavwrite.py
              aiffread.py
              aiffwrite.py
              auread.py
              auwrite.py
              ...
      effects/                  Subpackage for sound effects
              __init__.py
              echo.py
              surround.py
              reverse.py
              ...
      filters/                  Subpackage for filters
              __init__.py
              equalizer.py
              vocoder.py
              karaoke.py
              ...
```
When importing the package, Python searches through the directories on sys.path looking for the package subdirectory.

The __init__.py files are required to make Python treat directories containing the file as packages. This prevents directories with a common name, such as string, unintentionally hiding valid modules that occur later on the module search path. In the simplest case, __init__.py can just be an empty file, but it can also execute initialization code for the package or set the __all__ variable, described later.

Users of the package can import individual modules from the package, for example:
```py
import sound.effects.echo
```
This loads the submodule sound.effects.echo. It must be referenced with its full name.
```py
sound.effects.echo.echofilter(input, output, delay=0.7, atten=4)
```
An alternative way of importing the submodule is:
```py
from sound.effects import echo
```
This also loads the submodule echo, and makes it available without its package prefix, so it can be used as follows:
```py
echo.echofilter(input, output, delay=0.7, atten=4)
```
Yet another variation is to import the desired function or variable directly:
```py
from sound.effects.echo import echofilter
```
Again, this loads the submodule echo, but this makes its function echofilter() directly available:
```py
echofilter(input, output, delay=0.7, atten=4)
```
Note that when using from package import item, the item can be either a submodule (or subpackage) of the package, or some other name defined in the package, like a function, class or variable. The import statement first tests whether the item is defined in the package; if not, it assumes it is a module and attempts to load it. If it fails to find it, an ImportError exception is raised.

Contrarily, when using syntax like import item.subitem.subsubitem, each item except for the last must be a package; the last item can be a module or a package but can’t be a class or function or variable defined in the previous item.










