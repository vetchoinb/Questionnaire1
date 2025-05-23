<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Questionnaire Général</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f5f5f5;
        }
        .header {
            background-color: #4CAF50;
            color: white;
            padding: 15px;
            text-align: center;
            border-radius: 5px 5px 0 0;
        }
        .form-container {
            background-color: white;
            padding: 20px;
            border-radius: 0 0 5px 5px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            margin-bottom: 20px;
        }
        .form-group {
            margin-bottom: 15px;
            padding: 10px;
            border-bottom: 1px solid #eee;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        input[type="text"], input[type="number"] {
            width: 100%;
            padding: 8px;
            box-sizing: border-box;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        .radio-group {
            margin-top: 5px;
        }
        .timer {
            text-align: center;
            font-size: 1.2em;
            margin: 15px 0;
            color: #d32f2f;
            font-weight: bold;
        }
        button {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            margin-right: 10px;
        }
        button:hover {
            background-color: #45a049;
        }
        button:disabled {
            background-color: #cccccc;
            cursor: not-allowed;
        }
        .results-container {
            background-color: white;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            margin-top: 20px;
        }
        .result-item {
            padding: 10px;
            border-bottom: 1px solid #eee;
        }
        .correct {
            color: #4CAF50;
        }
        .incorrect {
            color: #f44336;
        }
        .final-score {
            font-weight: bold;
            font-size: 1.2em;
            margin-top: 10px;
        }
        .consolidated-results {
            margin-top: 30px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 8px;
            text-align: left;
        }
        th {
            background-color: #f2f2f2;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>Questionnaire Général</h1>
        <p id="date-display"></p>
    </div>
    
    <div class="form-container">
        <div class="timer">
            Temps restant: <span id="time">02:00</span>
        </div>
        
        <form id="quiz-form">
            <div class="form-group">
                <label for="nom">Nom et Prénom:</label>
                <input type="text" id="nom" name="nom" required>
            </div>
            
            <div class="form-group">
                <label>Sexe:</label>
                <div class="radio-group">
                    <input type="radio" id="homme" name="sexe" value="homme" required>
                    <label for="homme" style="display: inline; font-weight: normal;">Homme</label>
                    <input type="radio" id="femme" name="sexe" value="femme">
                    <label for="femme" style="display: inline; font-weight: normal;">Femme</label>
                </div>
            </div>
            
            <div class="form-group">
                <label for="q1">1. Quelle est la capitale du Burkina Faso?</label>
                <input type="text" id="q1" name="q1" required>
            </div>
            
            <div class="form-group">
                <label>2. Quelle est la capitale de la région du Centre-Ouest?</label>
                <div class="radio-group">
                    <input type="radio" id="q2a" name="q2" value="Réo" required>
                    <label for="q2a" style="display: inline; font-weight: normal;">Réo</label><br>
                    <input type="radio" id="q2b" name="q2" value="Sapouy">
                    <label for="q2b" style="display: inline; font-weight: normal;">Sapouy</label><br>
                    <input type="radio" id="q2c" name="q2" value="Koudougou">
                    <label for="q2c" style="display: inline; font-weight: normal;">Koudougou</label><br>
                    <input type="radio" id="q2d" name="q2" value="Léo">
                    <label for="q2d" style="display: inline; font-weight: normal;">Léo</label>
                </div>
            </div>
            
            <div class="form-group">
                <label>3. La capitale de la Russie est Moscou:</label>
                <div class="radio-group">
                    <input type="radio" id="q3a" name="q3" value="Vrai" required>
                    <label for="q3a" style="display: inline; font-weight: normal;">Vrai</label>
                    <input type="radio" id="q3b" name="q3" value="Faux">
                    <label for="q3b" style="display: inline; font-weight: normal;">Faux</label>
                </div>
            </div>
            
            <div class="form-group">
                <label>4. Quelle est la couleur du vin?</label>
                <div class="radio-group">
                    <input type="radio" id="q4a" name="q4" value="vert" required>
                    <label for="q4a" style="display: inline; font-weight: normal;">Vert</label><br>
                    <input type="radio" id="q4b" name="q4" value="rouge">
                    <label for="q4b" style="display: inline; font-weight: normal;">Rouge</label><br>
                    <input type="radio" id="q4c" name="q4" value="jaune">
                    <label for="q4c" style="display: inline; font-weight: normal;">Jaune</label><br>
                    <input type="radio" id="q4d" name="q4" value="orange">
                    <label for="q4d" style="display: inline; font-weight: normal;">Orange</label>
                </div>
            </div>
            
            <div class="form-group">
                <label for="q5">5. Quel est le nombre d'os dans le corps humain?</label>
                <input type="number" id="q5" name="q5" required>
            </div>
            
            <div class="form-group">
                <label for="q6">6. Quel est le nom du pape?</label>
                <input type="text" id="q6" name="q6" required>
            </div>
            
            <div class="form-group">
                <label for="q7">7. Quel nombre vient après 16?</label>
                <input type="number" id="q7" name="q7" required>
            </div>
            
            <div class="form-group">
                <label for="q8">8. Quel est le nom du concepteur?</label>
                <input type="text" id="q8" name="q8" required>
            </div>
            
            <div class="form-group">
                <label for="q9">9. Quelle est l'année de l'indépendance du Burkina Faso?</label>
                <input type="number" id="q9" name="q9" required>
            </div>
            
            <div class="form-group">
                <label for="q10">10. Quel est le roi des animaux?</label>
                <input type="text" id="q10" name="q10" required>
            </div>
            
            <button type="submit" id="submit-btn">Soumettre</button>
            <button type="button" id="reset-btn" style="background-color: #f44336;">Nouveau Questionnaire</button>
        </form>
    </div>

    <div class="results-container" id="results" style="display: none;">
        <h2>Résultats</h2>
        <div id="individual-results"></div>
        <div class="final-score" id="final-score"></div>
    </div>

    <div class="results-container consolidated-results" id="consolidated-results" style="display: none;">
        <h2>Résultats Consolidés</h2>
        <table id="results-table">
            <thead>
                <tr>
                    <th>Nom</th>
                    <th>Sexe</th>
                    <th>Score</th>
                    <th>Date</th>
                </tr>
            </thead>
            <tbody id="results-body">
            </tbody>
        </table>
    </div>

    <script>
        // Stockage des résultats
        let allResults = [];
        
        // Afficher la date actuelle
        const now = new Date();
        const options = { year: 'numeric', month: 'long', day: 'numeric', hour: '2-digit', minute: '2-digit' };
        document.getElementById('date-display').textContent = 'Date de collecte: ' + now.toLocaleDateString('fr-FR', options);
        
        // Configuration du timer
        let timeLeft = 120;
        let timer;
        
        function startTimer() {
            timeLeft = 120;
            updateTimerDisplay();
            clearInterval(timer);
            timer = setInterval(updateTimer, 1000);
        }
        
        function updateTimer() {
            timeLeft--;
            updateTimerDisplay();
            
            if (timeLeft <= 0) {
                clearInterval(timer);
                lockQuestionnaire();
                alert('Le temps est écoulé! Le questionnaire est maintenant verrouillé.');
            }
        }
        
        function updateTimerDisplay() {
            const minutes = Math.floor(timeLeft / 60);
            const seconds = timeLeft % 60;
            document.getElementById('time').textContent = 
                (minutes < 10 ? '0' : '') + minutes + ':' + (seconds < 10 ? '0' : '') + seconds;
        }
        
        function lockQuestionnaire() {
            document.getElementById('quiz-form').querySelectorAll('input').forEach(input => {
                input.disabled = true;
            });
            document.getElementById('submit-btn').disabled = true;
        }
        
        function unlockQuestionnaire() {
            document.getElementById('quiz-form').querySelectorAll('input').forEach(input => {
                input.disabled = false;
            });
            document.getElementById('submit-btn').disabled = false;
        }
        
        // Gestion de la soumission du formulaire
        document.getElementById('quiz-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Récupérer les données du formulaire
            const nom = document.getElementById('nom').value;
            const sexe = document.querySelector('input[name="sexe"]:checked').value;
            const date = new Date();
            
            // Calcul du score
            let score = 0;
            const results = [];
            
            // Question 1
            const q1 = document.getElementById('q1').value.trim().toLowerCase();
            const q1Correct = q1 === 'ouagadougou';
            if (q1Correct) score += 1;
            results.push({ question: 1, correct: q1Correct });
            
            // Question 2
            const q2 = document.querySelector('input[name="q2"]:checked');
            const q2Correct = q2 && q2.value === 'Koudougou';
            if (q2Correct) score += 1;
            results.push({ question: 2, correct: q2Correct });
            
            // Question 3
            const q3 = document.querySelector('input[name="q3"]:checked');
            const q3Correct = q3 && q3.value === 'Vrai';
            if (q3Correct) score += 1;
            results.push({ question: 3, correct: q3Correct });
            
            // Question 4
            const q4 = document.querySelector('input[name="q4"]:checked');
            const q4Correct = q4 && q4.value === 'rouge';
            if (q4Correct) score += 1;
            results.push({ question: 4, correct: q4Correct });
            
            // Question 5
            const q5 = document.getElementById('q5').value.trim();
            const q5Correct = q5 === '144';
            if (q5Correct) score += 1;
            results.push({ question: 5, correct: q5Correct });
            
            // Question 6
            const q6 = document.getElementById('q6').value.trim().toLowerCase();
            const q6Correct = q6 === 'françois';
            if (q6Correct) score += 1;
            results.push({ question: 6, correct: q6Correct });
            
            // Question 7
            const q7 = document.getElementById('q7').value.trim();
            const q7Correct = q7 === '17';
            if (q7Correct) score += 1;
            results.push({ question: 7, correct: q7Correct });
            
            // Question 8
            const q8 = document.getElementById('q8').value.trim().toLowerCase();
            const q8Correct = q8 === 'hervé';
            if (q8Correct) score += 1;
            results.push({ question: 8, correct: q8Correct });
            
            // Question 9
            const q9 = document.getElementById('q9').value.trim();
            const q9Correct = q9 === '1960';
            if (q9Correct) score += 1;
            results.push({ question: 9, correct: q9Correct });
            
            // Question 10
            const q10 = document.getElementById('q10').value.trim().toLowerCase();
            const q10Correct = q10 === 'lion';
            if (q10Correct) score += 1;
            results.push({ question: 10, correct: q10Correct });
            
            // Stocker le résultat
            const resultEntry = {
                nom,
                sexe,
                score,
                date: date.toLocaleString('fr-FR', options),
                details: results
            };
            
            allResults.push(resultEntry);
            
            // Afficher les résultats individuels
            displayIndividualResults(resultEntry);
            
            // Afficher les résultats consolidés
            displayConsolidatedResults();
            
            // Désactiver le bouton de soumission
            document.getElementById('submit-btn').disabled = true;
        });
        
        function displayIndividualResults(result) {
            const container = document.getElementById('individual-results');
            container.innerHTML = '';
            
            result.details.forEach((item, index) => {
                const div = document.createElement('div');
                div.className = 'result-item';
                div.innerHTML = `Question ${index + 1}: <span class="${item.correct ? 'correct' : 'incorrect'}">${item.correct ? 'Correct (1 point)' : 'Incorrect (0 point)'}</span>`;
                container.appendChild(div);
            });
            
            document.getElementById('final-score').textContent = `Score final: ${result.score}/10`;
            document.getElementById('results').style.display = 'block';
        }
        
        function displayConsolidatedResults() {
            const tbody = document.getElementById('results-body');
            tbody.innerHTML = '';
            
            allResults.forEach(result => {
                const tr = document.createElement('tr');
                tr.innerHTML = `
                    <td>${result.nom}</td>
                    <td>${result.sexe}</td>
                    <td>${result.score}/10</td>
                    <td>${result.date}</td>
                `;
                tbody.appendChild(tr);
            });
            
            document.getElementById('consolidated-results').style.display = 'block';
        }
        
        // Réinitialisation du formulaire
        document.getElementById('reset-btn').addEventListener('click', function() {
            document.getElementById('quiz-form').reset();
            unlockQuestionnaire();
            startTimer();
        });
        
        // Démarrer le timer au chargement
        startTimer();
    </script>
</body>
</html>
