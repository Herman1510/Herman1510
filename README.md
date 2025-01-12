<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Password Protected Quiz</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        .question {
            margin-bottom: 20px;
        }
        .result {
            margin-top: 20px;
            font-size: 20px;
        }
    </style>
</head>
<body>

<h1>Password Protected Quiz</h1>

<script>
    // Password protection logic
    const password = "MAKULA"; // The required password

    let enteredPassword = prompt("Enter password to access the quiz:");

    if (enteredPassword !== password) {
        alert("Incorrect password.");
        window.location.href = "about:blank"; // Redirect to a blank page if the password is incorrect
    } else {
        // Display the quiz if password is correct
        document.getElementById('quizContent').style.display = 'block';
    }
</script>

<div id="quizContent" style="display:none;">
    <form id="quizForm">
        <!-- Question 1 -->
        <div class="question">
            <label for="q1">Trauma to the pterion threatens injury to which artery?</label><br>
            <input type="radio" name="q1" value="a"> Anterior pterygoid<br>
            <input type="radio" name="q1" value="b"> Posterior auricular<br>
            <input type="radio" name="q1" value="c">
