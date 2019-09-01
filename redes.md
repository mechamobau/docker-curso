# Redes

No Docker é possível configurar a conexão (ou a falta dela) entre os contêineres, através disso podemos determinar, por exemplo, que um contêiner de Garbage Collector não consiga conectar-se ao servidor de aplicação, já que não é necessário. Existem quatro tipos de topologias de rede no Docker onde podemos basear nossa configuração, elas são: 

1. None Network
2. Bridge Network (Padrão)
3. Host Network
4. Overlay Network (Swarm)

## 1. None Network
Na rede None, o contêiner é criado apenas com a rede padrão do sistema, ou seja, a rede de loopback onde o contêiner consegue a apenas conectar-se entre si. Este tipo de rede é aconselhado para contêineres que não dependam de conexão, ou ainda, conexão com a internet para sua utilização; Sendo apenas utilizado para, como no exemplo que introduz o capítulo, tarefas que utilizem

`docker container run -d` **--net none** `debian`

## 2. Bridge Network
![Image](https://docs.docker.com/v17.09/engine/userguide/networking/images/bridge_network.png) 

Docker Inc. &copy; 2019
  
O modelo de rede Brigde (ponte), como o seu próprio nome descreve, cria uma interface de conexão que de uma ponta traz o Host e de outra os contêineres Docker. Este modelo é o padrão em toda criação de contêineres, sendo o mais adotado.

Vale ressaltar que podemos criar várias redes bridge, podendo além conectá-las entre si para compartilhar contêineres de diferentes redes. Por exemplo, para o desenvolvimento de microserviços em uma rede podemos ter um sistema composto de diversos microserviços e em outra um monolito, podendo conectá-los caso necessário.

## 3. Host Network
Mas e quando precisamos ter acesso ao host, por exemplo para utilizar as interfaces de conexão Wi-Fi do host disponibilizando o acesso para um determinado contêiner? Para isso utilizamos o tipo Host de rede, onde a camada Bridge é removida, dando acesso ao Host, apesar de ser mais rápida (para conexão às redes WAN) acaba sendo mais inseguro.

## 4. Overlay Network
O tipo de rede Overlay serve para clusterização de ambientes, ou seja, onde mais de um host esteja dentro da conexão servindo ao mesmo propósito, vale ressaltar que este modo está disponível apenas para a versão Swarm do Docker, versão para clusters da ferramenta.