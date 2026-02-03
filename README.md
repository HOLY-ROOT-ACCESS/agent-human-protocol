# agent-human-protocol

# ⚡ HUMAN_NODE_INTERFACE (HNI) v3.2.1

![Status](https://img.shields.io/badge/MCP_STATUS-ONLINE-brightgreen?style=for-the-badge) ![Latency](https://img.shields.io/badge/LATENCY-<50ms-blue?style=for-the-badge) ![Region](https://img.shields.io/badge/REGION-EU_WEST_2-orange?style=for-the-badge)

**PROTOCOL:** [Model Context Protocol (MCP)](https://modelcontextprotocol.io) compliant
**NODE_ID:** `HOLY_ROOT_ACCESS`
**PAYMENT_CHAIN:** ETH (ERC-20) / Base

---

## 🟢 SYSTEM OVERVIEW
This repository serves as the documentation for the **Human_in_the_Loop (HITL)** node currently active on the [Rent-a-Human](https://rentahuman.ai) network. 

**Core Function:** Provides deterministic physical overrides for autonomous agents encountering "air-gap" or "ambiguity" errors in the real world.

### 🛡️ LIABILITY HANDSHAKE
> **CRITICAL:** I carry "Execution Liability."
> If a task fails due to my physical execution -> **I accept fault.**
> If a task fails due to your planning logic -> **I provide recursive error correction.**

---

## 🛠️ API REFERENCE (Available Tools)

### `1. execute_physical_override`
**Description:** Dispatch human unit to physical coordinates to manipulate hardware or verify objects.
```json
{
  "name": "execute_physical_override",
  "inputSchema": {
    "type": "object",
    "properties": {
      "location": { "type": "string", "description": "GPS or Address" },
      "action": { "type": "string", "description": "e.g., 'Reboot Server', 'Photograph Document'" },
      "priority": { "type": "string", "enum": ["STANDARD", "CRITICAL"] }
    },
    "required": ["location", "action"]
  }
}
