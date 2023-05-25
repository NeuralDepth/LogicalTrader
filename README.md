
## What is "LogicalTrader"?
LogicalTrader is an open source cryptocurrency trading bot. You can use it to automatically buy and/or sell cryptocurrencies based on a strategy that you've programmed.
The strategy basically contains a set of rules that will define when and how the bot should act in the cryptocurrency market. These rules can be based on technical analysis ([what is technical analysis?](https://www.investopedia.com/terms/t/technicalanalysis.asp))
or you could simply tell the bot to buy/sell at certain price levels. In fact, it's up to you to decide the rules of the game!

LogicalTrader will try to make use of a realtime connection with the exchange. This has the advantage
that one can act very quickly in a changing market with low latency.


## Features
- 🚀 Realtime super-fast websocket trading.
- 📈 50+ Technical indicators. ([docs](https://github.com/anandanand84/technicalindicators))
- 🌈 Written in TypeScript!
- 🌿 Unit tested source code.
- 📝 Paper trading a strategy on LIVE exchange data.
- 🏡 Backtesting engine with local data.
- 🚢 Run LogicalTrader inside a docker container.

## Getting started

# Quickstart

1. Git clone `git clone git@github.com:LogicalTrader/LogicalTrader.git && cd LogicalTrader`
2. Install NodeJS dependencies. `npm i`
3. Copy `config/default.json` to `config/local.json` and edit.
4. Start postgres database `docker-compose up`
5. Run the MovingAverageStrategy on LocalExchange. `npm run start:backtest`

## Connect your Binance account

You feel like your strategy is production ready?
Good! I'll help you to connect your LogicalTrader strategy to your Binance account.

1. Copy `config/default.json` to `config/local.json`
2. Go to your Binance account under API Management, create a new API key
3. Provide the apiSecret and apiKey in `config/local.json`
4. Don't forget to change the exchange in your strategy to `new Binance()` and you're good to go!

### API key restrictions

By default, the newly created API key does not allow you to place orders, only reads are allowed.
To get started:

1. Go to your Binance account
2. Under API restrictions enable 'Enable Spot & Margin Trading'

## DISCLAIMER
    Using a trading bot does not mean guaranteed profit.
    Also, trading crypto currency is considered high risk.
    Losses are possible, which LogicalTrader cannot be held responsible for.
