<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Teddy Day My Love 🧸</title>

<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Poppins:wght@300;500&display=swap" rel="stylesheet">

<style>
body {
    margin: 0;
    padding: 0;
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #ffd6e8, #ffc2dd, #ffb3d9);
    overflow-x: hidden;
    text-align: center;
    color: white;
}

h1 {
    font-family: 'Pacifico', cursive;
    font-size: 2.8em;
    margin-top: 30px;
    text-shadow: 2px 2px 10px #ff69b4;
}

p {
    font-size: 1.1em;
    width: 85%;
    margin: auto;
    line-height: 1.6em;
}

.container {
    padding: 20px;
}

.btn {
    margin-top: 25px;
    padding: 12px 28px;
    font-size: 18px;
    border: none;
    border-radius: 30px;
    background: #ff4da6;
    color: white;
    cursor: pointer;
    box-shadow: 0 0 15px #ff85c1;
    transition: 0.3s;
}

.btn:hover {
    transform: scale(1.1);
    background: #ff1493;
}

.hidden {
    display: none;
}

/* Teddy Rain */
.teddy {
    position: fixed;
    top: -50px;
    font-size: 28px;
    animation: fall linear infinite;
}

@keyframes fall {
    to {
        transform: translateY(110vh);
    }
}

video {
    width: 85%;
    max-width: 360px;
    border-radius: 20px;
    margin-top: 20px;
    box-shadow: 0 0 20px #ff85c1;
}
</style>
</head>

<body>

<div class="container" id="home">
    <h1>Happy Teddy Day My Teddy 🧸💖</h1>

    <p>
        Tum meri life ka sabse soft, cutest aur warm hug ho.  
        Jaise teddy ko pakad ke sukoon milta hai, waise hi tum meri comfort ho.
    </p>

    <p style="margin-top:15px;">
        Tum meri smile ka reason ho, meri peace ho, aur meri favourite feeling ho 💕
    </p>

    <h2 style="margin-top:25px;">🧸 Teddy aapka intezaar kar raha hai 🧸</h2>

    <button class="btn" onclick="showSurprise()">Click for Your Teddy 🎁</button>
</div>

<div class="container hidden" id="surprise">
    <h1>Yeh Raha Aapka Teddy 🧸💞</h1>

    <p>
        Yeh teddy meri taraf se ek tight warm hug hai 🤗  
        Jab bhi tumhe meri yaad aaye, isse dekh lena…
    </p>

    <!-- LOOPING TEDDY VIDEO -->
    <video src="teddy.mp4" autoplay loop muted playsinline></video>

    <p style="margin-top:20px;">
        Happy Teddy Day meri sabse pyaari si jaan 🥰  
        Tum meri favourite ho, aaj bhi… kal bhi… hamesha 💖
    </p>
</div>

<script>
function showSurprise() {
    document.getElementById("home").classList.add("hidden");
    document.getElementById("surprise").classList.remove("hidden");
}

/* Teddy Rain Effect */
function createTeddy() {
    const teddy = document.createElement("div");
    teddy.classList.add("teddy");
    teddy.innerHTML = "🧸";
    teddy.style.left = Math.random() * window.innerWidth + "px";
    teddy.style.animationDuration = (3 + Math.random() * 5) + "s";
    document.body.appendChild(teddy);

    setTimeout(() => teddy.remove(), 8000);
}

setInterval(createTeddy, 400);
</script>

</body>
</html>
