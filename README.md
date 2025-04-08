<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gerador de Lorem Ipsum</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <h1>Gerador de Lorem Ipsum</h1>
  <p class="sub">Clique no botão para gerar um parágrafo de texto fictício.</p>
  
  <div class="buttons">
    <button onclick="gerarLorem()">Gerar Texto</button>
    <button onclick="copiarTexto()">Copiar Texto</button>
    <button onclick="limparTexto()">Limpar Texto</button>
  </div>

  <div class="output" id="resultado">
    <!-- Resultado será exibido aqui -->
  </div>

  <script>
    function gerarLorem() {
      const lorem = `Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. 
Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. 
Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.`;

      document.getElementById("resultado").textContent = lorem;
    }

    function copiarTexto() {
      const texto = document.getElementById("resultado").textContent;
      if (texto.trim() !== "") {
        navigator.clipboard.writeText(texto)
          .then(() => alert("Texto copiado com sucesso!"))
          .catch(err => alert("Erro ao copiar texto."));
      } else {
        alert("Não há texto para copiar.");
      }
    }

    function limparTexto() {
      document.getElementById("resultado").textContent = "";
    }
  </script>
</body>
</html>
