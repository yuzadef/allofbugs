# Web Application Testing Checklist

## Registration
- [ ] userA use userB verification link for verification. Do the verifications need to happen in their respective browser session?
- [ ] Register with existing emails, usernames or organization names. Does it overwrite the existing ones?
  - [ ] Add a trailing character `%0d%0a` to the inputs. Will the backend treat it as plain text? What impact will it have on the application if 
- [ ] Register for multiple accounts in a single session by using the same CSRF token repeatedly.
- [ ] Reuse email verification link.
- [ ] Register an URL for first name or last name? Does the application restricts this? If not, what happens to the account created?

## Invitation
- [ ] Invite a user to application and check the response. Is the invitation link or invitation code exposed?
- [ ] Use the invitation link when admin has already deleted the invitation before that. Does the user still have access to the link?
- [ ] Delete other user's invitation as a limited user on behalf of admin.

## Access control
- [ ] The only admin in an organization demotes himself to 'member' role. What will happen to the organization? Will a new admin gets automatically assigned to any of the limited users in the organization?
- [ ] Promote or demote other user roles on behalf of admin.
- [ ] Promote or demote your own account to other user roles.
