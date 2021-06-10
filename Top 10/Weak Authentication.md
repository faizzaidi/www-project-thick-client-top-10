---

layout: col-sidebar
title: A3 Weak Authentication
tags: OWASP Thick Client Top 10
level: 1
type: code/tool/documentation or other

---

## Description

An attacker can compromise the application (Tier Two and Three architecture) if account credentials and session IDs are not protected. Our experience shows that many applications use weak authentication methods. For example, when a user enters his Login ID and password, the hashed or clear text password of the corresponding Login ID is retrieved from the database and brought to the client.

The entered password is hashed at the client, and the two passwords are compared. Therefore, even on entering a wrong password for a known login ID, the actual hashed or clear text password comes to the client. The attacker can sniff hashed or clear text passwords on transit and use them for man-in-a-middle attacks or logging into the application.

## Risk

Attackers can steal passwords, gain access to the application and escalate privilege by sniffing and man-in-the-middle attack.

## Solution

The solution to this problem is to send the Login ID and the password hash from the client to the database server. The server should compare the received hash with the one stored in the database using a stored procedure and then authenticate the user. To prevent man-in-middle attacks, the client and server should communicate in the encrypted channel.