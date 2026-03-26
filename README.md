# QR Code Generator

A simple, elegant QR code generator with a black and white interface. Generate QR codes from URLs with customizable appearance options.

## Features

- **Clean Interface**: Minimalist black and white design with automatic dark mode support
- **URL Input**: Generate QR codes for any URL
- **Customizable Appearance**:
  - Adjustable size (128px - 512px)
  - Error correction levels (Low, Medium, Quartile, High - up to 30%)
  - Three QR code styles: Square, Dots, Rounded
  - Independent corner square styles: Square, Dot, Extra Rounded
  - Independent corner dot styles: Square, Dot
  - Customizable foreground and background colors
- **Auto-Generate**: QR code updates automatically as you type or change options
- **URL Persistence**: Settings are saved in the URL hash for easy sharing
- **Download**: Save generated QR codes as PNG images
- **Plain JavaScript**: No framework dependencies, minimal external libraries
- **Responsive**: Works on desktop and mobile devices

## Usage

1. Enter a URL in the input field (must start with `http://` or `https://`)
2. (Optional) Adjust size, style, error correction level, and colors
3. The QR code auto-generates as you type and change settings
4. Click "Generate QR Code" to manually regenerate, or "Clear" to reset
5. Click "Download QR Code" to save the image
6. Share the page URL with others to share your QR code settings

## Deploying to GitHub Pages

### Option 1: Using the GitHub Web Interface

1. Create a new repository on GitHub
2. Upload the `index.html` file to the repository
3. Go to repository Settings → Pages
4. Under "Source", select the branch (usually `main`) and root folder
5. Click Save
6. Your site will be available at `https://yourusername.github.io/repository-name/`

### Option 2: Using Git Command Line

```bash
# Initialize git repository
git init

# Add files
git add index.html README.md

# Commit
git commit -m "Initial commit: QR code generator"

# Add remote (replace with your repository URL)
git remote add origin https://github.com/yourusername/qr-code-gen.git

# Push to GitHub
git branch -M main
git push -u origin main
```

Then enable GitHub Pages in your repository settings as described in Option 1.

## Technical Details

- **QR Code Library**: Uses [qr-code-styling](https://github.com/kozakdenys/qr-code-styling) for advanced styling support
- **No Build Process**: Single HTML file with embedded CSS and JavaScript
- **Browser Compatibility**: Works in all modern browsers that support Canvas API and URLSearchParams
- **URL Parameters**: Settings are stored in URL hash (e.g., `#url=...&size=256&style=dots`)

## QR Code Styles

- **Square**: Classic QR code with square modules (default)
- **Dots**: Modern circular dot pattern
- **Rounded**: Square modules with rounded corners
- **Extra Rounded**: More aggressive rounded corners for a smoother look
- **Classy**: Vertical lines with smooth curves
- **Classy Rounded**: Classy style with additional rounding

## Corner Customization

QR codes have three large position markers (finder patterns) in the corners. You can customize these separately:

- **Corner Square**: The outer square frame of the position markers
  - Square, Dot, or Extra Rounded
- **Corner Dot**: The inner square/dot within each position marker
  - Square or Dot

Mix and match main patterns with corner styles for unique designs!

## Error Correction Levels

- **Low (7%)**: Can recover up to 7% of data
- **Medium (15%)**: Can recover up to 15% of data (default)
- **Quartile (25%)**: Can recover up to 25% of data
- **High (30%)**: Can recover up to 30% of data

Higher error correction levels make the QR code more resilient to damage but increase its complexity.

## License

Free to use and modify.
