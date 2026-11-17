# AlloX Bot

**Versi:** 1.0.0 · **Harga:** Rp 80.000 (~$5) · **Kontak pembelian:** [@rmndkyl](https://t.me/rmndkyl)

AlloX is an AI-powered capital allocation platform that transforms market narratives into diversified, risk-managed portfolios. This bot automates the Season 1 reward farming: daily check-in, initial claim, and chat-to-earn messaging.

## Kebutuhan

| Item | Detail |
|---|---|
| Runtime | Node.js 18+ |
| Wallet | EVM / sesuai chain proyek (kamu sendiri) |
| Proxy | tidak perlu |
| Captcha | tidak perlu |
| Akses | akun proyek yang kamu kelola sendiri |

## Pembayaran

E-Wallet: DANA / GoPay / ShopeePay · Bank: BCA / Seabank · Crypto: contact for wallet address.
Pembeli menghubungi [@rmndkyl](https://t.me/rmndkyl), kirim bukti transfer, lalu terima license key.

---

**Automated bot for AlloX AI Agent — Season 1 Genesis campaign.**

**Campaign:** Season 1 Genesis  
**Chain:** Multi-chain (Ethereum, Base, BNB Smart Chain, Solana)  
**Reward:** $ALLOX token  
**Status:** Active (474K+ users, $2.1M+ on-chain)

---

## Features

- **Wallet Authentication** — Sign message with EVM wallet (MetaMask, Binance Wallet, WalletConnect, Phantom)
- **Season 1 Claim** — Auto-claim 5,000 initial points
- **Daily Check-in** — Auto check-in for daily rewards
- **Chat-to-Earn** — Send AI chat messages to earn 25 points/message
- **Portfolio Tracking** — View portfolio stats and history
- **Referral Tracking** — Check referral status and stats
- **Multi-Wallet Support** — Process multiple wallets sequentially
- **Rate Limit Handling** — Respects 50 messages/day limit with auto-backoff

## Requirements

| Item | Required | Cost |
|------|----------|------|
| Node.js 18+ | ✅ | Free |
| EVM Wallet (private key) | ✅ | Free |
| API endpoint | ✅ | Free |
| Captcha solver | ❌ | — |
| Proxy | ❌ | — |

**Modal:** Rp 0 — completely free. No deposit, no gas fees required.

## Installation

```bash
cd ~/LYID-BOTS/allox-bot
npm install
```

## Configuration

Copy `.env.example` to `.env` and fill in your wallet:

```env
WRAPPED_PRIVATE_KEY=0x...
API_BASE=https://api.allox.ai
```

## Usage

```bash
# Single run
node src/bot.js

# With specific wallet
WRAPPED_PRIVATE_KEY=0x... node src/bot.js
```

### Bot Flow

1. **Login** — Signs authentication message with wallet
2. **Season 1 Claim** — Claims 5,000 points if not already claimed
3. **Daily Check-in** — Performs daily check-in
4. **Chat Messages** — Sends AI chat messages (up to 50/day, 25 pts each)
5. **Portfolio Check** — Displays portfolio status
6. **Referral Check** — Displays referral info
7. **Notifications** — Checks notifications

## Campaign Type

**Type K — XP Social via REST API**

| Action | Points |
|--------|--------|
| Initial claim | 5,000 |
| Chat message | 25/message |
| Portfolio creation | 250/portfolio |
| Daily limit | 50 messages/day |

## Endpoints

```
POST /auth/verify          — Wallet login
POST /auth/refresh         — Token refresh
POST /season1/claim        — Initial 5,000 pts claim
POST /checkin              — Daily check-in
GET  /checkin/status       — Check check-in status
POST /chat/allox/message   — Send chat message
GET  /portfolio            — List portfolios
GET  /portfolio/stats/full — Portfolio stats
GET  /referral/me          — Referral info
GET  /notifications        — Notifications
```

## Troubleshooting

| Issue | Solution |
|-------|----------|
| "Invalid wallet address format" | Check WALLET_ADDRESS in .env |
| "Message limit exceeded" | Wait 24h for reset, or use different wallet |
| "Provide txHash or signature+message" | Check-in requires EVM proof — use wallet with BNB for gas |
| 429 Too Many Requests | Backoff auto-handled, wait for rate limit reset |

## Project Links

- **Website:** https://www.allox.ai
- **App:** https://app.allox.ai
- **Twitter:** https://x.com/alloxdotai
- **Telegram:** https://t.me/alloxai
- **GitHub (Private):** https://github.com/layerairdrop/allox-bot
- **CertiK Audit:** https://skynet.certik.com/projects/allox

## Contact

- **Telegram:** @rmndkyl
- **GitHub:** https://github.com/rmndkyl
- **Channel:** @layerairdrop

---

*Built by LYID Airdrop Automation — https://lyid.vercel.app*
