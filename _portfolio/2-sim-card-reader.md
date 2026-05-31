---
title: "ISO 7816 SIM Card Reader"
subtitle: "Hardware-in-the-loop SIM card analysis and sniffing"
tech: ["C", "RP2350", "ISO 7816", "Pico SDK", "Logic Analyzer"]
sort_date: 2025
order: 2
period: "2025 – 2026"
---

## Overview

Custom hardware and firmware solution for intercepting and analysing SIM card communication. Built on the **Raspberry Pi Pico 2 (RP2350)** platform, this project captures the half-duplex ISO 7816 protocol traffic between a cellular modem and its SIM card.

## Technical Details

- **ISO 7816 protocol decoding** — T=0 character-level communication captured and parsed in real time
- **RP2350 firmware** — bare-metal C using the Pico SDK, with UART-based stdio for debugging
- **Half-duplex handling** — the single-wire ISO 7816 I/O line requires careful timing and direction sensing
- **Watchdog-protected** — 5-second hardware watchdog with crash-state tracking in noinit RAM for reliable long-duration captures
- **Logic analyzer integration** — captured traces validated against Saleae logic analyzer for correctness

## Outcome

Successfully captured and decoded live SIM-modem communication, revealing ATR sequences, file system reads, and authentication exchanges. The tool provides visibility into a normally opaque communication channel, useful for debugging eSIM profile switching and modem-SIM interaction issues.
