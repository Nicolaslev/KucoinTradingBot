# KucoinTradingBot

This BOT uses an algorythm called "The Bank" because it does 100% the contrary to what the market is doing. It will buy the dib and will take profits when the coin is mooning. The BOT will compare the value in cryto vs the value in USDT and then buy or sell accordingly. You can run multiple instances for several coins at the same time and the USDT will be split accordingly. EX : Trade 3 crypto, USDT = 1/4 of the total value. Trade 4 Crypto and USDT will be 20% of the total value.

It is not recommanded to CANCEL ALL orders unless there is a lot of cash in orders for USDT.

Kucoin Trading Bot - Program and configurations

The majority of people would think that having a bias for a crypto vs a cash position would give a bigger positive return. However, the Robot-trader automatically modifies the proportion by 1% to keep the value of the portfolio at the same ratio and thus take advantage of the volatility (% of average change in the action).

The robot has 50%/50% trade 4x when losing 17%. Other trades 3x. We thus have a robot that is 33% more sensitive to the market and it buys nearly 40% more crypto than we can resell when it goes up.

Strategy description
The strategy based on the spot average position is essentially a simplified version of the grid strategy. Keep fixing the ratio of the position of an investment target held to the total position. When the value of this investment target exceed an established threshold, sell part of the target to keep the ratio. When the value of this investment target become under than the established threshold, buy back part of the target to keep the ratio. Through continuous adjustment, the tartget ratio has been maintained at a fixed value to keep dynamic balancing.

e.g.: If the BTC market price is 10000 USDT, while the balance is 1 BTC and 10000 USDT.

Scenario 1: If the value of BTC is greater than the balance 10000 USDT and exceeds the threshold, like the price rising to 12000 USDT, sell 0.0833 BTC = (12000 - 10000)/2/12000, then the price drop down back to 10000 USDT, we buy back the same amount of BTC.

Scenario 2: If the value of BTC is less than the balance 10000 USDT and under than the threshold, like the price dropping down to 8000 USDT, buy 0.125 BTC = (10000 - 8000)/2/8000, then the price rises back to 10000 USDT, we sell the same amount of BTC.

Summary: In this case, keep well the ratio between the target and the total position, that is, to maintain the value ratio of the base and the remaining funds in the account to 1: 1, so it is called the average position strategy.

Advantages: The strategy of averaging positions is essentially a grid strategy, and its income comes from the fluctuation of prices within a certain range, so it will perform better in a shock market.

Disadvantages: The risk is that the price continues to rise or fall unilaterally after the adjustment of positions.

ORIGINAL GITHUB FROM KUCOIN HERE : https://github.com/Kucoin-academy/avg-position



Newton
How to easily transfer funds to and from a canadian bank account. 
They also offer interact deposit

![Newton code](https://user-images.githubusercontent.com/99097186/152657391-09b780f2-1971-4e13-9ca4-9e5a4e00a195.jpg)

Kucoin
Kucoin code to get 20% off fees. Remember to activation pay in KCS for an additional 20%

![KuCoin code](https://user-images.githubusercontent.com/99097186/152657466-d691534c-b5ea-47cd-b8d8-57f28bfa6778.jpg)

When you have created your account, create an API

![image](https://user-images.githubusercontent.com/99097186/152657512-12c436b8-d2fc-4543-96ab-c8b32e518408.png)

Copy api_key, api_secret, api_passphrase into the config.json file.
This must be done individually for each config.json file for each coin since the min_param and price_param are coin specific.

![APIdirections](https://user-images.githubusercontent.com/99097186/152657592-b8b396bb-6424-458e-90f8-533498128426.jpg)

Copy into each directory the avg_position.exe file into the respective coins folder

![image](https://user-images.githubusercontent.com/99097186/152657730-a58b6c5a-a914-412a-b426-830c362f1388.png)

Rename the .exe file to reflect the name of the coin. 
Remove the _xxx from the config_xxx.json and rename config.json

![image](https://user-images.githubusercontent.com/99097186/152658332-844dafbb-30aa-4cac-815e-26c223933350.png)


This is important to be able to restart the program on crash 

![image](https://user-images.githubusercontent.com/99097186/152657789-1c610612-304d-40e7-bae8-c8ce1a897114.png)

Download Restart on crash included in this repo. This will ensure your auto-trader is always running.

![image](https://user-images.githubusercontent.com/99097186/152657891-eceabf0a-868a-4399-b133-2809c718775d.png)

![image](https://user-images.githubusercontent.com/99097186/152657921-f61511de-04c0-4e32-946f-b91706562b6b.png)

![image](https://user-images.githubusercontent.com/99097186/152657933-e5833328-c782-4ec3-b219-a61c2460d989.png)

This will be what the interface will look like, you can run as many bots as you like, they will all thinks that they have 50% of the cash

![image](https://user-images.githubusercontent.com/99097186/152657996-6780f837-3015-425a-b4d9-7aeb11005232.png)

Present BTC CONFIG
  "symbol": "BTC",
  "min_param": "0.00003",
  "price_param": "0.0000000001"

Present ETH CONFIG
  "symbol": "ETH",
  "min_param": "0.0005",
  "price_param": "0.00000002"

Present KCS CONFIG
  "symbol": "KCS",
  "min_param": "0.10",
  "price_param": "0.0000010"

Present KDA CONFIG
  "symbol": "KDA",
  "min_param": "1.5",
  "price_param": "0.00004"

