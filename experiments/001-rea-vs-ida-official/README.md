# 001 — REA vs IDA Official (research)

**Date:** 2026-10-18
**Type:** Research (no hands-on experiment)

## Goal

Understand what REA (Reverse Engineer Anything) is, how it differs from IDA's
official AI plugin, and what "Free & open source software connects your IDA
installation with AI agents" means.

## What was done

- Researched recent news on REA (morluto/rea, MIT-licensed MCP server + CLI,
  `npx rea-agents setup`).
- Compared REA against Hex-Rays' official IDA MCP server (HexRaysSA/ida-mcp)
  and the community ida-pro-mcp (mrexodia).

## Findings

- REA went viral in October 2026 (~40 stars on Oct 2 to ~290k by mid-Oct).
  v6.0.0 (Oct 8) was the tipping point; v6.4.0 added Android device
  inspection and JEB support.
- REA is an agent orchestration layer: it drives Ghidra/Hopper/IDA (plus
  JADX, Binwalk/Unblob) and returns findings with evidence. It does not
  replace disassemblers. Its IDA support builds on the community ida-pro-mcp.
- Hex-Rays IDA MCP is the vendor-official, IDA-only bridge: MIT-licensed,
  installed via `uvx ida-hcli mcp install`, requires IDA 9.4+ with idalib.
  Deeper IDA integration — shared IDBs across agents, live GUI sync, ~20%
  fewer tokens via "code mode".
- The tagline decoded: the connector is free and open source; the IDA
  installation itself still needs a paid license.

## Outcome

Research complete. No hands-on reversing performed (information only, per
request). A practical demo is deferred until a licensed IDA and a target
binary are available.

## Sources

- https://hex-rays.com/blog/hex-rays-ida-mcp-server
- https://github.com/HexRaysSA/ida-mcp
