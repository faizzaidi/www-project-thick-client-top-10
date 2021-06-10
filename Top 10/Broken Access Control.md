---

layout: col-sidebar
title: A2 Broken Access Control
tags: OWASP Thick Client Top 10
level: 1
type: code/tool/documentation or other

---

## Description

In Two and Three-Tier architecture, access control policies such as users cannot act outside their intended permissions. Failures typically lead to unauthorized information disclosure, modification or destruction of all data, or performing a business function outside of the user's limits.

## Risk
The technical impact is attackers acting as users or administrators, users using privileged functions, or creating, accessing, updating, or deleting every record. The business impact depends on the protection needs of the application and data.

## Solution

Access control is only effective if enforced in trusted server-side code or server-less API, where the attacker cannot modify the access control check or metadata.