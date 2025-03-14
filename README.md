# meu-site-namoro

<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nosso Amor</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #000;
            color: #ff66b2;
        }
        .container {
            margin-top: 50px;
        }
        img {
            max-width: 300px;
            border-radius: 10px;
            margin-top: 20px;
            border: 3px solid #ff66b2;
        }
        #countdown {
            font-size: 24px;
            margin-top: 20px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Nosso Amor</h1>
        <p>Juntos desde 17 de março de 2023 às 20h</p>
        <blockquote class="imgur-embed-pub" lang="en" data-id="a/eXTQ8eP" data-context="false">
            <a href="//imgur.com/a/eXTQ8eP"></a>
        </blockquote>
        <script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>
        <div id="countdown"></div>
    </div>
    
    <script>
        function updateCountdown() {
            const startDate = new Date("2023-03-17T20:00:00");
            const now = new Date();
            let diff = now - startDate;
            
            let seconds = Math.floor((diff / 1000) % 60);
            let minutes = Math.floor((diff / 1000 / 60) % 60);
            let hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
            let days = Math.floor(diff / (1000 * 60 * 60 * 24));
            
            document.getElementById("countdown").innerHTML = 
                `${days} dias, ${hours} horas, ${minutes} minutos e ${seconds} segundos de amor!`;
        }
        
        setInterval(updateCountdown, 1000);
        updateCountdown();
    </script>
</body>
</html>
