---
title: "PubMed Abstract Listing Fetcher"
summary: "Designed especially with dissertation preliminary examiners in mind. Turn a plain-text reference list into one continuous HTML page of PubMed-matched abstracts."
tags:
  - Desktop
  - Electron
  - Science
date: '2026-05-13T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  placement: 2
  focal_point: Smart
  caption: 'Image credit: [**Studio Humi**](https://unsplash.com/illustrations/desk-with-laptop-tablet-coffee-and-writing-6dlOgFhHYZ8)'

url_code: 'https://github.com/vljlangen/pubmed-abstract-listing-fetcher'
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
slides: ""
---

**PubMed Abstract Listing Fetcher** is a small **open-source** Electron desktop application by Ville Langén, which helps you turn a plain-text bibliography into a **single continuous HTML page** of PubMed abstracts—useful when you are drafting, reviewing, or annotating a manuscript and want the abstract text beside each matched reference.

### The Problem

When you already have a numbered reference list (for example Vancouver-style, one reference per line), pulling the matching abstracts from PubMed by hand is slow and repetitive. You might want:

- One readable document that follows the order of **your** list
- A quick way to **skim** or archive abstract text next to each entry
- Outputs you can share or file away (HTML, PDF, plain text) without touching your manuscript’s project folder until you choose to

### The Solution

**[On GitHub](https://github.com/vljlangen/pubmed-abstract-listing-fetcher),** the project is available in two forms:

- **Desktop app:** use the **graphical** app described on this page.
- **Command line:** run it with Node.js (**node pubmed_abstracts.js**—see **For Linux (and command-line users)** below).

In the app, you paste references or load a **.txt** file, run **Get abstracts & save ZIP**, watch **terminal-style progress**, and when the run finishes you pick where to save a ZIP bundle. Work is performed under the operating system’s **temp** directory until you confirm a save path—nothing is written into your manuscript folders or elsewhere unless you choose to save it there.

### Use Cases

Suited for:

- **Dissertation preliminary examiners** and other reviewers who want a compact abstract listing aligned to a reference list
- **Students and researchers** assembling reading notes from a bibliography
- **Anyone** who prefers a **local-first** workflow: the app runs on your machine; you decide where exports live

It is **not** marketed for regulated clinical decisions, legal filings, or guaranteed completeness of PubMed matches—always verify critical citations in the primary literature.

### Why PubMed Abstract Listing Fetcher?

- **Order-preserving**: Your list drives the document, not a separate search session
- **Explicit saves**: Temp working files and a clear save dialog, so you are not surprised by files scattered through a project tree
- **Practical bundle**: HTML for reading, PDF for sharing or printing, TXT for grep-friendly archives

Turn a static reference list into a browsable abstract companion—on your own computer, at your own pace.

### Key Features

- **Plain-text input**: Paste into the app or load a **.txt** file. For how each line must look, see **Reference list format** below.
- **Sample list**: Optional control to download a minimal **example references.txt** you can edit and replace.
- **Progress feedback**: Terminal-style log while each line is resolved and abstracts are fetched.
- **ZIP export**: **pubmed_abstracts.html**, **pubmed_abstracts.pdf** (printed from the HTML via bundled Chromium), and **pubmed_abstracts.txt** (plain text derived from the HTML).

### How to Use (desktop app)

1. **Open the app** and paste your reference list, or use the file picker to load a **.txt** file
2. Optionally download the **example references.txt** to see the expected shape of each line
3. Click **Get abstracts & save ZIP** and wait until progress completes
4. When prompted, choose where to save the ZIP; extract it to get HTML, PDF, and TXT

## Reference list format (references.txt)

- Use **one reference per line**; empty lines are skipped.
- Leading list numbers (for example **1. …**, **2. …**) are fine—you do **not** need to remove them before running this program; they are stripped internally when searching PubMed.
- References should look **Vancouver-like** (typical numbered biomedical lists):
  - authors first (often with *et al.*)
  - then the article title
  - then journal, year, DOI, and similar details
- The fetcher needs a clear boundary **between the author block and the start of the title**. Use either a **full stop (period)** or a **colon** there, for example:
  - *…Lastname AB, Other CD. Title starts here…*
  - *…Lastname AB, et al: Title starts here…*
- Other colons in the line, such as in volume/issue **14(1):179** or in **doi:…**, are ignored when choosing that split.

See the sample [**references.txt**](https://github.com/vljlangen/pubmed-abstract-listing-fetcher/blob/main/references.txt) in the project files on GitHub for real lines.

### Download Options

Ready-built installers are on **GitHub Releases** (latest):

- **Windows (x64)**: portable **.exe** under Assets on the [latest release](https://github.com/vljlangen/pubmed-abstract-listing-fetcher/releases/latest). If SmartScreen warns about an unknown publisher, you may need **More info → Run anyway**
- **macOS**: **.dmg** under Assets—pick **arm64** for Apple Silicon (M1/M2/M3/…) or the **Intel/x64** build for older Macs. Drag the app to **Applications**; if Gatekeeper blocks the first launch, try **Right-click → Open** once

### For Linux (and command-line users)

On Linux you can skip the Electron UI and run the engine directly with **Node.js 20 or newer**:

1. Download or clone the [project from GitHub](https://github.com/vljlangen/pubmed-abstract-listing-fetcher) and **cd** into it
2. Place your references in **references.txt** in the working directory (or pass explicit input/output paths—see the README on GitHub)
3. Run:

```bash
node pubmed_abstracts.js
```

Defaults write **pubmed_abstracts.html** in the **current working directory** (this path is for the script, not the desktop app’s temp-and-save flow). Optionally set **NCBI_API_KEY** and **NCBI_CONTACT_EMAIL** in the environment for higher rate limits and polite identification with NCBI.

### Technical Details

- **Built with**: Electron (desktop UI), Chromium for PDF generation, and the same JavaScript matching/fetch pipeline as **pubmed_abstracts.js**
- **License**: MIT (full text on GitHub and in-app via the LICENSE modal)
- **Data handling**: Fetches use NCBI E-utilities; behavior and availability follow NCBI’s policies and limits

### Development & Support

The project is open source. Bug reports, feature ideas, and pull requests belong on **[GitHub](https://github.com/vljlangen/pubmed-abstract-listing-fetcher)**. **Questions or issues?** Use the **Issues** tab there.
