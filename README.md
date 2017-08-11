# work-at-s3wf
Para a vaga de desenvolvedor criamos um simples teste para verificar a fluência de programação. O teste e as instruções podem ser encontrados aqui..

## Trabalhe na S3wf

A S3WF é uma fábrica de software que tem como foco principal o desenvolvimento de aplicações web.
A nossa equipe é composta por pessoas que amam o que fazem e sempre estamos à procura de novos talentos.
Logo abaixo está a descrição de um pequeno teste para avaliar se o candidato possui algumas das habilidades básicas para trabalhar conosco.

# Aplicativo versão / PHP 7

```php
Você deve implementar um aplicativo em php que irá agendar uma tarefa para ser executada em um segundo momento, antes disso teremos que logar no aplicativo.

# Requisitos Login

 - Tela de Login e senha
 - Apresentar os erros possíveis se não conseguir logar
 - Usar javascript + jquery ou qualquer outro framework de domínio para tratar os erros na tela ( da forma mais simples que encontrar)
 - Os envios dos dados do login e senha tem que ser feitos com Ajax ( importante )
 - Os retornos de erro terão que ser feito com Ajax retornando Json ( importante )
 - Quando logar com sucesso criara uma sessão para que o usuário permaneça na tela de admin

# Requisitos Ambiente admin , após logar 

 - O ambiente administrativo é simples só terá mesmo nossa tabela em HTML contendo uma lista das tarefas a serem executadas e mais nada.
 - Nossa tabela em Html terá 08  colunas e 2 linhas
  Data inicial, Hora Inicial, Data Final, Hora Final, Tamanho do csv, Nome Csv, Download, Ação
  
# Criar o layout acima na tela do admin

- O button gerar csv irá disparar um AJAX para que possa agendar a execução
- Após disparar o ajax, o programa irá setar que a tarefa selecionada está pronta para ser executada.
- E o button na tela da ação irá ficar desativado enquanto não finaliza a execução.

# Requisitos Ambiente admin , após clicar em “gerar csv”

- Quando clicar em gerar csv na verdade o seu AJAX irá enviar para o PHP qual tarefa terá que ser executada e mais nada, o retorno é feito em json sucesso ou erro, e um algo para desativar o button ou enviar um msg para que o button altere o seu value para “em andamento”

- O programa PHP irá setar em uma tabela esta ação e mais nada.

- Caso faço F5 na ou atualizo a tela de alguma forma o programa irá entender que já foi clicado na ação e o mesmo fica desativado ou avisar que está “em andamento” a execução da tarefa.

- Requisitos programa script para gerar csv

```
