<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Presentación | Alex Lulichac</title>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&family=Roboto:wght@300;400&display=swap" rel="stylesheet">
  <style>
    body {
      background: linear-gradient(120deg, #011627 0%, #043957 40%, #0ff1 90%);
      min-height: 100vh;
      margin: 0;
      font-family: 'Roboto', Arial, sans-serif;
      color: #fff;
      overflow-x: hidden;
      position: relative;
    }
    .container {
      max-width: 650px;
      margin: 7vh auto 0 auto;
      background: rgba(10, 22, 50, 0.91);
      border-radius: 25px;
      box-shadow: 0 0 40px 0 #00f2fe88, 0 0 10px #4f8efc44, 0 0 60px #f0f;
      padding: 2.7rem 2.2rem 3.5rem 2.2rem;
      position: relative;
      z-index: 2;
      animation: fadeInUp 1.2s cubic-bezier(.32,0,.67,0.97);
      overflow: hidden;
    }
    h1 {
      font-family: 'Orbitron', sans-serif;
      font-size: 2.8rem;
      letter-spacing: 2px;
      background: linear-gradient(90deg, #0ff 20%, #00f2fe 65%, #ff2dff 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      text-shadow: 0 2px 22px #00f2fe99;
      margin-bottom: 0.6rem;
      animation: neonBlink 1.3s infinite alternate;
    }
    h2 {
      font-family: 'Orbitron', sans-serif;
      font-size: 1.4rem;
      font-weight: 700;
      color: #00f2fe;
      margin-bottom: 1.2rem;
      letter-spacing: 1px;
      animation: fadeInLeft 1.5s cubic-bezier(.55,.06,.68,.19);
      text-shadow: 0 0 8px #0ff, 0 0 4px #1ff;
    }
    p {
      font-size: 1.15rem;
      line-height: 1.7;
      color: #e6ecfa;
      margin-bottom: 1.5rem;
      animation: fadeInRight 1.6s cubic-bezier(.55,.06,.68,.19);
      text-shadow: 0 0 8px #00f8, 0 0 4px #0ff4;
    }
    .glow {
      position: absolute;
      pointer-events: none;
      width: 340px;
      height: 340px;
      border-radius: 50%;
      background: radial-gradient(circle, #00f2fe77 50%, #0ff1110 100%);
      top: -90px;
      right: -80px;
      z-index: 1;
      filter: blur(50px);
      animation: pulseGlow 4s infinite alternate;
    }
    .neon-border {
      border: 2.5px solid #00f2fe;
      box-shadow: 0 0 20px #00f2fe88, 0 0 40px #0ff3, 0 0 30px #ff2dff99;
      border-radius: 25px;
      padding: 1.2rem;
      margin-top: 2rem;
      animation: borderPulse 2.5s infinite alternate;
      position: relative;
      z-index: 2;
    }
    .neon-bar {
      width: 90px;
      height: 6px;
      border-radius: 4px;
      background: linear-gradient(90deg, #00f2fe, #ff2dff, #0ff);
      margin: 16px auto 28px auto;
      box-shadow: 0 0 24px #0ff, 0 0 16px #ff2dff;
      animation: barMove 2.7s infinite linear;
    }
    @keyframes barMove {
      0% { box-shadow: 0 0 24px #0ff, 0 0 16px #ff2dff;}
      50% { box-shadow: 0 0 40px #0ff, 0 0 40px #ff2dff;}
      100% { box-shadow: 0 0 24px #0ff, 0 0 16px #ff2dff;}
    }

    /* Imagenes flotantes */
    .floating-images {
      display: flex;
      justify-content: space-around;
      align-items: center;
      margin-bottom: 2.5rem;
      position: relative;
      z-index: 3;
      gap: 18px;
      flex-wrap: wrap;
    }
    .floating-img {
      width: 90px;
      height: 90px;
      object-fit: contain;
      border-radius: 20px;
      border: 2.5px solid #00f2fe;
      box-shadow: 0 0 24px #0ff9, 0 0 18px #ff2dff55, 0 0 10px #fff2;
      background: rgba(5, 15, 35, 0.7);
      animation: float 3.1s ease-in-out infinite, hueRotate 7s linear infinite;
      transition: transform 0.22s;
    }
    .floating-img:hover {
      transform: scale(1.08) rotate(-4deg);
      box-shadow: 0 0 36px #ff2dffcc, 0 0 30px #00f2feaa;
    }
    .floating-img:nth-child(2) { animation-delay: 1.1s; }
    .floating-img:nth-child(3) { animation-delay: 2.1s; }
    .floating-img:nth-child(4) { animation-delay: 1.7s; }

    @keyframes float {
      0%, 100% { transform: translateY(0) scale(1);}
      50% { transform: translateY(-22px) scale(1.06);}
    }
    @keyframes hueRotate {
      0% { filter: hue-rotate(0deg);}
      100% { filter: hue-rotate(360deg);}
    }

    /* Animaciones generales */
    @keyframes fadeInUp {
      0% { opacity: 0; transform: translateY(60px);}
      100% { opacity: 1; transform: translateY(0);}
    }
    @keyframes fadeInLeft {
      0% { opacity: 0; transform: translateX(-40px);}
      100% { opacity: 1; transform: translateX(0);}
    }
    @keyframes fadeInRight {
      0% { opacity: 0; transform: translateX(40px);}
      100% { opacity: 1; transform: translateX(0);}
    }
    @keyframes neonBlink {
      0% { text-shadow: 0 0 20px #00f2fe, 0 0 32px #0ff8;}
      100% { text-shadow: 0 0 44px #ff2dff, 0 0 54px #0ff;}
    }
    @keyframes pulseGlow {
      0% { opacity: 0.7; transform: scale(1);}
      100% { opacity: 1; transform: scale(1.18);}
    }
    @keyframes borderPulse {
      0% { box-shadow: 0 0 8px #00f2fe88, 0 0 24px #0ff2, 0 0 16px #ff2dff77; }
      100% { box-shadow: 0 0 32px #00f2fecc, 0 0 64px #0ff3, 0 0 48px #ff2dffcc;}
    }
    /* Neon circuit lines */
    .circuit {
      position: absolute;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      z-index: 0;
      pointer-events: none;
      overflow: hidden;
    }
    .circuit svg {
      width: 100%;
      height: 100%;
      opacity: 0.18;
      filter: drop-shadow(0 0 14px #0ff8);
      animation: circuitGlow 2.7s infinite alternate;
    }
    @keyframes circuitGlow {
      0% { filter: drop-shadow(0 0 10px #0ff);}
      100% { filter: drop-shadow(0 0 30px #ff2dff);}
    }
    /* Responsive */
    @media (max-width: 800px) {
      .container { max-width: 97vw; }
      .floating-img { width: 70px; height: 70px;}
      .glow { width: 160px; height: 160px; top: -30px; right: -30px;}
    }
    @media (max-width: 520px) {
      .container { padding: 0.6rem 0.2rem 1.5rem 0.2rem; }
      .neon-bar { width: 60px;}
    }
  </style>
</head>
<body>
  <div class="glow"></div>
  <div class="circuit">
    <svg viewBox="0 0 700 400" preserveAspectRatio="none">
      <polyline points="50,50 150,50 150,150 250,150" stroke="#0ff" stroke-width="2" fill="none" />
      <polyline points="400,200 550,200 550,70 670,70" stroke="#ff2dff" stroke-width="2" fill="none" />
      <polyline points="100,380 100,300 280,300" stroke="#0ff" stroke-width="2" fill="none" />
      <polyline points="350,400 350,320 600,320" stroke="#ff2dff" stroke-width="2" fill="none" />
      <circle cx="250" cy="150" r="4" fill="#fff" />
      <circle cx="600" cy="320" r="5" fill="#ff2dff" />
    </svg>
  </div>
  <div class="container neon-border">
    <h1>Alex Lulichac</h1>
    <div class="neon-bar"></div>
    <h2>Estudiante de Computación</h2>
    <div class="floating-images">
      <img class="floating-img" src="https://cdn-icons-png.flaticon.com/512/2721/2721290.png" alt="Icono PC" title="Computadora">
      <img class="floating-img" src="https://cdn-icons-png.flaticon.com/512/2721/2721317.png" alt="Icono Código" title="Código">
      <img class="floating-img" src="https://cdn-icons-png.flaticon.com/512/2721/2721307.png" alt="Icono Circuito" title="Circuito">
      <img class="floating-img" src="https://cdn-icons-png.flaticon.com/512/2721/2721322.png" alt="Icono Inteligencia Artificial" title="IA">
    </div>
    <p>
      ¡Hola! Soy <strong>Alex Lulichac</strong> y actualmente estudio la carrera de Computación en el <b>Instituto Computrom</b>. Me apasiona la tecnología, la innovación y el desarrollo de soluciones que puedan mejorar nuestro futuro.
    </p>
    <p>
      Me motiva aprender nuevas tecnologías y participar en proyectos que me permitan crecer como profesional y aportar a la evolución digital. Disfruto explorar áreas como la inteligencia artificial, la robótica, el desarrollo web y la electrónica.
    </p>
    <p style="text-align:center;font-size:1.12rem;">
      <span style="color:#00f2fe;text-shadow: 0 0 10px #0ff, 0 0 4px #fff;">¡Bienvenido/a a mi presentación personal futurista!</span>
    </p>
  </div>
</body>
</html>
