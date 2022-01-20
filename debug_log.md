# Debug Log

**Explain how you used the the techniques covered (Trace Forward, Trace Backward, Divide & Conquer) to uncover the bugs in each exercise. Be specific!**

In your explanations, you may want to answer:

- What is the expected vs. actual output?
- If there is a stack trace, what useful information does it contain?
- Which technique did you use, on which line numbers?
- What assumptions did you have about each line of code, and which ones were proven to be wrong?

_Example: I noticed that the program should show pizza orders once a new order is made, and that it wasn't showing any. So, I used the trace forward technique starting on line 13. I discovered the bug on line 27 was caused by a typo of 'pzza' instead of 'pizza'._

_Then I noticed another bug ..._

## Exercise 1

1. i installed the packages and immidiately ran the app
1. after submitting my order i run into an error stating that topping is an invalid argument for PizzaTopping
1. after locating PizzaTopping with cmd+f, i can spot the cause of the problem but have no idea what the app is trying to do with it
1. since PizzaTopping class didnt have "toppping" attr, i set the topping to topping_type on line 79 of app.py
1. there was redirect error saying could not build endpoint for / so i set it to home
1. an error i caught was the data wasnt committing into the DB so at line 82, a new line was created to commit the data
1. the console logged some parameters in which some didnt exist so an effort to correct the request id names were made
1. the method was wrong for /fulfill so it got changed from post to get
1. home.html still had the /fulfill method as post so i set it to get
1. pizza_id isnt obtained from the form but rather query from the URL so i changed request.form.get to request.args.get
1. there is another bug on line 78, 79 that appends toppings. The current issue is that it is appending from ToppingType rather than toppings_list but due to the relationship restriction on class Pizza, setting Pizza.toppings=toppings_list is impossible and iterating through toppings_list while "switch"-ing using ToppingType also seems impossible with my lack of python/flask knowledge

## Exercise 2

[[Your answer goes here!]]

## Exercise 3

[[Your answer goes here!]]
