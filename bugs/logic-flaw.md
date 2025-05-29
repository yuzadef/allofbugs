# business logic flaws

tags: `email-confirmation` `invitation` `purchase`

---

#### 1. email confirmation bypass leads to ATO -- `@email-confirmation`
- `description` attacker update his account to victim's email -- need to confirm the email sent to victim to achieve ATO -- race condition confuses the application and send the confirmation link to both attacker and victim -- allows attacker to achieve the ATO with zero-click.
- `impact` attacker completes the confirmation and gets access -- no victim interaction needed (zero-click ATO).

#### 2. invitation limit bypass for free-tier subscription -- `@invitation`
- `description` application restricts each workspace to only have 5 members invited -- attacker can invite more than 5 members via race condition which confuses the application with how to handle the multiple requests sent at the same time -- ultimately allows attacker to bypass the restriction.
- `impact` attacker exceeds user limit and adds unlimited members. 

#### 3. free-tier purchase limit restriction bypass -- `@purchase`
- `description` race condition allow malicious user to buy more than 1 domain while subscribed to the free tier subscription which should only allow users to buy only 1 domain
- `impact` abuse of free-tier plan.

#### 4. team members limit bypass in a workspace for free-tier subscription -- `@invitation`
- `description` improper logic on user invitation mechanism that shoud only allow free-tier users to invite up to 3 participants -- when the user invite participants, the invite status is on "Pending" -- all the users can accept the invitation and join the organization ultimately bypassing the restriction of only 3 participants for free-tier users.
- `impact` abuse of free-tier plan
