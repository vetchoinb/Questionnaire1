<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Questionnaire</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f5f7fa;
            margin: 0;
            padding: 20px;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            background: white;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0,0,0,0.1);
            overflow: hidden;
        }
        header {
            background: #2c3e50;
            color: white;
            padding: 20px;
            text-align: center;
        }
        h1 {
            margin: 0;
            font-size: 28px;
        }
        .timer-container {
            background: #e74c3c;
            color: white;
            padding: 10px;
            text-align: center;
            font-size: 18px;
            font-weight: bold;
        }
        .form-content {
            padding: 25px;
        }
        .form-group {
            margin-bottom: 20px;
            padding: 15px;
            background: #f8f9fa;
            border-radius: 5px;
            border-left: 4px solid #3498db;
        }
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
        }
        input[type="text"],
        input[type="number"] {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            box-sizing: border-box;
            font-size: 16px;
        }
        .radio-group {
            margin: 10px 0;
        }
        .radio-option {
            margin: 8px 0;
            display: flex;
            align-items: center;
        }
        .radio-option input {
            margin-right: 10px;
        }
        .submit-btn {
            background: #27ae60;
            color: white;
            border: none;
            padding: 12px 25px;
            font-size: 16px;
            border-radius: 5px;
            cursor: pointer;
            width: 100%;
            transition: background 0.3s;
        }
        .submit-btn:hover {
            background: #219653;
        }
        .results-link {
            text-align: center;
            margin-top: 20px;
            display: none;
        }
        .results-link a {
            color: #2980b9;
            text-decoration: none;
            font-weight: bold;
        }
        .locked {
            opacity: 0.7;
            pointer-events: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Questionnaire de Connaissances Générales</h1>
            <div id="current-date">Date de collecte: </div>
        </header>
        
        <div class="timer-container" id="timer">
            Temps restant: 02:00
        </div>
        
        <div class="form-content">
            <form id="quiz-form">
                <div class="form-group">
                    <label for="lastname">Nom:</label>
                    <input type="text" id="lastname" name="lastname" required>
                </div>
                
                <div class="form-group">
                    <label for="firstname">Prénom:</label>
                    <input type="text" id="firstname" name="firstname" required>
                </div>
                
                <div class="form-group">
                    <label>Sexe:</label>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" id="male" name="gender" value="male" required>
                            <label for="male">Homme</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" id="female" name="gender" value="female">
                            <label for="female">Femme</label>
                        </div>
                    </div>
                </div>
                
                <!-- Questions -->
                <div class="form-group">
                    <label for="q1">1. Quelle est la capitale du Burkina Faso?</label>
                    <input type="text" id="q1" name="q1" required>
                </div>
                
                <div class="form-group">
                    <label>2. Quelle est la capitale de la région du Centre-Ouest?</label>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" id="q2-1" name="q2" value="Réo" required>
                            <label for="q2-1">Réo</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" id="q2-2" name="q2" value="Sapouy">
                            <label for="q2-2">Sapouy</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" id="q2-3" name="q2" value="Koudougou">
                            <label for="q2-3">Koudougou</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" id="q2-4" name="q2" value="Léo">
                            <label for="q2-4">Léo</label>
                        </div>
                    </div>
                </div>
                
                <div class="form-group">
                    <label>3. "La capitale de la Russie est Moscou"</label>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" id="q3-1" name="q3" value="Vrai" required>
                            <label for="q3-1">Vrai</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" id="q3-2" name="q3" value="Faux">
                            <label for="q3-2">Faux</label>
                        </div>
                    </div>
                </div>
                
                <div class="form-group">
                    <label>4. Quelle est la couleur du vin?</label>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" id="q4-1" name="q4" value="vert" required>
                            <label for="q4-1">Vert</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" id="q4-2" name="q4" value="rouge">
                            <label for="q4-2">Rouge</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" id="q4-3" name="q4" value="jaune">
                            <label for="q4-3">Jaune</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" id="q4-4" name="q4" value="orange">
                            <label for="q4-4">Orange</label>
                        </div>
                    </div>
                </div>
                
                <div class="form-group">
                    <label for="q5">5. Combien d'os compte le corps humain?</label>
                    <input type="number" id="q5" name="q5" required>
                </div>
                
                <div class="form-group">
                    <label for="q6">6. Quel est le nom du pape actuel?</label>
                    <input type="text" id="q6" name="q6" required>
                </div>
                
                <div class="form-group">
                    <label for="q7">7. Quel nombre vient immédiatement après 16?</label>
                    <input type="number" id="q7" name="q7" required>
                </div>
                
                <div class="form-group">
                    <label for="q8">8. Quel est le nom du concepteur de ce questionnaire?</label>
                    <input type="text" id="q8" name="q8" required>
                </div>
                
                <div class="form-group">
                    <label for="q9">9. En quelle année le Burkina Faso a-t-il obtenu son indépendance?</label>
                    <input type="number" id="q9" name="q9" required>
                </div>
                
                <div class="form-group">
                    <label for="q10">10. Quel animal est souvent considéré comme le roi des animaux?</label>
                    <input type="text" id="q10" name="q10" required>
                </div>
                
                <button type="submit" class="submit-btn" id="submit-btn">Soumettre le questionnaire</button>
            </form>
            
            <div class="results-link" id="results-link">
                <p>Vos réponses ont été enregistrées. <a href="#" id="results-anchor">Afficher les résultats (Code requis)</a></p>
            </div>
        </div>
    </div>

    <script>
        // Afficher la date actuelle
        document.addEventListener('DOMContentLoaded', function() {
            const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };
            const today = new Date();
            document.getElementById('current-date').textContent += today.toLocaleDateString('fr-FR', options);
            
            // Gestion du timer
            let timeLeft = 120;
            const timerElement = document.getElementById('timer');
            const quizForm = document.getElementById('quiz-form');
            
            const countdown = setInterval(() => {
                const minutes = Math.floor(timeLeft / 60);
                const seconds = timeLeft % 60;
                
                timerElement.textContent = `Temps restant: ${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
                
                if (timeLeft <= 0) {
                    clearInterval(countdown);
                    timerElement.textContent = "Temps écoulé!";
                    quizForm.classList.add('locked');
                    alert("Le temps imparti est écoulé. Le questionnaire est maintenant verrouillé.");
                }
                timeLeft--;
            }, 1000);
            
            // Gestion de la soumission
            quizForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                // Calcul du score
                let score = 0;
                const answers = {
                    q1: document.getElementById('q1').value.trim().toLowerCase(),
                    q2: document.querySelector('input[name="q2"]:checked')?.value,
                    q3: document.querySelector('input[name="q3"]:checked')?.value,
                    q4: document.querySelector('input[name="q4"]:checked')?.value,
                    q5: parseInt(document.getElementById('q5').value),
                    q6: document.getElementById('q6').value.trim().toLowerCase(),
                    q7: parseInt(document.getElementById('q7').value),
                    q8: document.getElementById('q8').value.trim().toLowerCase(),
                    q9: parseInt(document.getElementById('q9').value),
                    q10: document.getElementById('q10').value.trim().toLowerCase()
                };
                
                // Vérification des réponses
                if (answers.q1 === "ouagadougou") score++;
                if (answers.q2 === "Koudougou") score++;
                if (answers.q3 === "Vrai") score++;
                if (answers.q4 === "rouge") score++;
                if (answers.q5 === 206) score++; // Note: 206 os dans le corps humain
                if (answers.q6 === "françois") score++;
                if (answers.q7 === 17) score++;
                if (answers.q8 === "hervé") score++;
                if (answers.q9 === 1960) score++;
                if (answers.q10 === "lion") score++;
                
                // Stockage des résultats
                const userData = {
                    nom: document.getElementById('lastname').value,
                    prenom: document.getElementById('firstname').value,
                    score: score,
                    date: today.toLocaleDateString('fr-FR', options),
                    tempsRestant: timeLeft
                };
                
                localStorage.setItem(`quiz_result_${userData.nom}_${userData.prenom}`, JSON.stringify(userData));
                
                // Affichage des résultats
                document.getElementById('results-link').style.display = 'block';
                quizForm.reset();
                
                alert(`Merci d'avoir participé!\nVotre score: ${score}/10`);
            });
            
            // Accès aux résultats
            document.getElementById('results-anchor').addEventListener('click', function(e) {
                e.preventDefault();
                const code = prompt("Veuillez entrer le code d'accès:");
                
                if (code === "1981") {
                    // Récupérer tous les résultats
                    const allResults = [];
                    for (let i = 0; i < localStorage.length; i++) {
                        const key = localStorage.key(i);
                        if (key.startsWith('quiz_result_')) {
                            allResults.push(JSON.parse(localStorage.getItem(key)));
                        }
                    }
                    
                    // Afficher les résultats
                    const resultsWindow = window.open('', '_blank');
                    resultsWindow.document.write(`
                        <!DOCTYPE html>
                        <html>
                        <head>
                            <title>Résultats du Questionnaire</title>
                            <style>
                                body { font-family: Arial, sans-serif; padding: 20px; }
                                h1 { color: #2c3e50; }
                                table { width: 100%; border-collapse: collapse; margin-top: 20px; }
                                th, td { padding: 12px; text-align: left; border-bottom: 1px solid #ddd; }
                                th { background-color: #3498db; color: white; }
                                tr:nth-child(even) { background-color: #f2f2f2; }
                            </style>
                        </head>
                        <body>
                            <h1>Résultats Consolidés</h1>
                            <table>
                                <tr>
                                    <th>Nom</th>
                                    <th>Prénom</th>
                                    <th>Score</th>
                                    <th>Date</th>
                                </tr>
                                ${allResults.map(result => `
                                    <tr>
                                        <td>${result.nom}</td>
                                        <td>${result.prenom}</td>
                                        <td>${result.score}/10</td>
                                        <td>${result.date}</td>
                                    </tr>
                                `).join('')}
                            </table>
                        </body>
                        </html>
                    `);
                    resultsWindow.document.close();
                } else {
                    alert("Code incorrect. Accès refusé.");
                }
            });
        });
    </script>
</body>
</html>
