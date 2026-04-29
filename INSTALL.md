# Install Codex Social AI Team

Run from the repository root:

```powershell
.\install.ps1
```

Then restart Codex.

Manual install:

```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE\.codex\skills"
Copy-Item ".\skills\*" "$env:USERPROFILE\.codex\skills" -Recurse -Force
```

Then restart Codex and ask:

```text
Use social-media-manager-codex to set up a test client social media workflow.
```
