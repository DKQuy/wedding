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

To add an image or video, put the file in the matching subfolder and add a figure inside `.gallery-grid` in `index.html`. Paths are relative to the repository root. Remove the empty-state paragraph if adding media to an empty gallery.

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