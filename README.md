# oumaima-gasmi-about-logistic-regression-Are-You-Ready-for-the-Zombie-Apocalypse-
Project Description It is no longer just a threat; it is now a reality! Zombies have been spotted all over the U.S. Work with your colleagues at the Centers for Disease Control and Prevention to identify the characteristics and supplies that seem to keep humans safe. Develop a logistic regression model that predicts the probability of becoming a zombie based on personal characteristics like age and sex, type of neighborhood people live in, and what emergency supplies are available. Practice bivariate tests like chi-squared and t-test to identify the most relevant variables for the model, develop and run the model, check model assumptions, and use the model to predict the probability of becoming a zombie for friends, family, and even yourself!  To complete this Project, you should be comfortable with basic data analysis in base R and visualization in ggplot2, and be familiar with chi-squared test, t-tests, and logistic regression.  The zombies dataset was created for this Project based on emergency preparedness recommendations. It consists of 200 observations and 14 variables. The variables include personal characteristics like age and sex, zombie status, a description of the neighborhood each participant lives in, and measures of supplies.




Project Tasks
1. ZOMBIES!
2. Compare zombies and humans
3. Compare zombies and humans (part 2)
4. Recode variables missing values
5. Selecting variables to predict zombie status
6. Build the model
7. Checking model assumptions
8. Interpreting assumptions and making predictions
9. What is your zombie probability?
10. Are you ready for the zombie apocalypse?


Task 1: Instructions
Load the zombie data and create a gallons-of-water-per-person variable.

Use read.csv() to bring in the data from datasets/zombies.csv and name it zombies.
Summarize zombies with the summary() command.
Create a water.person variable by dividing water by household.
Use summary() to check the new variable.
Good to know
This Project uses Base R functions and skills from Multiple and Logistic Regression, including estimating a logistic model, computing and interpreting odds ratios, predicting probabilities, and examining model fit.

Helpful links:

ggplot2 documentation
the apply() family functions DataCamp tutorial
more on the apply() functions at R-bloggers
You can reset the Project by clicking the circular arrow in the bottom-right corner of the screen if you are experiencing odd behavior. Resetting the Project will also discard all the code you have written so be sure to save it offline first.

Task 2: Instructions
Examine age and water per person by zombie status.

Load ggplot2 and gridExtra.
Plot age by zombie using ggplot() with geom_density(). Set alpha to 0.3 for transparency.
Plot water.person by zombie using ggplot() with geom_density(). Set alpha to 0.3 for transparency and add theme_minimal().
View both graphs with grid.arrange() from the gridExtra package.


Helpful links:
ggplot's themes documentation
ggplot's density plot documentation
gridExtra documentation



Task 3: Instructions
Determine the percentage of zombies for each category of the factor variables.

Use sapply() with is.factor() to create a data frame with only the factors.
Write a function to compute percent zombies and humans for each factor. Use lapply() to apply the function to zombies.factors.
Print the results.
In prop.table() use margin = 1 for row percents and margin = 2 for column percents.



Helpful links:

lapply() function documentation
sapply() function documentation
DataCamp course on Introduction to Function Writing in R


Task 4: Instructions
Recode missing values to appropriate categories for the clothing and document variables.

Add "No clothing" as a level of clothing and recode NA to "No clothing".
Add "No documents" as a level of documents and recode NA to "No documents".
Check recoding using summary() on zombies.

Helpful links:

The levels attribute of factor variables can be confusing, see the documentation for more information

Task 5: Instructions
Determine which characteristics are associated with zombie status.

Use sapply() and is.factor() to take a subset of factors in zombies.
Use lapply() to conduct chi-squared tests on variables in the zombies.factors subset with zombie.
Use t.test() to see if age and water.person are associated with zombie in the zombies data frame.
Examine chi-squared and t-test results.


Helpful links:

learn more about chisq.test()here
t.test() compares means across groups, see documentation
lapply() function documentation
sapply() function documentation
DataCamp course on Introduction to Function Writing in R



Task 6: Instructions
Develop and evaluate a logistic regression model.

Use the glm() command to model zombie.
Run odds.n.ends() to get model significance, fit, and odds ratios.
Print the results of odds.n.ends().
Helpful links:

odds.n.ends() package documentation
See the logistic regression chapter in the Multiple and Logistic Regression DataCamp course for more information

Task 7: Instructions
Check the no multicollinearity and linearity assumptions for the zombie model.

Load car and use vif() to check multicollinearity for zombie.model.
Calculate the logit of zombie to use for checking linearity.
Create scatter plots to check linearity for age and water.person. The arguments in geom_smooth() are the same for both plots.
Use grid.arrange() to view and examine both plots.

For linearity assumption checking, scatter plots will show two lines, a straight regression line and a curvy Loess curve, which captures more subtle localized detail. If the Loess curve is close to being straight, the relationship between x and y is linear. If it deviates a lot from being straight, the relationship is not linear.

Helpful links:

more about variance inflation factors from the vif() command
learn about Loess smoothing here and its use with ggplot() here


Task 8: Instructions
Use the model to predict the probability that two people are zombies.

Create a new data frame with data.frame() and enter the relevant data for the two people.
Use predict() on zombie.model to predict probabilities for the people in the new data frame.
Print the predicted probabilities.
Helpful links:

the base R predict() command documentation


Task 9: Instructions
Add your data to the newdata data frame and predict your zombie probability.

Add your data to the newdata data frame.
Use predict() to predict the probabilities for the newdata data frame.
Print the predictions to review your zombie probability!



Task 10: Instructions
How prepared are you?

What is your probability of becoming a zombie? Assign your probability of becoming a zombie to me.
How prepared are you for a real emergency? Assign one of the text lines below to preparedness_level.
"I got this!"
"Okay, but I should probably pick up a few emergency items at the store."
"I'm not going to fair well. Let's make an emergency kit!"

Helpful links: CDC preparedness website





















































