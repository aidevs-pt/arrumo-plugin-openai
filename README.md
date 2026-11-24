<p align="center">
  <img src="icon.svg" width="88" height="88" alt="">
</p>

<h1 align="center">OpenAI for Arrumo AI Video Editor</h1>

<p align="center">Transcription with timestamps and image generation from OpenAI.</p>

<p align="center">
  <a href="LICENSE"><img alt="License: AGPL-3.0" src="https://img.shields.io/badge/license-AGPL--3.0-2337B4"></a>
  <img alt="Bundled with Arrumo" src="https://img.shields.io/badge/bundled%20with-Arrumo-2337B4">
  <a href="https://www.aidevs.pt/tools/arrumo/docs/plugins/openai/images"><img alt="Docs in English, Spanish and Portuguese" src="https://img.shields.io/badge/docs-EN%20%C2%B7%20ES%20%C2%B7%20PT-111"></a>
</p>

This plugin ships with [Arrumo AI Video Editor](https://github.com/aidevs-pt/arrumo-video-editor), the free, open-source desktop app where an AI agent writes, designs, voices and cuts your videos and you approve every step. It comes installed with Arrumo; turn it on or off in **Settings › Plugins**.

## Guides

- **Images**: [English](https://www.aidevs.pt/tools/arrumo/docs/plugins/openai/images) · [Español](https://www.aidevs.pt/es/tools/arrumo/docs/plugins/openai/images) · [Português](https://www.aidevs.pt/pt/tools/arrumo/docs/plugins/openai/images)
- **Transcription and subtitles**: [English](https://www.aidevs.pt/tools/arrumo/docs/plugins/openai/transcription) · [Español](https://www.aidevs.pt/es/tools/arrumo/docs/plugins/openai/transcription) · [Português](https://www.aidevs.pt/pt/tools/arrumo/docs/plugins/openai/transcription)

## How it works

`image-generation.json` declares the OpenAI image endpoint, the default model and the **Image model** setting that overrides it. See the [OpenAI image generation guide](https://developers.openai.com/api/docs/guides/image-generation).

## Package a release candidate

From this checkout, use the Arrumo Plugin SDK packager with the adapter files
listed explicitly. Record the SDK commit and the SHA-256 printed by the tool.

```sh
python /path/to/plugin-sdk/tools/package_plugin.py . plugin.zip --include LICENSE --include README.md --include transcription.json --include transcription-timed.json --include image-generation.json
```

## Icon and trademarks

`icon.svg` shows OpenAI's logo so creators recognise the service this plugin connects to. OpenAI and the OpenAI logo are trademarks of OpenAI; the manifest's `iconNotice` says so wherever Arrumo shows the icon. The logo is not covered by this repository's license, and this plugin is not affiliated with or endorsed by OpenAI. The SVG is a square without rounded corners; Arrumo rounds it. If OpenAI asks, replace the logo with a generic symbol and remove `iconNotice`.

## Contributing

Contributions are welcome: read [CONTRIBUTING.md](CONTRIBUTING.md) and our [Code of Conduct](CODE_OF_CONDUCT.md). Report security problems privately as described in [SECURITY.md](SECURITY.md).

## License

Copyright © 2026 DEVS.AI UNIPESSOAL LDA. Licensed under the [GNU Affero General Public License v3.0](LICENSE). Built by [DEVS AI](https://aidevs.pt), who make custom AI solutions for companies.
