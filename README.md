# conversao-distancia

## Clonando repositorio

-- Primeiro clone este repositorio para sua maquina

## Requisitos
 - Docker

## Executando o projeto

Acesse o diretorio do projeto e siga os passos abaixo:

1. No seu terminal, navegue até o diretório onde está o seu Dockerfile e execute o comando para construir a imagem Docker:

```bash
docker build -t convercao-distancia .

```
2. Agora execute o Container com comando **docker run**:
```bash
docker run -d -p 8181:5000 conversao-distancia

```
- **docker run**: Executa um container a partir da imagem especificada.
- **-p 8181:5000**: Mapeia a porta 5000 do container para a porta 8181 do seu sistema local (isso lhe permite acessar a aplicação via navagador) 
- **convesao-distancia**: a imagem que você criou anteriormente.

3. **Acessando a Aplicação**:
- Acesse a url: [localhost:8181](http://localhost:8181)

## Outros comandos essenciais

1. Listar todos os containers em execução:

```bash
docker ps

```
 -  Listar todos os containers (em execução ou não)
```bash
docker ps -a

```

2. Para fazer o stop, container, utilize com comando **docker stop**:
```bash
docker stop <container_id>

```
- Substitua <container_id> pelo ID do seu container

3. **Para verificar as imagens Docker que você criou, execute o comando**:

```bash
docker images

```

### Configuração do Ambiente

  <p>Se ainda não tem Dcoker instalado, faça configuração de acordo com seu ambiente.</p>

#### Instalação no Ubuntu

##### 1. Atualizar o Sistema
Antes de instalar o Docker, atualize o sistema e instale as dependências necessárias:

```bash
sudo apt-get update
sudo apt-get install apt-transport-https ca-certificates curl software-properties-common

```
##### 2. Instalando o Docker

Adicione a chave oficial do Docker ao repositório APT:

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

```

##### Adicione o repositório Docker:

```bash
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```
##### Atualize o índice de pacotes e instale o Docker:

```bash
sudo apt-get update
sudo apt-get install docker-ce
```

#### 3. Verifique a Instalação

Verifique se o Docker foi instalado corretamente:

```bash
sudo docker --version

```

Para permitir que o Docker seja executado sem sudo (opcional), adicione seu usuário ao grupo docker:

```bash
sudo usermod -aG docker $USER

```
Depois disso, saia da sessão e faça login novamente ou use newgrp docker para aplicar as alterações.

#### Instalação no Windows

##### 1. Baixar o Docker Desktop

- Acesse o site oficial do Docker para Windows.
- Baixe o Docker Desktop for Windows - [Docker Desktop](https://www.docker.com/products/docker-desktop/).
- Execute o instalador e siga as instruções para completar a instalação.
- Após a instalação, abra o Docker Desktop e aguarde até que o Docker esteja em execução.

##### 2. Verificar a Instalação

Abra o Prompt de Comando ou PowerShell e digite:

```bash
docker --version

```
Isso deve exibir a versão do Docker instalada.

##### 3. Habilite o WSL 2 (Windows Subsystem for Linux)
Para usar o Docker com WSL 2, certifique-se de que o WSL 2 está instalado. Se não estiver, o Docker Desktop irá guiá-lo para a instalação do WSL 2 durante o processo de instalação.