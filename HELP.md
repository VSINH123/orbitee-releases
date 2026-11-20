# Orbity help

Step-by-step help for opening and setting up Orbity. Pick your computer, and follow the steps in order. Stuck? Jump to [Getting help](#getting-help).

- [Mac: opening Orbity](#mac-opening-orbity)
- [Windows: opening Orbity](#windows-opening-orbity)
- [Setting up a brain (Mac and Windows)](#setting-up-a-brain-mac-and-windows)
- [Getting help](#getting-help)

---

## Mac: opening Orbity

### 1. Install it
1. Open the `.dmg` file you downloaded (double-click it).
2. Drag **Orbity** onto the **Applications** folder in the same window.
3. When it has finished copying, **eject the .dmg**: in Finder, click the little eject button next to "Orbity" in the left sidebar. You can then delete the `.dmg` file.

### 2. Open it the first time
Open **Applications** and double-click **Orbity**. Your Mac may say it is blocked because it comes from outside the App Store. That's expected. To allow it:
1. Click **Done** (or **OK**) on the message.
2. Open **System Settings** (the grey gear icon in the Dock or Apple menu) and click **Privacy & Security** in the sidebar.
3. Scroll down until you see a message about "Orbity" being blocked, and click **Open Anyway**. **Do this within an hour of trying to open it**, or the button disappears. If it's gone, just try to open Orbity again to bring it back.
4. Type your Mac password if it asks, then click **Open**.

You only have to do this once.

### 3. If it says "damaged" or "permission denied"
Don't worry, the app is fine. This is how macOS treats apps that didn't come from the App Store. We'll fix it with two short commands.

1. Open **Terminal**: press **Command + Space**, type **Terminal**, and press **Enter**.
2. Copy this line, paste it into Terminal (**Command + V**), and press **Enter**:

       sudo xattr -cr /Applications/Orbity.app

3. Terminal asks for your **Mac password**. **You won't see anything as you type it, not even dots. That's normal.** Type it and press **Enter**.
4. Now do the same with this second line:

       sudo codesign --force --deep --sign - /Applications/Orbity.app

   (Enter your password again if it asks.)
5. Open **Orbity** from **Applications** again.

If Terminal says **"Operation not permitted"**, your Mac is stopping Terminal from changing apps. Open **System Settings > Privacy & Security > App Management**, switch **Terminal** on, quit Terminal, and run the two lines again.

Still not working? See [Getting help](#getting-help).

### 4. Allow Orbity to look at your screen (optional)
Orbity only looks at your screen when you press the 👀 button or the whiteboard's "Use my screen" button. Your Mac needs your permission for that, once:
1. Open **System Settings > Privacy & Security**.
2. Click **Screen & System Audio Recording**. (On older Macs it's called **Screen Recording**.)
3. Switch **Orbity** on. If Orbity isn't in the list, press the 👀 button once in Orbity and look again.
4. **Quit Orbity and open it again.** (Click the Orbity icon at the top of your screen, then **Quit Orbity**.)

### 5. Taking a screenshot of a problem
If something goes wrong, a picture helps us a lot:
1. Press **Command + Shift + 4**. Your pointer becomes a small cross.
2. Drag across the part of the screen you want to show, and let go.
3. The picture is saved on your **Desktop** as "Screenshot ….png".
4. Attach it to an email to **orbitypets@gmail.com**.

(To capture your whole screen instead, press **Command + Shift + 3**.)

---

## Windows: opening Orbity

### "Windows protected your PC"
This blue message appears because Orbity is new, and Windows hasn't seen it before. It is safe to continue:
1. Click **More info**.
2. Click **Run anyway**.

### There's no "Run anyway" button
Then your PC has **Smart App Control** turned on, and it blocks apps like this one completely. The easy fix is to get Orbity from the **Microsoft Store** instead. (Store link: coming soon.)

### Taking a screenshot of a problem
Press the **Windows key + Shift + S**, drag across the part of the screen you want to show, then open an email to **orbitypets@gmail.com** and press **Ctrl + V** to paste the picture in.

---

## Setting up a brain (Mac and Windows)

Orbity needs a "brain" to chat with you. Pick **one** of these.

### Option A: private and free (runs on your own computer)
Your chats never leave your computer. It needs a few gigabytes of space and is slower than the online option.

1. Go to **ollama.com**, download **Ollama** and install it. Open it once.
2. Open a terminal:
   - **Mac:** press **Command + Space**, type **Terminal**, press **Enter**.
   - **Windows:** click Start, type **Terminal**, press **Enter**.
3. Type this and press **Enter**. It downloads the brain (one time only, it takes a few minutes):

       ollama pull gemma3

   On an **older or slower computer**, use the smaller one instead:

       ollama pull gemma3:1b

4. In Orbity, open **Customize** (click your pet, then the ⚙️ button, or use the Orbity icon at the top or bottom of your screen), go to **Brain**, and press **Test brain**.

### Option B: easiest and free (uses Google's Gemini over the internet)
Quick to set up, and fast. **It has usage limits** (if it says it's busy, wait a minute), and **Google may use messages sent with a free key to improve its products**, so don't send anything private.

1. Go to **aistudio.google.com** and sign in with a Google account.
2. Click **Get API key**, then **Create API key**. **Don't add a payment card.** The free key doesn't need one.
3. Copy the key (a long line of letters and numbers).
4. In Orbity open **Customize**, and under Plan pick **Premium**.
5. Under **Brain** choose **Another AI**. Next to **Service**, choose **Gemini**.
6. Paste your key into the **API key** box, and press **Test brain**. When it says it works, press **Save**.

Keep your key private, like a password.

---

## Getting help

Email **orbitypets@gmail.com** and attach a **screenshot of the problem** (see the screenshot steps for [Mac](#5-taking-a-screenshot-of-a-problem) or [Windows](#taking-a-screenshot-of-a-problem)). Tell us:
- whether you have a Mac or Windows, and your Mac's macOS version if you know it;
- what you were trying to do;
- what you saw.

Please don't send your chats unless you're comfortable with us reading them.

[Back to the README](README.md)
