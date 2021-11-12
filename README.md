# SwapperChan Subgraphs

Subgraph for SwapperChan on BOBA Mainnet. 

Forked from `sushiswap-subgraph`. 


### Deploy

```` 
# authenticate api key
$ graph auth https://api.thegraph.com/deploy/ <API_KEY>

# build constants
$ cd packages/constants
$ yarn prepare:boba

# build subgraph
$ cd subgraphs/exchange
$ yarn prepare:boba
$ yarn codegen:boba
$ yarn build:boba

# deploy subgraph
$ yarn deploy:boba
````


### (SWAPPERCHAN-SUBGRAPH README)
Aims to deliver analytics & historical data for SwapperChan. Still a work in progress. Feel free to contribute!

The Graph exposes a GraphQL endpoint to query the events and entities within the SwapperChan ecosytem.

Current subgraph locations:

1. **Exchange**: Includes all SwapperChan Exchange data with Price Data, Volume, Users, etc: https://thegraph.com/hosted-service/subgraph/swapperchan/exchange


## To setup and deploy

For any of the subgraphs:

1. Run the `yarn run codegen:[subgraph]` command to prepare the TypeScript sources for the GraphQL (generated/schema) and the ABIs (generated/[ABI]/\*)
2. [Optional] run the `yarn run build:[subgraph]` command to build the subgraph. Can be used to check compile errors before deploying.
3. Run `graph auth https://api.thegraph.com/deploy/ <ACCESS_TOKEN>`
4. Deploy via `yarn run deploy:[subgraph]`.



