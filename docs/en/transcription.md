# Use OpenAI transcription in Arrumo

[Español](../es/transcription.md) · [Português](../pt/transcription.md)

In Arrumo Settings, open the OpenAI plugin and save an API key in its secret field. A workspace key takes precedence over the app default. Arrumo stores both in the system credential store.

Choose OpenAI in the transcription provider order for the workspace or when queueing a run. The run keeps that order. You can put another configured provider next in the list.

In delivery verification, choose **Generate subtitles** for the format you want. You can also turn on **Generate missing subtitles automatically** when queueing the draft. Both actions send audio for the selected output to the provider. Use **Import SRT** to supply your own subtitles instead.

## Check configuration from the CLI

Use these commands from a build that bundles the provider. The status command reports the configured scope without returning the key. The transcription command uploads the WAV and prints the normalized response.

```sh
arrumo-workspaces ./workspaces.sqlite plugin-credential-status openai 1 api-key
arrumo-workspaces ./workspaces.sqlite transcribe-wav 1 openai ./sample.wav
```

If subtitle generation fails, check that the output has audio, that the captured provider order includes a timed adapter, and that the credential is still configured.
