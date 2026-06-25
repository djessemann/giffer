# giffer

Dead-simple web app: upload a short video, get a high-quality GIF you can download or save to your phone.

**Live app → https://djessemann.github.io/giffer/**

Everything runs in your browser via [ffmpeg.wasm](https://ffmpegwasm.netlify.app/) — no video is ever uploaded to a server. Conversion uses a two-pass palette (`palettegen` + `paletteuse` with dithering) at 15 fps for clear, smooth output, best for clips of ~10 seconds or less.

## Run locally

It's a static site, but ffmpeg.wasm needs cross-origin isolation, so open it over HTTP rather than `file://`:

```sh
python3 -m http.server 8080
# then visit http://localhost:8080
```
