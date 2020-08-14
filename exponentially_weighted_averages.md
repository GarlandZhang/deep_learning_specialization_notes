aka expontially moving averages
![ex](https://i.gyazo.com/402fe45cbd8869c7caac8d2ae0f56812.png)
  - each new day, we take some information we learned from previous day (weighted by beta) to guess todays temperature
  - the larger the B, the more it relies on the previous data point, which relies on previous data points and so on... so it will be less noisy (green line)
  - the smaller the B, the more noisy but more up to date as it relies on more relevant data
 
## intuition
 - B = 0.9 is approx 10 days because it isnt until 0.9^10 when the value is insignificant
 - similarly, B = 0.98 is approx 50 days of using prev info
 - advantage of this method is it takes very little memory as it only relies on previous data point
 
## impl

![impl](https://i.gyazo.com/ec9bed21972cdd9cbe02fd90a2ca405b.png)

## bias correction
  - initially, EMA is heavily biased to new data points since there is no "history"
  - 
