<!DOCTYPE html>
<html lang="sv">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bibelspel</title>
    <style>
        body {
            background-color: #f0f0f0;
            font-family: Arial, sans-serif;
        }

        .container {
            text-align: center;
            padding: 50px;
        }

        h1 {
            color: green;
        }

        .button {
            padding: 15px 30px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
            margin: 10px;
        }

        .button:hover {
            background-color: #45a049;
        }

        #gameDetails {
            margin-top: 20px;
            color: #333;
        }

        .saldo {
            font-size: 20px;
            font-weight: bold;
        }

    </style>
</head>
<body>
    <div class="container">
        <h1>Bibelspel - Välkommen</h1>

        <p>Logga in och välj ett spel att börja spela. Dagliga bibelverser presenteras här!</p>

        <button class="button" onclick="startGame('Squid Game')">Starta Squid Game</button>
        <button class="button" onclick="startGame('Bibel Quiz')">Starta Bibel Quiz</button>
        <button class="button" onclick="startGame('Film Relaterat Spel')">Starta Film Relaterat Spel</button>

        <div id="gameDetails">
            <p id="gameStatus">Välj ett spel för att börja.</p>
            <div id="saldo" class="saldo">Poäng: 0</div>
            <div id="timer">Tid: 00:00</div>
        </div>
    </div>

    <script>
        let points = 0; // Poängsystemet för spelet
        let timer;
        let gameTimer = 0;

        function startGame(gameName) {
            // Nollställ poäng och timer
            points = 0;
            gameTimer = 0;
            document.getElementById('saldo').innerText = "Poäng: " + points;
            document.getElementById('timer').innerText = "Tid: 00:00";

            // Starta spelet och uppdatera status
            if (gameName === 'Squid Game') {
                document.getElementById('gameStatus').innerText = "Spelet Squid Game startar nu!";
                // Specifik logik för Squid Game
                startGameTimer();
            } else if (gameName === 'Bibel Quiz') {
                document.getElementById('gameStatus').innerText = "Bibel Quiz startar nu!";
                // Specifik logik för Bibel Quiz
                startGameTimer();
            } else if (gameName === 'Film Relaterat Spel') {
                document.getElementById('gameStatus').innerText = "Film-relaterat spel startar nu!";
                // Specifik logik för Film-relaterat spel
                startGameTimer();
            }
        }

        // Funktion för att starta timern
        function startGameTimer() {
            clearInterval(timer); // Stoppa eventuell tidigare timer
            timer = setInterval(function() {
                gameTimer++;
                let minutes = Math.floor(gameTimer / 60);
                let seconds = gameTimer % 60;
                document.getElementById('timer').innerText = "Tid: " + formatTime(minutes) + ":" + formatTime(seconds);
            }, 1000);
        }

        // Funktion för att formatera tid (ex. 09:05)
        function formatTime(time) {
            return time < 10 ? "0" + time : time;
        }
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="sv">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vidtube</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #4CAF50;
            color: white;
            text-align: center;
            padding: 10px 0;
        }
        .video-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            padding: 20px;
        }
        .video {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            width: 300px;
            overflow: hidden;
        }
        .video iframe {
            width: 100%;
            height: 200px;
        }
        .video-title {
            text-align: center;
            padding: 10px;
            font-size: 16px;
            background-color: #f1f1f1;
        }
    </style>
</head>
<body>

    <header>
        <h1>Vidtube - Titta på kristna och andra videos</h1>
    </header>

    <div class="video-container">
        <!-- YouTube Video Embed Example -->
        <div class="video">
            <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            <div class="video-title">Kristen video 1</div>
        </div>

        <div class="video">
            <iframe src="https://www.youtube.com/embed/kJQP7kiw5Fk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            <div class="video-title">Kristen video 2</div>
        </div>

        <div class="video">
            <iframe src="https://www.youtube.com/embed/tgbNymZ7vqY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            <div class="video-title">Kristen video 3</div>
        </div>
    </div>

</body>
</html>

<!DOCTYPE html>
<html lang="sv">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Välkommen till Bibelstudion! Spela interaktiva bibliska spel, lär dig mer om Bibeln och testa dina kunskaper med bibelquiz. För kristna och bibelintresserade." />
    <meta name="keywords" content="bibelspel, bibelstudier, kristna spel, bibelquiz, bibliska karaktärer, Bibeln, bibelverser, kristen spelplattform" />
    <meta name="author" content="Bibelstudion">
    <title>Bibelstudion - Interaktiva bibliska spel och quiz</title>
    <link rel="canonical" href="https://www.bibelstudion.se/" />
    <meta property="og:title" content="Bibelstudion - Interaktiva bibliska spel och quiz" />
    <meta property="og:description" content="Upptäck Bibelstudion, en hemsida med bibliska spel, quiz och dagliga bibelverser. Lär dig mer om Bibeln genom rolig och engagerande gameplay." />
    <meta property="og:image" content="https://www.bibelstudion.se/og-image.jpg" />
    <meta property="og:url" content="https://www.bibelstudion.se/" />
    <meta property="og:type" content="website" />
    <meta name="twitter:card" content="summary_large_image" />
    <meta name="twitter:site" content="@bibelstudion" />
    <meta name="twitter:title" content="Bibelstudion - Interaktiva bibliska spel och quiz" />
    <meta name="twitter:description" content="Upptäck Bibelstudion och lär dig om Bibeln genom spel, quiz och dagliga bibelverser." />
    <meta name="twitter:image" content="https://www.bibelstudion.se/og-image.jpg" />

    <!-- Favicon -->
    <link rel="icon" href="https://www.bibelstudion.se/favicon.ico" type="image/x-icon">
    
    <!-- Open Graph (OG) Meta Tags for social sharing -->
    <meta property="og:image" content="https://www.bibelstudion.se/images/bibelstudion-logo.jpg" />
    <meta property="og:locale" content="sv_SE" />
    
    <!-- Structured Data for rich snippets (JSON-LD) -->
    <script type="application/ld+json">
    {
        "@context": "https://schema.org",
        "@type": "WebSite",
        "name": "Bibelstudion",
        "url": "https://www.bibelstudion.se",
        "description": "Bibelstudion erbjuder interaktiva bibliska spel, quiz och dagliga bibelverser för kristna och Bibelintresserade.",
        "publisher": {
            "@type": "Organization",
            "name": "Bibelstudion",
            "logo": {
                "@type": "ImageObject",
                "url": "https://www.bibelstudion.se/images/logo.png"
            }
        }
    }
    </script>
    
    <!-- External Stylesheets -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Välkommen till Bibelstudion</h1>
        <nav>
            <ul>
                <li><a href="#spel">Bibelspel</a></li>
                <li><a href="#quiz">Bibelquiz</a></li>
                <li><a href="#dagens-bibelvers">Dagens Bibelvers</a></li>
                <li><a href="#kontakt">Kontakt</a></li>
            </ul>
        </nav>
    </header>

    <section id="spel">
        <h2>Interaktiva Bibliska Spel</h2>
        <p>Spela engagerande bibliska spel och lär dig om Bibeln genom rolig gameplay. Våra spel inkluderar klassiska berättelser från Bibeln, utmanande uppdrag och lärorika aktiviteter.</p>
    </section>

    <section id="quiz">
        <h2>Bibelquiz</h2>
        <p>Testa dina kunskaper om Bibeln med våra utmanande quiz. Hur mycket vet du om de bibliska karaktärerna och historierna? Utmana dina vänner och bli en expert!</p>
    </section>

    <section id="dagens-bibelvers">
        <h2>Dagens Bibelvers</h2>
        <p id="bibelvers"></p>
        <script>
            // JavaScript to display daily Bible verse (example)
            document.getElementById("bibelvers").innerText = "Johannes 3:16: 'Ty så älskade Gud världen att han gav sin enfödde Son, för att var och en som tror på honom inte ska gå förlorad utan ha evigt liv.'";
        </script>
    </section>

    <footer id="kontakt">
        <p>Kontakt oss på <a href="mailto:kontakt@bibelstudion.se">kontakt@bibelstudion.se</a></p>
    </footer>

    <!-- External Scripts -->
    <script src="scripts.js"></script>
</body>
</html>

<!DOCTYPE html>
<html lang="sv">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Studion - Bibliska Nyheter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: green;
            color: white;
            text-align: center;
            padding: 15px;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        .news-item {
            background-color: white;
            margin-bottom: 20px;
            padding: 15px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        .news-item h2 {
            color: green;
        }
        .news-item p {
            font-size: 1.1em;
        }
        .advertisement {
            text-align: center;
            margin: 20px 0;
        }
        footer {
            background-color: green;
            color: white;
            text-align: center;
            padding: 10px;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
    </style>
</head>
<body>

<header>
    <h1>Välkommen till Studion - Bibliska Nyheter</h1>
</header>

<div class="container">
    <!-- Exempel på en nyhet -->
    <div class="news-item">
        <h2>Senaste Bibliska Nyheter: Jesus' Återkomst - En Ny Tolkning</h2>
        <p>En ny tolkning av de bibliska skrifterna antyder en ökad global medvetenhet om Jesu återkomst. Många religiösa ledare talar nu om viktiga tecken som enligt profetiorna leder till denna stora händelse...</p>
        <p>För att förstå mer om vad detta innebär för världen idag, måste vi granska skrifterna på nytt och söka efter tecken i våra dagliga liv.</p>
        <a href="#">Läs mer...</a>
    </div>

    <!-- Annonsering -->
    <div class="advertisement">
        <p><strong>Annons:</strong> Köp den senaste boken om Bibelns profetior idag!</p>
    </div>

    <!-- Nyhetsflöde -->
    <div class="news-item">
        <h2>Global Tolkning av Bibeln Växer i Populäritet</h2>
        <p>Medan moderna teologer betonar vikten av att förstå de bibliska texterna genom dagens lins, får bibelstudier nytt liv genom globalt samarbete...</p>
        <a href="#">Läs mer...</a>
    </div>

    <!-- Ytterligare annonsering -->
    <div class="advertisement">
        <p><strong>Annons:</strong> Gå med i vårt nyhetsbrev för exklusiva bibelstudier!</p>
    </div>
</div>

<footer>
    <p>&copy; 2025 Studion - Alla rättigheter förbehållna</p>
</footer>

</body>
</html>


<!DOCTYPE html>
<html lang="sv">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Gå live och diskutera bibeln, delta i bibliska samtal och livestreams.">
    <meta property="og:title" content="Livestreaming Bibeln - Gå Live och Dela Ditt Tro">
    <meta property="og:description" content="Dela din bibelkunskap och delta i live-diskussioner om bibeln.">
    <meta property="og:image" content="path/to/your-image.jpg">
    <meta property="og:url" content="https://dinhemsida.com/livestream">
    <title>Livestreaming Bibeln</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Välkommen till Bibel Live Stream</h1>
    </header>

    <!-- Livestream Player -->
    <div class="livestream-container">
        <div class="livestream-header">
            <h2>Streama Nu!</h2>
            <p>Detta är din plats för bibliska samtal i realtid.</p>
        </div>
        <div id="live-player">
            <iframe src="https://dinlivestreamingplattform.com/live?stream_id=12345" width="100%" height="500px" frameborder="0" allowfullscreen></iframe>
        </div>
        <div class="live-interaction">
            <p>Tittare: <span id="viewer-count">0</span></p>
            <div id="live-chat">
                <!-- Här kan användarna chatta i realtid -->
                <textarea id="chat-input" placeholder="Skriv en kommentar..."></textarea>
                <button id="send-chat">Skicka</button>
                <div id="chat-box"></div>
            </div>
        </div>
        <div id="like-system">
            <button id="like-button">Gilla</button>
            <span id="like-count">0</span> Gillar
        </div>
    </div>

    <!-- Delningsknappar för sociala medier -->
    <div class="social-share">
        <button onclick="shareToFacebook()">Dela på Facebook</button>
        <button onclick="shareToInstagram()">Dela på Instagram</button>
        <button onclick="shareToTikTok()">Dela på TikTok</button>
    </div>

    <!-- Monetisering och Premiumfunktioner -->
    <div class="premium-options">
        <p>Vill du ha extra funktioner? Kostar 10 kr per livestream.</p>
        <button onclick="subscribeForPremium()">Aktivera Premium</button>
    </div>

    <script>
        // Interaktiv funktion för chat och likes
        let likeCount = 0;
        let viewerCount = 0;
        const viewerCountElement = document.getElementById('viewer-count');
        const likeButton = document.getElementById('like-button');
        const likeCountElement = document.getElementById('like-count');
        const chatInput = document.getElementById('chat-input');
        const chatBox = document.getElementById('chat-box');

        // Funktion för att hantera likes
        likeButton.addEventListener('click', () => {
            likeCount++;
            likeCountElement.textContent = likeCount;
        });

        // Funktion för att hantera chat
        document.getElementById('send-chat').addEventListener('click', () => {
            const message = chatInput.value;
            if (message) {
                const newMessage = document.createElement('div');
                newMessage.textContent = message;
                chatBox.appendChild(newMessage);
                chatInput.value = '';
            }
        });

        // Funktion för att uppdatera tittare
        function updateViewerCount() {
            viewerCount++;
            viewerCountElement.textContent = viewerCount;
        }

        // Simulera tittartillväxt
        setInterval(updateViewerCount, 5000); // Öka tittare var 5:e sekund

        // Funktioner för att dela på sociala medier
        function shareToFacebook() {
            window.open("https://www.facebook.com/sharer/sharer.php?u=" + window.location.href, "_blank");
        }

        function shareToInstagram() {
            alert("Instagram delar inte direkt länkar till livestreams. Dela istället via stories!");
        }

        function shareToTikTok() {
            alert("Dela din livestream på TikTok med hashtaggen #bibellive!");
        }

        // Funktion för att aktivera premium
        function subscribeForPremium() {
            alert("Du har valt att aktivera premiumfunktioner. Kostnad: 10 kr.");
        }
    </script>

    <footer>
        <p>&copy; 2025 Bibel Live Stream - Alla rättigheter förbehållna.</p>
    </footer>
</body>
</html>

.video-upload-section, .video-section, .monetization-info, .store-section, .seo-tips {
    margin: 20px;
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 8px;
    background-color: #f9f9f9;
}

button {
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    border: none;
    cursor: pointer;
}

button:hover {
    background-color: #45a049;
}

textarea {
    width: 100%;
    font-family: Consolas, monospace;
    padding: 10px;
}

input[type="text"], input[type="number"], textarea {
    width: 100%;
    padding: 10px;
    margin: 5px 0;
    border-radius: 5px;
    border: 1px solid #ddd;
}

<!DOCTYPE html>
<html lang="sv">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Presentsystem</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 800px;
            margin: 20px auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        .present-button {
            background-color: #28a745;
            color: #fff;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .present-button:hover {
            background-color: #218838;
        }
        .value-info {
            margin-top: 20px;
            font-size: 16px;
        }
        .value-info span {
            font-weight: bold;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Skicka en Present</h1>
        <p>Välj värde på presenten och skicka till kontoägaren.</p>

        <div id="present-buttons">
            <button class="present-button" onclick="sendGift(1)">Present värd 1 kr</button>
            <button class="present-button" onclick="sendGift(5)">Present värd 5 kr</button>
            <button class="present-button" onclick="sendGift(10)">Present värd 10 kr</button>
        </div>

        <div id="value-info" class="value-info">
            <p><span>Totalt skickat värde:</span> <span id="total-sent">0</span> kr</p>
            <p><span>Du får:</span> <span id="your-share">0</span> kr</p>
            <p><span>Kontoägaren får:</span> <span id="account-owner-share">0</span> kr</p>
        </div>
    </div>

    <script>
        let totalSent = 0;

        function sendGift(value) {
            totalSent += value;

            // Beräkna andelen
            let yourShare = (value * 0.2).toFixed(2);
            let accountOwnerShare = (value * 0.8).toFixed(2);

            // Uppdatera HTML
            document.getElementById("total-sent").innerText = totalSent.toFixed(2);
            document.getElementById("your-share").innerText = yourShare;
            document.getElementById("account-owner-share").innerText = accountOwnerShare;

            // Här kan du skicka transaktionen till servern för att lagra värdena.
        }
    </script>

</body>
</html>



