# mes-et-mais
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exercices - Mais vs Mes</title>
    <style>
        .correct { color: green; }
        .incorrect { color: red; }
        .feedback { margin-top: 5px; }
    </style>
    <script>
        function verifier() {
            let reponsesCorrectes = ["mais", "mes", "mais", "mes", "mais", "mes", "mes", "mais", "mes", "mais", "mes", "mais", "mes", "mes", "mais", "mais", "mes", "mes", "mais", "mes"];
            let score = 0;

            for (let i = 0; i < reponsesCorrectes.length; i++) {
                let userInput = document.getElementById('reponse' + (i + 1)).value.trim().toLowerCase();
                let feedback = document.getElementById('feedback' + (i + 1));

                if (userInput === reponsesCorrectes[i]) {
                    feedback.innerText = "✅ Correct";
                    feedback.className = "correct feedback";
                    score++;
                } else {
                    feedback.innerText = `❌ Incorrect. La bonne réponse est "${reponsesCorrectes[i]}". Rappel : "mais" est une conjonction indiquant une opposition (ex: Je veux venir, mais je suis occupé), tandis que "mes" est un adjectif possessif (ex: Mes livres sont sur la table).`;
                    feedback.className = "incorrect feedback";
                }
            }

            document.getElementById('score').innerText = `Votre score : ${score}/${reponsesCorrectes.length}`;
        }
    </script>
</head>
<body>
    <h2>Exercices - Complétez avec "mais" ou "mes"</h2>

    <p><strong>Règle :</strong> "Mais" est une conjonction de coordination qui exprime une opposition ou une restriction. "Mes" est un adjectif possessif qui désigne quelque chose qui appartient à la première personne du singulier (moi). Exemples : "Je veux venir, mais je suis occupé." (opposition) et "Mes livres sont sur la table." (possession).</p>

    <form>
        <ol>
            <li>Je voudrais venir, ___ je ne peux pas. <input type="text" id="reponse1"> <span id="feedback1"></span></li>
            <li>___ amis sont très sympathiques. <input type="text" id="reponse2"> <span id="feedback2"></span></li>
            <li>Il est gentil, ___ parfois un peu distrait. <input type="text" id="reponse3"> <span id="feedback3"></span></li>
            <li>J'ai oublié ___ clés sur la table. <input type="text" id="reponse4"> <span id="feedback4"></span></li>
            <li>Je veux bien essayer, ___ je ne promets rien. <input type="text" id="reponse5"> <span id="feedback5"></span></li>
            <li>Où sont ___ chaussures ? <input type="text" id="reponse6"> <span id="feedback6"></span></li>
            <li>___ parents sont partis en voyage. <input type="text" id="reponse7"> <span id="feedback7"></span></li>
            <li>Il est tard, ___ nous devons partir. <input type="text" id="reponse8"> <span id="feedback8"></span></li>
            <li>J'ai perdu ___ lunettes encore une fois. <input type="text" id="reponse9"> <span id="feedback9"></span></li>
            <li>Je suis fatigué, ___ je dois finir ce travail. <input type="text" id="reponse10"> <span id="feedback10"></span></li>
            <li>___ professeurs sont très compréhensifs. <input type="text" id="reponse11"> <span id="feedback11"></span></li>
            <li>Il voulait venir, ___ il a eu un empêchement. <input type="text" id="reponse12"> <span id="feedback12"></span></li>
            <li>___ livres sont tous rangés. <input type="text" id="reponse13"> <span id="feedback13"></span></li>
            <li>___ enfants aiment jouer dehors. <input type="text" id="reponse14"> <span id="feedback14"></span></li>
            <li>Je veux t'aider, ___ je ne sais pas comment. <input type="text" id="reponse15"> <span id="feedback15"></span></li>
            <li>Il voulait m'appeler, ___ il a oublié. <input type="text" id="reponse16"> <span id="feedback16"></span></li>
            <li>J'ai mis ___ affaires dans le sac. <input type="text" id="reponse17"> <span id="feedback17"></span></li>
            <li>___ projets sont très ambitieux. <input type="text" id="reponse18"> <span id="feedback18"></span></li>
            <li>Il pleut, ___ je sortirai quand même. <input type="text" id="reponse19"> <span id="feedback19"></span></li>
            <li>___ idées sont vraiment intéressantes. <input type="text" id="reponse20"> <span id="feedback20"></span></li>
        </ol>

        <button type="button" onclick="verifier()">Vérifier</button>
    </form>

    <p id="score"></p>
</body>
</html>
