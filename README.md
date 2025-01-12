<body>
    <h1>Password Protected Quiz</h1>

    <div id="quizContent" style="display:none;">
        <!-- Quiz content goes here -->
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
        // Password protection logic
        const password = "MAKULA"; // The required password

        let enteredPassword = prompt("Enter password to access the quiz:");

        if (enteredPassword === password) {
            document.getElementById('quizContent').style.display = 'block';
        } else {
            alert("Incorrect password.");
            window.location.href = "about:blank"; // Redirect to blank page if the password is incorrect
        }

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
