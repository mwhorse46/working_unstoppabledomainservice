# Resolution

## Installing Resolution

Resolution can be installed with either `yarn` or `npm`.

```shell
yarn add @unstoppabledomains/resolution
```

```shell
npm install @unstoppabledomains/resolution --save
```

If you're interested in resolving domains via the command line, see our
[CLI section](#command-line-interface).

## Updating Resolution

Resolution can be updated with either `yarn` or `npm`.

```shell
yarn upgrade @unstoppabledomains/resolution --latest
```

```shell
npm update @unstoppabledomains/resolution --save
```

## Using Resolution

## Initialize with Unstoppable Domains' UNS Proxy Provider

```javascript
const {default: Resolution} = require('@unstoppabledomains/resolution');

// obtain a key by following this document https://docs.unstoppabledomains.com/domain-distribution-and-management/quickstart/retrieve-an-api-key/#api-key
const resolution = new Resolution({apiKey: '<api_key>'});
```

> NOTE: The `apiKey` is only used resolve domains from UNS. Behind the scene, it
> still uses the default ZNS (Zilliqa) RPC url. For additional control, please
> specify your ZNS configuration.

```javascript
const {default: Resolution} = require('@unstoppabledomains/resolution');

const resolution = new Resolution({
  apiKey: '<api_key>',
  sourceConfig: {
    zns: {
      url: 'https://api.zilliqa.com',
      network: 'mainnet',
    },
  },
});
```

