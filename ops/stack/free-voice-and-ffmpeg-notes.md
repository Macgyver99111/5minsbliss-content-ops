# Free Voice Options + FFmpeg Integration Notes

## Free / low-cost voice options
1. **Edge TTS (Free)**
   - CLI/package: edge-tts
   - Pros: free, fast, multiple voices
   - Cons: less expressive than ElevenLabs

2. **Piper TTS (Local, Free)**
   - Fully local, no API cost
   - Good for batch generation

3. **Coqui TTS (Local, Free)**
   - Flexible but setup heavier

## FFmpeg integration plan (this machine has FFmpeg)
Pipeline:
1. Generate voiceover audio (mp3/wav)
2. Prepare still images (carousel frames or b-roll stills)
3. Compose slideshow video with subtitles

Example command:
```bash
ffmpeg -y -r 1/5 -i frame-%02d.png -i voiceover.mp3 \
  -c:v libx264 -vf "fps=30,format=yuv420p" -shortest output.mp4
```

Subtitle burn-in example:
```bash
ffmpeg -i output.mp4 -vf "subtitles=captions.srt" -c:a copy output-sub.mp4
```
