# Wedding Gallery

Store static gallery media here, then commit it to the repository. Files are served directly by the website; there is no browser upload.

```text
media/
|-- gallery/
|   |-- images/   # Wedding photos
|   |-- videos/   # Wedding videos
|   `-- README.md
`-- qr/            # Bank QR images, separate from the gallery
```

The main `index.html` coverflow uses optimized JPEG copies in `optimized/`; keep the original full-resolution photos in `images/`. Add each optimized image path to the `album` list in `CONFIG` in `index.html`. The current copies are resized to a maximum dimension of 1800px to keep the page quick to load.

`index2.html` has a separate `.gallery-grid` gallery. To add an image or video there, put it in the matching subfolder and add a figure inside `.gallery-grid` in `index2.html`. Paths are relative to the repository root.

```html
<figure class="gallery-item">
  <img src="media/gallery/images/anh-cuoi-01.jpg" alt="Cô dâu và chú rể">
  <figcaption class="gallery-caption">Khoảnh khắc của chúng mình</figcaption>
</figure>

<figure class="gallery-item">
  <video controls preload="metadata" playsinline>
    <source src="media/gallery/videos/video-cuoi-01.mp4" type="video/mp4">
  </video>
  <figcaption class="gallery-caption">Video cưới</figcaption>
</figure>
```