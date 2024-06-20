# HTML RESPONSE STATUS CODES
### Definition:  
HTTP response status codes are part of the HTTP protocol used by web servers to indicate the result of a client's request. 

### Types of HTTP Response Codes
These status codes are grouped into five categories:  
1. Informational responses
1. Successful responses
1. Redirection messages
1. Client error responses
1. Server error responses  

## Informational responses
1. __100 Continue__
The The server has recieved the request headers, and the clent should proceed to send the request body.
2. __101 Switching Protocals__
The requester has asked the server to switch protocols, and the server has agreed to do so.
3. __102 Processing (WebDAV)__ 
The server has received and is processing the request, but no response is available yet.

## __103 Early Hints__
This status code is primarily intended to be used with the Link header, letting the user agent start preloading resources while the server prepares a response or preconnect to an origin from which the page will need resources.

## Successful Responses
1. __200 OK__
The request was successful.  
```GET:``` The resource has been fetched and transmitted in the message body.  
```HEAD:``` The representation headers are included in the response without any message body.
```PUT or POST:``` The resource describing the result of the action is transmitted in the message body.
```TRACE:``` The message body contains the request message as received by the server.
2. __201 Created__
The request was successful, and a new resource was created.
3. __202 Accepted__
The request has been accepted for processing, but the processing is not complete.
4. __Non-Authoritatively__
This response code means the returned metadata is not exactly the same as is available from the origin server, but is collected from a local or a third-party copy.
5. __204 No Content__
The server successfully processed the request, but is not returning any content.
6. __205 Reset Content__
Tells the user agent to reset the document which sent this request.
7. __206 Partial Content__
This response code is used when the ```Range``` header is sent from the client to request only part of a resource.
8. __207 Multi-Status (WebDAV)__
Conveys information about multiple resources, for situations where multiple status codes might be appropriate.
9. __226 IM Used (HTTP Delta encoding)__
The server has fulfilled a ```GET``` request for the resource, and the response is a representation of the result of one or more instance-manipulations applied to the current instance.

## Redirection Messages
1. __300 Multiple Choices__
The request has more than one possible response and the user should uchoose one of them.
2. __301 Moved Permanently__
The requested resource has been permanently moved to a new URL.
3. __302 Found__
The requested resource resides temporarily under a different URL.
4. __303 See Other__
The server sent this response to direct the client to get the requested resource at another URI with a GET request.
5. __304 Not Modified__
This is used for caching purposes.
6. __305 Use Proxy__
Defined in a previous version of the HTTP specification to indicate that a requested response must be accessed by a proxy.
7. __306 unused__
This response code is no longer used; it is just reserved.
8. __307 Temporary Redirect__
The server sends this response to direct the client to get the requested resource at another URI with the same method that was used in the prior request.
9. __308 Permanent Redirect__
This means that the resource is now permanently located at another URI, specified by the Location: HTTP Response header.

## Client Error Responses
1. __400 Bad Request__
The server could not understand the request due to invalid syntax.
2. __401 Unauthorized__
This response means "unauthenticated". That is, the client must authenticate itself to get the requested response.
3. __402 Payment Required__
The initial aim for creating this code was using it for digital payment systems, however this status code is used very rarely and no standard convention exists.
4. __403 Forbidden__
The client does not have access rights to the content; that is, it is unauthorized, so the server is refusing to give the requested resource.
5. __404 Not Found__
The server can not find the requested resource.
6. __405 Method Not Allowed__
The request method is known by the server but is not supported by the target resource.
7. __406 Not Acceptable__
This response is sent when the web server, after performing server-driven content negotiation, doesn't find any content that conforms to the criteria given by the user agent.
8. __408 Request Timeout__
The server timed out waiting for the request.

## Server Error Response
1. __500 Internal Server Error__
The server has encountered a situation it does not know how to handle.
2. __501 Not Implemented__
The request method is not supported by the server and cannot be handled. The only methods that servers are required to support (and therefore that must not return this code) are ```GET``` and ```HEAD```.
3. __502 Bad Gateway__
This error response means that the server, while working as a gateway to get a response needed to handle the request, got an invalid response.
4. __503 Service Unavailable__
The server is not ready to handle the request, typically due to being overloaded or down for maintenance.
5. __504 Gateway Timeout__
This error response is given when the server is acting as a gateway and cannot get a response in time.