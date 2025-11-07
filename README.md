# IJORAS Citation Converter

<div align="center">

![Version](https://img.shields.io/badge/version-2.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Gemini](https://img.shields.io/badge/Powered%20by-Gemini%20AI-orange.svg)

**Professional academic reference formatting tool powered by Google's Gemini AI**

Convert your references to IJORAS (International Journal of Robotics and Automation Systems) style with ease.

[Features](#features) • [Quick Start](#quick-start) • [Usage Guide](#usage-guide) • [Examples](#examples) • [FAQ](#faq) • [Contributing](CONTRIBUTING.md) • [Deployment](DEPLOYMENT.md)

</div>

---

## 🌟 Features

### Core Functionality
- ✨ **AI-Powered Conversion** - Uses Google Gemini 2.0 Flash for intelligent reference formatting
- 📋 **Multiple Reference Types** - Supports journals, conferences, books, patents, theses, and more
- 🎯 **IJORAS Compliant** - Follows official IJORAS style guidelines
- 🔄 **Real-time Processing** - Instant conversion with live feedback

### User Experience
- 🌓 **Dark Mode** - Easy on the eyes with automatic theme switching
- 📊 **Live Statistics** - Track input lines and converted references in real-time
- 📱 **Responsive Design** - Works seamlessly on desktop, tablet, and mobile
- 🎨 **Modern UI** - Clean, professional interface with smooth animations

### Advanced Features
- 🔐 **Secure API Key Storage** - Keys stored locally in browser (localStorage)
- 📤 **Export Options** - Export to TXT or HTML formats
- 📋 **Copy to Clipboard** - One-click copying of formatted references
- 🔔 **Smart Notifications** - Visual feedback for all operations
- 📝 **Example References** - Pre-loaded examples to get started quickly
- ⚡ **Error Handling** - Comprehensive error messages and rate limit detection

---

## 🚀 Quick Start

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, or Edge)
- Internet connection
- Google Gemini API key ([Get one free here](https://aistudio.google.com/app/apikey))

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/lewbei/IJORAS-citation-convertor.git
   cd IJORAS-citation-convertor
   ```

2. **Open the tool**
   - Simply open `index.html` in your web browser
   - No installation or server required!

3. **Enter your API key**
   - Paste your Gemini API key in the input field
   - Click "Save Key" (stored locally in your browser)

4. **Start converting**
   - Paste your references
   - Click "Convert References"
   - Copy or export the formatted output

---

## 📖 Usage Guide

### Step-by-Step Tutorial

#### 1. Get Your API Key
1. Visit [Google AI Studio](https://aistudio.google.com/app/apikey)
2. Sign in with your Google account
3. Create a new API key
4. Copy the key (starts with `AIzaSy...`)

#### 2. Configure the Tool
1. Open `index.html` in your browser
2. Paste your API key in the "Gemini API Key" field
3. Click "💾 Save Key"
4. The key is saved in your browser's local storage

#### 3. Convert References
1. Paste your references in the left panel
2. Click "✨ Convert References"
3. Wait for the AI to process (usually 2-5 seconds)
4. Review the formatted output in the right panel

#### 4. Export Your Results
- **Copy**: Click "📋 Copy to Clipboard"
- **Export TXT**: Click "💾 Export TXT" for plain text
- **Export HTML**: Click "💾 Export HTML" for formatted HTML

### Keyboard Shortcuts

Speed up your workflow with these shortcuts:

| Shortcut | Action |
|----------|--------|
| `Ctrl/⌘ + Enter` | Convert references |
| `Ctrl/⌘ + K` | Clear input |
| `Ctrl/⌘ + L` | Load example references |
| `Ctrl/⌘ + D` | Toggle dark mode |
| `Ctrl/⌘ + Shift + C` | Copy output to clipboard |
| `Ctrl/⌘ + S` | Save API key |
| `F1` | Show all keyboard shortcuts |

**Tip:** Press `F1` anytime to see the complete list of shortcuts!

---

## 📚 Examples

**📖 For comprehensive examples**, see [EXAMPLES.md](EXAMPLES.md) which includes:
- 20+ reference examples covering all major types
- Journals, conferences, books, theses, patents, standards
- Input and expected output formats
- Tips for best results

### Quick Input Examples

#### Journal Article
```
J. Smith, K. Jones, and L. Brown, "Machine Learning Approaches for Pattern Recognition,"
IEEE Transactions on Neural Networks, vol. 30, no. 5, pp. 123-145, May 2020.
DOI: 10.1109/TNN.2020.123456
```

#### Conference Paper
```
A. Johnson and B. Williams, "Deep Learning Models for Image Classification,"
Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition,
pp. 200-210, 2019.
```

#### Book Chapter
```
G. O. Young, "Chapter on Machine Learning," Artificial Intelligence Handbook,
3rd ed., MIT Press, pp. 100-150, 1990.
```

### Output Format

The tool will format these as:

```
[1]	J. Smith, K. Jones and L. Brown, "Machine Learning Approaches for Pattern Recognition,"
	*IEEE Transactions on Neural Networks*, vol. 30, no. 5, pp. 123-145, 2020.
	DOI: https://doi.org/10.1109/TNN.2020.123456

[2]	A. Johnson and B. Williams, "Deep Learning Models for Image Classification,"
	*Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition*,
	pp. 200-210, 2019.

[3]	G. O. Young, "Chapter on Machine Learning," *Artificial Intelligence Handbook*,
	3rd ed., MIT Press, pp. 100-150, 1990.
```

---

## 🎨 Formatting Rules

The tool applies these IJORAS style guidelines:

### General Rules
- **Numbering**: Sequential [1], [2], [3]... with no trailing period
- **Authors**: Initials followed by surname (e.g., J. K. Author)
- **No "et al."**: List all authors in the reference list
- **Titles**: Title case with quotation marks for articles/chapters
- **Italics**: Journal and book names in italics
- **Dates**: Year only (YYYY), no months
- **DOI**: Full URL format: `https://doi.org/...`
- **Alignment**: Tab after reference number for proper alignment

### Reference Type Specific

#### Journals
Format: `"Title," *Journal Name*, vol. X, no. Y, pp. X–Y, Year.`

#### Books
Format: `*Book Title*, edition, Publisher, pp. X–Y, Year.`

#### Conferences
Format: `"Title," *Conference Name*, pp. X–Y, Year.`

#### Patents
Format: `Patent Name, Patent Number, Month Day, Year.`

#### Theses
Format: `"Title," Ph.D. dissertation/M.S. thesis, University, Year.`

---

## 🔧 Technical Details

### Built With
- **HTML5** - Structure
- **CSS3** - Modern styling with CSS Grid and Flexbox
- **Vanilla JavaScript** - No dependencies
- **Google Gemini 2.0 Flash API** - AI-powered conversion

### Browser Support
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Opera 76+

### API Usage
- Uses Gemini 2.0 Flash model
- Free tier: 60 requests per minute
- Rate limiting handled automatically

### Privacy & Security
- ✅ API key stored locally (localStorage)
- ✅ No data sent to third-party servers
- ✅ All processing via official Google API
- ✅ No tracking or analytics
- ✅ Open source - review the code yourself

---

## ❓ FAQ

### Q: Is this free to use?
**A:** Yes! The tool is free. You only need a free Gemini API key from Google.

### Q: Is my API key safe?
**A:** Yes. Your API key is stored only in your browser's local storage and is never sent anywhere except directly to Google's Gemini API.

### Q: How many references can I convert at once?
**A:** There's no hard limit, but we recommend batches of 10-20 references for optimal performance.

### Q: Does it work offline?
**A:** No, an internet connection is required to communicate with the Gemini API.

### Q: What if I get a rate limit error?
**A:** The free tier allows 60 requests per minute. If you hit the limit, wait a minute and try again.

### Q: Can I customize the formatting rules?
**A:** Yes! The prompt is in the JavaScript code. You can modify it to suit your needs.

### Q: What reference formats are supported as input?
**A:** The AI can understand most common citation formats (APA, MLA, Chicago, IEEE, etc.) and convert them to IJORAS style.

### Q: How accurate is the conversion?
**A:** The AI is highly accurate but always review the output. Complex references or unusual formats may need manual adjustment.

---

## 🐛 Troubleshooting

### Common Issues

#### "Invalid API key" error
- Verify your API key starts with `AIzaSy`
- Check for extra spaces or characters
- Generate a new key if needed

#### "API rate limit exceeded"
- Wait 60 seconds before trying again
- Consider upgrading to a paid Gemini plan for higher limits

#### References not converting correctly
- Check input format
- Try one reference at a time to identify problematic entries
- Ensure DOIs are valid URLs

#### Dark mode not working
- Clear browser cache
- Check if your browser supports CSS custom properties

---

## 🚀 Changelog

### Version 2.0 (Current)
- ✨ Complete UI/UX redesign
- 🌓 Dark mode support
- 📊 Live statistics
- 📤 Export to TXT/HTML
- 🔐 Secure API key management
- 📋 Copy to clipboard
- 🔔 Smart notifications
- 📱 Fully responsive design
- ⚡ Enhanced error handling
- 🎨 Modern, professional interface

### Version 1.0
- Basic reference conversion
- Gemini API integration
- Simple HTML interface

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Report Bugs** - Open an issue with details
2. **Suggest Features** - Share your ideas
3. **Submit Pull Requests** - Improve the code
4. **Improve Documentation** - Help others understand the tool

---

## 📄 License

This project is licensed under the MIT License - feel free to use, modify, and distribute.

---

## 👨‍💻 Author

Created by [lewbei](https://github.com/lewbei)

---

## 🙏 Acknowledgments

- Powered by [Google Gemini AI](https://ai.google.dev/)
- Inspired by IJORAS formatting guidelines
- Built for the academic community

---

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/lewbei/IJORAS-citation-convertor/issues)
- **Discussions**: [GitHub Discussions](https://github.com/lewbei/IJORAS-citation-convertor/discussions)
- **Email**: Open an issue for support

---

<div align="center">

**Made with ❤️ for researchers and academics**

[⬆ Back to Top](#ijoras-citation-converter)

</div>
