UT2P02 – Formulario 
En esta práctica he hecho una pequeña aplicación con HTML y PHP, primero he hecho un formulario en ut2p02,el sueldo tiene que ser mayor de 1000 y el puesto puede ser Base, Directivo o Alto cargo.

El formulario manda los datos al archivo ut2p02.php usando el método POST.
en el archivo PHP recojo los datos con:
$sueldo = $_POST["sueldo"];
$puesto = $_POST["puesto"];

Después uso varios if para poner el porcentaje según el puesto:
$porcentaje = 0;

if ($puesto == "base") {
    $porcentaje = 10;
}

if ($puesto == "directivo") {
    $porcentaje = 15;
}

if ($puesto == "alto") {
    $porcentaje = 20;
}

Luego calculo el complemento y el sueldo final:
$complemento = $sueldo * $porcentaje / 100;
$sueldoFinal = $sueldo + $complemento;

Y finalmente muestro el resultado con echo.
Por ejemplo, si el sueldo es 1200€ y el puesto es Base, el resultado es:
El sueldo base es de 1200€
El complemento es del 10%
El sueldo final es de 1320€

Durante la práctica tuve un problema porque la variable $porcentaje no estaba definida, y lo solucioné poniéndola primero a 0.
También tuve que ejecutar el proyecto desde Herd, porque PHP necesita un servidor para funcionar.
Con este ejercicio he practicado formularios HTML, POST, variables, condiciones if, operaciones y echo.