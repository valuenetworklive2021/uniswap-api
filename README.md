# Valueswap API

The Valueswap API is a set of **authenticated** endpoints used by market aggregators (e.g. coinmarketcap.com) to surface 
Valueswap liquidity and volume information. All information is fetched from the underlying subgraphs.

The API is designed around the CoinMarketCap
[requirements document](https://docs.google.com/document/d/1S4urpzUnO2t7DmS_1dc4EL4tgnnbTObPYXvDeBnukCg).

Prefer the Valueswap subgraph for any Valueswap queries whenever possible. The respective subgraphs will always have more
recent data.

V2 Subgraph: https://github.com/valuenetworklive2021/valueswap-v2-subgraph

V1 Subgraph: https://github.com/graphprotocol/valueswap-subgraph

## Getting an API Key

Please fill out [this form](https://forms.gle/4xucinVsTTPu71bT6) if you would like to get an API key.

## Using an API Key

You can use an API key by setting it in the `x-api-key` header, like so:

```sh
curl -v --compressed https://valuenetworklive2021.github.io/valueswap-api/v2/tickers -H 'x-api-key: abcd1234'
```

## Segregated data

Note the data returned by the V1 and V2 endpoints is segregated, i.e. there are no endpoints for combined data from 
both Valueswap V1 and V2.

## V1 Documentation

The documentation of the `/v1/` endpoints is [here](./v1.md).

## V2 Documentation

The documentation of the `/v2/` endpoints is [here](./v2.md).

## Deploying the API

The API uses the [serverless framework](https://serverless.com) and can easily be deployed to any AWS account,
via the `yarn sls deploy` command.

In order to configure your AWS account as a target, 
see [the serverless docs](https://www.serverless.com/framework/docs/providers/aws/guide/credentials/).
