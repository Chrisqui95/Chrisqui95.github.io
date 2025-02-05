
<html lang="en">
<head>
    
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Unclickable Button</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            margin: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #f0f0f0;
        }

        .container {
            position: relative;
            width: 100%;
            height: 100%;
        }

        button {
            position: absolute;
            padding: 10px 20px;
            font-size: 18px;
            cursor: pointer;
            background-color: #ff5733;
            color: white;
            border: none;
            border-radius: 5px;
        }
    </style>
</head>
<body>

    <div class="container">
        <button id="trickyButton">Press me:)</button>
    </div>

    <script>
        const button = document.getElementById("trickyButton");

        button.addEventListener("mouseenter", () => {
            const maxX = window.innerWidth - button.clientWidth;
            const maxY = window.innerHeight - button.clientHeight;

            const randomX = Math.floor(Math.random() * maxX);
            const randomY = Math.floor(Math.random() * maxY);

            button.style.left = randomX + "px";
            button.style.top = randomY + "px";
        });
    </script>

</body>
</html>
