# Trust boundaries

Threat Model v1.0 — CPS 5981 01, Week 02

Boundaries are derived from the zone each element sits in. A flow whose endpoints are in
different zones crosses one. Direction matters: the two directions between the same pair of
zones are separate boundaries, because the assumption being made differs.

Crossing flows: 4  —  distinct boundaries: 3

## 1. User's browser → Application server

**What crosses:** email address and password; search terms and order details

**Why this is a real boundary:** The customer's browser is outside the application's control, while the application server is inside the system's control. The server receives email addresses, passwords, search terms, and order details that the customer can modify before sending. The server therefore has to validate and safely handle this data rather than assume it is trustworthy.

**Confidence, and what would settle it:** I am highly confident. I directly observed registration and search input being sent from the browser to the running Juice Shop application. Browser Developer Tools showing the Network requests, or server request logs, would confirm the exact fields and requests crossing this boundary.

## 2. Application server → User's browser

**What crosses:** session token in a cookie

**Why this is a real boundary:** he application server sends a session token into the customer's browser, which is an environment the application does not fully control. The browser accepts and stores information supplied by the server, while the server is releasing authentication-related data into the client environment. The session token therefore crosses a change in ownership and trust.

**Confidence, and what would settle it:** Medium confidence. The model identifies a session token in a cookie, but I did not directly inspect the cookie during my browser observation. Browser Developer Tools showing the response headers, Cookies or Storage view, and Network traffic would confirm the exact token and its attributes.

## 3. Application server → Data store

**What crosses:** product and order records

**Why this is a real boundary:** The application server sends product and order records to a separate data-storage zone. The data store is receiving records produced by application logic and must rely on the application to send authorized, correctly structured, and appropriate data for storage. This change from application processing to persistent storage creates a separate trust decision.

**Confidence, and what would settle it:** Low to medium confidence. The starter model identifies a product database and this flow, but my browser observation did not directly expose the database or its queries. Source-code review, database configuration, schema information, or database query logs would confirm the actual storage component and the records crossing this boundary.
