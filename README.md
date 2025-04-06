            <!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Curso de Proyecciones Financieras - UAN</title>
    <style>
        :root {
            --azul-oscuro: #003366;
            --azul-medio: #0055a5;
            --azul-claro: #e6f2ff;
            --blanco: #ffffff;
            --gris: #f5f5f5;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            display: flex;
            min-height: 100vh;
            background-color: var(--gris);
            transition: margin-left 0.5s;
        }
        
        /* Menú lateral */
        .sidebar {
            width: 250px;
            background-color: var(--azul-oscuro);
            color: var(--blanco);
            height: 100vh;
            position: fixed;
            transition: transform 0.5s;
            z-index: 100;
            box-shadow: 2px 0 5px rgba(0, 0, 0, 0.1);
        }
        
        .sidebar.hidden {
            transform: translateX(-250px);
        }
        
        .sidebar-header {
            padding: 20px;
            text-align: center;
            border-bottom: 1px solid var(--azul-medio);
        }
        
        .sidebar-header img {
            max-width: 80%;
            margin-bottom: 10px;
        }
        
        .sidebar-menu {
            padding: 20px 0;
        }
        
        .sidebar-menu ul {
            list-style: none;
        }
        
        .sidebar-menu li {
            margin-bottom: 5px;
        }
        
        .sidebar-menu a {
            display: block;
            padding: 12px 20px;
            color: var(--blanco);
            text-decoration: none;
            transition: background-color 0.3s;
        }
        
        .sidebar-menu a:hover {
            background-color: var(--azul-medio);
        }
        
        .sidebar-menu a.active {
            background-color: var(--azul-medio);
            border-left: 4px solid var(--blanco);
        }
        
        /* Botón para ocultar/mostrar menú */
        .toggle-btn {
            position: fixed;
            left: 260px;
            top: 20px;
            background-color: var(--azul-oscuro);
            color: var(--blanco);
            border: none;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            cursor: pointer;
            z-index: 101;
            transition: left 0.5s;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }
        
        .toggle-btn.hidden {
            left: 10px;
        }
        
        /* Contenido principal */
        .main-content {
            flex: 1;
            margin-left: 250px;
            transition: margin-left 0.5s;
            padding: 20px;
        }
        
        .main-content.full-width {
            margin-left: 0;
        }
        
        /* Header */
        .header {
            background-color: var(--azul-oscuro);
            color: var(--blanco);
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        
        .header h1 {
            font-size: 24px;
        }
        
        .logo-container {
            display: flex;
            align-items: center;
        }
        
        .logo-container img {
            max-height: 60px;
            margin-right: 15px;
        }
        
        /* Secciones */
        .section {
            background-color: var(--blanco);
            border-radius: 8px;
            padding: 25px;
            margin-bottom: 20px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        
        .section h2 {
            color: var(--azul-oscuro);
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--azul-claro);
        }
        
        .section h3 {
            color: var(--azul-medio);
            margin: 15px 0 10px;
        }
        
        .section p, .section ul {
            margin-bottom: 15px;
            line-height: 1.6;
        }
        
        .section ul {
            padding-left: 20px;
        }
        
        .section li {
            margin-bottom: 8px;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .sidebar {
                transform: translateX(-250px);
            }
            
            .sidebar.hidden {
                transform: translateX(0);
            }
            
            .main-content {
                margin-left: 0;
            }
            
            .toggle-btn {
                left: 10px;
            }
            
            .toggle-btn.hidden {
                left: 260px;
            }
        }
    </style>
</head>
<body>
    <!-- Menú lateral -->
    <div class="sidebar" id="sidebar">
        <div class="sidebar-header">
            <img src="chatgpt-image-5-abr-2025-19-08-42.png" alt="Logo UAN">
            <h3>Contaduría Pública</h3>
        </div>
        <div class="sidebar-menu">
            <ul>
                <li><a href="#inicio" class="active">Inicio</a></li>
                <li><a href="#objetivos">Objetivos</a></li>
                <li><a href="#contenido">Contenido</a></li>
                <li><a href="#metodologia">Metodología</a></li>
                <li><a href="#evaluacion">Evaluación</a></li>
                <li><a href="#requisitos">Requisitos</a></li>
            </ul>
        </div>
    </div>
    
    <!-- Botón para ocultar/mostrar menú -->
    <button class="toggle-btn" id="toggleBtn">≡</button>
    
    <!-- Contenido principal -->
    <div class="main-content" id="mainContent">
        <!-- Header -->
        <div class="header">
            <div class="logo-container">
                <img src="chatgpt-image-5-abr-2025-19-12-15.png" alt="Logo Contaduría">
                <h1>Curso de Proyecciones Financieras</h1>
            </div>
        </div>
        
        <!-- Sección Inicio -->
        <section id="inicio" class="section">
            <h2>Bienvenido al Curso de Proyecciones Financieras</h2>
            <p>¡Es hora de poner en práctica tus habilidades contables y financieras de manera creativa!</p>
            <p>A lo largo de este curso, tendrás la oportunidad de desarrollar un plan de inversión único que combine tus conocimientos técnicos con tu creatividad para abordar los desafíos del mercado. No solo aprenderás a medir proyecciones financieras, sino también a presentar propuestas atractivas que puedan captar la atención de inversores reales.</p>
        </section>
        
        <!-- Sección Objetivos -->
        <section id="objetivos" class="section">
            <h2>Objetivos del curso</h2>
            <p>Al finalizar el curso, los estudiantes serán capaces de:</p>
            <ul>
                <li>Comprender y aplicar las metodologías de medición y evaluación de proyectos de inversión.</li>
                <li>Desarrollar proyecciones financieras detalladas para proyectos a corto, mediano y largo plazo.</li>
                <li>Utilizar herramientas y técnicas de análisis financiero para la toma de decisiones informadas.</li>
                <li>Crear planes de inversión sostenibles y atractivos para potenciales inversores, basados en datos concretos y proyecciones realistas.</li>
            </ul>
        </section>
        
        <!-- Sección Contenido -->
        <section id="contenido" class="section">
            <h2>Contenido del curso</h2>
            <p>Durante el curso abordaremos los siguientes temas clave:</p>
            
            <h3>Introducción a las proyecciones financieras</h3>
            <ul>
                <li>Definición y tipos de proyecciones</li>
                <li>Conceptos clave de análisis financiero</li>
                <li>La importancia de las proyecciones para la toma de decisiones empresariales</li>
            </ul>
            
            <h3>Metodologías de medición de proyectos de inversión</h3>
            <ul>
                <li>VAN (Valor Actual Neto) y TIR (Tasa Interna de Retorno)</li>
                <li>Flujo de caja proyectado y análisis de sensibilidad</li>
                <li>Riesgos y variables económicas a considerar</li>
            </ul>
            
            <h3>Elaboración de un plan de inversión</h3>
            <ul>
                <li>Investigación de mercado y análisis de competencia</li>
                <li>Estructura y componentes de un plan de inversión</li>
                <li>Presentación de proyecciones financieras atractivas y viables</li>
            </ul>
            
            <h3>Análisis y presentación de resultados financieros</h3>
            <ul>
                <li>Interpretación de los resultados obtenidos en las proyecciones</li>
                <li>Herramientas gráficas y visualización de datos</li>
                <li>Cómo estructurar un informe de inversión convincente</li>
            </ul>
        </section>
        
        <!-- Sección Metodología -->
        <section id="metodologia" class="section">
            <h2>Metodología</h2>
            <p>El curso será 100% interactivo, con clases teóricas y prácticas. Los estudiantes realizarán ejercicios, estudios de caso y finalmente, desarrollarán su propio plan de inversión. Durante las semanas de trabajo práctico, podrán contar con retroalimentación constante y personalizada.</p>
            <p><strong>Modalidad:</strong> Presencial</p>
        </section>
        
        <!-- Sección Evaluación -->
        <section id="evaluacion" class="section">
            <h2>Evaluación</h2>
            <p>La evaluación será continua y se basará en los siguientes criterios:</p>
            <ul>
                <li><strong>Participación activa en clases (20%)</strong></li>
                <li><strong>Ejercicios y estudios de caso (30%)</strong></li>
                <li><strong>Presentación y desarrollo del plan de inversión (50%)</strong></li>
            </ul>
        </section>
        
        <!-- Sección Requisitos -->
        <section id="requisitos" class="section">
            <h2>Requisitos para el curso</h2>
            <ul>
                <li>Tener conocimientos previos en contabilidad financiera y análisis de estados financieros.</li>
                <li>Tener acceso a herramientas básicas de software de hojas de cálculo (como Excel o Google Sheets) para realizar cálculos y simulaciones.</li>
            </ul>
        </section>
    </div>

    <script>
        // Función para ocultar/mostrar el menú lateral
        document.getElementById('toggleBtn').addEventListener('click', function() {
            const sidebar = document.getElementById('sidebar');
            const mainContent = document.getElementById('mainContent');
            const toggleBtn = document.getElementById('toggleBtn');
            
            sidebar.classList.toggle('hidden');
            mainContent.classList.toggle('full-width');
            toggleBtn.classList.toggle('hidden');
            
            // Cambiar el ícono del botón
            if (sidebar.classList.contains('hidden')) {
                toggleBtn.textContent = '≡';
            } else {
                toggleBtn.textContent = '×';
            }
        });
        
        // Función para resaltar el enlace activo en el menú
        document.querySelectorAll('.sidebar-menu a').forEach(link => {
            link.addEventListener('click', function(e) {
                // Prevenir el comportamiento predeterminado solo para enlaces que no son #
                if (this.getAttribute('href') === '#') {
                    e.preventDefault();
                }
                
                document.querySelectorAll('.sidebar-menu a').forEach(item => {
                    item.classList.remove('active');
                });
                this.classList.add('active');
            });
        });
        
        // Activar el enlace correspondiente al hacer scroll
        window.addEventListener('scroll', function() {
            const sections = document.querySelectorAll('.section');
            const navLinks = document.querySelectorAll('.sidebar-menu a');
            
            let curre   nt = '';
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                
                if (pageYOffset >= (sectionTop - 100)) {
                    current = section.getAttribute('id');
                }
            });
            
            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href') === `#${current}`) {
                    link.classList.add('active');
                }
            });
        });
    </script>
</body>
</html># Pagina-web-
