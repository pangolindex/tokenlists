# Avalanche Tokenlists

Token Lists is a specification for lists of token metadata (e.g. address, decimals, etc.) that can be used by any dApp
interfaces that needs one or more lists of tokens. Anyone can create and maintain a token list, as long as they follow
the specification. The Pangolin community invites you to add your token to our tokenlists!


## Adding Your Token to an Existing List


### General Requirements
1. Token should be verified on the [cchain explorer](https://cchain.explorer.avax.network).
2. Token must be added to a list that it qualifies for:
    * **[Top 15 Tokenlist](./top15.tokenlist.json)**: Token must be in the top 15 of eligible Avalanche tokens by marketcap.
    * **[AB Tokenlist](./ab.tokenlist.json)**: Token must be bridgeable on the Avalanche Bridge.
    * **[AEB Tokenlist](./aeb.tokenlist.json)**: Token must be bridgeable on the Avalanche-Ethereum Bridge.
    * **[DeFi Tokenlist](./defi.tokenlist.json)**: Token must be connected to a DeFi protocol running on Avalanche.
    * **[Stablecoin Tokenlist](./stablecoin.tokenlist.json)**: Token must be a stablecoin.
    * **[Fuji Tokenlist](./fuji.tokenlist.json)**: Token must be on the Fuji network.


## Adding Your Token
1. Add an entry in the `tokens` field of the appropriate tokenlist. Here is an example using PNG:
    ```json
    {
        "address": "0x60781C2586D68229fde47564546784ab3fACA982",
        "chainId": 43114,
        "name": "Pangolin",
        "symbol": "PNG",
        "decimals": 18,
        "logoURI": "https://raw.githubusercontent.com/ava-labs/bridge-tokens/main/avalanche-tokens/0x60781C2586D68229fde47564546784ab3fACA982/logo.png"
    }
    ```
2. Update the `timestamp` field to the current timestamp.
3. Update the `version` field to adhere to semantic versioning:

    * Increment major version when tokens are removed
    * Increment minor version when tokens are added
    * Increment patch version when tokens already on the list have minor details changed (name, symbol, logo URL, decimals)

    ***Note:*** Changing a token address or chain ID is considered both a remove and an add, and should be a major version update.


## Creating Your Own List

List creation is encouraged! The Pangolin team wants the community to develop their own lists and will not gatekeep new lists.


## Adding Your Token Logo

Avalanche token logos are [hosted here](https://github.com/pangolindex/tokens).
