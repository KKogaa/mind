---
title: Microsoft Entra ID
tags: [azure, azure-developer-associate, cloud, identity]
up: "[[azure]]"
---

# Microsoft Entra ID

Azure's cloud identity provider (formerly Azure Active Directory). It is the **authorization server** in the OAuth2 flow described in [[azure-authentication-authorization]] — the thing the web app redirects to, and that issues the token back.

> [!note] Stub — not yet filled in.

Topics to cover for AZ-204:

- Tenants, users, groups, and service principals.
- App registrations, and the difference between a client app and an exposed API.
- Managed identities (system-assigned vs user-assigned) and why they beat storing secrets.
- Conditional access policies and MFA.
- Entra ID B2C, for letting users bring a preferred identity such as Google or Apple.

## Related

- [[azure-authentication-authorization]] — OAuth2 roles and RBAC.
- [[azure-resource-groups]] — the scope that role assignments are made against.
- [[app-service]] — its built-in authentication delegates here.
