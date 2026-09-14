# OOSAI - Brainwave & Bell Studio

> A fully offline, privacy-first audio studio for meditation, sleep, focus, and ambient exploration. Every sound is synthesized in real time on your device - no audio files, no streaming, no servers, no tracking.

**Version:** 1.0.7
**Package:** `com.onemanstudios.oosai`
**Developer:** One Man Studios

---

## What It Is

**OOSAI** is a calm, private, offline-capable audio studio that fits in your pocket. The entire app - all synthesis, all presets, all statistics, all visuals - is generated in real time on your device. Nothing is downloaded, nothing is uploaded, and nothing leaves your phone unless you explicitly back it up.

The studio offers two complementary modes:

| Mode | Purpose |
|------|---------|
| **Brainwave** | Binaural beats, isochronic tones, and colored noise for entraining delta, theta, alpha, beta, and gamma brain states. Built for meditation, sleep, focus, and creative flow. |
| **Bell** | Generative bell textures built from additive synthesis with Freeverb reverb. Creates ambient, contemplative, atmospheric soundscapes that evolve forever without repeating. |

Both modes share a common session system - timers, fade in/out, interval bells, scheduled starts, mood tracking, and rich statistics - so the same workflow applies no matter which mode you choose.

> *"Math, Sound, Frequencies and Time shapes us."*

---

## Key Highlights

- **100% offline** - works on a plane, in a basement, anywhere. Zero network requests after install.
- **Zero audio assets** - every sound you hear is synthesized mathematically in real time. The app contains no MP3s, no WAV files, no samples, no recordings. The entire audio engine is pure code.
- **Zero permissions abuse** - only 3 permissions, all directly tied to audio playback. No internet, no storage, no microphone, no contacts, no location.
- **Zero tracking** - no analytics, no telemetry, no account, no cloud sync, no ads.
- **Tiny APK** - because there are no audio assets to ship, the entire app is just code.
- **Privacy first** - all your presets, mood ratings, streak history, and schedules live only in the app's private storage on your device.

---

## Requirements

### Device requirements
- **Android 4.4 (KitKat, API 19) or higher** - works on essentially any Android device from the last decade.
- **Headphones required for binaural beats** - each ear must receive its own tone for the binaural effect to work. Any wired or Bluetooth headphones will do.
- **Speakers are fine** for Bell mode, isochronic tones, and monaural beats.
- **Approximately 50 MB of free RAM** during playback for the real-time synthesis engine.
- **No internet connection required** at any point - not even on first launch.

### Headphone recommendations
- Wired earbuds or over-ear headphones give the strongest binaural effect.
- Bluetooth headphones work, but very low-latency codecs (aptX, LDAC) are preferred over standard SBC for tighter stereo separation.
- Stereo speakers on a phone or laptop will NOT produce the binaural effect - you will hear a mono mix.

---

## Permissions

OOSAI requests only three permissions, and every one of them is directly tied to audio playback. There is no internet permission, no storage permission, no microphone permission, no location permission, no contacts permission.

| Permission | Why it is needed |
|-----------|------------------|
| `WAKE_LOCK` | Keeps the CPU running during long playback sessions so audio does not stutter when the screen turns off. Without this, Android would put the app to sleep and the sound would cut out. |
| `FOREGROUND_SERVICE` | Allows OOSAI to run as a foreground service while audio is playing, so Android does not kill it in the background. |
| `FOREGROUND_SERVICE_MEDIA_PLAYBACK` | The specific foreground service type (introduced in Android 14) required for media playback services. Lets Android know this is a legitimate audio app, not a sneaky background process. |

That is the complete list. There is no `INTERNET`, no `READ_EXTERNAL_STORAGE`, no `RECORD_AUDIO`, no `ACCESS_FINE_LOCATION`, no `READ_CONTACTS` - nothing that touches your private data or your network.

---

## Features

### Brainwave Mode

Brainwave mode generates binaural beats by presenting two slightly different pure tones to each ear through headphones. The left ear hears the carrier frequency, and the right ear hears the carrier plus the beat frequency. The brain perceives a third phantom beat at the difference, encouraging neural entrainment toward delta, theta, alpha, beta, or gamma states.

- **Binaural beats** - the classic headphone-only mode. Standard entrainment, requires stereo separation.
- **Monaural beats** - both tones are mixed together in the air. Works on speakers, weaker entrainment, no headphones needed.
- **Harmonic Box** - uses 4 tones (2 per ear) for a richer, more immersive beat. Headphones required.
- **Isochronic tones** - regular amplitude pulses at the beat frequency. Stronger entrainment than binaural alone, works on speakers.
- **7 background noise colors:**
  - White - hiss like TV static, bright and even.
  - Pink - softer hiss, balanced for human hearing, like steady rain.
  - Brown - deep rumble, low-frequency, like ocean surf or distant thunder.
  - Ocean - synthesized ocean waves with rhythmic ebb and flow.
  - Gray - mid-frequency hiss, especially good at masking speech.
  - Green - filtered noise with a soft, soothing, warm character.
  - Violet - high-frequency hiss, airy and bright, like wind through leaves.
- **4 waveforms** - sine (smoothest), square (harshest), triangle (middle ground), sawtooth (bright).
- **3-band EQ** - low shelf at 200 Hz, peaking at 1 kHz, high shelf at 5 kHz, plus Bass+, Treble+, and Flat quick presets.
- **Stereo field** - Mid/Side stereo width control and L/R channel balance.
- **Frequency sweep** - gradually shifts the carrier tone from a start to an end frequency over a set duration. Useful for guided descents (e.g., 200 Hz to 100 Hz over 20 minutes to move from active beta to relaxed alpha). The beat frequency stays constant so the entrainment target is preserved.
- **30+ built-in presets** organized into 5 categories: Consciousness, Sleep, Brainwaves, Healing, Energy. Includes the complete Solfeggio frequency scale (174-963 Hz) and a dedicated Addiction Recovery / Neurological Repair set.

### Bell Mode

Bell mode uses additive synthesis - each bell strike is built from 5-9 sine-wave partials at specific frequency ratios that mimic real bells. Unlike a piano (which has near-harmonic partials), bells have strongly inharmonic partials, which gives them their distinctive metallic, shimmering character.

- **4 bell textures:**
  - Tubular - bright metallic chime, like orchestral tubular bells. Clear and ringing.
  - Church - deep, resonant, traditional church-bell character. Rich low end.
  - Bowl - singing-bowl tone, warm, rounded, meditative. Sustains long.
  - Crystal - ethereal, glassy, high-pitched. The most delicate and airy texture.
- **Freeverb reverb** - a classic reverb algorithm using 8 parallel comb filters and 4 series allpass filters. Creates the spacious, ambient reverb tail heard on each bell. Full control over room size, damping, width, and wet mix.
- **Shimmer** - an octave-up version of the reverb wet signal, added on top of the normal reverb. Creates an ethereal, ascending, angelic quality.
- **Stereo delay** - echo effect with independent left and right delay times and feedback control.
- **Strike transient** - a bandpass-filtered noise burst that adds the initial metallic attack to each bell.
- **Beating** - slight detune between partials creating a slow wavering effect for organic warmth.
- **Generative engine** - creates melodies using a random-walk algorithm through any key and scale, with optional bass layer, octave spread, time scatter, and humanization. The same seed always produces the same melody, so you can save a melody you love as a preset and come back to it months later.
- **25+ built-in presets** including Sera, Tempio, Cattedrale, Aurora, Notte, Deriva, Cristallo, Festa, Zen Garden, Samadhi, Merkaba, Lullaby, Midnight Toll, Floating, Crystal Focus, Flow State, Crystal Clarity, Heart Bell, Solace, Chakra Bells, Sunrise Bells, Celebration, Vitality, and more.

### Session & Wellness

Both modes share a complete session system so the same workflow applies no matter which mode you choose.

- **Session timers** - infinity, 15, 30, 45, 60, or 90 minutes, or a custom value.
- **Fade in / out** - gradual volume ramps at the start and end of a session to avoid sudden loud onset or abrupt cutoff.
- **Interval bell** - plays a soft singing-bowl chime every N minutes for mindfulness check-ins during long sessions.
- **Scheduled sessions** - auto-starts a session at a specific time, like a meditation alarm clock. Overlap detection prevents conflicts. Great for daily practice.
- **Mood tracking** *(opt-in, off by default)* - rate anxiety, focus, relaxation, and energy before and after each session. The effectiveness score (post minus pre) is aggregated per preset so you can see which presets actually work for you.
- **Statistics** - a 5-tab insights panel:
  - **Overview** - total sessions, total time, most-used presets.
  - **Streak** - current streak, best streak, and a 12-week GitHub-style activity calendar.
  - **Report** - week-over-week and month-over-month deltas in session time and count.
  - **Best Time** - a 24-hour heatmap showing when you meditate most.
  - **Effectiveness** - per-preset mood deltas ranked, so you can see which presets actually move the needle.
- **Favorites** - star any preset and filter the list to favorites only.
- **Custom presets** - save current settings as a personal preset. Custom presets appear at the top under "My Presets" and can be drag-reordered.
- **Master backup** - one-click JSON export and import of everything (settings, presets, stats, mood data, favorites).

### Visualization

- **Canvas 2D visualizer** - a Mandelbrot-flavored mandala with a pulsing core orb, a 6-fold flower of life pattern, expanding ripple rings, a particle field with parallax depth, radial frequency bars, an oscilloscope waveform overlay, and bell-strike ripples colored by pitch.
- **Spectrogram** - an optional scrolling spectrum analyzer.
- **Ripple canvas** - touch or note-on triggers painted ripples.
- **Logo canvas** - a live Mandelbrot fractal in the header.

### Android Integration

- **Foreground notification** - a persistent notification while audio is playing, with the current preset name and a Stop button. Survives screen lock.
- **Lock-screen controls** - play, pause, and stop from the lock screen or Bluetooth media keys.
- **Edge-to-edge UI** - transparent system bars with proper inset handling for notched and hole-punch displays.
- **Back-button aware** - back gesture or button closes any open drawer or modal first, and only exits the app when nothing is open.
- **Adaptive launcher icon** - a procedurally generated Mandelbrot fractal in an amber palette, rendered at every Android density from mdpi to xxxhdpi.

### Privacy

- **No internet** - once the app is installed, zero network requests. There is no internet permission in the manifest, so the app physically cannot connect to anything.
- **No cookies, no fingerprinting, no third-party scripts.**
- **No analytics, no telemetry, no account, no cloud sync, no ads.**
- **No audio files** - every sound is synthesized in real time from mathematical formulas. The APK contains zero bytes of audio data.
- **All user data is private** - presets, mood ratings, streak history, schedules, and favorites live only in the app's private storage on your device. They leave your device only when you explicitly use Export All to back them up to a JSON file.

---

## How the Audio Works (No Samples, No Files)

This is worth emphasizing because it is unusual: **OOSAI ships with zero audio assets.** There are no MP3s, no WAVs, no FLACs, no OGGs, no samples, no recordings of any kind inside the APK.

Every sound you hear is generated mathematically in real time:

- **Binaural beats** are produced by two oscillators running at slightly different frequencies, panned hard left and right.
- **Noise colors** are generated by filtering pure white noise through different digital filters. White noise itself is generated from a pseudorandom number generator.
- **Ocean sounds** are white noise passed through a lowpass filter whose cutoff frequency is slowly modulated by a sine wave LFO.
- **Bells** are built using additive synthesis: each strike is the sum of 5-9 sine-wave partials at specific inharmonic frequency ratios, each with its own decay envelope. A bandpass-filtered noise burst adds the initial metallic strike. The result is then passed through a Freeverb reverb (8 comb filters + 4 allpass filters), optional shimmer (octave-up reverb tail), and stereo delay.
- **Melodies** are generated by a random-walk algorithm through a musical scale, seeded by a number you can lock for reproducibility.

Because everything is code, the APK is tiny. Because everything is real-time, the audio never repeats in Bell generative mode - it can run for hours or days without looping.

---

## Installation

OOSAI is distributed as a signed APK file. Since it is not on the Google Play Store, you will need to enable sideloading.

### Steps

1. **Download the APK** file (`oosai.apk`) from the GitHub Releases page.
2. **Enable sideloading** on your Android device:
   - Android 8+: Settings > Apps > Special access > Install unknown apps, then allow your browser or file manager to install APKs.
   - Android 7 and below: Settings > Security > Unknown sources, then toggle it on.
3. **Open the APK** from your downloads or file manager.
4. **Tap Install** when prompted.
5. **Open OOSAI** from your app drawer.

The APK is signed with a self-signed certificate. Android may warn that the developer is unknown - this is expected for any sideloaded app that is not from the Play Store.

## Quick Start Guide

1. **Pick a mode** - tap Brainwave or Bell in the header.
2. **Open Presets** (top-right grid icon) - browse by category. Tap the star icon to favorite presets. Use Exp / Imp buttons to export or import preset packs as JSON.
3. **Open Controls** (gear icon) - every slider has an info icon next to it with a plain-English explanation of what it does. Tap any slider value for precise numeric input via a keypad.
4. **Press Play** - the large play button in the bottom transport bar.
5. **Set a timer** - in the Session tab, pick infinity / 15 / 30 / 45 / 60 / 90 min, or set a custom value.
6. **Enable the interval bell** - in the Session tab, toggle it on to get a soft chime every N minutes for mindfulness check-ins.
7. **Schedule a session** - in the Session tab, set a time, duration, and preset to auto-start. Great for daily practice.
8. **Enable mood tracking** *(optional)* - in the Session tab, toggle "Rate mood after sessions" to be prompted with an anxiety / focus / relaxation / energy rating after each session.
9. **Save your own presets** - use the Save button inside the presets drawer to capture current settings as a custom preset.
10. **Back up everything** - use Export All / Import All at the top of the controls drawer to back up all your data (settings, presets, stats, favorites, mood data) to a single JSON file.

### Mobile Gestures

| Gesture | Action |
|---------|--------|
| Tap slider value | Enter a precise numeric value via the keypad |
| Long-press a preset | Delete it (custom presets only) |
| Tap a star | Favorite or unfavorite a preset |
| Drag a custom preset | Reorder it within My Presets |
| Back gesture or button | Closes any open drawer or modal first; exits the app only when nothing is open |

---

## Brainwave Frequency Reference

| Range | Name | State |
|-------|------|-------|
| 0.5-4 Hz | Delta | Deep sleep, healing, unconscious |
| 4-8 Hz | Theta | Meditation, creativity, REM sleep |
| 8-13 Hz | Alpha | Relaxation, calm focus, light meditation |
| 13-30 Hz | Beta | Active thinking, concentration, alertness |
| 30-80 Hz | Gamma | Peak cognition, insight, high-level processing |

### Solfeggio Frequencies (built-in as presets)

- 174 Hz - Foundation (pain relief, security)
- 285 Hz - Quantum (tissue healing, energy)
- 396 Hz - Liberation (releasing fear, guilt)
- 417 Hz - Facilitating (change, transitions)
- 528 Hz - Transformation (DNA repair, love)
- 639 Hz - Connecting (relationships, harmony)
- 741 Hz - Awakening (intuition, expression)
- 852 Hz - Returning (spiritual order)
- 963 Hz - Nectar (crown chakra, oneness)

---

## Safety Notice

**Gamma frequencies (30+ Hz) may trigger seizures in individuals with photosensitive epilepsy.** If you have epilepsy, consult your doctor before using gamma-range presets. Discontinue use immediately if you experience headaches, dizziness, or visual disturbances.

Brainwave entrainment is a wellness tool, not a substitute for medical treatment. If you are being treated for epilepsy, severe depression, PTSD, or any neurological or psychiatric condition, consult your healthcare provider before using binaural beats or isochronic tones.

Do not use brainwave entrainment while operating machinery, driving, or performing any task that requires full attention.

---

## Data and Privacy

### What is stored on your device

- Your current settings (mode, frequencies, volumes, EQ, etc.)
- Your custom presets
- Your favorites
- Your session statistics (counts, durations, timestamps)
- Your mood ratings (if you have enabled mood tracking)
- Your scheduled sessions

All of this lives in the app's private storage. It is never sent anywhere.

### What is stored on servers

Nothing. There are no servers. The app has no internet permission.

### How to back up your data

Open the Controls drawer (gear icon) and tap Export All. You will be prompted to save a JSON file containing everything. Move this file to a safe location.

### How to restore your data

Open the Controls drawer and tap Import All. Select a previously exported JSON file. This replaces your current data.

### How to wipe everything

Open Session Insights (chart icon) and tap Clear All Data. Alternatively, uninstall the app.

---

## Troubleshooting

**No sound during playback**
- Check the master volume slider in the bottom transport bar.
- Check your device's media volume (not ringer volume).
- If using Brainwave mode, make sure headphones are connected - binaural beats will not work on phone speakers.
- Make sure the Bell Sound toggle (in Bell mode, Main tab) is on.

**Audio stutters or drops out**
- Close other audio apps (music players, YouTube, Spotify).
- If your device is in battery-saver mode, try disabling it - synthesis is CPU-intensive.
- Lower the Chunk Beats value in the Bell Advanced tab.

**Notification does not appear**
- Check that notifications are not blocked for OOSAI in your device settings.
- On Android 13+, make sure notification permission is granted.

**Scheduled session did not start**
- Make sure the app is not force-stopped. On some devices (Xiaomi, Huawei, Samsung), aggressive battery managers kill background apps. Add OOSAI to the battery optimization exemption list.
- Scheduled sessions fire at the start of the minute, so set the time one minute ahead to test.

**Binaural beats do not feel effective**
- Make sure you are using headphones, not speakers.
- Make sure the L/R channels are not swapped (some Bluetooth earbuds swap channels).
- Try a different beat mode (Monaural or Harmonic Box) if you cannot use headphones.
- Make sure the Stereo Width is at 100% and Channel Balance is at 0.

**Export or Import does not work**
- The file picker uses Android's Storage Access Framework. Make sure your file manager supports it.
- On Android 4.4 (KitKat), SAF may be unavailable on some vendor ROMs.

---

## Frequently Asked Questions

**Is this app free?**
Yes. OOSAI is released as a free, open tool for personal use.

**Does it contain ads?**
No. Zero ads, ever.

**Does it need internet?**
No. The app has no internet permission. It physically cannot connect to anything.

**Does it use any audio files?**
No. Every sound is synthesized mathematically in real time. The APK contains zero bytes of audio data.

**Does it work offline?**
Yes, fully. It works on a plane, in a tunnel, anywhere.

**Does it work on iPhone?**
No. OOSAI is Android-only at this time.

**Does it work on Android TV or Android Auto?**
It installs and runs, but the UI is designed for touch phones and tablets. Media-key play/pause/stop works over Bluetooth.

**Will it drain my battery?**
Real-time audio synthesis is CPU-intensive. Expect roughly the same battery usage as playing music from Spotify or YouTube. The WAKE_LOCK permission keeps the CPU awake during playback so the audio does not stutter, which does use more battery than idle.

**Can I use my own audio files as background?**
Not in this version. All audio is synthesized in real time.

**Can I export the audio to a WAV file?**
Not in this version. Audio is real-time only.

**Is the source code open?**
Only the APK is distributed at this time. The app is a personal project by One Man Studios.

**Will my data survive an app update?**
Yes. Updates install over the existing app and preserve your data.

---

## Credits

### Inspiration

**Campana** by Matteo Bassi (github.com/bassimatte/campana) - an open-source generative bell instrument originally written in Python. It pioneered the idea of slowly evolving, reverb-soaked bell textures as a meditative listening experience.

OOSAI re-implements the bell idea from scratch with a completely different backend. The entire synthesis engine was rewritten to run on-device in real time. The original Python code is not used, copied, or distributed. Only the musical inspiration is carried over.

### Implementation

OOSAI is designed, coded, and tuned end-to-end by **One Man Studios**. The bell partial ratios, texture definitions, and additive-synthesis-with-Freeverb approach are based on acoustics literature and the Campana project's approach. Everything else is original.

Special thanks to Matteo Bassi for open-sourcing Campana under a permissive license, to the Web Audio API working group for making sample-accurate on-device audio possible, and to everyone in the meditation, focus, and ambient-music communities whose feedback shaped the studio's direction.

---

## License

Released as a free, open tool for personal use. Strictly No Commerical Purposes or Monetizations.

---

## Links

- **One Man Studios - GitHub:** github.com/one-man-studios
- **Website:** comfyinsta.neocities.org
- **Campana (inspiration):** github.com/bassimatte/campana
