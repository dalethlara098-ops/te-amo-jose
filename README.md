<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Te Amo 💖</title>

<style>
body {
    margin: 0;
    padding: 0;
    background: linear-gradient(135deg, #ff9a9e, #fad0c4);
    font-family: Arial, sans-serif;
    text-align: center;
    color: white;
    overflow-x: hidden;
}

h1 {
    margin-top: 50px;
    font-size: 40px;
    animation: fadeIn 2s ease-in-out;
}

p {
    font-size: 20px;
}

button {
    background: white;
    color: #ff4e78;
    border: none;
    padding: 15px 25px;
    font-size: 18px;
    border-radius: 30px;
    cursor: pointer;
    margin-top: 20px;
    transition: 0.3s;
}

button:hover {
    transform: scale(1.1);
}

#carta {
    display: none;
    margin-top: 20px;
    padding: 20px;
    background: rgba(255,255,255,0.2);
    border-radius: 20px;
}

@keyframes fadeIn {
    from {opacity: 0;}
    to {opacity: 1;}
}

/* Corazones flotando */
.heart {
    position: fixed;
    bottom: -10px;
    font-size: 20px;
    animation: floatUp 5s linear infinite;
}

@keyframes floatUp {
    0% {transform: translateY(0); opacity: 1;}
    100% {transform: translateY(-100vh); opacity: 0;}
}
</style>
</head>

<body>

<h1>💖 Te Amo José 💖</h1>

<p>Eres lo mejor que me ha pasado ✨</p>

<img src="https://i.imgur.com/4M7IWwP.jpg" width="250" style="border-radius:20px;">

<br>

<button onclick="mostrarCarta()">Abrir Carta 💌</button>

<div id="carta">
    <p>
        Desde que llegaste a mi vida todo es más bonito.
        Gracias por existir, por tu sonrisa,
        por cada momento juntos.
        Te amo hoy, mañana y siempre 💕
    </p>
</div>

<audio autoplay loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
</audio>

<script>
function mostrarCarta() {
    document.getElementById("carta").style.display = "block";
}

function crearCorazon() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "💖";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = Math.random() * 20 + 15 + "px";
    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 5000);
}

setInterval(crearCorazon, 300);
</script>

</body>
</html>
