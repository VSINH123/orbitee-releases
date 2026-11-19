# Orbity

Orbity is a little pet that lives on top of your screen, floats above your other windows and answers your questions. Pick a dog, cat, bunny, fox or bear, give it a name and a personality, play games with it, and ask it for help with homework, reminders and study timers. It works on Windows and Mac.

Orbity is AI, so now and then an answer can be wrong. It needs an AI "brain" to chat: a free one that runs on your own computer, or an optional smarter one you connect with your own account (see below).

## Download

| System | Get it here |
|---|---|
| **Windows (recommended)** | Microsoft Store: link coming soon |
| **Windows (installer)** | [Orbity-Setup.exe on the latest release](../../releases/latest) |
| **Mac (Apple Silicon and Intel)** | [Orbity-universal.dmg on the latest release](../../releases/latest) |

On the release page, open **Assets** and pick the file for your system.

### Windows: "Windows protected your PC"
Because the installer is new and not yet signed, Windows may warn you. Click **More info**, then **Run anyway**.

There's no "Run anyway" button? Your PC has **Smart App Control** turned on, which blocks unsigned apps. Get Orbity from the Microsoft Store instead.

### Mac: "can't be opened"
1. Open the DMG and drag **Orbity** into **Applications**.
2. Try to open Orbity. macOS will refuse the first time.
3. Open **System Settings > Privacy & Security**, scroll down and click **Open Anyway**. (The button shows up for about an hour after you try to open the app.)
4. If macOS says the app is **damaged**, open Terminal and run this, then open Orbity again:

       xattr -dr com.apple.quarantine /Applications/Orbity.app

## Set up the free brain (once)

The free brain is a small AI model that runs on your own computer through a free program called Ollama. It's private and works without internet, but it's slower than the big online AIs.

1. Install **Ollama** from [ollama.com](https://ollama.com) and open it.
2. Open a terminal (Windows: search for "Terminal"; Mac: open "Terminal") and run:

       ollama pull gemma3

   It's a few gigabytes, one time only. On an older or slower computer, use the smaller one instead: `ollama pull gemma3:1b`
3. In Orbity, open **Customize** (the ⚙️ in the chat, or the tray / menu bar icon), go to **Brain**, and press **Test brain**.

## Optional: a smarter brain with your own API key

In **Customize**, choose **Premium**, pick a brain, paste your key, press **Test brain**, then **Save**:

- **Claude:** a key from [platform.claude.com](https://platform.claude.com)
- **ChatGPT:** a key from [platform.openai.com](https://platform.openai.com/api-keys)
- **Gemini:** choose "Another AI", then Gemini, with a key from [aistudio.google.com/apikey](https://aistudio.google.com/apikey) (it has a free tier with limits)

These services may charge you. Your key is stored encrypted on your computer and is only sent to the service you chose. See the [privacy policy](PRIVACY.md).

## Looking at your screen (Mac: allow Screen Recording)

The 👀 button and the whiteboard's "Use my screen" button take **one screenshot, only when you press them**. On a Mac you need to allow this once:

1. Open **System Settings > Privacy & Security > Screen & System Audio Recording** (called **Screen Recording** on older versions of macOS).
2. Switch **Orbity** on.
3. **Quit and reopen Orbity.**

Tip for the whiteboard: you can also snip part of your screen yourself (Windows: **Win+Shift+S**; Mac: **Cmd+Ctrl+Shift+4**) and paste it with **Ctrl+V** / **Cmd+V**.

## Updates

- **Microsoft Store version:** the Store updates it for you.
- **Windows installer from GitHub:** Orbity checks for new versions, downloads them quietly and installs them when you quit.
- **Mac:** Orbity shows a "New version available" notification that opens the [releases page](../../releases/latest). Download the new DMG and drag it over the old Orbity in Applications.

## Troubleshooting

- **My pet doesn't answer.** Make sure Ollama is running (look for its icon near the clock or in the menu bar, or open it again), and that you ran `ollama pull gemma3`. Then open Customize > Brain > **Test brain**. On an older computer try `ollama pull gemma3:1b` and type `gemma3:1b` in the Free model box.
- **I can't see my pet.** Click the Orbity icon near the clock (Windows) or in the menu bar (Mac) and choose **Summon**, or press **Ctrl+Shift+Space** (Mac: **Cmd+Shift+Space**).
- **The screenshot button doesn't work on a Mac.** See "Looking at your screen" above.
- **An answer was wrong or not suitable.** Please tell us: choose **Report a problem** from the tray / menu bar icon, or email **orbitypets@gmail.com**. You choose what to include in the email, and it's private.

## Uninstall

- **Windows:** Settings > Apps > Installed apps > Orbity > Uninstall. This works for both the Store and installer versions. The installer version keeps your pet's settings in `%APPDATA%\pip-desktop-pet`; delete that folder too if you want everything gone.
- **Mac:** quit Orbity, then drag it from Applications to the Trash. To remove your pet's settings, delete `~/Library/Application Support/pip-desktop-pet`.

## More

- [Privacy policy](PRIVACY.md)
- [Mac testing checklist](MAC-TESTING.md) (for people helping test on a Mac)
- Questions, problems or reports about a reply: orbitypets@gmail.com
- General bug reports and ideas can also go on the [GitHub issues page](../../issues/new) (that page is public, so don't put chats or personal details there)
