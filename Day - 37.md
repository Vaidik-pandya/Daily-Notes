Daily Notes : Day 37
Web API checklist part (1)
1: SOAP/XML These kind of APIs may be vulnerable to XXE, but usually DTD Declarations are disallowed in the input from the user.
2: Always check the CORS configuration of the API, as if it’s allowing to end request with the credentials from the attacker domain, a lot of damage can be done via CSRF from authenticated victims.
3: Usually some API endpoints are gong to need more privileges that others. Always try to access the more privileged endpoints from less privileged (unauthorized) accounts
4: Something like the following example might get you access to another user’s photo album:
/api/MyPictureList → /api/MyPictureList?user_id=<other_user_id>
5: Try to use the following symbols as wildcards: *, %, _, .
/api/users/*
/api/users/%
/api/users/_
/api/users/.