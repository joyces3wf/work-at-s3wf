# work-at-s3wf
Para a vaga de desenvolvedor criamos um simples teste para verificar a fluência de programação. O teste e as instruções podem ser encontrados abaixo:

## Trabalhe na S3WF

A S3WF é uma fábrica de software que tem como foco principal o desenvolvimento de aplicações web.
A nossa equipe é composta por pessoas que amam o que fazem. Sempre estamos à procura de novos talentos para fazer parte equipe.
Logo abaixo está a descrição de um pequeno teste para avaliar se o candidato possui algumas das habilidades básicas para trabalhar conosco.

# Pré-requisitos do sistema

- A versão do php terá que ser php 7.0.

- O sistema deverá ser desenvolvido em ambiente Linux. 

- O banco de dados você poderá usar Mysql ou Postgres.


# Desenvolvendo aplicativo

Você deve implementar um aplicativo em php que irá agendar uma tarefa para ser executada em um segundo momento, antes disso teremos que logar no aplicativo.

# Requisitos Login

 - Tela de Login e senha;
 
 - Apresentar os possíveis erros se não conseguir logar;
 
 - Usar javascript + jquery ou qualquer outro framework de domínio para tratar os erros na tela ( da forma mais simples que encontrar);
 
 - Os envios dos dados do login e senha tem que ser feitos com Ajax ( importante );
 
 - Os retornos de erro terão que ser feitos com Ajax retornando Json ( importante );
 
 - Quando logar com sucesso criará uma sessão para que o usuário permaneça na tela de admin.

# Requisitos Ambiente admin , após logar 

 - O ambiente administrativo é simples só terá mesmo nossa tabela em HTML contendo uma lista das tarefas a serem executadas e mais nada;
 
 - Nossa tabela em HTML terá 08  colunas e 2 linhas;
 
 - Data inicial, Hora Inicial, Data Final, Hora Final, Tamanho do csv, Nome Tarefa, Download, Ação;
 
 - A coluna ação é o "Gerar Csv";
 
 - A coluna Download terá um link "baixar" onde ele irá dar download do arquivo.
  
# Criar o layout acima na tela do admin

- O button "gerar csv" irá disparar um AJAX para que possa agendar a execução;

- Após disparar o ajax, o programa irá setar que a tarefa selecionada está pronta para ser executada;

- E o button na tela da ação ficará desativado enquanto não finaliza a execução.

# Requisitos Ambiente admin , após clicar em “gerar csv”

- Quando clicar em "gerar csv" na verdade o seu AJAX irá enviar para o PHP qual tarefa terá que ser executada e mais nada, o retorno é feito em json sucesso ou erro, e uma ação para desativar o button ou enviar uma mensagem para que o button altere o seu valor para “em andamento”;

- O programa PHP irá setar em uma tabela esta ação e mais nada, armazenar qual tarefa será executada, data inicio e hora inicio e um status de execução;

- Os status podem ser: 1 => pronto para executar, 2 => em andamento , 3 => erro, 4 => concluido;

- Caso faço F5 ou atualizo a tela o programa irá entender que já foi clicado na ação e o mesmo fica desativado ou avisar que está “em andamento” a execução da tarefa.

# Requisitos programa script para gerar csv

- Você irá desenvolver um script que irá rodar em bash, ou seja php -q programa.php;

- O programa bash irá ler sua tabela onde consta as tarefas a serem executadas;

- O programa irá gerar um arquivo .csv;

- O arquivo csv tem o seguinte layout: id;nome;matricula

- Faça uma função ou método para criar este arquivo com nomes, ids e matriculas fictícias até 1000 linhas, colocar um sleep de 5 segundos antes de gerar o arquivo;

- Assim que o programa acabar de gerar o csv ele deverá setar a base com as informações;

- Tratar a possibilidade do script ser executado simultaneamente e conflitar com os registros.

# Criação Banco de dados e tabelas

- Criar uma banco de dados para aplicação no Mysql ou Postgres;

- Usar o PDO do PHP e nada mais;

- Tabelas a serem criadas ( app_login, app_tarefas, app_agedamento_de_tarefas ).

# Fim de nosso programa

- Após finalizado nosso script php, ao dar F5 na tela ele apresentará o link para baixar o arquivo, e as informações de data e tamanho do arquivo;

- O button fica ativo novamente para que o usuário possa repetir o processo.

# Entrega do programa e organização do código

- Não utilize framework em PHP, queremos perceber seu conhecimento da linguagem sem frameworks;

- o programa poderá ser executado em nginx, apache ou por exemplo: php -S localhost:9001 -t public;

- A organização do fonte poderá ser feita da melhor forma que encontrar, exemplo de estrutura:

```sh
      index.php 
      src/class (classes do sistema)
      src/config (configs de banco por exemplo)
      cron/ (script que irá executar em bash ou linha de comando)
      scripts-sql/ (os exports das tabelas criadas e seus inserts os dumps)
      img
      css
      js
```
- Você irá dar um Fork no repositório e fazer um Pull request

- Qualquer dúvida abra um Issue


# Recomendações

- Escreva testes unitários; 

- Não preocupe-se com o código perfeito, lembre-se é somente um teste;

- Crie Classes para reutilização e melhor organização do seu código;

- Faça o melhor que conseguir.

```php

<?php print "Desejamos aos candidatos uma boa sorte!!!"; ?>

```







