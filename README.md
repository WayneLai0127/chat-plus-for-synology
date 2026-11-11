# Chat+ for Synology

**A keyboard-first Mac app for Synology Chat.** Same chat, same NAS, same sign-in. A cleaner interface, real shortcuts and link previews on top.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="images/hero-dark.png">
  <img alt="Chat+ for Synology: conversation with sections, link chips, a highlighted code block and a Jira hover card" src="images/hero-light.png">
</picture>

Chat+ opens the Synology Chat web app from your own NAS and draws a new interface over it. Sign-in, messages, encryption and notifications stay with Synology; Chat+ only changes how they look and how fast you get around.

### See it in action

![Demo: ⌘T jumps to a conversation, ⌃Tab goes back, a Jira hover card, a shared HTML report opening in place, and the ticket picker](images/demo.gif)

> Chat+ is an independent project. It is not made, endorsed or supported by Synology Inc. Synology and Synology Chat are trademarks of Synology Inc.

## Highlights

**A calmer interface**
- Message bubbles or a compact layout, a resizable sidebar, light and dark themes
- Opens straight into the chat, without a white flash, in your Mac's language
- Your own sidebar sections (drag conversations in, fold to unread), and unread conversations at the top if you turn that on in Synology Chat; drafts that survive restarts
- Bot posts made of `Key: value` lines become cards; runs of bot posts fold together
- A threads inbox across all conversations
- Mentions show each person's picture and name; in the message box a mention is one piece, removed with one Backspace
- See who's typing, with their pictures above the message box
- Code blocks are syntax-highlighted: name the language (```` ```js ````, `sql`, `py`, `bash`…) or let Chat+ guess, and mark lines with ```` ```js {2-3} ````

**Keyboard first**
- ⌘T jumps to any conversation, unread first · ⌃Tab cycles recent ones
- ⌥↑ / ⌥↓ the conversation above or below · ⌥⇧↑ / ⌥⇧↓ the next one with something unread
- ⌃⌥Space brings Chat+ forward from any app, with the switcher open (change or turn it off in your profile card)
- ⌘⇧T opens the threads you follow; arrows and Enter take you through them
- ⌘F searches this conversation, ⇧⌘F everywhere (`from:` `in:` `has:`) · ⌘/ lists every shortcut
- ⌘⇧J your downloads · ⌘⇧A your Synology apps

**Links and previews**
- Jira, Confluence, GitHub, Bitbucket, Google Docs and more become tidy chips; long URLs are shortened
- Shared HTML pages, PDFs, CSV tables, audio and video open in place
- GIFs: search GIPHY from the GIF button or `/gif`, and pasted GIPHY links play in the message
- With your own Atlassian token (optional): live ticket titles and status, hover cards, whole tickets and Confluence pages in the side panel (hover a Jira or Confluence chip and click its preview button: the description or page, comments and images, next to the chat), a ticket picker (type `PROJ-` to pick one of your issues, or paste an issue link: it becomes a card in your message, sent as the full link), and the tickets mentioned in each conversation

**Getting things done**
- Schedule a message for later, typing the time (`fri 10:00`, `tomorrow`, `30m`) or tabbing through the date, and set reminders on any message
- Slash commands: `/schedule`, `/poll` (people vote with one click), `/collapse` for long conversations, `/purpose`, `/invite`, `/leave`, plus Synology's own
- ⌘I shows a conversation's files and links (searchable, by type) and its members, invites people, and lets you leave a channel
- Right-click a message for quick reactions and every message action
- Downloads go straight to your Downloads folder, with progress in the header and a list to pause, open or show in Finder
- The Apps button opens Synology Drive, Calendar and your other DSM apps, like the classic App Launcher

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="images/0.7.0/slash-dark.png">
  <img alt="Typing / lists Synology's commands and the ones Chat+ adds, such as /schedule, /poll and /collapse" src="images/0.7.0/slash-light.png">
</picture>

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
- Your DSM sign-in is kept encrypted on disk with a key in your macOS Keychain.
- The optional Atlassian token is encrypted the same way and sent only to the Atlassian site you saved it for.
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

- **Notifications.** The Dock badge, bounce and sound work out of the box. Allow Chat+ in **System Settings → Notifications** and new messages show as regular notifications with the Chat+ icon; clicking one opens that message. If macOS doesn't show them, turn on pop-up banners in your profile card: they then come through Script Editor, and clicking one still opens the message.
- **Your data stays local.** Sections, drafts, reminders and link settings are kept on your Mac. Nothing is sent anywhere except your NAS, and Atlassian if you add a token.
- **Updates.** Once a day Chat+ asks GitHub whether a newer release exists (it fetches release info only; nothing about you is sent). When there is one, it offers to open the download page; install it by replacing the app, and your settings and sign-in are kept. Use **Check for Updates…** in the app menu any time, or untick **Check for Updates Automatically**.
- **Switching back.** ⌘⇧U toggles Synology's classic interface at any time.

## License

[MIT](LICENSE)
