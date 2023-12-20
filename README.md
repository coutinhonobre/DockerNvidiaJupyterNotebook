# TensorFlow GPU com Jupyter Notebook - Docker

Este projeto configura um ambiente Docker contendo TensorFlow com suporte a GPU e Jupyter Notebook, facilitando o desenvolvimento e a execução de projetos de aprendizado de máquina.

## Pré-requisitos

- Docker instalado.
- Docker Compose (para usar o arquivo `docker-compose.yaml`).
- Driver da NVIDIA e NVIDIA Docker (para suporte a GPU).

## Configuração

O projeto consiste em um Dockerfile que configura um ambiente com TensorFlow e Jupyter Notebook, e um arquivo `docker-compose.yaml` para facilitar o gerenciamento do container.

### Variáveis de Ambiente

- `JUPYTER_TOKEN`: Token fixo para acessar o Jupyter Notebook. (Padrão: `abcdef1234567890`)
- `JUPYTER_PASSWORD`: Senha fixa para acessar o Jupyter Notebook. (Padrão: `senha123`)

## Instruções de Uso

1. **Construir o Container**

   Para construir o container usando o Dockerfile, execute:

   ```bash
   docker build -t meu-tensorflow-gpu-jupyter .
   ```

   Com o Docker Compose, use:

   ```bash
   docker-compose up --build
   ```
2. **Executar o Container**

   Após a construção, inicie o container com:

   ```bash
   docker run -p 8888:8888 meu-tensorflow-gpu-jupyter
   ```

   Ou, se estiver usando o Docker Compose:

   ```bash
   docker-compose up
   ```
3. **Acessar Jupyter Notebook**

   Abra o navegador e acesse `http://localhost:8888`. Use o token `abcdef1234567890` ou a senha `senha123` para entrar.

## Notas Adicionais

- O projeto está configurado para usar GPU. Certifique-se de que seu sistema suporte e esteja configurado corretamente para isso.
- As variáveis de ambiente podem ser ajustadas conforme necessário. No entanto, não compartilhe valores sensíveis em repositórios públicos.
- Para mudar a configuração do projeto, edite o Dockerfile ou o arquivo `docker-compose.yaml`.

## Suporte e Contribuições

Para suporte, dúvidas ou contribuições, por favor, abra uma issue no repositório do projeto.
# DockerNvidiaJupyterNotebook
