<h1 align="center">
	<img width="128px" src="https://raw.githubusercontent.com/genie-team/graphql-genie/master/resources/logo.svg?sanitize=true" alt="GraphQL Genie Logo">
</h1>

# GraphQL Genie Subscriptions

[![npm version](https://img.shields.io/npm/v/graphql-genie-subscriptions.svg)](https://www.npmjs.com/package/graphql-genie-subscriptions)
[![Dependency Status](https://david-dm.org/genie-team/graphql-genie-subscriptions.svg)](https://david-dm.org/genie-team/graphql-genie-subscriptions)
[![devDependency Status](https://david-dm.org/genie-team/graphql-genie-subscriptions/dev-status.svg)](https://david-dm.org/genie-team/graphql-genie-subscriptions/?type=dev)
[![npm](https://img.shields.io/npm/l/graphql-genie-subscriptions.svg)](https://github.com/genie-team/graphql-genie-subscriptions/blob/master/LICENSE)

Pass in a pubsub object from [graphql-subscriptions](https://github.com/apollographql/graphql-subscriptions) and the necessary types and resolvers will be added to your schema

### Installation
Assuming you already have [GraphQL Genie](https://github.com/genie-team/graphql-genie) installed.

`npm install graphql-genie-subscriptions graphql-subscriptions` or `yarn add graphql-genie-subscriptions graphql-subscriptions`


### Enable plugin

```js
import { FortuneOptions, GraphQLGenie } from 'graphql-genie';
import subscriptionPlugin from 'graphql-genie-subscriptions';
import { PubSub } from 'graphql-subscriptions';

const genie = new GraphQLGenie(...args);

await genie.init();
// genie.use can be called before or after init
await genie.use(subscriptionPlugin(new PubSub())); 

//get the GraphQLSchema and use it with any other tools you need, such as subscriptions-transport-ws
const schema = genie.getSchema();
```

#### Thanks/Credit

Logo Icon made by [Freepik](http://www.freepik.com) from [www.flaticon.com](https://www.flaticon.com/) is licensed by [CC 3.0 BY](http://creativecommons.org/licenses/by/3.0/)