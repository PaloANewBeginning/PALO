<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Palo Store Android</title>
    <!-- Cargando Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Fuente Inter para un aspecto moderno -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #fafafa;
        }
        
        /* Animaciones suaves */
        .fade-in {
            animation: fadeIn 0.8s ease-out forwards;
            opacity: 0;
            transform: translateY(20px);
        }
        
        .delay-1 { animation-delay: 0.2s; }
        .delay-2 { animation-delay: 0.4s; }
        
        @keyframes fadeIn {
            to { opacity: 1; transform: translateY(0); }
        }

        /* Ocultar scrollbar en elementos horizontales */
        .no-scrollbar::-webkit-scrollbar {
            display: none;
        }
        .no-scrollbar {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }
    </style>
</head>
<body class="text-gray-800 antialiased selection:bg-gray-200 selection:text-black">

    <nav class="bg-white/90 backdrop-blur-md fixed w-full z-50 border-b border-gray-100 transition-all duration-300">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <!-- Logo -->
                <div class="flex-shrink-0 flex items-center gap-2">
                    <svg class="w-8 h-8 text-black" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M17.6 9.48l1.84-3.18c.16-.31.04-.69-.26-.85-.29-.15-.65-.06-.83.22l-1.88 3.24c-2.86-1.21-6.08-1.21-8.94 0L5.65 5.67c-.19-.28-.56-.38-.85-.22-.31.16-.42.54-.26.85l1.84 3.18C2.73 11.61.5 15.65.5 20h23c0-4.35-2.23-8.39-5.9-10.52zM8.1 17.04c-.66 0-1.2-.54-1.2-1.2s.54-1.2 1.2-1.2 1.2.54 1.2 1.2-.54 1.2-1.2 1.2zm7.8 0c-.66 0-1.2-.54-1.2-1.2s.54-1.2 1.2-1.2 1.2.54 1.2 1.2-.54 1.2-1.2 1.2z"/>
                    </svg>
                    <a href="#" class="text-2xl font-bold tracking-tighter text-black">Palo A New Beginning</a>
                </div>
                
                <!-- Menú de Escritorio -->
                <div class="hidden md:flex space-x-8 items-center">
                    <a href="#inicio" class="text-gray-500 hover:text-black transition-colors px-3 py-2 text-sm font-medium">Inicio</a>
                    <a href="#juegos" class="text-gray-500 hover:text-black transition-colors px-3 py-2 text-sm font-medium">Catálogo</a>
                    <a href="https://www.mediafire.com/file/s6wae73ng8gyurq/Palo_Store.apk/file" target="_blank" class="bg-black text-white px-5 py-2.5 rounded-full text-sm font-medium hover:bg-gray-800 transition-colors shadow-sm">Descargar App</a>
                </div>

                <!-- Botón Menú Móvil -->
                <div class="md:hidden flex items-center">
                    <button id="mobile-menu-btn" class="text-gray-500 hover:text-black focus:outline-none p-2">
                        <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                        </svg>
                    </button>
                </div>
            </div>
        </div>

        <!-- Menú Móvil (Oculto por defecto) -->
        <div id="mobile-menu" class="hidden md:hidden bg-white border-b border-gray-100 absolute w-full shadow-lg">
            <div class="px-4 pt-2 pb-6 space-y-2 flex flex-col items-center">
                <a href="#inicio" class="block text-gray-600 hover:text-black py-3 text-base font-medium w-full text-center border-b border-gray-50">Inicio</a>
                <a href="#juegos" class="block text-gray-600 hover:text-black py-3 text-base font-medium w-full text-center border-b border-gray-50">Catálogo</a>
                <a href="https://www.mediafire.com/file/s6wae73ng8gyurq/Palo_Store.apk/file" target="_blank" class="block bg-black text-white px-5 py-3 rounded-full text-base font-medium hover:bg-gray-800 mt-4 w-3/4 text-center">Descargar App</a>
            </div>
        </div>
    </nav>

    <!-- Sección Hero -->
    <main id="inicio" class="pt-32 pb-16 sm:pt-40 sm:pb-24 overflow-hidden bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative">
            <div class="text-center max-w-4xl mx-auto fade-in">
                <span class="text-xs font-bold tracking-widest text-gray-400 uppercase mb-4 block">Juegos y Ports para Android</span>
                <h1 class="text-5xl sm:text-6xl md:text-7xl font-extrabold text-black tracking-tight mb-8 leading-[1.1]">
                    Tu tienda favorita, <br>
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-gray-500 to-black">ahora en tu bolsillo.</span>
                </h1>
                <p class="mt-4 max-w-2xl mx-auto text-lg sm:text-xl text-gray-500 mb-10 font-light">
                    Descarga Palo A New Beginning para encontrar los mejores juegos para Android, incluyendo clásicos y las últimas novedades.
                </p>
                <div class="flex flex-col sm:flex-row justify-center gap-4">
                    <a href="https://www.mediafire.com/file/s6wae73ng8gyurq/Palo_Store.apk/file" target="_blank" class="bg-black text-white px-8 py-4 rounded-full text-lg font-medium hover:bg-gray-800 hover:-translate-y-1 transition-all duration-300 shadow-lg shadow-black/20 flex items-center justify-center gap-2">
                        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4"></path></svg>
                        APK Oficial
                    </a>
                    <a href="#juegos" class="bg-white text-black border-2 border-gray-200 px-8 py-4 rounded-full text-lg font-medium hover:bg-gray-50 hover:border-black transition-all duration-300">
                        Ver Catálogo
                    </a>
                </div>
            </div>
        </div>
    </main>

    <!-- Sección de Juegos (Grid y Buscador) -->
    <section id="juegos" class="py-24 bg-[#fafafa] min-h-screen">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row justify-between items-start md:items-end mb-12 gap-6">
                <div>
                    <h2 class="text-3xl font-bold text-black tracking-tight">Catálogo de Juegos</h2>
                    <p class="text-gray-500 mt-2">Explora y descarga cientos de juegos para tu Android.</p>
                </div>
                
                <!-- Buscador -->
                <div class="w-full md:w-96 relative">
                    <input type="text" id="buscador" placeholder="Buscar juego..." class="w-full bg-white border border-gray-200 text-gray-900 text-sm rounded-xl focus:ring-black focus:border-black block px-4 py-3 pl-10 transition-colors shadow-sm">
                    <svg class="w-5 h-5 text-gray-400 absolute left-3 top-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path></svg>
                </div>
            </div>

            <!-- Contenedor donde se insertarán los juegos por JavaScript -->
            <div id="grid-juegos" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6">
                <!-- Los juegos se inyectan aquí automáticamente -->
            </div>
            
            <!-- Mensaje cuando no hay resultados en el buscador -->
            <div id="no-resultados" class="hidden text-center py-20">
                <svg class="w-16 h-16 text-gray-300 mx-auto mb-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M9.172 16.172a4 4 0 015.656 0M9 10h.01M15 10h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                <h3 class="text-xl font-bold text-gray-900 mb-1">No se encontraron juegos</h3>
                <p class="text-gray-500">Intenta con otro término de búsqueda.</p>
            </div>
        </div>
    </section>

    <!-- Por qué elegirnos -->
    <section class="py-24 bg-white border-y border-gray-100">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-black tracking-tight">¿Por qué usar Palo Store?</h2>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-10">
                <div class="text-center">
                    <div class="w-16 h-16 mx-auto bg-gray-50 rounded-full flex items-center justify-center mb-6">
                        <svg class="w-8 h-8 text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path></svg>
                    </div>
                    <h3 class="text-xl font-bold text-black mb-3">Seguro</h3>
                    <p class="text-gray-500 font-light">Juegos para tu dispositivo.</p>
                </div>
                <div class="text-center">
                    <div class="w-16 h-16 mx-auto bg-gray-50 rounded-full flex items-center justify-center mb-6">
                        <svg class="w-8 h-8 text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
                    </div>
                    <h3 class="text-xl font-bold text-black mb-3">Enlaces Directos</h3>
                    <p class="text-gray-500 font-light">Descargas rápidas por MediaFire.</p>
                </div>
                <div class="text-center">
                    <div class="w-16 h-16 mx-auto bg-gray-50 rounded-full flex items-center justify-center mb-6">
                        <svg class="w-8 h-8 text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M4 4v5h.582m15.356 2A8.001 8.001 0 004.582 9m0 0H9m11 11v-5h-.581m0 0a8.003 8.003 0 01-15.357-2m15.357 2H15"></path></svg>
                    </div>
                    <h3 class="text-xl font-bold text-black mb-3">Actualizado</h3>
                    <p class="text-gray-500 font-light">Siempre buscamos traer las últimas versiones.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-white py-12 border-t border-gray-100">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-6 md:mb-0 text-center md:text-left">
                    <span class="text-xl font-bold tracking-tighter text-black flex items-center justify-center md:justify-start gap-2">
                        Palo A New Beginning
                    </span>
                    <p class="text-gray-400 text-sm mt-2">© 2026 Palo A New Beginning Android.</p>
                </div>
            </div>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            // Lógica Menú Móvil
            const btn = document.getElementById('mobile-menu-btn');
            const menu = document.getElementById('mobile-menu');

            if(btn && menu) {
                btn.addEventListener('click', () => {
                    menu.classList.toggle('hidden');
                });

                const links = menu.querySelectorAll('a');
                links.forEach(link => {
                    link.addEventListener('click', () => {
                        menu.classList.add('hidden');
                    });
                });
            }

            // --- BASE DE DATOS DE JUEGOS ---
            const todosLosJuegos = [
                {
                    nombre: "Cruel",
                    categoria: "FPS",
                    imagen: "https://i.ytimg.com/vi/CcoY0MdsT8c/hqdefault.jpg",
                    enlace: "https://www.mediafire.com/file/vwmxf5jthoimibx/Cruel_v1.0.0.apk/file",
                    descripcion: "CRUEL te lanza a un mundo retorcido. Desorientado y atrapado en un hotel extraño, encuentras un cuerpo sin vida."
                }, // <-- La coma vital

                 
                {
                    nombre: "Minecraft Dungeons",
                    categoria: "Acción",
                    imagen: "https://store-images.s-microsoft.com/image/apps.2957.14045794648370014.2229d39b-90c3-496e-8fac-9987450ca4d8.680871e0-da2a-4109-8e2c-4bc75b2d56f8",
                    enlace: "https://www.mediafire.com/file/vsanm78cxfmy31s/MD.apk/file",
                    descripcion: "Minecraft Dungeons es un juego de acción y exploración de mazmorras para hasta 4 jugadores, ambientado en el universo de Minecraft."
                }, // <-- La coma vital

                {
                    nombre: "Slient Hill",
                    categoria: "Terror",
                    imagen: "https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEheYQmIyWCJq2XHWmm8aa0nPd75EbxRse-iMa8paTITbtPoo8_u4-hfvLke7uxcbVrQ-lzqz7rxy7eVXIA7bNnv88yaqVncMRuSBxWyHaFO1gk5cFuxNYA2UbTdjRJ0yii8u1pqFRl-UZwxNhofe0jMZPPsxj1UV67nc4hpMuB8lEf52_ON_L7hEgoGsWw/s320/SH1Boxart.webp",
                    enlace: "https://www.mediafire.com/file/yigo6k3ry4c75mk/Silent_Hill_Android.zip/file",
                    descripcion: "Silent Hill (1999) es un videojuego de terror psicológico y survival horror desarrollado por Team Silent y publicado por Konami para la PlayStation original"
                }, // <-- La coma vital

                {
                    nombre: "FIFA 14",
                    categoria: "Fútbol",
                    imagen: "https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhNOL2z_-7VCsjS6BQatBLnu5ErL-lR5ZWZKT9sDC3YC72INbE4t9hmvcJxHb-1aGkBO9NO_gkbUk0jQWH2KnJHvCaJElpTh3Jq0xRKrQj9sFO9XNYDMVQiOkrAb_NmAG5cen-8c5w93juhyphenhyphen6OtSH_7NngkZMV-CmoCMcNznvLKgM55mHVCuUMOer9lgqg/w200-h200/OIP-3848931708.jpg",
                    enlace: "https://drive.google.com/file/d/1Z8aChxAsKPHMyOzFTox9CptMkpiulU40/view?pli=1",
                    descripcion: "incluía más de 30 ligas oficiales, más de 600 equipos con licencia y más de 16.000 jugadores con nombres reales, entre ellas la Premier League, La Liga y la Bundesliga."
                }, // <-- La coma vital


                {
                    nombre: "CloverPit",
                    categoria: "Horror",
                    imagen: "https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgeKBAhYknROwE56g9AP_TN8XxeVrUuAVfHIHqYlUazcdFTGCOIwW0fGPIICnlf_g-xrPHfijWWIPnlvpmhauhW8nfJdIzGv4gMnHYrX5nOo0b7693YuT9MtrxETgx3_JEdduEKTghiXGrUnrwYKgjFU38_7e_o-cbOuP-n4NI9OUrLVXpJmZ0_8fI_Auw/s320/images.jpeg",
                    enlace: "https://www.mediafire.com/file/39npj0erxhl1uo6/CloverPit_By_Palo_Store.apk/file",
                    descripcion: "CloverPit es un juego de realidad alternativa (ARG) y una experiencia de horror analógico alojada principalmente en un sitio web que simula ser un portal de juegos retro o un foro de nicho de los años 90 y principios de los 2000."
                }, // <-- La coma vital


                {
                    nombre: "Ultrakill",
                    categoria: "FPS",
                    imagen: "https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhDucJrVwXD3EwwKtmMy_ehHwzy_hlwkFAxzIOGzUgaY0B9PRlE1f2UmNo00eqAIlqGxcr-E_sKdRtLq1M5DQRZfVNxGoaEVLoInrnqWgzpl08ixjY6yhUWwhD6geQlKt5HDWSaBYlMHHC96gb7uAl9-5vrVZLt3rVPSRBSiF6MaXwpSO1eD4Y6bJRAdEc/s320/MV5BNjdmNDU5ZTEtOTVlNS00MWRkLTljMTktZjA5YjA5OWI4MmFjXkEyXkFqcGc@._V1_.jpg",
                    enlace: "https://www.mediafire.com/file/43hxxai0swx0irz/ULTRAKILL.apk/file",
                    descripcion: "ULTRAKILL es un videojuego de disparos en primera persona (FPS) ultraviolento y de ritmo rapidísimo, que evoca la estética y jugabilidad."
                }, // <-- La coma vital

                {
                    nombre: "Celeste",
                    categoria: "Plataformas",
                    imagen: "https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjwlgm5AFUVedHq8vfIGcr6Vr5C-5FBOavHXEU8lutUPy-7pFlR4SkU7b1fhL31MVPUvOpfr9Jq2QUPKRGRevAiSJjU9Mo5E_ZKnc-6v-dFVxN7KR3NmLWRvE6OmzGd0ySQnaJlAKTy8BXR2PXxG_k8pwhPjlTrdRzJDjSNJ6ENlfe0meQvtbdFEtAoykg/s320/691ba3e0801180a9864cc8a7694b6f98097f9d9799bc7e3dc6db92f086759252.jpeg",
                    enlace: "https://www.mediafire.com/file/wg55glm0if7gpcj/Celeste_-_PaloStore.apk/file",
                    descripcion: "Celeste es un aclamado videojuego de plataformas independiente que combina un gameplay exigente con una historia muy emotiva y personal."
                }, // <-- La coma vital

                {
                    nombre: "Gambonanza",
                    categoria: "Estrategia",
                    imagen: "https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgId0KwVrRCipmHS-aFdQA0zgK6pt7C48S8z85BEnHaKddrenCSHl1LrkWjXoaMr3XjJotk-FMEB_lT7-ClH25nNG9cLiix44sMwLAn3BcwoIXOH_VrDbSeUTX9FHKycR5dQELVu0QQqbOS5AUjYMRPLuduTOxGP-t49Kc0c_BD0akOzXmEEyedGD4LagA/s320/capsule_616x353%20(1).jpg",
                    enlace: "https://www.mediafire.com/file/270jm1wdtob4ek1/Gambonanza.apk/file",
                    descripcion: "Es un juego que toma las reglas del ajedrez y las transforma en una experiencia arcade o de rompecabezas más dinámica."
                }, // <-- La coma vital

                {
                    nombre: "Dead Cells",
                    categoria: "Accion",
                    imagen: "https://assets1.ignimgs.com/2019/06/10/dead-cells---button-fin-1560125633132.jpg?fit=bounds&dpr=1&quality=75&width=188px",
                    enlace: "https://www.mediafire.com/file/76qtmofe3tgpy5i/Dead_Cells_Palo_Store.apk/file",
                    descripcion: "Dead Cells es un aclamado videojuego que fusiona dos géneros muy populares: roguelike (si mueres, pierdes tu progreso de esa partida"
                }, // <-- La coma vital

                {
                    nombre: "The Amazing Spider-man 2",
                    categoria: "Accion",
                    imagen: "https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj5NZ8ngssa8dyEUTHaFf_Ijd30tqixhdYXGrV21Q9PqUlEX4X1xEV4Vog8AJu3jZ4Hb0E6P2Ru5ueCLFK4iqAqS06iZZ_bjmKnl2XnEe58pLzfNb1ycJt9lEHk_-jwip-n90VeKmOcNWyQ1KLufU8im-wsKPAXLxvWnOOnzwQ3zjCtAM-BykEnC4tZ-tM/s320/p9957538_v_h8_ab-493056462.jpg",
                    enlace: "https://www.mediafire.com/file/er1f1i6mcgx71g0/Spider_Man_2.rar/file",
                    descripcion: "Una recreación bastante amplia de Manhattan dividida en 6 distritos detallados (desde Times Square hasta Central Park) con gráficos que, para su época, eran de nivel de consola portátil",
                }, // <-- La coma vital

                {
                    nombre: "Carrion",
                    categoria: "Horror",
                    imagen: "https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiEcHIBZTJRRHydaS3rGkVt9ak178ieO4q-Vv4xw76-lynWrUQ7inOP2aUXk0BW1IWJ8xF2nKZGYtJtmgCuZpaaCIfQAN4K8JfGJlNcdiwJE35gNs_MiZjt6jSJBYAF4bOTmU1vMMmnvmtkyRVtYc785B4w_H8Y3N_ay6Yyr_Tw34aoZbsI_gMfzeag1ZU/s320/maxresdefault.jpg",
                    enlace: "https://www.mediafire.com/file/lp6u2xm22u8z20s/Carrion.apk/file",
                    descripcion: "El diseño del juego sigue la estructura de un Metroidvania (un mapa interconectado que requiere nuevas habilidades para desbloquear caminos), pero centrado en el movimiento fluido y la destrucción:",
                }, // <-- La coma vital





                // PEGA TU SIGUIENTE JUEGO AQUÍ ABAJO (Recuerda poner las llaves { } )
                
            ];

            // Elementos del DOM
            const gridJuegos = document.getElementById('grid-juegos');
            const buscadorInput = document.getElementById('buscador');
            const mensajeNoResultados = document.getElementById('no-resultados');

            // Función para renderizar los juegos en pantalla
            function renderizarJuegos(juegosParaMostrar) {
                if(!gridJuegos) return; 
                
                gridJuegos.innerHTML = ''; 

                if (juegosParaMostrar.length === 0) {
                    if(mensajeNoResultados) mensajeNoResultados.classList.remove('hidden');
                } else {
                    if(mensajeNoResultados) mensajeNoResultados.classList.add('hidden');
                    
                    juegosParaMostrar.forEach(juego => {
                        const card = document.createElement('div');
                        card.className = "bg-white rounded-2xl p-5 shadow-sm border border-gray-100 hover:shadow-xl hover:-translate-y-1 transition-all duration-300 group flex flex-col justify-between h-full fade-in";
                        
                        card.innerHTML = `
                            <div>
                                <div class="flex items-center gap-4 mb-4">
                                    <div class="w-16 h-16 rounded-xl overflow-hidden shadow-sm group-hover:scale-105 transition-transform shrink-0">
                                        <img src="${juego.imagen}" alt="${juego.nombre}" class="w-full h-full object-cover" loading="lazy">
                                    </div>
                                    <div>
                                        <h3 class="font-bold text-black text-lg leading-tight line-clamp-2">${juego.nombre}</h3>
                                        <span class="text-[10px] uppercase tracking-wider text-gray-500 font-bold bg-gray-50 px-2 py-1 rounded mt-1 inline-block">${juego.categoria}</span>
                                    </div>
                                </div>
                                <p class="text-xs text-gray-500 mb-5 line-clamp-3">${juego.descripcion}</p>
                            </div>
                            <a href="${juego.enlace}" target="_blank" rel="noopener noreferrer" class="block text-center w-full bg-black text-white text-sm font-semibold py-2.5 rounded-lg hover:bg-gray-800 transition-colors shadow-sm">
                                Descargar
                            </a>
                        `;
                        gridJuegos.appendChild(card);
                    });
                }
            }

            // Renderizar la lista inicial
            renderizarJuegos(todosLosJuegos);

            // Evento para el buscador
            if(buscadorInput) {
                buscadorInput.addEventListener('input', (e) => {
                    const termino = e.target.value.toLowerCase().trim();
                    
                    if (termino === '') {
                        renderizarJuegos(todosLosJuegos);
                        return;
                    }

                    const filtrados = todosLosJuegos.filter(juego => {
                        return juego.nombre.toLowerCase().includes(termino) || 
                               juego.categoria.toLowerCase().includes(termino) ||
                               juego.descripcion.toLowerCase().includes(termino);
                    });

                    renderizarJuegos(filtrados);
                });
            }
        });
    </script>
</body>
</html>
