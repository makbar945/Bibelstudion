<!DOCTYPE html>
<html lang="sv">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bibelstudion</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #8cc63f; /* Grön färg som liknar ComeOn Casino */
        }

        header {
            background-color: #006400; /* Mörkare grön för headern */
            color: white;
            padding: 20px;
            text-align: center;
        }

        nav {
            background-color: #4b8e14; /* Ljusare grön för navigering */
            overflow: hidden;
        }

        nav a {
            float: left;
            display: block;
            color: white;
            text-align: center;
            padding: 14px 20px;
            text-decoration: none;
        }

        nav a:hover {
            background-color: #ddd;
            color: black;
        }

        .content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            padding: 20px;
        }

        .video {
            width: 30%;
            margin: 10px;
            background-color: white;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            border-radius: 5px;
            overflow: hidden;
        }

        .video iframe {
            width: 100%;
            height: 200px;
        }

        .video h3 {
            text-align: center;
            padding: 10px;
            background-color: #006400; /* Mörkare grön för video rubriken */
            color: white;
        }

        .upload-section {
            width: 100%;
            text-align: center;
            margin-top: 20px;
        }

        .upload-section input {
            padding: 10px;
            font-size: 16px;
            margin-right: 10px;
        }

        .upload-section button {
            padding: 10px 20px;
            background-color: #006400; /* Mörkare grön för knappen */
            color: white;
            border: none;
            font-size: 16px;
        }

        .live-stream {
            background-color: #006400; /* Mörkare grön för livestream-sektionen */
            padding: 20px;
            color: white;
            text-align: center;
            margin-top: 20px;
        }
    </style>
</head>
<body>

<header>
    <h1>Bibelstudion - Dela och upptäck bibelrelaterade videor</h1>
</header>

<nav>
    <a href="#">Hem</a>
    <a href="#">Uppladdningar</a>
    <a href="#">Livestream</a>
    <a href="#">Min Profil</a>
</nav>

<div class="content">
    <div class="video">
        <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        <h3>Bibelstudie Video 1</h3>
    </div>
    <div class="video">
        <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        <h3>Bibelstudie Video 2</h3>
    </div>
    <div class="video">
        <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        <h3>Bibelstudie Video 3</h3>
    </div>
</div>

<div class="upload-section">
    <h2>Ladda upp din video</h2>
    <input type="file" name="video" accept="video/*">
    <button>Publicera Video</button>
</div>

<div class="live-stream">
    <h2>Gå Live</h2>
    <button>Starta Livestream</button>
</div>

</body>
</html>
