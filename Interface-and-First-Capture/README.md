# First Capture & Interface Exploration

**Objective:** Get comfortable with Wireshark’s GUI, capture live traffic, and understand the three‑way handshake.

## What I Did
- Captured traffic while browsing `http://testphp.vulnweb.com`.
- Located my IP and the server’s IP.
- Identified the TCP three‑way handshake (SYN, SYN‑ACK, ACK).
- Explored the three panes: Packet List, Packet Details, Packet Bytes.

## Key Takeaways
- The three‑way handshake is the foundation of every TCP connection – if you don’t see it, something’s wrong.
- The Packet Details pane lets you drill down into each protocol layer – a must for troubleshooting.

## Useful Filter I Learned
- `tcp.flags.syn==1` – shows only SYN packets (great for finding connection starts).

## Captures
![Wireshark Interface](Wireshark_Capture/screenshots/first_capture.png)
*The main window with a captured packet selected.*

![Three‑Way Handshake](Wireshark_Capture/screenshots/SYN_packets.png)
*SYN, SYN‑ACK, ACK packets filtered.*
