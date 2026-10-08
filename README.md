# FFX Encoder 3

Aplicativo para Windows voltado à organização, conversão e padronização de
arquivos de vídeo e áudio com FFmpeg integrado.

## Download

Baixe o instalador na página de [Releases](https://github.com/tecmabeinformatica/ffx-encoder-releases/releases/latest).

Versão atual: **3.0.5**

Arquivo: `FFX.Encoder.3.0.5.Instalador.exe`

## Novidades da versão 3.0.5

- Novo Modo Áudio, ativado automaticamente quando a pasta contém somente
  arquivos de áudio.
- Interface adaptada para liberar conversão, tratamento Podcast e ferramentas
  compatíveis com áudio.
- Conversão para AAC/M4A, MP3, Opus, FLAC e WAV, com opção de manter o formato
  original, escolher canais e normalizar o volume.
- Tratamento Podcast direto em arquivos de áudio, preservando metadados e com
  escolha do formato de saída.
- Pastas mistas continuam no Modo Vídeo e separam os áudios avulsos para evitar
  falhas de processamento.

## Novidades da versão 3.0.4

- Ícones vetoriais compatíveis com Windows 10 e Windows 11, sem depender da
  disponibilidade da fonte Segoe Fluent Icons.
- Conversão de vídeos HEVC HDR10 de 10 bits para H.264 com adaptação para SDR
  e formato de pixels compatível.
- Fallback automático para processamento pela CPU quando o encoder da GPU não
  consegue concluir a conversão.
- Verificação das faixas antes da troca de contêiner. Quando existem áudios,
  legendas, capas ou anexos incompatíveis com o formato de destino, o usuário
  pode cancelar ou continuar removendo somente esses itens; o vídeo e as
  demais faixas compatíveis continuam sendo processados.
- Mensagens detalhadas com o erro real retornado pelo FFmpeg.

## Novidades da versão 3.0.3

- Correção do modo inteligente para gravar os metadados obtidos do TMDb.
- Inclusão de título, descrição, sinopse e data ou ano nos arquivos processados.
- Uso dos dados específicos de cada episódio quando disponíveis.

## Novidades da versão 3.0.2

- Limpeza de metadados textuais sem recodificação, disponível também nas
  ferramentas em lote para processar séries e temporadas inteiras.
- Tratamento Podcast para reduzir ruído, melhorar a presença da voz, nivelar
  falas, comprimir a dinâmica e normalizar o volume final.
- Escolha do codec, bitrate, canais e contêiner na função Podcast.
- Opção para manter o contêiner original ou gerar arquivos MKV ou MP4; somente
  o áudio é recodificado durante esse tratamento.

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

## Integridade da versão 3.0.5

SHA-256:

```text
05EBF65F2AB8FE1FFFF31554C649ACBD34165B6DCCC5F877E690F4D4C9CA4FB1
```

## Observação de segurança

O Windows pode exibir um aviso do SmartScreen para aplicativos novos ou sem
assinatura digital reconhecida. Confirme que o arquivo foi obtido deste
repositório e compare o SHA-256 antes de executá-lo.

## Observação importante
O FFX Encoder é uma ferramenta de organização e processamento de arquivos existentes no
computador do usuário. Use apenas com arquivos sobre os quais você tenha direito de uso. O software
não é destinado a burlar proteções, obter conteúdo ilegal ou substituir obrigações legais do usuário.
