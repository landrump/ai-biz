# Dropbox Connection Setup

This document tracks the Dropbox connection approach for Listinglever without
storing credentials in the repository.

## Security note

Do not commit Dropbox app secrets, generated access tokens, refresh tokens, or
OAuth authorization codes to GitHub.

The Dropbox app secret and any generated token should be treated as compromised
if they were pasted into chat or any shared document. Rotate the app secret and
delete any generated token before using Dropbox for production uploads.

## Current status

- Dropbox app exists.
- App key has been provided out-of-band.
- App secret was shared in chat and should be rotated before use.
- Generated access token was referenced but not provided.
- No Dropbox MCP, CLI, API token, or mounted folder is currently configured in
  this agent environment.

## Target folder

Create a Dropbox folder:

```text
/Listinglever
```

Recommended subfolders:

```text
/Listinglever/01_Product_Files
/Listinglever/02_Marketing_Assets
/Listinglever/03_Launch_Checklists
/Listinglever/04_Metrics
/Listinglever/05_Archive
```

## Preferred connection paths

### Option A: Dropbox remote MCP

Use this if Cursor can connect to Dropbox MCP directly.

1. Add Dropbox remote MCP in Cursor or the agent host.
2. Authenticate with the Dropbox account that owns the Listinglever folder.
3. Grant the minimum needed permissions.
4. Tell the agent the working folder path:

```text
/Listinglever
```

After setup, the agent should test:

1. List `/Listinglever`.
2. Upload a small test file.
3. Read or list the uploaded test file.
4. Move the test file to archive or delete it.

### Option B: Dropbox API token as a local secret

Use this only if MCP is not available.

1. Rotate the app secret in Dropbox App Console.
2. Generate a short-lived access token or configure OAuth refresh-token flow.
3. Store credentials outside Git, such as in a local `.env` file or the cloud
   agent secret manager.
4. Never paste the token into a committed file.

Expected local-only variables:

```text
DROPBOX_APP_KEY=
DROPBOX_APP_SECRET=
DROPBOX_ACCESS_TOKEN=
DROPBOX_REFRESH_TOKEN=
DROPBOX_ROOT_FOLDER=/Listinglever
```

These names are documented for local setup only. Values must stay out of GitHub.

## Redirect URI guidance

If using OAuth instead of a generated token, add the redirect URI required by the
chosen tool or local script. Examples may include:

```text
http://localhost:53682/callback
```

or the callback URL provided by the MCP or automation tool.

Only add redirect URIs for tools actually being used.

## Immediate next step

The owner should rotate the Dropbox app secret and confirm which connection path
will be used:

1. Dropbox remote MCP, preferred if available.
2. Dropbox API token stored as a local secret, fallback.

Once a safe authenticated connection exists, the agent can upload Listinglever
review files, product manuscripts, image prompts, and launch trackers directly
to Dropbox.
