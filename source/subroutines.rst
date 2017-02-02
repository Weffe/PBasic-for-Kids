.. highlight:: basic
   :linenothreshold: 3

Subroutines
***********

Imagine you have a "special piece of code" that's 10 lines long. And you have to
use it 7 times in your program. Now, it's not too hard to copy and paste but
one can imagine that having to paste 70 lines of the same code can be repetitive
and ultimately "ugly". Ugly in the sense that you shouldn't have to repeat yourself.

There is a rule in programming that goes: **DON'T REPEAT YOURSELF (DRY)**

With subroutines, you can use the same piece of code without copy and pasting.

The structure of a subroutine is as follows:
::
    YourSubroutineName:
        (Code)
    RETURN


Example
=======
::

    MySubroutine:
        DEBUG "Hello there!", CR
        DEBUG "This is a subroutine", CR
    RETURN

To call and execute a subroutine you use the **GOSUB** keyword:
::
    Main:
        DEBUG "We're inside Main... Calling MySubroutine", CR
        GOSUB MySubroutine
        END

    MySubroutine:
        DEBUG "Hello there!", CR
        DEBUG "This is a subroutine", CR
    RETURN

Calculating the area of a square
================================

We can use variables within subroutines like so:
::
    sideLength  VAR     WORD
    result      VAR     WORD

    Main:
        sideLength = 50
        GOSUB calcSquareArea

        sideLength = 75
        GOSUB calcSquareArea

        sideLength = 100
        GOSUB calcSquareArea

        END

    calcSquareArea:
        DEBUG DEC "Calculating Area with side legnth: ", sideLength, CR
        result = sideLength * sideLength ' area = l x w
        DEBUG DEC "Result: ", result, CR
    RETURN

Conclusion
==========

Subroutines are a good way to organize and cleanup your code. If you have parts
where you need to constantly repeat yourself than put it into a subroutine! There
is no limit to how many times you can call a subroutine.

Practice
========

Create a movement sequence again but this time using subroutines. You should notice
you're code should look a lot cleaner this time around.
