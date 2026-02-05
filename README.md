# valentine_day
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Valentine Day</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <style>
        body {
            background-color: #f8cfd4;
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .card {
            background: white;
            width: 360px;
            padding: 30px;
            text-align: center;
            border-radius: 15px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }

        h2, h1 {
            color: #ff4d6d;
        }

        .buttons {
            position: relative;
            height: 80px;
            margin-top: 20px;
        }

        button {
            padding: 10px 25px;
            font-size: 16px;
            border: none;
            border-radius: 20px;
            cursor: pointer;
        }

        #yesBtn {
            background-color: #ff4d6d;
            color: white;
        }

        #noBtn {
            background-color: #ccc;
            position: absolute;
        }

        /* Hide wish page initially */
        #wishPage {
            display: none;
        }
    </style>
</head>
<body>

<!-- PAGE 1 -->
<div class="card" id="questionPage">
    <h2>Will you be my Valentine? 💕</h2>

    <div class="buttons">
        <button id="yesBtn">Yes</button>
        <button id="noBtn">No</button>
    </div>
</div>

<!-- PAGE 2 -->
<div class="card" id="wishPage">
    <h1>💖 Happy Valentine’s Day 💖</h1>
    <p style="font-size:20px;">You are my Valentine ❤️</p>
    <p style="font-size:18px;">Always & Forever 💕</p>
</div>

<script>
    const noBtn = document.getElementById("noBtn");
    const yesBtn = document.getElementById("yesBtn");
    const questionPage = document.getElementById("questionPage");
    const wishPage = document.getElementById("wishPage");

    // Move NO button
    noBtn.addEventListener("mouseover", () => {
        const x = Math.random() * 250;
        const y = Math.random() * 50;
        noBtn.style.left = x + "px";
        noBtn.style.top = y + "px";
    });

    // YES opens next page
    yesBtn.addEventListener("click", () => {
        questionPage.style.display = "none";
        wishPage.style.display = "block";
    });
</script>

</body>
</html>
