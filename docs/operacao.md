# Operação básica

Executar no host Umbrel, onde o contêiner se chama `cs2-server`:

```bash
sudo docker ps --filter name=cs2-server
sudo docker stop cs2-server
sudo docker start cs2-server
```

`stop` e `start` preservam o contêiner e suas montagens. A política `unless-stopped` reinicia o contêiner após falha ou reinício do Docker, exceto quando ele foi parado manualmente e permanece marcado como parado.

As montagens `bind` apontam para dados no host. Antes de atualizar a imagem ou recriar o contêiner, localizar as origens, conferir os arquivos e fazer backup dos dados persistentes. **Não usar `docker rm` nem `docker compose down -v` como parte deste procedimento.**

Para conferir a política de reinício sem expor credenciais:

```bash
sudo docker inspect --format '{{.HostConfig.RestartPolicy.Name}}' cs2-server
```

Os comandos de instalação e atualização serão adicionados após confirmação da configuração real, com todos os segredos substituídos por exemplos.
