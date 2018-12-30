# mycelia
Experimental Asynchronous Transaction Mesh Distributed Ledger

# contents
### 1. abstract

# abstract

Mycelia combines hash chaining and signature chaining, as used in blockchains, with the [Interval Tree Clock](https://blog.separateconcerns.com/2017-05-07-itc.html) to generate graphs out of user transactions, to create a proof of work distributed ledger that is not vulnerable to timing attacks nor double spends.

Instead of using proof of work to regulate a block time, because of the block being the base unit of the currency, in the 'coinbase' from being issued at an unbounded rate.

Thus it attempts to map with time an aggregate measure, and if there is one thing that Austrian Economics, most notably in Mises' *Human Action*, the subject of logistics networks is naturally touched on, as it is the core of how economies work.

This is obviously a mistake.

Both blocks (proof of having expended resources) and transactions use the very same technique. Each transaction has a unique hash identifier, and it is attached to the block as proof of knowing of the existence of this block, and thereby a proof of sequential occurrance.

Signatures allow an account to be created by attaching a fingerprint (address) to it and received by proving ownership using the private key to embed a signature on the hash of the preceding document that can be decoded by hashing the document the same way, and only the owner of the account can generate this correct signature.

Interval Tree Clocks use a somewhat similar but more simplified model of binding causality, but hash chains amount to a generalisation of the same technique of proving the sequence of causality without the benefit of the artificial crutch of a timestamp. A timestamp could be attached in the database, but the only one the node itself can trust is the timestamp on the network packet.

In fact, the linear part of the system is the account. Yes you can make as many as you want, it doesn't matter. Each one can be attached to many branches sideways, but they cannot be out of order, it is a syntax error to receive and then send, this can only be send and then receive.

The transactions are like the threads of fungal bodies searching through the mush under the leaves and under the ground, they form a web that links across the accounts. Some threads follow lines and grow thicker with the resources available, and others explore edges and some eventually find new paths.

The security of the system depends on a limited token issuance rate, no matter which way you think monetary economics works. Another thing that is arbitrarily issued based on a clock cannot work with an asynchronous system. Thus, the several metrics you can apply to authenticating and processing transactions to establish a weight to value ratio.

This ratio should be low towards value but within a normal range, maybe 3 standard deviations. But the only thing we can measure in this network is the transactions themselves.

The nodes that relay transactions sort them by these metrics, and those with the lowest nominal value and highest cost to process are left at the bottom of the queue, and ones that are both large and high value form the front of the line. This is not a consensus rule, it is an inclusion rule.

Transactions may or may not be considered to be authentic or honest by nodes based on many arbitrary metrics. Whether you build this control into the protocol or not it is possible to filter what you will deal with.

The other thing about asynchronous means also that the issuance of tokens, earned by a proof of work, are not evenly distributed in time. They basically spring into existence through the necessity of an exchange using the currency. So, as use rises, so does supply, and supply simply pauses if nobody uses it.

Instead of a consensus, miners have to mine the transactions, and so greater hashpower means a greater throughput, instead of a higher chance of finding a solution. The best way to do this is to pipeline as many differently optimised hash functions that would require a fast pipe to each stage to accelerate, and this moves it back to a more general purpose hardware base, PCI express cards and fast, low latency network connections, the 'backing' of a Mycelia based payment network.

Thus, miners are not going to be as interested also in trying to process these, and they may have many days long clearance times, or if it exceeds the network's total memory pool capacity, in its age, it will never be processed. This will be rare for legitimate transactions. Fraudulent ones will tend to be low value, made by miners to print their own tokens. But if nobody will let them be spent, or few do, eventually everyone forgets about it, as the coinbase it creates cannot be spent.
