.. highlight:: basic
   :linenothreshold: 3

Do Loops
********

Lets say you want to do something forever... in programming you would use a
do-loop to perform this action!

Here's a basic example that constantly prints to the terminal:
::
        DO
            DEBUG "Hi there!", CR
        LOOP

Here's another example that prints the value of x and increases its value:
::
        x   VAR     WORD

        Init:
            x = 1
        Main:
            DO
                DEBUG DEC ? x, CR
                x = x + 1
            LOOP

DO-WHILE loop
=============

However, more often than not you will want to test some condition to determine
whether the loop code should run or continue to run.

To do this we use a DO-WHILE loop like so:
::
        x   VAR     WORD

        Init:
            x = 1
        Main:
            DO WHILE (x <= 5) ' condition to test before entering loop statements
                DEBUG "#", CR
                x = x + 1
            LOOP

Conclusion
==========

DO loops are useful when you need to run something forever or until some special condition breaks.

For an imaginary example:
::
        Main:
            DO WHILE (some_special_condition = 1)
                ' Do some calculations
            LOOP
