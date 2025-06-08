# Proctora — Your Stealth Companion for Proctored Exams & Interviews

Proctora is a desktop & web companion that quietly sits on top of your screen and lets you
consult an AI assistant **without being detected** by proctoring or interview software.
Think of it as a stealth overlay that gives you just-in-time answers, explanations and
resources while keeping you fully compliant with on-screen monitoring.

> **⚠️ Disclaimer**: Proctora is intended for **ethical** use only. Make sure you have the
> right to use third-party assistance in your context. The authors are **not responsible**
> for misuse.

---

## ✨ Key Features

• **Invisible Overlay** – A translucent black panel that can be toggled on/off and moved
anywhere. It stays invisible to screen-share & proctoring apps while being visible to you.

• **AI-Powered Q&A** – Powered by OpenAI/GPT. Ask questions, summarise text or get hints at
any time. Answers appear instantly inside the overlay.

• **Drag-and-Drop Text Capture** – Select any on-screen text, drag it onto the red "drop"
zone and it is sent straight to the AI as context.

• **Token-Based Usage** – Every new user receives **5 000 free tokens**. Purchase extra
tokens directly from the desktop app when you run low.

• **Customisable Prompts** – Tweak the system prompt to change the tone, depth or format of
the AI's answers.

• **Full Keyboard Control** – No mouse? No problem. All actions can be triggered with
discreet keyboard shortcuts (see below).

• **Context Management** – Reset or trim the conversation to avoid token overflows with a
single shortcut.

• **Screenshot & OCR** – Capture any region of your screen and convert it to text for quick question input.

• **Clipboard Paste** – Instantly send whatever is on your clipboard to the AI with a single shortcut.

• **Cross-Platform** – Works on Windows, macOS and major Linux distributions.

---

## 🛠️ How It Works (High-Level)

1. **Desktop Shell** – The Electron-based desktop client launches a frameless, always-on-top
   window with a transparent background.
2. **Stealth Rendering** – The overlay is flagged as _"non-capture"_ using specific window
   attributes, making it invisible to most screen-recording or exam software.
3. **Secure IPC** – Your prompts are encrypted locally and sent to the Proctora backend,
   which proxies requests to the OpenAI API.
4. **AI Response** – Replies are streamed back and rendered line-by-line inside the overlay
   for near real-time feedback.
5. **Local Hotkeys** – A global keyboard listener (working outside app focus) handles all
   shortcuts without stealing focus from the exam/interview window.

---

## 🚀 Getting Started as a User

1. **Download & Install** the Proctora Desktop app from the [releases page](#) _(link
   coming soon)_.
2. **Launch Proctora** – You will start with 5 000 free tokens.
3. **Set Preferences** – Open _Settings_ to adjust overlay opacity, position and AI prompt.
4. **Start Your Exam/Interview** – Keep Proctora running in the background.
5. **Toggle Overlay** – Press **Ctrl + Shift + V** to show/hide the overlay.
6. **Ask a Question** – Press **Ctrl + Shift + H**, type your query, then **Ctrl + Shift + R**
   to send.
7. **Capture On-Screen Text** – Drag text (or an image with OCR enabled) onto the small red
   drop zone in the top-left corner.
8. **Reset Context** – After a question, press **Ctrl + Shift + D** if you want a clean
   slate.

### Default Keyboard Shortcuts

| Action                     | Shortcut          |
| -------------------------- | ----------------- |
| Toggle overlay visibility  | `Ctrl-Shift-V`    |
| Open input box             | `Ctrl-Shift-H`    |
| Send prompt                | `Ctrl-Shift-R`    |
| Screenshot & OCR           | `Ctrl-Shift-S`    |
| Paste clipboard text       | `Ctrl-Shift-C`    |
| Reset conversation context | `Ctrl-Shift-D`    |
| Clear canvas               | `Ctrl-Shift-X`    |
| Scroll chat                | `Ctrl-↑ / Ctrl-↓` |
| Increase overlay opacity   | `Ctrl-Shift-↑`    |
| Decrease overlay opacity   | `Ctrl-Shift-↓`    |
| Quit application           | `Ctrl-Shift-Q`    |

_(All shortcuts can be customised in Settings.)_

---

## 💳 Token System

Proctora uses OpenAI under the hood, so each request consumes tokens. To keep things fair
and sustainable:

1. **Free Tier** – 5 000 tokens on sign-up.
2. **Pay-as-You-Go** – Buy bundles from the _Buy Tokens_.
3. **Usage Meter** – The top bar always shows remaining tokens in real-time.

---

## 🔐 Security & Privacy

• **Local Encryption** – Your token & prompt history are stored encrypted on disk.

• **No Screen Capture** – The overlay uses `setWindowDisplayAffinity` (Windows) /
`NSWindowCollectionBehaviorCanJoinAllSpaces + ignoresMouseEvents` (macOS) so proctoring
tools cannot capture it.

• **GDPR Compliant** – We do not log your prompts or store personal data on our servers.

---

## 📺 Demo

Want to see it in action? Check the **Demo** page of the web client or watch the [YouTube
walkthrough](#).

---

## 🗺️ Roadmap

- [ ] Built-in OCR for images
- [ ] Whisper-powered voice input
- [ ] Automatic citation & source links
- [ ] Audio capture & transcription

---

## 🤝 Contributing

Contributions are welcome! Please open an issue to discuss your idea first. Make sure to
follow the code style enforced by **ESLint + Prettier** and include relevant unit tests.

---

## 📝 License

MIT © 2024 Proctora Team
