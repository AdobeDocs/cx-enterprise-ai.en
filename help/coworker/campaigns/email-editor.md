---
description: description.
title: Understand the email editor
---
# Understand the email editor {#email-editor}

The email editor lets you refine an AI-generated email directly on the campaign board. Edit the subject line and preheader, format text and images inline, or swap in a different template. <!-- It's an inline editor over the email's actual HTML, not a drag-and-drop block builder. -->

>[!PREREQUISITES]
>
>Create a campaign with a generated email.

## What this feature does

Clicking an email card on the campaign board opens the email editor as a side panel. From there, the user can edit the subject and preheader (with AI-suggested alternatives), click into the email body to select and format text or images, switch between AI-generated variants, swap the HTML template, check email-client compatibility, and send a test email to their own inbox. Changes save automatically, and past versions can be reviewed and restored.

### Key behaviors

- Clicking any text or image in the email body selects it and reveals a floating formatting toolbar.
- Text formatting options: Bold, Italic, Underline, font, and font size.
- Image options: Replace, Delete, Link, Edit with Express, Generate image (AI), Upload from computer.
- Image uploads are capped at 10 MB; images over roughly 3 MB are automatically compressed, with a quality note recommending images under 3 MB.
- Subject and preheader fields each have a "Smart suggestions" option for AI-generated alternatives.
- Changes autosave (on blur, and shortly after formatting actions) — a status indicator shows Unsaved changes, Saving…, Saved, Autosaved, or Unable to save (with a Retry option).
- Undo/redo is available for the current editing session.
- Past saved versions can be previewed and restored from a version history panel.
- If multiple AI-generated variants exist, the user can switch between them from a thumbnail panel.
- The email's HTML template can be swapped using "Switch HTML Template."
- "Send test email" sends a real preview to the user's own inbox using sample data; it doesn't affect campaign reporting.
- An email-client compatibility check is available in some environments, covering Gmail, Outlook, Apple Mail, Yahoo Mail, Samsung Email, and Thunderbird. [NEEDS INPUT — this is behind a feature flag; confirm whether it's enabled for the target audience before documenting it as generally available]

## How to access

1. Open the desired campaign and click Open editor in the email card.

SCREENSHOT

1. Edit the **Subject** and **Preheader** fields directly, or click **Smart suggestions** next to either for AI-generated alternatives.
1. Click into the email body to select a text block or image, then use the floating toolbar that appears to format the text or manage the image.
1. Use **Switch HTML Template** to replace the email body with a different template.
1. Use **Send test email**, enter a recipient address, and click **Send** to email a live preview to that address.
1. Use the version history icon to preview and restore an earlier saved version.
1. Changes save automatically — no manual save step is required.

### Input fields / parameters

| Field | Description | Required? |
| --- | --- | --- |
| Subject | The email's subject line | No (can be left blank; not currently enforced) |
| Preheader | The preview text shown next to the subject in an inbox | No |
| Recipient email address | Where to send a test email | Yes, for Send test email |

## UI callouts

> **Tech writer note**: Screenshots needed for the following:

- [ ] The email editor side panel (subject/preheader fields plus email body)
- [ ] The floating toolbar for text selection
- [ ] The floating toolbar for image selection
- [ ] The AI variant thumbnail panel
- [ ] The version history panel
- [ ] The "Switch HTML Template" dialog
- [ ] The Send test email dialog
- [ ] The email-client compatibility checker (if enabled in the target environment)

## What this feature does not do

- It isn't a drag-and-drop block builder — there's no block library, and content blocks can't be added, removed, or reordered; editing happens directly on the existing email HTML.
- It doesn't currently support inserting personalization/merge tags.
- It doesn't provide an alt-text field for images.
- It doesn't enforce a subject line, preheader, or other content-level checks before an email is considered "ready" — the only pre-launch checks are campaign-level (sending setup, a test email sent, a real audience), not checks on the email content itself.
- Desktop/mobile preview toggling isn't available in the standard campaign email editing view. [NEEDS INPUT to confirm scope]
- [NEEDS INPUT — to confirm with engineer: whether the editor becomes fully read-only (not just the sender field) once a campaign has been activated/launched.]
