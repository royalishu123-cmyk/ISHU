<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Counter Webpage</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-image: url('https://images.unsplash.com/photo-1517245386807-bb43f82c33c4');
            background-size: cover;
            background-position: center;
            color: white;
            height: 100vh;
            margin: 0;
            padding-top: 100px;
        }
         .container {
            background-color: rgba(0, 0, 0, 0.6);
            display: inline-block;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 0 10px white;
        }
          h1 {
            font-size: 40px;
            margin-bottom: 20px;
        }
        #count {
            font-size: 60px;
            margin: 20px 0;
        }
        button {
            font-size: 18px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: 0.3s;
        }
        button:hover {
            opacity: 0.8;
        }
        #increment-btn {
            background-color: #28a745;
            color: white;
        }
        #save-btn {
            background-color: #007bff;
            color: white;
        }
        #saved {
            margin-top: 20px;
            font-size: 18px;
            background-color: rgba(255, 255, 255, 0.2);
            padding: 10px;
            border-radius: 8px;
        }
    </style>
</head>

<body>
    <div class="container">
        <h1>Counter App</h1>
        <!-- Counter Display -->
        <div id="count">0</div>
        <!-- Buttons -->
        <button id="increment-btn" onclick="increment()">Increase Count</button>
        <button id="save-btn" onclick="save()">Save Count</button>
        <!-- Display Saved Counts -->
        <p id="saved">Previous Counts: </p>
    </div>
    <!-- JavaScript Logic -->
    <script>
        let count = 0;
        let savedCounts = [];
        function increment() {
            count++;
            document.getElementById("count").textContent = count;
        }
        function save() {
            if (count === 0) return; // do nothing if count is 0
            savedCounts.push(count);
            document.getElementById("saved").textContent = "Previous Counts: " + savedCounts.join(" - ");
            count = 0;
            document.getElementById("count").textContent = count;
        }
    </script>
</body>
</html>
