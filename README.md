# Avalanche Tokenlists

Token Lists is a specification for lists of token metadata (e.g. address, decimals, etc.) that can be used by any dApp
interfaces that needs one or more lists of tokens. Anyone can create and maintain a token list, as long as they follow
the specification. The Pangolin community invites you to add your token to our tokenlists!


## Adding Your Token to an Existing List


### General Requirements
1. Token should be verified on the [Snowtrace Explorer](https://snowtrace.io/verifyContract).
2. Token must be added to a list that it qualifies for:
    * **[Pangolin Tokenlist](./pangolin.tokenlist.json)**: Token must be on the Avalanche network.
    * **[Fuji Tokenlist](./fuji.tokenlist.json)**: Token must be on the Fuji network.


## Adding Your Token
1. Add an entry in the `tokens` field of the appropriate tokenlist. Please use the [checksum address](https://docs.ethers.io/v5/api/utils/address/#address). Here is an example using PNG:
    ```json
    {
      "chainId": 43114,
      "address": "0x60781C2586D68229fde47564546784ab3fACA982",
      "decimals": 18,
      "name": "Pangolin",
      "symbol": "PNG",
      "logoURI": "https://raw.githubusercontent.com/pangolindex/tokens/main/assets/43114/0x60781C2586D68229fde47564546784ab3fACA982/logo_24.png"
    }
    ```
2. Update the `timestamp` field to the current timestamp.
3. Update the `version` field to adhere to semantic versioning:

    * Increment major version when tokens are removed
    * Increment minor version when tokens are added
    * Increment patch version when tokens already on the list have minor details changed (name, symbol, logo URL, decimals)

    ***Note:*** Changing a token address or chain ID is considered both a remove and an add, and should be a major version update.

## Adding Your Token Logo

Token logos are [hosted here](https://github.com/pangolindex/tokens).
