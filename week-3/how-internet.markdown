# How Internet? w/ Sean Duhaime


_Glossary_
URL: Uniform Resource Link
URI: Uniform Resource Indicator
ASCII: Character Set that is used to create URL's (no spaces, not an available character)
  - A space is represented by %20
  - This is called *Encoding*
Endpoint: Another term for URL


*Anatomy of a URL*
Protocol:// Host (or Domain) : [port] / Path ( URI ) 

*Protocols* - Dictates how data is transferred over the internet
HTTP://
HTTPS://


*Web Application Architecture*
Client/Server Relationship
Client = Web Browser

_*The Web Stack*_ (client/server architecture)
- Endpoint (https://google.com/images/penguin.png)
  - This is our request to a web server for resources
    - In particular, a `penguin.png` resource
  - Sits at the /TOP MOST LEVEL/ of Web-App Architecture
- F5's (Load Balancers)
  - Takes all requests coming in, and parses them
  - Then hands off all requests to available servers in a round-robin type fashion
    - This is to prevent congestion and improve performance
- Web Servers (EX: Apache)
  - What serves up the HTML, CSS, JS, video, images
  - Almost every web server on the internet is an Apache web server
- Application Servers (EX: Tomcat)
  - Where your applications lives (the code base)
    - You can find the `java.exe` files here
  - This is where ServiceNow lives
  - Almost every application server on the internet is a Tomcat application server
- Databases (EX: MySQL)
  - Stores data in records

*TCP/IP Suite* (encompasses the majority of data transmission on the internet)
HTTP: Highest level protocol of the entire suite
  - Sits at the very top, which is called the _Application Layer_

*NOTE*: There are also other lower level types of protocols
DHCP: Dynamic Host Control Protocol
  - This protocol assigns IP's to your computers so that you can go out and play
DNS: Domain Name Services
  - Translates domain to IP
  - Like a big phonebook for web servers (matching google.com to 192.168.28.10)
TCP: Transmission Control Protocol
IP: Internet Protocol



HTTP is a _stateless_ protocol
- _EVERYTHING_ is encapsulated in the Request/Response
  - The client does *NOT* need to remember anything about the server
  - The server does *NOT* need to remember anything about the client
- Metaphor:
  - Stateful: Open tunnel between Sean and Laurel, they know everything about each other
  - Stateless: Throwing a ball between Sean and Laurel, and they are confirming it's all good before sending back 


| Client | ----------> | Server |

Everything has to be in the /HTTP Message/
- This includes authentication, the HTTP request, etc.

_*HTTP MESSAGE*_
| Headers |   \  (Authorization)
		------ Always sent in XML or JSON
|  Body   |   /


*Status Codes*
200 - OK
201 - Created
403 - Forbidden
404 - Not Found

*Verbs*
Get - Read from the Server
Post - Insert to the Server
Put - Update existing in the Server 
Delete - Delete existing

*REST* - A convention/style of structuring your HTTP requests
- Makes use of HTTP vehicle (and verbs)
- When we create our HTTP requests, we will use the same verbiage when we write up our headers and bodies
- There is no distinction between REST and RESTful
  - `RESTful` is used when you build an API that conforms to REST standards
- Stands for `Representational State Transfer`
- Can be _inbound_ or _outbound_
  - Inbound: Provider
    - Providing resources: Amazon or Google
  - Outbound: Consumer
    - Requesting resources: You or someone else trying to visit their web site

*Auth*
- None
- Basic (username / password)
- OAuth2.0 (token-based authentiation)
  - Access Token (way to authenticate through an intemediary `ID-Provider`)
  - Refresh Token (when access token expires, refresh token goes to ID-provider and asks for another until it's denied)


*Identity Management*
_2 Main Tenents_
1. Authentication
  - Who are you?
  - 
2. Authorization
  - What are you allowed to do?
  - Gets you through the door, but limits your abilities



















