# The Guilty Project
A Python app that makes a forecast every day on how much the user will spend in that month based on their spending so far in the month and sends an email notification to them if the forecast is more than their budget, saying they should spend only 'x' amount today if they want to get back on track with their budget. 

The app is made with streamlit, firebase and the nordigen (Gocardless) API.

## How the app works

The app is designed as a web application and is made with streamlit due to its simple and easy nature. Users can sign up for the app by providing info on their budget, email address and connecting their bank account to track and receive emails when their forecasted spending for the month exceeds their budget, along with how much they should spend that day to get back on track with spending under budget. 

- The app uses nordigen (GoCardless) to connect to the users bank account, and store authentication tokens and user info during the oboarding process in firebase.
- Once signed up, the user will receive an onboarding email giving instructions on how the forecasting is calculated, when they will typically receive emails and the conetents of the email (such as expected monthly spend, how much to spend that day to get back on track, and what to do if they have unavoidable incoming expenses)
- Users can log in to the web app after signing up to change their settings, such as - email, username, budget amount, pay date, etc...

## Distribution & Use
The program is primarily distributed as a web app that users can access here: <a href="URL> https:// </a>

## Challenges
- Finding a suitable library to connect to the user's bank data was difficult as it needed to be both simple and cost-effective for an open-source free-to-use project. Among many other options (ex: Plaid, TrueLayer) Nordigen was the the best fit in these categories.
- With the same metrics of simplicity and cost-effectiveness in mind, I wanted an easy low-code/no-code front-end solution to showcase the web app. Unlike most options (bubble io, flutter, javascript), streamlit was the best option I could find.

Features you hope to implement in the future



