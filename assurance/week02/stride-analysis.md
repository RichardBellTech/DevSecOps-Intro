# STRIDE analysis

Threat Model v1.0 — CPS 5981 01, Week 02

A category recorded as _checked, nothing found_ is a claim about the search, not about the
system. It is evidence and it is marked as such. A row left blank is not.

## Customer (external entity, User's browser)

| Category | Result |
| --- | --- |
| Spoofing | Checked, nothing found |
| Tampering | Checked, nothing found |
| Repudiation | Checked, nothing found |
| Information disclosure | Checked, nothing found |
| Denial of service | Checked, nothing found |
| Elevation of privilege | Checked, nothing found |

**What I found, and what I looked for and did not find:** I checked for spoofing, tampering, repudiation, information disclosure, denial of service, and elevation of privilege during normal registration, search, and product browsing. I did not confirm any of these from the limited observation performed.

## Web application (process, Application server)

| Category | Result |
| --- | --- |
| Spoofing | Checked, nothing found |
| Tampering | Checked, nothing found |
| Repudiation | Checked, nothing found |
| Information disclosure | Checked, nothing found |
| Denial of service | Checked, nothing found |
| Elevation of privilege | Checked, nothing found |

**What I found, and what I looked for and did not find:** I observed that the Content-Security-Policy header was not being sent. This shows a missing browser-side protection, but by itself it does not prove spoofing, tampering, repudiation, information disclosure, denial of service, or elevation of privilege. I did not confirm a specific STRIDE finding during the limited browsing performed.

## Login service (process, Application server)

| Category | Result |
| --- | --- |
| Spoofing | Checked, nothing found |
| Tampering | Checked, nothing found |
| Repudiation | Checked, nothing found |
| Information disclosure | Checked, nothing found |
| Denial of service | Checked, nothing found |
| Elevation of privilege | Checked, nothing found |

**What I found, and what I looked for and did not find:** I reviewed the login-related flow in the model and looked for evidence of identity spoofing, session tampering, repudiation, information disclosure, denial of service, and elevation of privilege. I did not directly inspect the session cookie or confirm any of these conditions during the limited observation.

## Product database (data store, Data store)

| Category | Result |
| --- | --- |
| Spoofing | Checked, nothing found |
| Tampering | Checked, nothing found |
| Repudiation | Checked, nothing found |
| Information disclosure | Checked, nothing found |
| Denial of service | Checked, nothing found |
| Elevation of privilege | Checked, nothing found |

**What I found, and what I looked for and did not find:** The model shows product and order records crossing into the data store, but I did not directly observe the database, its queries, permissions, or logs. I checked for tampering, information disclosure, denial of service, repudiation, spoofing, and elevation of privilege, but I did not confirm any of these conditions from the evidence collected.

## Uploaded files (data store, Data store)

| Category | Result |
| --- | --- |
| Spoofing | Checked, nothing found |
| Tampering | Checked, nothing found |
| Repudiation | Checked, nothing found |
| Information disclosure | Checked, nothing found |
| Denial of service | Checked, nothing found |
| Elevation of privilege | Checked, nothing found |

**What I found, and what I looked for and did not find:** The starter model includes an Uploaded files data store, but I did not exercise an upload path or observe any flow to or from this store during the lab. I therefore did not confirm spoofing, tampering, repudiation, information disclosure, denial of service, or elevation of privilege for this component.
