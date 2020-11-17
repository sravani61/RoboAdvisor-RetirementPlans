# Robo Advisor-Retirement Plans

Planning for retirement if not done at the right time can be a nightmare. This roboadvisor "Retirement Planning",
can be of little help in determining what king of portfolio can be picked for the risk tolerance level of the investor.

AWS services used:

1. Amazon lex

2. Lambda

3. s3

4. Cloudwatch


Using Lex:

The robo was build using the Lex service. Several intents are defined for the robo advisor to detect a need of conversation.

Fours slots for age, investment amount, name, and risk level are created and all the slots are marked rrequired for the assessment.

Several validation techniques are used for age and investment amount.

The robo is programmed to output the ideal portfolio weights for bonds and equities for the respective risk level.


Using Lambda:

The conversation between robo advisor and the python program is done using lambda.

The intended responses for the risk levels inputted are coded in the lambda function, so, that the investor can get the ideal bond and euity weeights for the investment portfolio.

Four test cases are used to check the lambda function, for negative value inputs and for out of bound inputs.


Using S3:

The icons used for the report card creation are saved in S3 and the public links for S3 are used as image URLs.


Using CloudWatch:

Excellent log keeper it is! While coding for data validations, CloudWatch came in extremely handy to check for errors and eventually create the best lambda function.


Data Validations used:

1. Age of the investor should be between 1 and 65 years.
2. Investment amount should be greater than $5000.


Risk levels provided to pick:

None, Very Low, Low, Medium, High, Very High.
