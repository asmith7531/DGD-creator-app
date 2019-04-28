# DGD-creator-app
<hr>
Im going to try and take the DGD-generator repository and make it into a node application so I can write the output as a text file to the local machine, and hopefully add application features and maybe a UI in the future.

#Dependencies
<hr>
-Lodash
-Inquirer

#PsuedoCode
<hr><hr>
This program will automate the creation of Dangerous Goods Shipping Documents per EMD specifications.

VARIABLES
<hr>
Input Variables
-PO#'s
-lot #
-# of bottles per lot #
-box size
-address

Output Variables
-box volumes and quantities
-most cost efficient overpack
-box weights
-box dimensions

LOGICAL RULES
<hr>
-Box size bottle rules:

    4x1:  4 bottles @ 3.785 liters each

    2x1:  2 bottles @ 10 liters each

    4x4:  4 bottles @ 4 liters each

    6x1:  6 bottles @ 1 liter each

    ****2 quart sized boxes 2 bottles @ 1 liter each

-Overpack rules
XL=27 4x1 boxes
L=18 4x1 boxes
S=8 4x1 boxes

PLAN
<hr>
Input form takes in the input variables

  -PO#s are pushed to an array and console logged out

  -# of bottles gets stored as a variable and divided by the number of bottles per box

    -the remainder tells us if there is/are incomplete boxes

    -keep the bottles separate by lot #

  -box size tells us how many bottles per box and how many boxes per overpack

  -address is stored as a string and pushed to a matrix
