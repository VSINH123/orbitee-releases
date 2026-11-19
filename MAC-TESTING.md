# Orbity: Mac testing checklist

Thanks for helping test Orbity on a Mac! This takes about 10 minutes. For each line, note whether it works, doesn't work, or looks odd. Also note your Mac type (Apple Silicon or Intel) and your macOS version, and send your notes to whoever asked you to test, or email them to orbitypets@gmail.com.

## Install
1. Download the `.dmg` from the [latest release](https://github.com/VSINH123/orbitee-releases/releases/latest) (under **Assets**).
2. Open the DMG and drag **Orbity** into **Applications**.
3. Try to open Orbity. macOS will refuse the first time because the app isn't from the App Store. Then:
   - Open **System Settings > Privacy & Security**, scroll down and click **Open Anyway** (it appears for about an hour after you try to open the app). Confirm with your password.
   - If macOS says the app is **damaged**, open Terminal and run `xattr -dr com.apple.quarantine /Applications/Orbity.app`, then open it again.
   - Note which of these you needed.

## Checks
- [ ] A pet appears on screen. There is **no Orbity icon in the Dock**.
- [ ] A small dog icon is in the **menu bar** (top right), sharp and not blurry or oversized. Clicking it shows a menu that starts with "Orbity".
- [ ] Click the pet, type a message and press Enter. (The free brain needs Ollama; without it you'll get a friendly message explaining that. That's fine. See the [README](README.md) to set it up.)
- [ ] Drag the pet to another spot, and to a second monitor if you have one. It stays on top of other windows, including a full-screen app.
- [ ] **Cmd+Shift+Space** sends the pet away and brings it back.
- [ ] Copy some text, then press **Cmd+Alt+Space**. The pet offers to explain it.
- [ ] The tooltip on the 👋 button says **Cmd**, not Ctrl.
- [ ] Open the whiteboard (📝). The hint says **Cmd+Ctrl+Shift+4**, then **Cmd+V**. Try it: snip part of your screen, click the whiteboard, press Cmd+V. The picture appears. Cmd+C and Cmd+V also work in the text box.
- [ ] Press 👀 (or "Use my screen" on the whiteboard) **before** allowing Screen Recording. You should get a friendly message explaining how to allow it, and System Settings should open. Switch Orbity on under **Screen & System Audio Recording**, quit and reopen Orbity, and try again. The screenshot should now work.
- [ ] Customize (⚙️): change the pet's name and look. Quit from the menu bar ("Quit Orbity") and reopen. Your changes are still there.
- [ ] In the menu bar menu, **Privacy policy** opens a web page and **Report a problem** opens a new email.
- [ ] Menu bar menu, "Start when I log in": tick it, then restart your Mac or log out and in. Orbity starts.
- [ ] Play fetch and tug of war once each. The pet runs across the screen and nothing gets stuck.
- [ ] Type "remind me to stretch in 1 minute". A notification appears (allow notifications if asked).

## Good to know
- On a Mac, Orbity does not install updates by itself. When a new version exists, you'll get a "New version available" notification that opens the download page. If you are testing an older version, you may see this.
