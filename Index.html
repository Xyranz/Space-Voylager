<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Space Voyager - Game Luar Angkasa Seru</title>
    <!-- Tailwind CSS untuk Styling Modern -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Lucide Icons untuk Ikon Indah -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        /* Mencegah scroll default dan seleksi teks pada perangkat mobile */
        body {
            touch-action: none;
            -webkit-user-select: none;
            user-select: none;
            background-color: #0b0f19;
        }
        canvas {
            display: block;
            background: radial-gradient(circle, #1a1c2e 0%, #0b0f19 100%);
        }
    </style>
</head>
<body class="overflow-hidden h-screen w-screen flex flex-col justify-between font-sans text-white">

    <!-- Header / Navigasi Atas -->
    <header class="p-4 flex justify-between items-center bg-gray-900/80 backdrop-blur-md border-b border-gray-800 z-10 w-full">
        <div class="flex items-center space-x-2">
            <i data-lucide="rocket" class="w-8 h-8 text-indigo-500 animate-pulse"></i>
            <span class="text-xl font-black tracking-wider bg-clip-text text-transparent bg-gradient-to-r from-indigo-400 to-cyan-400">
                SPACE VOYAGER
            </span>
        </div>
        <div class="flex items-center space-x-6">
            <div class="text-center">
                <p class="text-xs text-gray-400 uppercase tracking-widest font-semibold">Skor</p>
                <p id="score-display" class="text-xl font-bold text-yellow-400">0</p>
            </div>
            <div class="text-center">
                <p class="text-xs text-gray-400 uppercase tracking-widest font-semibold">Tertinggi</p>
                <p id="high-score-display" class="text-xl font-bold text-cyan-400">0</p>
            </div>
            <button id="sound-toggle" class="p-2 rounded-full bg-gray-800 hover:bg-gray-700 transition">
                <i data-lucide="volume-2" id="sound-icon" class="w-5 h-5 text-gray-300"></i>
            </button>
        </div>
    </header>

    <!-- Area Utama Game -->
    <main class="relative flex-grow flex items-center justify-center w-full h-full overflow-hidden">
        <!-- Canvas Game -->
        <canvas id="gameCanvas" class="w-full h-full object-contain"></canvas>

        <!-- Layar Mulai / Start Screen Overlay -->
        <div id="start-screen" class="absolute inset-0 bg-black/85 flex flex-col items-center justify-center z-20 px-6 text-center">
            <div class="max-w-md bg-gray-900/90 border border-gray-800 p-8 rounded-2xl shadow-2xl backdrop-blur-lg">
                <i data-lucide="shield-alert" class="w-16 h-16 text-indigo-500 mx-auto mb-4 animate-bounce"></i>
                <h1 class="text-3xl font-extrabold mb-2 bg-clip-text text-transparent bg-gradient-to-r from-indigo-400 to-cyan-400">
                    Misi Penyelamatan
                </h1>
                <p class="text-gray-400 text-sm mb-6">
                    Kendalikan pesawat luar angkasa Anda melewati hujan asteroid yang mematikan. Kumpulkan kristal energi untuk mendapatkan poin ekstra!
                </p>
                
                <!-- Petunjuk Kontrol -->
                <div class="grid grid-cols-2 gap-4 text-xs text-left text-gray-300 mb-8 border-t border-b border-gray-800 py-4">
                    <div>
                        <p class="font-bold text-indigo-400 mb-1 flex items-center">
                            <i data-lucide="monitor" class="w-4 h-4 mr-1"></i> PC / Laptop
                        </p>
                        <p>Tombol <kbd class="px-1.5 py-0.5 bg-gray-800 border border-gray-700 rounded text-yellow-400 font-mono">A</kbd> / <kbd class="px-1.5 py-0.5 bg-gray-800 border border-gray-700 rounded text-yellow-400 font-mono">D</kbd> atau Panah Kiri/Kanan untuk berbelok.</p>
                    </div>
                    <div>
                        <p class="font-bold text-indigo-400 mb-1 flex items-center">
                            <i data-lucide="smartphone" class="w-4 h-4 mr-1"></i> HP / Android
                        </p>
                        <p>Ketuk tombol sentuh di bagian bawah layar untuk bermanuver.</p>
                    </div>
                </div>

                <button id="start-btn" class="w-full py-4 bg-gradient-to-r from-indigo-600 to-cyan-600 hover:from-indigo-500 hover:to-cyan-500 font-bold rounded-xl shadow-lg shadow-indigo-500/30 transition transform active:scale-95 text-lg">
                    MULAI JELAJAH
                </button>
            </div>
        </div>

        <!-- Layar Game Over / Game Over Screen Overlay (Hidden by Default) -->
        <div id="game-over-screen" class="absolute inset-0 bg-black/90 flex flex-col items-center justify-center z-20 px-6 text-center hidden">
            <div class="max-w-md bg-gray-900/95 border border-red-900/50 p-8 rounded-2xl shadow-2xl backdrop-blur-lg">
                <div class="w-16 h-16 bg-red-950/50 border border-red-500/30 rounded-full flex items-center justify-center mx-auto mb-4">
                    <i data-lucide="skull" class="w-8 h-8 text-red-500 animate-pulse"></i>
                </div>
                <h2 class="text-3xl font-extrabold text-red-500 mb-1">PESAWAT HANCUR!</h2>
                <p class="text-gray-400 text-sm mb-6">Anda menabrak asteroid di luar angkasa.</p>
                
                <div class="bg-gray-800/50 rounded-xl p-4 mb-6 flex justify-around border border-gray-700">
                    <div>
                        <p class="text-xs text-gray-400">Skor Akhir</p>
                        <p id="final-score" class="text-2xl font-bold text-yellow-400">0</p>
                    </div>
                    <div class="border-r border-gray-700 h-10 my-auto"></div>
                    <div>
                        <p class="text-xs text-gray-400">Skor Terbaik</p>
                        <p id="final-high-score" class="text-2xl font-bold text-cyan-400">0</p>
                    </div>
                </div>

                <button id="restart-btn" class="w-full py-4 bg-gradient-to-r from-emerald-600 to-teal-600 hover:from-emerald-500 hover:to-teal-500 font-bold rounded-xl shadow-lg shadow-emerald-500/30 transition transform active:scale-95 text-lg flex items-center justify-center space-x-2">
                    <i data-lucide="rotate-ccw" class="w-5 h-5"></i>
                    <span>MAIN LAGI</span>
                </button>
            </div>
        </div>
    </main>

    <!-- Kontrol Sentuh Khusus HP / Android -->
    <div id="touch-controls" class="w-full bg-gray-950 border-t border-gray-900 p-4 pb-6 flex justify-around items-center select-none z-10 md:hidden">
        <button id="btn-left" class="w-24 h-24 bg-gray-800/80 active:bg-indigo-600/80 border border-gray-700 rounded-2xl flex items-center justify-center transition active:scale-90 shadow-lg text-white">
            <i data-lucide="chevron-left" class="w-12 h-12"></i>
        </button>
        <button id="btn-right" class="w-24 h-24 bg-gray-800/80 active:bg-indigo-600/80 border border-gray-700 rounded-2xl flex items-center justify-center transition active:scale-90 shadow-lg text-white">
            <i data-lucide="chevron-right" class="w-12 h-12"></i>
        </button>
    </div>

    <!-- Script Logika Game -->
    <script>
        // Inisialisasi Ikon Lucide
        lucide.createIcons();

        // Elemen DOM
        const canvas = document.getElementById('gameCanvas');
        const ctx = canvas.getContext('2d');
        const startScreen = document.getElementById('start-screen');
        const gameOverScreen = document.getElementById('game-over-screen');
        const startBtn = document.getElementById('start-btn');
        const restartBtn = document.getElementById('restart-btn');
        const scoreDisplay = document.getElementById('score-display');
        const highScoreDisplay = document.getElementById('high-score-display');
        const finalScore = document.getElementById('final-score');
        const finalHighScore = document.getElementById('final-high-score');
        const soundToggle = document.getElementById('sound-toggle');
        const soundIcon = document.getElementById('sound-icon');
        const btnLeft = document.getElementById('btn-left');
        const btnRight = document.getElementById('btn-right');

        // Pengaturan Sistem Suara Sintetis (Web Audio API)
        let isMuted = false;
        const audioCtx = new (window.AudioContext || window.webkitAudioContext)();

        function playSound(freq, type, duration) {
            if (isMuted) return;
            try {
                const osc = audioCtx.createOscillator();
                const gain = audioCtx.createGain();
                osc.connect(gain);
                gain.connect(audioCtx.destination);
                
                osc.type = type;
                osc.frequency.setValueAtTime(freq, audioCtx.currentTime);
                
                gain.gain.setValueAtTime(0.1, audioCtx.currentTime);
                gain.gain.exponentialRampToValueAtTime(0.00001, audioCtx.currentTime + duration);
                
                osc.start();
                osc.stop(audioCtx.currentTime + duration);
            } catch (e) {
                console.log("Error playing audio: ", e);
            }
        }

        soundToggle.addEventListener('click', () => {
            isMuted = !isMuted;
            if (isMuted) {
                soundIcon.setAttribute('data-lucide', 'volume-x');
            } else {
                soundIcon.setAttribute('data-lucide', 'volume-2');
                playSound(600, 'sine', 0.1);
            }
            lucide.createIcons();
        });

        // Pengaturan Canvas Adaptif
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
        }
        window.addEventListener('resize', resizeCanvas);
        resizeCanvas();

        // State Utama Game
        let gameRunning = false;
        let score = 0;
        let highScore = parseInt(localStorage.getItem('space_high_score') || '0');
        highScoreDisplay.textContent = highScore;

        // Kontrol State
        let keys = {};
        let touchLeft = false;
        let touchRight = false;

        // Event Listener Keyboard (PC)
        window.addEventListener('keydown', (e) => {
            keys[e.code] = true;
        });
        window.addEventListener('keyup', (e) => {
            keys[e.code] = false;
        });

        // Event Listener Touch (Android)
        btnLeft.addEventListener('touchstart', (e) => { e.preventDefault(); touchLeft = true; });
        btnLeft.addEventListener('touchend', (e) => { e.preventDefault(); touchLeft = false; });
        btnRight.addEventListener('touchstart', (e) => { e.preventDefault(); touchRight = true; });
        btnRight.addEventListener('touchend', (e) => { e.preventDefault(); touchRight = false; });

        // Komponen Entitas Game
        let player = {
            x: 0,
            y: 0,
            width: 40,
            height: 40,
            speed: 8,
            angle: 0
        };

        let stars = [];
        let obstacles = [];
        let crystals = [];
        let particles = [];
        let speedMultiplier = 1;

        // Reset & Inisialisasi Game
        function initGame() {
            score = 0;
            speedMultiplier = 1;
            scoreDisplay.textContent = score;
            obstacles = [];
            crystals = [];
            particles = [];
            
            // Atur posisi awal pesawat di tengah bawah
            player.x = canvas.width / 2 - player.width / 2;
            player.y = canvas.height - player.height - 30;

            // Buat bintang background
            stars = [];
            for (let i = 0; i < 80; i++) {
                stars.push({
                    x: Math.random() * canvas.width,
                    y: Math.random() * canvas.height,
                    size: Math.random() * 2 + 1,
                    speed: Math.random() * 3 + 1
                });
            }
        }

        // Fungsi membuat partikel efek tabrakan/kristal
        function createExplosion(x, y, color, count = 10) {
            for (let i = 0; i < count; i++) {
                particles.push({
                    x: x,
                    y: y,
                    vx: (Math.random() - 0.5) * 8,
                    vy: (Math.random() - 0.5) * 8,
                    radius: Math.random() * 3 + 1,
                    color: color,
                    alpha: 1,
                    decay: Math.random() * 0.03 + 0.01
                });
            }
        }

        // Loop Logika & Render Game
        function update() {
            if (!gameRunning) return;

            // 1. Logika Pergerakan Pesawat
            if (keys['KeyA'] || keys['ArrowLeft'] || touchLeft) {
                player.x -= player.speed;
                player.angle = -0.15; // Miringkan pesawat ke kiri
            } else if (keys['KeyD'] || keys['ArrowRight'] || touchRight) {
                player.x += player.speed;
                player.angle = 0.15; // Miringkan pesawat ke kanan
            } else {
                player.angle = 0;
            }

            // Batasi pesawat di dalam layar
            if (player.x < 0) player.x = 0;
            if (player.x > canvas.width - player.width) player.x = canvas.width - player.width;

            // 2. Efek Bintang Bergerak
            stars.forEach(star => {
                star.y += star.speed * speedMultiplier;
                if (star.y > canvas.height) {
                    star.y = 0;
                    star.x = Math.random() * canvas.width;
                }
            });

            // Tingkatkan tingkat kesulitan seiring waktu
            speedMultiplier += 0.0001;

            // 3. Spawn Asteroid (Obstacles) & Kristal
            if (Math.random() < 0.02 * speedMultiplier && obstacles.length < 8) {
                obstacles.push({
                    x: Math.random() * (canvas.width - 40),
                    y: -50,
                    width: Math.random() * 25 + 25,
                    height: Math.random() * 25 + 25,
                    speed: Math.random() * 4 + 3,
                    rotation: Math.random() * Math.PI * 2,
                    rotSpeed: (Math.random() - 0.5) * 0.05
                });
            }

            if (Math.random() < 0.008 && crystals.length < 3) {
                crystals.push({
                    x: Math.random() * (canvas.width - 20),
                    y: -30,
                    size: 15,
                    speed: 3
                });
            }

            // 4. Update Asteroid
            for (let i = obstacles.length - 1; i >= 0; i--) {
                let obs = obstacles[i];
                obs.y += obs.speed * speedMultiplier;
                obs.rotation += obs.rotSpeed;

                // Tabrakan dengan Pesawat Player (AABB & Circular Approximation)
                if (
                    obs.x < player.x + player.width - 5 &&
                    obs.x + obs.width > player.x + 5 &&
                    obs.y < player.y + player.height - 5 &&
                    obs.y + obs.height > player.y + 5
                ) {
                    // Game Over
                    gameRunning = false;
                    createExplosion(player.x + player.width/2, player.y + player.height/2, '#ef4444', 30);
                    createExplosion(obs.x + obs.width/2, obs.y + obs.height/2, '#a1a1aa', 15);
                    playSound(150, 'sawtooth', 0.6);
                    playSound(80, 'sine', 0.8);
                    
                    setTimeout(endGame, 1000);
                }

                // Hapus jika keluar layar
                if (obs.y > canvas.height) {
                    obstacles.splice(i, 1);
                    score += 1;
                    scoreDisplay.textContent = score;
                }
            }

            // 5. Update Kristal Energi (Bonus Skor)
            for (let i = crystals.length - 1; i >= 0; i--) {
                let cry = crystals[i];
                cry.y += cry.speed * speedMultiplier;

                // Deteksi ambil kristal
                if (
                    cry.x < player.x + player.width &&
                    cry.x + cry.size > player.x &&
                    cry.y < player.y + player.height &&
                    cry.y + cry.size > player.y
                ) {
                    crystals.splice(i, 1);
                    score += 15;
                    scoreDisplay.textContent = score;
                    createExplosion(cry.x + cry.size/2, cry.y + cry.size/2, '#22c55e', 12);
                    playSound(880, 'sine', 0.25);
                    continue;
                }

                // Hapus jika keluar layar
                if (cry.y > canvas.height) {
                    crystals.splice(i, 1);
                }
            }

            // 6. Update Partikel Efek
            for (let i = particles.length - 1; i >= 0; i--) {
                let p = particles[i];
                p.x += p.vx;
                p.y += p.vy;
                p.alpha -= p.decay;
                if (p.alpha <= 0) {
                    particles.splice(i, 1);
                }
            }
        }

        // Menggambar Semua Komponen Game di Canvas
        function draw() {
            // Bersihkan Canvas
            ctx.clearRect(0, 0, canvas.width, canvas.height);

            // 1. Gambar Bintang Latar Belakang
            ctx.fillStyle = '#ffffff';
            stars.forEach(star => {
                ctx.globalAlpha = star.speed / 4;
                ctx.beginPath();
                ctx.arc(star.x, star.y, star.size, 0, Math.PI * 2);
                ctx.fill();
            });
            ctx.globalAlpha = 1.0;

            // 2. Gambar Partikel Efek
            particles.forEach(p => {
                ctx.save();
                ctx.globalAlpha = p.alpha;
                ctx.fillStyle = p.color;
                ctx.beginPath();
                ctx.arc(p.x, p.y, p.radius, 0, Math.PI * 2);
                ctx.fill();
                ctx.restore();
            });

            // 3. Gambar Kristal Energi
            crystals.forEach(cry => {
                ctx.save();
                ctx.translate(cry.x + cry.size/2, cry.y + cry.size/2);
                ctx.fillStyle = '#22c55e';
                ctx.shadowColor = '#22c55e';
                ctx.shadowBlur = 15;
                ctx.beginPath();
                // Gambar bentuk berlian
                ctx.moveTo(0, -cry.size/2);
                ctx.lineTo(cry.size/2, 0);
                ctx.lineTo(0, cry.size/2);
                ctx.lineTo(-cry.size/2, 0);
                ctx.closePath();
                ctx.fill();
                ctx.restore();
            });

            // 4. Gambar Asteroid (Obstacles)
            obstacles.forEach(obs => {
                ctx.save();
                ctx.translate(obs.x + obs.width/2, obs.y + obs.height/2);
                ctx.rotate(obs.rotation);
                
                // Badan Asteroid dengan warna abu-abu bervariasi
                ctx.fillStyle = '#4b5563';
                ctx.strokeStyle = '#374151';
                ctx.lineWidth = 2;
                
                ctx.beginPath();
                // Gambar asteroid tidak beraturan sederhana
                ctx.moveTo(0, -obs.height/2);
                ctx.lineTo(obs.width/3, -obs.height/3);
                ctx.lineTo(obs.width/2, 0);
                ctx.lineTo(obs.width/3, obs.height/3);
                ctx.lineTo(0, obs.height/2);
                ctx.lineTo(-obs.width/3, obs.