.. highlight:: basic
   :linenothreshold: 3

FOR Loops
*********

For loops are a little different than do-loops. For loops were created with the purpose
in mind of having a program execute between a range. That range is defined by you!

Here's an example that counts from 0 to 10:
::
        x   VAR     WORD

        Main:
            FOR x = 0 TO 10
                DEBUG DEC ? x, CR
            NEXT
            END

By default, a FOR loop will step through 1 by 1. We can change this behavior by
adding a specific value for STEP.

Here the example counts from 0 to 10 but increasing by STEPS of 2:
::
        x   VAR     WORD

        Main:
            FOR x = 0 TO 10 STEP 2
                DEBUG DEC ? x, CR
            NEXT
            END

Notice how only even numbers are being displayed!

We can also make a FOR loop that decreases in range.
Here's what I mean:
::
        Main:
            FOR 10 TO 5
                DEBUG "Hello!"
            NEXT
            END

Conclusion
==========

FOR loops are very useful when you know there should be a range where a program should
run. If we need to run something 10 times then it would be useful to use a FOR loop as
its easy to create.

Take this for example, printing 1 to 10 by hand:
::
        Main:
            DEBUG "1"
            DEBUG "2"
            DEBUG "3"
            DEBUG "4"
            DEBUG "5"
            DEBUG "6"
            DEBUG "7"
            DEBUG "8"
            DEBUG "9"
            DEBUG "10"
            END

**VS**

Printing 1 to 10 using a for loop:
::
        x   VAR     WORD

        Main:
            FOR x = 1 to 10
                DEBUG DEC x
            NEXT
            END
