# FFX Encoder 3

Aplicativo para Windows voltado à organização, conversão e padronização de
arquivos de vídeo com FFmpeg integrado.

## Download

Baixe o instalador na página de [Releases](https://github.com/tecmabeinformatica/ffx-encoder-releases/releases/latest).

Versão atual: **3.0.1**

Arquivo: `FFX.Encoder.3.0.1.Instalador.exe`

## Aceleração por GPU

O FFX Encoder seleciona automaticamente o encoder disponível para o codec
escolhido, sem exigir uma configuração adicional:

- NVIDIA: NVENC.
- Intel: Quick Sync Video (QSV).
- AMD Radeon: AMF.
- CPU: utilizada automaticamente quando não existe encoder compatível para o
  codec selecionado.

A aceleração depende dos codecs oferecidos por cada placa. Por exemplo, a AMD
Radeon RX 5700 codifica H.264/AVC e H.265/HEVC por AMF, mas não possui encoder
AV1 por hardware; nesse caso, AV1 é processado pela CPU.

No Gerenciador de Tarefas, algumas Radeon mostram o uso do encoder dedicado no
gráfico **Video Codec**, em vez de **Video Encode**. A CPU também pode trabalhar
durante a decodificação, aplicação de filtros, áudio e preparação dos quadros.

## Requisitos

- Windows 10 ou Windows 11, 64 bits.
- Espaço livre para instalação e processamento dos vídeos.
- Conexão com a internet para os recursos do TMDb.

## Instalação

1. Baixe o instalador pela página de Releases.
2. Execute o arquivo baixado.
3. Escolha português, inglês ou espanhol e siga as instruções do instalador.

O instalador possui interface gráfica moderna, cria um desinstalador nativo e
oferece atalhos e integração com o menu de contexto do Windows. O aplicativo
inclui os componentes necessários para executar o FFmpeg.

Em instalações novas, o caminho padrão é `C:\Program Files\FFX Apps\FFX Encoder 3`.
Cada aplicativo FFX deve ocupar sua própria subpasta em `FFX Apps`; a
desinstalação do Encoder não remove os outros aplicativos.

Para usar capas e metadados, é necessária uma chave da API do TMDb. Ela pode
ser solicitada gratuitamente após o cadastro no site oficial do TMDb. O
aplicativo funciona sem a chave, mas alguns recursos ficam indisponíveis.

## Integridade da versão 3.0.1

SHA-256:

```text
962C4B183F7374756EAF08C05B7E577216F24893E54E866DE0ED64CA753C8AB3
```

## Observação de segurança

O Windows pode exibir um aviso do SmartScreen para aplicativos novos ou sem
assinatura digital reconhecida. Confirme que o arquivo foi obtido deste
repositório e compare o SHA-256 antes de executá-lo.

## Observação importante
O FFX Encoder é uma ferramenta de organização e processamento de arquivos existentes no
computador do usuário. Use apenas com arquivos sobre os quais você tenha direito de uso. O software
não é destinado a burlar proteções, obter conteúdo ilegal ou substituir obrigações legais do usuário.
