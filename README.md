# The Guilty Project
A Python app that makes a daily forecast on how much the user is expected to spend that month based on their spending so far and sends an email notification to the user if the forecasted amount is more than their budget saying they should spend only 'x' amount today if they want to get back on track with their budget. 

The app is made with streamlit, firebase and the nordigen (Gocardless) API.

## How the app works

The app is designed as a web application and is made with streamlit due to its simple and easy nature. Users can sign up for the app by providing info on their budget, email address and connecting their bank account to track and receive emails when their forecasted spending for the month exceeds their budget, along with how much they should spend that day to get back on track with spending under budget. 

- The app uses nordigen (GoCardless) to connect to the users' bank accounts, and store authentication tokens and user info during the onboarding process in firebase.
- Once signed up, the user will receive an onboarding email giving instructions on how the forecasting is calculated when they will typically receive emails and the conetents of the email (such as expected monthly spend, how much to spend that day to get back on track, and what to do if they have unavoidable incoming expenses)
- Users can log in to the web app after signing up to change their settings, such as - email, username, budget amount, pay date, etc...

### The Forecasting process
- The amount of money spent in the last 7 days divided by 7 provides the **average spending rate**, which is multiplied by the days remaining in the budget month to forecast the money spent that month.
- When calculating the total money spent in a time period, if 'x' pounds are spent from the bank account and 'x' pounds are sent to the bank account, then it is considered as no money spent. This is to take into account friends splitting bills, and paying back any previous expenses
- No transaction with a value above 15% of the total budget is taken into account when calculating total money spent, as usually these are miscellaneous transactions that are not part of the monthly budgets (like tuition expenses, rent, etc...)

### Distribution
The program is primarily distributed as a web app that users can access on: <a href="URL> https:// </a>


## Challenges

- Finding a suitable library to connect to the user's bank data was difficult as it needed to be both simple and cost-effective for an open-source free-to-use project. Among many other options (ex: Plaid, TrueLayer) Nordigen was the the best fit in these categories.
- With the same metrics of simplicity and cost-effectiveness in mind, I wanted an easy low-code/no-code front-end solution to showcase the web app. Unlike most options (bubble io, flutter, javascript), streamlit was the best option I could find.
- There was also a struggle with deciding if the program should be a web app, a flutter-based mobile app, or something else. But nothing was as effective as combining a signup page and an email system, instead of a full-scale app.


## Features for the future
- Display all transactions and select transactions that are not part of the budget to exclude them from all calculations
- AI-generated memes/jokes in the email to motivate the user into spending less (ex: A roasting joke on the state of their bank account)
- Offer discounts and deals from famous vendors to satisfy cravings and help reduce spending


