# Language Translation Tool

A simple web-based tool to translate text between 100+ languages. Built with plain HTML, CSS, and JavaScript — no installation, no backend server, and no API key required.

## Features

- Translate text between 100+ languages
- Auto-detect source language
- Swap source and target languages with one click
- Copy translated text to clipboard
- Listen to original and translated text (text-to-speech)
- Live character count
- Works entirely in the browser

## How to Run

1. Download `language-translation-tool.html`
2. Double-click the file (or right-click → Open with → your browser)
3. Start translating — no setup needed

That's it. There is nothing to install and no server to start.

## How to Use

1. Choose the **From** language (or leave it on "Detect language")
2. Choose the **To** language
3. Type or paste text into the **Input** box
4. Click **Translate**
5. The result appears in the **Output** box
   - Click **Copy** to copy the translation
   - Click **Listen** to hear the input or output read aloud
   - Click the swap icon to reverse the From/To languages

Keyboard shortcut: press `Ctrl + Enter` (or `Cmd + Enter` on Mac) while typing to translate instantly.

## How It Works

| Part | Technology |
|---|---|
| Interface | HTML + CSS (dark theme, responsive) |
| Logic | Vanilla JavaScript (no frameworks) |
| Translation | Free public translation endpoint (`translate.googleapis.com`) |
| Text-to-speech | Browser's built-in `SpeechSynthesis` API |
| Copy to clipboard | Browser's built-in `Clipboard` API |

When you click **Translate**, the page sends your text to a free, key-free translation endpoint using JavaScript's `fetch()`, then displays the returned translation. Multi-line text is translated line by line so paragraph breaks are preserved.

## Project Structure

Everything lives in a single file:

```
language-translation-tool.html   → HTML structure + CSS styling + JavaScript logic
```

This was kept as one file on purpose, so it's easy to copy, share, and run without any build step.

## Notes & Limitations

- This uses an **unofficial free endpoint**, not the paid Google Cloud Translation API. It's reliable for personal and academic projects but is not meant for high-traffic production use.
- An active internet connection is required, since translation happens over the network.
- Text-to-speech voice availability depends on the languages installed in your browser/OS.
- If translation requests start failing under heavy use, switching to an official paid API (Google Cloud Translate, Microsoft Translator) or a self-hosted option (LibreTranslate) is the next step.

## Possible Improvements

- Save recent translations / history
- Detect and display which language was auto-detected
- Add a dark/light theme toggle
- Add file upload for translating documents

## Author

Built as part of an internship project on practical, no-dependency web tools.
