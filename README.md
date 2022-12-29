# Adjusting-short-straddle-Quant-bot-
Algorithmic implementation of my invention , automated adjustment of delta hedged initialized short straddle deployed over Derivatives (Options) market

![demo](https://user-images.githubusercontent.com/86561124/209945234-b9e96e77-0bf2-49ec-99c1-b412ca4d26a3.gif)

**Skills Used** - Finance , Options and Derivatives , Options Trading Strategies , Market neutral stratergy , Delta hedging , Quantitative Finance (Quant) , Python 

## About the project - 

The above GIF shows an algorithm automatically trading options so that the P/L graph stays in the profit zone even if the underlying stock price leaves the breakeven points region . 

Traditional Short straddle is a market neutral stratergy (delta approx 0 ) meaning that we gain money if the stock moves sideways , i.e. does not go too much up or down . It has more than 50% chance theortically , since points closer to the current spot position have higher chances compared to the farther points . This strategy also has a positive theta due to selling of a call and a put , meaning that stock maintaining its position inside the pyramid will also lead to earning money , since the premium of the options has extrinsic value too . 

![image](https://user-images.githubusercontent.com/86561124/209947331-230b66a2-1b8f-4cff-9497-179f77bf5346.png)


Since the options exactly equal to the stock value may not be availaible in the market , we can set up a straddle near the original position and delta hedge it . Delta hedging is the practice of making delta of a portfolio 0 , so that it becomes insensitive to the market's motion . Such moves are often used to maximise the probablity of profit , and are even used by volatility and theta traders . 

However , if the market moves a little bit out of the profit zone , this may lead to losses . In such cases , adjustments are made . However , adjustements are difficult to make and are often done by skilled traders . However , I have implemented a short straddle along with my algorithm in such a way that it can adjust automatically to slight changes in the market . This can be seen in the above GIF where my P/L zone changes shape automatically if the market moves out of the profit zone .  

## My algorithm - 

* Sell few puts close to the point where the initial short straddle is to be placed .
* Delta hedge the portfolio by calculating the delta of call and put from the current stock price , and sell the calls at the same strike as puts . 
* Now , if the market moves above the upper breakeven point , 

