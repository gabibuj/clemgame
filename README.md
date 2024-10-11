<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Validation du RevPAR</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; padding-top: 50px; }
        input, button { font-size: 18px; padding: 10px; }
        #message { margin-top: 20px; font-weight: bold; }
    </style>
</head>
<body>
    <h1>Validation du RevPAR</h1>
    <input type="number" id="revparInput" placeholder="Entrez le RevPAR">
    <button onclick="validateRevPAR()">Valider</button>
    <div id="message"></div>

    <script>
        function validateRevPAR() {
            const correctRevPAR = 8450; // Exemple : 243,15€
            const input = document.getElementById('revparInput').value;
            const message = document.getElementById('message');

            if (parseInt(input) === correctRevPAR) {
                message.style.color = 'green';
                message.innerHTML = 'Félicitations ! Vous avez trouvé le bon RevPAR. Votre cadeau vous attend à la réception.';
            } else {
                message.style.color = 'red';
                message.innerHTML = 'Désolé, ce n\'est pas le bon RevPAR. Essayez encore !';
            }
        }
    </script>
</body>
</html>
