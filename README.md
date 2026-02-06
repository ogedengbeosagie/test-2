# test-2
My Valentine
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Click Me</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
    body {
        margin: 0;
        height: 100vh;
        background: linear-gradient(135deg, #5a189a, #7b2cbf);
        display: flex;
        align-items: center;
        justify-content: center;
        font-family: Arial, sans-serif;
        color: white;
        text-align: center;
    }

    .container {
        max-width: 500px;
        padding: 20px;
        cursor: pointer;
    }

    h1 {
        font-size: 28px;
        line-height: 1.4;
    }

    .buttons {
        margin-top: 30px;
        display: none;
        gap: 15px;
        justify-content: center;
    }

    button {
        padding: 12px 24px;
        font-size: 16px;
        border: none;
        border-radius: 25px;
        cursor: pointer;
        background: white;
        color: #5a189a;
    }

    button:hover {
        opacity: 0.9;
    }
</style>
</head>

<body>

<div class="container" id="screen">
    <h1 id="text">Click me</h1>

    <div class="buttons" id="buttons">
        <button onclick="yes()">YES!</button>
        <button onclick="no()">No</button>
    </div>
</div>

<script>
const messages = [
    "We've made so many memories",
    "You make me happy",
    "You make me smile every single day",
    "I have one question to ask you",
    "Will you be my Valentine?"
];

let index = -1;
const text = document.getElementById("text");
const buttons = document.getElementById("buttons");

document.getElementById("screen").addEventListener("click", () => {
    if (index < messages.length - 1) {
        index++;
        text.innerText = messages[index];

        if (index === messages.length - 1) {
            buttons.style.display = "flex";
        }
    }
});

function yes() {
    text.innerText = "You just made me the happiest person ever 💜";
    buttons.style.display = "none";
}

function no() {
    text.innerText = "You still mean a lot to me 💜";
    buttons.style.display = "none";
}
</script>

</body>
</html>
