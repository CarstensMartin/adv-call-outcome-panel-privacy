# Privacy policy: Call outcome panel

Last updated 3 October 2026.

## What this is

Call outcome panel is a private browser extension used by the people on one
call desk to log the outcome of outbound calls in one CRM, at
`crm.advplus.ae`, and to see whether the workplace a lead has given is open
right now. It is private and is installed only by named testers.

## What it handles

The extension handles personal data belonging to other people, on the
operator's own machine. It has no server, no analytics and no telemetry. It
makes no network request of its own, and it sends no data to the developer or
to any third party. Three things leave the machine, described below, and each
happens only when the operator presses a button.

- It reads the lead name, phone number (and a second number when the contact
  field holds two), work email address and membership number that the CRM is
  already displaying on the page, so it can fill in a call comment, label a
  callback, name the workplace it recognises from the email address, and open
  the lead's member profile.
- It also reads the lead's tags, its lead-source label and the CRM's own
  System comment line naming the partner company, on the page the operator
  already has open, to tell a partner lead from any other and to name the
  company. The company is kept only in the day's call log on the operator's
  machine, and is sent nowhere.
- When the operator presses Number, No. 2 or Name, it copies the lead's phone
  number, second number or name to the operator's own clipboard, for their
  dialler. The clipboard is local.
- It writes to that CRM, using the CRM's own controls, when the operator
  presses a button: a call comment, an activity, the follow up date and
  status, and the record's Step.
- It keeps the calls logged since the last export, the calls an export has
  taken and not yet confirmed as saved, the time and file name of the last
  export, two preferences set on its options page (whose desk this profile
  is, and the operator's own coupon code for a promotion message they copy, and each client's coupon code for that client's deal welcome),
  and for at most two minutes the one contact the Add WA button is
  handing to WhatsApp Web, deleted the moment it is read, and a small log of
  any WhatsApp Web page element the Add WA script could not find, with how
  many times and when, and the time the Add WA script last found its WhatsApp
  registration out of date after an update, in `chrome.storage.local` on that machine. It does not use
  `chrome.storage.sync`, so nothing is replicated to a Google account or to any
  other device.
- It keeps, in the CRM tab's own session storage, the name of the pipeline
  last chosen on the leads list (B2C, for example), so the Refresh button can
  pick it again after it returns to the list. The browser clears session
  storage when the tab is closed.
- It opens the lead's own member profile on the same CRM in a new tab when
  the operator presses Membership, and on a member profile the linked partner
  or main member. Every member profile is on the site the panel already runs
  on, so nothing is sent anywhere new.
- On one desk it can put a follow-up message on the clipboard with the lead's
  first name and workplace filled in, for the operator to paste into a chat
  they send themselves, and the location of a guide file on that machine. The
  extension sends nothing; the clipboard is local.
- The operator can export the logged calls to a file, which is written to their
  own downloads folder and goes nowhere else.

## What leaves the machine

When the operator chooses an outcome that books an agreed callback, the
extension opens a new browser tab at Google Calendar's own event creation page
with the event details already filled in. The event title contains the lead's
phone number and name, so the diary entry is usable; the description carries
the callback time on both clocks, and the location field carries the place the
operator typed for the lead, if they typed one. Those details reach Google
Calendar, in the operator's own account, at the moment the operator asks for
that event and only then. The extension does not save the event; the operator
does.

On a desk where the operator has allowed it on the options page, the Add WA
button opens WhatsApp Web in a new tab and fills its New contact form with the
lead's first name, a last name carrying their company or the word B2C, and the
lead's phone number. Those details reach WhatsApp, in the operator's own
account, at the moment the operator presses Add WA and only then. The contact
is held in local storage for at most two minutes and deleted as soon as
WhatsApp Web reads it. The extension does not save the contact; the operator
does. An install that never allows the WhatsApp Web permission never runs
anything on WhatsApp.

On a desk set up with a Google Drive folder, the guide buttons open that
desk's own Google Drive folder in a new tab instead of copying a file path.
The address carries only the folder's id, which is baked into the extension
for that desk; no lead detail is in it, and nothing is uploaded. A desk
without a Google Drive folder never opens one.

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
`chrome://extensions`, deletes all of it. An exported file is the operator's
own file in their downloads folder: removing the extension does not delete it,
and the operator deletes it like any other file of theirs. Nothing is held
anywhere else for anyone to delete.

## Selling and sharing

No data is sold, shared, or transferred to any third party. No data is used for
advertising, credit assessment or lending. No data is used for any purpose
beyond logging a call on the record in front of the operator. The use of this
data complies with the Chrome Web Store User Data Policy, including the Limited
Use requirements.

## Changes

If the extension changes what it stores or where anything goes, this page
changes with it.
