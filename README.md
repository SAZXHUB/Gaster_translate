<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gaster's Translation</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
        }
        textarea {
            width: 100%;
            height: 100px;
        }
        #output {
            margin-top: 20px;
            font-size: 24px;
            word-wrap: break-word;
        }
    </style>
</head>
<body>
    <h1>Gaster's Translation</h1>
    <textarea id="input" placeholder="Enter English text here"></textarea>
    <button id="translateBtn">Translate</button>
    <div id="output"></div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const translationMap = {
                'A': '✌', 'B': '👌', 'C': '👍', 'D': '👎', 'E': '👉', 'F': '👆', 'G': '☝', 'H': '🖐',
                'I': '🖐', 'J': '😊', 'K': '😐', 'L': '😕', 'M': '💣', 'N': '☠', 'O': '✋', 'P': '👁',
                'Q': '✈', 'R': '☀', 'S': '💧', 'T': '❄', 'U': '✞', 'V': '†', 'W': '✠', 'X': '✇',
                'Y': '✡', 'Z': '☪'
            };

            function translate() {
                const input = document.getElementById('input').value.toUpperCase();
                let output = '';
                for (let char of input) {
                    if (translationMap[char]) {
                        output += translationMap[char];
                    } else if (char === ' ') {
                        output += ' ';
                    } else {
                        output += char;
                    }
                }
                document.getElementById('output').textContent = output;
            }

            document.getElementById('translateBtn').addEventListener('click', translate);
        });
    </script>
</body>
</html>
