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
            line-height: 1.6;
        }
        .form-group {
            margin-bottom: 15px;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        input[type="text"], input[type="number"], input[type="date"], select {
            width: 100%;
            padding: 8px;
            margin-top: 5px;
            box-sizing: border-box;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        .radio-group {
            margin: 8px 0;
        }
        .timer {
            font-size: 1.2em;
            font-weight: bold;
            color: #d9534f;
            margin: 15px 0;
            padding: 10px;
            background-color: #f8f9fa;
            border-radius: 4px;
            text-align: center;
        }
        .locked {
            background-color: #f2dede;
        }
        button {
            padding: 10px 15px;
            margin: 5px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }
        #submitBtn {
            background-color: #5cb85c;
            color: white;
        }
        #resetBtn {
            background-color: #f0ad4e;
            color: white;
        }
        button:disabled {
            background-color: #cccccc;
            cursor: not-allowed;
        }
        #databaseLink {
            display: inline-block;
            margin-top: 20px;
            padding: 10px 15px;
            background-color: #337ab7;
            color: white;
            text-decoration: none;
            border-radius: 4px;
        }
        #databaseLink:hover {
            background-color: #286090;
        }
    </style>
</head>
<body>
    <h1>Questionnaire Général</h1>
    <div class="timer" id="timer">Temps restant: 02:00</div>
    
    <form id="quizForm">
        <div class="form-group">
            <label for="collectionDate">Date de collecte:</label>
            <input type="date" id="collectionDate" name="collectionDate" required>
        </div>
        
        <div class="form-group">
            <label for="lastName">Nom:</label>
            <input type="text" id="lastName" name="lastName" required>
        </div>
        
        <div class="form-group">
            <label for="firstName">Prénom:</label>
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
        
        <div style="text-align: center; margin-top: 20px;">
            <button type="button" id="submitBtn">Envoyer les réponses</button>
            <button type="button" id="resetBtn">Réinitialiser</button>
        </div>
        
        <input type="hidden" id="score" name="score">
        <input type="hidden" id="timeSpent" name="timeSpent">
        <input type="hidden" id="submissionTime" name="submissionTime">
    </form>
    
    <div style="text-align: center; margin-top: 30px;">
        <a href="resultat.html" id="databaseLink">Accéder aux résultats (Mot de passe requis)</a>
    </div>
    
    <script>
        // Réponses correctes (insensible à la casse)
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
        let timeLeft = 120; // 2 minutes en secondes
        let isTimerRunning = false;
        let startTime;
        
        // Éléments du DOM
        const timerElement = document.getElementById('timer');
        const submitBtn = document.getElementById('submitBtn');
        const resetBtn = document.getElementById('resetBtn');
        const quizForm = document.getElementById('quizForm');
        const inputs = quizForm.querySelectorAll('input[type="text"], input[type="number"], input[type="radio"], input[type="date"]');
        
        // Initialiser le stockage local si nécessaire
        if (!localStorage.getItem('quizResults')) {
            localStorage.setItem('quizResults', JSON.stringify([]));
        }
        
        // Démarrer le chronomètre à la première interaction
        function startTimerOnFirstInteraction() {
            if (!isTimerRunning) {
                startTimer();
                isTimerRunning = true;
                startTime = new Date();
                
                // Retirer les écouteurs après le démarrage
                inputs.forEach(input => {
                    input.removeEventListener('focus', startTimerOnFirstInteraction);
                    input.removeEventListener('click', startTimerOnFirstInteraction);
                });
            }
        }
        
        // Ajouter des écouteurs d'événements pour démarrer le timer
        inputs.forEach(input => {
            input.addEventListener('focus', startTimerOnFirstInteraction);
            input.addEventListener('click', startTimerOnFirstInteraction);
        });
        
        // Formatage du temps (mm:ss)
        function formatTime(seconds) {
            const mins = Math.floor(seconds / 60).toString().padStart(2, '0');
            const secs = (seconds % 60).toString().padStart(2, '0');
            return `${mins}:${secs}`;
        }
        
        // Démarrer le chronomètre
        function startTimer() {
            timer = setInterval(() => {
                timeLeft--;
                timerElement.textContent = `Temps restant: ${formatTime(timeLeft)}`;
                
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
            if (document.getElementById('q1').value.trim().toLowerCase() === correctAnswers.q1) score++;
            
            // Question 2
            const q2Selected = document.querySelector('input[name="q2"]:checked');
            if (q2Selected && q2Selected.value.toLowerCase() === correctAnswers.q2) score++;
            
            // Question 3
            const q3Selected = document.querySelector('input[name="q3"]:checked');
            if (q3Selected && q3Selected.value.toLowerCase() === correctAnswers.q3) score++;
            
            // Question 4
            const q4Selected = document.querySelector('input[name="q4"]:checked');
            if (q4Selected && q4Selected.value.toLowerCase() === correctAnswers.q4) score++;
            
            // Question 5
            if (document.getElementById('q5').value.trim().toLowerCase() === correctAnswers.q5) score++;
            
            // Question 6
            if (document.getElementById('q6').value.trim().toLowerCase() === correctAnswers.q6) score++;
            
            // Question 7
            if (document.getElementById('q7').value.trim().toLowerCase() === correctAnswers.q7) score++;
            
            // Question 8
            if (document.getElementById('q8').value.trim().toLowerCase() === correctAnswers.q8) score++;
            
            // Question 9
            if (document.getElementById('q9').value.trim().toLowerCase() === correctAnswers.q9) score++;
            
            // Question 10
            if (document.getElementById('q10').value.trim().toLowerCase() === correctAnswers.q10) score++;
            
            return score;
        }
        
        // Calculer le temps passé
        function calculateTimeSpent() {
            if (startTime) {
                const endTime = new Date();
                return Math.floor((endTime - startTime) / 1000); // en secondes
            }
            return 0;
        }
        
        // Envoyer les données
        function submitData() {
            const score = calculateScore();
            const timeSpent = calculateTimeSpent();
            const submissionTime = new Date().toISOString();
            
            // Stocker les métadonnées
            document.getElementById('score').value = score;
            document.getElementById('timeSpent').value = timeSpent;
            document.getElementById('submissionTime').value = submissionTime;
            
            // Collecter toutes les données du formulaire
            const formData = new FormData(quizForm);
            const result = {};
            
            formData.forEach((value, key) => {
                result[key] = value;
            });
            
            // Ajouter l'horodatage
            result.submissionTime = submissionTime;
            
            // Enregistrer dans le stockage local
            const results = JSON.parse(localStorage.getItem('quizResults'));
            results.push(result);
            localStorage.setItem('quizResults', JSON.stringify(results));
            
            // Afficher le résultat
            alert(`Merci pour votre participation!\nVotre score: ${score}/10\nTemps passé: ${timeSpent} secondes`);
            
            // Réinitialiser le formulaire
            resetForm();
        }
        
        // Réinitialiser le formulaire
        function resetForm() {
            quizForm.reset();
            clearInterval(timer);
            timeLeft = 120;
            isTimerRunning = false;
            timerElement.textContent = "Temps restant: 02:00";
            timerElement.classList.remove('locked');
            
            // Réactiver les champs
            inputs.forEach(input => {
                input.disabled = false;
            });
            submitBtn.disabled = false;
            
            // Réattacher les écouteurs pour le prochain questionnaire
            inputs.forEach(input => {
                input.addEventListener('focus', startTimerOnFirstInteraction);
                input.addEventListener('click', startTimerOnFirstInteraction);
            });
        }
        
        // Écouteurs d'événements
        submitBtn.addEventListener('click', submitData);
        resetBtn.addEventListener('click', resetForm);
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Résultats du Questionnaire</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f5f5f5;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        h1 {
            color: #2c3e50;
            text-align: center;
            margin-bottom: 30px;
        }
        .password-form {
            max-width: 400px;
            margin: 50px auto;
            padding: 20px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            text-align: center;
        }
        .password-form input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        .password-form button {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 4px;
            cursor: pointer;
        }
        .password-form button:hover {
            background-color: #2980b9;
        }
        .error {
            color: #e74c3c;
            margin-top: 10px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 12px;
            text-align: left;
        }
        th {
            background-color: #3498db;
            color: white;
            position: sticky;
            top: 0;
        }
        tr:nth-child(even) {
            background-color: #f2f2f2;
        }
        tr:hover {
            background-color: #e9e9e9;
        }
        .score {
            font-weight: bold;
            text-align: center;
        }
        .high-score {
            color: #27ae60;
        }
        .medium-score {
            color: #f39c12;
        }
        .low-score {
            color: #e74c3c;
        }
        .stats {
            margin: 20px 0;
            padding: 15px;
            background-color: #ecf0f1;
            border-radius: 4px;
        }
        .export-btn {
            background-color: #2ecc71;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 4px;
            cursor: pointer;
            margin: 10px 0;
        }
        .export-btn:hover {
            background-color: #27ae60;
        }
    </style>
</head>
<body>
    <div class="container" id="passwordContainer">
        <div class="password-form">
            <h2>Accès aux résultats</h2>
            <p>Veuillez entrer le mot de passe pour accéder aux données</p>
            <input type="password" id="passwordInput" placeholder="Mot de passe">
            <button id="loginBtn">Accéder</button>
            <div id="errorMsg" class="error"></div>
        </div>
    </div>
    
    <div class="container" id="resultsContainer" style="display: none;">
        <h1>Résultats du Questionnaire</h1>
        
        <div class="stats">
            <h3>Statistiques globales</h3>
            <p id="totalSubmissions">Nombre total de soumissions: 0</p>
            <p id="averageScore">Score moyen: 0/10</p>
            <p id="bestScore">Meilleur score: 0/10</p>
            <button id="exportBtn" class="export-btn">Exporter les données (CSV)</button>
        </div>
        
        <div style="overflow-x: auto;">
            <table id="resultsTable">
                <thead>
                    <tr>
                        <th>Date/Heure</th>
                        <th>Nom</th>
                        <th>Prénom</th>
                        <th>Sexe</th>
                        <th>Score</th>
                        <th>Temps (s)</th>
                        <th>Détails</th>
                    </tr>
                </thead>
                <tbody id="resultsBody">
                    <!-- Les données seront insérées ici par JavaScript -->
                </tbody>
            </table>
        </div>
    </div>
    
    <script>
        // Éléments du DOM
        const passwordContainer = document.getElementById('passwordContainer');
        const resultsContainer = document.getElementById('resultsContainer');
        const passwordInput = document.getElementById('passwordInput');
        const loginBtn = document.getElementById('loginBtn');
        const errorMsg = document.getElementById('errorMsg');
        const resultsBody = document.getElementById('resultsBody');
        const totalSubmissions = document.getElementById('totalSubmissions');
        const averageScore = document.getElementById('averageScore');
        const bestScore = document.getElementById('bestScore');
        const exportBtn = document.getElementById('exportBtn');
        
        // Mot de passe
        const CORRECT_PASSWORD = "1981";
        
        // Vérifier le mot de passe
        loginBtn.addEventListener('click', () => {
            if (passwordInput.value === CORRECT_PASSWORD) {
                passwordContainer.style.display = 'none';
                resultsContainer.style.display = 'block';
                loadResults();
            } else {
                errorMsg.textContent = "Mot de passe incorrect. Veuillez réessayer.";
            }
        });
        
        // Permettre aussi la validation avec Entrée
        passwordInput.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') {
                loginBtn.click();
            }
        });
        
        // Charger les résultats depuis le localStorage
        function loadResults() {
            const results = JSON.parse(localStorage.getItem('quizResults')) || [];
            
            // Trier par date (du plus récent au plus ancien)
            results.sort((a, b) => new Date(b.submissionTime) - new Date(a.submissionTime));
            
            // Afficher les statistiques
            totalSubmissions.textContent = `Nombre total de soumissions: ${results.length}`;
            
            if (results.length > 0) {
                const scores = results.map(r => parseInt(r.score));
                const sum = scores.reduce((a, b) => a + b, 0);
                const avg = (sum / results.length).toFixed(1);
                const max = Math.max(...scores);
                
                averageScore.textContent = `Score moyen: ${avg}/10`;
                bestScore.textContent = `Meilleur score: ${max}/10`;
            }
            
            // Afficher les résultats dans le tableau
            resultsBody.innerHTML = '';
            
            results.forEach(result => {
                const row = document.createElement('tr');
                
                // Déterminer la classe CSS pour le score
                let scoreClass = 'low-score';
                if (result.score >= 7) scoreClass = 'high-score';
                else if (result.score >= 4) scoreClass = 'medium-score';
                
                row.innerHTML = `
                    <td>${new Date(result.submissionTime).toLocaleString()}</td>
                    <td>${result.lastName}</td>
                    <td>${result.firstName}</td>
                    <td>${result.gender}</td>
                    <td class="score ${scoreClass}">${result.score}/10</td>
                    <td>${result.timeSpent}</td>
                    <td><button onclick="showDetails('${result.submissionTime}')">Voir</button></td>
                `;
                
                resultsBody.appendChild(row);
            });
        }
        
        // Afficher les détails d'une soumission
        function showDetails(submissionTime) {
            const results = JSON.parse(localStorage.getItem('quizResults')) || [];
            const result = results.find(r => r.submissionTime === submissionTime);
            
            if (result) {
                let details = `Détails de la soumission du ${new Date(result.submissionTime).toLocaleString()}\n\n`;
                details += `Nom: ${result.lastName} ${result.firstName}\n`;
                details += `Sexe: ${result.gender}\n`;
                details += `Score: ${result.score}/10\n`;
                details += `Temps passé: ${result.timeSpent} secondes\n\n`;
                
                // Ajouter les réponses aux questions
                for (let i = 1; i <= 10; i++) {
                    details += `Question ${i}: ${result['q'+i] || 'Non répondue'}\n`;
                }
                
                alert(details);
            }
        }
        
        // Exporter les données en CSV
        exportBtn.addEventListener('click', () => {
            const results = JSON.parse(localStorage.getItem('quizResults')) || [];
            
            if (results.length === 0) {
                alert("Aucune donnée à exporter.");
                return;
            }
            
            // Créer l'en-tête CSV
            let csv = "Date;Nom;Prénom;Sexe;Score;Temps (s)\n";
            
            // Ajouter les données
            results.forEach(result => {
                csv += `"${new Date(result.submissionTime).toLocaleString()}";`;
                csv += `"${result.lastName}";`;
                csv += `"${result.firstName}";`;
                csv += `"${result.gender}";`;
                csv += `"${result.score}";`;
                csv += `"${result.timeSpent}"\n`;
            });
            
            // Créer un blob et un lien de téléchargement
            const blob = new Blob([csv], { type: 'text/csv;charset=utf-8;' });
            const url = URL.createObjectURL(blob);
            const link = document.createElement('a');
            link.href = url;
            link.setAttribute('download', `resultats_questionnaire_${new Date().toISOString().slice(0,10)}.csv`);
            document.body.appendChild(link);
            link.click();
            document.body.removeChild(link);
        });
    </script>
</body>
</html>
