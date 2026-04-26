# PortSwigger Lab - Username Enumeration via Response Timing

## Vulnerability
Username enumeration using response timing (side-channel attack)

## Description
The application returned consistent error messages for login attempts, but response times varied depending on whether the username existed.

## What I did
- Observed that responses took longer for certain usernames
- Identified a valid username by analyzing timing differences
- Performed password testing for the valid user to gain access

## Key Learning
- Even when responses are identical, timing differences can leak information
- Side-channel attacks can bypass standard security measures
- Careful observation is critical in identifying subtle vulnerabilities

## Impact
An attacker can enumerate valid usernames without relying on visible differences, increasing the risk of brute-force attacks.

## Fix
- Ensure consistent response times for all authentication attempts
- Avoid processing differences based on username validity
- Implement rate limiting and account lockout mechanisms
