# QR Studio

A modern, privacy-friendly QR code generator and scanner that runs entirely in your browser.

Generate customizable QR codes for websites, text, Wi-Fi networks, email addresses, phone numbers, SMS messages, and contacts — or scan existing QR codes using your camera or an image file.

**Live demo:** https://lkristof.github.io/qr-studio/

## Features

### QR Code Generator

Generate QR codes for multiple content types:

* **Website** — URLs with automatic `https://` handling
* **Text** — plain text content
* **Wi-Fi** — network name, password, encryption type, and hidden networks
* **Email** — recipient, subject, and message
* **Phone** — phone numbers
* **SMS** — recipient and pre-filled message
* **Contact** — vCard contact information

QR codes are updated with a live preview while editing.

### Customization

Customize the appearance and output of generated QR codes:

* Multiple built-in color presets
* Custom foreground and background colors
* Adjustable QR code size
* Configurable error-correction level
* Live preview
* Resettable styling options

### Export

Generated QR codes can be:

* Downloaded as **PNG**
* Downloaded as **SVG**
* Copied directly to the clipboard as an image
* Copied as their encoded value

### QR Code Scanner

Scan QR codes using:

* Your device's **camera**
* An **image file** from your device

On supported devices, camera zoom controls are also available.

### Local History

QR Studio keeps a history of both:

* Generated QR codes
* Scanned QR codes

History is stored locally in your browser using `localStorage` and can be cleared at any time.

### Privacy

QR Studio is designed to work entirely on the client side.

QR code generation and scanning happen directly in your browser. Generated content and scan history are not sent to a backend server.

For scanned links, the application only allows supported protocols such as:

* `https`
* `http`
* `mailto`
* `tel`

### Additional Features

* Responsive design for desktop and mobile
* Automatic light and dark mode
* Hungarian and English interface
* Progressive Web App manifest
* Keyboard-accessible controls
* Camera scanning with HTTPS or localhost
* No build process required
* No backend required

## Tech Stack

QR Studio is a lightweight static web application built with:

* HTML5
* CSS3
* Vanilla JavaScript
* [QRCode.js](https://github.com/davidshimjs/qrcodejs)
* [html5-qrcode](https://github.com/mebjas/html5-qrcode)

The required QR libraries are included locally in the repository, so the application does not depend on a CDN at runtime.

## Getting Started

### Clone the repository

```bash
git clone https://github.com/lkristof/qr-studio.git
cd qr-studio
```

### Run locally

Since QR Studio is a static web application, you can serve it with any local HTTP server.

For example, using Python:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

> Camera access requires a secure context. Browsers generally allow camera access on HTTPS websites and on `localhost`.

You can also deploy the project directly to any static hosting provider such as GitHub Pages.

## Project Structure

```text
qr-studio/
├── assets/
│   ├── images/
│   └── js/
├── index.html
├── site.webmanifest
└── LICENSE
```

The application is intentionally kept simple: the interface, styling, and application logic are contained in the static frontend, while third-party QR libraries and assets are stored locally.

## Deployment

No compilation or build step is required.

Upload the repository to a static web host or enable GitHub Pages for the repository.

The public version of QR Studio is available at:

https://lkristof.github.io/qr-studio/

## Contributing

Contributions, bug reports, and suggestions are welcome.

If you would like to improve QR Studio:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Commit your changes.
5. Open a pull request.

## License

This project is licensed under the **MIT License**.

See the [LICENSE](./LICENSE) file for details.
