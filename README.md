# ISHU
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Counter App</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>Counter App</h1>
        <div id="counter">0</div>
        <button onclick="increment()">Increment</button>
        <button onclick="save()">Save</button>
        <div id="saved-counts">
            <h2>Saved Counts:</h2>
            <p id="save-list"></p>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    text-align: center;
    background-image: url('your-background-image.jpg');
    background-size: cover;
    color: white;
}

.container {
    background-color: rgba(0, 0, 0, 0.6);
    padding: 30px;
    margin: 100px auto;
    width: 300px;
    border-radius: 10px;
}

button {
    padding: 10px 20px;
    margin: 10px;
    font-size: 16px;
    cursor: pointer;
}

#counter {
    font-size: 48px;
    margin: 20px 0;
}
let count = 0;

function increment() {
    count++;
    document.getElementById('counter').innerText = count;
}

function save() {
    const saveList = document.getElementById('save-list');
    saveList.textContent += count + ' - ';
    count = 0;
    document.getElementById('counter').innerText = count;
}
