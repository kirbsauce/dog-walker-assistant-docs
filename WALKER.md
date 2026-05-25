# Walker Guide

A short tour of the app for shelter walkers.

![Screenshot: Roster screen, default WALK ORDER sort](images/walker-roster.png)

## Signing in

DWA uses your shelter Google account. Tap **Sign in with Google** on the launch
screen and pick your address; an admin must have added you to the walker list
beforehand. If sign-in fails, message an admin.

## The roster screen

The roster lists every adoptable dog in the kennel today. Each row shows:

- **Kennel** — where to find the dog (e.g. `AC03`).
- **Name** — the dog's name; **bold** name means recent surgery or bold-potty.
- **Color** — the dog's color grade (see below).
- **W1 / W2** — first and second walk checkboxes.
- **PG** — playgroup attended.

Tap a row to open the dog's detail page; tap a checkbox to mark the slot done.

![Screenshot: Roster row with W1/W2/PG columns annotated](images/walker-roster-row.png)

## Color grades

Each dog wears a color from easiest to hardest:

> Green → Pink → Aqua → Blue− → Blue → Gold− → Gold → Red → Black

Your own color grade (set in the settings panel) is the **hardest** color you're
qualified to walk. You can walk any dog at or below your grade. Dogs above your
grade appear dimmed at the bottom of the list when a view-based sort like WALK
ORDER is active.

## Checking off walks

When you walk a dog, tap **W1** (or W2 if W1 is already done). The checkbox
writes back to the shelter Google Sheet; the page refreshes once the write
propagates. There's no separate undo button — tap a checked box again to clear
it.

Cell colors tell you what's pending:

- **Yellow / amber** on a walk cell — that walk slot is urgent.
- **Green** on PG — the dog is reserved for playgroup but hasn't attended yet.
- **Cyan** on W1 — the dog is reserved for training but hasn't walked yet.

A check on a cell wins over its color — once you check the box, the prior
background drops.

## The WALK ORDER sort

The default sort puts the hardest color you can walk at the top. Within a
color, dogs go yellow (urgent) → amber (dim) → neutral → reserved → done. Dogs
above your color grade fall to the bottom, dimmed.

![Screenshot: SORT BY overlay with WALK ORDER selected](images/walker-sort-overlay.png)

You can pick a different sort from the **SORT BY** overlay (sort icon in the
header). WALK ORDER (and other view-based sorts) are one-way orderings — the
asc/desc toggle is only used for plain field sorts like name or kennel.

## FAQ

**Why doesn't my checkbox tick stick?** The write goes to the source Sheet;
the page reads from a mirror that updates via `IMPORTRANGE`. Give it a few
seconds and pull-to-refresh if needed.

**Why is a dog dimmed?** Their color grade is higher than yours. You can still
see them, but they're not on your walk list today.

**Where's the refresh button?** Top-right of the header. On mobile you can also
pull the roster down to refresh.
