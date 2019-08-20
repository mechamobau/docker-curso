### Comparaçao entre máquinas virtuais (VM) e Containers _Docker_

Entrando um pouco dentro da estrutura _Docker_, veremos o porquê dele ser tão performático em relação a uma máquina virtual, assim como seu funcionamento. Na comparação abaixo, temos na esquerda a estrutura de uma máquina virtual e na direita a de um _Container Docker_.

|                                                    VM                                                     |                                        Container _Docker_                                        |
| :-------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------: |
| ![Arquitetura de uma VM](https://oer.gitlab.io/oer-on-oer-infrastructure/figures/OS/virtual-machines.png) | ![Arquitetura Docker](https://oer.gitlab.io/oer-on-oer-infrastructure/figures/OS/containers.png) |

Fonte: https://oer.gitlab.io/oer-on-oer-infrastructure/Docker.html

Como podemos ver _Docker_ compartilha de recurso do sistema operacional para funcionar, não precisando inicializar uma estrutura complexa para seu funcionamento.
