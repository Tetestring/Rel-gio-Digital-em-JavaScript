<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Relógio Digital</title>

    <!--CSS AQUI -->
    <style>
        body{
            margin: 0;
            height: 100vh;
            display: flex;   /*centraliza e orgarniza layout */
            justify-content: center; /*Centraliza horizontalmente (esquerda/direita)*/
            align-items: center; /* centraliz5a verticalmente (cima/baixo)*/
            background: #f17e7e; /*Define a aultura da tela*/
            font-family: Arial, Helvetica, sans-serif; /* Tipo de letra*/
        }

        .relogio{
            color: #dde6e4;
            font-size: 60px;
            background:#0d0e0d;
            padding: 20px 40px;
            border-radius: 10px;
            letter-spacing: 3px;
        }
    </style>
</head>
<body>
    
    <div class= "relogio" id= "relogio">
        00:00:00
    </div>


    <!--JS AQUI-->
    <script>

function atualizarRelogio() {
    const agora = new Date();

    let horas = agora.getHours();
    let minutos = agora.getMinutes();
    let segundos = agora.getSeconds();

    // Coloca zero à esquerda se for menor que 10
    horas = horas < 10 ? "0" + horas : horas;
    minutos = minutos < 10 ? "0" + minutos : minutos;
    segundos = segundos < 10 ? "0" + segundos : segundos;

    document.getElementById("relogio").innerText = horas + ":" + minutos + ":" + segundos;
        }

        // Atualiza a cada 1 segundo
      setInterval(atualizarRelogio, 1000);

      // Chama assim que a página abrir
      atualizarRelogio();
    </script>
    
</body>
</html>
