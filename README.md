<!DOCTYPE html>
<html>
<head>
  <title>Calculadora de Média</title>
  <style>
    #resultado {
      font-size: 18px;
    }
  </style>
</head>
<body>

  <label for="nota1">Nota 1:</label>
  <input type="number" id="nota1"><br><br>
  
  <label for="nota2">Nota 2:</label>
  <input type="number" id="nota2"><br><br>
  
  <button onclick="calcularMedia()">Calcular Média</button><br><br>
  
  <span>Média: <span id="media"></span></span><br>
  <span>Situação: <span id="situacao"></span></span>
  
  <script>
    function calcularMedia() {
      const nota1 = parseFloat(document.getElementById('nota1').value);
      const nota2 = parseFloat(document.getElementById('nota2').value);

      const media = (nota1 + nota2) / 2;
      let situacao, cor;

      if (media >= 6) {
        situacao = 'Aprovado';
        cor = 'blue';
      } else {
        situacao = 'Reprovado';
        cor = 'red';
      }

      document.getElementById('media').innerHTML = media.toFixed(2);
      document.getElementById('situacao').innerHTML = situacao;
      document.getElementById('situacao').style.color = cor;
    }
  </script>
</body>
</html>
