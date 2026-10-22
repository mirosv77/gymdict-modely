# Modely reči pre appku GymDict

Súbory modelov, ktoré si appka **GymDict** (hlasový tréningový denník do fitka, vydáva Dorotty, s. r. o.)
stiahne pri prvom spustení alebo v Nastaveniach. Reč sa potom rozpoznáva len v mobile, bez internetu
(whisper.cpp v1.9.3). Appka súbory sťahuje cez adresu `https://dorotty.cloud/modely/<súbor>`, ktorá
presmeruje na vydanie v tomto repozitári.

- Podpora: https://dorotty.cloud/gymdict
- Zásady ochrany súkromia: https://dorotty.cloud/gymdict/sukromie
- Kontakt: info@dorotty.cloud

## Súbory (vydanie v1)

| Súbor | Veľkosť (B) | SHA-256 |
|---|---:|---|
| `ggml-kinit-parakeet-tdt-0.6b-v3-sk-q4_0.bin` | 355 615 679 | `91f6639ebc9edf7437d6c7d3b8bf6342d9695887f5ae2b824dbc634c5dd652d1` |
| `ggml-kinit-parakeet-tdt-0.6b-v3-sk-q5_0.bin` | 433 901 039 | `16e6add6efce74023ddaf70d1541e36e8253b06f07511d3bc693beb7f1216344` |
| `ggml-kinit-whisper-small-sk-q5_1.bin` | 190 085 504 | `f654a1d4bbcedc793b2c12875ed4b75dc57e790e849cf4a718e22f2318efe5ec` |
| `ggml-kinit-whisper-base-sk-q5_1.bin` | 59 707 642 | `e9f05487d8490571dc8401ebf433839ef4ab967e694463235ec14b9dfdccf581` |
| `ggml-silero-v6.2.0.bin` | 885 098 | `2aa269b785eeb53a82983a20501ddf7c1d9c48e33ab63a41391ac6c9f7fb6987` |

## Pôvod, licencie a zmeny

### Parakeet TDT 0.6B v3, slovenský (KInIT)

- Súbory `ggml-kinit-parakeet-tdt-0.6b-v3-sk-*.bin`.
- Parakeet TDT 0.6B v3 © NVIDIA ([nvidia/parakeet-tdt-0.6b-v3](https://huggingface.co/nvidia/parakeet-tdt-0.6b-v3)),
  slovenská verzia © Kempelenov inštitút inteligentných technológií (KInIT)
  ([kinit/parakeet-tdt-0.6b-v3-sk](https://huggingface.co/kinit/parakeet-tdt-0.6b-v3-sk/tree/45003b0f84e6013400f05cb5eff564461d5f4774)).
- Licencia: [Creative Commons Attribution 4.0 (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).
- Zmeny: prevedené do formátu ggml skriptom `convert-parakeet-to-ggml.py` z whisper.cpp v1.9.3
  a kvantizované (q4_0, q5_0). Zmeny urobila Dorotty, s. r. o., v roku 2026.

### Whisper Small a Base, slovenské (KInIT)

- Súbory `ggml-kinit-whisper-small-sk-q5_1.bin` a `ggml-kinit-whisper-base-sk-q5_1.bin`.
- © KInIT ([kinit/whisper-small-sk](https://huggingface.co/kinit/whisper-small-sk/tree/50946518f91432354172a43f6ee009fb3b97c3e2),
  [kinit/whisper-base-sk](https://huggingface.co/kinit/whisper-base-sk/tree/4be43dfee41c851d6b534fb802fcd486ef2e8c97)),
  dotrénované z modelov OpenAI Whisper (licencia MIT).
- Licencia: Apache License 2.0, text v súbore [`LICENSE-Apache-2.0.txt`](LICENSE-Apache-2.0.txt).
- Zmeny: prevedené do formátu ggml skriptom `convert-h5-to-ggml.py` z whisper.cpp v1.9.3 (s mel filtrami
  z [openai/whisper](https://github.com/openai/whisper), licencia MIT) a kvantizované (q5_1). Zmeny urobila
  Dorotty, s. r. o., v roku 2026.

### Silero VAD (detekcia reči)

- Súbor `ggml-silero-v6.2.0.bin` z [ggml-org/whisper-vad](https://huggingface.co/ggml-org/whisper-vad/tree/9ffd54a1e1ee413ddf265af9913beaf518d1639b),
  bez zmien.
- [Silero VAD](https://github.com/snakers4/silero-vad) © Silero Team, licencia MIT, text v súbore
  [`LICENSE-MIT-Silero.txt`](LICENSE-MIT-Silero.txt).

## English

Speech recognition models downloaded by the GymDict app (a voice workout log by Dorotty, s. r. o.).
Speech is recognized on the device only (whisper.cpp v1.9.3). Parakeet TDT 0.6B v3 © NVIDIA, Slovak
version © KInIT, CC BY 4.0. Whisper Small/Base SK © KInIT, based on OpenAI Whisper, Apache 2.0.
Silero VAD © Silero Team, MIT. The Parakeet and Whisper files were converted to the ggml format and
quantized by Dorotty, s. r. o. in 2026; the Silero VAD file is unchanged.
