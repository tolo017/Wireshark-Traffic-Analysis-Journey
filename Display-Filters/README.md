# Mastering Display Filters

**Objective:** Learn to isolate specific traffic using display filters.

## What I Did
- Applied filters for IP addresses (`ip.addr == x.x.x.x`).
- Filtered by protocol (`http`, `tcp`).
- Found HTTP POST requests (`http.request.method == "POST"`).
- Followed an HTTP stream to see a login form submission.
- Combined filters using `and`, `or`, `contains`.

## Key Takeaways
- Display filters are your scalpel – they cut through the noise.
- `Follow Stream` is the most powerful feature for seeing the full conversation.
- The `contains` operator helps find specific strings in packets.

## Filters I’ll Keep Handy
- `http.request.method == "POST"` – find form submissions.
- `tcp.flags.syn==1 and tcp.flags.ack==0` – initial SYN packets (port scan detection).
- `http contains "password"` – find packets with password fields.
- `ip.addr == 192.168.1.1 and tcp.port == 80` – traffic from a specific device on port 80.

## Screenshots
![HTTP POST Filter](Wireshark_Capture/screenshots/filter-http-post.png)
*Only POST requests are shown.*

![Follow HTTP Stream](Wireshark_Capture/screenshots/follow-http-stream.png)
*The reconstructed conversation showing login data.*
