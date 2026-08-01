---
title: Work Todo
tags: [work, todo]
up: "[[goals]]"
---

# Work Todo

- sync uat to develop
## things to remember for pass to prod 29
- remove referral from get user by document number and me service, add validate card api to apim, (only remove referral from the dtos maybe because it will break referral service if we modify the user interface)
- remove referral from the user repository and model 
- make the coupon client in transaction communicate to support with the url and code instead and not with apim 
- make internal negative file to use the apim instead

- add fail_card_attempts to user table
- add ban_type, banned_at, ban_reason, unbanned_at to user table
- add the table utms
- add the table user_card_identifiers

- apis to add to apim: add utm api to apim, add validate card api to apim

### optional
- remove unecesary environment variables from transaction function
- add safety to utm api input in support

### TODO: today 
- remove coupon client to point to apim and remove subscription key

## Related

- [[bcp-lead]] — the client project these items sit under.
- [[things-todo]] — personal counterpart.
- [[azure-study-todo]] — certification counterpart.
