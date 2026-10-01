<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Made for My Special One ❤️</title>
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts (Kanit & Prompt & Great Vibes) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Kanit:wght@300;400;500;600&family=Prompt:wght@300;400;500;600&display=swap" rel="stylesheet">
    
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        body {
            font-family: 'Prompt', 'Kanit', sans-serif;
            background: linear-gradient(135deg, #fff5f7 0%, #fed6e3 50%, #fecfef 100%);
            color: #5c3d46;
            overflow-x: hidden;
        }

        .font-cursive {
            font-family: 'Great Vibes', cursive;
        }

        /* Floating Hearts Background Container */
        #heart-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
            overflow: hidden;
        }

        .floating-heart {
            position: absolute;
            bottom: -50px;
            color: rgba(255, 126, 153, 0.6);
            animation: floatUp 8s linear infinite;
        }

        @keyframes floatUp {
            0% {
                transform: translateY(0) rotate(0deg) scale(0.8);
                opacity: 0.8;
            }
            100% {
                transform: translateY(-110vh) rotate(360deg) scale(1.2);
                opacity: 0;
            }
        }

        /* Glassmorphism Card Effect */
        .glass-card {
            background: rgba(255, 255, 255, 0.75);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.8);
            box-shadow: 0 10px 30px rgba(255, 182, 193, 0.3);
        }

        .glass-card-hover {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .glass-card-hover:hover {
            transform: translateY(-5px) scale(1.02);
            box-shadow: 0 15px 35px rgba(244, 114, 182, 0.4);
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #fbcfe8;
        }
        ::-webkit-scrollbar-thumb {
            background: #f472b6;
            border-radius: 10px;
        }

        /* Pulse Heart Animation */
        .pulse-heart {
            animation: pulse 1.5s infinite;
        }
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.15); }
        }

        /* Modal Animation */
        .modal-enter {
            animation: modalFadeIn 0.3s ease-out forwards;
        }
        @keyframes modalFadeIn {
            from { opacity: 0; transform: scale(0.9) translateY(20px); }
            to { opacity: 1; transform: scale(1) translateY(0); }
        }
    </style>
</head>
<body class="relative min-h-screen pb-12 selection:bg-pink-300 selection:text-pink-900">

    <div id="heart-container"></div>

    <!-- MAIN CONTAINER -->
    <div class="relative z-10 max-w-4xl mx-auto px-4 py-8 space-y-12">

        <header class="text-center space-y-4 pt-6">
            <div class="inline-block p-2 px-4 rounded-full bg-pink-100 text-pink-600 text-sm font-medium shadow-sm mb-2">
                ✨ Happy Anniversary & Special Moments ✨
            </div>
            <h1 class="text-4xl sm:text-6xl font-bold text-pink-600 tracking-tight leading-tight">
                Made For <span class="font-cursive text-5xl sm:text-7xl text-rose-500 underline decoration-pink-300">My Special One</span>
            </h1>
            <p class="text-gray-600 max-w-lg mx-auto text-sm sm:text-base">
                ขอบคุณนะที่เข้ามาเป็นเรื่องราวดีๆ และความสุขในทุกๆ วันของฉัน ❤️️
            </p>
        </header>

        <section class="glass-card rounded-3xl p-6 shadow-xl border border-pink-100 max-w-md mx-auto">
            <div class="flex items-center space-x-4">
                <div class="relative group">
                    <img id="music-cover" src="https://images.unsplash.com/photo-1518895949257-7621c3c786d7?w=300&auto=format&fit=crop&q=80" alt="Music Cover" class="w-16 h-16 rounded-2xl object-cover shadow-md group-hover:rotate-6 transition-transform duration-300">
                    <div class="absolute inset-0 bg-black/20 rounded-2xl flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity">
                        <i class="fa-solid fa-music text-white text-xs"></i>
                    </div>
                </div>
                <div class="flex-1 min-w-0">
                    <h3 class="font-semibold text-gray-800 text-base truncate" id="song-title">เพลงของเรา (Our Favorite Song)</h3>
                    <p class="text-xs text-pink-500 font-medium truncate" id="song-artist">Artist - Love Song 💕</p>
                    
                    <!-- Progress Bar -->
                    <div class="w-full bg-pink-100 h-2 rounded-full mt-3 cursor-pointer overflow-hidden" id="progress-container">
                        <div class="bg-pink-500 h-full w-1/3 rounded-full transition-all duration-100" id="progress-bar"></div>
                    </div>
                    <div class="flex justify-between text-[10px] text-gray-400 mt-1">
                        <span id="current-time">0:00</span>
                        <span id="total-time">3:45</span>
                    </div>
                </div>
            </div>

            <!-- Controls -->
            <div class="flex items-center justify-center space-x-6 mt-4 pt-2 border-t border-pink-100/50">
                <button id="prev-btn" class="text-gray-400 hover:text-pink-500 transition-colors">
                    <i class="fa-solid fa-backward-step text-lg"></i>
                </button>
                <button id="play-btn" class="w-12 h-12 bg-pink-500 hover:bg-pink-600 text-white rounded-full flex items-center justify-center shadow-lg shadow-pink-300 transition-all transform hover:scale-105 active:scale-95">
                    <i class="fa-solid fa-play text-lg translate-x-0.5" id="play-icon"></i>
                </button>
                <button id="next-btn" class="text-gray-400 hover:text-pink-500 transition-colors">
                    <i class="fa-solid fa-forward-step text-lg"></i>
                </button>
            </div>
            
            <!-- Hidden Audio Element -->
            <audio id="bg-music" loop>
                <!-- เปลี่ยน URL ตรงนี้เป็นไฟล์ MP3 เพลงของคุณได้เลย -->
                <source src="https://cdn.pixabay.com/download/audio/2022/05/27/audio_1808fbf07a.mp3?filename=lofi-study-112191.mp3" type="audio/mpeg">
                Browser ไม่รองรับการเล่นเสียง
            </audio>
        </section>

        <section class="glass-card rounded-3xl p-6 sm:p-8 text-center shadow-xl space-y-6">
            <div class="space-y-1">
                <h2 class="text-xl sm:text-2xl font-bold text-gray-800">
                    <i class="fa-solid fa-heart text-pink-500 pulse-heart mr-2"></i>
                    ระยะเวลาที่เราเดินทางมาร่วมกัน
                </h2>
                <p class="text-xs sm:text-sm text-gray-500">นับตั้งแต่วันแรกที่เราเริ่มตกลงคบกัน...</p>
            </div>

            <div class="grid grid-cols-2 sm:grid-cols-4 gap-3 sm:gap-4">
                <div class="bg-white/80 p-4 rounded-2xl shadow-sm border border-pink-100">
                    <span class="block text-3xl sm:text-4xl font-extrabold text-pink-600" id="days">00</span>
                    <span class="text-xs text-gray-500 font-medium">วัน (Days)</span>
                </div>
                <div class="bg-white/80 p-4 rounded-2xl shadow-sm border border-pink-100">
                    <span class="block text-3xl sm:text-4xl font-extrabold text-pink-500" id="hours">00</span>
                    <span class="text-xs text-gray-500 font-medium">ชั่วโมง (Hours)</span>
                </div>
                <div class="bg-white/80 p-4 rounded-2xl shadow-sm border border-pink-100">
                    <span class="block text-3xl sm:text-4xl font-extrabold text-pink-400" id="minutes">00</span>
                    <span class="text-xs text-gray-500 font-medium">นาที (Minutes)</span>
                </div>
                <div class="bg-white/80 p-4 rounded-2xl shadow-sm border border-pink-100">
                    <span class="block text-3xl sm:text-4xl font-extrabold text-rose-400" id="seconds">00</span>
                    <span class="text-xs text-gray-500 font-medium">วินาที (Seconds)</span>
                </div>
            </div>
            
            <p class="text-xs text-pink-400 font-medium italic">"And every single second with you is my favorite."</p>
        </section>

        <section class="space-y-6">
            <div class="text-center space-y-1">
                <h2 class="text-2xl font-bold text-gray-800">📸 ความทรงจำของเรา (Our Memories)</h2>
                <p class="text-xs text-gray-500">ช่วงเวลาดีๆ ที่อยากบันทึกเก็บไว้ตลอดไป</p>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
                <!-- Photo Card 1 -->
                <div class="glass-card glass-card-hover rounded-2xl overflow-hidden p-3 bg-white/90">
                    <div class="relative overflow-hidden rounded-xl aspect-square mb-3">
                        <img src="https://images.unsplash.com/photo-1516589178581-6cd7833ae3b2?w=500&auto=format&fit=crop&q=80" alt="Memory 1" class="w-full h-full object-cover transform hover:scale-110 transition-transform duration-500">
                    </div>
                    <div class="px-2 pb-2 text-center">
                        <h3 class="font-semibold text-pink-600 text-sm">เดทแรกของเรา ☕</h3>
                        <p class="text-xs text-gray-500 mt-1">วันที่ตื่นเต้นที่สุดและมีความสุขมากที่สุด</p>
                    </div>
                </div>

                <!-- Photo Card 2 -->
                <div class="glass-card glass-card-hover rounded-2xl overflow-hidden p-3 bg-white/90">
                    <div class="relative overflow-hidden rounded-xl aspect-square mb-3">
                        <img src="https://images.unsplash.com/photo-1522673607200-164d1b6ce486?w=500&auto=format&fit=crop&q=80" alt="Memory 2" class="w-full h-full object-cover transform hover:scale-110 transition-transform duration-500">
                    </div>
                    <div class="px-2 pb-2 text-center">
                        <h3 class="font-semibold text-pink-600 text-sm">ทริปไปเที่ยวด้วยกัน 🌊</h3>
                        <p class="text-xs text-gray-500 mt-1">นั่งมองพระอาทิตย์ตกดินข้างๆ เธอ</p>
                    </div>
                </div>

                <!-- Photo Card 3 -->
                <div class="glass-card glass-card-hover rounded-2xl overflow-hidden p-3 bg-white/90">
                    <div class="relative overflow-hidden rounded-xl aspect-square mb-3">
                        <img src="https://images.unsplash.com/photo-1518199266791-5375a83190b7?w=500&auto=format&fit=crop&q=80" alt="Memory 3" class="w-full h-full object-cover transform hover:scale-110 transition-transform duration-500">
                    </div>
                    <div class="px-2 pb-2 text-center">
                        <h3 class="font-semibold text-pink-600 text-sm">วันธรรมดาที่พิเศษ 💖</h3>
                        <p class="text-xs text-gray-500 mt-1">แค่มีเธออยู่ใกล้ๆ วันไหนๆ ก็ดีเสมอ</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="glass-card rounded-3xl p-6 sm:p-8 shadow-xl space-y-6">
            <div class="text-center space-y-1">
                <h2 class="text-2xl font-bold text-gray-800">💌 เหตุผลที่ตกหลุมรักเธอ</h2>
                <p class="text-xs text-gray-500">กดที่การ์ดเพื่อเปิดดูข้อความน่ารักๆ นะ</p>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                <!-- Interactive Card 1 -->
                <div onclick="toggleReason(this)" class="cursor-pointer bg-white/70 hover:bg-pink-50 p-4 rounded-2xl border border-pink-100 transition-all duration-300">
                    <div class="flex items-center space-x-3">
                        <div class="w-10 h-10 rounded-full bg-pink-100 flex items-center justify-center text-pink-500 shrink-0">
                            <i class="fa-solid fa-smile-beam"></i>
                        </div>
                        <div>
                            <h4 class="font-semibold text-pink-600 text-sm">1. รอยยิ้มของเธอ</h4>
                            <p class="reason-content text-xs text-gray-600 hidden mt-1">เพราะเวลาเธอยิ้มหรือหัวเราะ มันทำให้โลกทั้งใบสดใสขึ้นมาทันทีเลย 😊</p>
                        </div>
                    </div>
                </div>

                <!-- Interactive Card 2 -->
                <div onclick="toggleReason(this)" class="cursor-pointer bg-white/70 hover:bg-pink-50 p-4 rounded-2xl border border-pink-100 transition-all duration-300">
                    <div class="flex items-center space-x-3">
                        <div class="w-10 h-10 rounded-full bg-pink-100 flex items-center justify-center text-pink-500 shrink-0">
                            <i class="fa-solid fa-hand-holding-heart"></i>
                        </div>
                        <div>
                            <h4 class="font-semibold text-pink-600 text-sm">2. ความใส่ใจของเธอ</h4>
                            <p class="reason-content text-xs text-gray-600 hidden mt-1">เธอคอยเป็นห่วงและใส่ใจในเรื่องเล็กๆ น้อยๆ เสมอ ไม่เคยเปลี่ยน 💕</p>
                        </div>
                    </div>
                </div>

                <!-- Interactive Card 3 -->
                <div onclick="toggleReason(this)" class="cursor-pointer bg-white/70 hover:bg-pink-50 p-4 rounded-2xl border border-pink-100 transition-all duration-300">
                    <div class="flex items-center space-x-3">
                        <div class="w-10 h-10 rounded-full bg-pink-100 flex items-center justify-center text-pink-500 shrink-0">
                            <i class="fa-solid fa-mug-hot"></i>
                        </div>
                        <div>
                            <h4 class="font-semibold text-pink-600 text-sm">3. พื้นที่ปลอดภัย</h4>
                            <p class="reason-content text-xs text-gray-600 hidden mt-1">การได้อยู่ข้างๆ เธอทำให้รู้สึกสบายใจและเป็นตัวเองได้มากที่สุด 🏡</p>
                        </div>
                    </div>
                </div>

                <!-- Interactive Card 4 -->
                <div onclick="toggleReason(this)" class="cursor-pointer bg-white/70 hover:bg-pink-50 p-4 rounded-2xl border border-pink-100 transition-all duration-300">
                    <div class="flex items-center space-x-3">
                        <div class="w-10 h-10 rounded-full bg-pink-100 flex items-center justify-center text-pink-500 shrink-0">
                            <i class="fa-solid fa-star"></i>
                        </div>
                        <div>
                            <h4 class="font-semibold text-pink-600 text-sm">4. การเป็นเธอ</h4>
                            <p class="reason-content text-xs text-gray-600 hidden mt-1">ชอบทุกอย่างที่เป็นเธอ ขอบคุณที่เกิดมาให้รักนะคนเก่ง ✨</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="text-center py-6">
            <button onclick="openModal()" class="px-8 py-4 bg-gradient-to-r from-pink-500 to-rose-400 hover:from-pink-600 hover:to-rose-500 text-white font-semibold rounded-full shadow-lg shadow-pink-300 transform hover:scale-105 active:scale-95 transition-all flex items-center justify-center space-x-2 mx-auto">
                <i class="fa-solid fa-envelope-open-text text-xl"></i>
                <span>เปิดจดหมายความในใจ 💌</span>
            </button>
        </section>

        <!-- Footer -->
        <footer class="text-center text-xs text-pink-400 pt-4">
            Made with ❤️ for You | Forever & Always
        </footer>
    </div>

    <div id="love-modal" class="fixed inset-0 bg-black/40 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4">
        <div class="glass-card bg-white rounded-3xl max-w-lg w-full p-6 sm:p-8 space-y-6 relative modal-enter border-2 border-pink-200">
            <!-- Close Button -->
            <button onclick="closeModal()" class="absolute top-4 right-4 w-8 h-8 rounded-full bg-pink-100 text-pink-500 hover:bg-pink-200 flex items-center justify-center transition-colors">
                <i class="fa-solid fa-xmark"></i>
            </button>

            <!-- Letter Content -->
            <div class="text-center space-y-4">
                <div class="w-16 h-16 bg-pink-100 text-pink-500 rounded-full flex items-center justify-center mx-auto text-2xl pulse-heart">
                    <i class="fa-solid fa-heart"></i>
                </div>
                <h3 class="text-2xl font-bold text-gray-800">ถึงคนพิเศษของฉัน 💖</h3>
                <div class="text-sm text-gray-600 leading-relaxed text-left space-y-3 max-h-60 overflow-y-auto pr-2">
                    <p>
                        ขอบคุณสำหรับทุกๆ ช่วงเวลาที่ผ่านมานะ ไม่ว่าจะวันที่มีความสุข หรือวันที่เหนื่อยล้า การมีเธออยู่ข้างๆ คือเรื่องที่ดีที่สุดเสมอ
                    </p>
                    <p>
                        หวังว่าเว็บไซต์เล็กๆ นี้น่าจะช่วยสร้างรอยยิ้มให้เธอได้นะ อยากให้อยู่ด้วยกันแบบนี้ไปนานๆ เติบโตและมีความสุขไปด้วยกันในทุกๆ วันนะคับ!
                    </p>
                    <p class="text-right font-medium text-pink-600">
                        รักเธอที่สุดเลยนะ ❤️
                    </p>
                </div>
                <button onclick="closeModal()" class="w-full py-3 bg-pink-500 hover:bg-pink-600 text-white rounded-2xl font-semibold transition-colors shadow-md shadow-pink-200">
                    เก็บความทรงจำนี้ไว้ในใจ ✨
                </button>
            </div>
        </div>
    </div>

    <script>
        /* --- 1. FLOATING HEARTS BACKGROUND --- */
        function createHearts() {
            const container = document.getElementById('heart-container');
            const heartIcons = ['fa-heart', 'fa-hand-holding-heart', 'fa-spa'];
            
            setInterval(() => {
                const heart = document.createElement('i');
                const randomIcon = heartIcons[Math.floor(Math.random() * heartIcons.length)];
                
                heart.className = `fa-solid ${randomIcon} floating-heart`;
                heart.style.left = Math.random() * 100 + 'vw';
                heart.style.animationDuration = (Math.random() * 4 + 6) + 's'; // 6-10s
                heart.style.fontSize = (Math.random() * 15 + 10) + 'px'; // 10-25px
                
                container.appendChild(heart);
                
                setTimeout(() => {
                    heart.remove();
                }, 10000);
            }, 600);
        }

        /* --- 2. ANNIVERSARY DAYS COUNTER --- */
        // ** ปรับเปลี่ยนวันที่เริ่มต้นคบกันตรงนี้ ** (ปี, เดือน [0-11], วัน)
        // หมายเหตุ: เดือนเริ่มนับจาก 0 (ม.ค. = 0, ก.พ. = 1, ..., ธ.ค. = 11)
        const startDate = new Date(2023, 1, 14, 0, 0, 0); // ตัวอย่าง: 14 กุมภาพันธ์ 2023

        function updateCounter() {
            const now = new Date();
            const diff = now - startDate;

            const 
