# Fembot Keep-Alive — Chrome Extension

A lightweight Chrome extension that keeps the Fembot Discord bot online by pinging its server every 4 minutes.

---

## How It Works

After you're done installing the extension, paste this link into the **Server URL** field: `https://fembot-IAmReddie.replit.app`
That's it! Now as long as you or someone else has their browser open, the bot will stay online! 
Thank you for helping!

---

## How It Works

When you toggle the extension on, it runs a background process that sends a small request to the bot's server URL at regular intervals. This prevents the hosting server from going to sleep due to inactivity, keeping the bot online and responsive in your Discord server — even when no one is actively using it.

- Pings the server every **4 minutes**
- Runs silently in the background while Chrome is open
- Shows real-time status (Online / Idle / Unreachable) in the popup
- Remembers your settings between browser sessions

---

## Is It Safe?

Yes. Here's why:

- **No data is collected.** The extension only sends a basic request to the URL you provide — nothing else.
- **No permissions to your Discord.** The extension has no access to your Discord account, messages, or servers.
- **No external servers.** It communicates only with the URL you enter — nothing is sent anywhere else.
- **Open source.** Every line of code is visible in this repo. You can read exactly what it does before installing it.
- **No login required.** You don't need to sign in to anything.

The only permissions it requests are:
- `storage` — to remember the server URL and toggle state
- `alarms` — to schedule the ping every 4 minutes
- `host_permissions: <all_urls>` — to be allowed to reach the server URL you enter

---

## How to Install the Extension

Chrome does not allow installing extensions from a zip file directly. Follow these steps:

### Step 1 — Download and unpack

1. Download `fembot-extension.zip`
2. Right-click the zip file and select **Extract All** (Windows) or double-click it (Mac)
3. This creates a folder called `fembot-extension` — keep it somewhere permanent (e.g. your Documents folder)

### Step 2 — Load in Chrome

1. Open Chrome and go to: `chrome://extensions`
2. Enable **Developer mode** using the toggle in the top-right corner
3. Click **Load unpacked**
4. Select the `fembot-extension` folder you extracted in Step 1

The extension will now appear in your Chrome toolbar.

### Step 3 — Configure it

1. Click the extension icon in your toolbar
2. Paste the bot's server URL into the **Server URL** field `https://fembot-IAmReddie.replit.app`
3. Toggle **Keep bot alive** on
4. The status will change to **Online** once the first ping succeeds

> **Note:** The extension only works while Chrome is open. For the bot to stay online 24/7, the server itself must be deployed and always running.

---

## Troubleshooting

| Status | Meaning |
|---|---|
| Online | Server responded successfully |
| Server error | Server is reachable but returned an error |
| Unreachable | Could not connect to the server URL |
| Idle | Extension is toggled off |

If you see **Unreachable**, double-check that the URL is correct and includes `https://`.
