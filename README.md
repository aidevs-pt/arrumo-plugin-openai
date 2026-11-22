# Arrumo OpenAI Plugin

The default OpenAI adapter for transcription and image generation.

## Icon and trademarks

`icon.svg` is a generic symbol drawn for Arrumo (a sound wave beside a page and a frame, for transcription and images), covered by this repository's
license. It is not the provider's logo: the provider has not published permission for its
logo to appear in another app's interface, so the plugin does not use it. The name is used
only to say which service the plugin connects to; this plugin is not affiliated with or
endorsed by the provider.

## Transcription and subtitles

[English](docs/en/transcription.md) · [Español](docs/es/transcription.md) · [Português](docs/pt/transcription.md)

## Images

[English](docs/en/images.md) · [Español](docs/es/images.md) · [Português](docs/pt/images.md)

`image-generation.json` declares the OpenAI image endpoint, the default model and the **Image model** setting that overrides it. See the [OpenAI image generation guide](https://developers.openai.com/api/docs/guides/image-generation).

## Package a release candidate

From this checkout, use the Arrumo Plugin SDK packager with the adapter files
listed explicitly. Record the SDK commit and the SHA-256 printed by the tool.

```sh
python /path/to/plugin-sdk/tools/package_plugin.py . plugin.zip --include LICENSE --include README.md --include transcription.json --include transcription-timed.json --include image-generation.json
```
