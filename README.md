<!--
  Name     : README.md
  Purpose  : Overview of the sstv repository (SSTV transmission, reception and diagnosis)
  Author   : Eric PERRET
  Date     : 2026-10-17
  Version  : 1.2
  License  : CC BY-NC 4.0
-->

# 📻 SSTV

🇫🇷 [Version française : LISEZMOI.md](LISEZMOI.md)

Slow Scan Television (SSTV) in the browser: encode an image into an audio file, decode a file or live sound, diagnose a recording. Three standalone HTML files, no library, no installation. User interfaces in French (diagnostic tool in English).

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
| Modes | Robot36 colour and B&W, Robot72, Martin M1 / M2, Scottie S1 / S2, PD120, PD180 (duration shown) |
| Signal | PCM 16-bit mono 44.1 kHz WAV, sample-accurate timing (Robot36 line = 150.000 ms) |
| Header | Standard VIS code (start bit, 7 bits, even parity, stop bit), optional 1 s calibration tone at 1,900 Hz |
| Output | Downloaded WAV file, to be played through a transmitter or a loudspeaker |

## SSTV Decoder Ultimate

![SSTV Decoder Ultimate](screenshot_sstv_decoder_ultimate.png)

| Feature | Description |
|---|---|
| Sources | WAV file (8 / 16 / 24 / 32-bit or float, mono or stereo, any sample rate), or live audio from the microphone at its native sample rate (smartphone friendly, screen kept awake) |
| Modes | Automatic detection by VIS code, or forced: Robot36 / 72, Martin M1 / M2, Scottie S1 / S2, PD90 to PD240 |
| Synchronisation | Robot36: sync tracked line by line and measured clock (no slant); automatic AFC, manual Doppler offset |
| Analysis | Signal analysis, image displayed as it decodes, debug log |
| Output | PNG export of the decoded image |

## SSTV Diagnostic

![SSTV Diagnostic](screenshot_sstv_diagnostic.png)

| Feature | Description |
|---|---|
| Input | WAV file |
| Searches | VIS code, sync pulses, line duration measurement |
| Plot | Instantaneous frequency, measurement on click |
| Results | Detected markers, timing analysis, log |

---

## Amateur radio

SSTV is used by radio amateurs to send images over HF / VHF. These tools let you experiment without a transmitter, through an audio cable or acoustic coupling; transmitting on amateur bands still requires a licence.

## History

| Version | Change |
|---|---|
| 2026-10-17 | Files renamed without copy suffix, header blocks, home page fixed, README / LISEZMOI rewritten |
| 2026-10-17 | Transmitter 4.1: standard VIS, exact timing, Robot36 fixed. Decoder 1.1: VIS detection, any WAV format, Robot36 sync tracking. Validated against an external decoder and ARISS / PySSTV recordings (Robot36 only) |
| 2026-10-17 | Decoder 1.2: live microphone reception on the same decoding chain as files (Robot36 VIS, sync tracking, measured clock), tested on simulated acoustic coupling |

## License

[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) — see [LICENSE (CC BY-NC 4.0)](<LICENSE (CC BY-NC 4.0)>).

## Author

**Eric PERRET** — [GitHub](https://github.com/ericperret)
