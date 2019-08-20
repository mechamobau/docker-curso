# Conceitos básicos de _Docker_

Começando nossos estudos em _Docker_, precisamos primeiro dominar os conceitos básicos da ferramenta, afinal: O que é o _Docker_? Para o que ele serve? Qual a diferença entre um `Container` _Docker_ e uma VM (_Virtual Machine_)? Estas e outras perguntas estão listadas logo abaixo.

## O que é o _Docker_?

Antes de tudo, o _Docker_ é um sistema de virtualização, porém não é baseado em máquinas virtuais. E essa diferença vem pelo fato do _Docker_ necessitar de uma máquina _Host_, consumindo os recursos de seu hospedeiro, tais como: _kernel_, _hardware_, binários, bibliotecas, entre outros recursos necessários para a utilização do _Docker_.

Portanto, o que podemos dizer é que o _Docker_ é uma _engine_ de virtualização de `Containers`.

## O que é um `Container`?

Um `Container` é um processo separado do sistema hospedeiro e através dele podemos inicializar outros processos internamente. É como se o `Container` fosse uma interface diferente de execução do Sistema Operacional, onde tudo o que acontece nele fique de fora do que está contido no `Container`, isolado da máquina _Host_.

## Para o que serve o Docker?

Dentro `Container` podemos ter um sistema de arquivos segregado do sistema hospedeiro, impedindo de eventuais falhas nos processos (e suas dependências) que estejam rodando no `Container` por não estarem compartilhando com o sistema hospedeiro.

Assim sendo, o `Docker` é um ótimo aliado para a configuração de ambientes de desenvolvimento (e de produção).

## Qual a diferença entre um `Container` _Docker_ e uma VM (_Virtual Machine_)?

O que torna o `Container` uma ótima ferramenta para o desenvolvimento e uma grande de diferença entre as VMs é que além de estar isolado do sistema hospedeiro, o `Container` é mais leve e consome menos memória que uma máquina virtual, pois todas as necessidades que o `Container` tem para sua execução já são atendidas por utilizar binários e bibliotecas da "máquina-mãe", digamos assim.

## Qual a arquitetura por detrás do _Docker_?

O _Docker_ se baseia nos serviços LXC (_Linux Containers_) para virtualização. Isto quer dizer que, os _containers_ que são iniciados pelo _Docker_, são iniciados baseados em sistemas _Linux_ em seu interior, ou seja, diferente de uma virtualização convencional onde podemos, por exemplo, instalar um Sistema Operacional Windows em um Linux, ou vice-versa, no Docker isto não é possível pela tecnologia utilizada em seu interior.

E isto não é ruim, pois a maioria dos servidores que hospedam sites e serviços online na web rodam alguma distro `Linux`, ou seja, os `containers` possuem um performance garantida.

## O que torna o `Docker` tão popular?

Além do fato de ser escrito em Go, linguagem esta que possui uma performance maior em `multi-thread` e sistemas paralelos e de ser baseado em virtualização baseado em Sofware (onde o sistema _Docker_ aloca os processos e serviços necessários), o `Docker` é uma ferramenta `open-source` onde a comunidade contribui com o desenvolvimento da plataforma.

E além dos citados acima, o _Container_ e o _Host_ compartilham o _Kernel_ do Sistemas Operacional, trazendo uma performance e garantindo um isolamento satisfatório de suas interfaces internas de processamento, podendo por exemplo determinar a quantidade núcleos que o _Container_ consumirá, o quanto o _Container_ pode consumir de rede, de memória RAM e entre outros recursos do _Host_.
