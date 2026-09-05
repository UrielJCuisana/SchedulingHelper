# Lifeguard Timesheet Maker — GitHub Pages

This project is a fully static browser app. There is no backend and no build step.

## Files to upload

```text
/
├── index.html
└── README.md   (optional; not required by the app)
```

Only `index.html` is required for the site to work.

## Deploy with GitHub Pages

1. Create a GitHub repository.
2. Upload `index.html` to the repository root. You may also upload this README.
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select your branch (usually `main`) and the folder `/ (root)`.
6. Save. GitHub will publish the site at a URL like:
   `https://USERNAME.github.io/REPOSITORY-NAME/`

## How it works

- The user chooses or drags in a `.xlsx` schedule using the browser file picker.
- Excel parsing happens entirely in browser JavaScript.
- Lifeguard filtering, multi-day selection, open-shift handling, and PDF generation all happen client-side.
- Generated PDFs are browser downloads (`Blob` URLs); no upload or server storage is used.
- On supported Chromium browsers, **Save all to a folder** uses the browser File System Access API. If unavailable, normal PDF download buttons still work.

## Browser recommendation

Use a current Microsoft Edge or Google Chrome version. The app uses modern browser APIs for local `.xlsx` decompression.
