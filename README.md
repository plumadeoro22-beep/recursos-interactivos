[Rubrica1z.html](https://github.com/user-attachments/files/22192274/Rubrica1z.html)
<!DOCTYPE html>
```html
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Despierta el Interés y Autonomía en el Aula</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            text-align: center;
            margin-bottom: 30px;
        }

        h1 {
            color: #4a6da7;
            font-size: 2rem;
            margin-bottom: 10px;
        }

        .card {
            background-color: white;
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            margin-bottom: 30px;
        }

        .btn {
            display: inline-block;
            background-color: #4a6da7;
            color: white;
            padding: 12px 24px;
            border-radius: 8px;
            text-decoration: none;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            border: none;
            margin: 10px 5px;
        }

        .btn:hover {
            background-color: #3a5d97;
            transform: translateY(-2px);
        }

        .input-field {
            width: 100%;
            padding: 12px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
            margin-bottom: 20px;
        }

        .question-card {
            background-color: #f9f9ff;
            border-left: 4px solid #4a6da7;
            padding: 25px;
            margin-bottom: 25px;
            border-radius: 0 8px 8px 0;
        }

        .scenario {
            background-color: #e8f0fe;
            border-left: 4px solid #2196f3;
            padding: 15px;
            margin-bottom: 20px;
            border-radius: 0 8px 8px 0;
            font-style: italic;
        }

        .options {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
            margin-top: 15px;
        }

        .option {
            padding: 15px;
            background-color: white;
            border: 2px solid #eee;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
        }

        .option:hover {
            border-color: #4a6da7;
            background-color: #f0f4ff;
        }

        .option i {
            margin-right: 10px;
            color: #4a6da7;
        }

        .feedback {
            padding: 20px;
            border-radius: 8px;
            margin-top: 20px;
            font-weight: 500;
        }

        .correct {
            background-color: #d4edda;
            color: #155724;
            border: 1px solid #c3e6cb;
        }

        .incorrect {
            background-color: #f8d7da;
            color: #721c24;
            border: 1px solid #f5c6cb;
        }

        .progress-bar {
            height: 10px;
            background-color: #eee;
            border-radius: 5px;
            overflow: hidden;
            margin-bottom: 20px;
        }

        .progress-fill {
            height: 100%;
            background-color: #4a6da7;
            width: 0%;
            transition: width 0.5s ease;
        }

        .score-display {
            text-align: center;
            font-size: 1.2rem;
            font-weight: bold;
            color: #4a6da7;
            margin-bottom: 20px;
        }

        .hidden {
            display: none;
        }

        .text-content {
            line-height: 1.8;
            font-size: 1.05rem;
        }

        .competency-badge {
            display: inline-block;
            background-color: #e3f2fd;
            color: #1565c0;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 0.85rem;
            margin-right: 8px;
            margin-bottom: 8px;
        }

        @media (max-width: 768px) {
            .options {
                grid-template-columns: 1fr;
            }
            
            .btn {
                padding: 10px 16px;
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Pantalla de Inicio -->
        <div id="start-screen" class="card">
            <h1>🎯 Evaluación Docente: Rúbrica 1</h1>
            <p class="text-center mb-4">Dominio del Profesorado en Promoción del Interés y Autonomía</p>
            <div class="scenario">
                <i class="fas fa-quote-left mr-2"></i>
                "Esta herramienta evalúa tu capacidad para aplicar la Rúbrica 1 en contextos reales del aula, analizando situaciones complejas y tomando decisiones pedagógicas informadas."
            </div>
            <label for="teacher-name" class="block mb-2">Nombre del Docente:</label>
            <input type="text" id="teacher-name" class="input-field" placeholder="Ingresa tu nombre completo">
            <button class="btn" onclick="startGame()">Iniciar Evaluación</button>
        </div>

        <!-- Pantalla de Bienvenida -->
        <div id="welcome-screen" class="card hidden">
            <h1>🚀 Bienvenido al Desafío Pedagógico</h1>
            <div class="scenario">
                <i class="fas fa-lightbulb mr-2"></i>
                "Analiza situaciones reales del aula y toma decisiones pedagógicas fundamentadas en la Rúbrica 1. Este ejercicio desarrollará tu competencia para involucrar activamente a los estudiantes."
            </div>
            <p class="mb-4"><span class="font-bold">Competencias a Evaluar:</span></p>
            <div>
                <span class="competency-badge">Promover Interés</span>
                <span class="competency-badge">Fomentar Autonomía</span>
                <span class="competency-badge">Promover Reflexión</span>
                <span class="competency-badge">Gestión de Clase</span>
            </div>
            <button class="btn mt-6" onclick="showReading()">Continuar al Material</button>
        </div>

        <!-- Selección de Lectura -->
        <div id="reading-screen" class="card hidden">
            <h2>📚 Fundamentos de la Rúbrica 1</h2>
            <div class="scenario">
                <i class="fas fa-book-open mr-2"></i>
                "Revise el texto base que sustenta la evaluación. Luego, pondrá a prueba su comprensión aplicándola a situaciones reales del aula."
            </div>
            <button class="btn mt-4" onclick="showText()">Leer Texto Completo</button>
        </div>

        <!-- Texto Completo -->
        <div id="full-text-screen" class="card hidden">
            <h2>Despertar el Interés, Autonomía y Reflexión en el Aula</h2>
            <div class="text-content" id="full-text">
                <strong>R1-Involucra activamente a los estudiantes en el proceso de aprendizaje</strong><br><br>
                
                Imaginemos un aula donde los estudiantes no solo escuchan, sino que brillan con curiosidad, donde las preguntas fluyen como un río y cada idea es una semilla que germina. ¿Cómo llegar a este escenario? La respuesta está en tres pilares fundamentales de la 1° rúbrica: despertar el interés, fomentar la autonomía, y promover la reflexión. Estos no son simples caprichos pedagógicos, sino principios respaldados por la ciencia y la experiencia.<br><br>
                
                Despertar el interés no es un lujo, sino una necesidad biológica y cognitiva. Estudios demuestran que cuando algo captura nuestra atención, el cerebro libera dopamina, un neurotransmisor vinculado al placer y la motivación, que nos impulsa a explorar y aprender. Además, la amígdala —centro emocional del cerebro— trabaja en conjunto con el hipocampo para consolidar recuerdos, haciendo que lo aprendido con interés perdure. Como decía John Locke, el verdadero rol del docente no es saturar de información, sino encender en los estudiantes el amor por el conocimiento. Sin embargo, muchos educadores caen en la trampa de cumplir con un plan de clases rígido, olvidando que sin interés genuino, el aprendizaje se convierte en un mero trámite mecánico.<br><br>
                
                Opinar y decidir con autonomía es el segundo pilar clave. Permitir que los estudiantes opinen, decidan y exploren no es un acto de rebeldía pedagógica, sino una estrategia respaldada por Ausubel y Piaget. Cuando los alumnos tienen libertad para pensar y proponer, construyen conocimiento de manera significativa, vinculando lo nuevo con lo conocido. La autonomía fomenta la creatividad y la perseverancia, esenciales para enfrentar retos. No obstante, algunos docentes se resisten, argumentando que perderán el control del tiempo o que las sesiones deben seguir un guion inflexible. ¿Cómo esperar que los estudiantes se involucren si incluso las conclusiones ya están predeterminadas?<br><br>
                
                Finalmente, la reflexión sobre lo aprendido transforma la información en comprensión profunda al encontrarle utilidad y sentido. Esto supone no solo que tengan claro qué es lo que van a aprender y cómo, sino que tengan oportunidad de conversarlo. Rebeca Anijovich y Perrenoud destacan que cuando los estudiantes conocen los objetivos y criterios de evaluación, pueden autorregular su proceso, identificar fortalezas y debilidades, y enfocar sus esfuerzos. Sin embargo, en un sistema obsesionado por enseñar con sesiones de 45 o 90 minutos, muchos docentes sienten que no hay espacio para estas conversaciones, reduciendo el aprendizaje a una lista de tareas mecánicas.<br><br>
                
                En conclusión, enseñar no es transmitir, sino inspirar. Despertar el interés, dar autonomía y promover la reflexión para comprender el sentido no son opciones, sino condiciones para un aprendizaje verdadero. Como educadores, debemos preguntarnos: ¿queremos estudiantes pasivos o mentes curiosas y críticas? El cambio comienza en nuestras aulas. ¡Abramos espacio para el asombro, la voz y la reflexión de nuestros alumnos!<br><br>
                
                Ver video: <a href="#" style="color:#4a6da7;">https://vt.tiktok.com/ZSAWsSwKX/</a><br>
                Dr. Jorge Espinoza Fernández
            </div>
            <button class="btn mt-4" onclick="startQuiz()">Comenzar Evaluación Práctica</button>
        </div>

        <!-- Evaluación -->
        <div id="quiz-screen" class="card hidden">
            <h2>🔍 Evaluación Práctica: Aplicación de la Rúbrica 1</h2>
            <div class="progress-bar">
                <div class="progress-fill" id="progress-fill"></div>
            </div>
            <div class="score-display" id="score-display">Preguntas analizadas: 0/10</div>
            
            <div id="question-container"></div>
            
            <div id="feedback-container" class="hidden"></div>
            
            <div id="navigation-buttons">
                <button class="btn hidden" id="prev-btn" onclick="previousQuestion()">
                    <i class="fas fa-arrow-left mr-2"></i>Anterior
                </button>
                <button class="btn hidden" id="next-btn" onclick="nextQuestion()">
                    Siguiente<i class="fas fa-arrow-right ml-2"></i>
                </button>
                <button class="btn hidden" id="submit-btn" onclick="submitQuiz()">
                    <i class="fas fa-check-circle mr-2"></i>Enviar Respuestas
                </button>
            </div>
        </div>

        <!-- Resultados -->
        <div id="results-screen" class="card hidden">
            <h2>🏆 Resultados de la Evaluación</h2>
            <div class="score-display" id="final-score"></div>
            <div id="result-feedback"></div>
            <button class="btn mt-4" onclick="restartGame()">
                <i class="fas fa-redo mr-2"></i>Jugar Nuevamente
            </button>
        </div>
    </div>

    <script>
        // Variables globales
        let currentTeacherName = '';
        let currentQuestionIndex = 0;
        let score = 0;
        let answeredQuestions = [];
        
        // Preguntas del cuestionario con alto nivel cognitivo
        const questions = [
            {
                question: "En una clase de matemáticas, observas que varios estudiantes parecen desmotivados y distraídos. Según la Rúbrica 1, ¿cuál sería la acción más efectiva para recuperar su interés?",
                scenario: "Contexto: Clase de matemáticas de 7mo grado. Los estudiantes parecen aburridos y no prestan atención a la explicación sobre ecuaciones lineales.",
                options: [
                    "Aumentar el volumen de la voz y repetir la explicación",
                    "Introducir un problema contextual relacionado con sus intereses (ej: deportes, videojuegos)",
                    "Asignar ejercicios adicionales de refuerzo",
                    "Llamar la atención individualmente a los estudiantes distraídos"
                ],
                correctAnswer: 1,
                feedback: {
                    correct: "¡Excelente! Has identificado que conectar el contenido con intereses personales (como deportes o videojuegos) libera dopamina y aumenta la motivación intrínseca, cumpliendo con el primer pilar de la rúbrica.",
                    incorrect: "Aunque algunas acciones podrían tener efecto temporal, no abordan la raíz del problema. La clave está en vincular el contenido con intereses reales de los estudiantes para generar motivación genuina."
                }
            },
            {
                question: "Durante una discusión grupal sobre un proyecto de ciencias, un grupo de estudiantes mantiene posiciones contrarias y no logran consenso. Según la Rúbrica 1, ¿cómo deberías intervenir?",
                scenario: "Contexto: Grupo de 4to medio trabajando en un proyecto sobre energías renovables. Dos estudiantes defienden la energía solar mientras otros prefieren la eólica. La discusión se ha estancado.",
                options: [
                    "Decidir yo mismo cuál opción es mejor y comunicárselo al grupo",
                    "Facilitar un diálogo estructurado donde cada grupo presente evidencias y argumentos",
                    "Dividir el grupo en subgrupos para trabajar por separado",
                    "Limitar el tiempo de discusión para evitar conflictos"
                ],
                correctAnswer: 1,
                feedback: {
                    correct: "Perfecto! Has aplicado correctamente el tercer pilar: promover la reflexión. Facilitar diálogos estructurados permite a los estudiantes conocer perspectivas diferentes, autorregular su proceso y tomar decisiones informadas.",
                    incorrect: "Estas acciones limitan la autonomía y la reflexión. Decidir por ellos o dividirlos evita que desarrollen habilidades de negociación y pensamiento crítico."
                }
            },
            {
                question: "En una clase de literatura, notas que un estudiante siempre responde brevemente y parece poco comprometido. Según la Rúbrica 1, ¿qué estrategia sería más adecuada?",
                scenario: "Contexto: Estudiante de 2do medio en clase de literatura. Responde con monosílabos y parece desinteresado en los análisis de personajes.",
                options: [
                    "Pedirle que responda con más detalle y recordarle las expectativas de participación",
                    "Invitarlo a compartir sus opiniones en privado después de clase",
                    "Adaptar las actividades para incluir expresiones artísticas alternativas (dibujos, collages)",
                    "Ignorar su falta de participación para no presionarlo"
                ],
                correctAnswer: 2,
                feedback: {
                    correct: "¡Muy bien! Has reconocido que ofrecer múltiples vías de expresión (artística, verbal, escrita) permite a los estudiantes demostrar comprensión de maneras diversas, fomentando así su autonomía y compromiso.",
                    incorrect: "Las otras opciones pueden generar resistencia o vergüenza. Adaptar las actividades respeta diferentes estilos de aprendizaje y promueve una participación más genuina."
                }
            },
            {
                question: "Antes de iniciar una nueva unidad sobre geografía mundial, ¿cuál sería la mejor forma de preparar a los estudiantes según la Rúbrica 1?",
                scenario: "Contexto: Unidad sobre continentes y países. Los estudiantes tienen dificultades para recordar nombres y ubicaciones.",
                options: [
                    "Presentar un mapa y pedir que memoricen los nombres de los países",
                    "Explicar claramente los objetivos de aprendizaje y cómo evaluarán su comprensión",
                    "Dar una lista de países para investigar individualmente",
                    "Organizar un concurso de memoria rápida sobre nombres de países"
                ],
                correctAnswer: 1,
                feedback: {
                    correct: "Correcto! Has aplicado el tercer pilar: promover la reflexión. Al explicar objetivos y criterios de evaluación, los estudiantes pueden autorregular su proceso, identificar lo que necesitan aprender y enfocar sus esfuerzos de manera eficiente.",
                    incorrect: "Estas estrategias se centran en memorización pasiva sin contexto ni propósito. La clave está en que los estudiantes entiendan 'por qué' y 'cómo' aprender, no solo 'qué' memorizar."
                }
            },
            {
                question: "En una clase de arte, un estudiante muestra resistencia a usar ciertas técnicas porque cree que 'no sabe dibujar'. Según la Rúbrica 1, ¿cómo deberías responder?",
                scenario: "Contexto: Estudiante de 3er medio en clase de arte. Se niega a intentar la técnica de acuarela porque dice 'soy malo para dibujar'.",
                options: [
                    "Demostrarle cómo hacerlo tú mismo y pedir que imite tu estilo",
                    "Reflexionar juntos sobre qué significa 'ser bueno para dibujar' y establecer metas realistas",
                    "Cambiar la actividad a otra técnica que considere más fácil",
                    "Decirle que con práctica todos pueden mejorar"
                ],
                correctAnswer: 1,
                feedback: {
                    correct: "Excelente! Has integrado perfectamente los tres pilares: despertando interés al reflexionar sobre sus percepciones, fomentando autonomía al permitir que establezca sus propias metas, y promoviendo reflexión sobre el concepto de habilidad.",
                    incorrect: "Estas respuestas son superficiales. Demostrar o cambiar de actividad no aborda las creencias limitantes del estudiante. La clave está en el diálogo reflexivo que transforma su mindset."
                }
            },
            {
                question: "Durante una lección de historia, observas que los estudiantes no comprenden el contexto social de un período histórico. Según la Rúbrica 1, ¿qué acción tomarías?",
                scenario: "Contexto: Clase de historia de Chile sobre la Independencia. Los estudiantes confunden hechos históricos con mitos populares y no distinguen causas sociales de eventos individuales.",
                options: [
                    "Repetir la explicación con términos más simples",
                    "Utilizar mapas conceptuales y diagramas de flujo para visualizar relaciones causa-efecto",
                    "Asignar un ensayo corto para reforzar el concepto",
                    "Proyectar un documental histórico para ilustrar el contexto"
                ],
                correctAnswer: 1,
                feedback: {
                    correct: "¡Muy bien! Has identificado que utilizar representaciones visuales (mapas conceptuales) facilita la comprensión profunda al mostrar relaciones complejas, aplicando así el tercer pilar de la rúbrica.",
                    incorrect: "Aunque algunas acciones podrían ayudar, no abordan la raíz del problema. Repetir o asignar tareas sin contexto no promueve una comprensión significativa."
                }
            },
            {
                question: "En una clase de tecnología, un grupo de estudiantes quiere modificar radicalmente un proyecto original. Según la Rúbrica 1, ¿cómo deberías reaccionar?",
                scenario: "Contexto: Proyecto de robótica escolar. Un grupo propone agregar funciones no contempladas en la guía inicial, argumentando que 'sería más interesante'.",
                options: [
                    "Rechazar la modificación para mantener el cronograma previsto",
                    "Aceptar la modificación pero reducir el tiempo de otras actividades",
                    "Negociar un compromiso: aceptar la modificación si entregan el proyecto base primero",
                    "Delegar la decisión al grupo sin supervisión adicional"
                ],
                correctAnswer: 2,
                feedback: {
                    correct: "Perfecto! Has equilibrado dos pilares clave: fomentando autonomía al permitir modificaciones creativas, pero manteniendo estructura al exigir la entrega del proyecto base primero. Esto enseña responsabilidad y gestión de tiempo.",
                    incorrect: "Estas respuestas no equilibran adecuadamente autonomía y estructura. Rechazar elimina oportunidades de creatividad; delegar sin supervisión puede generar desorganización."
                }
            },
            {
                question: "Antes de una evaluación escrita, ¿qué estrategia recomendarías según la Rúbrica 1 para ayudar a los estudiantes a prepararse de manera efectiva?",
                scenario: "Contexto: Evaluación de matemáticas sobre álgebra. Muchos estudiantes reportan ansiedad y dificultad para organizar su estudio.",
                options: [
                    "Proporcionar un resumen detallado de los temas a estudiar",
                    "Enseñar técnicas de estudio organizadas y metacognitivas (mapas mentales, esquemas)",
                    "Realizar un repaso intensivo la tarde anterior",
                    "Asegurarse de que todos tengan los apuntes completos"
                ],
                correctAnswer: 1,
                feedback: {
                    correct: "¡Excelente! Has aplicado el tercer pilar: promover la reflexión. Enseñar técnicas metacognitivas les permite autorregular su aprendizaje, identificar fortalezas y debilidades, y desarrollar habilidades de estudio independientes.",
                    incorrect: "Estas estrategias son pasivas y dependen del docente. Proporcionar resúmenes o apuntes no enseña a los estudiantes a aprender por sí mismos ni a reflexionar sobre sus procesos."
                }
            },
            {
                question: "En una clase de idiomas, notas que un estudiante siempre se sienta aparte y no participa en las actividades grupales. Según la Rúbrica 1, ¿cómo abordarías esta situación?",
                scenario: "Contexto: Estudiante de 1er medio en clase de inglés. Siempre se sienta en el último pupitre y no interactúa en parejas ni grupos.",
                options: [
                    "Forzarlo a cambiar de asiento y participar",
                    "Hablar con él en privado para entender sus motivos y preferencias",
                    "Ignorarlo para no causar incomodidad",
                    "Eximirlo de las actividades grupales"
                ],
                correctAnswer: 1,
                feedback: {
                    correct: "Correcto! Has mostrado sensibilidad y respeto por la diversidad de estilos de aprendizaje. Entender sus motivos permite adaptar estrategias de inclusión de manera efectiva y respetuosa.",
                    incorrect: "Estas acciones pueden generar rechazo o aislamiento. Forzar o ignorar no promueven una integración positiva ni respetan la autonomía del estudiante."
                }
            },
            {
                question: "Al finalizar una unidad completa, ¿qué método de cierre considerarías más efectivo según la Rúbrica 1?",
                scenario: "Contexto: Unidad sobre sistemas solares terminada. Los estudiantes han aprendido sobre planetas, órbitas y fenómenos astronómicos.",
                options: [
                    "Administrar una prueba escrita para evaluar conocimientos",
                    "Realizar un debate abierto sobre lo más sorprendente que aprendieron",
                    "Asignar un trabajo práctico de investigación individual",
                    "Repasar rápidamente los puntos más importantes"
                ],
                correctAnswer: 1,
                feedback: {
                    correct: "¡Muy bien! Has identificado que los debates promueven la reflexión colectiva, permiten compartir perspectivas diversas y profundizan el aprendizaje a través del diálogo, aplicando así el tercer pilar de la rúbrica.",
                    incorrect: "Aunque algunas actividades tienen valor, no promueven la reflexión profunda. Las pruebas miden memorización; trabajos individuales pueden ser aislados; los repasos son pasivos."
                }
            }
        ];

        // Funciones del juego
        function startGame() {
            const teacherName = document.getElementById('teacher-name').value.trim();
            if (!teacherName) {
                alert('Por favor ingresa tu nombre');
                return;
            }
            
            currentTeacherName = teacherName;
            document.getElementById('start-screen').classList.add('hidden');
            document.getElementById('welcome-screen').classList.remove('hidden');
        }

        function showWelcome() {
            document.getElementById('welcome-screen').classList.remove('hidden');
        }

        function showReading() {
            document.getElementById('welcome-screen').classList.add('hidden');
            document.getElementById('reading-screen').classList.remove('hidden');
        }

        function showText() {
            document.getElementById('reading-screen').classList.add('hidden');
            document.getElementById('full-text-screen').classList.remove('hidden');
        }

        function startQuiz() {
            document.getElementById('full-text-screen').classList.add('hidden');
            document.getElementById('quiz-screen').classList.remove('hidden');
            loadQuestion();
        }

        function loadQuestion() {
            const question = questions[currentQuestionIndex];
            const container = document.getElementById('question-container');
            
            container.innerHTML = `
                <div class="question-card">
                    <h3>Pregunta ${currentQuestionIndex + 1}: ${question.scenario}</h3>
                    <div class="options">
                        ${question.options.map((option, index) => `
                            <div class="option" onclick="selectOption(${index})">
                                <i class="fas fa-comment-dots mr-2"></i>${String.fromCharCode(65 + index)}. ${option}
                            </div>
                        `).join('')}
                    </div>
                </div>
            `;
            
            updateNavigationButtons();
            updateProgress();
        }

        function selectOption(selectedIndex) {
            const question = questions[currentQuestionIndex];
            const isCorrect = selectedIndex === question.correctAnswer;
            
            if (isCorrect) {
                score++;
            }
            
            answeredQuestions[currentQuestionIndex] = {
                selected: selectedIndex,
                correct: question.correctAnswer,
                isCorrect: isCorrect
            };
            
            showFeedback(isCorrect, question.feedback[isCorrect ? 'correct' : 'incorrect']);
            updateScoreDisplay();
        }

        function showFeedback(isCorrect, message) {
            const feedbackContainer = document.getElementById('feedback-container');
            feedbackContainer.className = `feedback ${isCorrect ? 'correct' : 'incorrect'}`;
            feedbackContainer.textContent = message;
            feedbackContainer.classList.remove('hidden');
        }

        function updateNavigationButtons() {
            const prevBtn = document.getElementById('prev-btn');
            const nextBtn = document.getElementById('next-btn');
            const submitBtn = document.getElementById('submit-btn');
            
            if (currentQuestionIndex === 0) {
                prevBtn.classList.add('hidden');
            } else {
                prevBtn.classList.remove('hidden');
            }
            
            if (currentQuestionIndex === questions.length - 1) {
                nextBtn.classList.add('hidden');
                submitBtn.classList.remove('hidden');
            } else {
                nextBtn.classList.remove('hidden');
                submitBtn.classList.add('hidden');
            }
        }

        function updateProgress() {
            const progressFill = document.getElementById('progress-fill');
            const percentage = ((currentQuestionIndex + 1) / questions.length) * 100;
            progressFill.style.width = `${percentage}%`;
        }

        function updateScoreDisplay() {
            const answeredCount = answeredQuestions.filter(q => q !== undefined).length;
            document.getElementById('score-display').textContent = `Preguntas analizadas: ${answeredCount}/${questions.length}`;
        }

        function previousQuestion() {
            if (currentQuestionIndex > 0) {
                currentQuestionIndex--;
                loadQuestion();
            }
        }

        function nextQuestion() {
            if (currentQuestionIndex < questions.length - 1) {
                currentQuestionIndex++;
                loadQuestion();
            }
        }

        function submitQuiz() {
            showResults();
        }

        function showResults() {
            document.getElementById('quiz-screen').classList.add('hidden');
            document.getElementById('results-screen').classList.remove('hidden');
            
            const finalScoreElement = document.getElementById('final-score');
            const resultFeedbackElement = document.getElementById('result-feedback');
            
            const percentage = Math.round((score / questions.length) * 100);
            finalScoreElement.textContent = `Puntuación final: ${score}/${questions.length} (${percentage}%)`;
            
            let feedback = '';
            if (percentage >= 80) {
                feedback = `¡Fantástico, ${currentTeacherName}! Tu puntuación de ${percentage}% indica un excelente dominio de la aplicación práctica de la Rúbrica 1. Eres capaz de tomar decisiones pedagógicas informadas y promover activamente el involucramiento estudiantil.`;
            } else if (percentage >= 60) {
                feedback = `Buen trabajo, ${currentTeacherName}. Con un ${percentage}%, demuestras un buen entendimiento de cómo aplicar la Rúbrica 1 en contextos reales. Considera revisar algunas áreas para fortalecer tu práctica docente.`;
            } else {
                feedback = `Es momento de profundizar, ${currentTeacherName}. Tu puntuación de ${percentage}% indica que necesitas reforzar tu comprensión práctica de la Rúbrica 1. Te recomendamos revisar casos similares y practicar más estrategias pedagógicas.`;
            }
            
            resultFeedbackElement.innerHTML = `<p>${feedback}</p>`;
        }

        function restartGame() {
            currentQuestionIndex = 0;
            score = 0;
            answeredQuestions = [];
            
            document.getElementById('results-screen').classList.add('hidden');
            document.getElementById('start-screen').classList.remove('hidden');
            document.getElementById('teacher-name').value = '';
            document.getElementById('feedback-container').classList.add('hidden');
        }
    </script>
</body>
</html>
