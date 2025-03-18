# Open Redirect

- Open redirect does not only occur within parameters, it can also occur in the base url (e.g. https://victim.com//evil.com => https://evil.com)
- If `//evil.com` not works, try `/%2Fevil.com`
- If the `.com` is cut, try `//evil%2E.com` -- double encoding?

### Parameters commonly vulnerable to Open Redirects
```
returnTo=
domain_name=
url=
```
