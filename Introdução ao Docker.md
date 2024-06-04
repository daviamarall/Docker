### Introdução ao Docker

#### O que é Docker?
Docker é uma plataforma de software que permite a criação, o teste e a implantação de aplicativos em contêineres. Os contêineres permitem que um desenvolvedor empacote um aplicativo com todas as partes necessárias, como bibliotecas e outras dependências, e o envie como uma única unidade.

#### Por que usar Docker?
- **Portabilidade**: Os contêineres Docker podem ser executados em qualquer lugar, desde o ambiente de desenvolvimento até a produção, garantindo consistência.
- **Eficiência**: Os contêineres compartilham o sistema operacional subjacente, o que os torna mais leves que as máquinas virtuais.
- **Isolamento**: Os contêineres fornecem isolamento de recursos, garantindo que um aplicativo em um contêiner não interfira em outro.

#### Instalação do Docker
A instalação do Docker varia dependendo do sistema operacional. Para sistemas Linux, você pode instalar o Docker a partir dos repositórios de pacotes. Para Windows e macOS, é necessário baixar e instalar o Docker Desktop.

#### Comandos básicos do Docker
- `docker pull`: Baixa uma imagem do Docker Hub.
- `docker run`: Cria e inicia um contêiner a partir de uma imagem.
- `docker ps`: Lista os contêineres em execução.
- `docker stop`: Para a execução de um contêiner.
- `docker rm`: Remove um contêiner.
- `docker rmi`: Remove uma imagem.

Exemplo de uso:
```bash
docker pull ubuntu:latest
docker run -it ubuntu bash
```

Neste exemplo, o primeiro comando baixa a imagem mais recente do Ubuntu do Docker Hub. O segundo comando cria um novo contêiner a partir dessa imagem e abre um shell bash interativo dentro dele.