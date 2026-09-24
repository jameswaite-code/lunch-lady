# LunchLady.io

A northern dinner lady in your browser. Give the webcam your best face for five seconds and she sizes you up (barnet altitude, hooter heft, peeper wattage, clobber volume and more), then tells you what to have for your dinner at a real restaurant near you.

Everything runs in the browser. Nothing is uploaded or saved.

## Run it

Camera, microphone and location need a secure context, so serve it from localhost (or HTTPS):

```bash
python3 -m http.server 8792
```

Then open http://localhost:8792.

## How it works

- Face landmarks and expressions: [MediaPipe Face Landmarker](https://ai.google.dev/edge/mediapipe/solutions/vision/face_landmarker), loaded from a CDN.
- Hair and clothes: colour and texture sampled above the forehead and below the chin.
- Restaurants: [OpenStreetMap](https://www.openstreetmap.org/copyright) via the Overpass API, place search via Nominatim.
