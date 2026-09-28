# Hand → Visible Light Wavelength

A Python/Flask website that uses your webcam and MediaPipe Hands to turn the distance between two hands into a visible-light wavelength.

- Hands close: violet/blue, around 380 nm
- Hands farther apart: orange/red, up to 700 nm
- Hands touching: white
- Live wavelength shown on screen

## Run

```bash
python -m venv .venv
# Windows:
.venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate

pip install -r requirements.txt
python app.py
```

Open http://localhost:5000 in a modern browser and allow camera access.

## Notes

The mapping is intentionally visual rather than a physical measurement of emitted light. The displayed wavelength is the wavelength assigned to the hand separation. MediaPipe is loaded from jsDelivr, so internet access is needed unless you vendor the JavaScript assets locally.
