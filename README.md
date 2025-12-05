# 📊 Marp Product Documentation Presentation

A professional, version-control friendly product documentation presentation built with **Marp** (Markdown Presentation Ecosystem).

## 📋 Overview

This project demonstrates how to create maintainable and portable presentation slides using Marp Markdown. The presentation showcases various Marp features essential for technical documentation and product presentations.

**Author:** 24f1002299@ds.study.iitm.ac.in

## ✨ Features

- **Custom Theming**: Embedded CSS for consistent branding with Inter font family and professional color scheme
- **Automatic Page Numbers**: Built-in pagination for easy navigation
- **Background Images**: Support for full-slide background imagery
- **Mathematical Equations**: LaTeX/KaTeX support for algorithmic and mathematical notation
- **Code Syntax Highlighting**: Clean code snippets with proper formatting
- **Machine-Readable Contact**: Email embedded in both content and footer
- **Version Control Friendly**: Pure Markdown source that diffs cleanly in Git

## 📁 Project Structure

```
Q2/
├── README.md          # This file
└── slides.md          # Main presentation source
```

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v14 or higher)
- [Marp CLI](https://github.com/marp-team/marp-cli)

### Installation

```bash
# Install Marp CLI globally
npm install -g @marp-team/marp-cli
```

### Usage

**Preview in browser:**

```bash
marp --preview slides.md
```

**Export to PDF:**

```bash
marp slides.md -o slides.pdf
```

**Export to PowerPoint:**

```bash
marp slides.md -o slides.pptx
```

**Export to HTML:**

```bash
marp slides.md -o slides.html
```

## 📐 Presentation Content

The presentation covers:

1. **Title Slide**: Introduction with contact information
2. **Marp Benefits**: Why use Marp for product documentation
3. **Feature Overview**: List of demonstrated capabilities
4. **Background Image Slide**: Visual demonstration with modern tech imagery
5. **Mathematical Equations**: Master Theorem notation example
6. **Code Snippets**: Python example for parsing product metadata

## 🎨 Customization

The embedded CSS in `slides.md` can be modified to:

- Change color schemes (currently using `#0b5394` blue accent)
- Update fonts (currently using Inter, system-ui fallbacks)
- Adjust layout and spacing
- Add additional custom classes

## 📚 Resources

- [Marp Official Documentation](https://marp.app/)
- [Marp CLI Documentation](https://github.com/marp-team/marp-cli)
- [Marpit Framework](https://marpit.marp.app/)

## 📄 License

This project is created for educational purposes as part of the TDS Graded Assignment 8.

---

_Created with ❤️ using Marp Markdown_
