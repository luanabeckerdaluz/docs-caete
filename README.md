# Documentação HARMONIZE-Brazil

**Este repositório possui um **[Github Actions](.github/workflows/deploy-docs.yml)** configurado para fazer deploy automático no repositório https://github.com/Harmonize-Brazil/Harmonize-Brazil.github.io.**

**Qualquer commit na main deste repositório acionará o build e deploy!**

_______________________________________________________________

## Configurando o Build e deploy automático

O workflow criado para o Github Pages pode ser acessado no arquivo `.github/workflows/deploy-docs.yml`. O pipeline dele utiliza uma imagem base com Python 10, instala os pacotes necessários com base no arquivo `requirements.txt` deste repositório, realiza o build da documentação sphinx utilizando o comando `make html` e depois publica na branch `gh-pages`.

Entretanto, a permissão para escrita no repositório `Harmonize-Brazil.github.io` precisou ser configurada! Para isso, foram utilizadas **deploy keys**. Uma deploy key é a configuração de uma chave SSH onde um repositório consegue acessar o outro. Utilize o passo a passo a seguir para criar e configurar a deploy key neste repositório e no repositório de destino:

- **1)** Crie uma chave ssh localmente utilizando o comando `ssh-keygen -t ed25519 -C "github-actions-deploy" -f deploy_key`.

- **2)** Serão gerados 2 arquivos, um chamado `deploy_key.pub` (chave pública) e outro chamado `deploy_key` (chave privada).

- **3)** Acesse o repositoŕio `Harmonize-Brazil.github.io`, vá em `Settings` -> `Deploy keys`, e clique em `Add deploy key`. Sete um nome qualquer (ex.: `Github-Pages`) e cole na chave o conteúdo do arquivo `deploy_key.pub`. Será somente 1 linha.

- **4)** Acesse este repositoŕio `docs`, vá em `Settings` -> `Secrets and variables` -> `Actions`, então clique em `New repository secret`. O nome precisa ser **obrigatoriamente** `DEPLOY_KEY`. E o secret será todo o conteúdo do arquivo `deploy_key`.

Após isso, este repositório `docs` conseguirá escrever no repositório `Harmonize-Brazil.github.io`!

_______________________________________________________________

## Como fazer build localmente

Para realizar o build na sua máquina, temos que criar um ambiente conda e instalar nossos pacotes descritos em `requirements.txt`. Alternativamente, você pode criar um venv ao invés de utilizar o conda.

```bash
conda create -c conda-forge --yes --name sphinx python=3.10
conda activate sphinx
pip install -r requirements.txt
```

Após ter o ambiente criado e ativo, utilize o seguinte comando para buildar:

```bash
make html
```

Após buildado, acesse o site abrindo o arquivo **_build/html/index.html**.