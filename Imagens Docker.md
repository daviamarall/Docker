### Imagens Docker

#### O que são imagens Docker?
Uma imagem Docker é um modelo de somente leitura que contém um conjunto de instruções necessárias para criar um contêiner Docker. Ela inclui o sistema operacional, bibliotecas, dependências e o próprio aplicativo. As imagens são usadas como base para criar contêineres em tempo de execução.

#### Docker Hub e repositórios de imagens
O Docker Hub é um serviço de registro de imagens Docker públicas e privadas. Ele permite que os desenvolvedores compartilhem e distribuam suas imagens Docker. Além do Docker Hub, existem outros repositórios públicos e privados disponíveis para armazenamento e compartilhamento de imagens.

#### Criando e modificando imagens Docker
Para criar uma imagem Docker, é possível usar o comando `docker commit` para salvar as alterações feitas em um contêiner. No entanto, a prática recomendada é usar um Dockerfile, que é um arquivo de texto com instruções que definem como a imagem deve ser construída. O Dockerfile é mais eficiente e reproduzível do que o `docker commit`.

Exemplo de Dockerfile para criar uma imagem simples com um servidor web nginx:
```Dockerfile
# Use a imagem oficial do nginx como base
FROM nginx:latest

# Copie o arquivo index.html para o diretório de documentos do nginx
COPY index.html /usr/share/nginx/html/
```

#### Dockerfile: criação de imagens personalizadas
O Dockerfile é um arquivo de texto que contém uma lista de instruções para a construção de uma imagem Docker. Cada instrução no Dockerfile cria uma nova camada na imagem. As instruções comuns incluem `FROM`, `COPY`, `RUN`, `EXPOSE` e `CMD`.

Exemplo de uso do Dockerfile:
1. Crie um arquivo chamado `Dockerfile` com o conteúdo acima.
2. Crie um arquivo `index.html` com algum conteúdo.
3. Execute o seguinte comando para construir a imagem:
   ```bash
   docker build -t meu-nginx .
   ```
4. Execute o seguinte comando para iniciar um contêiner com base na imagem criada:
   ```bash
   docker run -d -p 80:80 meu-nginx
   ```
   Agora você pode acessar o servidor web nginx em `http://localhost` e verá o conteúdo do arquivo `index.html`.