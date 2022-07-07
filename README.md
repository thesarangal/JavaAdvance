# Java (Advance)

## Network Protocol
A network protocol is an established set of rules that determine how data is transmitted between different devices in the same network. Essentially, it allows connected devices to communicate with each other, regardless of any differences in their internal processes, structure or design.

### Types of Network Protocol
- **Transmission Control Protocol (TCP)**:
  TCP is a connection-oriented protocol, which means a connection is established and maintained until the applications at each end have finished exchanging messages.

- **Internet Protocol (IP)**:
  The Internet Protocol is a set of rules for communication over the internet, such as sending mail, streaming video, or connecting to a website. An IP address identifies a network or device on the internet.

- **User Datagram Protocol (UDP)**:
  UDP is a communications protocol that is primarily used to establish low-latency and loss-tolerating connections between applications on the internet. UDP speeds up transmissions by enabling the transfer of data before an agreement is provided by the receiving party.

- **Post office Protocol (POP)**:
  The post office protocol (POP) is the most commonly used message request protocol in the Internet world for transferring messages from an e-mail server to an e-mail client. With POP3, the e-mail client requests new messages from the e-mail server, and the server “pops” all new messages out to the client.

- **Simple mail transport Protocol (SMTP)**:
  SMTP is a push protocol and is used to send the mail whereas POP (post office protocol) or IMAP (internet message access protocol) are used to retrieve those emails at the receiver’s side.

- **File Transfer Protocol (FTP)**:
  Refers to a group of rules that govern how computers transfer files from one system to another over the internet

- **Hyper Text Transfer Protocol (HTTP)**:
  HTTP is a protocol for fetching resources such as HTML documents. It is the foundation of any data exchange on the Web and it is a client-server protocol, which means requests are initiated by the recipient, usually the Web browser.

- **Hyper Text Transfer Protocol Secure (HTTPS)**:
  Data sent using HTTPS is secured via Transport Layer Security protocol (TLS), which provides three key layers of protection: Encryption: Encrypting the exchanged data to keep it secure from attackers.

- **Telnet (TErminaL NETwork)**:
  Allows you to connect to remote computers (called hosts) over a TCP/IP network (such as the internet). Using telnet client software on your computer, you can make a connection to a telnet server (that is, the remote host)

- **Gopher**:
  The Gopher protocol is a communication protocol designed for distributing, searching, and retrieving documents in Internet Protocol networks.

## HTTP
Communication between clients and servers is done by requests and responses:

- A client (a browser) sends an HTTP request to the web
- A web server receives the request
- The server runs an application to process the request
- The server returns an HTTP response (output) to the browser
- The client (the browser) receives the response

### HTTP Request
An HTTP request is made by a client, to a named host, which is located on a server. The aim of the request is to access a resource on the server.

To make the request, the client uses components of a URL (Uniform Resource Locator), which includes the information needed to access the resource. The components of a URL explains URLs.

A correctly composed HTTP request contains the following elements:
#### Request line

```GET /software/htp/cics/index.html HTTP/1.1```

  The request line is the first line in the request message. It consists of at least three items:
  1. A method. The method is a one-word command that tells the server what it should do with the resource. For example, the server could be asked to send the resource to the client.
  The path component of the URL for the request. For instance: GET, POST, PUT and DELETE etc.
  2. The path identifies the resource on the server. For instance: End URL "/software/networking/index.html"
  3. The HTTP version number, showing the HTTP specification to which the client has tried to make the message comply. For instance: HTTP/1.1

#### HTTP headers, or Header Fields.

```
Accept-Language: fr, de
If-Modified-Since: Fri, 10 Dec 2004 11:22:13 GMT
```
HTTP headers are written on a message to provide the recipient with information about the message, the sender, and the way in which the sender wants to communicate with the recipient.

Each HTTP header is made up of a name and a value.

#### Message body (if needed)
The body content of any HTTP message can be referred to as a message body or entity body. Technically, the entity body is the actual content of the message. The message body contains the entity body, which can be in its original state, or can be encoded in some way for transport, such as by being broken into chunks (chunked transfer-coding).

Message bodies are appropriate for some request methods and inappropriate for others. For example, a request with the POST method, which sends input data to the server, has a message body containing the data. A request with the GET method, which asks the server to send a resource, does not have a message body.

### HTTP Response
An HTTP response is made by a server to a client. The aim of the response is to provide the client with the resource it requested, or inform the client that the action it requested has been carried out; or else to inform the client that an error occurred in processing its request.

An HTTP response contains:
#### Status line

```aidl
HTTP/1.1 200 OK
```

The status line is the first line in the response message. It consists of three items:
1. The HTTP version number, showing the HTTP specification to which the server has tried to make the message comply. For example, the HTTP version is HTTP/1.1
2. A status code, which is a three-digit number indicating the result of the request. For example, the status code is 200
3. A reason phrase, also known as status text, which is human-readable text that summarizes the meaning of the status code. For example, the reason phrase is OK

#### HTTP headers

```aidl
Date: Thu, 09 Dec 2004 12:07:48 GMT
Server: IBM_CICS_Transaction_Server/3.1.0(zOS)
Content-type: image/jpg
```

The HTTP headers for a server's response contain information that a client can use to find out more about the response, and about the server that sent it.

This information can assist the client with displaying the response to a user, with storing (or caching) the response for future use, and with making further requests to the server now or in the future. 

#### Message body
The message body of a response may be referred to for convenience as a response body.

For a response to a successful request, the message body contains either the resource requested by the client, or some information about the status of the action requested by the client. For a response to an unsuccessful request, the message body might provide further information about the reasons for the error, or about some action the client needs to take to complete the request successfully.