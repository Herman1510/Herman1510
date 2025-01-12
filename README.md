<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quiz</title>
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

<h1>Quiz</h1>

<div id="quizContent">
    <form id="quizForm">
        <!-- Question 1 -->
        <div class="question">
            <label for="q1">Trauma to the pterion threatens injury to which artery?</label><br>
            <input type="radio" name="q1" value="a"> Anterior pterygoid<br>
            <input type="radio" name="q1" value="b"> Posterior auricular<br>
            <input type="radio" name="q1" value="c"> Common maxillary<br>
            <input type="radio" name="q1" value="d"> External carotid<br>
            <input type="radio" name="q1" value="e"> Middle meningeal<br>
        </div>
        <button type="button" onclick="submitQuiz()">Submit</button>
    </form>
    <div class="result" id="result"></div>
</div>

<script>
    function submitQuiz() {
        const answers = {
            q1: "e" // Correct answer for question 1
        };

        let score = 0;
        let totalQuestions = 1;

        let selectedAnswer = document.querySelector(`input[name="q1"]:checked`);
        if (selectedAnswer && selectedAnswer.value === answers.q1) {
            score++;
        }

        let result = document.getElementById('result');
        result.textContent = `Your score is: ${score} out of ${totalQuestions}`;
    }
</script>

</body>
</html>
