<!DOCTYPE html>
<html>
	
<head>
	
	<meta charset="utf-8">
	<title>Ordenar números de mayor a menor</title>
	<meta name="autor" content="Javier Álvarez Chavarría">
	<meta name="description" content="PHP">
	<link rel="stylesheet"  href="css/style.css">

</head>

<body>

<h2>Ordenar elementos de un arreglo de mayor a menor</h2>

<?php

$numeros = array(1,20,33,84,52,4,70,-8,92,10);//Se crea e inicializa el arreglo
$nElementos = count($numeros);//Número de elementos del arreglo
$cont = $nElementos;//Contador para elementos del arreglo
$contLoops = 1;//Contador para ciclo For

echo "<h3>Arreglo a modificar:  ";
print_r($numeros);//Imprime en pantalla el arreglo
echo "</h3>";


for ($i = 1; $i<$nElementos; $i++) {//Ciclo For externo, recorre desde el segundo elemento hasta el último elemento del arreglo

echo "<p style='font-family: Verdana ;color:Orange'>Paso ". $contLoops."</p>";

   for ($j = 0; $j < $nElementos - 1 ; $j++) {//Ciclo For interno, recorre desde el primer elemento hasta el penúltimo elemento del arreglo
       
       echo "Se compara " . $numeros[$j] . " y " . $numeros[$j+1] ;
       if ($numeros[$j] > $numeros[$j+1]) {//Comparación de los elementos del arreglo para verificar cuál de los 2 elementos es mayor
       		
       		echo " = ".$numeros[$j] . " es mayor que ". $numeros[$j+1];

       }else{

       		echo " = ".$numeros[$j] . " es menor que ". $numeros[$j+1];
       }

       if ($numeros[$j+1] > $numeros[$j]) {
           $temp = $numeros[$j]; $temp
           $numeros[$j] = $numeros[$j+1];
           $numeros[$j+1] = $temp;
       }//Al terminar con el If el resultado es el intercambio de los elementos

 	echo "<br>";

   }//Fin del ciclo For interno

echo "<br>";
print_r($numeros) ;//Imprime en pantalla el arreglo
echo "<p style='font-family: Verdana ;color:Green'>En el ciclo ". $contLoops.". El elemento de menor valor es ". $numeros[$cont-1]."</p>";
$contLoops++;//El contador del ciclo externo aumenta 1
$cont--;//El contador de los elementos resta 1

}//Fin del ciclo For externo

echo "<br><br>";
echo "<h3>Arreglo ordenado de mayor a menor: ";
print_r($numeros) ;//Imprime en pantalla el arreglo
echo "</h3><br><br><br>";

 
</body>

</html>
