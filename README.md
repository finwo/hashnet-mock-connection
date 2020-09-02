# hashnet-mock-connection

Mock connection for hashnet tests

## Install

```
npm install --save hashnet-mock-connection
```

## Usage

```js
const Connection = require('hashnet-mock-connection');
const Peer       = require('hashnet').Peer;

const alice = new Peer();
const bob   = new Peer();

Connection.linkPeers(alice, bob, 123, 456);
```

## API

### constructor(delayAtoB, delayBtoA)

Returns an array with 2 ends of a pipe which emulate the api implemented by [simple-peer](https://npmjs.com/package/simple-peer)

- delayAtoB: How long it takes a message from the first to the second pipe end
- delayBtoA: How long it takes a message from the second to the first pipe end

### .linkPeers(peerA, peerB, delayAtoB, delayBtoA)

Create a connection between 2 existing hashnet peers

- peerA: the first peer to attach the connection to
- peerB: the second peer to attach the connection to
- delayAtoB: How long it takes a message from the first to the second pipe end
- delayBtoA: How long it takes a message from the second to the first pipe end
