<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Juego Demo Pixel</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: #222;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: 'Press Start 2P', cursive;
      color: white;
    }

    #game {
      position: relative;
      width: 640px;
      height: 480px;
      background: url('https://i.ibb.co/f4qNMQC/floor.png') repeat; /* piso de madera */
      border: 6px solid #654321;
      box-shadow: 0 0 20px rgba(0,0,0,0.8);
    }

    /* Personaje */
    #player {
      position: absolute;
      width: 32px;
      height: 32px;
      background: url('https://i.ibb.co/F6bKjz1/character.png') no-repeat;
      background-size: cover;
      left: 50px;
      top: 200px;
    }

    /* Puerta */
    #door {
      position: absolute;
      width: 64px;
      height: 64px;
      background: url('https://i.ibb.co/bzYPV0k/door.png') no-repeat;
      background-size: cover;
      right: 50px;
      top: 200px;
    }

    /* UI */
    #hud {
      position: absolute;
      top: 10px;
      left: 50%;
      transform: translateX(-50%);
      background: rgba(0,0,0,0.6);
      padding: 8px 12px;
      border: 2px solid #fff;
      border-radius: 6px;
    }

    input {
      font-family: inherit;
      font-size: 12px;
      padding: 4px;
    }

    button {
      font-family: inherit;
      font-size: 12px;
      padding: 4px 6px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div id="game">
    <div id="hud">
      <p>Esta es ___ bicicleta (David)</p>
      <input type="text" id="answer" placeholder="Tu respuesta...">
      <button onclick="checkAnswer()">Enviar</button>
      <p id="score">Tiempo: 300s | Puntos: 0</p>
    </div>
    <div id="player"></div>
    <div id="door"></div>
  </div>

  <script>
    let score = 0;
    let time = 300;

    function checkAnswer() {
      const input = document.getElementById("answer").value.trim().toLowerCase();
      if (input === "mi") {
        score += 10;
        alert("¡Correcto! La puerta se abre 🎉");
      } else {
        alert("Respuesta incorrecta ❌");
      }
      document.getElementById("score").innerText = `Tiempo: ${time}s | Puntos: ${score}`;
    }

    // Contador
    setInterval(() => {
      if (time > 0) {
        time--;
        document.getElementById("score").innerText = `Tiempo: ${time}s | Puntos: ${score}`;
      }
    }, 1000);
  </script>
</body>
</html>
