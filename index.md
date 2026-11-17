# Privacy policy: Call outcome panel

Last updated 17 November 2026.

## What this is

Call outcome panel is a private browser extension used by the people on one
call desk to log the outcome of outbound calls in one CRM, at
`crm.advplus.ae`, and to see whether the workplace a lead has given is open
right now. It is private and is installed only by named testers.

## What it handles

The extension handles personal data belonging to other people, on the
operator's own machine. It has no server, no analytics and no telemetry. It
makes no network request of its own and sends no data to the developer.
Nothing is sent anywhere except where the operator presses a control that
opens or fills another site, listed below under What leaves the machine. Four
things leave the machine in that way, and each happens only after the
operator presses a button.

- It reads the lead name, phone number (and a second number when the contact
  field holds two), work email address and membership number that the CRM is
  already displaying on the page, so it can fill in a call comment, label a
  callback, name the workplace it recognises from the email address, and open
  the lead's member profile.
- It also reads the lead's tags, its lead-source label and the CRM's own
  System comment line naming the partner company, on the page the operator
  already has open, to tell a partner lead from any other and to name the
  company. To find that System line it reads the lead's comment history; no
  other comment is kept. It also reads the Program, Package, Plan, Clubs and
  Total Price of the CRM's own booking entries for the lead, to show them in
  the panel and to tell which employer the lead belongs to; they are not kept. The company is kept in the day's call log on the operator's
  machine. It also goes where the operator asks the panel to put it: into a
  message or email draft the operator sends themselves, and, when the
  operator presses Add WA, into the WhatsApp contact's last name (described
  below). It is sent nowhere else.
- When the operator presses Number, No. 2 or Name, it copies the lead's phone
  number, second number or name to the operator's own clipboard, for their
  dialler. When the CRM's comment box cannot be filled, it puts the call
  comment on the clipboard instead, and shows it in the panel to copy by hand
  if the clipboard refuses. The clipboard is local.
- It writes to that CRM, using the CRM's own controls, when the operator
  presses a button: a call comment, an activity, the follow up date and
  status, and the record's Step. When an activity cannot be saved or
  confirmed, the panel writes a line to the browser's developer console with
  the last four digits of the lead's number; it stays in the console and is
  not stored or sent.
- On a named desk, an email button drafts an email in the CRM's own New
  email composer, with the lead's first name, their company when the lead is
  a partner's, and that desk's signature filled in. It never presses Send:
  the operator reads the draft and sends it, or does not. If the composer
  refuses the draft, the draft is put on the operator's clipboard instead.
- On a desk where the operator has ticked Maqsam Call in the panel on the
  options page, the panel shows a Dialler for the lead on screen: Call, Hang
  up and Mute, worked through Maqsam's web dialer (described below). A desk
  that never ticks it has no Dialler and never runs anything on Maqsam.
- It keeps the calls logged since the last export, the calls an export has
  taken and not yet confirmed as saved, the time and file name of the last
  export, the settings made on its options page (whose desk this profile
  is, the operator's own coupon code for a promotion message they copy, each
  client's coupon code for that client's deal welcome, and, on a desk that
  ticked Maqsam Call in the panel, whether the Dialler logs rang-out,
  voicemail and DNCR calls by itself), on a desk that allowed WhatsApp Web
  the one contact the Add WA button is handing to WhatsApp Web, deleted the
  moment it is read and otherwise by the panel on the CRM page once it is two
  minutes old, a small log of any WhatsApp Web page element the Add WA script
  could not find, with how many times and when and a short note of the miss
  (which can name the lead's country and dial code), and the time the Add WA
  script last found its WhatsApp registration out of date after an update,
  in `chrome.storage.local` on that machine. It does not use
  `chrome.storage.sync`, so nothing is replicated to a Google account or to any
  other device.
- Each logged call holds the lead's phone number, which identifies the row,
  the call comment, the outcome, the time, the desk, whether the Dialler or a
  press logged it, and, where known, whether the lead is B2B or B2C, the
  partner company and the domain of the lead's work email. The exported file
  holds the same. Logged calls stay in `chrome.storage.local` until the
  operator exports them and confirms the export was saved; nothing deletes
  them by age.
- It keeps, in the CRM tab's own session storage, the name of the pipeline
  last chosen on the leads list (B2C, for example), so the Refresh button can
  pick it again after it returns to the list. The browser clears session
  storage when the tab is closed.
- On a desk that ticked Maqsam Call in the panel, it keeps in the browser's
  session storage which CRM tab placed the last call (a tab number, nothing
  about the lead), so the call's end is reported to the tab that asked for
  it. The browser clears it when the browser closes.
- It opens the lead's own member profile on the same CRM in a new tab when
  the operator presses Membership. Where the lead shows a membership number
  but no profile link, the button opens the CRM's Members search in a new
  tab instead, with that membership number in the page's address.
- On a member profile the same button, Open lead, opens the CRM's own search
  page in a new tab with the member's phone number, or their email when no
  phone number can be read, in the page's address, and the operator picks
  the lead from the results. That address, and so the browser's history,
  carries the phone number or email. Nothing is stored for it.
- Every page these two buttons open is on the site the panel already runs
  on, so nothing is sent anywhere new.
- On a named desk it can put a follow-up message on the clipboard with the
  lead's first name and workplace filled in, for the operator to paste into
  a chat they send themselves, and the location of a guide file on that
  machine. The extension sends nothing; the clipboard is local.
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

On a named desk the Add WA button opens WhatsApp Web in a new tab. Only once
the operator has allowed WhatsApp Web on the options page does it also fill
its New contact form with the lead's first name, a last name carrying their
surname and, in brackets, their company or the word B2B or B2C, and the
lead's phone number. Those details reach WhatsApp, in the operator's own
account, at the moment the operator presses Add WA and only then. The contact
is held in local storage until WhatsApp Web reads it, which deletes it at
once; one that no WhatsApp tab read is deleted by the panel on the CRM page
once it is two minutes old, and none is kept when the WhatsApp tab fails to
open. The extension does not save the contact; the operator does. Without
that permission Add WA stores nothing and fills nothing: it only opens
WhatsApp Web, and nothing runs on WhatsApp.

On a desk set up with a Google Drive folder, the guide buttons open that
desk's own Google Drive folder in a new tab instead of copying a file path.
The address carries only the folder's id, which is baked into the extension
for that desk; no lead detail is in it, and nothing is uploaded. A desk
without a Google Drive folder never opens one.

On a desk where the operator has ticked Maqsam Call in the panel on the
options page, which asks Chrome for permission to work on Maqsam's web dialer
at `portal.av.maqsam.com`, the Dialler's Call button opens Maqsam's web dialer
in a tab behind the CRM, in the operator's own Maqsam account, types the
lead's phone number into the dialer's own number field and presses the
dialer's own Call button. If, at the press, the extension finds that
permission is not held (for example just after it was withdrawn), Call
instead opens Maqsam's web dialer in a new tab with the lead's phone number in
the page's address, so the browser's history carries it. Hang up and Mute
press Maqsam's own buttons. While
that tab is open, the extension reads what the dialer shows, such as whether a
call is ringing, connected or ended and any refusal message, and shows it in
the panel; it stores none of it. For two minutes after each press the panel
also writes a line to the browser's developer console for each change the
dialer shows, with any phone number shortened to its last three digits; that
line stays in the console and is not stored or sent. The phone number reaches Maqsam at the moment
the operator presses Call and only then. When Maqsam asks whether to call a
number on the UAE Do Not Call Registry, only the operator's own click answers
it. An install that never ticks Maqsam Call in the panel never runs anything on
Maqsam.

The Dialler can also log the obvious outcomes of a call the operator placed
with Call: one that rang out, went to voicemail or was refused as DNCR. This
is off until the operator ticks it, in a second box on the options page. When
it is on, that outcome is written to the record through the same controls as
the operator's own press, after a three second countdown the operator can
cancel, and only while the CRM tab has focus. A call that stayed connected
for 12 seconds or more is never logged by itself. A pickup shorter than that
is logged as Voicemail or Unanswered after the same countdown, so the
operator cancels it if somebody spoke. The comment written is the one the
operator's own press would write, so for a B2C lead's first contact that rang
out it also says a WhatsApp was sent, which the operator sends themselves;
Cancel during the countdown stops it.

On a named desk, an email draft's signature carries the desk's logo as an
image hosted at `lh3.googleusercontent.com`, so the CRM's email composer loads
that image when the draft is filled in. Its address is the same for every
draft and carries no lead detail.

No other request is made to any other service.

## Permissions

- `storage` keeps the operator's own working state on their own machine, so a
  page navigation in the CRM does not lose a day of un-exported calls.
- `scripting` lets the extension run its own packaged scripts on WhatsApp Web
  and on Maqsam's web dialer, and only once the operator has allowed that site
  on the options page.
- `https://crm.advplus.ae/*` is the single site the panel runs on. There is no
  wildcard and no other host granted on install.
- `https://web.whatsapp.com/*` and `https://portal.av.maqsam.com/*` are
  optional. Each is asked for only when the operator ticks its box on the
  options page, and is given back when the box is unticked.

## Data retention and deletion

Everything the extension stores is in the browser profile on the operator's
machine. Removing the extension, or clearing its site data from
`chrome://extensions`, deletes all of it. An exported file is the operator's
own file in their downloads folder: removing the extension does not delete it,
and the operator deletes it like any other file of theirs. Logged calls stay
in extension storage until the operator confirms an export was saved; they
are not deleted by age, and removing the extension deletes any that remain.
Nothing is held anywhere else for anyone to delete.

## Selling and sharing

No data is sold. Nothing is sent anywhere except where the operator presses a
control that opens or fills another site, listed above under What leaves the
machine, each in the operator's own account; apart from those, no data is
shared with or transferred to any third party. No data is used for
advertising, credit assessment or lending. No data is used for any purpose
beyond the single purpose of working the lead record in front of the
operator: placing and logging the call and preparing its follow up. No person
other than the operator reads it: none of it is sent to the developer. The
use of this data complies with the Chrome Web Store User Data Policy,
including the Limited Use requirements.

## Changes

If the extension changes what it stores or where anything goes, this page
changes with it.
