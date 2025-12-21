# Backup Mozilla Profiles



## Some key files:



### Essential Files to Back Up (Minimal Set for Core Functionality)


| File/Folder                  | Size Impact | What It Restores                                                                 | Notes |
|------------------------------|-------------|----------------------------------------------------------------------------------|-------|
| **logins.json** + **key4.db** | Small      | Saved passwords and login credentials                                            | Required together. |
| **places.sqlite**            | Medium     | Bookmarks, browsing/download history, favicons                                   | Core for saved URLs/bookmarks. |
| **prefs.js** (and **user.js** if you have it) | Small | All custom settings/preferences (homepage, privacy, UI tweaks, many extension settings) | Main file for personalization. |
| **extensions** folder (or **extensions.json**) | Small-Medium | Installed extensions/add-ons (the .xpi files or references)                      | You'll reinstall extensions if missing, but this preserves them. Extension data often in storage (skip for size). |
| **bookmarkbackups** folder   | Small      | Automatic bookmark backups (JSON files)                                          | Redundant if you have places.sqlite, but useful fallback. |
| **cookies.sqlite**           | Small-Medium | Cookies, including session/persistent cookies for staying logged in to websites (often bypasses repeated 2FA) | Great for keeping active sessions after restore. Usually small but very useful. |
| **search.json.mozlz4**       | Small      | Custom search engines                                                            | Optional but nice. |
| **containers.json**          | Small      | Multi-Account Containers data (if you use it)                                    | Optional. |
| **cert9.db** (and **cert_override.txt** if present) | Small | Custom security certificates/exceptions                                          | If you have site exceptions. |


### Files/Folders You Can Safely Skip

- **cache** / **cache2** folder — Browser cache (images, pages); can be gigabytes; fully regenerates.
- **storage** folder — Site-specific data (localStorage, IndexedDB for web apps/extensions); often huge; sites re-save data as needed.
- **startupCache** — Temporary startup files; regenerates.
- **thumbnails** folder (if present) — New Tab page thumbnails; safe to skip.
- **sessionstore-backups** / **sessionstore.jsonlz4** — Open tabs/sessions; skip unless you need exact session restore.
- **minidumps** / **Crash Reports** — Crash data; not needed.
- Any **shader-cache** or temporary folders.

