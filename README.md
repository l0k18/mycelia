# mycelia
Experimental Asynchronous Transaction Mesh Distributed Ledger

# contents
### 1. abstract

# abstract

Mycelia combines hash chaining and signature chaining, as used in blockchains, with the [Interval Tree Clock](https://blog.separateconcerns.com/2017-05-07-itc.html) to generate graphs out of user transactions, to create a proof of work distributed ledger that is not vulnerable to timing attacks nor double spends.

Instead of using proof of work to regulate a block time, because of the block being the base unit of the currency, in the 'coinbase' from being issued at an unbounded rate. Instead, miners simply eventually have to prune the graph, and linking to a recent past block proves causal sequence and the value created by this modulates by the weight to size ratio, meaning it will be preferable to join to previous transactions with a good ratio, as these give the best yield from the work.

Lowest value are large in data size, signature weight, and low nominal value of all the outputs. Highest value are small in size and high in value. All transactions have a constant network-wide cost in an unchanging difficulty target. Instead of a race for higher efficiency, simply more hashpower means more transaction processing capacity, and greater chance of winning the acceptance by the modulation of a joined transaction with its ratio.

A miner can thus set a threshold, and not process more. Nodes could be configured to go into sleep mode when business is slow. Scaling overheads can raise a miner's threshold. So, it will not link as the confirmer to another transaction unless the resultant coinbase is worth it.

If a transaction goes unlinked for a long time, it becomes a candidate for pruning, and is effectively ignored out of existence.

In each case by transaction I mean the proven block, it is a different object representing a network node's view of the data, and the more links back to a block there is made, the stronger the consensus becomes.

When two conflicting transactions spending from the same thread back to a coinbase, nodes ignore both of them due to their close time and differing destinations. More than 2 would be even more definitive. They will be immediately discarded. Honest transactions do not attempt to rewrite the history.

The value of the transactions should follow a normal distribution, and abnormal transactions are spam, attempting to issue currency without concrete resources backing it, specifically, resources sacrificed to this sole purpose. Checking, proving, signing and propagating a block has a definite cost and the reward for it is the primary purpose of providing this service.

The supply thus is complete in the sense of the full capacity of the network encoding of the value, the genesis block spends to one or more accounts, and these accounts can then spend them, split them and join them, and they form the body of the Mycelia, the supply of tokens.
