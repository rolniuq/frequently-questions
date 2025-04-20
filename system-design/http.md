## HTTP Versions Overview

HTTP (HyperText Transfer Protocol) is an application-layer protocol used for communication between clients and servers, particularly in the context of web browsing.

### HTTP/1.0 (1996)
- Text-based protocol
- Built on top of TCP
- Each request opens a **new TCP connection** (no keep-alive)
- No pipelining, requests are sent and processed one at a time
- No built-in encryption (TLS was not yet standardized)

### HTTP/1.1 (1997)
- Still text-based and built on TCP
- **Connection reuse** via `keep-alive` — multiple requests per TCP connection
- **Pipelining** supported: multiple requests can be sent without waiting, but **responses must be received in order**
- Suffers from **Head-of-Line (HOL) blocking** at the application layer
- Supports TLS via `https://`

### HTTP/2 (2015)
- **Binary protocol**, not plain text
- Introduced **streams and multiplexing**: multiple independent request-response pairs over a single TCP connection
- Supports **out-of-order** responses
- Reduces latency significantly
- Still suffers from **HOL blocking**, but at the **TCP (transport) layer**
- TLS is widely used but not mandatory

### HTTP/3 (2022)
- Built on **UDP**, not TCP
- Uses the **QUIC** protocol (Quick UDP Internet Connections)
- Eliminates HOL blocking by using **independent streams**
- TLS is **mandatory and built into QUIC**
- Designed for better performance in **mobile and high-latency networks**
