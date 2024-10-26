<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Do You Love Me?</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f5f5f5;
            font-family: Arial, sans-serif;
        }
        .container {
            text-align: center;
        }
        h1 {
            color: #333;
        }
        .buttons {
            margin-top: 20px;
        }
        .btn {
            padding: 10px 20px;
            font-size: 18px;
            margin: 10px;
            cursor: pointer;
        }
        #noBtn {
            position: relative;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>I love you. Do you love me?</h1>
        <div class="buttons">
            <button class="btn" onclick="showMessage()">Yes!</button>
            <button class="btn" id="noBtn" onmouseover="moveButton()">No!</button>
        </div>
        <p id="message" style="display: none; color: green; font-size: 20px; margin-top: 20px;">Thank You for Accept me Dear!</p>
    </div>

    <script>
        function moveButton() {
            const noBtn = document.getElementById('noBtn');
            const randomX = Math.floor(Math.random() * 300) - 150;
            const randomY = Math.floor(Math.random() * 300) - 150;
            noBtn.style.transform = `translate(${randomX}px, ${randomY}px)`;
        }

        function showMessage() {
            document.getElementById('message').style.display = 'block';
        }
    </script>
</body>
</html>
