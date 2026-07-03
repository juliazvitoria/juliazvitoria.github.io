<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Music Reviews</title>

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{
font-family:'Inter',sans-serif;
background:transparent;
color:white;
padding:40px;
}

.container{
max-width:950px;
margin:auto;
}

h1{
font-size:42px;
font-weight:700;
margin-bottom:8px;
}

.subtitle{
color:#9ca3af;
margin-bottom:35px;
}

.review{

display:grid;
grid-template-columns:170px 1fr;
gap:25px;

margin-bottom:30px;

background:rgba(255,255,255,.06);
backdrop-filter:blur(18px);

border:1px solid rgba(255,255,255,.08);

border-radius:20px;

padding:22px;

transition:.3s;

}

.review:hover{

transform:translateY(-5px);

background:rgba(255,255,255,.08);

}

.cover{

width:170px;
height:170px;
border-radius:12px;
object-fit:cover;

box-shadow:0 10px 30px rgba(0,0,0,.4);

}

.album{

font-size:30px;
font-weight:700;

}

.artist{

color:#a1a1aa;
margin-top:4px;
margin-bottom:15px;

}

.score{

display:inline-block;

padding:7px 14px;

background:#22c55e;

border-radius:999px;

font-weight:bold;

margin-bottom:18px;

}

.review p{

line-height:1.8;

color:#ddd;

}

.footer{

margin-top:40px;

text-align:center;

color:#777;

font-size:14px;

}

@media(max-width:700px){

.review{

grid-template-columns:1fr;

}

.cover{

width:100%;

height:auto;

}

h1{

font-size:34px;

}

}

</style>

</head>

<body>

<div class="container">

<h1>🎵 Music Reviews</h1>

<div class="subtitle">
Minhas opiniões sobre álbuns, EPs e singles.
</div>

<div class="review">

<img class="cover"
src="https://upload.wikimedia.org/wikipedia/en/2/2d/Radioheadokcomputer.png">

<div>

<div class="album">
OK Computer
</div>

<div class="artist">
Radiohead • 1997
</div>

<div class="score">
★★★★★ 5.0
</div>

<p>

Um dos discos mais importantes da história do rock alternativo.
Cada faixa acrescenta algo diferente, e a produção continua
impressionante décadas depois. "Paranoid Android" e "No Surprises"
continuam entre minhas favoritas.

</p>

</div>

</div>

<div class="review">

<img class="cover"
src="https://upload.wikimedia.org/wikipedia/en/b/b2/Tyler%2C_the_Creator_-_IGOR.png">

<div>

<div class="album">
IGOR
</div>

<div class="artist">
Tyler, the Creator • 2019
</div>

<div class="score">
★★★★☆ 4.5
</div>

<p>

Uma mistura excelente de neo-soul, hip-hop e pop experimental.
O álbum conta uma história do começo ao fim e possui uma identidade
sonora muito marcante.

</p>

</div>

</div>

<div class="review">

<img class="cover"
src="https://upload.wikimedia.org/wikipedia/en/0/0b/Brat_album_cover.png">

<div>

<div class="album">
BRAT
</div>

<div class="artist">
Charli XCX • 2024
</div>

<div class="score">
★★★★★ 5.0
</div>

<p>

Energia do começo ao fim. Produção eletrônica criativa, refrões fortes
e um dos lançamentos pop mais comentados dos últimos anos.

</p>

</div>

</div>

<div class="footer">

Feito por você 🎧

</div>

</div>

</body>
</html>
