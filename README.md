# TickerV3
Display Crypto Prices from Coinbase AND Binance including 

- Bitcoin
- Litecoin
- Ethereum
- Bitcoin Cash
- Ethereum Classic
- Monero
- Stellar
- IOTA
- DASH
- NANO

## Requirements
- NodeMCU ESP8266
- MAX7219 Dot Matrix Module

## Update 
Want to add/delete coins? Modify the total amount of coins and the function configureCoins() 

```c
// Number of coins to display
#define TOTAL_COINS 10
.
.
.
void configureCoins() { 
  Coin bitcoin = { .url = "/products/BTC-USD/ticker", .ticker = "BTC", .isCoinbaseCoin = true }; 
  Coin monero = { .url = "/api/v1/ticker/price?symbol=XMRBTC", .ticker = "Monero", .isCoinbaseCoin = false };
}
  
```
