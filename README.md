

1. **Get list information of Mdex's major liquidity providers：**

   

   **URL**：https://gateway.mdex.cc/v2/mdex/pairs

   **Params**：-
   mdex_chainid : 当前链ID，Heco: 128(默认), Bsc: 56, Eth: 1
   
   **Reponse data**：

   ```
   {
   	"code": 0,
   	"result": {
   		"0xfbe7b74623e4be82279027a286fa3a5b5280f77c": {
   			"pair_name": "HBTC/USDT",
   			"pair_price": "449.9264438481456884701",
   			"token0": "0x66a79d23e58475d2738179ca52cd0b41d73f0bea",
   			"token0_symbol": "HBTC",
   			"token1": "0xa71edc38d189767582c38a3145b5873052c3e47a",
   			"token1_symbol": "USDT"
   		},
       "0x78c90d3f8a64474982417cdb490e840c01e516d4": {
         "pair_name": "ETH/USDT",
         "pair_price": "85.02236430853983927455",
         "token0": "0x64ff637fb478863b7468bc97d30a5bf3a428a1fd",
         "token0_symbol": "ETH",
         "token1": "0xa71edc38d189767582c38a3145b5873052c3e47a",
         "token1_symbol": "USDT"
       }
       ......
   	},
   	"message": "Success",
   	"extra": null
   }
   ```

   **Description：**

   ```
   result.0xfbe7b74623e4be82279027a286fa3a5b5280f77c : Liquidity pair address
   pair_name：Liquidity pair name
   pair_price：Liquidity pair benchmark usdst price
   token0: The first token address of the liquidity pair
   token0_symbol：The first token name of the liquidity pair
   token1： The second token address of the liquidity pair
   token1_symbol： The second token name of the liquidity pair
   ```

   



2. **Obtain single currency price quotation list information:**

   **URL**：https://gateway.mdex.cc/v2/mdex/tokens

   **Params**：-
   mdex_chainid : 当前链ID，Heco: 128(默认), Bsc: 56, Eth: 1
   
   **Reponse data**：

   ```
   {
   	"code": 0,
   	"result": {
   		"0xa71edc38d189767582c38a3145b5873052c3e47a": {
   			"token_name": "USDT",
   			"price": 1,
   			"volume_24hr": 1636617629.4297485,
   			"decimals": 18
   		},
   		"0x64ff637fb478863b7468bc97d30a5bf3a428a1fd": {
   			"token_name": "ETH",
   			"price": "1807.023672701018828076",
   			"volume_24hr": 260325200.09362411,
   			"decimals": 18
   		}
   		......
   	},
   	"message": "Success",
   	"extra": null
   }
   ```

   **Description：**

   ```
   result.0xa71edc38d189767582c38a3145b5873052c3e47a： Token address
   token_name: Token name
   price： The price of the token against the benchmark usdt
   volume_24hr： The total trading volume of the token in 24 hours
   decimals：Token decimal
   ```

   
