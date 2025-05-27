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
        .form-container {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        .question {
            margin-bottom: 15px;
            padding: 10px;
            border-bottom: 1px solid #eee;
        }
        .timer {
            text-align: center;
            font-size: 1.2em;
            margin-bottom: 20px;
            color: #333;
        }
        .time-warning {
            color: red;
            font-weight: bold;
        }
        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 15px;
            border: none;
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
        input[type="text"], input[type="number"] {
            padding: 8px;
            margin: 5px 0;
            border: 1px solid #ddd;
            border-radius: 4px;
            width: 100%;
            box-sizing: border-box;
        }
        .locked {
            color: red;
            font-weight: bold;
        }
        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.4);
        }
        .modal-content {
            background-color: #fefefe;
            margin: 15% auto;
            padding: 20px;
            border: 1px solid #888;
            width: 80%;
            max-width: 500px;
            border-radius: 8px;
        }
        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }
        .close:hover {
            color: black;
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
        tr:nth-child(even) {
            background-color: #f9f9f9;
        }
    </style>
</head>
<body>
    <div class="form-container">
        <h1>Questionnaire Général</h1>
        <div class="timer">Temps restant: <span id="time">120</span> secondes</div>
        
        <form id="quizForm">
            <input type="hidden" id="collectionDate" name="collectionDate">
            
            <div class="question">
                <label for="fullName">Nom et Prénom:</label>
                <input type="text" id="fullName" name="fullName" required>
            </div>
            
            <div class="question">
                <label>Sexe:</label><br>
                <input type="radio" id="male" name="gender" value="homme" required>
                <label for="male">Homme</label><br>
                <input type="radio" id="female" name="gender" value="femme">
                <label for="female">Femme</label>
            </div>
            
            <div class="question">
                <label for="q1">1. Quelle est la capitale du Burkina Faso?</label>
                <input type="text" id="q1" name="q1" required>
            </div>
            
            <div class="question">
                <label>2. Quelle est la capitale de la région du Centre-Ouest?</label><br>
                <input type="radio" id="q2a" name="q2" value="Réo">
                <label for="q2a">Réto</label><br>
                <input type="radio" id="q2b" name="q2" value="Sapouy">
                <label for="q2b">Sapouy</label><br>
                <input type="radio" id="q2c" name="q2" value="Koudougou">
                <label for="q2c">Koudougou</label><br>
                <input type="radio" id="q2d" name="q2" value="Léo">
                <label for="q2d">Léo</label>
            </div>
            
            <div class="question">
                <label>3. La capitale de la Russie est Moscou:</label><br>
                <input type="radio" id="q3a" name="q3" value="Vrai">
                <label for="q3a">Vrai</label><br>
                <input type="radio" id="q3b" name="q3" value="Faux">
                <label for="q3b">Faux</label>
            </div>
            
            <div class="question">
                <label>4. Quelle est la couleur du vin?</label><br>
                <input type="radio" id="q4a" name="q4" value="vert">
                <label for="q4a">Vert</label><br>
                <input type="radio" id="q4b" name="q4" value="rouge">
                <label for="q4b">Rouge</label><br>
                <input type="radio" id="q4c" name="q4" value="jaune">
                <label for="q4c">Jaune</label><br>
                <input type="radio" id="q4d" name="q4" value="orange">
                <label for="q4d">Orange</label>
            </div>
            
            <div class="question">
                <label for="q5">5. Quel est le nombre d'os dans le corps humain?</label>
                <input type="number" id="q5" name="q5" required>
            </div>
            
            <div class="question">
                <label for="q6">6. Quel est le nom du pape?</label>
                <input type="text" id="q6" name="q6" required>
            </div>
            
            <div class="question">
                <label for="q7">7. Quel nombre vient après 16?</label>
                <input type="number" id="q7" name="q7" required>
            </div>
            
            <div class="question">
                <label for="q8">8. Quel est le nom du concepteur?</label>
                <input type="text" id="q8" name="q8" required>
            </div>
            
            <div class="question">
                <label for="q9">9. Quelle est l'année de l'indépendance du Burkina Faso?</label>
                <input type="number" id="q9" name="q9" required>
            </div>
            
            <div class="question">
                <label for="q10">10. Quel est le roi des animaux?</label>
                <input type="text" id="q10" name="q10" required>
            </div>
            
            <button type="submit" id="submitBtn">Envoyer les réponses</button>
            <button type="button" id="resetBtn">Nouveau questionnaire</button>
        </form>
        
        <div id="resultContainer" style="display: none; margin-top: 20px;">
            <h2>Résultats</h2>
            <p>Score: <span id="score">0</span>/10</p>
            <p>Accédez à toutes les réponses consolidées avec ce <a href="#" id="resultsLink">lien codé</a>.</p>
        </div>
    </div>

    <!-- Modal pour le code d'accès -->
    <div id="codeModal" class="modal">
        <div class="modal-content">
            <span class="close">&times;</span>
            <h2>Accès aux résultats</h2>
            <p>Veuillez entrer le code d'accès :</p>
            <input type="password" id="accessCode" placeholder="Code d'accès">
            <button id="validateCode">Valider</button>
            <p id="codeError" style="color: red; display: none;">Code incorrect. Veuillez réessayer.</p>
        </div>
    </div>

    <!-- Modal pour afficher les résultats consolidés -->
    <div id="resultsModal" class="modal">
        <div class="modal-content" style="width: 90%; max-width: 800px;">
            <span class="close">&times;</span>
            <h2>Résultats Consolidés</h2>
            <div id="resultsTable"></div>
        </div>
    </div>

    <script>
        // Définir les réponses correctes
        const correctAnswers = {
            q1: "ouagadougou",
            q2: "Koudougou",
            q3: "Vrai",
            q4: "rouge",
            q5: "206",
            q6: "françois",
            q7: "17",
            q8: "hervé",
            q9: "1960",
            q10: "lion"
        };

        // Initialiser le timer
        let timeLeft = 120;
        let timer;
        let formLocked = false;

        // Définir la date de collecte
        document.getElementById('collectionDate').value = new Date().toISOString().split('T')[0];

        // Démarrer le timer
        function startTimer() {
            timer = setInterval(function() {
                timeLeft--;
                document.getElementById('time').textContent = timeLeft;
                
                if (timeLeft <= 30) {
                    document.getElementById('time').className = 'time-warning';
                }
                
                if (timeLeft <= 0) {
                    clearInterval(timer);
                    lockForm();
                }
            }, 1000);
        }

        // Verrouiller le formulaire
        function lockForm() {
            formLocked = true;
            document.getElementById('time').textContent = "0";
            document.getElementById('time').className = 'locked';
            
            const inputs = document.querySelectorAll('input');
            inputs.forEach(input => {
                input.disabled = true;
            });
            
            document.getElementById('submitBtn').disabled = true;
            alert("Le temps est écoulé! Le questionnaire est verrouillé.");
        }

        // Calculer le score
        function calculateScore(formData) {
            let score = 0;
            
            // Question 1
            if (formData.get('q1').toLowerCase() === correctAnswers.q1) score++;
            
            // Question 2
            if (formData.get('q2') === correctAnswers.q2) score++;
            
            // Question 3
            if (formData.get('q3') === correctAnswers.q3) score++;
            
            // Question 4
            if (formData.get('q4') === correctAnswers.q4) score++;
            
            // Question 5
            if (formData.get('q5') === correctAnswers.q5) score++;
            
            // Question 6
            if (formData.get('q6').toLowerCase() === correctAnswers.q6) score++;
            
            // Question 7
            if (formData.get('q7') === correctAnswers.q7) score++;
            
            // Question 8
            if (formData.get('q8').toLowerCase() === correctAnswers.q8) score++;
            
            // Question 9
            if (formData.get('q9') === correctAnswers.q9) score++;
            
            // Question 10
            if (formData.get('q10').toLowerCase() === correctAnswers.q10) score++;
            
            return score;
        }

        // Envoyer les données
        function sendData(formData, score) {
            // Stocker les données localement
            const allResults = JSON.parse(localStorage.getItem('quizResults') || '[]');
            allResults.push({
                date: formData.get('collectionDate'),
                nom: formData.get('fullName'),
                sexe: formData.get('gender'),
                reponses: {
                    q1: formData.get('q1'),
                    q2: formData.get('q2'),
                    q3: formData.get('q3'),
                    q4: formData.get('q4'),
                    q5: formData.get('q5'),
                    q6: formData.get('q6'),
                    q7: formData.get('q7'),
                    q8: formData.get('q8'),
                    q9: formData.get('q9'),
                    q10: formData.get('q10')
                },
                score: score
            });
            localStorage.setItem('quizResults', JSON.stringify(allResults));
            
            return true;
        }

        // Réinitialiser le formulaire
        function resetForm() {
            document.getElementById('quizForm').reset();
            document.getElementById('resultContainer').style.display = 'none';
            timeLeft = 120;
            formLocked = false;
            document.getElementById('time').textContent = timeLeft;
            document.getElementById('time').className = '';
            
            const inputs = document.querySelectorAll('input');
            inputs.forEach(input => {
                input.disabled = false;
            });
            
            document.getElementById('submitBtn').disabled = false;
            clearInterval(timer);
            startTimer();
        }

        // Afficher les résultats consolidés
        function showConsolidatedResults() {
            const results = JSON.parse(localStorage.getItem('quizResults') || '[]');
            const resultsTable = document.getElementById('resultsTable');
            
            if (results.length === 0) {
                resultsTable.innerHTML = "<p>Aucun résultat disponible pour le moment.</p>";
                return;
            }
            
            let html = '<table>';
            html += '<tr><th>Date</th><th>Nom</th><th>Sexe</th><th>Score</th><th>Détails</th></tr>';
            
            results.forEach(result => {
                html += `<tr>
                    <td>${result.date}</td>
                    <td>${result.nom}</td>
                    <td>${result.sexe}</td>
                    <td>${result.score}/10</td>
                    <td><button class="view-details" data-id="${results.indexOf(result)}">Voir</button></td>
                </tr>`;
            });
            
            html += '</table>';
            resultsTable.innerHTML = html;
            
            // Ajouter les événements pour les boutons "Voir"
            document.querySelectorAll('.view-details').forEach(button => {
                button.addEventListener('click', function() {
                    const resultId = this.getAttribute('data-id');
                    const result = results[resultId];
                    
                    let detailsHtml = `<h3>Détails des réponses - ${result.nom}</h3>`;
                    detailsHtml += `<p>Date: ${result.date} | Sexe: ${result.sexe} | Score: ${result.score}/10</p>`;
                    detailsHtml += '<table>';
                    detailsHtml += '<tr><th>Question</th><th>Réponse donnée</th><th>Réponse correcte</th></tr>';
                    
                    // Question 1
                    detailsHtml += `<tr>
                        <td>1. Capitale du Burkina Faso</td>
                        <td>${result.reponses.q1}</td>
                        <td>${correctAnswers.q1}</td>
                    </tr>`;
                    
                    // Question 2
                    detailsHtml += `<tr>
                        <td>2. Capitale du Centre-Ouest</td>
                        <td>${result.reponses.q2}</td>
                        <td>${correctAnswers.q2}</td>
                    </tr>`;
                    
                    // Question 3
                    detailsHtml += `<tr>
                        <td>3. Capitale de la Russie</td>
                        <td>${result.reponses.q3}</td>
                        <td>${correctAnswers.q3}</td>
                    </tr>`;
                    
                    // Question 4
                    detailsHtml += `<tr>
                        <td>4. Couleur du vin</td>
                        <td>${result.reponses.q4}</td>
                        <td>${correctAnswers.q4}</td>
                    </tr>`;
                    
                    // Question 5
                    detailsHtml += `<tr>
                        <td>5. Nombre d'os</td>
                        <td>${result.reponses.q5}</td>
                        <td>${correctAnswers.q5}</td>
                    </tr>`;
                    
                    // Question 6
                    detailsHtml += `<tr>
                        <td>6. Nom du pape</td>
                        <td>${result.reponses.q6}</td>
                        <td>${correctAnswers.q6}</td>
                    </tr>`;
                    
                    // Question 7
                    detailsHtml += `<tr>
                        <td>7. Nombre après 16</td>
                        <td>${result.reponses.q7}</td>
                        <td>${correctAnswers.q7}</td>
                    </tr>`;
                    
                    // Question 8
                    detailsHtml += `<tr>
                        <td>8. Nom du concepteur</td>
                        <td>${result.reponses.q8}</td>
                        <td>${correctAnswers.q8}</td>
                    </tr>`;
                    
                    // Question 9
                    detailsHtml += `<tr>
                        <td>9. Indépendance Burkina Faso</td>
                        <td>${result.reponses.q9}</td>
                        <td>${correctAnswers.q9}</td>
                    </tr>`;
                    
                    // Question 10
                    detailsHtml += `<tr>
                        <td>10. Roi des animaux</td>
                        <td>${result.reponses.q10}</td>
                        <td>${correctAnswers.q10}</td>
                    </tr>`;
                    
                    detailsHtml += '</table>';
                    
                    // Afficher les détails dans une alerte (pour simplifier)
                    alert(detailsHtml);
                });
            });
            
            document.getElementById('resultsModal').style.display = 'block';
        }

        // Gérer la soumission du formulaire
        document.getElementById('quizForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            if (formLocked) {
                alert("Le questionnaire est verrouillé. Temps écoulé.");
                return;
            }
            
            const formData = new FormData(this);
            const score = calculateScore(formData);
            
            // Envoyer les données
            if (sendData(formData, score)) {
                // Afficher le résultat
                document.getElementById('score').textContent = score;
                document.getElementById('resultContainer').style.display = 'block';
                
                // Configurer le lien codé
                document.getElementById('resultsLink').onclick = function(e) {
                    e.preventDefault();
                    document.getElementById('codeModal').style.display = 'block';
                };
                
                // Réinitialiser pour un nouveau questionnaire
                setTimeout(resetForm, 3000);
            }
        });

        // Gérer le bouton de réinitialisation
        document.getElementById('resetBtn').addEventListener('click', resetForm);

        // Gérer la modal de code d'accès
        document.getElementById('validateCode').addEventListener('click', function() {
            const enteredCode = document.getElementById('accessCode').value;
            
            if (enteredCode === "1981") {
                document.getElementById('codeModal').style.display = 'none';
                document.getElementById('codeError').style.display = 'none';
                showConsolidatedResults();
            } else {
                document.getElementById('codeError').style.display = 'block';
            }
        });

        // Fermer les modals
        document.querySelectorAll('.close').forEach(closeBtn => {
            closeBtn.addEventListener('click', function() {
                this.closest('.modal').style.display = 'none';
            });
        });

        // Fermer les modals en cliquant à l'extérieur
        window.addEventListener('click', function(event) {
            if (event.target.className === 'modal') {
                event.target.style.display = 'none';
            }
        });

        // Démarrer le timer au chargement
        startTimer();
    </script>
</body>
</html>
