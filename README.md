<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Questionnaire</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        input[type="text"], input[type="number"], input[type="date"], select {
            width: 100%;
            padding: 8px;
            box-sizing: border-box;
        }
        .radio-group, .checkbox-group {
            margin: 5px 0;
        }
        .timer {
            font-size: 1.2em;
            font-weight: bold;
            color: #d9534f;
            margin-bottom: 15px;
        }
        button {
            padding: 10px 15px;
            background-color: #5cb85c;
            color: white;
            border: none;
            cursor: pointer;
            margin-right: 10px;
        }
        button:disabled {
            background-color: #cccccc;
            cursor: not-allowed;
        }
        .locked {
            color: #d9534f;
            font-weight: bold;
        }
        #databaseLink {
            display: block;
            margin-top: 20px;
            text-align: center;
            color: #337ab7;
            text-decoration: none;
        }
        #databaseLink:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <h1>Questionnaire</h1>
    <div class="timer" id="timer">Temps restant: 120 secondes</div>
    
    <form id="quizForm">
        <div class="form-group">
            <label>Date de collecte:</label>
            <input type="date" id="collectionDate" name="collectionDate" required>
        </div>
        
        <div class="form-group">
            <label>Nom:</label>
            <input type="text" id="lastName" name="lastName" required>
        </div>
        
        <div class="form-group">
            <label>Prénom:</label>
            <input type="text" id="firstName" name="firstName" required>
        </div>
        
        <div class="form-group">
            <label>Sexe:</label>
            <div class="radio-group">
                <input type="radio" id="male" name="gender" value="Homme" required>
                <label for="male" style="display: inline;">Homme</label>
            </div>
            <div class="radio-group">
                <input type="radio" id="female" name="gender" value="Femme">
                <label for="female" style="display: inline;">Femme</label>
            </div>
        </div>
        
        <div class="form-group">
            <label for="q1">1. Quelle est la capitale du Burkina Faso?</label>
            <input type="text" id="q1" name="q1" required>
        </div>
        
        <div class="form-group">
            <label>2. Quelle est la capitale de la région du Centre-Ouest?</label>
            <div class="radio-group">
                <input type="radio" id="q2_1" name="q2" value="Réo">
                <label for="q2_1" style="display: inline;">Réo</label>
            </div>
            <div class="radio-group">
                <input type="radio" id="q2_2" name="q2" value="Sapouy">
                <label for="q2_2" style="display: inline;">Sapouy</label>
            </div>
            <div class="radio-group">
                <input type="radio" id="q2_3" name="q2" value="Koudougou">
                <label for="q2_3" style="display: inline;">Koudougou</label>
            </div>
            <div class="radio-group">
                <input type="radio" id="q2_4" name="q2" value="Léo">
                <label for="q2_4" style="display: inline;">Léo</label>
            </div>
        </div>
        
        <div class="form-group">
            <label>3. La capitale de la Russie est Moscou:</label>
            <div class="radio-group">
                <input type="radio" id="q3_1" name="q3" value="Vrai">
                <label for="q3_1" style="display: inline;">Vrai</label>
            </div>
            <div class="radio-group">
                <input type="radio" id="q3_2" name="q3" value="Faux">
                <label for="q3_2" style="display: inline;">Faux</label>
            </div>
        </div>
        
        <div class="form-group">
            <label>4. Quelle est la couleur du vin?</label>
            <div class="radio-group">
                <input type="radio" id="q4_1" name="q4" value="vert">
                <label for="q4_1" style="display: inline;">Vert</label>
            </div>
            <div class="radio-group">
                <input type="radio" id="q4_2" name="q4" value="rouge">
                <label for="q4_2" style="display: inline;">Rouge</label>
            </div>
            <div class="radio-group">
                <input type="radio" id="q4_3" name="q4" value="jaune">
                <label for="q4_3" style="display: inline;">Jaune</label>
            </div>
            <div class="radio-group">
                <input type="radio" id="q4_4" name="q4" value="orange">
                <label for="q4_4" style="display: inline;">Orange</label>
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
        
        <div class="form-group">
            <button type="button" id="submitBtn">Envoyer</button>
            <button type="button" id="resetBtn">Réinitialiser</button>
        </div>
        
        <input type="hidden" id="score" name="score">
        <input type="hidden" id="timeSpent" name="timeSpent">
        <input type="hidden" id="submissionTime" name="submissionTime">
    </form>
    
    <a href="#" id="databaseLink">Accéder à la base de données</a>
    
    <script>
        // Réponses correctes
        const correctAnswers = {
            q1: "ouagadougou",
            q2: "koudougou",
            q3: "vrai",
            q4: "rouge",
            q5: "144",
            q6: "françois",
            q7: "17",
            q8: "hervé",
            q9: "1960",
            q10: "lion"
        };
        
        // Variables pour le chronomètre
        let timer;
        let timeLeft = 120;
        let isTimerRunning = false;
        let startTime;
        
        // Éléments du DOM
        const timerElement = document.getElementById('timer');
        const submitBtn = document.getElementById('submitBtn');
        const resetBtn = document.getElementById('resetBtn');
        const quizForm = document.getElementById('quizForm');
        const databaseLink = document.getElementById('databaseLink');
        const inputs = quizForm.querySelectorAll('input[type="text"], input[type="number"], input[type="radio"], input[type="date"]');
        
        // Initialiser la base de données si elle n'existe pas
        if (!localStorage.getItem('quizDatabase')) {
            localStorage.setItem('quizDatabase', JSON.stringify({
                records: [],
                password: "1981"
            }));
        }
        
        // Démarrer le chronomètre lors de la première interaction
        function startTimerOnFirstInteraction() {
            if (!isTimerRunning) {
                startTimer();
                isTimerRunning = true;
                startTime = new Date();
                
                // Retirer les écouteurs après le premier démarrage
                inputs.forEach(input => {
                    input.removeEventListener('focus', startTimerOnFirstInteraction);
                    input.removeEventListener('click', startTimerOnFirstInteraction);
                });
            }
        }
        
        // Ajouter des écouteurs pour démarrer le chronomètre
        inputs.forEach(input => {
            input.addEventListener('focus', startTimerOnFirstInteraction);
            input.addEventListener('click', startTimerOnFirstInteraction);
        });
        
        // Fonction pour démarrer le chronomètre
        function startTimer() {
            timer = setInterval(() => {
                timeLeft--;
                timerElement.textContent = `Temps restant: ${timeLeft} secondes`;
                
                if (timeLeft <= 0) {
                    clearInterval(timer);
                    lockQuestionnaire();
                    timerElement.textContent = "Temps écoulé! Questionnaire verrouillé.";
                    timerElement.classList.add('locked');
                }
            }, 1000);
        }
        
        // Verrouiller le questionnaire
        function lockQuestionnaire() {
            inputs.forEach(input => {
                input.disabled = true;
            });
            submitBtn.disabled = true;
        }
        
        // Calculer le score
        function calculateScore() {
            let score = 0;
            
            // Question 1
            if (document.getElementById('q1').value.trim().toLowerCase() === correctAnswers.q1) {
                score += 1;
            }
            
            // Question 2
            const q2Selected = document.querySelector('input[name="q2"]:checked');
            if (q2Selected && q2Selected.value.toLowerCase() === correctAnswers.q2) {
                score += 1;
            }
            
            // Question 3
            const q3Selected = document.querySelector('input[name="q3"]:checked');
            if (q3Selected && q3Selected.value.toLowerCase() === correctAnswers.q3) {
                score += 1;
            }
            
            // Question 4
            const q4Selected = document.querySelector('input[name="q4"]:checked');
            if (q4Selected && q4Selected.value.toLowerCase() === correctAnswers.q4) {
                score += 1;
            }
            
            // Question 5
            if (document.getElementById('q5').value.trim().toLowerCase() === correctAnswers.q5) {
                score += 1;
            }
            
            // Question 6
            if (document.getElementById('q6').value.trim().toLowerCase() === correctAnswers.q6) {
                score += 1;
            }
            
            // Question 7
            if (document.getElementById('q7').value.trim().toLowerCase() === correctAnswers.q7) {
                score += 1;
            }
            
            // Question 8
            if (document.getElementById('q8').value.trim().toLowerCase() === correctAnswers.q8) {
                score += 1;
            }
            
            // Question 9
            if (document.getElementById('q9').value.trim().toLowerCase() === correctAnswers.q9) {
                score += 1;
            }
            
            // Question 10
            if (document.getElementById('q10').value.trim().toLowerCase() === correctAnswers.q10) {
                score += 1;
            }
            
            return score;
        }
        
        // Calculer le temps passé
        function calculateTimeSpent() {
            if (startTime) {
                const endTime = new Date();
                const timeDiff = endTime - startTime; // en millisecondes
                return Math.floor(timeDiff / 1000); // convertir en secondes
            }
            return 0;
        }
        
        // Envoyer les données
        function submitData() {
            const score = calculateScore();
            const timeSpent = calculateTimeSpent();
            const submissionTime = new Date().toISOString();
            
            // Stocker le score, le temps passé et l'heure de soumission dans des champs cachés
            document.getElementById('score').value = score;
            document.getElementById('timeSpent').value = timeSpent;
            document.getElementById('submissionTime').value = submissionTime;
            
            // Récupérer les données du formulaire
            const formData = new FormData(quizForm);
            const data = {};
            formData.forEach((value, key) => {
                data[key] = value;
            });
            
            // Ajouter l'heure de soumission
            data.submissionTime = submissionTime;
            
            // Enregistrer dans la base de données
            const db = JSON.parse(localStorage.getItem('quizDatabase'));
            db.records.push(data);
            localStorage.setItem('quizDatabase', JSON.stringify(db));
            
            // Afficher le résultat
            alert(`Questionnaire soumis!\nScore: ${score}/10\nTemps passé: ${timeSpent} secondes`);
            
            // Réinitialiser le formulaire
            resetForm();
        }
        
        // Réinitialiser le formulaire
        function resetForm() {
            quizForm.reset();
            clearInterval(timer);
            timeLeft = 120;
            isTimerRunning = false;
            timerElement.textContent = "Temps restant: 120 secondes";
            timerElement.classList.remove('locked');
            
            // Réactiver tous les champs
            inputs.forEach(input => {
                input.disabled = false;
            });
            submitBtn.disabled = false;
            
            // Réattacher les écouteurs pour le prochain démarrage
            inputs.forEach(input => {
                input.addEventListener('focus', startTimerOnFirstInteraction);
                input.addEventListener('click', startTimerOnFirstInteraction);
            });
        }
        
        // Afficher la base de données
        function showDatabase() {
            const password = prompt("Entrez le mot de passe pour accéder à la base de données:");
            const db = JSON.parse(localStorage.getItem('quizDatabase'));
            
            if (password === db.password) {
                // Trier les enregistrements par ordre chronologique (du plus récent au plus ancien)
                const sortedRecords = db.records.sort((a, b) => 
                    new Date(b.submissionTime) - new Date(a.submissionTime));
                
                // Créer une nouvelle fenêtre pour afficher la base de données
                const dbWindow = window.open("", "_blank");
                dbWindow.document.write(`
                    <!DOCTYPE html>
                    <html lang="fr">
                    <head>
                        <meta charset="UTF-8">
                        <meta name="viewport" content="width=device-width, initial-scale=1.0">
                        <title>Base de données - Questionnaire</title>
                        <style>
                            body {
                                font-family: Arial, sans-serif;
                                margin: 20px;
                            }
                            h1 {
                                color: #337ab7;
                                text-align: center;
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
                                position: sticky;
                                top: 0;
                            }
                            tr:nth-child(even) {
                                background-color: #f9f9f9;
                            }
                            tr:hover {
                                background-color: #f1f1f1;
                            }
                            .score-cell {
                                font-weight: bold;
                                text-align: center;
                            }
                            .good-score {
                                color: #5cb85c;
                            }
                            .bad-score {
                                color: #d9534f;
                            }
                        </style>
                    </head>
                    <body>
                        <h1>Base de données des réponses</h1>
                        <table>
                            <thead>
                                <tr>
                                    <th>Date</th>
                                    <th>Nom</th>
                                    <th>Prénom</th>
                                    <th>Sexe</th>
                                    <th>Score</th>
                                    <th>Temps passé</th>
                                </tr>
                            </thead>
                            <tbody>
                                ${sortedRecords.map(record => `
                                    <tr>
                                        <td>${new Date(record.submissionTime).toLocaleString()}</td>
                                        <td>${record.lastName}</td>
                                        <td>${record.firstName}</td>
                                        <td>${record.gender}</td>
                                        <td class="score-cell ${record.score >= 5 ? 'good-score' : 'bad-score'}">${record.score}/10</td>
                                        <td>${record.timeSpent} sec</td>
                                    </tr>
                                `).join('')}
                            </tbody>
                        </table>
                    </body>
                    </html>
                `);
            } else if (password !== null) {
                alert("Mot de passe incorrect!");
            }
        }
        
        // Écouteurs d'événements
        submitBtn.addEventListener('click', submitData);
        resetBtn.addEventListener('click', resetForm);
        databaseLink.addEventListener('click', showDatabase);
    </script>
</body>
</html>
