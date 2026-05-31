---
title: "Mobile Network Latency Monitor"
subtitle: "Scalable multi-MNO latency tracking platform"
tech: ["Python", "Docker", "5G", "eSIM", "SGP.22", "Containers"]
period: "March 2025 – Present"
---

## Overview

A scalable, secure, containerised platform for monitoring mobile network latency across multiple providers. Designed to track real-world network performance at scale.

## Architecture

- **Frontend website** — dashboard for visualising latency data across providers
- **Backend databases** — time-series storage with rate limiting for API protection
- **Client nodes** — distributed data collection agents running on cellular-connected hardware
- **Containerised deployment** — every component runs in Docker for portability and reproducibility

## Current Status

The proof of concept is operational and being ported to use **SGP.22 eSIMs** with switchable profiles and **5G modems**, targeting 20+ mobile network operators per client node. This enables real-time, apples-to-apples latency comparisons across providers from a single piece of hardware.
