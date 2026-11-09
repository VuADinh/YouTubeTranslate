# YouTube Real-time Subtitle Translator

[中文文档](README_CN.md)

A lightweight browser extension that translates YouTube subtitles in real-time to Chinese or other languages.

## 🎥 Demo Video

<div align="center">
  <a href="https://youtu.be/tbZKdEU6Z9o">
    <img src="https://img.youtube.com/vi/tbZKdEU6Z9o/maxresdefault.jpg" alt="Demo Video" style="width:100%;max-width:800px;">
  </a>
  <p><em>Click to watch the demo video</em></p>
</div>

## ✨ Features

- 🌐 **Real-time Translation** - Automatically detects and translates YouTube subtitles
- 🎯 **Dual Subtitles** - Original and translated subtitles displayed simultaneously
- 🚀 **Zero Latency** - Uses efficient translation API with almost no delay
- 💾 **Smart Caching** - Caches translation results to avoid redundant translations
- 🎨 **Native Styling** - Perfectly integrated into YouTube interface
- 🌍 **Multi-language Support** - Supports translation to 8+ languages

## 📦 Installation

### Chrome / Edge

1. Download the [latest release](https://github.com/orange2ai/youtube-subtitle-translator/releases/latest)
2. Extract the zip file
3. Open your browser and navigate to `chrome://extensions/`
4. Enable "Developer mode" in the top right corner
5. Click "Load unpacked extension"
6. Select the extracted folder
7. Done! The extension icon will appear in your toolbar

### Firefox

1. Download the [latest release](https://github.com/orange2ai/youtube-subtitle-translator/releases/latest)
2. Extract the zip file
3. Open your browser and navigate to `about:debugging#/runtime/this-firefox`
4. Click "Load Temporary Add-on"
5. Select the `manifest.json` file in the extracted folder
6. Done!

## 🎮 Usage

1. **Open a YouTube video**
   - Make sure the video has subtitles (auto-generated or manual)
   - Enable subtitles by clicking the CC button

2. **View translations**
   - Translated subtitles will automatically appear above the original subtitles
   - Both original and translated text are displayed for easy comparison

3. **Adjust settings**
   - Click the extension icon in your browser toolbar
   - Toggle translation on/off
   - Select target language (default: Simplified Chinese)

## ⚙️ Supported Languages

- 🇨🇳 Simplified Chinese
- 🇹🇼 Traditional Chinese
- 🇺🇸 English
- 🇯🇵 Japanese
- 🇰🇷 Korean
- 🇪🇸 Spanish
- 🇫🇷 French
- 🇩🇪 German
- 🇻🇳 Vietnamese

## 🔧 Technical Implementation

- **Translation Engine**: Google Translate API (free)
- **Subtitle Detection**: MutationObserver for real-time DOM monitoring
- **Caching**: JavaScript Map for translation result caching
- **Styling**: Perfectly adapted to YouTube's native subtitle style

## 📝 File Structure

```
youtube-translator-extension/
├── manifest.json       # Extension configuration
├── content.js          # Core translation logic
├── styles.css          # Subtitle styling
├── popup.html          # Settings interface
├── popup.js            # Settings logic
├── background.js       # Background service
├── icons/              # Extension icons
│   ├── icon16.png
│   ├── icon48.png
│   └── icon128.png
└── README.md           # Documentation
```

## 🚀 Advanced Features

### Using Better Translation APIs

You can replace the translation engine in `content.js`:

**DeepL API** (higher quality):
```javascript
const url = 'https://api-free.deepl.com/v2/translate';
// See DeepL documentation for implementation
```

**OpenAI API** (context-aware):
```javascript
const url = 'https://api.openai.com/v1/chat/completions';
// See OpenAI documentation for implementation
```

### Local Translation Model (Offline)

Use Transformers.js to run models in the browser:
```javascript
import { pipeline } from '@xenova/transformers';
const translator = await pipeline('translation', 'Xenova/nllb-200-distilled-600M');
```

## ⚠️ Notes

1. **Subtitles Required**
   - The video must have subtitles (auto-generated or uploaded)
   - The extension cannot work without subtitles

2. **Network Requirements**
   - Requires access to Google Translate API
   - May need proxy configuration in restricted regions

3. **Performance Impact**
   - Translation consumes some network and CPU resources
   - Caching mechanism reduces redundant translations

## 🐛 Troubleshooting

### Translation not showing
1. Check if the video has subtitles
2. Confirm subtitles are enabled (CC button)
3. Refresh the page and try again
4. Check browser console for errors

### Translation delay
1. Check network connection
2. Clear browser cache
3. Consider using a faster translation API

### Styling issues
1. YouTube may have updated its interface
2. CSS selectors may need updating
3. Please submit an issue for feedback

## 📄 License

MIT License

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues and pull requests.

## 📧 Contact

For questions or suggestions, please open an issue on GitHub.

---

**Enjoy barrier-free YouTube viewing!** 🎉

## 🙏 Credits

Developed by orangebot 🍊 with OpenClaw
