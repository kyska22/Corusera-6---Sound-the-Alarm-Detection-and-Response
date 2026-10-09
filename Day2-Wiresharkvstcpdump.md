# Wireshark vs. tcpdump

## Overview

Wireshark and tcpdump are network protocol analyzers used to capture and analyze network traffic. Although they share several capabilities, they differ significantly in their interfaces, filtering workflows, and typical use cases.

## Comparison

| Aspect | Wireshark | tcpdump |
|---|---|---|
| Interface | Graphical User Interface (GUI) | Command-Line Interface (CLI) |
| Primary use | Interactive packet analysis | Packet capture and command-line analysis |
| Filtering | Capture filters and powerful display filters | Capture filters based on libpcap/BPF |
| Packet inspection | Detailed protocol dissection, packet details and hexadecimal/ASCII views | Command-line packet summaries and captured data |
| Remote environments | Can be used through TShark, but primarily GUI-oriented | Well suited to remote systems and servers without GUI access |
| License | Open source, GNU GPL | Open source, BSD 3-Clause |

## Similarities

- Both capture and analyze network traffic.
- Both use `libpcap` for packet capture.
- Both can work with packet capture files such as `pcap`.
- Captures produced by tcpdump can be opened and analyzed in Wireshark.

## Visual comparison

```mermaid
flowchart LR
    W["🦈 Wireshark<br/><br/>
    • GUI<br/>
    • Interactive analysis<br/>
    • Protocol dissectors<br/>
    • Display filters"]

    S["🔎 Shared capabilities<br/><br/>
    • Packet capture<br/>
    • Traffic analysis<br/>
    • libpcap<br/>
    • Capture filters<br/>
    • PCAP files"]

    T["💻 tcpdump<br/><br/>
    • CLI<br/>
    • Terminal-based capture<br/>
    • Remote/server environments<br/>
    • BPF/libpcap filters"]

    W --- S
    S --- T
