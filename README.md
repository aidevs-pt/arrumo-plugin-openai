# Arrumo OpenAI Plugin

The default OpenAI adapter for transcription and image generation.

## Icon and trademarks

`icon.svg` shows OpenAI's logo so creators recognise the service this plugin connects to. OpenAI and the OpenAI logo are trademarks of OpenAI; the manifest's `iconNotice` says so wherever Arrumo shows the icon. The logo is not covered by this repository's license, and this plugin is not affiliated with or endorsed by OpenAI. The SVG is a square without rounded corners; Arrumo rounds it. If OpenAI asks, replace the logo with a generic symbol and remove `iconNotice`.

## Transcription and subtitles

[English](https://github.com/aidevs-pt/arrumo-docs/blob/main/content/docs/en/plugins/openai/transcription.md) · [Español](https://github.com/aidevs-pt/arrumo-docs/blob/main/content/docs/es/plugins/openai/transcription.md) · [Português](https://github.com/aidevs-pt/arrumo-docs/blob/main/content/docs/pt/plugins/openai/transcription.md)

## Images

[English](https://github.com/aidevs-pt/arrumo-docs/blob/main/content/docs/en/plugins/openai/images.md) · [Español](https://github.com/aidevs-pt/arrumo-docs/blob/main/content/docs/es/plugins/openai/images.md) · [Português](https://github.com/aidevs-pt/arrumo-docs/blob/main/content/docs/pt/plugins/openai/images.md)

`image-generation.json` declares the OpenAI image endpoint, the default model and the **Image model** setting that overrides it. See the [OpenAI image generation guide](https://developers.openai.com/api/docs/guides/image-generation).

## Package a release candidate

From this checkout, use the Arrumo Plugin SDK packager with the adapter files
listed explicitly. Record the SDK commit and the SHA-256 printed by the tool.

```sh
python /path/to/plugin-sdk/tools/package_plugin.py . plugin.zip --include LICENSE --include README.md --include transcription.json --include transcription-timed.json --include image-generation.json
```
