<h1 align="center">🐘 PHP</h1>
  
## O que aprendi com essa linguagem maravilhosa:

**Consideraçoes iniciais:**

  Tentei algumas vezes aprender PHP, mas falhei miseravelmente em todas as tentativas por nao ter força de vontade para ir atrás das minhas dúvidas (que eram muitas). Sempre tive problemas com interpretaçao (de texto ou nao) e por incrível que pareça descobri que tenho uma interpretacao melhor em Ingles???? nao faço idéia do porque, mas por conta disso, esse curso abriu minha mente de uma forma absurda e consegui entender todos os conceitos que eu tinha dúvidas nas primeiras vezes que tentei aprender. Por conta disso, gostaria de te agradecer muito por isso. 
  
  PHP é uma linguagem que sempre curti, porém sempre tive medo de aprender de cara por aparentar ser algo difícil, mas depois de assistir as aulas eu percebi que o objetivo do PHP é simplificar ,de certa forma, muitos conceitos de outras linguagens e tornar o desenvolvimento mais fácil e ágil.
  
  **Laracasts:**
  
  Eu amei esse curso do Laracasts, o professor Jeffrey ensina de uma forma muito didática, simples e visual, e com isso consegui aprender 99% dos conceitos sem ter dúvida. No terceiro e quarto episódio logo de cara já matei algumas dúvidas simples que eu nao havia entendido vendo alguns conteúdos no YouTube, como: A **diferença** de usar `<?=$exemplo;?>` e `<?php echo $example; ?>`(que na verdade é só uma simplificaçao); **como usar concatenaçao**; **A necessidade de utlizar um close tag `?/>` quando php é utilizado no meio de um arquivo  html**; e PRINCIPALMENTE **a facilidade de usar o comando `php -S localhost:8888` no terminal em vez de instalar Xampp ou algo do tipo**. - Nesses dois episódios foi estudado o uso de variáveis, como printar algo na tela utilizando echo, o uso de contatenaçoes (ex: `$name = Gabriel; echo "Hello" . $name;`), localhost e algumas curiosidades, funçao `htmlspecialchars()` (que tenho algumas dúvidas quanto a utilizaçao, mas pelo que entendi converte tudo para String).
   
   Da aula 5 a aula 10 os assuntos abordado foram:
   
   - O uso do `require` (linkar um path para o arquivo atual), algo que procurei saber como funcionava quando eu estava fazendo um sistema de login mas nao achei nada a respeito. <-Aula 5
   
   - Array -> algo que eu nao sabia usar de uma maneira correta em php, tenho bastantante experiencia com o assunto em outras linguagens, mas nas primeiras vezes que estudei sofri bastante para entender a apliicaçao. Além disso aprendi a funcionalidade de `foreach` e `endforeach` (simplificação do `for` para trabalhar com vetores e matrizes). <-Aula 6
   
   - Associative Arrays -> É utilizado quando voce quer utilizar chaves nomeadas que voce atribuiu a elas. É utilizado da seguinte forma: `$person =['age' => 19, 'hair' => 'brown'];` -> `$key` utiliza a chave que voce definiu na Associative Array. <- Aula 7

   - Function `var_dump()` -> Imprime todos os elementos do Array. Function `die()`-> Pelo que entendi, após a utilizaçao desta funçao, os elementos abaixo da linha do código sao ignorados. Ou seja, imprime uma mensagem e sai do Script atual. - Abreviaçao da funçao `exit()`. Function `unset` -> Imprime todos elementos do array especificado, menos uma característica escolhida. Ex: `unset(person['age']);` <- Aula 7 
  
   -  Boolean -> Famoso 01 tropa de elite e TF do lol. Nesta aula aprendi algumas functions tbm, como `ucwords` (que faz com que a primeira letra de cada palavra fique maiúscula) -> Ex `<?= ucwords($example);?>`. Tambem aprendi a utilizar e implementar o **Boolean Operator** -> `true ? 'do something' : 'do something else'` <- Aula 8
   
   - Conditional -> Nessa aula solucionei minha maior dúvida, que era como implementar uma condiçao de uma maneira correta em php. Uma condiçao utiliza a seguinte estrutura: `if($condition){ }else{ }` -> Ex: `if($task['completed'{ echo 'finished'; }else { echo 'incomplete'; }])`. Também pode ser representada da seguinte forma: `if(!$task[completed{ echo 'incomplete';}])`. A `!` representa uma negaçao, pode ser utilizada da mesma forma para uma condiçao. <- Aula 9  
  
   -  `Function example(){ }`-> Além de aprender a estrutura de uma funçao - `Function dumper($one, $two){ var_dump($one, $two);} dumper ('hello', 'Gabriel');` - também aprendi a usar a `function dd()` (funçao que realiza die dump) -> Ex: `function dd($data){ echo '<pre>'; die (var_dump($data)); echo '<pre>';} dd('hello');` -> Aula 10


  Da aula 11 a aula 13 os assuntos abordados foram:
  
  - Instalaçao do mySQL e utilizaçao do mesmo no Terminal - Nessa aula sofri MUITO procurando um erro `ERROR 1045 (28000): Access denied for user 'root'@'localhost' (using password: YES)` que estava ocorrendo no terminal. Passei longas 2 horas procurando por mim mesmo, pois aprendi que é com porrada que se aprende. Aprendi a como navegar, criar, usar, excluir, inserir e mostrar tables e database pelo terminal, utilizando os comandos: `my sql -u root`, `show data bases;`, `create database exemplo;`, `use exemplo;`, `show exemplo;`, `create table exemplo`, `create table exemplo(description text, completed boolean)`, `describe exemplo;`, `drop table exemplo;`, `insert into exemplo`. -> Aula 11
  
  -
  
  -
  
  -
  
