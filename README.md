# AWS Cost Alert System

## What this does
This project automatically sends me an email if my AWS spending goes above $10 in a month. No manual checking required. It runs on its own 24/7.

## Why I built this
As someone learning AWS, it is easy to accidentally leave services running and get charged without knowing. This system gives me a safety net so I always know what is happening with my bill.

## How it works
1. **AWS Budgets** monitors my account spending every day
2. When my bill crosses $10, Budgets fires a message to SNS
3. **Amazon SNS** receives that message and sends it to all subscribers
4. I get an **email alert** instantly

## AWS services used
- **AWS Budgets** monitors spending and triggers the alert
- **Amazon SNS (Simple Notification Service)** receives the trigger and sends the notification
- **Email subscription** delivers the alert to my inbox

## What I learned
- How AWS Budgets connects to SNS using an ARN
- The difference between SNS Standard and FIFO topics
- Why billing services have to be configured in us-east-1 specifically
- How to wire multiple AWS services together to create an automated workflow

## Status
Live and running on my AWS account.
