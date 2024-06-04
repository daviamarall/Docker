### Contêineres Docker

#### Criando e executando contêineres Docker
Para criar e executar um contêiner Docker, você pode usar o comando `docker run` seguido do nome da imagem que deseja utilizar. Por exemplo, para criar um contêiner Ubuntu e executar um shell interativo dentro dele, você pode fazer o seguinte:

```bash
docker run -it ubuntu bash
```

Isso criará um novo contêiner a partir da imagem Ubuntu e abrirá um shell bash interativo dentro dele. O parâmetro `-it` permite interação com o terminal.

#### Gerenciamento de contêineres
Para gerenciar contêineres Docker, você pode usar os seguintes comandos:

- `docker ps`: Lista os contêineres em execução.
- `docker stop`: Para a execução de um contêiner.
- `docker start`: Inicia um contêiner parado.
- `docker restart`: Reinicia um contêiner.
- `docker rm`: Remove um ou mais contêineres.
- `docker inspect`: Exibe informações detalhadas sobre um contêiner.

#### Redes e volumes em contêineres Docker
Os contêineres Docker podem ser conectados a redes específicas e podem ter volumes montados para armazenar dados persistentes. Por exemplo, para conectar um contêiner a uma rede específica, você pode usar o seguinte comando:

```bash
docker network connect minha-rede meu-container
```

Para criar um volume e montá-lo em um contêiner, você pode usar os comandos `docker volume create` e `docker run` com a opção `-v`. Por exemplo:

```bash
docker volume create meu-volume
docker run -d --name meu-container -v meu-volume:/app meu-imagem
```

Isso criará um volume chamado `meu-volume` e o montará no diretório `/app` do contêiner `meu-container`.

#### Compartilhamento de arquivos entre o host e o contêiner
Para compartilhar arquivos entre o host e o contêiner, você pode usar a opção `-v` do comando `docker run` para montar um diretório do host no contêiner. Por exemplo, para montar o diretório `/home/user/meu-diretorio` do host no diretório `/app` do contêiner, você pode usar o seguinte comando:

```bash
docker run -v /home/user/meu-diretorio:/app meu-imagem
```

Isso montará o diretório do host no contêiner e qualquer alteração feita em um local será refletida no outro.