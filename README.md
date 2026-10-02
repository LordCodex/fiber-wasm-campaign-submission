# Fiber WASM Campaign Submission

## Reflection

I found it interesting that a complete Fiber node could run directly in the browser using WebAssembly and Web Workers.

One problem I encountered was that the public peer handshake timed out multiple times when I tried to connect. The error indicated that the node was running, but the peer handshake had timed out. I expected the connection to succeed immediately, so this was confusing. I continued retrying the connection and waiting for the peer state to update. Eventually, the connection succeeded and I was able to continue with the channel setup and payment.

The channel process also took longer than expected because it had to move through negotiation and on-chain confirmation before reaching `ChannelReady`. This helped me understand the difference between opening a funded channel on-chain and sending a fast off-chain payment.

After completing the campaign, I’m interested in building browser-based applications for instant CKB payments, such as games, tipping systems, demonstrations, and lightweight payment apps. I would improve the tutorials by adding more information about handshake timeouts, retry behavior, expected waiting times, and the different channel state transitions.

## Proof

- Quest 1: `Screenshot 2026-10-02 at 6.00.51 pm.png`
- Quest 2: `Screenshot 2026-10-02 at 6.22.05 pm.png`
- Additional intermediate payment screenshot: `Screenshot 2026-10-02 at 6.16.46 pm.png`
