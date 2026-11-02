# Chat+ for Synology

**A keyboard-first Mac app for Synology Chat.** Same chat, same NAS, same sign-in. A cleaner interface, real shortcuts and link previews on top.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="images/hero-dark.png">
  <img alt="Chat+ for Synology: conversation with sections, a bot card, link chips and a Jira hover card" src="images/hero-light.png">
</picture>

Chat+ opens the Synology Chat web app from your own NAS and draws a new interface over it. Sign-in, messages, encryption and notifications stay with Synology; Chat+ only changes how they look and how fast you get around.

> Chat+ is an independent project. It is not made, endorsed or supported by Synology Inc. Synology and Synology Chat are trademarks of Synology Inc.

## Highlights

**A calmer interface**
- Message bubbles, a resizable sidebar, light and dark themes
- Your own sidebar sections (drag conversations in, fold to unread), drafts that survive restarts
- Bot posts made of `Key: value` lines become cards; runs of bot posts fold together
- A threads inbox across all conversations

**Keyboard first**
- ⌘T jumps to any conversation, unread first · ⌃Tab cycles recent ones
- ⌥↑ / ⌥↓ the conversation above or below · ⌥⇧↑ / ⌥⇧↓ the next one with something unread
- ⌘F searches this conversation, ⇧⌘F everywhere (`from:` `in:` `has:`) · ⌘/ lists every shortcut

**Links and previews**
- Jira, Confluence, GitHub, Bitbucket, Google Docs and more become tidy chips; long URLs are shortened
- Shared HTML pages, PDFs, CSV tables, audio and video open in place
- With your own Atlassian token (optional): live ticket titles and status, hover cards, a ticket picker (type `PROJ-` to pick one of your issues), and the tickets mentioned in each conversation

**Getting things done**
- Schedule a message for later, set reminders on any message, slash commands as in Synology's own client

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="images/switcher-dark.png">
  <img alt="The ⌘T switcher filtering conversations as you type" src="images/switcher-light.png">
</picture>

## How it works, and why it's safe

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="images/how-dark.png">
  <img alt="Chat+ runs inside the official Synology Chat web app, which talks only to your NAS" src="images/how-light.png">
</picture>

- The window only ever shows your NAS. Other links open in your browser.
- You sign in on DSM's own page; Chat+ doesn't read or store your password.
- Server and web-app updates from Synology reach Chat+ automatically.
- The optional Atlassian token is encrypted with the macOS Keychain and sent only to your `*.atlassian.net`.
- Shared HTML pages open in a sandbox with no access to your session.

## Install

1. Download `Chat-Plus-for-Synology-<version>-universal.dmg` from [Releases](../../releases).
2. Optional: check it against `SHA256SUMS.txt` from the same release:
   ```bash
   shasum -a 256 Chat-Plus-for-Synology-*-universal.dmg
   ```
3. Open the disk image and drag **Chat+ for Synology** to Applications.
4. The app isn't notarized by Apple yet, so the first time macOS blocks it: open **System Settings → Privacy & Security** and click **Open Anyway** (or right-click the app → Open).
5. Enter your Chat address, for example `https://nas.example.com/chat/` or `https://example.synology.me:5001/chat/`, then sign in as usual. You can change it later from the app menu.

**Requirements:** macOS 12 or later (Apple silicon or Intel), and a Synology NAS running Synology Chat Server that your Mac can reach.

## Good to know

- **Notifications.** The Dock badge, bounce and sound work out of the box. Pop-up banners can be turned on in your profile card; without an Apple Developer signature macOS shows them through Script Editor, and clicking one still opens the message.
- **Your data stays local.** Sections, drafts, reminders and link settings are kept on your Mac. Nothing is sent anywhere except your NAS, and Atlassian if you add a token.
- **Switching back.** ⌘⇧U toggles Synology's classic interface at any time.

## License

[MIT](LICENSE)
