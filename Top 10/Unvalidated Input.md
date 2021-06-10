---

layout: col-sidebar
title: A1 Unvalidated Input
tags: OWASP Thick Client Top 10
level: 1
type: code/tool/documentation or other

---

## Definition

In many thick client applications (Three-Tier architecture), the user requests are not validated before being used by the application. Attackers can use this flaw to launch injection attacks like SQL, XML, JSON, and more. An injection attack is possible when the application does not validate user input for special characters and codes. An attacker can exploit this vulnerability by supplying specially crafted statements to the application.


## Risk

This attack can result in authentication bypass, viewing unauthorized data, application malfunction, data deletion, or malicious command injection, including database shutdown.

## Solution

The solution to this problem is input validation. The application should check for any special character and code in the user input. If any special character like ' or command code is present, the application should ignore the input and throw an appropriate error message to the user.

