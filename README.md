# The Guilty Project
A Python app that makes a forecast every day on how much the user will spend in that month based on their spending so far in the month and sends an email notification to them if the forecast is more than their budget, saying they should spend only 'x' amount today if they want to get back on track with their budget. 

The app is made with streamlit, firebase and the nordigen (Gocardless) API.

## How the app works

The app is designed as a web application and is made with streamlit due to its simple and easy nature. Users can sign up for the app by providing info on their budget, email address and connecting their bank account to track and receive emails when their forecasted spending for the month exceeds their budget, along with how much they should spend that day to get back on track with spending under budget. 

- The app uses nordigen (GoCardless) to connect to the users bank account, and store authentication tokens and user info during the oboarding process in firebase.
- Once signed up, the user will receive an onboarding email giving instructions on how the forecasting is calculated, when they will typically receive emails and the conetents of the email (such as expected monthly spend, how much to spend that day to get back on track, and what to do if they have unavoidable incoming expenses) 

- including details on email system and metrics in report

How to build it

Use it for free on the website

Why you used the technologies you used

Some of the challenges you faced

Features you hope to implement in the future



