# Arrumo OpenAI Plugin

The default OpenAI adapter for transcription and image generation.

Copyright © 2026 DEVS AI Unipessoal LDA. Licensed under the [GNU Affero General Public License v3.0](LICENSE).

For custom AI solutions for your company, visit [DEVS AI](https://aidevs.pt).

The bundled transcription adapter uses `transcription.json` to declare the OpenAI endpoint, model, and SDK credential field. It returns transcript text and detected language metadata. See the [OpenAI file transcription guide](https://developers.openai.com/api/docs/guides/speech-to-text).

Delivery subtitles use `transcription-timed.json`, which requests timestamped
speaker segments from the diarization model. Arrumo uses the returned segment
times as caption boundaries. [OpenAI transcription response formats](https://developers.openai.com/api/reference/resources/audio/subresources/transcriptions/methods/create/)

## Transcription and subtitles

[English](docs/en/transcription.md) · [Español](docs/es/transcription.md) · [Português](docs/pt/transcription.md)

## Package a release candidate

From this checkout, use the Arrumo Plugin SDK packager with the adapter files
listed explicitly. Record the SDK commit and the SHA-256 printed by the tool.

```sh
python /path/to/plugin-sdk/tools/package_plugin.py . plugin.zip --include LICENSE --include README.md --include transcription.json --include transcription-timed.json
```
