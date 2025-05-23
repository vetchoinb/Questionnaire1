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
        .history-container {
            margin-top: 30px;
            background-color: #e8f5e9;
            padding: 20px;
            border-radius: 5px;
        }
        .history-item {
            margin-bottom: 20px;
            padding: 15px;
            background-color: white;
            border-radius: 5px;
            box-shadow: 0 1px 3px rgba(0,0,0,0.1);
        }
        .history-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
            padding-bottom: 5px;
            border-bottom: 1px solid #eee;
        }
        .history-title {
            font-weight: bold;
            color: #2e7d32;
        }
        .history-date {
            color: #666;
            font-size: 0.9em;
        }
        .history-responses {
            margin-top: 10px;
        }
        .response-row {
            display: flex;
            margin-bottom: 5px;
        }
        .response-question {
            font-weight: bold;
            width: 150px;
        }
        .response-answer {
            flex-grow: 1;
        }
        .locked {
            opacity: 0.6;
            pointer-events: none;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>Questionnaire Général</h1>
        <p id="date-display"></p>
    </div>
    
    <div class="form-container" id="questionnaire">
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
            <button type="button" id="reset-btn" style="background-color: #f44336;">Nouvelle tentative</button>
        </form>
    </div>

    <div class="results-container" id="current-results" style="display: none;">
        <h2>Résultats de la dernière soumission</h2>
        <div id="individual-results"></div>
        <div class="final-score" id="final-score"></div>
    </div>

    <div class="history-container" id="history-container">
        <h2>Historique des soumissions</h2>
        <div id="history-items"></div>
    </div>

    <script>
        // Stockage des résultats
        let allResults = [];
        let timer;
        let timeLeft = 120;
        
        // Afficher la date actuelle
        const now = new Date();
        const dateOptions = { year: 'numeric', month: 'long', day: 'numeric', hour: '2-digit', minute: '2-digit' };
        document.getElementById('date-display').textContent = 'Date de collecte: ' + now.toLocaleDateString('fr-FR', dateOptions);
        
        // Démarrer le timer
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
            document.getElementById('quiz-form').querySelectorAll('input, button').forEach(element => {
                element.disabled = true;
            });
            document.getElementById('questionnaire').classList.add('locked');
        }
        
        function unlockQuestionnaire() {
            document.getElementById('quiz-form').querySelectorAll('input, button').forEach(element => {
                element.disabled = false;
            });
            document.getElementById('questionnaire').classList.remove('locked');
        }
        
        // Gestion de la soumission du formulaire
        document.getElementById('quiz-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Récupérer les données du formulaire
            const formData = {
                nom: document.getElementById('nom').value,
                sexe: document.querySelector('input[name="sexe"]:checked').value,
                q1: document.getElementById('q1').value,
                q2: document.querySelector('input[name="q2"]:checked')?.value || '',
                q3: document.querySelector('input[name="q3"]:checked')?.value || '',
                q4: document.querySelector('input[name="q4"]:checked')?.value || '',
                q5: document.getElementById('q5').value,
                q6: document.getElementById('q6').value,
                q7: document.getElementById('q7').value,
                q8: document.getElementById('q8').value,
                q9: document.getElementById('q9').value,
                q10: document.getElementById('q10').value,
                date: new Date()
            };
            
            // Calcul du score
            let score = 0;
            const results = [];
            
            // Question 1
            const q1Correct = formData.q1.trim().toLowerCase() === 'ouagadougou';
            if (q1Correct) score += 1;
            results.push({ question: 1, correct: q1Correct, answer: formData.q1 });
            
            // Question 2
            const q2Correct = formData.q2 === 'Koudougou';
            if (q2Correct) score += 1;
            results.push({ question: 2, correct: q2Correct, answer: formData.q2 });
            
            // Question 3
            const q3Correct = formData.q3 === 'Vrai';
            if (q3Correct) score += 1;
            results.push({ question: 3, correct: q3Correct, answer: formData.q3 });
            
            // Question 4
            const q4Correct = formData.q4 === 'rouge';
            if (q4Correct) score += 1;
            results.push({ question: 4, correct: q4Correct, answer: formData.q4 });
            
            // Question 5
            const q5Correct = formData.q5.trim() === '144';
            if (q5Correct) score += 1;
            results.push({ question: 5, correct: q5Correct, answer: formData.q5 });
            
            // Question 6
            const q6Correct = formData.q6.trim().toLowerCase() === 'françois';
            if (q6Correct) score += 1;
            results.push({ question: 6, correct: q6Correct, answer: formData.q6 });
            
            // Question 7
            const q7Correct = formData.q7.trim() === '17';
            if (q7Correct) score += 1;
            results.push({ question: 7, correct: q7Correct, answer: formData.q7 });
            
            // Question 8
            const q8Correct = formData.q8.trim().toLowerCase() === 'hervé';
            if (q8Correct) score += 1;
            results.push({ question: 8, correct: q8Correct, answer: formData.q8 });
            
            // Question 9
            const q9Correct = formData.q9.trim() === '1960';
            if (q9Correct) score += 1;
            results.push({ question: 9, correct: q9Correct, answer: formData.q9 });
            
            // Question 10
            const q10Correct = formData.q10.trim().toLowerCase() === 'lion';
            if (q10Correct) score += 1;
            results.push({ question: 10, correct: q10Correct, answer: formData.q10 });
            
            // Stocker le résultat
            const resultEntry = {
                nom: formData.nom,
                sexe: formData.sexe,
                score,
                date: formData.date,
                results,
                formData
            };
            
            allResults.push(resultEntry);
            
            // Afficher les résultats
            displayCurrentResults(resultEntry);
            displayHistory();
            
            // Désactiver le bouton de soumission
            document.getElementById('submit-btn').disabled = true;
        });
        
        function displayCurrentResults(result) {
            const container = document.getElementById('individual-results');
            container.innerHTML = '';
            
            result.results.forEach((item, index) => {
                const div = document.createElement('div');
                div.className = 'result-item';
                div.innerHTML = `Question ${index + 1}: <span class="${item.correct ? 'correct' : 'incorrect'}">${item.correct ? 'Correct (1 point)' : 'Incorrect (0 point)'}</span> - Réponse: ${item.answer}`;
                container.appendChild(div);
            });
            
            document.getElementById('final-score').textContent = `Score final: ${result.score}/10`;
            document.getElementById('current-results').style.display = 'block';
        }
        
        function displayHistory() {
            const container = document.getElementById('history-items');
            container.innerHTML = '';
            
            if (allResults.length === 0) {
                container.innerHTML = '<p>Aucune soumission enregistrée.</p>';
                return;
            }
            
            allResults.forEach((result, index) => {
                const item = document.createElement('div');
                item.className = 'history-item';
                
                const header = document.createElement('div');
                header.className = 'history-header';
                header.innerHTML = `
                    <span class="history-title">Soumission ${index + 1} - ${result.nom}</span>
                    <span class="history-date">${result.date.toLocaleString('fr-FR', dateOptions)}</span>
                `;
                
                const score = document.createElement('div');
                score.className = 'final-score';
                score.textContent = `Score: ${result.score}/10`;
                
                const responses = document.createElement('div');
                responses.className = 'history-responses';
                
                result.results.forEach((q, qIndex) => {
                    const row = document.createElement('div');
                    row.className = 'response-row';
                    row.innerHTML = `
                        <span class="response-question">Question ${qIndex + 1}:</span>
                        <span class="response-answer ${q.correct ? 'correct' : 'incorrect'}">${q.answer} (${q.correct ? '1 point' : '0 point'})</span>
                    `;
                    responses.appendChild(row);
                });
                
                item.appendChild(header);
                item.appendChild(score);
                item.appendChild(responses);
                container.appendChild(item);
            });
        }
        
        // Réinitialisation du formulaire
        document.getElementById('reset-btn').addEventListener('click', function() {
            document.getElementById('quiz-form').reset();
            document.getElementById('current-results').style.display = 'none';
            unlockQuestionnaire();
            startTimer();
        });
        
        // Démarrer le timer au chargement
        startTimer();
        
        // Afficher l'historique vide au départ
        displayHistory();
    </script>
</body>
</html>
