📝 Challenge Overview
Category: Web Exploitation

Event: picoMini by CMU-Africa

Description: This challenge involves inspecting client-side source code, decoding a classic substitution cipher, and manipulating HTTP headers to bypass access controls to uncover the hidden flag.

🔍 Methodology
1. Source Code Inspection & Cipher Decoding
The first step was to inspect the HTML page source of the provided challenge URL. Buried within the source code was a developer comment containing scrambled text:
<!-- ABGR: Wnpx - grzcbenel olcnff: hfr urnqre "K-Qri-Npprff: lrf" -->

Based on the challenge context, this was recognized as a ROT13 cipher. Decoding the text revealed a hidden developer note:

NOTE: Jack - temporary bypass: use header "X-Dev-Access: yes"

2. Header Injection & Caching Bypass
The decoded note indicated that appending a custom HTTP header would bypass the gate. When initially sending the request with X-Dev-Access: yes via an interception proxy, the server responded with a 304 Not Modified. This was due to the presence of browser caching headers (If-Modified-Since and If-None-Match).

By stripping these caching headers from the request, the server was forced to process the injected bypass header and returned a 200 OK response containing the full HTML source.

3. API Endpoint Discovery
While the bypass header successfully worked on the root (/) endpoint, the flag was not located in the HTML body. Inspecting the JavaScript on the returned page revealed an API call:

>after doing api discovery 
> in burp suite 
> in the request packet of login 
> send to repeater 
> i added the X-Dev-Access: yes
>got the ctf in the response of burp!!
____________________________________________________________
