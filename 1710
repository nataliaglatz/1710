<?php

$txt_usuario = trim(@$_POST['txt_usuario']); // trim= comando para tirar espaços do lado direito e esquerdo da variável
$txt_senha = md5(trim(@$_POST['txt_senha'])); // md5= codificar senha, não precisa usar no usuário 

@session_start(); //iniciar sessão 
$_SESSION['usuario'] = NULL; //"_" =variável de ambiente
$_SESSION['senha'] = NULL; //"_" =variável de ambiente senha
if ($txt_usuario && $txt_senha != '') { //!= operador(vazio). Condicional 
    $_SESSION['usuario'] = $txt_usuario; //Variável de ambiente igua a variável texto usuário
    $_SESSION['senha'] = $txt_senha;//Variável de ambiente igua a variável texto senha
}
$host = 'localhost'; // servidor
if ($_SERVER['SERVER_NAME'] != 'localhost') { //condicional 
    $host = 'otherhost.mysql.com'; //nome do host 
}//conector

$db = 'stopots'; //database (banco de dados)
$usuario = 'root'; // variável do usuário
$senha = ''; 

try{ //controle de tentativa
    $conexao = mysqli_connect($host, $usuario, $senha);
    echo 'Conexão bem sucedida.';
} catch (Exception $e){ //pegar o erro se der erro 
    die('Não foi possível conectar ao banco de dados. Erro: ' . $e); // morrer: dar fim no erro 
}

$conexao = mysqli_connect($host,$usuario,$senha); // conectar usuário e senha no localhost

mysqli_select_db($conexao,$db); // comando para selecionar a base de dados 
?>

<!--Documentação feito em dupla por Aleciane e Eduardo-->