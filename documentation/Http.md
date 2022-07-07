# HTTP
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

Also Check:
- [Query string](https://en.wikipedia.org/wiki/Query_string)
- [List of HTTP header fields](https://en.wikipedia.org/wiki/List_of_HTTP_header_fields)

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

### HTTP Methods

#### GET
The GET method is used to retrieve information from the given server using a given URI. Requests using GET should only retrieve data and should have no other effect on the data.

#### HEAD
Same as GET, but transfers the status line and header section only.

#### POST
A POST request is used to send data to the server, for example, customer information, file upload, etc. using HTML forms.

#### PUT
Replaces all current representations of the target resource with the uploaded content.

#### DELETE
Removes all current representations of the target resource given by a URI.

#### CONNECT
Establishes a tunnel to the server identified by a given URI.

#### OPTIONS
Describes the communication options for the target resource.

#### TRACE
Performs a message loop-back test along the path to the target resource.

### Status Codes and Reason Phrases

In the HTTP response that is sent to a client, the status code, which is a three-digit number, is accompanied by a reason phrase (also known as status text) that summarizes the meaning of the code.

Along with the HTTP version of the response, these items are placed in the first line of the response, which is therefore known as the status line.

The status codes are classified by number range, with each class of codes having the same basic meaning.
- The range 100-199 is classed as Informational.
- 200-299 is Successful.
- 300-399 is Redirection.
- 400-499 is Client error.
- 500-599 is Server error.

Some mostly used HTTP Status Code:
- HTTP Status Code 200 - OK
- HTTP Status Code 201 - Created
- HTTP Status Code 301 - Permanent Redirect
- HTTP Status Code 302 - Temporary Redirect
- HTTP Status Code 401 - Un-Authentication
- HTTP Status Code 403 - Refuse to Accept i.e. Cause of Permissions
- HTTP Status Code 404 - Not Found
- HTTP Status Code 410 - Gone
- HTTP Status Code 500 - Internal Server Error
- HTTP Status Code 503 - Service Unavailable

Also Check:
- [List of HTTP status codes](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes)
- [HTTP response status codes](hhttps://developer.mozilla.org/en-US/docs/Web/HTTP/Status)

##### *Source: Internet*