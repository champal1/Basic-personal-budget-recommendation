# Basic-personal-budget-recommendation
Hello My name is Alejandro and I am a Computer Science major. Currently studying at Foothill College, waiting to be accepted to UCSC in Fall 2026.
This is a project for my future job at Intuit. I've created a basic money budget tracker and to generate recommendations based on different number of users that spend similar to what the user typed. 
Built by: Alejandro Vargas | Foothill College | Math 2BL (Linear Algebra Lab) by Jeff Anderson

Project Overview:

This project will demonstrate pratical application of linear algebra concepts, which consisit of:

-Analyze spending in 7 different categories
-Find similar users using linear algebra concepts like cosine similarity
-Display recommendations based on other users spending
-Generate a graph to visuallize the spending for each category between user and other users
-Store all the results into a txt file as a receipt 

Example Visual:

Below is the example output:

Hello welcome to your budget tracker!
Lets focus on how much money you want to save this month
Lets get started, how much money have you made this month:$ 2000.00
You entered: $2000.00
What percent of the money do you want to save?:% 15
You want to save 15.0%, which is $300.00
Great! You plan on spending $1700.00 this month!
Now lets breakdown how much you spend on these categories
How much do you spend on groceries: $160
How much do you spend on bills: $200
How much do you spend on entertainment: $170
How much do you spend on shopping: $200
How much do you spend on gas: $90
How much do you spend on dinning: $190
How much do you spend on other stuff not mentioned: $490
You have spent a total of $1500.0!
You spend less than expected by $200.00
Comparing to other users
Here is the number of user 12 
Now finding users similar spending as you
Now calulating cosine similarity with each user
User 1, half similar
User 2, half similar
User 3, half similar
User 4, half similar
User 5, pretty similar
User 6, half similar
User 7, half similar
User 8, pretty similar
User 9, half similar
User 10, pretty similar
User 11, half similar
User 12, half similar
The users similar to you are User 5 , User 8 , User 10
Now that we did all the proper calculations, lets display the final results
Here is how much you spend on each category [160. 200. 170. 200.  90. 190. 490.]
Breakdown:
 Grocery  = $160.0
 Bills    = $200.0
 Entertainment = $170.0
 Shopping = $200.0
 Gas      = $90.0
 Dinning  = $190.0
 Other    = $490.0
Here is the average from the users that are similar to me [138.33 446.   227.33 264.67  57.67 349.33 272.67]
Grocery: = 138.33
Bills: = 446.00
Entertainment: = 227.33
Shopping: = 264.67
Gas: = 57.67
Dinning: = 349.33
Other: = 272.67
Calculating and finalizing the difference between similar users to mine by category
Here is the data after finalizing the vector subtraction:
Grocery: $21.67
Grocery looks like you need to cut $21.67
You are spending 160.0, Similar user: 138.33
Bills: $-246.00
Bills your doing great, the average for this category $446.0
Entertainment: $-57.33
Entertainment your doing great, the average for this category $227.33
Shopping: $-64.67
Shopping your doing great, the average for this category $264.67
Gas: $32.33
Gas looks like you need to cut $32.33
You are spending 90.0, Similar user: 57.67
Dinning: $-159.33
Dinning your doing great, the average for this category $349.33
Other: $217.33
Other looks like you need to cut $217.33
You are spending 490.0, Similar user: 272.67
You could save a total of 271.33 per month
Loading graph for comparison
============================================================
Budget Summary
============================================================
Income for the month: $2000.00
How much you planned to spend: $1700.00
Which means you want to save: $300.00
Here is how much you actually spend: $1500.00
Looks like you underspend on this category, great!
Here are some possible recomendations
You under spend by: $200.00
Users analyzed: 12
Similar users found: 3
The average spending: $1756.00

Below is the example graph visual using matplot:

<img width="1989" height="1118" alt="Screenshot (90)" src="https://github.com/user-attachments/assets/a0bc4eb9-9c6e-4bae-9e73-72ed30bf3343" />

Breakdown of Linear Alegebra concepts used:

1. 







