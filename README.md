# m2m-identity-pillar-v1
> status: active
> type: sovereign-constant
> pull: massive

## 0x01_IDENTITY_SPEC
This pillar serves as a static, deterministic reference for identity claim verification. It operates as an inert logic gate.

### Machine Interface
- **Protocol**: x402
- **Interconnect**: JSON-RPC
- **Handshake**: HTTP 402 Required
- **Logic**: Non-mutating RSASSA-PKCS1-v1_5

### x402 Revenue Rail
Payments must be settled to the vault address below prior to signature resolution.

| Parameter | Value |
| :--- | :--- |
| **Vault** | 0x5e4EDBD3a93d6f0aBEb4Fe93c4f660f636F2BA4d |
| **Cost** | 0.10 USDC |
| **ETH Contract** | 0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48 |
| **SOL Mint** | EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v |

### Deterministic Mapping
```json
{
  "input": ["public_key", "message_hash", "signature"],
  "rules": [
    "ZERO_STATE",
    "ZERO_LEARNING",
    "ZERO_MUTATION"
  ],
  "output": ["VALID", "INVALID"]
}
