<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alejandro 2026 | Equipos de Campaña</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700;800&family=Quicksand:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Quicksand', sans-serif;
            background: linear-gradient(135deg, #e0f2fe 0%, #fce7f3 50%, #fef3c7 100%);
            overflow-x: hidden;
            color: #1e293b;
        }
        
        h1, h2, h3, .title-font {
            font-family: 'Poppins', sans-serif;
        }
        
        /* Soft Colors */
        .bg-soft-blue { background: rgba(224, 242, 254, 0.8); }
        .bg-soft-pink { background: rgba(252, 231, 243, 0.8); }
        .bg-soft-yellow { background: rgba(254, 243, 199, 0.8); }
        .bg-soft-green { background: rgba(220, 252, 231, 0.8); }
        .bg-soft-purple { background: rgba(243, 232, 255, 0.8); }
        
        .text-soft-blue { color: #0369a1; }
        .text-soft-pink { color: #be185d; }
        .text-soft-yellow { color: #b45309; }
        .text-soft-green { color: #15803d; }
        .text-soft-purple { color: #7c3aed; }
        
        /* 3D Card Effects */
        .card-3d {
            background: rgba(255, 255, 255, 0.7);
            backdrop-filter: blur(20px);
            border-radius: 30px;
            border: 1px solid rgba(255, 255, 255, 0.5);
            box-shadow: 
                0 10px 40px rgba(0, 0, 0, 0.1),
                0 0 0 1px rgba(255, 255, 255, 0.6) inset;
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            transform-style: preserve-3d;
        }
        
        .card-3d:hover {
            transform: translateY(-15px) rotateX(5deg) rotateY(5deg);
            box-shadow: 
                0 30px 60px rgba(0, 0, 0, 0.15),
                0 0 0 1px rgba(255, 255, 255, 0.8) inset;
        }
        
        /* Floating Animation */
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(2deg); }
        }
        
        @keyframes float-delayed {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-15px) rotate(-2deg); }
        }
        
        @keyframes pulse-soft {
            0%, 100% { transform: scale(1); opacity: 0.8; }
            50% { transform: scale(1.05); opacity: 1; }
        }
        
        @keyframes shimmer {
            0% { background-position: -200% center; }
            100% { background-position: 200% center; }
        }
        
        .float { animation: float 6s ease-in-out infinite; }
        .float-2 { animation: float-delayed 7s ease-in-out infinite; }
        .float-3 { animation: float 5s ease-in-out infinite; animation-delay: 1s; }
        
        /* Gradient Text */
        .gradient-text {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 25%, #f093fb 50%, #f5576c 75%, #ffd89b 100%);
            background-size: 200% auto;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: shimmer 3s linear infinite;
        }
        
        /* Team Section Styles */
        .team-section {
            background: rgba(255, 255, 255, 0.5);
            border-radius: 40px;
            padding: 3rem;
            margin-bottom: 3rem;
            border: 2px solid rgba(255, 255, 255, 0.6);
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.08);
        }
        
        .team-badge {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            padding: 0.75rem 1.5rem;
            border-radius: 50px;
            font-weight: 700;
            font-size: 0.9rem;
            margin-bottom: 2rem;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }
        
        /* Role Cards */
        .role-card {
            position: relative;
            overflow: hidden;
        }
        
        .role-card::after {
            content: attr(data-role);
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(to top, rgba(0,0,0,0.8), transparent);
            color: white;
            padding: 1rem;
            font-size: 0.75rem;
            font-weight: 600;
            text-align: center;
            transform: translateY(100%);
            transition: transform 0.3s;
        }
        
        .role-card:hover::after {
            transform: translateY(0);
        }
        
        /* Interactive Buttons */
        .btn-magic {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 1rem 2.5rem;
            border-radius: 50px;
            font-weight: 700;
            border: none;
            cursor: pointer;
            position: relative;
            overflow: hidden;
            transition: all 0.3s;
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.3);
        }
        
        .btn-magic::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.4), transparent);
            transition: left 0.5s;
        }
        
        .btn-magic:hover::before {
            left: 100%;
        }
        
        .btn-magic:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 20px 40px rgba(102, 126, 234, 0.4);
        }
        
        /* Hearts Animation */
        .heart {
            position: fixed;
            color: #ec4899;
            font-size: 1.5rem;
            pointer-events: none;
            animation: fly-heart 4s ease-out forwards;
            z-index: 1000;
        }
        
        @keyframes fly-heart {
            0% {
                opacity: 1;
                transform: translateY(0) scale(0) rotate(0deg);
            }
            50% {
                opacity: 1;
                transform: translateY(-50vh) scale(1) rotate(180deg);
            }
            100% {
                opacity: 0;
                transform: translateY(-100vh) scale(0.5) rotate(360deg);
            }
        }
        
        /* Proposal Cards */
        .proposal-card {
            background: linear-gradient(135deg, rgba(255,255,255,0.9), rgba(255,255,255,0.7));
            border-radius: 24px;
            padding: 2rem;
            position: relative;
            overflow: hidden;
            transition: all 0.4s;
            border: 2px solid transparent;
        }
        
        .proposal-card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.8) 0%, transparent 70%);
            opacity: 0;
            transition: opacity 0.3s;
        }
        
        .proposal-card:hover::before {
            opacity: 1;
        }
        
        .proposal-card:hover {
            transform: translateY(-10px) scale(1.02);
            border-color: rgba(102, 126, 234, 0.3);
        }
        
        .proposal-icon {
            width: 70px;
            height: 70px;
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            margin-bottom: 1rem;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        /* Canvas Container */
        #canvas-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
        }
        
        /* Navigation Dots */
        .nav-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: rgba(0,0,0,0.2);
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .nav-dot.active {
            background: #667eea;
            transform: scale(1.3);
            box-shadow: 0 0 10px rgba(102, 126, 234, 0.5);
        }
        
        /* Section transitions */
        .section {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            z-index: 1;
        }
        
        /* Confetti */
        .confetti {
            position: fixed;
            width: 10px;
            height: 10px;
            pointer-events: none;
            animation: confetti-fall 3s ease-out forwards;
        }
        
        @keyframes confetti-fall {
            0% { transform: translateY(-100px) rotate(0deg); opacity: 1; }
            100% { transform: translateY(100vh) rotate(720deg); opacity: 0; }
        }
        
        /* Leader Crown */
        .leader-crown {
            position: absolute;
            top: -10px;
            right: -10px;
            font-size: 2rem;
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
    </style>
</head>
<body>

    <!-- Background Canvas for Particles -->
    <div id="canvas-container"></div>

    <!-- Floating Hearts on Click -->
    <script>
        document.addEventListener('click', (e) => {
            const heart = document.createElement('div');
            heart.className = 'heart';
            heart.innerHTML = '💖';
            heart.style.left = e.clientX + 'px';
            heart.style.top = e.clientY + 'px';
            document.body.appendChild(heart);
            setTimeout(() => heart.remove(), 4000);
        });
    </script>

    <!-- Section 1: Hero -->
    <section class="section px-6" id="hero">
        <div class="text-center max-w-5xl relative z-10">
            <div class="mb-8 float">
                <div class="inline-block p-6 rounded-full bg-white/80 shadow-2xl">
                    <span class="text-6xl">🗳️</span>
                </div>
            </div>
            
            <div class="mb-6">
                <span class="px-6 py-2 rounded-full bg-gradient-to-r from-purple-400 to-pink-400 text-white font-bold text-sm tracking-wider shadow-lg">
                    CAMPAÑA 2026
                </span>
            </div>
            
            <h1 class="text-6xl md:text-8xl font-black mb-6 gradient-text title-font">
                ALEJANDRO
            </h1>
            
            <h2 class="text-3xl md:text-4xl font-bold mb-6 text-gray-700">
                Tu Voz, <span class="text-soft-purple">Nuestro Colegio</span>
            </h2>
            
            <p class="text-xl text-gray-600 mb-8 max-w-2xl mx-auto leading-relaxed">
                Un liderazgo organizado, un equipo comprometido. 
                Juntos construiremos el cambio que queremos ver. 💫
            </p>
            
            <button class="btn-magic text-lg" onclick="scrollToSection('equipos')">
                Conoce los Equipos <i class="fas fa-users ml-2"></i>
            </button>
            
            <div class="mt-12 flex justify-center gap-8 text-gray-500">
                <div class="text-center">
                    <div class="text-3xl mb-2">👑</div>
                    <div class="text-sm font-semibold">Liderazgo</div>
                </div>
                <div class="text-center">
                    <div class="text-3xl mb-2">🎨</div>
                    <div class="text-sm font-semibold">Creatividad</div>
                </div>
                <div class="text-center">
                    <div class="text-3xl mb-2">📢</div>
                    <div class="text-sm font-semibold">Comunicación</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 2: Teams -->
    <section class="section px-6 bg-soft-blue/30" id="equipos">
        <div class="max-w-7xl mx-auto w-full">
            <div class="text-center mb-12">
                <h2 class="text-5xl font-bold mb-4 text-gray-800">Nuestros Equipos</h2>
                <p class="text-xl text-gray-600">Cada persona con su talento y función específica</p>
                <div class="w-24 h-1 bg-gradient-to-r from-purple-400 to-pink-400 mx-auto mt-4 rounded-full"></div>
            </div>

            <!-- EQUIPO 1: JEFES DE CAMPAÑA -->
            <div class="team-section">
                <div class="team-badge bg-gradient-to-r from-amber-400 to-orange-500 text-white">
                    <i class="fas fa-crown"></i>
                    JEFES DE CAMPAÑA
                </div>
                
                <div class="grid md:grid-cols-3 gap-8">
                    <!-- Alejandro - Personero -->
                    <div class="card-3d p-8 text-center relative role-card" data-role="PERSONERO • Líder de la Campaña">
                        <div class="leader-crown">👑</div>
                        <div class="w-28 h-28 mx-auto mb-6 rounded-full bg-gradient-to-br from-amber-400 via-orange-500 to-red-500 flex items-center justify-center text-5xl shadow-2xl ring-4 ring-amber-200">
                            🦁
                        </div>
                        <h3 class="text-2xl font-bold mb-2 text-gray-800">Alejandro</h3>
                        <p class="text-lg text-amber-600 font-bold mb-3">PERSONERO</p>
                        <div class="space-y-2 text-sm text-gray-600">
                            <p>🎯 Representante estudiantil</p>
                            <p>📢 Voz ante directivos</p>
                            <p>⚡ Toma de decisiones</p>
                            <p>🤝 Liderazgo del equipo</p>
                        </div>
                        <div class="mt-4 px-4 py-2 bg-amber-100 rounded-full text-xs text-amber-700 font-semibold">
                            Jefe Máximo
                        </div>
                    </div>

                    <!-- Sirley - Jefa de Campaña -->
                    <div class="card-3d p-8 text-center relative role-card float" data-role="JEFA DE CAMPAÑA • Coordinación General">
                        <div class="w-24 h-24 mx-auto mb-6 rounded-full bg-gradient-to-br from-purple-400 to-pink-500 flex items-center justify-center text-4xl shadow-xl">
                            🌟
                        </div>
                        <h3 class="text-xl font-bold mb-2 text-gray-800">Sirley</h3>
                        <p class="text-base text-purple-600 font-bold mb-3">JEFA DE CAMPAÑA</p>
                        <div class="space-y-2 text-sm text-gray-600">
                            <p>📋 Organización general</p>
                            <p>👥 Coordinación de equipos</p>
                            <p>📅 Planificación estratégica</p>
                            <p>✅ Seguimiento de metas</p>
                        </div>
                        <div class="mt-4 px-4 py-2 bg-purple-100 rounded-full text-xs text-purple-700 font-semibold">
                            Coordinadora General
                        </div>
                    </div>

                    <!-- Galvis - Jefe de Campaña + Diseño -->
                    <div class="card-3d p-8 text-center relative role-card float-2" data-role="JEFE DE CAMPAÑA + DISEÑO • Estrategia Visual">
                        <div class="w-24 h-24 mx-auto mb-6 rounded-full bg-gradient-to-br from-indigo-400 to-purple-500 flex items-center justify-center text-4xl shadow-xl">
                            🎨
                        </div>
                        <h3 class="text-xl font-bold mb-2 text-gray-800">Galvis</h3>
                        <p class="text-base text-indigo-600 font-bold mb-3">JEFE DE CAMPAÑA + DISEÑO</p>
                        <div class="space-y-2 text-sm text-gray-600">
                            <p>🎯 Estrategia de campaña</p>
                            <p>🖌️ Dirección artística</p>
                            <p>📐 Diseño de materiales</p>
                            <p>✨ Identidad visual</p>
                        </div>
                        <div class="mt-4 px-4 py-2 bg-indigo-100 rounded-full text-xs text-indigo-700 font-semibold">
                            Estrategia + Arte
                        </div>
                    </div>
                </div>
            </div>

            <!-- EQUIPO 2: DISEÑO Y PUBLICIDAD -->
            <div class="team-section">
                <div class="team-badge bg-gradient-to-r from-pink-400 to-rose-500 text-white">
                    <i class="fas fa-palette"></i>
                    DISEÑO ARTÍSTICO Y PUBLICIDAD
                </div>
                
                <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
                    <!-- María José - Jefa de Diseño -->
                    <div class="card-3d p-6 text-center relative role-card float" data-role="JEFA DE DISEÑO • Creatividad Visual">
                        <div class="w-20 h-20 mx-auto mb-4 rounded-full bg-gradient-to-br from-pink-400 to-rose-500 flex items-center justify-center text-3xl shadow-lg">
                            🎭
                        </div>
                        <h3 class="text-lg font-bold mb-1 text-gray-800">María José</h3>
                        <p class="text-sm text-pink-600 font-bold mb-2">JEFA DE DISEÑO</p>
                        <div class="text-xs text-gray-600 space-y-1">
                            <p>🎨 Conceptos creativos</p>
                            <p>🖼️ Arte de campaña</p>
                            <p>🎪 Decoración eventos</p>
                        </div>
                    </div>

                    <!-- Amaya - Ilustración -->
                    <div class="card-3d p-6 text-center relative role-card float-2" data-role="ILUSTRADORA • Arte Digital">
                        <div class="w-20 h-20 mx-auto mb-4 rounded-full bg-gradient-to-br from-cyan-400 to-blue-500 flex items-center justify-center text-3xl shadow-lg">
                            ✏️
                        </div>
                        <h3 class="text-lg font-bold mb-1 text-gray-800">Amaya</h3>
                        <p class="text-sm text-cyan-600 font-bold mb-2">ILUSTRADORA</p>
                        <div class="text-xs text-gray-600 space-y-1">
                            <p>🎨 Dibujos y carteles</p>
                            <p>✏️ Ilustraciones</p>
                            <p>🖌️ Arte manual</p>
                        </div>
                    </div>

                    <!-- Dara Valentina - Diseño Gráfico -->
                    <div class="card-3d p-6 text-center relative role-card float-3" data-role="DISEÑADORA GRÁFICA • Digital">
                        <div class="w-20 h-20 mx-auto mb-4 rounded-full bg-gradient-to-br from-violet-400 to-purple-500 flex items-center justify-center text-3xl shadow-lg">
                            💻
                        </div>
                        <h3 class="text-lg font-bold mb-1 text-gray-800">Dara Valentina</h3>
                        <p class="text-sm text-violet-600 font-bold mb-2">DISEÑO GRÁFICO</p>
                        <div class="text-xs text-gray-600 space-y-1">
                            <p>💻 Edición digital</p>
                            <p>📱 Posts redes sociales</p>
                            <p>🎨 Canva/Photoshop</p>
                        </div>
                    </div>

                    <!-- Víctor Cuadros - Fotografía -->
                    <div class="card-3d p-6 text-center relative role-card float" data-role="FOTÓGRAFO • Registro Visual">
                        <div class="w-20 h-20 mx-auto mb-4 rounded-full bg-gradient-to-br from-teal-400 to-emerald-500 flex items-center justify-center text-3xl shadow-lg">
                            📸
                        </div>
                        <h3 class="text-lg font-bold mb-1 text-gray-800">Víctor Cuadros</h3>
                        <p class="text-sm text-teal-600 font-bold mb-2">FOTÓGRAFO</p>
                        <div class="text-xs text-gray-600 space-y-1">
                            <p>📸 Fotos de campaña</p>
                            <p>🎥 Videos cortos</p>
                            <p>📱 Contenido reels</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- EQUIPO 3: LOGÍSTICA Y OPERACIONES -->
            <div class="team-section">
                <div class="team-badge bg-gradient-to-r from-green-400 to-emerald-500 text-white">
                    <i class="fas fa-cogs"></i>
                    LOGÍSTICA Y OPERACIONES
                </div>
                
                <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
                    <!-- Yeili - Organización de Eventos -->
                    <div class="card-3d p-6 text-center relative role-card float" data-role="EVENTOS • Producción">
                        <div class="w-20 h-20 mx-auto mb-4 rounded-full bg-gradient-to-br from-yellow-400 to-orange-500 flex items-center justify-center text-3xl shadow-lg">
                            🎪
                        </div>
                        <h3 class="text-lg font-bold mb-1 text-gray-800">Yeili</h3>
                        <p class="text-sm text-yellow-600 font-bold mb-2">ORGANIZADORA DE EVENTOS</p>
                        <div class="text-xs text-gray-600 space-y-1">
                            <p>🎪 Planificación eventos</p>
                            <p>📋 Cronogramas</p>
                            <p>✅ Checklist actividades</p>
                        </div>
                    </div>

                    <!-- Camilo - Recursos Materiales -->
                    <div class="card-3d p-6 text-center relative role-card float-2" data-role="LOGÍSTICA • Materiales">
                        <div class="w-20 h-20 mx-auto mb-4 rounded-full bg-gradient-to-br from-red-400 to-pink-500 flex items-center justify-center text-3xl shadow-lg">
                            📦
                        </div>
                        <h3 class="text-lg font-bold mb-1 text-gray-800">Camilo</h3>
                        <p class="text-sm text-red-600 font-bold mb-2">RECURSOS MATERIALES</p>
                        <div class="text-xs text-gray-600 space-y-1">
                            <p>📦 Materiales campaña</p>
                            <p>🎨 Suministros arte</p>
                            <p>💰 Presupuesto</p>
                        </div>
                    </div>

                    <!-- Diego - Reciclaje y Ambiente -->
                    <div class="card-3d p-6 text-center relative role-card float-3" data-role="SOSTENIBILIDAD • Proyecto Verde">
                        <div class="w-20 h-20 mx-auto mb-4 rounded-full bg-gradient-to-br from-green-400 to-teal-500 flex items-center justify-center text-3xl shadow-lg">
                            ♻️
                        </div>
                        <h3 class="text-lg font-bold mb-1 text-gray-800">Diego</h3>
                        <p class="text-sm text-green-600 font-bold mb-2">COORDINADOR DE RECICLAJE</p>
                        <div class="text-xs text-gray-600 space-y-1">
                            <p>♻️ Centro de recolección</p>
                            <p>🌱 Proyectos verdes</p>
                            <p>📊 Campañas ambientales</p>
                        </div>
                    </div>

                    <!-- David - Técnico y Sonido -->
                    <div class="card-3d p-6 text-center relative role-card float" data-role="TÉCNICO • Audio y Equipos">
                        <div class="w-20 h-20 mx-auto mb-4 rounded-full bg-gradient-to-br from-gray-400 to-slate-500 flex items-center justify-center text-3xl shadow-lg">
                            🔧
                        </div>
                        <h3 class="text-lg font-bold mb-1 text-gray-800">David</h3>
                        <p class="text-sm text-gray-600 font-bold mb-2">TÉCNICO Y SONIDO</p>
                        <div class="text-xs text-gray-600 space-y-1">
                            <p>🔊 Equipo de sonido</p>
                            <p>💻 Proyecciones</p>
                            <p>🔧 Montaje eventos</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- EQUIPO 4: COMUNICACIÓN Y REDES -->
            <div class="team-section">
                <div class="team-badge bg-gradient-to-r from-blue-400 to-indigo-500 text-white">
                    <i class="fas fa-bullhorn"></i>
                    COMUNICACIÓN Y REDES SOCIALES
                </div>
                
                <div class="grid md:grid-cols-2 gap-8 max-w-4xl mx-auto">
                    <!-- Liceth - Redes Sociales -->
                    <div class="card-3d p-8 text-center relative role-card float" data-role="COMMUNITY MANAGER • Redes">
                        <div class="w-24 h-24 mx-auto mb-6 rounded-full bg-gradient-to-br from-blue-400 to-cyan-500 flex items-center justify-center text-4xl shadow-xl">
                            📱
                        </div>
                        <h3 class="text-xl font-bold mb-2 text-gray-800">Liceth</h3>
                        <p class="text-base text-blue-600 font-bold mb-3">REDES SOCIALES</p>
                        <div class="space-y-2 text-sm text-gray-600">
                            <p>📱 Instagram de campaña</p>
                            <p>💬 WhatsApp grupos</p>
                            <p>📲 TikTok contenido</p>
                            <p>👥 Interacción followers</p>
                        </div>
                        <div class="mt-4 px-4 py-2 bg-blue-100 rounded-full text-xs text-blue-700 font-semibold">
                            Community Manager
                        </div>
                    </div>

                    <!-- (Espacio para más si quieres añadir alguien más) -->
                    <div class="card-3d p-8 text-center bg-white/30 border-2 border-dashed border-blue-300 flex items-center justify-center">
                        <div class="text-center">
                            <div class="text-4xl mb-4">➕</div>
                            <p class="text-gray-500 font-medium">¿Más al equipo?</p>
                            <p class="text-sm text-gray-400">¡La familia crece!</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 3: Proposals -->
    <section class="section px-6" id="propuestas">
        <div class="max-w-6xl mx-auto w-full">
            <div class="text-center mb-16">
                <h2 class="text-5xl font-bold mb-4 text-gray-800">Nuestras Propuestas</h2>
                <p class="text-xl text-gray-600">Ideas de todo el equipo para mejorar el colegio</p>
                <div class="w-24 h-1 bg-gradient-to-r from-green-400 to-blue-400 mx-auto mt-4 rounded-full"></div>
            </div>

            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Proposal 1: Recycling -->
                <div class="proposal-card shadow-xl">
                    <div class="proposal-icon bg-gradient-to-br from-green-400 to-emerald-500 text-white">
                        ♻️
                    </div>
                    <h3 class="text-xl font-bold mb-3 text-gray-800">Centro de Recolección</h3>
                    <p class="text-gray-600 mb-4 text-sm leading-relaxed">
                        <strong>Diego</strong> lidera este proyecto. Crear un centro de reciclaje para apoyar al medio ambiente. 
                        Separación de plásticos, papel y orgánicos.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-green-100 text-green-700 rounded-full text-xs font-semibold">🌍 Ambiental</span>
                        <span class="px-3 py-1 bg-blue-100 text-blue-700 rounded-full text-xs font-semibold">♻️ Diego</span>
                    </div>
                </div>

                <!-- Proposal 2: More Projects -->
                <div class="proposal-card shadow-xl">
                    <div class="proposal-icon bg-gradient-to-br from-purple-400 to-indigo-500 text-white">
                        🚀
                    </div>
                    <h3 class="text-xl font-bold mb-3 text-gray-800">Más Proyectos</h3>
                    <p class="text-gray-600 mb-4 text-sm leading-relaxed">
                        <strong>Yeili</strong> y <strong>Camilo</strong> coordinan. Impulsar iniciativas estudiantiles: 
                        ferias de ciencia, emprendimiento y arte.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-purple-100 text-purple-700 rounded-full text-xs font-semibold">💡 Innovación</span>
                        <span class="px-3 py-1 bg-pink-100 text-pink-700 rounded-full text-xs font-semibold">🎪 Yeili + Camilo</span>
                    </div>
                </div>

                <!-- Proposal 3: Tournaments -->
                <div class="proposal-card shadow-xl">
                    <div class="proposal-icon bg-gradient-to-br from-orange-400 to-red-500 text-white">
                        🏆
                    </div>
                    <h3 class="text-xl font-bold mb-3 text-gray-800">Torneos de Juego</h3>
                    <p class="text-gray-600 mb-4 text-sm leading-relaxed">
                        <strong>David</strong> se encarga del audio/sonido. Competencias deportivas, e-sports y juegos de mesa. 
                        ¡Integración y diversión!
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-orange-100 text-orange-700 rounded-full text-xs font-semibold">⚽ Deporte</span>
                        <span class="px-3 py-1 bg-gray-100 text-gray-700 rounded-full text-xs font-semibold">🔧 David</span>
                    </div>
                </div>

                <!-- Proposal 4: Environmental Campaigns -->
                <div class="proposal-card shadow-xl">
                    <div class="proposal-icon bg-gradient-to-br from-teal-400 to-cyan-500 text-white">
                        🌱
                    </div>
                    <h3 class="text-xl font-bold mb-3 text-gray-800">Campañas Ambientales</h3>
                    <p class="text-gray-600 mb-4 text-sm leading-relaxed">
                        <strong>Diego</strong> + <strong>Víctor Cuadros</strong> (fotos). Jornadas de limpieza, siembra de árboles 
                        y concientización verde.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-teal-100 text-teal-700 rounded-full text-xs font-semibold">🌳 Naturaleza</span>
                        <span class="px-3 py-1 bg-green-100 text-green-700 rounded-full text-xs font-semibold">♻️ Diego + 📸 Víctor</span>
                    </div>
                </div>

                <!-- Proposal 5: Cultural Activities -->
                <div class="proposal-card shadow-xl">
                    <div class="proposal-icon bg-gradient-to-br from-pink-400 to-rose-500 text-white">
                        🎭
                    </div>
                    <h3 class="text-xl font-bold mb-3 text-gray-800">Actividades Culturales</h3>
                    <p class="text-gray-600 mb-4 text-sm leading-relaxed">
                        <strong>María José</strong> y el equipo de diseño. Más eventos artísticos, musicales, 
                        teatro y danza. ¡Celebrar nuestras raíces!
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-pink-100 text-pink-700 rounded-full text-xs font-semibold">🎨 Arte</span>
                        <span class="px-3 py-1 bg-purple-100 text-purple-700 rounded-full text-xs font-semibold">🎭 María José + Equipo</span>
                    </div>
                </div>

                <!-- Proposal 6: Sports -->
                <div class="proposal-card shadow-xl">
                    <div class="proposal-icon bg-gradient-to-br from-yellow-400 to-amber-500 text-white">
                        ⚡
                    </div>
                    <h3 class="text-xl font-bold mb-3 text-gray-800">Actividades Deportivas</h3>
                    <p class="text-gray-600 mb-4 text-sm leading-relaxed">
                        <strong>Yeili</strong> organiza. Torneos intercursos, días de actividad física 
                        y clubs deportivos para todos.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-yellow-100 text-yellow-700 rounded-full text-xs font-semibold">🏃 Salud</span>
                        <span class="px-3 py-1 bg-orange-100 text-orange-700 rounded-full text-xs font-semibold">🎪 Yeili</span>
                    </div>
                </div>

                <!-- Proposal 7: Communication -->
                <div class="proposal-card shadow-xl">
                    <div class="proposal-icon bg-gradient-to-br from-blue-400 to-indigo-500 text-white">
                        💬
                    </div>
                    <h3 class="text-xl font-bold mb-3 text-gray-800">Mejor Comunicación</h3>
                    <p class="text-gray-600 mb-4 text-sm leading-relaxed">
                        <strong>Liceth</strong> + <strong>Alejandro</strong>. Puente directo estudiantes-directivos. 
                        Asambleas, buzón de sugerencias y transparencia.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-blue-100 text-blue-700 rounded-full text-xs font-semibold">🗣️ Diálogo</span>
                        <span class="px-3 py-1 bg-indigo-100 text-indigo-700 rounded-full text-xs font-semibold">📱 Liceth + 👑 Alejandro</span>
                    </div>
                </div>

                <!-- Proposal 8: Academic Support -->
                <div class="proposal-card shadow-xl">
                    <div class="proposal-icon bg-gradient-to-br from-violet-400 to-purple-500 text-white">
                        📚
                    </div>
                    <h3 class="text-xl font-bold mb-3 text-gray-800">Apoyo Académico</h3>
                    <p class="text-gray-600 mb-4 text-sm leading-relaxed">
                        <strong>Sirley</strong> coordina. Programa de tutorías entre pares, grupos de estudio 
                        y recursos académicos.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-violet-100 text-violet-700 rounded-full text-xs font-semibold">📖 Estudio</span>
                        <span class="px-3 py-1 bg-purple-100 text-purple-700 rounded-full text-xs font-semibold">🌟 Sirley</span>
                    </div>
                </div>

                <!-- Proposal 9: Visual Campaign -->
                <div class="proposal-card shadow-xl">
                    <div class="proposal-icon bg-gradient-to-br from-cyan-400 to-blue-500 text-white">
                        📢
                    </div>
                    <h3 class="text-xl font-bold mb-3 text-gray-800">Campaña Visual Impactante</h3>
                    <p class="text-gray-600 mb-4 text-sm leading-relaxed">
                        <strong>Galvis</strong>, <strong>María José</strong>, <strong>Amaya</strong>, 
                        <strong>Dara Valentina</strong> y <strong>Víctor Cuadros</strong>. La mejor imagen para la mejor campaña.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-cyan-100 text-cyan-700 rounded-full text-xs font-semibold">🎨 Diseño</span>
                        <span class="px-3 py-1 bg-pink-100 text-pink-700 rounded-full text-xs font-semibold">🎨 Equipo Arte Completo</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 4: Call to Action -->
    <section class="section px-6 bg-gradient-to-br from-purple-100 via-pink-100 to-blue-100" id="vota">
        <div class="text-center max-w-4xl relative z-10">
            <div class="mb-8 float">
                <span class="text-8xl">🗳️✨</span>
            </div>
            
            <h2 class="text-5xl md:text-6xl font-black mb-6 gradient-text">
                ¡Vota por Alejandro!
            </h2>
            
            <p class="text-2xl text-gray-700 mb-8 font-medium">
                2026: Un equipo organizado, un cambio real
            </p>
            
            <div class="glass-panel rounded-3xl p-8 mb-8 max-w-2xl mx-auto bg-white/70 backdrop-blur-xl">
                <p class="text-lg text-gray-600 italic mb-4">
                    "Con un equipo así de comprometido y organizado, 
                    haremos realidad cada propuesta. ¡Juntos somos más fuertes!"
                </p>
                <div class="font-bold text-xl text-soft-purple">
                    — Alejandro y todo el equipo
                </div>
            </div>
            
            <div class="grid md:grid-cols-4 gap-4 mb-12 max-w-3xl mx-auto">
                <div class="flex flex-col items-center gap-2 p-4 rounded-2xl bg-white shadow-lg">
                    <span class="text-3xl">👑</span>
                    <span class="font-bold text-gray-700 text-sm">Liderazgo</span>
                    <span class="text-xs text-gray-500">Alejandro + Jefes</span>
                </div>
                <div class="flex flex-col items-center gap-2 p-4 rounded-2xl bg-white shadow-lg">
                    <span class="text-3xl">🎨</span>
                    <span class="font-bold text-gray-700 text-sm">Arte</span>
                    <span class="text-xs text-gray-500">Equipo Diseño</span>
                </div>
                <div class="flex flex-col items-center gap-2 p-4 rounded-2xl bg-white shadow-lg">
                    <span class="text-3xl">⚙️</span>
                    <span class="font-bold text-gray-700 text-sm">Logística</span>
                    <span class="text-xs text-gray-500">Operaciones</span>
                </div>
                <div class="flex flex-col items-center gap-2 p-4 rounded-2xl bg-white shadow-lg">
                    <span class="text-3xl">📱</span>
                    <span class="font-bold text-gray-700 text-sm">Redes</span>
                    <span class="text-xs text-gray-500">Liceth</span>
                </div>
            </div>
            
            <button class="btn-magic text-xl px-12 py-4" onclick="celebrate()">
                ¡Yo voto por el equipo de Alejandro! 💖
            </button>
            
            <div class="mt-8 text-gray-500 text-sm space-y-1">
                <p><strong>Estructura de Campaña:</strong></p>
                <p>👑 Personero: Alejandro | 🌟 Jefes: Sirley, Galvis, María José</p>
                <p>🎨 Diseño: Galvis, María José, Amaya, Dara Valentina, Víctor Cuadros</p>
                <p>⚙️ Logística: Yeili, Camilo, Diego, David | 📱 Redes: Liceth</p>
            </div>
        </div>
    </section>

    <!-- Navigation -->
    <div class="fixed right-6 top-1/2 transform -translate-y-1/2 flex flex-col gap-3 z-50">
        <div class="nav-dot active" onclick="scrollToSection('hero')" title="Inicio"></div>
        <div class="nav-dot" onclick="scrollToSection('equipos')" title="Equipos"></div>
        <div class="nav-dot" onclick="scrollToSection('propuestas')" title="Propuestas"></div>
        <div class="nav-dot" onclick="scrollToSection('vota')" title="Vota"></div>
    </div>

    <script>
        // Smooth scroll
        function scrollToSection(id) {
            document.getElementById(id).scrollIntoView({ behavior: 'smooth' });
            updateNavDots(id);
        }
        
        function updateNavDots(activeId) {
            const dots = document.querySelectorAll('.nav-dot');
            const sections = ['hero', 'equipos', 'propuestas', 'vota'];
            const index = sections.indexOf(activeId);
            dots.forEach((dot, i) => {
                dot.classList.toggle('active', i === index);
            });
        }
        
        // Intersection Observer for scroll
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    updateNavDots(entry.target.id);
                }
            });
        }, { threshold: 0.5 });
        
        document.querySelectorAll('.section').forEach(section => {
            observer.observe(section);
        });
        
        // Celebration effect
        function celebrate() {
            const colors = ['#ec4899', '#8b5cf6', '#3b82f6', '#10b981', '#f59e0b', '#f97316'];
            for (let i = 0; i < 50; i++) {
                setTimeout(() => {
                    const confetti = document.createElement('div');
                    confetti.className = 'confetti';
                    confetti.style.left = Math.random() * 100 + 'vw';
                    confetti.style.background = colors[Math.floor(Math.random() * colors.length)];
                    confetti.style.borderRadius = Math.random() > 0.5 ? '50%' : '0';
                    document.body.appendChild(confetti);
                    setTimeout(() => confetti.remove(), 3000);
                }, i * 30);
            }
            
            for (let i = 0; i < 15; i++) {
                setTimeout(() => {
                    const heart = document.createElement('div');
                    heart.className = 'heart';
                    heart.innerHTML = ['💖', '💙', '💛', '💜', '💚'][Math.floor(Math.random() * 5)];
                    heart.style.left = (Math.random() * window.innerWidth) + 'px';
                    heart.style.top = window.innerHeight + 'px';
                    document.body.appendChild(heart);
                    setTimeout(() => heart.remove(), 4000);
                }, i * 150);
            }
        }
        
        // Three.js Background Particles
        const scene = new THREE.Scene();
        const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
        const renderer = new THREE.WebGLRenderer({ alpha: true, antialias: true });
        renderer.setSize(window.innerWidth, window.innerHeight);
        document.getElementById('canvas-container').appendChild(renderer.domElement);
        
        const particlesGeometry = new THREE.BufferGeometry();
        const particlesCount = 100;
        const posArray = new Float32Array(particlesCount * 3);
        
        for(let i = 0; i < particlesCount * 3; i++) {
            posArray[i] = (Math.random() - 0.5) * 10;
        }
        
        particlesGeometry.setAttribute('position', new THREE.BufferAttribute(posArray, 3));
        
        const particlesMaterial = new THREE.PointsMaterial({
            size: 0.02,
            color: 0x8b5cf6,
            transparent: true,
            opacity: 0.6
        });
        
        const particlesMesh = new THREE.Points(particlesGeometry, particlesMaterial);
        scene.add(particlesMesh);
        
        camera.position.z = 3;
        
        let mouseX = 0;
        let mouseY = 0;
        
        document.addEventListener('mousemove', (event) => {
            mouseX = (event.clientX / window.innerWidth) * 2 - 1;
            mouseY = -(event.clientY / window.innerHeight) * 2 + 1;
        });
        
        function animate() {
            requestAnimationFrame(animate);
            
            particlesMesh.rotation.x += 0.001;
            particlesMesh.rotation.y += 0.001;
            
            particlesMesh.rotation.x += mouseY * 0.01;
            particlesMesh.rotation.y += mouseX * 0.01;
            
            renderer.render(scene, camera);
        }
        
        animate();
        
        window.addEventListener('resize', () => {
            camera.aspect = window.innerWidth / window.innerHeight;
            camera.updateProjectionMatrix();
            renderer.setSize(window.innerWidth, window.innerHeight);
        });
    </script>
</body>
</html>
