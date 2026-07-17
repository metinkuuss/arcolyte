Olyte
A permissionless AMM (automated market maker) built on Arc Testnet, the EVM-compatible L1 by Circle where USDC is the native gas token.
Live app: https://olyte.netlify.app
What it does
Olyte lets anyone launch a token, open a trading pool for it, and swap — all in one place, without writing any code.
Token launcher
Create a real, standalone ERC-20 token in a few seconds: name, symbol, fixed initial supply, minted directly to your wallet. No further minting after creation.
Permissionless pools
Anyone can open a USDC pool for any ERC-20 token on Arc Testnet, not just tokens launched through this app. One pool per token, priced with the constant-product formula (`x * y = k`), the same model used by Uniswap v2.
Two-sided swaps
Pick a direction (USDC → token or token → USDC), type an amount, and see a live estimate of what you'll receive before confirming.
Zap
Don't hold the paired token? Deposit USDC only. Olyte automatically swaps half of it for the paired token and deposits both sides as balanced liquidity, in a single transaction.
Real yield
A 0.30% fee on every swap stays inside the pool, so each LP share is worth a little more over time as trading happens — there is no inflationary token emission or fabricated APY, only real trading fees.
Portfolio
See every pool you've provided liquidity to, and its current value in USDC-equivalent terms, in one place.
Price charts
Rebuilt directly from on-chain swap history for each pool — no external price feed or indexer required.
Search
Filter the pool list by token symbol or contract address.
Browsable without a wallet
Anyone can browse pools and prices without connecting a wallet. Connecting is only required to trade, add liquidity, or launch a token.
Stack
Two Solidity contract families:
`TokenFactory` / `SimpleToken` — deploys standalone fixed-supply ERC-20 tokens
`AMMFactory` / `SimpleAMM` — deploys and manages USDC/token liquidity pools
Deployed with Hardhat
Frontend: vanilla JavaScript + ethers.js, no backend, no database — everything reads and writes directly on-chain
Hosted on Netlify
Network
Chain: Arc Testnet
Chain ID: 5042002
RPC: https://rpc.testnet.arc.network
Explorer: https://testnet.arcscan.app
Faucet: https://faucet.circle.com
Status
Testnet only. No real monetary value. This is an early, actively evolving build — feedback and issues are welcome.
