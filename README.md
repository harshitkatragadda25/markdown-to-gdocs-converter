# Markdown to Google Docs Converter

A Python-based solution that converts markdown meeting notes into beautifully formatted Google Docs with proper styling, hierarchical structure, and interactive checkboxes.

## 🎯 Features

- **Proper Heading Hierarchy**: H1, H2, and H3 styled appropriately
- **Interactive Checkboxes**: Markdown checkboxes converted to Google Docs checkboxes
- **Assignee Highlighting**: @mentions styled in bold blue
- **Nested Bullets**: Maintains proper indentation hierarchy
- **Footer Styling**: Meeting metadata in italic gray
- **Error Handling**: Comprehensive error handling with clear messages

## 🚀 Quick Start

### Prerequisites
- Google Account
- Access to Google Colab

### Setup Instructions

#### Option 1: Run in Google Colab (Recommended)

1. **Open the notebook directly in Colab**
   - Click this badge: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/markdown-to-gdocs-converter/blob/main/markdown_to_gdocs.ipynb)
   - Replace `YOUR_USERNAME` with your GitHub username

2. **Run the notebook**
   - Click **"Runtime"** → **"Run all"**
   - Authenticate with Google when prompted
   - The script will create a new Google Doc automatically

3. **Access Your Document**
   - The notebook will output a direct link to your new Google Doc
   - The document will be created in your Google Drive

#### Option 2: Download and Upload to Colab

1. Download `markdown_to_gdocs.ipynb` from this repository
2. Go to [Google Colab](https://colab.research.google.com/)
3. Click **"File"** → **"Upload notebook"**
4. Upload the downloaded .ipynb file
5. Run all cells

## 📦 Dependencies

All dependencies are automatically installed in the notebook:

google-api-python-client
google-auth-httplib2
google-auth-oauthlib

## 🏗️ Project Structure
markdown-to-gdocs-converter/
│
├── markdown_to_gdocs.ipynb    # Main Colab notebook
├── README.md                   # This file
├── requirements.txt            # Python dependencies
└── sample_output.png          # Screenshot (optional)

## 💻 Code Architecture

### Components

1. **MarkdownParser Class**
   - Parses markdown into structured elements
   - Handles headings, bullets, checkboxes, and text
   - Detects @mentions and nesting levels

2. **GoogleDocsFormatter Class**
   - Creates new Google Docs
   - Applies proper styling (headings, bullets, colors)
   - Manages formatting requests efficiently

3. **Main Function**
   - Orchestrates the conversion process
   - Provides user feedback at each step
   - Handles errors gracefully

## 🎨 Formatting Details

| Markdown Element | Google Docs Style |
|-----------------|-------------------|
| `# Title` | Heading 1 |
| `## Section` | Heading 2 |
| `### Subsection` | Heading 3 |
| `- [ ] Task` | Checkbox bullet |
| `@name` | Bold, blue text |
| Nested bullets | Proper indentation |
| Footer text | Italic, gray |

## 🔧 Customization

To use your own markdown content, modify the `MARKDOWN_CONTENT` variable in the notebook:
```python
MARKDOWN_CONTENT = """
# Your Title
## Your Content
...
"""
```

## 📝 Example Usage

The script converts this markdown:
```markdown
## Action Items
- [ ] @sarah: Finalize Q3 roadmap by Friday
```

Into a Google Doc with:
- ✅ Interactive checkbox
- **@sarah** in bold blue
- Task text in normal formatting

## ⚠️ Troubleshooting

### Authentication Issues
- Make sure you're logged into your Google account
- Clear browser cache and try again
- Check that you've authorized the necessary permissions

### API Errors
- If you hit quota limits, wait a few minutes and try again
- Ensure you have access to Google Docs API

## 🤝 Contributing

Feel free to submit issues or pull requests for improvements!

## 📄 License

MIT License - feel free to use this for your projects

## 👤 Author

**Harshit Katragadda**
- Machine Learning Engineer at UNIFY
- GitHub: [harshitkatragadda25](https://github.com/harshitkatragadda25)

## 🙏 Acknowledgments

- Google Docs API documentation
- Python markdown parsing community

---

**Created as part of a Full Stack Software Engineer Assessment**

**Time taken**: ~30 minutes
