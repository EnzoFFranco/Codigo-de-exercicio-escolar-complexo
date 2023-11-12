# Codigo-de-exercicio-escolar-complexo
Esse código é sobre um exercicio que pedia que o programa PHP recebesse um número e retornasse o maior número primo inferior possível do número digitado. A professora não conseguiu resolver e disse para pesquisarmos, eu (Enzo Ferreira Franco), queria por puro ego resolver sozinho, após certo tempo consegui, e venho aqui postar o código.

Enunciado: 

Crie uma função que receba um número inteiro como argumento e retorne o maior valor primo inferior a esse argumento. Se o argumento for negativo, a função deverá retornar o valor zero.

Código: 
<?php




  $np = $_POST["np"];

function primom($v){

    if($v < 0){
        print("Número negativo, inválido");
    }
    else if($v == 0 or $v == 1 or $v == 2){
        print("O valor digitado é 0, ou 1 ou 2, nesses casos não há números menores primos");
    }
    else{
    $primo = 1;
    while ($primo<4){
        $v = $v - 1;
        $primo = 1;
        for($i = 2 ;$i < $v ;$i= $i + 1)
        {
            $c = $v % $i;
            if($c == 0){
                $primo = 0;
            }


        }
        if($primo == 1){
            print("O número primo mais próximo é: $v");
            $primo = 5;
        }
    }
    }
}
primom($np);




?>
