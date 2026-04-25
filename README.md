# Texarkana Future Leaders — Member Landing Pages

**Maintained by:** txkfutureleaders@gmail.com  
**Live site:** `https://[yourusername].github.io/[repo-name]/`  
**Purpose:** Individual landing pages for TFL members, accessible via QR code on their badge.

---

## How This Works

Each TFL member has their own webpage that looks like:
```
https://[yourusername].github.io/[repo-name]/tfl-01.html
```

That URL is encoded in the QR code printed on their badge. When someone scans the badge, they land on that member's personal page — which shows their photo, the TFL intro video, and a link to the interest form with that member's referral ID pre-filled automatically.

The NFC tap on the badge is a **separate system** and is not managed here. This repository handles QR code destinations only.

---

## Repository Structure

```
your-repo/
│
├── README.md               ← This file
├── index.html              ← TFL main landing page (future)
├── tfl-01.html             ← Member page (first member)
├── tfl-02.html             ← Member page (second member)
├── tfl-03.html             ← (continue pattern)
│
└── photos/
    ├── tfl-01.jpg          ← Member photo (matches page number)
    ├── tfl-02.jpg
    └── tfl-03.jpg
```

**Naming rules:**
- Member IDs are assigned in order: TFL-01, TFL-02, TFL-03...
- Page filename matches the ID: `tfl-01.html`
- Photo filename matches the ID: `tfl-01.jpg`
- Never reuse an ID, even if a member leaves the program

---

## Adding a New Member — Step by Step

This is the full process every time a new member joins TFL.

### Step 1 — Get the member's photo ready
- Photo should be a clear headshot or portrait
- Crop it so the face is centered and visible
- Rename the file to match their ID: `tfl-05.jpg`
- Recommended size: at least 800px wide, JPG or PNG format

### Step 2 — Upload the photo to GitHub
1. Go to your repository on GitHub.com
2. Click the **`photos`** folder
3. Click **Add file → Upload files**
4. Drag in the member's photo (`tfl-05.jpg`)
5. Scroll down and click **Commit changes**

### Step 3 — Create the member's page
1. Go back to the root of your repository (click the repo name at the top)
2. Click **Add file → Create new file**
3. Name the file: `tfl-05.html`
4. Open the template file (`tfl-template.html`) — copy everything inside it
5. Paste it into the new file editor on GitHub

### Step 4 — Make the three replacements
Find and replace these three placeholders in the file:

| Placeholder | Replace with | Example |
|---|---|---|
| `PHOTO_PLACEHOLDER.jpg` | `photos/tfl-05.jpg` | Member's photo path |
| `FIRST` and `LAST` | Member's actual name | `JORDAN` / `SMITH` |
| `VIDEO_ID_HERE` | TFL YouTube video ID | `dQw4w9WgXcQ` |
| `NOTION_FORM_URL_HERE` | Pre-filled form URL | See Section below |
| `TFL Member` (role line) | Keep as-is for now | Update when paths are earned |

> **Note on the name:** The name displays in two lines — put the first name where it says `FIRST` and the last name where it says `LAST`. If the member only goes by one name, delete the `<br><span>LAST</span>` line entirely.

### Step 5 — Build the pre-filled Notion form URL
Every member gets a personalized version of the interest form link that automatically includes their referral ID. No one filling out the form has to do anything extra — it just records who referred them.

Take the base Notion form URL:
```
https://[your-notion-form-link-here]
```

Add the member's referral ID to the end:
```
https://[your-notion-form-link-here]?referral=TFL-05
```

Paste that full URL where it says `NOTION_FORM_URL_HERE` in the file.

### Step 6 — Commit (save) the file
1. Scroll down below the editor
2. Click **Commit new file**
3. The page is now live at: `https://[yourusername].github.io/[repo-name]/tfl-05.html`

### Step 7 — Test it
1. Open the URL in a browser on your phone
2. Confirm the photo loads, the video plays, and the form button works
3. If the photo doesn't load, double-check the filename spelling exactly matches

### Step 8 — Generate and print the QR code
- The QR code for this member should encode: `https://[yourusername].github.io/[repo-name]/tfl-05.html`
- Generate it using your existing QR code tool
- Print and add to their badge

---

## Getting the YouTube Video ID

You only need to do this once — it's the same video ID on every member's page.

1. Open your TFL intro video on YouTube
2. Click **Share → Copy Link**
3. The link looks like: `https://youtu.be/dQw4w9WgXcQ`
4. The video ID is the 11-character code at the end: `dQw4w9WgXcQ`
5. In each HTML file, the embed URL should read: `https://www.youtube.com/embed/dQw4w9WgXcQ`

---

## Updating an Existing Member's Page

To update a photo, name, or role after a member earns a new path level:

1. Go to the repository on GitHub.com
2. Click the member's `.html` file (e.g. `tfl-03.html`)
3. Click the **pencil icon** (Edit this file) in the top right
4. Make your changes
5. Scroll down and click **Commit changes**

Changes go live within 1–2 minutes.

---

## If a Member Leaves the Program

- **Do not delete their page or reuse their ID**
- Edit their page file and remove the photo (replace with a blank or TFL logo image)
- The page can remain live as an inactive placeholder
- Their ID number is retired permanently

---

## Member ID Log

Use this table to track assigned IDs. Update it every time someone joins.

| ID | Status | Date Joined | Notes |
|---|---|---|---|
| TFL-01 | Active | | |
| TFL-02 | Active | | |
| TFL-03 | Active | | |

---

## Troubleshooting

**Page says 404 (not found)**  
→ Make sure GitHub Pages is enabled: Settings → Pages → Source: main branch  
→ Double-check the filename is exactly `tfl-01.html` (all lowercase)

**Photo isn't showing**  
→ Check that the photo file is in the `photos/` folder  
→ Check that the filename in the HTML matches exactly (case-sensitive)

**Video isn't playing**  
→ Confirm the YouTube video is set to Public, not Private or Unlisted  
→ Check that the video ID in the embed URL is correct

**Form link isn't working**  
→ Open the Notion form URL in a browser first to confirm it's still active  
→ Check that `?referral=TFL-XX` is appended with no spaces

---

## Contact & Access

**Repository owner:** txkfutureleaders@gmail.com  
**Program contact:** TFL@groundfloorcollective.org | 909-441-1768  
**Instagram/Facebook:** @texarkanafutureleaders

*TFL operates under Ground Floor Collective and is not affiliated with or endorsed by any named institution.*
