# Basics
## Client
- The device (like your phone, laptop, or app) that sends a request for data. Example: Your browser when you open google.com.
## Server
- The computer that stores, processes, and sends data back to the client when requested. Example: Google’s server sends you the Google homepage when your browser asks for it.
## Protocol
- A set of rules that decides how data is sent and received over a network. Example: HTTP, HTTPS, FTP are all protocols.
## IP (Internet Protocol)
- Responsible for addressing and routing data packets so they reach the correct destination over the internet. Example: Your laptop might have an IP like 192.168.1.1 in a local network.
## TCP (Transmission Control Protocol)
- Makes sure data is delivered correctly and in order between client and server. Breaks data into smaller parts (called packets). Numbers them. Resends if any are lost. Ensures no data is missing or jumbled. Example: When you stream a video, TCP makes sure no video chunks are missing.
## Port Number
- A virtual gate through which your device communicates with the server for a particular service. Examples: Port 80 → HTTP, Port 443 → HTTPS, Port 25 → Email (SMTP). Analogy: Like different counters at a bank (cash deposit, loan enquiry) — each has a number.
## SSL (Secure Sockets Layer)
- An old encryption protocol that made internet connections secure. Fact: Now outdated and replaced by TLS.
## TLS (Transport Layer Security)
- A modern, secure version of SSL. Encrypts data so no one can read it while it’s moving between client and server. Example: When you buy something online, TLS keeps your card details safe.
## Http and Https
- **HTTP (HyperText Transfer Protocol)** is an application layer protocol used to transfer data (text, images, videos, etc.) over the web.
  - Follows a client-server model where the client sends a request, and the server responds with data.
  - Technical details:
    - Runs over TCP/IP protocols.
    - Uses port number 80.
    - Establishes a TCP connection for each request, and closes it after the response.
  - Key Features:
    - Connectionless: Connection is closed after each request-response.
    - Stateless: Server doesn’t remember previous requests from the client.
    - Media-independent: Can transfer any type of data if both sides understand it.

- **HTTPS (HyperText Transfer Protocol Secure)** is a secure version of HTTP that encrypts the data transferred over the web.
  - Protects sensitive information like passwords, personal data, and payment details by making data unreadable to attackers.
  - Technical details:
    - Uses TLS (Transport Layer Security) for encryption (earlier called SSL).
    - Runs on port number 443.
    - Ensures data confidentiality and integrity between client and server.
