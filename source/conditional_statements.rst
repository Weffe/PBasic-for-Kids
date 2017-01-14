..  toctree::
    :maxdepth: 3
    :numbered:
    Conditional Statements
    Chaining mutliple IF.. THEN statements together

Conditional Statements
**********************
Conditional statement are used as a way to direct the way things operate. For example, if I say "Please go to the store to
buy milk. If they don't have milk then buy apple juice".

Notice how If there isn't milk then we buy apple juice. However if there IS milk then we buy milk. This type of conditional statements
are ordered like this in PBasic:

::
        IF (*condition*) THEN
            *statement(s)*


A condition is made up of comparison symbols

==========================  ==========
Comparison Operator Symbol	Definition
==========================  ==========
=	                        Equal
<>	                        Not Equal
>	                        Greater Than
<	                        Less Than
>=	                        Greater Than or Equal To
<=	                        Less Than or Equal To
==========================  ==========


**Here are some examples:**
::
        IF (4 = 5) THEN
            DEBUG "4 equals 5"
        ENDIF

        IF (10 <= 100) THEN
            DEBUG "10 is less than or equal to 100"
        ENDIF


Chaining mutliple IF.. THEN statements together
===============================================
You can also call chain multiple IF.. THEN statements together through the use of IF.. ELSEIF.. and/or ELSE..

**Structure for Multiple If statements:**
::
        IF (condition) THEN
            statement(s)
        ELSEIF (condition) THEN
            statement(s)
        ELSE
            statement(s)
        ENDIF


**Example:**
::
    x   VAR     WORD

    Main:
        x = 100

        IF (x < 200) THEN
            DEBUG DEC ? x
        ELSEIF (x < 50) THEN
            DEBUG DEC ? x
        ELSE
            DEBUG DEC ? x
        ENDIF

**Notes about Mutliple If statements**
It's not necessary to have an ELSE statement at the end. If it's omitted then the statement will stop at the last ELSEIF statement instead.

Also you have the ability to nest statements inside of each other like so:
::
        x   VAR     WORD

        Main:
            x = 5

            IF (x < 10) THEN
                IF (x > 5) THEN
                    DEBUG "x is between 5 and 10"
                    DEBUG ? x

