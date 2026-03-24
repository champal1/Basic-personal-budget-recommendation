# Basic-personal-budget-recommendation
Hello My name is Alejandro and I am a Computer Science major. Currently studying at Foothill College, waiting to be accepted to UCSC in Fall 2026.
This is a project for my future job at Intuit. I've created a basic money budget tracker and to generate recommendations based on different number of users that spend similar to what the user typed.

Built for Intuit Software Engineer 1

Creator: Alejandro Vargas 

School: Foothill College 

Course: Math 2BL (Linear Algebra Lab) by Jeff Anderson

Project Overview:

This project will demonstrate pratical application of linear algebra concepts, which consisit of:

-Analyze spending in 7 different categories

-Find similar users using linear algebra concepts like cosine similarity

-Display recommendations based on other users spending

-Generate a graph to visuallize the spending for each category between user and other users

-Display the results to user

-Transfer all the results into a text file as a receipt for the user

Example Visual:

Below is the example output:

Hello welcome to your budget tracker!

Lets focus on how much money you want to save this month

Lets get started, how much money have you made this month:$ 2000.00

You entered: $2000.00

What percent of the money do you want to save?:% 20

You want to save 20.0%, which is $400.00

Great! You plan on spending $1600.00 this month!

Now lets breakdown how much you spend on these categories

How much do you spend on groceries: $200

How much do you spend on bills: $250

How much do you spend on entertainment: $150

How much do you spend on shopping: $300

How much do you spend on gas: $100

How much do you spend on dinning: $200

How much do you spend on other stuff not mentioned: $600

You have spent a total of $1800.0!

You overspend by $200.00

Let me find recommendations on where to save based on other users...

Comparing to other users

Here is the number of user 13 

Now finding users similar spending as you

Now calulating cosine similarity with each user

User 1, half similar

User 2, pretty similar

User 3, pretty similar

User 4, half similar

User 5, pretty similar

User 6, pretty similar

User 7, half similar

User 8, half similar

User 9, pretty similar

User 10, half similar

User 11, pretty similar

User 12, half similar

User 13, half similar

The users similar to you are User 2 , User 3 , User 5 , User 6 , User 9 , User 11

Now that we did all the proper calculations, lets display the final results

Here is how much you spend on each category [200. 250. 150. 300. 100. 200. 600.]

Breakdown:

 Grocery  = $200.0
 
 Bills    = $250.0
 
 Entertainment = $150.0
 
 Shopping = $300.0
 
 Gas      = $100.0
 
 Dinning  = $200.0
 
 Other    = $600.0
 
Here is the average from the users that are similar to me $[280.5  301.5  238.   248.83  57.   210.   540.67]

Grocery: = 280.50

Bills: = 301.50

Entertainment: = 238.00

Shopping: = 248.83

Gas: = 57.00

Dinning: = 210.00

Other: = 540.67

Calculating and finalizing the difference between similar users to mine by category

Here is the data after finalizing the vector subtraction:

Grocery: $-80.50

Grocery your doing great, the average for this category $280.5

Bills: $-51.50

Bills your doing great, the average for this category $301.5

Entertainment: $-88.00

Entertainment your doing great, the average for this category $238.0

Shopping: $51.17

Shopping looks like you need to cut $51.17

You are spending $300.00, Similar users are spending: $248.83

Gas: $43.00

Gas looks like you need to cut $43.00

You are spending $100.00, Similar users are spending: $57.00

Dinning: $-10.00

Dinning your doing great, the average for this category $210.0

Other: $59.33

Other looks like you need to cut $59.33

You are spending $600.00, Similar users are spending: $540.67

You could save a total of 153.50 per month

Loading graph for comparison

------------------------------

Budget Summary

------------------------------

Income for the month: $2000.00

How much you planned to spend: $1600.00

Which means you want to save: $400.00

Here is how much you actually spend: $1800.00

You overspend by: $200.00

Users analyzed: 13

Similar users found: 6

The average spending: $1876.50

Below is the example graph visual using matplot:

<img width="1994" height="1113" alt="Screenshot (93)" src="https://github.com/user-attachments/assets/0ff67c09-dc54-4cb5-b077-8fe509dbacdf" />


Below is the text file receipt:

Budget Summary

Income for the month: $2000.00

How much you planned to spend: $1700.00

Which means you want to save: $300.00

Here is how much you actually spend: $1305.00

You under spend by: $395.00

Users analyzed: 8

Similar users found: 1


Linear Alegebra Implementation:

1. Vector Model
   -Display each category in a 7 dimension vector and store the users response also in a 7 dimension vector, using array
   spending vector = groceries, bills, entertainment, shopping, gas, dining, other
   my_data_as_vector(my_vector_list
   np.array(my_vector_list)

2. Dot Product
   -compare spending between the users and your inputs, by specific category
   formula: a x b = a1 x b1 + a2 x b2 +... + a7 x b7
   dot_results = np.dot(vector_a,vector_b)
   results = np.dot(my_spending_list,user_sp)

3. Vector Norms
   -Calculate magnitude and helps determine the similarity between vectors
   Equation: || x ||2 = square root (x^2 1 + x^2 2 + x^2 3 + ... x^2n)
   vector_norm(vector_x)
   mag = np.linalg.norm(vector_x)

4. Cosine Simularity
   -measure the similar between the other users results from mine, between 0-1, 0 not similar and 1 identical
   sim = (a,b) = a x b / ||a|| x ||b||
   cosine_sim(vector_a, vector_b)

5. Scalar Multiplication and vector addiction
   After calculating the users with cosine above 0.8, average the remaining users spending
     average = (1/n) x (v1 + v2 + v3 ... + vn)
     average_spending_users = np.round(add_array_users / many_user, 2)

6. Vector subtraction
    -After getting the average of the users for each category, now subtract it with my results for each category
     difference = my spending - average users spending
     vector_sub = my_spending_list5 - average_spending_users

Detailed overview:

Ask user for their monthly income and how much they want to save, then ask how much they spend on average for 7 categories

Convert the inputs into 7D numpy arrray

Generate random number of users ranging from 5-30 with realistic spending patterns for each category

Then add the other users and find the average by using dot product, vector norms and cosine simularity,

  - if cosine sim is 0.8 or above and saving percent within the same range as user, keep

Average the similar users spending using scalar multiplation and vector addiction

After getting the average for each category, subtract user and the other users average spending to find where to cut spending

Print out the results, use verbose it hide the math from user, only print the important information, what the user wants to see

Display bar graph of the spending for each category

Print results into a text file as a receipt

