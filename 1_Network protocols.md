### *Introduction:*

- This is the first video in a series on high-level design, focusing on network protocols.
- Explains the role of network protocols in communication between computers.
- Introduces the concept of client-server and peer-to-peer models.
- Provides insights on choosing the right protocol for specific applications like WhatsApp, Google Meet, etc.

### *Network Protocols:*

- *Definition:* Network protocols define the rules and regulations for communication between systems over a network.
- *OSI Model:* Refers to the Open Systems Interconnection Model, a layered architecture for network communication (not covered in detail).
- *Key Layers:*
    - *Application Layer:* Handles user-facing communication (e.g., web browsing, email).
    - *Transport Layer:* Manages reliable data transfer between applications (e.g., TCP/UDP).

### *Application Layer Protocols:*

- *Client-Server Model:*
    - *Client:* Initiates requests (e.g., web browser).
    - *Server:* Responds to requests (e.g., web server).
    - *Examples:* HTTP, FTP, SMTP, IMAP, Web Sockets.
- *Peer-to-Peer Model:*
    - *Peers:* all machines can send and receive requests from each other
    - *Example:* File sharing, instant messaging, WebRTC.

*HTTP (Hypertext Transfer Protocol):*

- *Key Points:*
    - Most widely used protocol for web communication.
    - Connection-oriented.
    - Used for accessing web pages, web applications.
- *Example:* WhatsApp (uses web sockets over HTTP for messaging).

*FTP (File Transfer Protocol):*

- *Key Points:*
    - Transferring files between computers.
    - Two connections: Control connection and Data connection.

*SMTP (Simple Mail Transfer Protocol):*

- *Key Points:*
    - Sending emails.
    - Works with IMAP for receiving and reading emails.

*IMAP (Internet Message Access Protocol):*

- *Key Points:*
    - Receiving and reading emails.
    - Allows access to emails from multiple devices.

### *Transport Layer Protocols:*

- *TCP (Transmission Control Protocol):*
    - *Key Points:*
        - Connection-oriented (establishes a virtual connection).
        - Divides data into packets and sequences them for reliable transmission.
        - Provides error checking and retransmission.
    - *Use Case:* WhatsApp, applications requiring reliable data transfer.
- *UDP (User Datagram Protocol):*
    - *Key Points:*
        - Connectionless.
        - Sends data in packets without establishing a connection.
        - No guarantee of delivery or order.
        - Faster and more efficient than TCP.
    - *Use Case:* Live streaming, video calling, applications where some data loss is acceptable.

### *Key Takeaways:*

- *Understanding network protocols is crucial for designing distributed systems.*
- *Client-server and peer-to-peer models are fundamental architectures for communication.*
- *TCP provides reliable data transfer, while UDP prioritizes speed.*
- *The choice of protocol depends on the specific requirements of the application.*
