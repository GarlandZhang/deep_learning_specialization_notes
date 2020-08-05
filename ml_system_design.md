## building spam classifier

![spam classifier](https://i.gyazo.com/c4a37936c2f277cb4ea77a27570b1a4a.png)


1. start w/ simple algo, implement it, and test early on cv set
2. plot learning curves to decide if high bias or high variance => apply corresponding solutions
3. manually examine misclassifications on cv set  to spot trend on where most errors are made

"For example, assume that we have 500 emails and our algorithm misclassifies a 100 of them. We could manually analyze the 100 emails and categorize them based on what type of emails they are. We could then try to come up with new cues and features that would help us classify these 100 emails correctly"

"It is very important to get error results as a single, numerical value. Otherwise it is difficult to assess your algorithm's performance. For example if we use stemming, which is the process of treating the same word with different forms (fail/failing/failed) as one word (fail), and get a 3% error rate instead of 5%, then we should definitely add it to our model. However, if we try to distinguish between upper case and lower case letters and end up getting a 3.2% error rate instead of 3%, then we should avoid using this new feature. Hence, we should try new things, get a numerical value for our error rate, and based on our result decide whether we want to keep the new feature or not."
  - we find these error categories from manually examining the errors in the cv set
