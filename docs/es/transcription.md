# Usa la transcripción de OpenAI en Arrumo

[English](../en/transcription.md) · [Português](../pt/transcription.md)

En los ajustes de Arrumo, abre el plugin de OpenAI y guarda una clave de API en su campo secreto. La clave del espacio de trabajo tiene prioridad sobre la clave predeterminada de la aplicación. Arrumo guarda ambas en el almacén de credenciales del sistema.

Elige OpenAI en el orden de proveedores de transcripción del espacio de trabajo o al añadir un proceso a la cola. El proceso conserva ese orden. Puedes colocar otro proveedor configurado después.

Al verificar la entrega, elige **Generar subtítulos** para el formato que quieras. También puedes activar **Generar automáticamente los subtítulos que falten** al poner el borrador en cola. Ambas acciones envían al proveedor el audio de la salida seleccionada. Usa **Importar SRT** para añadir tus propios subtítulos.

## Comprueba la configuración desde la CLI

Usa estos comandos en una compilación que incluya el proveedor. El comando de estado indica el ámbito configurado sin devolver la clave. El de transcripción sube el WAV y muestra la respuesta normalizada.

```sh
arrumo-workspaces ./workspaces.sqlite plugin-credential-status openai 1 api-key
arrumo-workspaces ./workspaces.sqlite transcribe-wav 1 openai ./sample.wav
```

Si falla la generación, comprueba que la salida tenga audio, que el orden de proveedores guardado incluya un adaptador con marcas de tiempo y que la credencial siga configurada.
