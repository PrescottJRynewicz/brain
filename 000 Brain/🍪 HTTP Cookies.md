---
Created On: 2023-08-23, 17:04
Unique ID: 202308231704
---
**Status:** #thought 

**Tags:**  [[Software Engineering]] [[Web Development]] #SoftwareCards 

# 🍪 HTTP Cookies

#### What is an HTTP Cookie
?
A cookie is a ***small*** piece of data that a web server sends to a client. The client can store this information and return it to the server later. Cookies remember **stateful** information for the stateless HTTP protocol. 
<!--SR:!2025-01-19,345,250-->


#### How do you set a Cookie? 
?
In your web server (or any server a client is interaction with), you respond with the `Set-Cookie` header.
<!--SR:!2025-10-15,489,270-->

#### How do you define the lifetime of a cookie?
?
1. Session cookie: The browser determines when a session ends (and some browsers restore sessions, so the cookie would never go away).
2. _Permanent_ cookies are deleted at a date specified by the `Expires` attribute or after a period specified by the `Max-Age` attribute.
<!--SR:!2024-09-04,35,170-->


#### What is the `Secure` cookie attribute?
?
This means cookies will only be sent over SSL-verified (`https`) connections.
<!--SR:!2025-07-09,516,310-->

#### What is the `HttpOnly` cookie attribute?
?
This means that the cookie is not accessible to the `Document.cookie` Javascript API.
<!--SR:!2024-09-16,52,210-->

#### What is the `Domain` cookie attribute?
?
This specifies which domains can receive a cookie.
<!--SR:!2027-02-09,971,310-->

#### What is the Path cookie attribute?
?
This attribute specifies a path that must exist for the cookie to be sent.
<!--SR:!2025-08-17,430,250-->


#### What is the `SameSite` cookie attribute?
?
This attribute will only send cookies if the cookie is from the origin site.
<!--SR:!2024-09-07,54,230-->

#### What are the options for the `SameSite` cookie attribute?
?
With `Strict`, the browser only sends the cookie with requests from the cookie's origin site. `Lax` is similar, except the browser also sends the cookie when the user _navigates_ to the cookie's origin site (even if the user is coming from a different site). For example, by following a link from an external site. `None` specifies that cookies are sent on both originating and cross-site requests, but _only in secure contexts_ (i.e., if `SameSite=None` then the `Secure` attribute must also be set). If no `SameSite` attribute is set, the cookie is treated as `Lax`.
<!--SR:!2024-10-28,257,241-->










---
# References

[MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
