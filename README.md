# StegoVault-Web
StegoVault by enrali.nl

Client-side zero-knowledge decryptor for StegoVault images and ZIP archives (PNG, JPG, BMP, ZIP).

## Features & Supported Parameters

### 1. Direct URL Loading (`?file=` or `?url=`)
Load an image or zip file automatically when the page opens:
```text
https://<your-site>/?file=https://example.com/vault.zip
https://<your-site>/?url=https://example.com/image.png&name=my-test.png
```

### 2. Base64 URL Fragment (`#data=` or `#zip=`)
Directly pass base64-encoded zip or image data without hosting the file on a server (fragment `#` avoids HTTP 414 length limits):
```text
https://<your-site>/#data=<base64-string>&name=test.zip
```

### 3. Drag & Drop and Clipboard
- Drag any `.zip`, `.png`, `.jpg`, or `.bmp` file directly onto the container.
- Paste an image or file from the clipboard using `Ctrl+V`.

### 4. Window PostMessage
External apps / webviews can pass files programmatically:
```javascript
window.postMessage({ file: blob, name: 'stego.zip' }, '*');
```

