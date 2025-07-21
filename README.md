<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Evaluación Escolar 3er Grado - Perú</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Comic Sans MS', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #FF9E7D, #FFD166, #06D6A0, #118AB2, #073B4C);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            color: #333;
            background-size: 400% 400%;
            animation: gradientBG 15s ease infinite;
        }
        
        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        .container {
            width: 100%;
            max-width: 900px;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
            overflow: hidden;
            position: relative;
            border: 5px solid #FFD166;
        }
        
        .header {
            background: linear-gradient(to right, #EF476F, #FFD166);
            color: white;
            padding: 25px;
            text-align: center;
            position: relative;
            border-bottom: 5px solid #06D6A0;
        }
        
        .header h1 {
            font-size: 2.2rem;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            color: #073B4C;
        }
        
        .header p {
            font-size: 1.1rem;
            opacity: 0.9;
            color: #073B4C;
            font-weight: bold;
        }
        
        .logo {
            position: absolute;
            top: 15px;
            left: 20px;
            background: white;
            border-radius: 50%;
            width: 70px;
            height: 70px;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            border: 3px solid #EF476F;
        }
        
        .logo i {
            font-size: 2.5rem;
            color: #EF476F;
        }
        
        .screen {
            padding: 30px;
            display: none;
        }
        
        .active {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .welcome-screen {
            text-align: center;
            background: url('https://images.unsplash.com/photo-1523240795612-9a054b0db644?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8Y2hpbGRyZW58fHx8fHwxNzIwOTU4NzI0&ixlib=rb-4.0.3&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=600') center/cover no-repeat;
            border-radius: 15px;
            padding: 40px 20px;
            position: relative;
        }
        
        .welcome-overlay {
            background: rgba(255, 255, 255, 0.85);
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .gender-icons {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin: 30px 0;
        }
        
        .gender-icons i {
            font-size: 6rem;
            border-radius: 50%;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .girl-icon {
            background-color: #FF9E7D;
            color: #EF476F;
        }
        
        .boy-icon {
            background-color: #118AB2;
            color: #073B4C;
        }
        
        .input-group {
            margin: 25px 0;
        }
        
        .input-group label {
            display: block;
            margin-bottom: 10px;
            font-size: 1.2rem;
            font-weight: 500;
            color: #073B4C;
        }
        
        .input-group input {
            width: 100%;
            max-width: 400px;
            padding: 15px;
            border: 2px solid #06D6A0;
            border-radius: 50px;
            font-size: 1.1rem;
            text-align: center;
            margin: 0 auto;
            display: block;
            transition: all 0.3s;
            background-color: #FFFAF0;
        }
        
        .input-group input:focus {
            border-color: #EF476F;
            box-shadow: 0 0 10px rgba(239, 71, 111, 0.3);
            outline: none;
        }
        
        .btn {
            background: linear-gradient(to right, #118AB2, #073B4C);
            color: white;
            border: none;
            padding: 15px 40px;
            font-size: 1.2rem;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s;
            margin: 15px 5px;
            font-weight: 600;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            position: relative;
            overflow: hidden;
        }
        
        .btn:after {
            content: '';
            position: absolute;
            top: -50%;
            left: -60%;
            width: 20px;
            height: 200%;
            background: rgba(255, 255, 255, 0.3);
            transform: rotate(30deg);
            transition: all 0.8s;
        }
        
        .btn:hover:after {
            left: 120%;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
        }
        
        .btn:active {
            transform: translateY(1px);
        }
        
        .btn-start {
            background: linear-gradient(to right, #06D6A0, #118AB2);
        }
        
        .btn-subject {
            width: 100%;
            max-width: 300px;
            padding: 20px;
            margin: 15px auto;
            display: block;
            text-align: center;
            font-size: 1.3rem;
            border-radius: 15px;
            background: linear-gradient(to right, #FF9E7D, #EF476F);
            border: 3px solid #FFD166;
            color: white;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
            transition: all 0.3s;
        }
        
        .btn-subject:hover {
            transform: scale(1.05);
        }
        
        .btn-subject:nth-child(2) {
            background: linear-gradient(to right, #118AB2, #06D6A0);
        }
        
        .btn-subject:nth-child(3) {
            background: linear-gradient(to right, #FFD166, #FF9E7D);
        }
        
        .question-container {
            margin: 20px 0;
            background: rgba(255, 255, 255, 0.7);
            padding: 20px;
            border-radius: 15px;
            border: 2px dashed #06D6A0;
        }
        
        .question-number {
            font-size: 1.1rem;
            color: #EF476F;
            margin-bottom: 10px;
            font-weight: bold;
        }
        
        .question {
            font-size: 1.4rem;
            margin-bottom: 25px;
            font-weight: 600;
            color: #073B4C;
            line-height: 1.4;
        }
        
        .options-container {
            display: grid;
            grid-template-columns: 1fr;
            gap: 15px;
            margin: 25px 0;
        }
        
        .option {
            background-color: #FFFAF0;
            border: 2px solid #FFD166;
            border-radius: 12px;
            padding: 15px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .option:hover {
            background-color: #E0F7FA;
            border-color: #118AB2;
            transform: translateX(5px);
        }
        
        .option.selected {
            background-color: #C8F7DC;
            border-color: #06D6A0;
            transform: scale(1.02);
            box-shadow: 0 0 10px rgba(6, 214, 160, 0.3);
        }
        
        .progress-container {
            background-color: #E9ECEF;
            border-radius: 10px;
            height: 20px;
            margin: 30px 0;
            overflow: hidden;
            border: 2px solid #118AB2;
        }
        
        .progress-bar {
            height: 100%;
            background: linear-gradient(to right, #EF476F, #FF9E7D);
            width: 0%;
            transition: width 0.5s ease;
        }
        
        .result-screen {
            text-align: center;
            background: url('https://images.unsplash.com/photo-1508780709619-79562169bc64?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8Y2VsZWJyYXRpb258fHx8fHwxNzIwOTU5MTM5&ixlib=rb-4.0.3&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=600') center/cover no-repeat;
            border-radius: 15px;
        }
        
        .result-overlay {
            background: rgba(255, 255, 255, 0.9);
            border-radius: 15px;
            padding: 30px;
        }
        
        .result-icon {
            font-size: 6rem;
            margin: 20px 0;
            color: #FFD166;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        .result-title {
            font-size: 2.5rem;
            margin: 20px 0;
            color: #EF476F;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.2);
        }
        
        .score {
            font-size: 5rem;
            font-weight: 700;
            color: #118AB2;
            margin: 20px 0;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
        }
        
        .result-text {
            font-size: 1.4rem;
            margin: 20px 0;
            color: #073B4C;
            line-height: 1.6;
        }
        
        .grade-box {
            background: #FFFAF0;
            border-radius: 15px;
            padding: 20px;
            margin: 20px auto;
            max-width: 500px;
            border: 3px solid #06D6A0;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .grade-title {
            font-size: 1.5rem;
            color: #EF476F;
            margin-bottom: 15px;
        }
        
        .grade-item {
            display: flex;
            justify-content: space-between;
            padding: 10px;
            border-bottom: 1px solid #06D6A0;
        }
        
        .grade-item:last-child {
            border-bottom: none;
        }
        
        .grade-label {
            font-weight: bold;
            color: #118AB2;
        }
        
        .btn-restart {
            background: linear-gradient(to right, #06D6A0, #118AB2);
            padding: 15px 50px;
            font-size: 1.3rem;
        }
        
        .btn-menu {
            background: linear-gradient(to right, #FF9E7D, #EF476F);
        }
        
        .btn-email {
            background: linear-gradient(to right, #FFD166, #FF9E7D);
        }
        
        .btn-delete {
            background: linear-gradient(to right, #EF476F, #FF6B6B);
            margin-top: 20px;
        }
        
        .btn-history {
            background: linear-gradient(to right, #118AB2, #06D6A0);
            margin-top: 10px;
        }
        
        .email-options {
            margin-top: 30px;
            padding: 20px;
            background: rgba(255, 255, 255, 0.7);
            border-radius: 15px;
            max-width: 500px;
            margin: 30px auto;
        }
        
        .email-option {
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 15px 0;
            padding: 15px;
            background: #E0F7FA;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s;
            border: 2px solid #118AB2;
        }
        
        .email-option:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            background: #B2EBF2;
        }
        
        .email-icon {
            font-size: 2.5rem;
            margin-right: 15px;
        }
        
        .gmail { color: #dd4b39; }
        
        .email-text {
            font-size: 1.2rem;
            font-weight: 500;
            color: #073B4C;
        }
        
        .subject-title {
            text-align: center;
            color: #EF476F;
            margin-bottom: 30px;
            font-size: 1.8rem;
            padding-bottom: 15px;
            border-bottom: 3px solid #FFD166;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.1);
        }
        
        .subject-icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
            display: block;
            color: #118AB2;
        }
        
        .timer {
            font-size: 1.2rem;
            text-align: center;
            padding: 10px;
            background: linear-gradient(to right, #EF476F, #FF9E7D);
            color: white;
            border-radius: 50px;
            margin: 10px auto;
            width: 100px;
            border: 2px solid white;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.2);
        }
        
        .email-confirmation {
            background: #FFFAF0;
            border-radius: 15px;
            padding: 25px;
            margin: 25px auto;
            max-width: 500px;
            text-align: center;
            border: 3px solid #06D6A0;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .email-confirmation i {
            font-size: 4rem;
            color: #06D6A0;
            margin-bottom: 20px;
        }
        
        .pin-popup {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            display: none;
        }
        
        .pin-content {
            background: white;
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            max-width: 400px;
            width: 90%;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            border: 3px solid #EF476F;
        }
        
        .pin-title {
            font-size: 1.8rem;
            color: #EF476F;
            margin-bottom: 20px;
        }
        
        .pin-input {
            width: 100%;
            padding: 15px;
            font-size: 1.5rem;
            text-align: center;
            margin: 20px 0;
            border: 2px solid #06D6A0;
            border-radius: 10px;
            letter-spacing: 5px;
        }
        
        .pin-btn {
            padding: 12px 30px;
            font-size: 1.2rem;
            margin: 0 10px;
        }
        
        .decoration {
            position: absolute;
            width: 100px;
            height: 100px;
            z-index: -1;
            font-size: 4rem;
            color: #FFD166;
            text-shadow: 0 0 10px rgba(0,0,0,0.2);
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .decoration-1 {
            top: 10%;
            left: 5%;
            animation: float 6s infinite ease-in-out;
        }
        
        .decoration-2 {
            top: 20%;
            right: 5%;
            animation: float 8s infinite ease-in-out;
        }
        
        .decoration-3 {
            bottom: 10%;
            left: 10%;
            animation: float 7s infinite ease-in-out;
        }
        
        .decoration-4 {
            bottom: 15%;
            right: 10%;
            animation: float 9s infinite ease-in-out;
        }
        
        @keyframes float {
            0% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(10deg); }
            100% { transform: translateY(0) rotate(0deg); }
        }
        
        /* Fondos temáticos para cada materia */
        .math-theme .question-container {
            background: url('https://images.unsplash.com/photo-1509228468518-180dd4864904?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80') center/cover;
            background-color: rgba(255, 255, 255, 0.7);
        }
        
        .com-theme .question-container {
            background: url('https://images.unsplash.com/photo-1495446815901-a7297e633e8d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80') center/cover;
            background-color: rgba(255, 255, 255, 0.7);
        }
        
        .sci-theme .question-container {
            background: url('https://images.unsplash.com/photo-1532094349884-543bc11b234d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80') center/cover;
            background-color: rgba(255, 255, 255, 0.7);
        }
        
        /* Pantalla de historial */
        #historyScreen {
            max-height: 80vh;
            overflow-y: auto;
        }
        
        .history-container {
            background: rgba(255, 255, 255, 0.8);
            border-radius: 15px;
            padding: 20px;
            margin: 20px 0;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .history-title {
            text-align: center;
            color: #118AB2;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #FFD166;
            font-size: 1.8rem;
        }
        
        .history-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        
        .history-table th {
            background: #06D6A0;
            color: white;
            padding: 12px;
            text-align: left;
        }
        
        .history-table td {
            padding: 10px;
            border-bottom: 1px solid #06D6A0;
        }
        
        .history-table tr:nth-child(even) {
            background-color: #f2f9f7;
        }
        
        .history-table tr:hover {
            background-color: #e0f7fa;
        }
        
        .no-history {
            text-align: center;
            padding: 30px;
            font-size: 1.2rem;
            color: #EF476F;
        }
        
        @media (max-width: 600px) {
            .header h1 {
                font-size: 1.8rem;
                padding-left: 60px;
                padding-right: 20px;
            }
            
            .header p {
                font-size: 1rem;
            }
            
            .logo {
                width: 50px;
                height: 50px;
            }
            
            .logo i {
                font-size: 1.8rem;
            }
            
            .question {
                font-size: 1.2rem;
            }
            
            .option {
                font-size: 1rem;
                padding: 12px;
            }
            
            .btn {
                padding: 12px 30px;
                font-size: 1.1rem;
            }
            
            .btn-subject {
                font-size: 1.1rem;
                padding: 15px;
            }
            
            .score {
                font-size: 4rem;
            }
            
            .result-title {
                font-size: 2rem;
            }
            
            .result-icon {
                font-size: 4rem;
            }
            
            .email-option {
                flex-direction: column;
                text-align: center;
            }
            
            .email-icon {
                margin-right: 0;
                margin-bottom: 10px;
            }
            
            .history-table {
                font-size: 0.9rem;
            }
            
            .history-table th, .history-table td {
                padding: 8px 5px;
            }
            
            .gender-icons {
                gap: 15px;
            }
            
            .gender-icons i {
                font-size: 4rem;
                padding: 15px;
            }
        }
    </style>
</head>
<body>
    <!-- Elementos decorativos flotantes corregidos -->
    <div class="decoration decoration-1"><i class="fas fa-star"></i></div>
    <div class="decoration decoration-2"><i class="fas fa-sun"></i></div>
    <div class="decoration decoration-3"><i class="fas fa-cloud"></i></div>
    <div class="decoration decoration-4"><i class="fas fa-moon"></i></div>
    
    <div class="container">
        <div class="header">
            <div class="logo">
                <i class="fas fa-star"></i>
            </div>
            <h1>Evaluación Escolar</h1>
            <p>3er Grado de Primaria - Perú</p>
        </div>
        
        <!-- Pantalla de bienvenida -->
        <div id="welcomeScreen" class="screen active">
            <div class="welcome-screen">
                <div class="welcome-overlay">
                    <div class="gender-icons">
                        <i class="fas fa-female girl-icon"></i>
                        <i class="fas fa-male boy-icon"></i>
                    </div>
                    <h2 style="color: #073B4C; margin-bottom: 20px;">¡Bienvenido al Examen de Evaluación!</h2>
                    <p style="font-size: 1.2rem; line-height: 1.6; max-width: 600px; margin: 0 auto 30px; color: #118AB2;">
                        Demuestra tus conocimientos en Matemática, Comunicación y Ciencia. 
                        Responde correctamente a todas las preguntas para obtener la máxima puntuación.
                    </p>
                    
                    <div class="input-group">
                        <label for="playerName">Ingresa tu nombre completo:</label>
                        <input type="text" id="playerName" placeholder="Escribe tu nombre aquí" autocomplete="off">
                    </div>
                    
                    <button id="startBtn" class="btn btn-start">Comenzar Examen <i class="fas fa-play"></i></button>
                    <button id="historyBtn" class="btn btn-history">Ver Historial <i class="fas fa-history"></i></button>
                </div>
            </div>
        </div>
        
        <!-- Pantalla de selección de materia -->
        <div id="subjectScreen" class="screen">
            <h2 class="subject-title">Elige una Materia</h2>
            
            <button class="btn-subject" data-subject="matematica">
                <i class="fas fa-calculator subject-icon"></i>
                Matemática
            </button>
            
            <button class="btn-subject" data-subject="comunicacion">
                <i class="fas fa-book subject-icon"></i>
                Comunicación
            </button>
            
            <button class="btn-subject" data-subject="ciencia">
                <i class="fas fa-flask subject-icon"></i>
                Ciencia y Tecnología
            </button>
            
            <button id="backToWelcomeBtn" class="btn btn-menu">Volver <i class="fas fa-arrow-left"></i></button>
        </div>
        
        <!-- Pantalla de preguntas -->
        <div id="quizScreen" class="screen">
            <div class="timer" id="timer">45:00</div>
            <div class="question-container">
                <div class="question-number" id="questionNumber">Pregunta 1 de 10</div>
                <div class="question" id="question"></div>
                
                <div class="options-container" id="optionsContainer"></div>
            </div>
            
            <div class="progress-container">
                <div class="progress-bar" id="progressBar"></div>
            </div>
            
            <div style="text-align: center;">
                <button id="nextBtn" class="btn">Siguiente <i class="fas fa-arrow-right"></i></button>
            </div>
        </div>
        
        <!-- Pantalla de resultados -->
        <div id="resultScreen" class="screen">
            <div class="result-screen">
                <div class="result-overlay">
                    <i class="fas fa-star result-icon"></i>
                    <h2 class="result-title">¡Examen Completado!</h2>
                    
                    <div id="playerInfo" style="font-size: 1.3rem; margin: 20px 0; color: #EF476F;"></div>
                    
                    <div class="score" id="finalScore">0/20</div>
                    
                    <div class="result-text" id="resultText"></div>
                    
                    <div class="grade-box">
                        <h3 class="grade-title">Escala de Calificación</h3>
                        <div class="grade-item">
                            <span class="grade-label">Logro destacado (AD):</span>
                            <span>18-20 puntos</span>
                        </div>
                        <div class="grade-item">
                            <span class="grade-label">Logro esperado (A):</span>
                            <span>14-17 puntos</span>
                        </div>
                        <div class="grade-item">
                            <span class="grade-label">En proceso (B):</span>
                            <span>11-13 puntos</span>
                        </div>
                        <div class="grade-item">
                            <span class="grade-label">En inicio (C):</span>
                            <span>0-10 puntos</span>
                        </div>
                    </div>
                    
                    <div id="gradeResult" class="result-text" style="font-weight: bold; font-size: 1.6rem;"></div>
                    
                    <button id="deleteBtn" class="btn btn-delete">Borrar Resultados</button>
                    
                    <div class="email-options">
                        <h3 style="color: #EF476F; margin-bottom: 15px; text-shadow: 1px 1px 1px rgba(0,0,0,0.1);">Enviar resultados a:</h3>
                        <div class="email-option" id="gmailOption">
                            <i class="fab fa-google email-icon gmail"></i>
                            <div class="email-text">Enviar con Gmail</div>
                        </div>
                    </div>
                    
                    <button id="restartBtn" class="btn btn-restart">Repetir Examen</button>
                    <button id="menuBtn" class="btn btn-menu">Menú Principal</button>
                    <button id="viewHistoryBtn" class="btn btn-history">Ver Historial</button>
                </div>
            </div>
        </div>
        
        <!-- Pantalla de confirmación de envío -->
        <div id="emailScreen" class="screen">
            <div class="result-screen">
                <div class="email-confirmation">
                    <i class="fas fa-check-circle"></i>
                    <h2 class="result-title">Resultados Enviados</h2>
                    <p class="result-text">
                        Los resultados han sido enviados correctamente a:
                    </p>
                    <p style="font-size: 1.4rem; font-weight: bold; margin: 15px 0; color: #118AB2;">
                        albertoaltamirano1820@gmail.com
                    </p>
                    <p class="result-text">
                        El profesor recibirá tu evaluación y te dará retroalimentación.
                    </p>
                    
                    <button id="backToResultsBtn" class="btn btn-menu">Volver a Resultados</button>
                </div>
            </div>
        </div>
        
        <!-- Pantalla de historial -->
        <div id="historyScreen" class="screen">
            <div class="history-container">
                <h2 class="history-title"><i class="fas fa-history"></i> Historial de Evaluaciones</h2>
                
                <div id="historyContent">
                    <!-- El contenido del historial se generará dinámicamente -->
                </div>
                
                <div style="text-align: center; margin-top: 20px;">
                    <button id="backToMenuFromHistory" class="btn btn-menu">Volver al Menú</button>
                    <button id="clearHistoryBtn" class="btn btn-delete">Borrar Historial</button>
                </div>
            </div>
        </div>
        
        <!-- Popup de PIN para borrar resultados -->
        <div class="pin-popup" id="pinPopup">
            <div class="pin-content">
                <h3 class="pin-title">Ingresa el PIN para borrar</h3>
                <input type="password" class="pin-input" id="pinInput" maxlength="7" placeholder="0000000">
                <div>
                    <button class="btn btn-delete pin-btn" id="confirmPinBtn">Confirmar</button>
                    <button class="btn btn-menu pin-btn" id="cancelPinBtn">Cancelar</button>
                </div>
            </div>
        </div>
        
        <div class="footer" style="text-align: center; padding: 15px; background: #073B4C; color: white; font-size: 0.9rem;">
            <p>Desarrollado según el Currículo Nacional de Educación Básica - MINEDU Perú</p>
        </div>
    </div>

    <script>
        // Variables globales
        let playerName = "";
        let currentSubject = "";
        let currentQuestionIndex = 0;
        let score = 0;
        let timer;
        let timeLeft = 45 * 60; // 45 minutos en segundos
        let questions = [];
        let userAnswers = [];
        let grade = "";
        const DELETE_PIN = "5602265"; // PIN para borrar resultados
        
        // Datos de las preguntas
        const questionData = {
            matematica: [
                {
                    pregunta: "¿Cuál es el resultado de 234 + 156?",
                    opciones: ["380", "390", "400", "370"],
                    respuesta: 1
                },
                {
                    pregunta: "María tiene 3 cajas con 8 chocolates cada una. ¿Cuántos chocolates tiene en total?",
                    opciones: ["24", "21", "18", "27"],
                    respuesta: 0
                },
                {
                    pregunta: "¿Cuántos centímetros hay en 2 metros?",
                    opciones: ["20 cm", "200 cm", "2000 cm", "100 cm"],
                    respuesta: 1
                },
                {
                    pregunta: "En una tienda hay 125 manzanas. Si se venden 48 manzanas, ¿cuántas quedan?",
                    opciones: ["77", "87", "73", "83"],
                    respuesta: 0
                },
                {
                    pregunta: "¿Cuál es la fracción que representa la mitad de una pizza?",
                    opciones: ["1/3", "1/4", "1/2", "2/3"],
                    respuesta: 2
                },
                {
                    pregunta: "Si un libro cuesta 15 soles y compro 3 libros, ¿cuánto pago en total?",
                    opciones: ["35 soles", "45 soles", "40 soles", "50 soles"],
                    respuesta: 1
                },
                {
                    pregunta: "¿Cuántos lados tiene un triángulo?",
                    opciones: ["4", "5", "3", "6"],
                    respuesta: 2
                },
                {
                    pregunta: "¿Cuál es el número que falta en la secuencia: 15, 20, 25, __, 35?",
                    opciones: ["28", "30", "32", "29"],
                    respuesta: 1
                },
                {
                    pregunta: "Ana tiene 8 stickers y le da 3 a su hermana. ¿Cuántos stickers le quedan?",
                    opciones: ["5", "6", "4", "7"],
                    respuesta: 0
                },
                {
                    pregunta: "¿Cuál es el perímetro de un cuadrado que mide 4 cm por cada lado?",
                    opciones: ["8 cm", "12 cm", "16 cm", "20 cm"],
                    respuesta: 2
                }
            ],
            comunicacion: [
                {
                    pregunta: "¿Cuál es el sujeto en la oración: \"Los niños juegan en el parque\"?",
                    opciones: ["juegan", "Los niños", "en el parque", "parque"],
                    respuesta: 1
                },
                {
                    pregunta: "¿Cuál de estas palabras es un sustantivo?",
                    opciones: ["correr", "rápido", "casa", "muy"],
                    respuesta: 2
                },
                {
                    pregunta: "¿Cuál es el plural de \"pez\"?",
                    opciones: ["pezes", "peces", "pezs", "pescados"],
                    respuesta: 1
                },
                {
                    pregunta: "¿Qué signo de puntuación se usa al final de una pregunta?",
                    opciones: ["Punto (.)", "Coma (,)", "Signos de interrogación (¿?)", "Punto y coma (;)"],
                    respuesta: 2
                },
                {
                    pregunta: "¿Cuál es el antónimo de \"grande\"?",
                    opciones: ["alto", "pequeño", "gordo", "ancho"],
                    respuesta: 1
                },
                {
                    pregunta: "En el cuento \"Los tres cochinitos\", ¿cuál es el personaje principal?",
                    opciones: ["El lobo", "La mamá cerdita", "Los tres cochinitos", "El cazador"],
                    respuesta: 2
                },
                {
                    pregunta: "¿Cuál de estas palabras tiene acento en la última sílaba?",
                    opciones: ["árbol", "ratón", "música", "rápido"],
                    respuesta: 1
                },
                {
                    pregunta: "¿Qué tipo de texto es una receta de cocina?",
                    opciones: ["Narrativo", "Descriptivo", "Instructivo", "Poético"],
                    respuesta: 2
                },
                {
                    pregunta: "¿Cuál es el diminutivo de \"perro\"?",
                    opciones: ["perrazo", "perrito", "perruno", "perrera"],
                    respuesta: 1
                },
                {
                    pregunta: "¿Cuál de estas oraciones está escrita correctamente?",
                    opciones: [
                        "Los niños esta jugando",
                        "Los niños están jugando",
                        "Los niños estan jugando",
                        "Los niño están jugando"
                    ],
                    respuesta: 1
                }
            ],
            ciencia: [
                {
                    pregunta: "¿Cuáles son los tres estados de la materia?",
                    opciones: [
                        "Sólido, líquido y vapor",
                        "Sólido, líquido y gaseoso",
                        "Duro, blando y líquido",
                        "Frío, tibio y caliente"
                    ],
                    respuesta: 1
                },
                {
                    pregunta: "¿Qué necesita una planta para crecer?",
                    opciones: [
                        "Solo agua",
                        "Solo luz solar",
                        "Agua, luz solar y aire",
                        "Solo tierra"
                    ],
                    respuesta: 2
                },
                {
                    pregunta: "¿Cuál es la función principal del corazón?",
                    opciones: [
                        "Ayudar a respirar",
                        "Bombear sangre por todo el cuerpo",
                        "Digestión de los alimentos",
                        "Pensar"
                    ],
                    respuesta: 1
                },
                {
                    pregunta: "¿Cuál de estos animales es carnívoro?",
                    opciones: ["Vaca", "Caballo", "León", "Conejo"],
                    respuesta: 2
                },
                {
                    pregunta: "¿Qué pasa cuando ponemos agua en el congelador?",
                    opciones: [
                        "Se evapora",
                        "Se congela y se vuelve hielo",
                        "Se calienta",
                        "Cambia de color"
                    ],
                    respuesta: 1
                },
                {
                    pregunta: "¿Cuál es el planeta más cercano al Sol?",
                    opciones: ["Tierra", "Marte", "Venus", "Mercurio"],
                    respuesta: 3
                },
                {
                    pregunta: "¿Qué órgano del cuerpo humano nos permite ver?",
                    opciones: ["Nariz", "Ojos", "Oídos", "Boca"],
                    respuesta: 1
                },
                {
                    pregunta: "¿Cuál de estos materiales conduce la electricidad?",
                    opciones: ["Madera", "Plástico", "Cobre", "Vidrio"],
                    respuesta: 2
                },
                {
                    pregunta: "¿Qué es la fotosíntesis?",
                    opciones: [
                        "Cuando las plantas duermen",
                        "Cuando las plantas producen su alimento usando luz solar",
                        "Cuando las plantas se mueven",
                        "Cuando las plantas crecen"
                    ],
                    respuesta: 1
                },
                {
                    pregunta: "¿Cuál es la fuente de energía más importante para la Tierra?",
                    opciones: ["La Luna", "El Sol", "Las estrellas", "El viento"],
                    respuesta: 1
                }
            ]
        };
        
        // Elementos DOM
        const welcomeScreen = document.getElementById('welcomeScreen');
        const subjectScreen = document.getElementById('subjectScreen');
        const quizScreen = document.getElementById('quizScreen');
        const resultScreen = document.getElementById('resultScreen');
        const emailScreen = document.getElementById('emailScreen');
        const historyScreen = document.getElementById('historyScreen');
        const pinPopup = document.getElementById('pinPopup');
        const playerNameInput = document.getElementById('playerName');
        const startBtn = document.getElementById('startBtn');
        const historyBtn = document.getElementById('historyBtn');
        const viewHistoryBtn = document.getElementById('viewHistoryBtn');
        const backToWelcomeBtn = document.getElementById('backToWelcomeBtn');
        const backToMenuFromHistory = document.getElementById('backToMenuFromHistory');
        const subjectBtns = document.querySelectorAll('.btn-subject');
        const questionElement = document.getElementById('question');
        const optionsContainer = document.getElementById('optionsContainer');
        const nextBtn = document.getElementById('nextBtn');
        const questionNumberElement = document.getElementById('questionNumber');
        const progressBar = document.getElementById('progressBar');
        const finalScoreElement = document.getElementById('finalScore');
        const resultTextElement = document.getElementById('resultText');
        const gradeResultElement = document.getElementById('gradeResult');
        const restartBtn = document.getElementById('restartBtn');
        const menuBtn = document.getElementById('menuBtn');
        const deleteBtn = document.getElementById('deleteBtn');
        const clearHistoryBtn = document.getElementById('clearHistoryBtn');
        const gmailOption = document.getElementById('gmailOption');
        const backToResultsBtn = document.getElementById('backToResultsBtn');
        const timerElement = document.getElementById('timer');
        const playerInfoElement = document.getElementById('playerInfo');
        const pinInput = document.getElementById('pinInput');
        const confirmPinBtn = document.getElementById('confirmPinBtn');
        const cancelPinBtn = document.getElementById('cancelPinBtn');
        const historyContent = document.getElementById('historyContent');
        
        // Event Listeners
        startBtn.addEventListener('click', startGame);
        historyBtn.addEventListener('click', showHistory);
        viewHistoryBtn.addEventListener('click', showHistory);
        backToWelcomeBtn.addEventListener('click', () => {
            subjectScreen.classList.remove('active');
            welcomeScreen.classList.add('active');
        });
        backToMenuFromHistory.addEventListener('click', () => {
            historyScreen.classList.remove('active');
            welcomeScreen.classList.add('active');
        });
        subjectBtns.forEach(btn => {
            btn.addEventListener('click', selectSubject);
        });
        nextBtn.addEventListener('click', nextQuestion);
        restartBtn.addEventListener('click', restartGame);
        menuBtn.addEventListener('click', goToMenu);
        deleteBtn.addEventListener('click', showPinPopup);
        clearHistoryBtn.addEventListener('click', showPinPopupForHistory);
        gmailOption.addEventListener('click', () => sendResultsByEmail('gmail'));
        backToResultsBtn.addEventListener('click', () => {
            emailScreen.classList.remove('active');
            resultScreen.classList.add('active');
        });
        confirmPinBtn.addEventListener('click', processPin);
        cancelPinBtn.addEventListener('click', () => {
            pinPopup.style.display = 'none';
            pinInput.value = '';
        });
        
        // Variable para controlar la acción del PIN
        let currentPinAction = "";
        
        // Función para iniciar el juego
        function startGame() {
            playerName = playerNameInput.value.trim();
            
            if (playerName === "") {
                alert("Por favor, ingresa tu nombre para comenzar.");
                return;
            }
            
            // Cambiar a la pantalla de selección de materia
            welcomeScreen.classList.remove('active');
            subjectScreen.classList.add('active');
        }
        
        // Función para mostrar historial
        function showHistory() {
            loadHistory();
            welcomeScreen.classList.remove('active');
            resultScreen.classList.remove('active');
            historyScreen.classList.add('active');
        }
        
        // Función para cargar historial
        function loadHistory() {
            const history = JSON.parse(localStorage.getItem('examHistory')) || [];
            
            if (history.length === 0) {
                historyContent.innerHTML = `
                    <div class="no-history">
                        <i class="fas fa-history" style="font-size: 4rem; margin-bottom: 20px; color: #06D6A0;"></i>
                        <p>No hay evaluaciones registradas en el historial.</p>
                        <p>¡Completa un examen para ver tus resultados aquí!</p>
                    </div>
                `;
                return;
            }
            
            let html = `
                <table class="history-table">
                    <thead>
                        <tr>
                            <th>Fecha</th>
                            <th>Nombre</th>
                            <th>Materia</th>
                            <th>Puntaje</th>
                            <th>Calificación</th>
                        </tr>
                    </thead>
                    <tbody>
            `;
            
            history.forEach(result => {
                const date = new Date(result.date);
                const formattedDate = `${date.getDate()}/${date.getMonth() + 1}/${date.getFullYear()}`;
                const formattedTime = `${date.getHours().toString().padStart(2, '0')}:${date.getMinutes().toString().padStart(2, '0')}`;
                
                html += `
                    <tr>
                        <td>${formattedDate}<br>${formattedTime}</td>
                        <td>${result.name}</td>
                        <td>${getSubjectName(result.subject)}</td>
                        <td>${result.score}/20</td>
                        <td style="color: ${result.grade.color}; font-weight: bold;">${result.grade.grade}</td>
                    </tr>
                `;
            });
            
            html += `
                    </tbody>
                </table>
            `;
            
            historyContent.innerHTML = html;
        }
        
        // Función para mostrar popup de PIN para borrar historial
        function showPinPopupForHistory() {
            currentPinAction = "deleteHistory";
            pinPopup.style.display = 'flex';
            pinInput.focus();
        }
        
        // Función para seleccionar materia
        function selectSubject(e) {
            currentSubject = e.currentTarget.dataset.subject;
            questions = questionData[currentSubject];
            currentQuestionIndex = 0;
            score = 0;
            userAnswers = [];
            
            // Aplicar tema según la materia seleccionada
            quizScreen.classList.remove('math-theme', 'com-theme', 'sci-theme');
            switch(currentSubject) {
                case "matematica":
                    quizScreen.classList.add('math-theme');
                    break;
                case "comunicacion":
                    quizScreen.classList.add('com-theme');
                    break;
                case "ciencia":
                    quizScreen.classList.add('sci-theme');
                    break;
            }
            
            // Iniciar temporizador
            timeLeft = 45 * 60;
            startTimer();
            
            // Cargar primera pregunta
            loadQuestion();
            
            // Cambiar a la pantalla de preguntas
            subjectScreen.classList.remove('active');
            quizScreen.classList.add('active');
        }
        
        // Función para cargar pregunta
        function loadQuestion() {
            resetOptions();
            const currentQuestion = questions[currentQuestionIndex];
            
            // Actualizar número de pregunta
            questionNumberElement.textContent = `Pregunta ${currentQuestionIndex + 1} de ${questions.length}`;
            
            // Actualizar barra de progreso
            const progressPercentage = ((currentQuestionIndex) / questions.length) * 100;
            progressBar.style.width = `${progressPercentage}%`;
            
            // Mostrar pregunta
            questionElement.textContent = currentQuestion.pregunta;
            
            // Mostrar opciones
            currentQuestion.opciones.forEach((opcion, index) => {
                const optionElement = document.createElement('div');
                optionElement.classList.add('option');
                optionElement.textContent = opcion;
                optionElement.dataset.index = index;
                optionElement.addEventListener('click', selectOption);
                optionsContainer.appendChild(optionElement);
            });
            
            // Actualizar botón siguiente
            if (currentQuestionIndex === questions.length - 1) {
                nextBtn.textContent = "Finalizar Examen";
            } else {
                nextBtn.textContent = "Siguiente";
            }
        }
        
        // Función para seleccionar opción
        function selectOption(e) {
            const selectedOption = e.currentTarget;
            const options = document.querySelectorAll('.option');
            
            // Remover selección previa
            options.forEach(option => {
                option.classList.remove('selected');
            });
            
            // Seleccionar la opción actual
            selectedOption.classList.add('selected');
            
            // Guardar respuesta del usuario
            userAnswers[currentQuestionIndex] = parseInt(selectedOption.dataset.index);
        }
        
        // Función para resetear opciones
        function resetOptions() {
            optionsContainer.innerHTML = '';
        }
        
        // Función para pasar a la siguiente pregunta
        function nextQuestion() {
            // Verificar si se ha seleccionado una respuesta
            if (userAnswers[currentQuestionIndex] === undefined) {
                alert("Por favor, selecciona una respuesta antes de continuar.");
                return;
            }
            
            // Verificar respuesta (cada respuesta correcta suma 2 puntos)
            const currentQuestion = questions[currentQuestionIndex];
            if (userAnswers[currentQuestionIndex] === currentQuestion.respuesta) {
                score += 2;
            }
            
            // Pasar a la siguiente pregunta
            currentQuestionIndex++;
            
            if (currentQuestionIndex < questions.length) {
                loadQuestion();
            } else {
                showResults();
            }
        }
        
        // Función para mostrar resultados
        function showResults() {
            // Detener temporizador
            clearInterval(timer);
            
            // Determinar calificación
            grade = determineGrade(score);
            
            // Guardar resultado en historial
            saveToHistory();
            
            // Cambiar a pantalla de resultados
            quizScreen.classList.remove('active');
            resultScreen.classList.add('active');
            
            // Mostrar información del jugador
            playerInfoElement.textContent = `${playerName} - ${getSubjectName(currentSubject)}`;
            
            // Mostrar puntaje (de 0 a 20)
            finalScoreElement.textContent = `${score}/20`;
            
            // Mostrar mensaje según puntaje
            let message = "";
            if (score === 20) {
                message = "¡Excelente trabajo! Has logrado la máxima puntuación. ¡Felicidades!";
            } else if (score >= 14) {
                message = "¡Muy buen trabajo! Has demostrado un gran conocimiento en esta materia.";
            } else if (score >= 11) {
                message = "Buen intento. Sigue estudiando para mejorar tus resultados.";
            } else {
                message = "Necesitas repasar más esta materia. ¡No te rindas!";
            }
            
            resultTextElement.textContent = message;
            
            // Mostrar calificación
            gradeResultElement.textContent = `Calificación: ${grade.grade} - ${grade.message}`;
            gradeResultElement.style.color = grade.color;
        }
        
        // Función para guardar resultados en historial
        function saveToHistory() {
            const result = {
                name: playerName,
                subject: currentSubject,
                score: score,
                total: 20,
                date: new Date().toISOString(),
                grade: grade
            };
            
            // Obtener historial actual o inicializar
            let history = JSON.parse(localStorage.getItem('examHistory')) || [];
            
            // Agregar nuevo resultado al inicio
            history.unshift(result);
            
            // Guardar en localStorage (mantener solo los últimos 10 resultados)
            localStorage.setItem('examHistory', JSON.stringify(history.slice(0, 10)));
        }
        
        // Función para determinar la calificación (puntaje de 0 a 20)
        function determineGrade(score) {
            if (score >= 18) return { 
                grade: 'AD', 
                message: 'Logro destacado',
                color: '#06D6A0'
            };
            if (score >= 14) return { 
                grade: 'A', 
                message: 'Logro esperado',
                color: '#118AB2'
            };
            if (score >= 11) return { 
                grade: 'B', 
                message: 'En proceso',
                color: '#FF9E7D'
            };
            return { 
                grade: 'C', 
                message: 'En inicio',
                color: '#EF476F'
            };
        }
        
        // Función para reiniciar el juego
        function restartGame() {
            currentQuestionIndex = 0;
            score = 0;
            userAnswers = [];
            
            // Reiniciar temporizador
            timeLeft = 45 * 60;
            startTimer();
            
            // Cargar primera pregunta
            loadQuestion();
            
            // Volver a la pantalla de preguntas
            resultScreen.classList.remove('active');
            quizScreen.classList.add('active');
        }
        
        // Función para volver al menú principal
        function goToMenu() {
            // Detener temporizador si está activo
            clearInterval(timer);
            
            // Volver al menú principal
            resultScreen.classList.remove('active');
            welcomeScreen.classList.add('active');
        }
        
        // Función para mostrar popup de PIN
        function showPinPopup() {
            currentPinAction = "deleteCurrent";
            pinPopup.style.display = 'flex';
            pinInput.focus();
        }
        
        // Función para procesar el PIN
        function processPin() {
            const enteredPin = pinInput.value;
            
            if (enteredPin === DELETE_PIN) {
                if (currentPinAction === "deleteCurrent") {
                    // Resetear todo y volver a selección de materia
                    currentQuestionIndex = 0;
                    score = 0;
                    userAnswers = [];
                    clearInterval(timer);
                    
                    pinPopup.style.display = 'none';
                    pinInput.value = '';
                    
                    resultScreen.classList.remove('active');
                    subjectScreen.classList.add('active');
                } else if (currentPinAction === "deleteHistory") {
                    // Borrar historial
                    localStorage.removeItem('examHistory');
                    loadHistory();
                    pinPopup.style.display = 'none';
                    pinInput.value = '';
                }
            } else {
                alert("PIN incorrecto. No se puede realizar la acción.");
                pinInput.value = '';
                pinInput.focus();
            }
        }
        
        // Función para enviar resultados por correo
        function sendResultsByEmail(provider) {
            // Construir asunto y cuerpo del mensaje
            const subject = `Resultados de Evaluación - ${playerName}`;
            const body = `Estimado profesor,\n\n` +
                         `Adjunto los resultados de la evaluación realizada por el estudiante:\n\n` +
                         `Nombre: ${playerName}\n` +
                         `Materia: ${getSubjectName(currentSubject)}\n` +
                         `Puntuación: ${score}/20\n` +
                         `Calificación: ${grade.grade} - ${grade.message}\n\n` +
                         `Fecha: ${new Date().toLocaleString()}\n\n` +
                         `Escala de Calificación:\n` +
                         `- Logro destacado (AD): 18-20 puntos\n` +
                         `- Logro esperado (A): 14-17 puntos\n` +
                         `- En proceso (B): 11-13 puntos\n` +
                         `- En inicio (C): 0-10 puntos\n\n` +
                         `Atentamente,\nSistema de Evaluación Escolar`;
            
            // Construir enlace mailto
            const mailtoLink = `mailto:albertoaltamirano1820@gmail.com?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;
            
            // Construir enlace específico para el proveedor
            let providerLink = mailtoLink;
            
            if (provider === 'gmail') {
                providerLink = `https://mail.google.com/mail/?view=cm&fs=1&to=albertoaltamirano1820@gmail.com&su=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;
            }
            
            // Abrir enlace en una nueva pestaña
            window.open(providerLink, '_blank');
            
            // Mostrar pantalla de confirmación
            resultScreen.classList.remove('active');
            emailScreen.classList.add('active');
        }
        
        // Función para obtener nombre de materia
        function getSubjectName(subject) {
            switch(subject) {
                case "matematica":
                    return "Matemática";
                case "comunicacion":
                    return "Comunicación";
                case "ciencia":
                    return "Ciencia y Tecnología";
                default:
                    return subject;
            }
        }
        
        // Función para iniciar temporizador
        function startTimer() {
            clearInterval(timer);
            updateTimer();
            
            timer = setInterval(() => {
                timeLeft--;
                updateTimer();
                
                if (timeLeft <= 0) {
                    clearInterval(timer);
                    showResults();
                }
            }, 1000);
        }
        
        // Función para actualizar temporizador
        function updateTimer() {
            const minutes = Math.floor(timeLeft / 60);
            const seconds = timeLeft % 60;
            timerElement.textContent = `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
        }
        
        // Inicializar la aplicación
        document.addEventListener('DOMContentLoaded', () => {
            // Cargar historial si existe
            if (!localStorage.getItem('examHistory')) {
                // Inicializar historial vacío
                localStorage.setItem('examHistory', JSON.stringify([]));
            }
        });
    </script>
</body>
</html>
