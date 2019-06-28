# NodeJS Monobank API client

Simple Monobank API client wrapper build on promises.

## Installation

### yarn:

```
yarn add monobank-api-client
```

### npm:

```
npm i monobank-api-client
```

## Usage

```
const { MonobankApi } = require('monobank-api-client');

const api = new MonobankApi(
    {
        token: 'YOUR_API_TOKEN',
    }
);

// promise resolved with CurrencyInfo[]
api.getCurrencyList();

// promise resolved with UserInfo
api.getUserInfo();

// promise resolved with Transaction[]
api.getStatement({ account: 'ACCOUNT_ID', from: new Date('2019-06-01'), to: new Date('2019-06-28')});
```