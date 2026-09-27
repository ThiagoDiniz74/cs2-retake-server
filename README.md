# Servidor CS2 Retake em Docker

Documentação de um servidor de Counter-Strike 2 configurado em um contêiner Docker no meu ambiente Umbrel.

## Estado atual

- Contêiner `cs2-server` em execução com a imagem `joedwards32/cs2` no momento da verificação de 27/09/2026.
- Metamod e CounterStrikeSharp montados no contêiner; diretórios de configuração e plugin CS2Retake montados separadamente.
- Diretórios e arquivos do AstraSkins também aparecem como montagens. A captura confirma as montagens, mas não valida a execução do plugin.
- Tempo de congelamento ajustado para 5 segundos.
- Acompanhamento da disponibilidade pelo Uptime Kuma.
- Política Docker de reinício: `unless-stopped`.

> Os caminhos no host, as versões dos plugins e a configuração de portas ainda precisam ser conferidos antes de publicar instruções de instalação reproduzíveis.

## O que aprendi

- Instalação e operação de um servidor de jogo em Docker.
- Organização de arquivos persistentes e configuração de plugins.
- Ajustes de regras do modo Retake e verificação do funcionamento.
- Monitoramento da disponibilidade do serviço.

## Documentação

- [Arquitetura](docs/arquitetura.md): montagem dos componentes no contêiner.
- [Operação](docs/operacao.md): comandos básicos e comportamento da reinicialização.

Arquivos do jogo, plugins de terceiros e dados privados não fazem parte deste repositório.

## Segurança

Não publicar token GSLT, senha RCON, credenciais Steam, IP público, webhooks, arquivos `.env`, backups ou dumps de configuração. Consulte `SEGURANCA.md` antes do commit.
