# Entrega Trabalho Individual 2020-1
## O que foi feito
1. Containerização :heavy_check_mark:
2. Integração contínua :heavy_check_mark:
3. Deploy contínuo (Extra) :x:

## Ferramentas utilizadas
### Containerização
* Docker
* docker-compose

### Integração Contínua e controle de qualidade
* GitHub Actions
* Sonar Cloud

## Como utilizar
### Docker
1. ```make build```
2. ```make run```
   
### Integração Contínua
Os passos realizados para [integração contínua](https://github.com/lucasdutraf/Trabalho-Individual-2020-1/actions) para ambos os módulos do projeto foram:
* Build
* Instalar dependências
* Executar os testes
* Coleta de métricas (Sonar Cloud)