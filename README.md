<h1 align="center">🐘 PHP</h1>
  
## O que aprendi durante o curso:
  
  **Laracasts:**
  
  Eu curti muito esse curso do Laracasts, o professor Jeffrey ensina de uma forma muito didática, simples e visual, e com isso consegui aprender 80% dos conceitos sem ter dúvida. No terceiro e quarto episódio logo de cara já matei algumas dúvidas simples que eu nao havia entendido vendo alguns conteúdos no YouTube, como: A **diferença** de usar `<?=$exemplo;?>` e `<?php echo $example; ?>`(que na verdade é só uma simplificaçao); **como usar concatenaçao**; **A necessidade de utlizar um close tag `?/>` quando php é utilizado no meio de um arquivo  html**; e PRINCIPALMENTE **a facilidade de usar o comando `php -S localhost:8888` no terminal em vez de instalar Xampp ou algo do tipo**. - Nesses dois episódios foi estudado o uso de variáveis, como printar algo na tela utilizando echo, o uso de contatenaçoes (ex: `$name = Gabriel; echo "Hello" . $name;`), localhost e algumas curiosidades, funçao `htmlspecialchars()` (que tenho algumas dúvidas quanto a utilizaçao, mas pelo que entendi converte tudo para String).
   
   Da aula 5 a aula 10 os assuntos abordado foram:
   
   **Aula 5**
   
   - O uso do `require` (linkar um path para o arquivo atual). 
   Ex: 
   ```
   require 'index.view.php';
   ```

   **Aula 6**
   
   - Array -> algo que eu nao sabia usar de uma maneira correta em php, tenho experiencia com o assunto em outras linguagens, mas nas primeiras vezes que estudei sofri para entender a aplicaçao. 
   Ex:
   ```
<?php
$person =[
'age' => 19, 
'hair' => 'brown'
];
```
   Além disso aprendi a funcionalidade de `foreach` e `endforeach` (simplificação do `for` para trabalhar com vetores e matrizes). 
   
   **Aula 7**
   
   - Associative Arrays -> É utilizado quando voce quer utilizar chaves nomeadas que voce atribuiu a elas. Usa-se da seguinte forma: 
  
```
<?php
$person =[
'age' => 19, 
'hair' => 'brown'
];
echo "Gabriel is " . $person['age'] . " years old.";
``` 
   - `$key` utiliza a chave que voce definiu na Associative Array.

   - Function `var_dump()` -> Imprime todos os elementos do Array. 
   
   - Function `die()`-> Pelo que entendi, imprime uma mensagem e sai do Script atual. 
   
   - Function `unset` -> Destrói a variavel que foi especificada. 
   Ex: 
   
   index.view.php
   ```
<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
    <meta charset="utf-8">
    <title></title>
</head>
<body>

<ul>

    <?php foreach ($person as $feature) : ?>

    <li><?= $feature; ?></li>

    <?php endforeach;?>

</ul>
```

  index.php
 ```
<?php
$person =[
  'age' => 19,
  'hair' => 'brown'
];

unset ($person['age']);

require 'index.view.php';
```

saída:
```
•brown
```
   **Aula 8**
  
   -  Boolean -> Famoso 01 da tropa de elite. Um boolean expressa um valor de verdade, que pode ser **true** ou **false**. 
   Ex estrutura:
   ```
   true ? 'do something' : 'do somehing else'
   
   ```
   Ex aplicaçao:
   ```
   <strong>
     Status: 
   </strong> 
      <?= $task['completed'] ? 'Complete' : 'Incomplete'; ?>
   ```
   Nesta aula aprendi algumas functions tbm, como `ucwords` (que faz com que a primeira letra de cada palavra fique maiúscula), e a como pesquisar devidamente um problema.
   
   **Aula 9**
   
   - Conditional -> Nessa aula solucionei minha maior dúvida, que era como implementar uma condiçao de uma maneira correta em php. Uma condiçao utiliza a seguinte estrutura: 
   ```
   if($condition){
    }else{
   }
   ```
   
Exemplo de aplicaçao: 
  
```
<?php
if($task['completed']){
echo 'finished';
}else {
  echo 'incomplete'; 
}])
```

Também pode ser representada da seguinte forma:
```
if(!$task[completed]){ 
echo 'incomplete';
}])
```
      
  A `!` representa uma negaçao, pode ser utilizada da mesma forma para uma condiçao.  
  
   **Aula 10**
  
   -  Function -> Além de aprender a estrutura de uma funçao 
 ```
 Function dumper($one, $two){
 var_dump($one, $two);
 } 
 dumper ('hello', 'Gabriel');
 ```
 também aprendi a usar a `function dd()` (funçao que realiza die dump)
 Ex: 
 ```
 function dd($data){
   echo '<pre>'; die (var_dump($data)); 
   echo '<pre>';
 } 
 dd('hello');
 ```


  Da aula 11 a aula 14 os assuntos abordados foram relativos a db:
  
  **Aula 11**
  
  - Instalaçao do mySQL e utilizaçao do mesmo no Terminal - Nessa aula sofri MUITO procurando um erro `ERROR 1045 (28000): Access denied for user 'root'@'localhost' (using password: YES)` que estava ocorrendo no terminal. Passei longas 2 horas procurando por mim mesmo, pois aprendi que é com porrada que se aprende. Aprendi a como navegar, criar, usar, excluir, inserir e mostrar tables e database pelo terminal, utilizando os comandos: 
 ```
 my sql -u root
 ```
 ```
 show data bases;
 ```
 ```
 create database exemplo;
 ``` 
 ```
 use exemplo;
 ```
 ```
 show exemplo;
 ```
 ```
 create table exemplo
 ```
 ```
 create table exemplo(description text, completed boolean)
 ```
 ```
 describe exemplo;
 ```
 ```
 drop table exemplo;
 ```
 ```
 insert into exemplo
 ```

  **Aula 12**
  
  - Class -> Aprendi que Classe é uma estrutura que abstrai um conjunto de elementos contendo características parecidas. Uma Classe é utilizada da seguinte forma: `class Person{ }` -> É utilizado uma letra maiúscula no ínicio da palavra (no caso do exemplo `Person`), assim como um pronome. Além disso aprendi a usar as keywords `public` e `protected` (só a própria classe/classes geradas podem acessar o conteúdo). Alem de classes, o outro tópico principal foi Objetos - Ainda tenho algumas dúvidas, mas vou pesquisar. Ex: `$tasks = [ new Task('Go to Store')];`

  **Aula 13**
  
  - PDO Class -> Basicamente é uma classe que dirige conexoes com banco de dados. Pode ser utilizado da seguinte forma: `try{ $pdo = new PDO('mysql:host=127.0.0.1; dbname=exemplo', 'root', '')} catch{PDOException $e{ die('Nao pode conectar')} $statement = $pdo->prepare('select * from ***database***'); $statement -> execute();`. fetchAll -> `$tasks = $statement -> fetchAll(PDO::FETCH_OBJ);`-> é possível fazer desta forma também (forma correta): *criar Task class* e depois `$tasks = $statement -> fetchAll(PDO::FETCH_CLASS, 'Task');`
  
  **Aula 14**
  
  - PDO Refactoring -> uso de Query Builder - cria e roda database queries. -no caso da aula usei o select para selecionar tudo de um table em particular. Aprendi principalemnte a utilizar corretamente Construtores -> a partir do QueryBuilder. Como estou estudando Java na faculdade, achei muitas semelhanças com php, principalmte com o uso de Construtores, declaraçao de funçao, classes e etc. De certa forma isso favoreceu a conseguir entender de ma maneira mais fácil. 
  
  **Aula 15**
  
  - A aula 15 foi dedicada a aprender a esconder passwords. - Foi um conhecimento muito útil para o meu projeto *SEARCHIT*, onde eu estava tentando aplicar um sistema de login e cadastro. Ex: `return[ 'database' => [ 'name => 'exemplo', 'username => 'root', 'password' => 'new-password', 'connection' => mysql:host=127.0.0.1', 'options' => [ ] ] ];` . Exemplo com ERRORMODE: `return[ 'database' => [ 'name => 'exemplo', 'username => 'root', 'password' => 'new-password', 'connection' => mysql:host=127.0.0.1', 'options' => [ PDO::ATTR_ERRMODE => PDO::ERRMODE_EXCEPTION ] ] ];` - ERRMODE_EXCEPTION trás um feedback mais destalhado.

  **Aula 16**
  
  - Fazer um Router (Rota) -> **Essa foi a aula com mais conteúdos e mais complicada para mim**. O Router básicamente é um caminho para acessar uma parte de um site  através de uma URI. Com o Router é possível acesssar partes em específico de um site (como Contato, Valores da empresa, etc.) - na aula o professsor usou o exemplo de Contact, About Us e Culture. -> Pelo que entendi os frameworks cumprem o papel do router, inclusive no final da aula o professor disse que era necessário saber o conceito, mas nao necessariamente se preocupar muito com a implementaçao, pois o frameworks fazem esse trab pra nós.
  
  **Aula 17**
  
  -  Essa foi a aula mais suave, como ja tenho um contato de longo prazo com html, apenas relembrei alguns conceitos, como: Acessar e compartilhar HTML em templates (adicionar links); Pintar um pouco de botao; Partials function-> Diminui em funçoes mais específicas. 
  
  **Aula 18 e 19**
  
  - Na aula 18 aprendi sobre Array Filtering, que como o próprio nome sugere, filtra arrays - ou seja, se vc escolher um Array em específico para ser filtrado, ou filtrar mais de um Array, é válido a autilizaçao de Array Filtering. Também aprendi sobre Array map (remapeia/transforma e cria um novo array) e Array column (retorna valores de uma coluna determinada). Na aula 19 a aula foi relativa a formulário (açoes de um formulário comum), types e request/get (sao variaveis *super globais* que coletam informaçoes especificas. Ex de estutura: `var_dump($_REQUEST);` ou `var_dump($_GET);` )
  
  **Aula 20**
  
  - A aula 20 foi muito importante na minha questao de login e cadastro, aprendi a como inserir o nome/informaçao digitado do form no data base (table). <- ainda tenho algumas dúvidas.
  
  **Aula 21**
  
  - Composer -> Em vez de usar 1 milhao de require's o composer faz autoloading das classes e facilita/simplifica o código. -> Aula 21
  
  **Aula 22**
  
  -DI Container -> Gerencia e Automotiza o injecting e reading de objetos. Ex: `App::bind('config', require 'config.php'); $config = App::get('config');` 
  
  **Aula 23**
  
  - Controller -> Geralmente um Controller é responsavel por receber uma request e retornar uma response. Essa foi uma aula dedicada exclusivamente para o ensino de Controllers, consegui entender todo o conceito.
  
  **Aula 24**
  
  - Namespaces -> Basicamente tem a principal funçao de organizar melhor o código, evitando conflitos com o nome de objetos, classes, funçoes e agrupando classes. Tem o objetivo de encapsular itens. Já ouvi falar por ter estudado um pouco de C++.
  
  **Aula 25**
  
  -Laravel
  Instalaçao, configuraçao e explicaçao -> Explicaçao e introduçao, a partir do arquivo criado no curso, da parte mais básica de Laravel. Como assisto suas lives a mais de 2 anos já tenho uma boa base do básico de Laravel, entao consegui entender todos os conceitos perfeitamente. Ansioso para o próximo passo!
  
## TMJ PRIMAO

Aprendi MUITO com esse curso, foi um impulso enorme para eu finalmente entender e perder o medo de php. Te agradeço imensamente pelo help primo, espero que tenha curtido o resumo, nao escrevo um texto desde o Enem KKKKKKKKKK coracao roxo
