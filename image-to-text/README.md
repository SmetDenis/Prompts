# Image-to-Text Prompts

Optical character recognition and image analysis prompts for extracting, analyzing, and processing visual content. These prompts handle various image types from screenshots to scientific documents with high precision.

## Available Prompts

- [image-analyzer.md](image-analyzer.md) - Image Analyzer: Generates structured descriptions of images including objects, text, context, and visual elements
- [ocr-assistant.md](ocr-assistant.md) - OCR Assistant: High-precision conversion of scientific and technical images to GitHub Flavored Markdown
- [ocr-translator.md](ocr-translator.md) - OCR Translator: Language detection and translation of OCR-extracted text with formatting preservation

## Recommended Parameters

Most prompts suggest:
```yaml
temperature: 0.2       # Low creativity for accurate text extraction and analysis
reasoning_effort: "high"   # Careful handling of OCR errors and complex visual elements
```
