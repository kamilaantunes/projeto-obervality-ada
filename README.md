<h1>Projeto-Observability</h1>

<h2>Projeto desenvolvido para a disciplina de Observability do curso de DevOps da Ada Tech + Núclea</h2>

Professor: Israel Nogueira

Alunas: Bruna Leal, Kamila Antunes e Ren Wrobleski

<h2>Objetivo</h2>

O objetivo do projeto é instrumentar uma aplicação de exemplo com as ferramentas de observabilidade:
Prometheus, AlertManager, Grafana e Graylog.


<h2>Tecnologias</h2>

    AWS
    Docker
    Docker Compose
    Prometheus
    Alertmanager
    Grafana
    Graylog

<h2>Execução</h2>

1) Instalação do Docker + Docker Compose

sudo apt update
sudo apt install
sudo apt install net-tools
curl -fsSL https://get.docker.com/ | sh
sudo curl -L https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose –-version

2) Executar git clone, copie a pasta para dentro do WSL e então execute:

cp -r /mnt/c/Users/NOMEDOUSUARIO/Downloads/PASTADOPROJETO ~/

Abra o diretório do projeto:

cd ~/PASTADOPROJETO

3) Execute o script setup.sh

Para automatizar a criação das aplicações python e executar o comando docker-compose up -d para criar e iniciar os containers

./setup.sh (ou caso precise de permissão sudo - sudo ./setup.sh )

4) Executar o docker-compose informando o arquivo .env

docker-compose -p projeto  --env-file .env up -d

Remover todos os containers

docker rm -f $(docker ps -a -q)

5) Acessar os containers com localhost:PORTADOCONTAINER
Para acessar o Grafana acesse seu navegador e digite: localhost:3000

Login: admin | Senha: admin

6) Para importar o Dashboard
 Dashboards New -> Import -> Upload dashboard JSON file Selecione o arquivo: dashboard.json -> Import

<h2>Evidências do Dashboard e do Graylog</h2>

