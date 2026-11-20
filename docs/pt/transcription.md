# Usa a transcrição do OpenAI no Arrumo

[English](../en/transcription.md) · [Español](../es/transcription.md)

Nas definições do Arrumo, abre o plugin do OpenAI e guarda uma chave de API no campo de segredo. A chave do espaço de trabalho tem prioridade sobre a chave predefinida da aplicação. O Arrumo guarda ambas no armazenamento de credenciais do sistema.

Escolhe o OpenAI na ordem de fornecedores de transcrição do espaço de trabalho ou ao colocar uma execução na fila. A execução mantém essa ordem. Podes colocar outro fornecedor configurado a seguir.

Na verificação da entrega, escolhe **Gerar legendas** para o formato que queres. Também podes ativar **Gerar automaticamente as legendas em falta** ao colocar o rascunho na fila. As duas ações enviam para o fornecedor o áudio da saída selecionada. Usa **Importar SRT** para forneceres as tuas próprias legendas.

## Verifica a configuração na CLI

Usa estes comandos numa compilação que inclua o fornecedor. O comando de estado indica o âmbito configurado sem devolver a chave. O comando de transcrição envia o WAV e apresenta a resposta normalizada.

```sh
arrumo-workspaces ./workspaces.sqlite plugin-credential-status openai 1 api-key
arrumo-workspaces ./workspaces.sqlite transcribe-wav 1 openai ./sample.wav
```

Se a geração falhar, confirma que a saída tem áudio, que a ordem de fornecedores guardada inclui um adaptador com marcas temporais e que a credencial continua configurada.
