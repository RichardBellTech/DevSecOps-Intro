# Abuse cases

Threat Model v1.0 — CPS 5981 01, Week 02

**Mission:** Allow legitimate customers to register, find products, and complete purchases while keeping customer, product, and order information accurate.

Each case names an actor, what they can already do, what they do with it, what stops being
true for the mission, and what that costs.

## Case 1

- **Actor:** A person with no account.
- **Capability:** Can access the public web application and send requests without logging in.
- **Action sequence:** Sends crafted requests to the application in an attempt to access functions or data that should require authentication.
- **Mission effect:** Customer and order information can no longer be relied on as representing legitimate customer activity.
- **Impact:** Customer and order information can no longer be relied on as representing legitimate customer activity.

Because A person with no account. can Sends crafted requests to the application in an attempt to access functions or data that should require authentication., Customer and order information can no longer be relied on as representing legitimate customer activity. occurs, costing Customer and order information can no longer be relied on as representing legitimate customer activity..

## Case 2

- **Actor:** A customer with an ordinary account.
- **Capability:** Can log in normally and use the application features available to a standard customer.
- **Action sequence:** Attempts to change or access another customer’s order information by modifying identifiers or request data sent to the application.
- **Mission effect:** Order information can no longer be trusted as belonging only to the correct customer.
- **Impact:** Incorrect or exposed order information could cause customer harm, support and investigation costs, and loss of confidence in the application.

Because A customer with an ordinary account. can Attempts to change or access another customer’s order information by modifying identifiers or request data sent to the application., Order information can no longer be trusted as belonging only to the correct customer. occurs, costing Incorrect or exposed order information could cause customer harm, support and investigation costs, and loss of confidence in the application..

## Case 3

- **Actor:** A member of staff using an authorized account.
- **Capability:** Can access customer or order information needed to perform normal job duties.
- **Action sequence:** Uses legitimate staff access to view or change customer or order information beyond what is needed for the assigned job.
- **Mission effect:** Customer and order information can no longer be relied on as accurate and limited to appropriate business use.
- **Impact:** Misuse of authorized access could cause incorrect records, privacy concerns, investigation costs, disciplinary action, and loss of customer trust.A

Because A member of staff using an authorized account. can Uses legitimate staff access to view or change customer or order information beyond what is needed for the assigned job., Customer and order information can no longer be relied on as accurate and limited to appropriate business use. occurs, costing Misuse of authorized access could cause incorrect records, privacy concerns, investigation costs, disciplinary action, and loss of customer trust.A.

## Case 4

- **Actor:** An automated client or bot. 
- **Capability:** Can send repeated requests to public application endpoints at a much higher rate than a normal human user.
- **Action sequence:** Sends a large number of repeated requests to search, product, or account-related functions in order to consume application resources.
- **Mission effect:** Legitimate customers may no longer be able to search for products or use account functions reliably because application resources are being consumed by automated requests.
- **Impact:** High request volume could slow or interrupt normal use of the application, causing lost transactions, support costs, and reduced customer confidence.

Because An automated client or bot.  can Sends a large number of repeated requests to search, product, or account-related functions in order to consume application resources., Legitimate customers may no longer be able to search for products or use account functions reliably because application resources are being consumed by automated requests. occurs, costing High request volume could slow or interrupt normal use of the application, causing lost transactions, support costs, and reduced customer confidence..

## Case 5

- **Actor:** A compromised customer browser or malicious browser extension.
- **Capability:** Can alter browser behavior, read or modify page content, and interact with the application using the customer’s active session.
- **Action sequence:** Uses the customer’s active session to alter requests or submit actions the customer did not intend.
- **Mission effect:** Customer actions and order information can no longer be relied on as reflecting what the legitimate customer actually intended.
- **Impact:** Unauthorized actions could create incorrect orders, expose customer information, require investigation and recovery work, and reduce trust in the application.

Because A compromised customer browser or malicious browser extension. can Uses the customer’s active session to alter requests or submit actions the customer did not intend., Customer actions and order information can no longer be relied on as reflecting what the legitimate customer actually intended. occurs, costing Unauthorized actions could create incorrect orders, expose customer information, require investigation and recovery work, and reduce trust in the application..

## Case 6

- **Actor:** A former staff member whose account or access has not been removed
- **Capability:** Still has valid credentials or access rights that allow entry to staff-only functions or data.
- **Action sequence:** Uses the still-active staff access to view or change customer, product, or order information after authorization should have ended.
- **Mission effect:** Customer, product, and order information can no longer be relied on as being changed only by currently authorized staff.
- **Impact:** Continued access after employment or authorization ends could lead to unauthorized changes, exposure of customer information, investigation costs, and loss of trust.

Because A former staff member whose account or access has not been removed can Uses the still-active staff access to view or change customer, product, or order information after authorization should have ended., Customer, product, and order information can no longer be relied on as being changed only by currently authorized staff. occurs, costing Continued access after employment or authorization ends could lead to unauthorized changes, exposure of customer information, investigation costs, and loss of trust..
