# ProyectoJSON.github.io
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Proyecto Tercer Trimestre JSON</title>
</head>
<body>
    <div class="general">
        <header class="imagen"><h1>PROYECTO CON JSON</h1></header>
        <div id="central">
            <nav>
                <ul>
                    <li><a href="index.html"><img src="imagenes/casa.png"></a></li>
                    <li><a href="#"><img src="imagenes/palanca-de-mando.png"></a></li>
                    <li><a href="formulario.html"><img src="imagenes/letra.png"></a></li>
                    <li><a href="#"><img src="imagenes/grupo.png"></a></li>
                </ul>
            </nav>
        <div id="principal"></div>
    </div>
        <footer>
            <p> 28/05/2023 Proyecto JSON Imanol Alonso Vera 1º DAW</p>
        </footer>
    </div>

 <script>
    fetch('https://free-to-play-games-database.p.rapidapi.com/api/games?platform=pc',{
	 method: 'GET',
	 headers: {
	 	'X-RapidAPI-Key': '6794d82e63msh7504074a084680cp10b435jsn696e01831761',
	 	'X-RapidAPI-Host': 'free-to-play-games-database.p.rapidapi.com'
	 }})
        .then(response => response.json())
        .then(function (juegos) {
            document.getElementById("principal").innerHTML = "";

            for (var i = 0; i < 24; i++) {

                document.getElementById("principal").innerHTML +=
                    "<div class='tarjeta'>" +
                       "<a href='juego.html?id=" + juegos[i].id + "'>" + "<img src='" + juegos[i].thumbnail + "'> " + "</a>" +
                            "<p>" + juegos[i].title + "</p>"
                    "</div>";              
            }
        });  
</script>
</body>
</html>
