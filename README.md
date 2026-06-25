# giffer

Dead-simple web app: upload a short video, get a high-quality GIF you can download or save to your phone.

**Live app → https://djessemann.github.io/giffer/**

Everything runs in your browser — no video is ever uploaded to a server. Frames are captured from the video via canvas and encoded with [gifenc](https://github.com/mattdesl/gifenc), each frame quantized to an optimal 256-color palette at 15 fps for clear, smooth output. Best for clips of ~10 seconds or less. No plugins, no WebAssembly download, works on mobile.

## Run locally

It's a static site. Open it over HTTP rather than `file://` (so the CDN module loads):

```sh
python3 -m http.server 8080
# then visit http://localhost:8080
```
