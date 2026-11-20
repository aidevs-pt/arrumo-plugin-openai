# Use OpenAI images in Arrumo

[Español](../es/images.md) · [Português](../pt/images.md)

In Arrumo's settings, open the OpenAI plugin and save an API key in its secret field. A workspace key takes precedence over the app default; Arrumo keeps both in the system credential store and never shows them to agents.

When a format asks for thumbnails, the run's agent writes one image prompt per thumbnail and Arrumo asks the image providers in the run's captured order. OpenAI is skipped when it has no key. Generated thumbnails are saved as workspace assets and wait for your review with the titles and descriptions.

## Choose the model

The plugin uses `gpt-image-2.5-flare` by default. To use a newer model, set **Image model** in the plugin's settings for the app or a workspace. Leave it empty to follow the plugin's default.
