# Use as imagens do OpenAI no Arrumo

[English](../en/images.md) · [Español](../es/images.md)

Nas definições do Arrumo, abra o plugin do OpenAI e guarde uma chave de API no campo secreto. A chave do espaço de trabalho tem prioridade sobre a da aplicação; o Arrumo guarda ambas no cofre de credenciais do sistema e nunca as mostra aos agentes.

Quando um formato pede miniaturas, o agente da execução escreve uma instrução por miniatura e o Arrumo pede-as aos fornecedores de imagens pela ordem guardada na execução. O OpenAI é ignorado se não tiver chave. As miniaturas ficam guardadas como recursos do espaço de trabalho e aguardam a sua revisão com os títulos e descrições.

## Escolha o modelo

O plugin usa `gpt-image-2.5-flare` por omissão. Para usar um modelo mais recente, defina **Modelo de imagem** nas definições do plugin para a aplicação ou um espaço de trabalho. Deixe vazio para seguir o modelo predefinido do plugin.
