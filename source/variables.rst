Variables
*********
Variables are a way to temporarily store data. Think of it as the same as variables in your math class where you can define
x = 5

Defining and Using Variables
============================
Before you can use a variable in a PBASIC program you must declare it. "Declare" means letting the BASIC Stamp know that
you plan to use a variable. The format for declaring variables is as follows
::
        variable_name    VAR     VarType


VarType refers to the following 4 values: **Bit**, **Nib**, **Byte**, and **Word**. Try to think of a variable type as classifying how much
space the variable has to store values.

========    ===========
VarType     Value Size
========    ===========
Bit         Value can be 0 or 1
Nib         Value can be 0 to 15
Byte        Value can be 0 to 255
Word        Value can be 0 to 65535
========    ===========

Here's an analogy of how the size difference works
++++++++++++++++++++++++++++++++++++++++++++++++++
We can arrange these 4 objects in order by how much they can store: Envelope, Shoebox, Fridge, Room
::
        Envelope (Bit) < Shoebox (Nib) < Fridge (Byte) < Room (Word)

Some examples of declaring variables
++++++++++++++++++++++++++++++++++++
Choose variable names that make sense to you and are not absurd like: ThisVariable_DoessomethingreallyCOOL
::
        x               VAR     Bit
        dog             VAR     WORD
        is_zero         VAR     Nib
        someVariable    VAR     Byte


Some Notes on Variable Types
============================
Under certain situations you might use different variable types. However, for the programming problems that you will
encounter while undergoing the competition it might be best to just stick to **Byte** and **Word**
