---
title: Setting Up Actions
sidebar_position: 4
description: Learn how to create and configure rules in Adobe Launch to load the Zeotap SDK, track events, and sync user identities.
---

# Setting Up Action

In Adobe Launch, **Rules** define when and how extensions should act. The Zeotap Collect Extension relies on rules to determine when to:

- [Send events](/adobe/docs/Actions/trackEvents) (e.g., page views, clicks, form submissions)
- [Sync user identities](/adobe/docs/Actions/syncUserIdentity)
- [Set consent or Brand Consent properties](/adobe/docs/Actions/setCustomConsent)

A rule in Adobe Launch follows the structure:

```
Event → Condition (optional) → Action
```

This section walks you through configuring all essential rules for Zeotap integration. Before setting up actions, make sure you have [installed](/adobe/docs/installation) and [configured](/adobe/docs/configure) the Zeotap extension.

---

## Note

- You can reuse **Data Elements** for identity variables like email, phone, or login ID.
- Use **Conditions** to scope rules to specific environments (e.g., dev vs prod) or paths.
- You may chain multiple **Track Event** actions in a single rule if needed.

---

:::warning Deprecated
`Load Zeotap SDK` rule is not needed anymore. The launch tag will load the Zeotap SDK automatically.
:::

## Load Zeotap SDK

### Purpose
Loads the Zeotap SDK on every page where you want to collect data.

### Steps

1. Navigate to **Rules > Create New Rule**
2. Name it: `Load Zeotap SDK`
3. Under **Events**, choose:
   - **Library Loaded (Page Top)**
4. Under **Actions**:
   - Extension: **Zeotap Collect**
   - Action Type: **Load SDK**
5. Click **Save** and add it to your build library

For more information about specific actions, see our guides on [tracking events](/adobe/docs/Actions/trackEvents), [syncing user identities](/adobe/docs/Actions/syncUserIdentity), and [managing consent](/adobe/docs/Actions/setCustomConsent).

