# Trabalhando com Containers

## Criando contâineres

```
docker container run
```

> `-p <porta-de-saida>:<porta-de-entrada>`: Deixa como porta de acesso a porta de saida, para a porta de entrada (interna) do container. Por exemplo, `-p 8080:80` ao acessarmos a porta 8080, a porta 80 interna do container é devolvida.

> `-name <nome-do-container>`: Afilia o nome do container ao nome referenciado no comando.

> `-v <caminho-interno-do-host>:<caminho-do-interno-container>`: Faz um `link` entre o volume interno do container com o volume interno do host.

## Gerenciamento dos containeres

```
docker container ps
```

> Lista os processos relacionados ao docker

```
docker container ps -a
```

> Lista todos os processos (ativos e inativos) relacionados ao docker

```
docker container ls
docker container list
```

> Lista os contâineres docker

```
docker container logs <nome-do-contâiner>
```

> Exibe os logs do container referenciado no comando

```
docker container inspect <nome-do-container>
```

> Exibe um JSON contendo todas as características do contâiner

```
docker container exec <nome-do-container> <COMANDO>
```

> Executa o comando referenciado no comando dentro do container
