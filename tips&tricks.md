# tips & tricks

## tags for navigation
`@2fa` `@add-to-cart`

### edge cases
- `@2fa` -- ***2fa verification bypass*** || upon verification, see if the user token (*jwt*, *base64*, *etc..*) is already assigned in the request header or body data. if already assigned, take note of the user token, drop the otp verification request so the otp is not used, make a request to "*authenticated*" endpoints/features and see if it works. attackers could bypass 2fa verification/authentication due to the implementation flaw.
- `@add-to-cart` -- ***partial dos on certain feature*** || set the quantity of the item to a large amount (e.g., *1000000), the application might not know how to handle that big of an amount and later, cause the page to hang. in a scenario where an application has a feature to share the user's cart to other users, when the other users display the big amount on their page, their page will hang and this is a partial dos bug.
