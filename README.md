<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sistema de Reviews</title>

<style>
body{
    font-family: Arial, sans-serif;
    background:#f5f5f5;
    margin:0;
    padding:30px;
}

.container{
    max-width:700px;
    margin:auto;
}

h1{
    text-align:center;
}

.card{
    background:white;
    padding:20px;
    border-radius:10px;
    margin-bottom:20px;
    box-shadow:0 2px 10px rgba(0,0,0,.1);
}

textarea{
    width:100%;
    height:120px;
    resize:none;
    padding:10px;
}

select{
    padding:8px;
    margin-top:10px;
}

button{
    background:#007bff;
    color:white;
    border:none;
    padding:10px 20px;
    border-radius:8px;
    cursor:pointer;
    margin-top:10px;
}

button:hover{
    background:#0056b3;
}

.review{
    background:white;
    border-radius:10px;
    padding:15px;
    margin-top:15px;
    box-shadow:0 2px 8px rgba(0,0,0,.1);
}

.like{
    background:#ff4081;
    margin-top:10px;
}

.like:hover{
    background:#e91e63;
}

.data{
    color:gray;
    font-size:13px;
}
</style>

</head>
<body>

<div class="container">

<h1>⭐ Sistema de Reviews</h1>

<div class="card">

<h3>Nova Review</h3>

<textarea id="texto" placeholder="Escreva sua review..."></textarea>

<br>

<select id="nota">
<option value="5">⭐⭐⭐⭐⭐ (5)</option>
<option value="4">⭐⭐⭐⭐ (4)</option>
<option value="3">⭐⭐⭐ (3)</option>
<option value="2">⭐⭐ (2)</option>
<option value="1">⭐ (1)</option>
</select>

<br>

<button onclick="salvarReview()">
Publicar Review
</button>

</div>

<h2>Reviews</h2>

<div id="reviews"></div>

</div>

<script>

let reviews = JSON.parse(localStorage.getItem("reviews")) || [];

function salvarReview(){

    let texto = document.getElementById("texto").value;

    let nota = document.getElementById("nota").value;

    if(texto.trim()==""){
        alert("Escreva uma review.");
        return;
    }

    reviews.unshift({
        texto,
        nota,
        likes:0,
        data:new Date().toLocaleString()
    });

    localStorage.setItem("reviews",JSON.stringify(reviews));

    document.getElementById("texto").value="";

    mostrarReviews();

}

function curtir(indice){

    reviews[indice].likes++;

    localStorage.setItem("reviews",JSON.stringify(reviews));

    mostrarReviews();

}

function mostrarReviews(){

    let lista=document.getElementById("reviews");

    lista.innerHTML="";

    reviews.forEach((review,index)=>{

        lista.innerHTML+=`
        <div class="review">

            <div class="data">${review.data}</div>

            <h3>${"⭐".repeat(review.nota)}</h3>

            <p>${review.texto}</p>

            <button class="like" onclick="curtir(${index})">
            ❤️ Curtir (${review.likes})
            </button>

        </div>
        `;

    });

}

mostrarReviews();

</script>

</body>
</html>
