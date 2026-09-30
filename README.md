# KABBO-PAGE approvals

This public repository contains the installation-ID allowlist used by KABBO-PAGE.

## Approving an installation

1. When the app says approval is pending, use **Copy ID** and send that ID to the repository owner.
2. The owner adds the ID as a new line in [`approved_ids.txt`](./approved_ids.txt) and commits the change.
3. The user selects **Check again** in the app or closes and reopens it.

Each installation gets a random ID that is persisted in the user's local app-data directory. The list is checked over HTTPS on each startup and when **Check again** is pressed. If the list cannot be reached, the app stays locked. Removing an ID revokes it on the next check.

This is a basic client-side allowlist, not a tamper-proof license system. Do not put Telegram tokens, chat IDs, account details, or other secrets in this public repository; only installation IDs belong in `approved_ids.txt`.
