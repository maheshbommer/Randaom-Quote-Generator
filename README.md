# Randaom-Quote-Generator
Random Quote Generator using HTML, CSS, and JavaScript with a clean and responsive UI.
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Random Quote Generator</title>

<style>
    *{
        margin:0;
        padding:0;
        box-sizing:border-box;
        font-family: Arial, sans-serif;
    }

    body{
        height:100vh;
        display:flex;
        justify-content:center;
        align-items:center;
        background:#f4f4f4;
    }

    .container{
        width:90%;
        max-width:600px;
        background:#fff;
        padding:30px;
        border-radius:12px;
        box-shadow:0 4px 10px rgba(0,0,0,0.1);
        text-align:center;
    }

    h1{
        margin-bottom:20px;
        color:#333;
    }

    #quote{
        font-size:22px;
        color:#444;
        margin-bottom:15px;
        line-height:1.5;
    }

    #author{
        font-size:18px;
        color:#777;
        margin-bottom:20px;
        font-style:italic;
    }

    button{
        background:#007bff;
        color:white;
        border:none;
        padding:12px 20px;
        border-radius:8px;
        cursor:pointer;
        font-size:16px;
    }

    button:hover{
        opacity:0.9;
    }
</style>
</head>
<body>

<div class="container">
    <h1>Random Quote Generator</h1>

    <p id="quote">Click the button to get a quote.</p>
    <p id="author"></p>

    <button onclick="generateQuote()">New Quote</button>
</div>

<script>
const quotes = [
    {
        quote: "The future depends on what you do today.",
        author: "Mahatma Gandhi"
    },
    {
        quote: "Success is not final, failure is not fatal: it is the courage to continue that counts.",
        author: "Winston Churchill"
    },
    {
        quote: "Believe you can and you're halfway there.",
        author: "Theodore Roosevelt"
    },
    {
        quote: "Dream big and dare to fail.",
        author: "Norman Vaughan"
    },
    {
        quote: "Do something today that your future self will thank you for.",
        author: "Sean Patrick Flanery"
    }
];

function generateQuote() {
    const randomIndex = Math.floor(Math.random() * quotes.length);

    document.getElementById("quote").textContent =
        `"${quotes[randomIndex].quote}"`;

    document.getElementById("author").textContent =
        `— ${quotes[randomIndex].author}`;
}

// Show a random quote when the page loads
window.onload = generateQuote;
</script>

</body>
</html>
