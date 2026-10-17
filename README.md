<!--
  Name     : README.md
  Purpose  : Overview of the sstv repository (SSTV transmission, reception and diagnosis)
  Author   : Eric PERRET
  Date     : 2026-10-17
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
| Signal | 44.1 / 48 / 22.05 kHz sampling, low-pass filter, line transition smoothing |
| Header | VIS code (automatic detection at reception), 1 s calibration tone at 1,900 Hz |
| Output | Downloaded WAV file, to be played through a transmitter or a loudspeaker |

## SSTV Decoder Ultimate

![SSTV Decoder Ultimate](screenshot_sstv_decoder_ultimate.png)

| Feature | Description |
|---|---|
| Sources | WAV file, or live audio (microphone, permission requested) |
| Modes | Automatic detection by VIS code, or forced: Robot36 / 72, Martin M1 / M2, Scottie S1 / S2, PD90 to PD240 |
| Synchronisation | PLL on sync pulses, automatic AFC, manual Doppler offset, slant correction |
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

## License

[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) — see [LICENSE (CC BY-NC 4.0)](<LICENSE (CC BY-NC 4.0)>).

## Author

**Eric PERRET** — [GitHub](https://github.com/ericperret)
