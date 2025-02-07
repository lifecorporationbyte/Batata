# Batata
Batata
<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Labirinto Secreto</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; background-color: black; color: white; }
        #labirinto { 
            width: 300px; height: 300px; 
            border: 2px solid white; 
            display: flex; flex-wrap: wrap; 
            margin: 20px auto; position: relative;
        }
        .palavra { 
            width: 30%; height: 30px; 
            display: flex; justify-content: center; align-items: center; 
            border: 1px solid gray; font-size: 14px; cursor: pointer; 
        }
        #respostaBox { margin-top: 20px; }
        #respostaInput { padding: 5px; font-size: 16px; }
        #responderBtn { padding: 5px 10px; font-size: 16px; cursor: pointer; }
        .secreto { position: absolute; bottom: 10px; right: 10px; font-size: 5px; color: black; }
    </style>
</head>
<body>

    <h1>Encontre a Palavra Correta</h1>
    <div id="labirinto">
        <div class="palavra">sombra</div>
        <div class="palavra">vento</div>
        <div class="palavra">anfitrião</div>
        <div class="palavra">chama</div>
        <div class="palavra">código</div>
        <div class="palavra">energia</div>
        <div class="palavra">oculto</div>
        <div class="palavra">neblina</div>
        <div class="palavra">mistério</div>
        <a href="secreto.html" class="secreto">x</a>
    </div>

    <div id="respostaBox">
        <input type="text" id="respostaInput" placeholder="Digite a palavra certa">
        <button id="responderBtn">Responder</button>
    </div>

    <script>
        document.getElementById("responderBtn").addEventListener("click", function() {
            let resposta = document.getElementById("respostaInput").value.toLowerCase();
            if (resposta === "energia") {
                window.location.href = "https://www.google.com/search?q=anfitrião";
            } else {
                alert("Resposta errada. Tente novamente.");
            }
        });
    </script>

</body>
</html>
