# Form Builder App Wireframe

A clickable, black-and-white wireframe of **India Observatory Forms** — a mobile app
for conservation field teams who collect data offline, often with no signal.

Everything is a single self-contained HTML file. No build step, no dependencies to
install: open `mobile-app-bw.html` in a browser.

## The model

A form is a **template, not a one-off task**. It can be filled any number of times,
and every submission is saved as its own **record**, titled by the field the form
marks as its record title — District, Village Name, Farm Plot ID. One form therefore
covers every location in a programme, and the same location can be recorded again
next month. Repeat visits stack under a single row for that place.

## What the prototype covers

**Filling and submitting**
- All 18 field types, with the right mobile keyboard for each
- GPS capture with permission handling, accuracy readout and manual entry when denied
- Photo capture from camera or library; finger-drawn signature stored as an image
- Required-field validation that blocks submission and marks what is missing
- Confirmation carrying a submission ID and timestamp

**Offline first**
- Records are written to the device first and queued for sync
- Waiting-to-sync records and unfinished drafts are kept distinct — a draft cannot
  sync because it is not finished

**Sections**
- Dashboard — coverage figures, search, filters
- My Forms — assigned forms, filtered by programme and status
- My Records — every submission with ID, programme, form, location, time and review
  status; full-text search
- Programmes — read-only; programmes are managed on the web portal
- Sync, Notifications, Help & Support, Profile

**Review lifecycle**
Once uploaded, a record moves Pending → Verified → Completed. That status is set by
an Org Admin on the web portal; the mobile app only displays it.

**Access**
Mobile is for Field Users only. There is no role switcher — an Org Admin account is
refused at sign-in and pointed to the web portal.

## Design

Monochrome throughout. State is carried by fill, outline and weight rather than by
hue: a solid badge is done, an outlined badge is in progress, a flat one is inactive.
Nothing in the interface depends on colour to be understood.

## Note

This is a prototype. All data is seeded in the file, state resets on reload, and the
credentials shown on the login screen are dummy values.
