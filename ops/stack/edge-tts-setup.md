# Edge TTS Setup (Installed)

## Status
Installed and tested on this machine.

## Binary
`~/.local/bin/edge-tts`

## Test output
- `assets/audio/edge-tts-sample-jenny.mp3`
- `assets/audio/edge-tts-sample-jenny.vtt`

## Example command
```bash
~/.local/bin/edge-tts \
  --text "Welcome to 5 mins Bliss." \
  --voice en-US-JennyNeural \
  --write-media assets/audio/sample.mp3 \
  --write-subtitles assets/audio/sample.vtt
```
