---
layout: "single"
title: "Altcoins: What's The Deal?"
description: "Wondering what all the other cryptocurrencies are? In this article I break down the essence and significance of Altcoins."
categories: ["Bitcoin", "Cryptocurrency", "Altcoins", "Web3"]
last_modified_at: 2025-06-25
thumbnail: /assets/img/crypto_set.jpg

header:
  overlay_image: "/assets/img/crypto_set.jpg"
  overlay_filter: "0.5"
  show_overlay_text: false
  caption: "Image Credit: @myriammira on Freepik"
  title: ""

---


<p><em>So perhaps you know a thing or two about Bitcoin, but you still might be wondering, “What the heck are all these other cryptocurrencies that get thrown around with Bitcoin, too?” What I hope you’ll learn from this post is an introduction to the world of altcoins and why they’re relevant.</em></p>


<div class="intro">
<h3>What Is An Altcoin?</h3>

<p>An alt-coin is typically known to be any cryptocurrency besides Bitcoin—and sometimes Ethereum-- since the vast majority of altcoins began as projects forked from one of the two. For the sake of this article’s coherency, I will be lumping Ethereum into the altcoin pile. Altcoins encompass a diverse range of cryptocurrencies that serve different purposes beyond just being alternatives to Bitcoin. These include stablecoins like DAI and USDC that aim to maintain price stability, utility tokens such as Chainlink (LINK) which provide specific functions within their ecosystems, meme coins like Shiba Inu (SHIB) that often rely on community and culture, and platform coins like Solana (SOL) and Cardano (ADA) that support decentralized applications and smart contracts.</p>
</div>
![Cryptocurrencies](/assets/img/crypto_set.jpg)<center>Image Credit: @myriammira on Freepik</center>

<br>

<p>If you became a little lost with terms like “stablecoin” or “smart contract”, worry not. Just know that like Bitcoin, altcoins have their own unique blockchains, economic models, reward systems, and innovations. An example of an early altcoin, Litecoin was created in 2011 to function as Bitcoin’s silver equivalent. Its design was oriented towards enabling for faster transaction completion times and it had a friendlier entry-level barrier to transaction mining.</p>


<h3>Cryptocurrency Innovation And The Blockchain Trilemma</h3>

<p>To better understand where a significant portion of the drive for innovation comes from within the cryptocurrency world, let’s examine this industry through the lens of the “blockchain trilemma”. Originally expounded by the creator of Ethereum, Vitalik Buterin, the concept refers to the trade-offs across three core design features in a blockchain: security, scalability, and decentralization.<sup><a href="#fn1" id="ref1">1</a></sup> Here, security refers to how well a network is able to resist attacks and manipulation from bad actors, scalability is determined by a network’s ability to efficiently process an increasing number of transactions as its user base increases, and decentralization refers to the degree to which network control is equally distributed to all users of the network.</p>

<p>It’s often the case that a cryptocurrency cannot improve two of the factors without sacrificing the one remaining. Bitcoin has incredible security and decentralization capabilities, but this comes at the cost of its scalability. Based on the current data I found, Bitcoin is currently only able to process somewhere around 5 <abbr title="Transactions Per Second">tps</abbr><sup><a href="#fn2" id="ref2">2</a></sup>. Compared to Ethereum at 16 tps, Solana at 1,318 tps, and Visa’s VisaNet whopping 24,000 the difference is strikingly notable<sup><a href="#fn3" id="ref3">3</a></sup>. Solana in terms of tps, fees, and developer capabilities totally blows Bitcoin out of the water, but this is at the sacrifice of network decentralization. Its network speed is largely due in part because of its high performance node hardware requirements, making the entry-barrier to participating in the network considerably higher than other cryptocurrencies.</p>



<img src="/assets/img/trilemma.png" 
        alt="Trilemma Illustration" 
        width="600" 
        height="600" 
        style="display: block; margin: 0 auto" />


<p>So in the case of developing a new cryptocurrency, developers are immediately presented with the problem of how to approach the blockchain trilemma when developing their altcoin: will their protocol feature an advanced level of network security and scalability at the expense of decentralization like Solana, or like in the case of Cardano, will the protocol seek to strike a balance between all 3 factors? This dilemma undoubtedly continues to be a driving factor in the innovation of blockchain technology today.</p>

<h3>Altcoins Today</h3>

<p>As of writing this article, the total number of altcoins in existence is around 20,000; however, it’s likely that the vast majority of these coins are inactive or discontinued projects<sup><a href="#fn4" id="ref4">4</a></sup>. In the major centralized exchanges like Coinbase and Binance, the number of cryptocurrencies being traded on these platforms is around 260 and above 360 respectively<sup><a href="#fn5" id="ref5">5</a></sup>. Altcoin trading is not limited to only centralized exchanges though. Decentralized exchanges such as Uniswap allow for a far more inclusive range of altcoin selection and any over-the-counter (OTC) trade theoretically makes it possible for any altcoin to be traded.</p>


<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Top 10 Cryptocurrencies by Market Cap</title>
    <style>
        table {
            width: 80%;
            border-collapse: collapse;
            margin: 20px auto;
        }
        th, td {
            padding: 10px;
            border: 1px solid #ddd;
            text-align: center;
        }
        th {
            background-color: #f4f4f4;
        }
    </style>
</head>
<body>
    <h1 style="text-align:center;">Top 10 Cryptocurrencies by Market Cap<sup><a href="#fn6" id="ref6">6</a></sup></h1>
    <table id="crypto-table">
        <thead>
            <tr>
                <th>Rank</th>
                <th>Name</th>
                <th>Symbol</th>
                <th>Price (USD)</th>
                <th>Market Cap (USD)</th>
                <th>24h Change (%)</th>
            </tr>
        </thead>
        <tbody>
            <!-- Data will be inserted here -->
        </tbody>
    </table>

    <script>
        async function fetchCryptoData() {
            const url = 'https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&order=market_cap_desc&per_page=10&page=1&sparkline=false';
            try {
                const response = await fetch(url);
                const data = await response.json();

                const tableBody = document.querySelector('#crypto-table tbody');

                data.forEach((coin, index) => {
                    const row = document.createElement('tr');

                    row.innerHTML = `
                        <td>${index + 1}</td>
                        <td><img src="${coin.image}" alt="${coin.name}" width="20" style="vertical-align: middle;"> ${coin.name}</td>
                        <td>${coin.symbol.toUpperCase()}</td>
                        <td>$${coin.current_price.toLocaleString()}</td>
                        <td>$${coin.market_cap.toLocaleString()}</td>
                        <td>${coin.price_change_percentage_24h.toFixed(2)}%</td>
                    `;

                    tableBody.appendChild(row);
                });
            } catch (error) {
                console.error('Error fetching data:', error);
            }
        }

        fetchCryptoData();
    </script>
</body>
</html>`

<p>All things considered, it's wise for anyone exploring the cryptocurrency space to develop a fundamental understanding of altcoins. The industry is fast-paced and constantly evolving, which can make it difficult to stay on top of. But beyond the meme coins and pump-and-dump schemes lie projects with real-world applications and long-term potential. And in a world where institutional capital and adoption are accelerating, keeping an eye on these developments could prove worthwhile. What seems speculative today may become foundational tomorrow.</p>


<div class="fn">
	<hr>
	<ol>
		<li id="fn1">
			<a href="https://www.theblock.co/learn/249536/what-is-the-blockchain-trilemma" target="_blank" rel="noopener">
				Crooks, Nathan. “What Is the Blockchain Trilemma?” The Block, 19 Sept. 2023, www.theblock.co/learn/249536/what-is-the-blockchain-trilemma. 
		</a>
		<a href="#fn1">&larrhk;</a>
		</li>
	
	
		<li id="fn2">
			<a href="https://www.blockchain.com/explorer/charts/transactions-per-second" target="_blank" rel="noopener">
				“Blockchain.com | Charts - Transaction Rate per Second.” Www.blockchain.com, www.blockchain.com/explorer/charts/transactions-per-second.
		</a>
		<a href="#fn2">&larrhk;</a>
		</li>
		
		
		<li id="fn3">
			<a href="https://chainspect.app/dashboard" target="_blank" rel="noopener">
				Chainspect. “TPS Dashboard [Real Metrics].” Chainspect, 2024, chainspect.app/dashboard. 
		</a>
		<a href="#fn3">&larrhk;</a>
		</li>
		
		
		
		<li id="fn4">
			<a href="https://www.statista.com/statistics/863917/number-crypto-coins-tokens/" target="_blank" rel="noopener">
				de Best, Raynor. “Number of Crypto Coins 2013-2021.” Statista, 22 Mar. 2022, www.statista.com/statistics/863917/number-crypto-coins-tokens/. 
		</a>
		<a href="#fn4">&larrhk;</a>
		</li>
		
		
		<li id="fn5">
			<a href="https://coinledger.io/tools/coinbase-vs-binance" target="_blank" rel="noopener">
				“Coinbase vs. Binance (June 2024) | CoinLedger.” Coinledger.io, coinledger.io/tools/coinbase-vs-binance. 
		</a>
		<a href="#fn5">&larrhk;</a>
		</li>
		
		
		<li id="fn6">
			<a href="https://www.coingecko.com/" target="_blank" rel="noopener">
				coingecko.com
		</a>
		<a href="#fn6">&larrhk;</a>
		</li>
	</ol>
</div>
