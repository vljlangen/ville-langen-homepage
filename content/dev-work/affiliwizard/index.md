---
title: "AffiliWizard: Author-Affiliation Formatting Tool"
summary: "A GUI application that transforms Excel author-affiliation data into properly formatted academic paper listings with automatic numbering and multiple export formats."
tags:
  - Science
date: '2024-12-01T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  focal_point: Smart

url_code: 'https://github.com/vljlangen/affiliwizard'
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
slides: ""
---

**AffiliWizard v1.0.0** is a lightweight GUI tool created by Ville Langén, designed to solve a common problem in academic writing: formatting author-affiliation lists with proper numbering and structure.

### The Problem

When writing academic papers with multiple authors from different institutions, creating a properly formatted author-affiliation list can be tedious and error-prone. You often need to:

- Number affiliations sequentially
- Match authors to their respective institutions
- Format everything consistently
- Export to various formats for different journals

### The Solution

AffiliWizard streamlines this process with a simple, intuitive interface that transforms your Excel data into professionally formatted author lists.

### Key Features

- **Simple Copy-Paste Interface**: Copy data directly from Excel spreadsheets
- **Automatic Numbering**: Intelligently assigns superscript numbers to affiliations
- **Multiple Export Formats**: Save as .docx, .html, or plain text
- **Cross-Platform**: Available for macOS, Windows, and web browsers
- **No Installation Required**: Use the online version instantly

### How to Use

1. **Prepare Your Data**: Organize your author-affiliation data in Excel with columns for:
   - Author Name (including degrees/titles)
   - Affiliation 1
   - Affiliation 2 (optional)
   - Additional affiliations as needed

2. **Copy and Paste**: Select and copy your data from Excel, then paste it into AffiliWizard's text box

3. **Export**: Choose your preferred format (.docx, HTML, or Plain Text) and save

### Input Format Example

```
Author Name          | Affiliation 1              | Affiliation 2
John Doe, MD         | Bogus Institute, CA, USA   | Example Institute, TS, USA
Jane Doe, MD         | Sample University, TX, USA |
```

### Sample Output (HTML Format)

**Authors:**
John Doe, MD<sup>1,2</sup>, Jane Doe, MD<sup>3</sup>

**Affiliations:**
1. Bogus Institute, CA, USA
2. Example Institute, TS, USA  
3. Sample University, TX, USA

### Download Options

**Desktop Applications:**
- **macOS Apple Silicon**: [AffiliWizard-macOS-arm64.dmg](https://github.com/vljlangen/affiliwizard/releases)
- **Windows**: [AffiliWizard.exe](https://github.com/vljlangen/affiliwizard/releases)

**Online Version:**
For immediate use without downloads: [https://affiliwizard.netlify.app/](https://affiliwizard.netlify.app/)

### For Linux Users

Linux users can build AffiliWizard from source:

1. **Install Python 3** (recommended 3.8+)
2. **Set up virtual environment**:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```
3. **Run directly**:
   ```bash
   python AffiliWizard.py
   ```

### Technical Details

- **Built with**: Python and tkinter for the GUI
- **License**: MIT License - free to use and modify
- **Dependencies**: Minimal Python libraries for maximum compatibility
- **File Size**: Lightweight application under 10MB

### Use Cases

Perfect for:
- **Academic researchers** preparing manuscripts
- **Journal editors** formatting submission requirements  
- **Conference organizers** creating program listings
- **Grant applications** with multiple institutional collaborators

### Development & Support

AffiliWizard is actively maintained and open source. Contributions, bug reports, and feature requests are welcome on the [GitHub repository](https://github.com/vljlangen/affiliwizard).

**Questions or issues?** Feel free to reach out through the project's GitHub issues page.

### Why AffiliWizard?

In academic writing, the little details matter. AffiliWizard ensures your author-affiliation formatting is:
- **Consistent** across all your publications
- **Professional** and journal-ready  
- **Error-free** with automatic numbering
- **Time-saving** with streamlined workflow

Transform your author-affiliation formatting from a tedious task into a one-click solution with AffiliWizard! 