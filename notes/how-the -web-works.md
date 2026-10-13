# TryHackMe: How the Web Works

**Learning Path:** Pre Security
**Platform:** TryHackMe
**Status:** Completed
**Tools Used:** Web browser

## 1. Overview

I completed the *How the Web Works* room on TryHackMe as part of my cybersecurity learning journey. This room helped me develop a better understanding of how websites work and how browsers communicate with web servers.

My main learning areas included DNS, URL structure, HTTP and HTTPS, HTTP methods, and HTTP status codes. I found the different parts of a URL and the meanings of HTTP status codes particularly interesting.

This write-up documents my learning and provides a reference for concepts that are important when studying web technologies and web application security.

## 2. Key Concepts Learned

### 2.1 Domain Name System (DNS)

The Domain Name System (DNS) translates domain names, such as `example.com`, into IP addresses that computers can use to locate network services.

**Why it matters in cybersecurity:** Understanding DNS helps explain how users reach websites and provides useful context when investigating domains, resolving connectivity problems, or studying suspicious web activity.

### 2.2 Understanding URL Structure

A Uniform Resource Locator (URL) identifies the location of a resource and can specify how it should be accessed.

Example:

`https://www.example.com:443/products/item?id=25#details`

The different components include:

| Component    | Example          | Function                                           |
| ------------ | ---------------- | -------------------------------------------------- |
| Scheme       | `https`          | Specifies the protocol used to access the resource |
| Subdomain    | `www`            | Identifies a subdomain of the main domain          |
| Domain name  | `example.com`    | Identifies the domain                              |
| Port         | `443`            | Specifies the network service port                 |
| Path         | `/products/item` | Identifies the requested resource path             |
| Query string | `?id=25`         | Passes parameters to the resource                  |
| Fragment     | `#details`       | Identifies a section within the resource           |

Not every URL contains all these components. Ports may also be omitted when the browser uses the protocol's default port.

**Cybersecurity relevance:** Understanding URL structure can help when examining suspicious links, identifying misleading domains, and recognizing parameters that may influence how a web application behaves.

### 2.3 HTTP and HTTPS

HTTP (Hypertext Transfer Protocol) is used for communication between clients, such as web browsers, and web servers.

HTTPS is HTTP carried over Transport Layer Security (TLS). TLS helps protect communications through encryption, integrity protection, and server authentication.

Common default ports are:

* **HTTP:** Port 80
* **HTTPS:** Port 443

These are default ports, not requirements that every web server must follow. A service can be configured to use a different port.

One important lesson is that HTTPS helps protect data in transit, but it does not automatically mean that a website is legitimate or free from vulnerabilities.

### 2.4 HTTP Methods

HTTP methods describe the intended action associated with a request.

| Method    | Typical purpose                                                  |
| --------- | ---------------------------------------------------------------- |
| `GET`     | Retrieve a resource                                              |
| `POST`    | Submit data or request processing                                |
| `PUT`     | Create or replace a resource at a specified target               |
| `PATCH`   | Partially modify a resource                                      |
| `DELETE`  | Request deletion of a resource                                   |
| `HEAD`    | Retrieve response headers without the response body              |
| `OPTIONS` | Discover communication options supported by a server or resource |

The server's implementation and permissions determine what actually happens when a request is received.

**Cybersecurity relevance:** Understanding HTTP methods provides a foundation for analyzing web requests, application behavior, access controls, and potential security weaknesses.

### 2.5 HTTP Status Codes

HTTP status codes communicate the outcome of a request. They are grouped into five classes:

| Code range | Category      | Meaning                                                          |
| ---------- | ------------- | ---------------------------------------------------------------- |
| `1xx`      | Informational | The request process is continuing                                |
| `2xx`      | Success       | The request was successfully received, understood, and handled   |
| `3xx`      | Redirection   | Further action is needed, often to access another location       |
| `4xx`      | Client error  | There is an issue with the request or the client's authorization |
| `5xx`      | Server error  | The server failed to fulfil an apparently valid request          |

Some useful examples are:

* **200 OK:** The request succeeded.
* **301 Moved Permanently:** The resource has a permanent new location.
* **302 Found:** The resource is temporarily located elsewhere.
* **400 Bad Request:** The server cannot or will not process the request because of a perceived client error.
* **401 Unauthorized:** Valid authentication credentials are missing or invalid, depending on the authentication scheme.
* **403 Forbidden:** The server refuses to fulfil the request.
* **404 Not Found:** The requested resource could not be found.
* **500 Internal Server Error:** The server encountered an unexpected condition.

Learning about these codes was one of the most interesting parts of the room for me because they help explain how a web request is handled and what a response may indicate.

Status codes provide useful clues, but they do not always reveal the full cause of a problem. The response body, headers, application logs, and surrounding context may also be needed.

## 3. My Learning Experience

I used a web browser to work through the room's learning material and questions.

The concepts that stood out most to me were:

* Identifying the different components of a URL and understanding their functions.
* Distinguishing HTTP from HTTPS and learning their common default ports.
* Understanding that HTTP methods communicate the intended action of a request.
* Learning how HTTP status codes are grouped and what common codes indicate.

These concepts helped me connect what happens in a browser with the underlying communication between a client and a web server.

## 4. Relevance to Cybersecurity

Understanding how the web works provides a foundation for further cybersecurity learning, particularly web application security and penetration testing.

This knowledge can help me build toward:

* Examining URLs and identifying suspicious links.
* Understanding web requests and responses.
* Interpreting status codes during troubleshooting and security analysis.
* Learning how web applications handle requests, authentication, and access control.

These are foundational concepts I can build on as I progress through my cybersecurity training.

## 5. Key Takeaway

Completing *How the Web Works* strengthened my understanding of the basic technologies behind websites. I learned how DNS, URL components, HTTP methods, status codes, and web servers fit into web communication.

My next step is to continue developing these foundations through further hands-on cybersecurity exercises and structured learning.

---

**Learning source:** TryHackMe — How the Web Works
**Author:** Esther Anne
**Profile:** https://tryhackme.com/p/E.Annie

*This document is a personal learning summary supported by general technical explanations. It is not a record of independent penetration testing or vulnerability assessment.*

