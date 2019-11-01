# Docs Features

## Guia para implantação do deploy contínuo do Mkdocs
### Mkdocs + CircleCI

Para realizar o deploy manual no mkdocs, no diretório onde estiver mkdocs.yml, basta rodar o comando:

```
  mkdocs gh-deploy  
```
Para mais informações, [Deploy no Mkdocs](https://www.mkdocs.org/user-guide/deploying-your-docs/) 

Para automatizar o processo utilizando nossa CI, segue o arquivo de configuração [config.yml](https://github.com/thiagorpereira/DocsFeatures/blob/master/.circleci/config.yml)

### Obs:
Como é necessaŕio uma autentificação do github para realizar o deploy, é necessaŕio gerar uma [SSH key](https://help.github.com/en/enterprise/2.17/user/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

Será gerada uma chave publica e outra privada;
* A chave privada deve ser inserida no CircleCI do projeto e então será gerado um fingersprint que será utilizado no config.yml; 
* A chave publica, deve-se realizar um upload da mesma no Deploy Keys no GitHub do projeto para de fato ocorrer a conexão



