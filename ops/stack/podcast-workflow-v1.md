# Podcast-style YouTube Workflow (Voice + Kinetic Text)

## Recommendation
Yes — podcast format is a strong fit for 5minsbliss:
- Lower production friction
- Better consistency for long-term cadence
- Strong match with reflective content style

## Video format
- 6-10 min audio-led episodes
- Visual layer: themed still background + kinetic key phrases
- Captions always on (English)

## Production chain
1. Final script (English)
2. Voice generation (Edge TTS / ElevenLabs)
3. Timestamp key lines for on-screen text
4. FFmpeg render:
   - static/loop background
   - audio track
   - subtitles burn-in
5. Upload package (title, description, chapters, tags)

## FFmpeg baseline
```bash
ffmpeg -loop 1 -i bg.png -i voice.mp3 \
  -vf "subtitles=captions.srt:force_style='Fontsize=18,Outline=1'" \
  -c:v libx264 -tune stillimage -c:a aac -b:a 192k -shortest output.mp4
```
