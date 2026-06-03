---
title: Admin Guide
description: Admin-only features in Dog Walker Assistant — kennel verification, user management, and notifications.
---

# Admin Guide

A tour of the admin-only features. You'll see these only if your account has the
`admin` role.

## Where admin tools live

Admin tools are in the **nav menu** (not the settings panel). Open the menu and,
alongside the walker items (Search, Kennel Map, Resources), admins also see:

- **Kennel Verification**
- **Notifications**
- **User Management**

![Screenshot: Nav menu showing admin-only items](images/admin-nav-menu.png)

## Kennel verification

**Kennel Verification** cross-checks each dog's roster kennel against the
shelter's GIS kennel data, so you can spot dogs whose location in the sheet
doesn't match where they actually are. Each row shows a status:

- **MATCH** (green) — roster and GIS agree.
- **MISMATCH** (red) — they disagree; the row shows the kennel GIS reports.
  Investigate.
- **NOT FOUND** (orange) — the animal ID isn't in GIS today. Likely off-site or
  just-arrived.

![Screenshot: Kennel verification with MATCH, MISMATCH, and NOT FOUND rows](images/admin-kennel-verify.png)

Tap **Run verification** (or **Re-run verification** afterward) to run a fresh
batch; summary counts for matches, mismatches, and not-found appear at the top.
Tap any row to jump to that dog's page.

## User management

**User Management** lists everyone with access. For each user you'll see an
active/blocked dot, their name and email, and — if you have permission — a role
control and a block/unblock action. Tap **+** to add a new user by their Google
address.

![Screenshot: User management list with role and status controls](images/admin-users.png)

Roles:

- **walker** — default; can use the app and see the roster.
- **admin** — everything a walker can do, plus the tools above. (Older `super`
  accounts display as **admin**.)

New walkers can request access themselves (you'll be notified) or you can add
them with **+**; either way they show as inactive until you approve them. The
first time you activate an account, DWA emails the walker to let them know it's
ready — replies come back to the maintainer.

## Notifications

Push notifications are **available to every user** now — each walker enables them
under **Settings → NOTIFICATIONS**, no admin role required. The admin
**Notifications** screen and the server-side scheduled jobs handle push messages
sent out to subscribed walkers (e.g. routine reminders).
