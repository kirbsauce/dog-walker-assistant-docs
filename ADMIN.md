# Admin Guide

A short tour of the admin-only features. You'll see these sections only if your
account has the `admin` or `super` role.

## Opening the settings panel

Tap the gear icon in the header. Admins and supers see extra sections under
**TOOLS** and **USERS**.

![Screenshot: Settings panel showing admin TOOLS and USERS sections](images/admin-settings-panel.png)

## Kennel verification

The **Kennel verification** screen cross-checks each dog's roster kennel against
San José ACS's GIS data, so you can spot dogs whose location in the sheet
doesn't match where they actually are.

- **MATCH** (green) — roster and GIS agree.
- **MISMATCH** (red) — roster says one kennel, GIS says another. Investigate.
- **NOT FOUND** (yellow) — animal ID isn't in GIS today. Likely off-site or
  just-arrived.

![Screenshot: Kennel verification screen with all three status types visible](images/admin-kennel-verify.png)

Opening this screen from the settings panel automatically refreshes the data;
the timestamp under the title shows when the last batch ran. Use the refresh
icon (↺) at any time to re-run.

Tap a row to jump to that dog's detail page.

## Managing users

The **User management** section under settings lets you add or remove walkers,
set their color grade, and promote or demote roles.

Roles:

- **walker** — default; can use the app and see the roster.
- **admin** — everything a walker can do, plus the tools above.
- **super** — admin, plus can manage other admins.

New walkers must be invited by email (their shelter Google address) before they
can sign in.

![Screenshot: User management list with role and color grade controls](images/admin-users.png)

## Push notifications

Toggle **Push notifications** in the settings panel to enable browser push for
your own account. The first toggle prompts the OS to allow notifications.

The app also runs scheduled push jobs server-side (configured via cron) for
routine reminders to all subscribed walkers.
