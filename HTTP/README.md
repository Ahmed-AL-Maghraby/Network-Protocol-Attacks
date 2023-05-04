
## What's The HTTP ?
HTTP stands for Hypertext Transfer Protocol. It is an application protocol used for transmitting data over the internet.



<br>

| Name  | OSI Layer | Port | Attack  |
| ---   | ---       | ---  | ---     |
|   HTTP    |    Application       |   80  TCP | - HTTP flooding <BR> -  HTTP injection <br> - HTTP hijacking <br> - HTTP spoofing <br> - HTTP response splitting |

<br>

## HTTP status codes

| Code | Description |
| --- | --- |
| 200 OK   |   indicates that the request was successful and the server is returning the requested data  |
| 301 Moved Permanently   |   indicates that the requested resource has been permanently moved to a new URL  |
| 302 Found   |   indicates that the requested resource has been temporarily moved to a new URL  |
| 400 Bad Request   |   indicates that the client's request is malformed or invalid  |
| 401 Unauthorized   |   indicates that the client is not authorized to access the requested resource  |
| 403 Forbidden   |   indicates that the client does not have permission to access the requested resource  |
| 404 Not Found   |   indicates that the requested resource could not be found on the server  |
| 500 Internal Server Error   |   indicates that there was an error on the server while processing the request  |
| 503 Service Unavailable   |   indicates that the server is currently unable to handle the request due to a temporary overload or maintenance  |
| 201 Created   |   indicates that the request was successful and a new resource has been created on the server  |
| 204 No Content   |   indicates that the server has successfully processed the request, but there is no response to return  |
| 302 Found   |   indicates that the requested resource has been temporarily moved to a new URL  |
| 304 Not Modified   |   indicates that the client's cached copy of the requested resource is still valid and can be used  |
| 400 Bad Request   |   indicates that the client's request is malformed or invalid  |
| 401 Unauthorized   |   indicates that the client is not authorized to access the requested resource  |
| 403 Forbidden   |   indicates that the client does not have permission to access the requested resource  |
| 405 Method Not Allowed   |   indicates that the HTTP method used in the request is not supported for the requested resource  |
| 429 Too Many Requests   |   indicates that the client has sent too many requests in a given amount of time and is being rate  |  limited by the server  |
| 500 Internal Server Error   |   indicates that there was an error on the server while processing the request  |
| 503 Service Unavailable   |   indicates that the server is currently unable to handle the request due to a temporary overload or maintenance  |

<BR>

## Several Common Attacks 

1. HTTP flooding: Also known as a DDoS (Distributed Denial of Service) attack, HTTP flooding involves overwhelming a web server with a large number of requests. This can cause the server to become unresponsive or crash, making it unavailable to legitimate users.

2. HTTP injection: This type of attack involves injecting malicious code into HTTP requests or responses in order to exploit vulnerabilities in web applications. Examples of HTTP injection attacks include SQL injection and cross-site scripting (XSS) attacks.

3. HTTP hijacking: Also known as session hijacking or cookie theft, HTTP hijacking involves stealing a user's session ID or authentication credentials in order to gain unauthorized access to their account. This can be done by intercepting HTTP requests or responses or by exploiting vulnerabilities in web applications.

4. HTTP spoofing: This type of attack involves impersonating a legitimate web server or user in order to gain access to sensitive information or to execute malicious code. Examples of HTTP spoofing attacks include DNS spoofing and IP spoofing.
5. HTTP response splitting: This type of attack involves manipulating HTTP responses in order to inject malicious code into a victim's browser or to steal sensitive information. This can be done by exploiting vulnerabilities in web applications or by manipulating HTTP headers.

<br>
  
## Detect Attacks By Wireshark

+ Nmap and brute force
  
```
 http.user_agent contains "nmap"
 http.request.uri contains "admin"
 http.request.full_uri contains "admin"
```
+ Detect ataacks tools
  
```
  (http.user_agent contains "sqlmap") or (http.user_agent contains "Nmap") or (http.user_agent contains "Wfuzz") or (http.user_agent contains "Nikto")
```
  
  
+ Log4j 

```
 http.request.method == "POST"
 (ip contains "jndi") or ( ip contains "Exploit")
 (frame contains "jndi") or ( frame contains "Exploit")
 (http.user_agent contains "$") or (http.user_agent contains "==")
```

The attack starts with a "POST" request
There are known cleartext patterns: "jndi:ldap" and "Exploit.class"
  
  
<BR>

## wireshark filters

| Filter | Description |
| --- | --- |
|  http  |    This filter displays all HTTP traffic in the capture  |
|  http.request  |    This filter displays only HTTP request packets  |
|  http.response  |    This filter displays only HTTP response packets  |
|  http.host  |    This filter displays HTTP traffic for a specific host  |
|  http.request.method  |    This filter displays HTTP traffic for a specific HTTP method, such as GET or POST  |
|  http.request.uri  |    This filter displays HTTP traffic for a specific URI or URL  |
|  http.cookie  |    This filter displays HTTP traffic that includes cookies  |
|  http.user_agent  |    This filter displays HTTP traffic that includes a specific user agent  |
|  http.response.code  |    This filter displays HTTP traffic that includes a specific response code, such as 200 OK or 404 Not Found  |
|  http.request.version  |    This filter displays HTTP traffic that uses a specific version of the HTTP protocol, such as HTTP/1.1  |
|  http.content_type  |    This filter displays HTTP traffic that includes a specific content type, such as text/html or application/json  |
|  http.request.uri.query  |    This filter displays HTTP traffic that includes a specific query string in the request URI  |
|  http.request.uri.path  |    This filter displays HTTP traffic that includes a specific path in the request URI  |
|  http.response.content_length  |    This filter displays HTTP traffic that includes a specific content length in the response  |
|  http.request.uri.contains  |    This filter displays HTTP traffic that includes a specific string in the request URI  |
|  http.request.method == "POST"  |    This filter displays only HTTP POST requests  |
|  http.request.method == "GET" && |  http.request.uri contains "search"  |    This filter displays only HTTP GET requests that include the word "search" in the request URI  |
|  http.response.code >= 400  |    This filter displays HTTP traffic that includes response codes indicating errors or failures, such as 4xx or 5xx  |
|  http.request.line  |    This filter displays the first line of HTTP request messages  |
|  http.response.line  |    This filter displays the first line of HTTP response messages  |



<BR>

## Protocol on Wireshark

<img src="https://github.com/ahmed-kamal-el-maghraby/Images/blob/main/http.png" height="300" >
<img src="https://github.com/ahmed-kamal-el-maghraby/Images/blob/main/http2.PNG" height="400" >
<img src="https://github.com/ahmed-kamal-el-maghraby/Images/blob/main/http3.PNG" height="400" >


<BR>








