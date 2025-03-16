<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Find Your Phone</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f0f0f0;
            padding: 20px;
        }
        .container {
            margin: 20px;
            padding: 20px;
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }
        .hidden {
            display: none;
        }
        #sans {
            background-color: #2e3b4e;
            color: white;
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
            font-size: 20px;
        }
        .button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            font-size: 16px;
        }
        .button:hover {
            background-color: #45a049;
        }
        #startButton {
            background-color: #008CBA;
            color: white;
            font-size: 24px;
        }
        #startButton:hover {
            background-color: #007B9F;
        }
    </style>
</head>
<body>

    <div class="container" id="welcomeSection">
        <h1>Welcome to our AMAZING Find My Phone Website!</h1>
        <p>We are about to help you find your phone... but first, you'll need to pass a few challenges. Ready?</p>
        <button id="startButton" class="button" onclick="startProcess()">Start</button>
    </div>

    <div class="container hidden" id="captchaSection">
        <h2>Step 1: Solve the CAPTCHA</h2>
        <img src="captcha (1).png" alt="CAPTCHA" />
        <input type="text" id="captchaInput" placeholder="Enter CAPTCHA" />
        <button class="button" onclick="checkCaptcha()">Submit</button>
        <p id="captchaError" style="color: red; display: none;">Incorrect CAPTCHA, try again!</p>
    </div>

    <div class="container hidden" id="worldleSection">
        <h2>Step 2: Submit the Daily Worldle Answer</h2>
        <p>Guess the word for today's Worldle!</p>
        <input type="text" id="worldleInput" placeholder="Enter Worldle answer" />
        <button class="button" onclick="checkWorldle()">Submit</button>
        <p id="worldleError" style="color: red; display: none;">Incorrect Worldle answer! The correct answer was im not telling you cuz im annoying</p>
    </div>

    <div class="container hidden" id="sansSection">
        <h2>Step 3: Defeat groblin!</h2>
        <div id="sans">groblin is laughing... Can you defeat him?</div>
        <button class="button" onclick="defeatSans()">Fight groblin</button>
        <p id="sansError" style="color: red; display: none;">You lost to groblin, try again!</p>
    </div>

    <div class="container hidden" id="guessNumberSection">
        <h2>Step 4: Guess the Number (1-50)</h2>
        <input type="number" id="numberGuess" placeholder="Guess a number between 1 and 50" min="1" max="50" />
        <button class="button" onclick="checkNumberGuess()">Submit</button>
        <p id="numberGuessError" style="color: red; display: none;">Incorrect guess!</p>
    </div>

    <div class="container hidden" id="finalMessage">
        <h2>Your Phone Status</h2>
        <p>Your phone is somewhere.</p>
    </div>

    <script>
        let captchaSolved = false;
        let worldleSolved = false;
        let sansDefeated = false;
        let numberGuessedCorrectly = false;

        // Set today's correct Worldle answer
        const correctWorldleAnswer = "stamp";  // Change this for each day

        function startProcess() {
            document.getElementById("welcomeSection").classList.add("hidden");
            document.getElementById("captchaSection").classList.remove("hidden");
        }

        function checkCaptcha() {
            const captchaInput = document.getElementById("captchaInput").value;
            if (captchaInput === "12345") {
                captchaSolved = true;
                document.getElementById("captchaSection").classList.add("hidden");
                document.getElementById("worldleSection").classList.remove("hidden");
            } else {
                document.getElementById("captchaError").style.display = "block";
            }
        }

        function checkWorldle() {
            const worldleInput = document.getElementById("worldleInput").value.toLowerCase();
            if (worldleInput === correctWorldleAnswer) {
                worldleSolved = true;
                document.getElementById("worldleSection").classList.add("hidden");
                document.getElementById("sansSection").classList.remove("hidden");
            } else {
                document.getElementById("worldleError").style.display = "block";
                document.getElementById("correctWord").textContent = correctWorldleAnswer;
            }
        }

        function defeatSans() {
            const sansText = document.getElementById("sans");
            sansText.textContent = "groblin is throwing stuff! Dodge them!";
            setTimeout(() => {
                sansText.textContent = "groblin is laughing... You're winning!";
                sansDefeated = true;
                document.getElementById("sansSection").classList.add("hidden");
                document.getElementById("guessNumberSection").classList.remove("hidden");
            }, 3000);
        }

        function checkNumberGuess() {
            const guess = parseInt(document.getElementById("numberGuess").value);
            const correctNumber = Math.floor(Math.random() * 50) + 1;
            if (guess === correctNumber) {
                numberGuessedCorrectly = true;
                document.getElementById("guessNumberSection").classList.add("hidden");
                document.getElementById("finalMessage").classList.remove("hidden");
            } else {
                document.getElementById("numberGuessError").style.display = "block";
            }
        }
    </script>

</body>
</html>
