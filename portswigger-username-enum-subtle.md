# PortSwigger Lab - Username Enumeration via Subtle Differences

## Vulnerability
Username enumeration through subtle differences in responses

## What happened
- The application returned slightly different responses for valid and invalid usernames
- Differences were not obvious (required careful comparison)
- Identified a valid username by analyzing response variations
- Then performed password testing to gain access

## Key Learning
- Not all vulnerabilities are obvious — small differences matter
- Response length, wording, or behavior can reveal sensitive info
- Careful observation is critical in web security

## Fix
- Use consistent responses for all authentication attempts
- Avoid leaking any difference between valid and invalid users
