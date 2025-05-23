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
        .radio-group, .checkbox-group {
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
        }
        button:hover {
            background-color: #45a049;
        }
        button:disabled {
            background-color: #cccccc;
            cursor: not-allowed;
        }
        .results {
            display: none;
            margin-top: 20px;
            padding: 15px;
            background-color: #e8f5e9;
            border-radius: 5px;
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
        
        <div class="results" id="results">
            <h3>Résultats:</h3>
            <p id="score-display"></p>
            <p>Les réponses consolidées sont disponibles sur le <a href="#" id="results-link">site web</a>.</p>
        </div>
    </div>

    <script>
        // Afficher la date actuelle
        const now = new Date();
        const options = { year: 'numeric', month: 'long', day: 'numeric' };
        document.getElementById('date-display').textContent = 'Date de collecte: ' + now.toLocaleDateString('fr-FR', options);
        
        // Configuration du timer
        let timeLeft = 120; // 2 minutes en secondes
        const timer = setInterval(updateTimer, 1000);
        
        function updateTimer() {
            timeLeft--;
            const minutes = Math.floor(timeLeft / 60);
            const seconds = timeLeft % 60;
            document.getElementById('time').textContent = 
                (minutes < 10 ? '0' : '') + minutes + ':' + (seconds < 10 ? '0' : '') + seconds;
            
            if (timeLeft <= 0) {
                clearInterval(timer);
                document.getElementById('quiz-form').querySelectorAll('input').forEach(input => {
                    input.disabled = true;
                });
                document.getElementById('submit-btn').disabled = true;
                alert('Le temps est écoulé! Le questionnaire est maintenant verrouillé.');
            }
        }
        
        // Gestion de la soumission du formulaire
        document.getElementById('quiz-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Calcul du score
            let score = 0;
            
            // Question 1
            const q1 = document.getElementById('q1').value.trim().toLowerCase();
            if (q1 === 'ouagadougou') score += 1;
            
            // Question 2
            const q2 = document.querySelector('input[name="q2"]:checked');
            if (q2 && q2.value === 'Koudougou') score += 1;
            
            // Question 3
            const q3 = document.querySelector('input[name="q3"]:checked');
            if (q3 && q3.value === 'Vrai') score += 1;
            
            // Question 4
            const q4 = document.querySelector('input[name="q4"]:checked');
            if (q4 && q4.value === 'rouge') score += 1;
            
            // Question 5
            const q5 = document.getElementById('q5').value.trim();
            if (q5 === '144') score += 1;
            
            // Question 6
            const q6 = document.getElementById('q6').value.trim().toLowerCase();
            if (q6 === 'françois') score += 1;
            
            // Question 7
            const q7 = document.getElementById('q7').value.trim();
            if (q7 === '17') score += 1;
            
            // Question 8
            const q8 = document.getElementById('q8').value.trim().toLowerCase();
            if (q8 === 'hervé') score += 1;
            
            // Question 9
            const q9 = document.getElementById('q9').value.trim();
            if (q9 === '1960') score += 1;
            
            // Question 10
            const q10 = document.getElementById('q10').value.trim().toLowerCase();
            if (q10 === 'lion') score += 1;
            
            // Afficher les résultats
            document.getElementById('score-display').textContent = `Votre score: ${score}/10`;
            document.getElementById('results').style.display = 'block';
            
            // Configurer le lien des résultats
            document.getElementById('results-link').href = `https://votresiteweb.com/resultats?code=1981&score=${score}`;
            
            // Désactiver le bouton de soumission
            document.getElementById('submit-btn').disabled = true;
        });
        
        // Réinitialisation du formulaire
        document.getElementById('reset-btn').addEventListener('click', function() {
            document.getElementById('quiz-form').reset();
            document.getElementById('results').style.display = 'none';
            document.getElementById('submit-btn').disabled = false;
            
            // Réinitialiser le timer
            timeLeft = 120;
            document.getElementById('time').textContent = '02:00';
            
            // Réactiver tous les champs
            document.getElementById('quiz-form').querySelectorAll('input').forEach(input => {
                input.disabled = false;
            });
        });
    </script>
</body>
</html>
