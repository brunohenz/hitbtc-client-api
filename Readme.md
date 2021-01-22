# HitBTC Client API 

This is a simple client to connect in the HitBTC Exchange API.

The main objective is provide a simple interface to consume the methods to consulting, create orders, sell and buy cryptos in HitBTC.

## Installation

`pip install hitbtc-api-brunohenz`

## Pré-Req
To use de client and connect to HitBTC API, is necessary create a account in the exchange and generate a API KEY in path https://hitbtc.com/settings/api-keys

## Usage

```python
from hitbtcapi.hitbtc import HitBtc

APIKey = 'API-KEY'
SecretKey = 'SECRET-KEY'

client = HitBtc(APIKey, SecretKey)

# Get OrderBooks by Symbol
orderbooks = client.get_orderbook('smartbtc')
print(orderbooks)

# Create a order
order = client.create_order(
    {'symbol': 'smartbtc', 
     'side': 'buy', 
     'quantity': 1, 
     'price': '0.000148'
     })

print(order)
```

## Avaliable Methods

### Currencies
`client.get_currencies()`

### Order Books
`client.get_orderbook('smartbtc')`

### Orders
`get_orders()`

`create_order({'symbol': 'smartbtc', 'side': 'buy', 'quantity': 1, 'price': '0.000148'})`

### Trades
`get_trades_history('smartbtc')`