---
title: Welcome to my brutal honest calculator
---

<!DOCTYPE html>
<html>
<head>
    <title>Age Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 500px;
            margin: 50px auto;
            padding: 20px;
            text-align: center;
        }
        input, button {
            margin: 10px;
            padding: 8px;
            font-size: 16px;
        }
        #result {
            margin-top: 20px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <h1>Age Calculator</h1>
    <input type="number" id="age" placeholder="How old are you lad?!">
    <button onclick="checkAge()">Check Age</button>
    <p id="result"></p>

    <script>
        function checkAge() {
            const age = parseInt(document.getElementById('age').value);
            let message = "";

            if (isNaN(age)) {
                message = "You are an idiot!";
            } else if (age < 0) {
                message = "You haven't been born yet!";
            } else if (age === 0) {
                message = "You are a newborn!";
            } else if (age > 0 && age <= 2) {
                message = "Hah! You're just a baby :X";
            } else if (age > 2 && age <= 12) {
                message = "You are a child!";
            } else if (age > 12 && age <= 18) {
                message = "You are a teenager";
            } else if (age > 18 && age < 88) {
                message = "You are an adult";
            } else if (age >= 80 && age <= 120) {
                message = "You are old as shit!";
            } else {
                message = "You are a GOD!";
            }

            document.getElementById('result').textContent = message;
        }
    </script>
</body>
</html>
