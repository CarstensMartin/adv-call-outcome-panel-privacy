# Privacy policy: ADV+ call outcome panel

Last updated 13 September 2026.

## What this is

ADV+ call outcome panel is a private browser extension used by the people on
one call desk to log the outcome of outbound calls in one CRM, at
`crm.advplus.ae`, and to see whether the workplace a lead has given is open
right now. It is private and is installed only by named testers.

## What it collects

**Nothing.** The extension has no server, no analytics and no telemetry. It
makes no network request of its own, and it sends no data to the developer or
to any third party.

## What it handles, and where that stays

The extension does work with personal data belonging to other people, on the
operator's own machine. Being clear about that matters more than the fact that
none of it is collected.

- It reads the lead name, phone number and work email address that the CRM is
  already displaying on the page, so it can fill in a call comment, label a
  callback, and name the workplace it recognises from the email address.
- It writes call comments and activity entries back to that CRM, using the
  CRM's own controls, when the operator presses a button.
- It keeps the calls logged since the last export, and the operator's own panel
  settings (whether the panel is showing, the area last typed, and one
  preference set on its options page, whose desk this profile is), in
  `chrome.storage.local` on that machine. It does not use
  `chrome.storage.sync`, so nothing is replicated to a Google account or to any
  other device.
- On one desk it can put a follow-up message on the clipboard with the lead's
  first name and workplace filled in, for the operator to paste into a chat
  they send themselves. The extension sends nothing; the clipboard is local.
- The operator can export the logged calls to a file, which is written to their
  own downloads folder and goes nowhere else.

## The one thing that leaves the machine

When the operator chooses an outcome that books an agreed callback, the
extension opens a new browser tab at Google Calendar's own event creation page
with the event details already filled in. The event title contains the lead's
phone number and name, so the diary entry is usable.

That means those details reach Google Calendar, in the operator's own account,
at the moment the operator asks for that event and only then. The extension
does not save the event; the operator does. No other request is made to any
other service.

## Permissions

- `storage` keeps the operator's own working state on their own machine, so a
  page navigation in the CRM does not lose a day of un-exported calls.
- `https://crm.advplus.ae/*` is the single site the panel runs on. There is no
  wildcard, no other host and no optional permission that could later widen
  without a new review.

## Data retention and deletion

Everything the extension stores is in the browser profile on the operator's
machine. Removing the extension, or clearing its site data from
`chrome://extensions`, deletes all of it. There is nothing held anywhere else
for anyone to delete.

## Selling and sharing

No data is sold, shared, or transferred to any third party. No data is used for
advertising, credit assessment or lending. No data is used for any purpose
beyond logging a call on the record in front of the operator.

## Changes

If the extension changes what it stores or where anything goes, this page
changes with it.
