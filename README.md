# Instagram Follow Checker

A lightweight, privacy-first web tool that analyses your Instagram data export and tells you exactly who isn't following you back, who your one-sided fans are, and who you're mutuals with.

No login. No server. Everything runs entirely in your browser.

---

## Features

- **Not following back** — see everyone you follow who doesn't follow you back
- **Fans** — see everyone who follows you but you don't follow back
- **Mutual followers** — see everyone you and your followers share a connection with
- **Live search** — filter any list by username instantly
- **Stats dashboard** — follower count, following count, not-back count, and fan count at a glance
- **Copy list** — copy any list to your clipboard in one tap
- **Step-by-step guide** — built-in instructions for exporting your Instagram data
- **100% private** — your data never leaves your device

---

## How to Use

### Step 1 — Export your Instagram data

1. Open Instagram and go to your **profile**
2. Tap the **☰ menu** → Settings and privacy
3. Tap **Accounts Center** → Your information and permissions
4. Tap **Export your information** → Create export
5. Choose **Export to device** and enter your email
6. Under **Customize information**, open the **Connections** tab and select only **Followers and following**
7. Set **Date range** to **All time**
8. Set **Format** to **JSON**
9. Tap **Start export** and confirm with your password
10. Wait for the email from Instagram, then download the `.zip` file

### Step 2 — Upload and analyze

1. Open `instagram-follow-checker.html` in your browser
2. Tap the upload zone and select the `.zip` file you downloaded
3. Tap **Analyze account**
4. Browse the results across the three tabs

---

## Important: Understanding "All Time" Data

This tool uses the **All time** date range when exporting from Instagram. This gives you the complete historical record of everyone who has ever followed you and everyone you have ever followed.

However, Instagram's export is **not a live snapshot.** It is a **log of follow events** — meaning it records when someone followed you or when you followed someone, but it **never records unfollows.**

This means:

- The export may include people you followed years ago and have since unfollowed
- The export may include people who followed you and then unfollowed you
- The tool has no way to detect these cases since unfollow events are simply not present in the data

**The best way to verify accuracy** is to compare the follower and following counts shown by the tool against the numbers on your actual Instagram profile. If they roughly match, your results are reliable.

---

## Privacy

This tool is entirely client-side. Your Instagram data is:

- Never uploaded to any server
- Never stored in any database
- Never shared with any third party
- Processed only in your browser's memory and discarded when you close the tab

---

## Limitations

| Limitation | Reason |
|---|---|
| Results may not perfectly match your current follow state | Instagram's export logs follow events but never records unfollows |
| Only works with JSON format exports | HTML format exports have a different structure |
| Requires a `.zip` file | Instagram bundles the JSON files inside a ZIP archive |
| No Instagram login or real-time sync | Instagram's API is restricted and not available to regular users |

---

## Tech Stack

- Vanilla HTML, CSS, and JavaScript — no frameworks
- [JSZip](https://stuk.github.io/jszip/) for reading the `.zip` file in the browser
- [Outfit](https://fonts.google.com/specimen/Outfit) and [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) from Google Fonts

---


