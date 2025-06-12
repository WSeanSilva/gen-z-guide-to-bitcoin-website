---
layout: "post"
title: "Bitcoin Technicals Explained Part 1"
categories: Bitcoin Fundamentals Technical Series
date: 2025-01-25
---

If you don't know by now, I am a big proponent of understanding Bitcoin before you buy. A lot of people have no idea how the technology works but wish they did. 
My job here is to help readers like you scale the learning-curve in a way that is not horribly overburdening, but also doesn't skirt away from tackling the technical intricacies.

In a previous article titled *[What Is Bitcoin](http://localhost:4000/GenZGuideToBitcoin/bitcoin/fundamentals/beginner/what-is-btc)*, I briefly touched upon the topics of the network and nodes.
This post will be spent diving into these two concepts, how they relate to one another and work in practice. In successive posts to this series of *"Bitcoin Technicals Explained"*, I will give insight to concepts like 
private keys, cryptography, mining, Bitcoin's predecessors, and more.

<h3>The Bitcoin Network</h3>

First, the Bitcoin network can almost be thought of like a global, decentralized computer hive-mind that operates independently of any central oversight.
Right now there are thousands of computers (known as nodes) across the globe that store the entire history of Bitcoin transactions.
All nodes are connected to each other and each are in equal status to one another. The term "<em>Peer-to-Peer</em>" is often used in place of this definition.<sup><a href="#fn1" id="ref1">1</a></sup>
Nodes play an essential role in the Bitcoin network since they are responsible for validating and propagating transactions to every other node.

<h3>Transactions on Bitcoin</h3>

Transactions on the Bitcoin network are grouped into structures called blocks.
Each block is _cryptographically_ verified and linked to the block that came before it, forming a chain of blocks. 
This design ensures that the history of transactions is immutable and transparent, providing a robust and tamper-proof record.
So, if you've heard of a __blockchain__ before, that is exactly what I am describing here. In a future post, I will provide an explanation for cryptography.

When a bitcoin transaction is performed, the data of such is transmitted to the closest accessible node. But before the data of a transaction is broadcast to other nodes, several things must happen first.
The following prerequisites adhere to the rules of the Bitcoin protocol. These are some which will suffice for you to know as of now:
<ul>
	<li>Transactions must be correctly formatted according to protocol standards.</li>
	<li>Each input within the transaction must have a digital signature which is verified via cryptography.</li>
	<li>Inputs being sent are checked by the node to verify that they have not already been sent in another transaction (<em>Double Spending</em>).</li>
	<li>The total Bitcoin being spent in a transaction (sum of inputs) must be equal to <strong>or</strong> greater than the total amount being sent to the recipients (sum of outputs) plus a transaction fee.</li>
</ul>
If everything checks out, the node will broadcast the received transaction to all nodes within reach, and these nodes will repeat the same process with every other node in existence.
It is demonstrated therefore how the Bitcoin network is a distributed, decentralized, peer-to-peer cash system through the network system of nodes.
And since transactions are not reliant on a central system to be conducted, you can think of how
Venmo transactions between two people must be facilitated and cleared by the banks involved as well as Venmo to see how Bitcoin removes the need for any mediators.

The significance behind the decentralized nature of Bitcoin is that by default, transactions between two parties can be conducted without being frozen, censored, or scrutinized by any central overseer.
I'll let the reader use their imagination as to what someone could get away with by using Bitcoin in a black market...but I digress.

<h3>In Conclusion</h3>
This post was dedicated primarily to the Bitcoin network and how nodes and transactions play their critical part in the system. Therefore, it would make the most sense to shed light on their contingents in future posts. A high-level analysis
of how transactions function is great, but readers will definitely benefit from learning about cryptography and mining. These two topics are highly technical and complex, but gaining an understanding will prove to be incredibly beneficial
for those looking to establish themselves with Bitcoin or other cryptocurrencies for that matter. Please stay tuned for more within the Bitcoin Technicals Explained series!



<div class="fn">
	<hr>
	<ol>
		<li id="fn1">
			<a href="https://learnmeabitcoin.com/beginners/guide/network/" target="_blank" rel="noopener">
				Walker, G. (2024, December 18). Home. What is the Bitcoin Network? https://learnmeabitcoin.com/beginners/guide/network/ 
		</a>
		<a href="#fn1">&larrhk;</a>
		</li>
	
	</ol>
</div>
