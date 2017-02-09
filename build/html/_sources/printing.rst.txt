.. highlight:: basic
   :linenothreshold: 3

Printing output to the Terminal
*******************************
**DEBUG** is used to print output to the computer screen while running your program. Think of it as a way to make sure things are
are running properly while your program runs.

**The easiest use case is regular messages:**
::
        DEBUG   "Hello, World!"
        DEBUG   "I'm learning how to program."

Using the comma seperator
=========================

We can have multiple messages added together on the same line by using the comma seperator:
::
        DEBUG   "Wow this is a", " multi message!"

Printing on new lines
=====================

**We can use the keyword (CR) to start on a new line. Think of it like pressing enter in Microsoft Word:**
::
        DEBUG   "This should be on", CR
        DEBUG   "multiple lines."

Printing variables
==================

**We can also print variables:**
::

    x   VAR     Word

    Init:
        x = 65

    Main:
        DEBUG x
        END

Uh oh! When trying to run the above code there should be an issue. It's printing the letter "A"?!
This is because by default the BS2 model displays everything as ASCII_ characters. I won't go into detail what ASCII is but
you can follow the link to read more.

..  _ASCII: https://en.wikipedia.org/wiki/ASCII

Anyways, in order to properly print the value of *x* we need to use the decimal formatter, **DEC**:
::

    x   VAR     Word

    Init:
        x = 65

    Main:
        DEBUG DEC x
        END

Auto-printing variables
=======================

**Using the keyword (?) we can auto-print the variable name and value:**
::

    x   VAR     Word

    Init:
        x = 65

    Main:
        DEBUG DEC ? x
        END

Example of combining everything together
========================================

::

        x   VAR     Word
        y   VAR     Word

        Init:
            x = 65
            y = 99
        Main:
            DEBUG DEC "Our value of x is: ", x, CR
            DEBUG DEC ? y
            END
