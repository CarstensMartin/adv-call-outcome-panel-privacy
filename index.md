# Privacy policy: Call outcome panel

Last updated 23 September 2026.

## What this is

Call outcome panel is a private browser extension used by the people on one
call desk to log the outcome of outbound calls in one CRM, at
`crm.advplus.ae`, and to see whether the workplace a lead has given is open
right now. It is private and is installed only by named testers.

## What it handles

The extension handles personal data belonging to other people, on the
operator's own machine. It has no server, no analytics and no telemetry. It
makes no network request of its own, and it sends no data to the developer or
to any third party. Two things leave the machine, described below, and both
happen only when the operator presses a button.

- It reads the lead name, phone number and work email address that the CRM is
  already displaying on the page, so it can fill in a call comment, label a
  callback, and name the workplace it recognises from the email address.
- It writes to that CRM, using the CRM's own controls, when the operator
  presses a button: a call comment, an activity, the follow up date and
  status, and the record's Step.
- It keeps the calls logged since the last export, a marker for a call that is
  being logged at that moment, the time and file name of the last export, and
  one preference set on its options page (whose desk this profile is), in
  `chrome.storage.local` on that machine. It does not use
  `chrome.storage.sync`, so nothing is replicated to a Google account or to any
  other device.
- On one desk it can put a follow-up message on the clipboard with the lead's
  first name and workplace filled in, for the operator to paste into a chat
  they send themselves. The extension sends nothing; the clipboard is local.
- The operator can export the logged calls to a file, which is written to their
  own downloads folder and goes nowhere else.

## The two things that leave the machine

When the operator chooses an outcome that books an agreed callback, the
extension opens a new browser tab at Google Calendar's own event creation page
with the event details already filled in. The event title contains the lead's
phone number and name, so the diary entry is usable. Those details reach Google
Calendar, in the operator's own account, at the moment the operator asks for
that event and only then. The extension does not save the event; the operator
does.

When the operator presses WhatsApp, the extension opens a new browser tab at
`wa.me`, WhatsApp's own click to chat address, with the lead's phone number in
the address and the lead's name in the message box. Those details reach
WhatsApp at the moment the operator asks for that chat and only then. The
extension does not send the message; the operator does.

No other request is made to any other service.

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
beyond logging a call on the record in front of the operator. The use of this
data complies with the Chrome Web Store User Data Policy, including the Limited
Use requirements.

## Changes

If the extension changes what it stores or where anything goes, this page
changes with it.
