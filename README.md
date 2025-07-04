# MediaWiki to Obsidian Vault Converter 🧭

This script converts a MediaWiki XML dump into a clean, tag-driven Obsidian Markdown vault — including images, categories, infoboxes, and structured YAML frontmatter.

🗂️ If you want to organize your Obsidian vault into folders based on tags, check out my [Obsidian Organizer](https://github.com/mak-kirkland/obsidian-organizer).

## ✨ Features

- ✅ Converts MediaWiki pages to Obsidian-compatible Markdown
- 🏷️ Extracts and normalizes categories as `tags`
- 📦 Converts infoboxes into YAML frontmatter (including images)
- 🔧 Infers tags from infobox types using noun inflection
- 🖼️ Downloads and embeds images as `![[images/Filename]]`
- 🔗 Converts internal links to Obsidian `[[Wikilinks]]`
- 📚 Automatically generates tag-based index files under `_indexes/`
- 🐢 Supports optional Pandoc for better Markdown rendering
- 🔍 Verbose mode for detailed output and easier troubleshooting

---

## 📦 Requirements

- Python 3.8+
- [`pandoc`](https://pandoc.org/) (optional, but recommended for better Markdown conversion)

Install Python dependencies with:

```bash
pip install -r requirements.txt
```

## 🚀 Usage

```bash
python convert.py INPUT_XML [OUTPUT_DIR] [--skip-redirects] [--verbose]
```

| Argument           | Description                                         |
| ------------------ | --------------------------------------------------- |
| `INPUT_XML`        | Path to your MediaWiki XML dump                     |
| `OUTPUT_DIR`       | Optional output folder (default: `obsidian_vault/`) |
| `--skip-redirects` | Ignore redirect pages                               |
| `--verbose`        | Enable verbose logging (disables progress bar)      |


## 🗂️ Output Structure

```text
obsidian_vault/
├── _indexes/
│   ├── _people.md
│   ├── _locations.md
│   └── ...
├── images/
│   ├── Example.jpg
│   └── ...
├── Page_Title_1.md
├── Page_Title_2.md
└── ...
```

## 👤 Author

Created by Michael Kirkland
