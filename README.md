<!--
  Name     : README.md
  Purpose  : Overview of the sstv repository (SSTV transmission, reception and diagnosis)
  Author   : Eric PERRET
  Date     : 2026-10-18
  Version  : 1.7
  License  : CC BY-NC 4.0
-->

# 📻 SSTV

🇫🇷 [Version française : LISEZMOI.md](LISEZMOI.md)

Slow Scan Television (SSTV) in the browser: encode an image into an audio file, decode a file or live sound, diagnose a recording. Three standalone HTML files, no library, no installation. User interfaces in French (diagnostic tool in French or English, after the browser).

▶️ **[Tools home page](https://ericperret.github.io/sstv/index2.html)**

| Tool | Launch |
|---|---|
| SSTV multi-mode transmitter v4 | ▶️ **[sstv_tx_multimode_v4.html](https://ericperret.github.io/sstv/sstv_tx_multimode_v4.html)** |
| SSTV Decoder Ultimate | ▶️ **[sstv_decoder_ultimate.html](https://ericperret.github.io/sstv/sstv_decoder_ultimate.html)** |
| SSTV Diagnostic | ▶️ **[sstv_diagnostic.html](https://ericperret.github.io/sstv/sstv_diagnostic.html)** |

---

## SSTV multi-mode transmitter v4

![SSTV multi-mode transmitter v4](screenshot_sstv_tx_multimode_v4.png)

| Feature | Description |
|---|---|
| Image | Image loading, scaled to the chosen mode |
| Modes | Robot36 colour and B&W, Robot72, Martin M1 / M2, Scottie S1 / S2, PD90, PD120, PD160, PD180, PD240 (duration shown) |
| Signal | PCM 16-bit mono 44.1 kHz WAV, sample-accurate timing (Robot36 line = 150.000 ms) |
| Header | Standard VIS code (start bit, 7 bits, even parity, stop bit), optional 1 s calibration tone at 1,900 Hz |
| Output | Downloaded WAV file, to be played through a transmitter or a loudspeaker |

## SSTV Decoder Ultimate

![SSTV Decoder Ultimate](screenshot_sstv_decoder_ultimate.png)

| Feature | Description |
|---|---|
| Sources | WAV file (8 / 16 / 24 / 32-bit or float, mono or stereo, any sample rate), or live audio from the microphone at its native sample rate (smartphone friendly, screen kept awake) |
| Modes | Automatic detection by VIS code, or forced: Robot36 / 72, Martin M1 / M2, Scottie S1 / S2, PD90 to PD240 |
| Synchronisation | All modes: sync tracked line by line and measured clock (no slant); automatic frequency correction (AFC) measured on the VIS leader and the sync pulses, up to ±250 Hz |
| WAV file | Opening a file runs the built-in diagnostic (VIS, sync measurements, clock error, drift, sync deviation and frequency plots) and decodes at once when the mode is known |
| Microphone | Family selector (Robot, Martin, Scottie, PD); reception starts on START; the last 5 minutes are kept and tapping the image decodes them again in the next sub-mode, even after STOP |
| Output | PNG export of the decoded image; WAV recording of the microphone capture |

## SSTV Diagnostic

![SSTV Diagnostic](screenshot_sstv_diagnostic.png)

| Feature | Description |
|---|---|
| Input | Any WAV file (8 / 16 / 24 / 32-bit or float, mono or stereo, any sample rate) |
| Measurements | Standard VIS, all 11 modes, sync pulses measured line by line: line period, clock error (ppm), cumulative drift (ms and pixels), sync duration and frequency |
| Plots | Sync deviation from nominal timing (a clock error shows as a slope); instantaneous frequency with zoom and A / B measurement on click |
| Language | French or English, after the browser |

---

## Versions

The tools at the root of the repository are the **approved** version. Work in progress lives in the [dev/](dev/) folder, same file names, online at ▶️ **[dev/index2.html](https://ericperret.github.io/sstv/dev/index2.html)**. A version is copied to the root only once approved; each approved version is tagged (`tx-4.2`, `rx-1.8`, `diag-2.0`…).

## Amateur radio

SSTV is used by radio amateurs to send images over HF / VHF. These tools let you experiment without a transmitter, through an audio cable or acoustic coupling; transmitting on amateur bands still requires a licence.

## History

| Version | Change |
|---|---|
| 2026-10-17 | Files renamed without copy suffix, header blocks, home page fixed, README / LISEZMOI rewritten |
| 2026-10-17 | Transmitter 4.1: standard VIS, exact timing, Robot36 fixed. Decoder 1.1: VIS detection, any WAV format, Robot36 sync tracking. Validated against an external decoder and ARISS / PySSTV recordings (Robot36 only) |
| 2026-10-17 | Decoder 1.2: live microphone reception on the same decoding chain as files (Robot36 VIS, sync tracking, measured clock), tested on simulated acoustic coupling |
| 2026-10-17 | Decoder 1.3: microphone left at its default settings (browser processing off only on request), level meter in dBFS, recording of the microphone capture to WAV |
| 2026-10-17 | Decoder 1.4: no log displayed; microphone tab simplified: Robot36 only, start on regular sync pulses (VIS optional), touch-friendly audio processing toggle usable during capture, level meter -90 to 0 dBFS, capture recording below the image |
| 2026-10-17 | Decoder 1.5: microphone reception starts on START without waiting for VIS or sync, runs continuously until STOP (images follow one another), locks on the first sync found; a Robot36 VIS realigns the image to the top |
| 2026-10-17 | Decoder 1.6: microphone with echo cancellation and noise suppression off, automatic gain (preamp) on with a button to turn it off; PNG and WAV downloads fixed on Chrome Android |
| 2026-10-18 | Approved: transmitter 4.1, decoder 1.6. In progress in [dev/](https://ericperret.github.io/sstv/dev/index2.html): transmitter 4.2 (Robot72 fixed, PD90 / PD160 / PD240), decoder 1.7 (all modes with sync tracking, microphone family selector, 5-minute buffer re-decoded by tapping the image) |
| 2026-10-18 | Approved: diagnostic 2.0 |
| 2026-10-18 | In progress in dev/: decoder 1.8, file tab with the built-in diagnostic: opening a WAV runs the measurements and decodes at once when the mode is known (VIS or chosen); automatic frequency correction (AFC) measured on the VIS leader and the sync pulses, up to ±250 Hz; Analyse / Decode buttons, manual Doppler, waveform and spectrogram removed |
| 2026-10-18 | Approved: transmitter 4.2, decoder 1.8 |
| 2026-10-18 | In progress in dev/: decoder 1.9, microphone with all browser processing off, automatic gain (preamp) included; preamp button removed |
| 2026-10-18 | In progress in dev/: decoder 1.10, B&W variant of every mode (same signal, luminance only: transmitted Y for Robot and PD, BT.601 luminance of R, G, B for Martin and Scottie), each mode followed by its B&W variant when tapping the image, B&W variants in the file mode selector; transmitter 4.3, non-standard "Robot36 B&W" removed |

## License

[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) — see [LICENSE (CC BY-NC 4.0)](<LICENSE (CC BY-NC 4.0)>).

## Author

**Eric PERRET** — [GitHub](https://github.com/ericperret)
