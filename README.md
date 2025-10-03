# Activity 4 — ERC-20 Mini DApp (Team 06)

I built a tiny single-page DApp that talks to my ERC-20 token through MetaMask.  
The page connects a wallet, switches to the right network, loads token info, shows my balance, and lets me send tokens.

---

## TL;DR
- **My network:** DIDLab **Team 06** — Chain ID **31342** (`0x7a6e`), RPC `https://hh-06.didlab.org`
- **Teammate’s default network:** DIDLab **Team 07** — Chain ID **31343** (`0x7a6f`), RPC `https://hh-07.didlab.org`
- **Token:** `Team06Token (T06)`, **18** decimals
- **Token address (Team 06):** `0x5FbDB2315678afecb367f032d93F642f64180aa3`
- **Important:** Transfers only work when **both wallets are on the same network**. For this activity we used **Team 06**.

---

## What I built
- A one-file web app (`index.html`) with plain HTML + vanilla JS.
- No backend; it calls `window.ethereum` (MetaMask) directly.
- Reads ERC-20 `name/symbol/decimals/balanceOf`, and sends `transfer`.
- Shows a minimal “Tx Log” so I can copy the transaction hash.

---

## Network details

### Me — Team 06
- **Network name:** DIDLab Team 06  
- **RPC URL:** https://hh-06.didlab.org  
- **Chain ID (dec):** 31342  
- **Chain ID (hex):** 0x7a6e  
- **Currency:** ETH

### Teammate — Team 07
- **Network name:** DIDLab Team 07  
- **RPC URL:** https://hh-07.didlab.org  
- **Chain ID (dec):** 31343  
- **Chain ID (hex):** 0x7a6f  
- **Currency:** ETH

> If my teammate is on Team 07, they must switch to **Team 06** to receive/send **T06** for this demo.

---

## How I run the app locally
```bash
# from the repo root
npx http-server -p 8000
# then open:
http://127.0.0.1:8000

> If my teammate starts on Team 07, they must switch to **Team 06** before we exchange **T06**.

---

## Run locally
~~~bash
# from the repo root
npx http-server -p 8000
# then open this in a browser with MetaMask installed:
http://127.0.0.1:8000
~~~

---

## How to use the page
1. In the page, set **Team = 06**.  
2. Click **Connect & Switch Network** → approve in MetaMask.  
3. Paste the token address: `0x5FbDB2315678afecb367f032d93F642f64180aa3`.  
4. Click **Load Token** → **Token** shows `Team06Token (T06), 18d, 0x…` and **Balance** appears.  
5. (Optional) Click **Add Token to MetaMask** so T06 shows in **Assets**.  
6. **Transfer**: paste recipient 0x (also on Team 06), enter amount in human units (e.g., `10`), click **Send**, approve.

---

## What I verified / what I got
- Wallet connection + network switch to **Team 06** ✅  
- Token metadata & balance loaded from chain ✅  
- Sent **T06** to my teammate; they sent some back ✅  
- **Proof:** Tx hash appears in my page’s **Tx Log**; balances update in the app and in MetaMask.


