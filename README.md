Download Link: https://assignmentchef.com/product/solved-csci1300-1310-assignment-3-the-concept-of-program-decomposition
<br>



<ol>

 <li>Applying the concept of program decomposition.</li>

 <li>Implement fundamental programming constructs, such as variables, expressions, conditionals, and iterative control structures.</li>

 <li>Become acquainted with simple file I/O commands.</li>

 <li>Design functions in program construction, and understand parameter passing and return values.</li>

</ol>

Read the entire assignment carefully before beginning. In this assignment, you’re going to develop a simulated community message board where users can post items they have for sale or search for items they want to buy. Your program will search for matches, e.g. there is a bike for sale for $50 and a bike wanted, where the buyer will pay up to $60, and remove items from the message board as they are sold. Users have the option of posting and searching for as many items as they choose before they quit the program.




<h2>Getting started</h2>

Your program should display a menu with the following selections:

<ol>

 <li>Insert an item.</li>

 <li>Search for an item.</li>

 <li>Print the message board.</li>

 <li></li>

</ol>




Use the following C++ print and input statements for your menu:




cout &lt;&lt; “1. Insert an item.” &lt;&lt; endl; cout &lt;&lt; “2. Search for an item.” &lt;&lt; endl; cout &lt;&lt; “3. Print the message board.” &lt;&lt; endl;

cout &lt;&lt; “4. Quit.”&lt;&lt; endl; getline(myFile, choice);




​                             Note: the <em>getline</em>​ () command assumes you have a variable called “choice” defined and that it’s a string. This menu should be displayed after every transaction is complete unless the user selects Quit. The user can select the option they want using the number for the option. For example, to add an item, they type 1.




<h2>Item types</h2>

There are only five types of items: bike, microwave, dresser, truck and chicken. When you prompt the user, your prompt needs to include the exact text shown here:




“Enter the item type-b,m,d,t,c:”

“Enter the item cost:”




The user types the first letter of the item type to indicate the type they want to add.




Data in the message board is stored as a 2D array. One dimension of the array is the number of items in the message board and the other dimension is the parameters for each item. Each item on the message board contains the type and the cost.




​                 Assume you have an array called <em>msgBoard</em>​ and you want to store the following three items.




bike, $50 truck, $1000

microwave, $10




Your array would look like




msgBoard[0][0] = ‘b’; msgBoard[0][1] = ‘50’; msgBoard[1][0] = ‘t’; msgBoard[1][1] = ‘1000’; msgBoard[2][0] = ‘m’;

msgBoard[2][1] = ‘10’;




<strong>All values are stored as strings in this example.  </strong>




<h2>Insert an item</h2>

If the user selects 1 to add an item, they should be prompted for the type of item to add and the cost of the item. When an element is added to the message board array, it should be added at the first available position. Don’t sort the data, we will be running test cases with expected output for each input. Duplicates are also okay.




<h2>Search for an item</h2>

When the user selects 2 to find an item, they should be prompted with the item type, and the maximum price they are willing to pay for the item. Your code should then search the array and return the first item with the correct type and a cost that is less than or equal to the price that the user will pay.




Use the following text in your prompts:




“Enter the item type-b,m,d,t,c:”

“Enter the maximum item cost:”




For example, if the user types b and 50, they want a bicycle and are willing to pay up to $50 for it. Your program should find the first bicycle in the list that sells for $50 or less.




If a match is found, print “Sold &lt;type&gt;for&lt;cost&gt;”




<h2>                                   The <em>type</em>​ is one of the following: bike, microwave, dresser, truck, ​ or​ chicken​ .​</h2>




The <em>cost</em>​ is the actual item cost, not what the user is willing to pay.




The item should then be deleted from the array.




If the item is not found, print “Item not found”.




Note: if your values are stored as strings, they will need to be cast as integers to compare price values. You will also need to convert the type values stored in the array to nice, understandable values. For example, ‘b’ needs to be displayed as ‘bike’.




<h2>Print the message board</h2>

If the user selects Print the message board, your program should display the items in the message board array in the following format:




&lt;type&gt;: &lt;cost&gt;




<h2>Quit</h2>

If the user selects 4 for Quit, the program should exit the while loop that controls the program, which will cause the program to exit.




<h2>Implementation details</h2>

There are a few requirements for your program that you need to meet to receive full credit.




<ol>

 <li>Your array needs to be big enough to store 20 items.</li>

 <li>You need to have functions for inserting to the message board, searching the message board, and printing the message board.</li>

 <li>Your text you display in your menu and other outputs need to match the text given in this document.</li>

</ol>




<h2>Breaking down the problem</h2>

This assignment is our first assignment this semester that is one large problem instead of two or three small problems. If you’ve read the assignment write-up and you’re not sure where to start, it can be helpful to think of the problem in stages and complete each stage before moving on to the next stage. Here is a suggested approach for breaking down this problem into smaller problems.




<ol>

 <li>Build the main menu. Write the loop that asks for user input and test that your menu recognizes the four user options to Insert, Search, Print, and Quit. In your code, you can print which menu item is selected to test that you menu code is working. Be sure to remove these print statements later once you’ve developed the real code for the menu item.</li>

 <li>Build the sub-menus. The Insert and Search menu items have sub-menus that are displayed when the user selects that menu item. Build and test your sub-menus using print statements to verify which sub-menu was selected. Again, make sure you remove the print statements once you develop the real code for the sub-menu item.</li>

 <li>Initialize the array to hold the message board data. The list should be initialized outside of your menu loop.</li>

 <li>Build the code to add items to the array. This code needs to use the user inputs for the type and cost of the item, and add them to the array in the appropriate index.</li>

 <li>Build the code to find items in the array and delete them from the array if the item is found. This code should be located under the find menu item and use the inputs from the user.</li>

 <li>Build the code to print the array that runs when the print menu option is selected.</li>

 <li>If your main menu loop doesn’t already handle the Quit functionality, modify the menu loop to quit the program when the user selects Quit.</li>

 <li>Do a happy dance.</li>

</ol>