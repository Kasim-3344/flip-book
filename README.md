# PDF Flipbook Viewer

Frontend-only React + TypeScript + Vite project with a reusable PDF flipbook module powered by `pdfjs-dist`.

## Run locally

```bash
npm install
npm run dev
```

## Place your PDF

Add your document to `public/pdfs/`.

Example:

```text
public/pdfs/sample.pdf
```

## Demo entry point

The app renders a demo viewer from `src/pages/FlipbookDemo.tsx`.

The reusable component lives in `src/components/flipbook/FlipbookViewer.tsx` and accepts:

```tsx
<FlipbookViewer
  pdfUrl="/pdfs/sample.pdf"
  title="Sample Flipbook"
  options={{
    showSidebar: true,
    showZoom: true,
    showFullscreen: true,
    showSoundToggle: true,
    showPageJump: true,
  }}
/>
```

## Notes

- PDF loading is local and static only.
- No backend, upload flow, auth, or storage integration is included.
- The PDF.js worker is configured for Vite builds inside `usePdfLoader`.
