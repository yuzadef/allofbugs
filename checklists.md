# web application testing by features

## registration
- [ ] userA use userB verification link for verification. Do the verifications need to happen in their respective browser session?
- [ ] register with existing emails, usernames or organization names. Does it overwrite the existing ones?
  - [ ] add a trailing character `%0d%0a` to the inputs. Will the backend treat it as plain text? What impact will it have on the application if 
- [ ] register for multiple accounts in a single session by using the same CSRF token repeatedly.
- [ ] reuse email verification link.
- [ ] register an URL for first name or last name? Does the application restricts this? If not, what happens to the account created?

## invitation
- [ ] invite a user to application and check the response. Is the invitation link or invitation code exposed?
- [ ] use the invitation link when admin has already deleted the invitation before that. Does the user still have access to the link?
- [ ] delete other user's invitation as a limited user on behalf of admin.

## access control
- [ ] the only admin in an organization demotes himself to 'member' role. What will happen to the organization? Will a new admin gets automatically assigned to any of the limited users in the organization?
- [ ] promote or demote other user roles on behalf of admin.
- [ ] promote or demote your own account to other user roles.

## password reset
- [ ] receive password reset link of other users via HPP (duplicate parameters)
- [ ] reuse password reset link
- [ ] password reset link leaked in 3rd party application referer header
- [ ] password reset link poisoning via host header injection
- [ ] 
