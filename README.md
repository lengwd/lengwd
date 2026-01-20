<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> Wenda Leng - Personal Page</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }

        @keyframes float {
            0% {transform: translateY(0px);}
            50% {transform: translateY(-20px);}
            100% {transform: translateY(0px);}
        }

        .gradient-text {
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-image: linear-gradient(to right, #60a5fa, #c084fc);
        }

        .animate-float {
            animation: float 6s ease-in-out infinite;
        }

        .glass-card {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
    </style>
</head>
<body class="min-h-screen bg-slate-900 overflow-hidden relative selection:bg-purple-500 selection:text-white">
    <div class="fixed top-0 left-0 w-full h-full overflow-hidden -z-10">
        <div class="absolute top-[-10%] left-[-10%] w-[500px] h-[500px] bg-blue-600/20 rounded-full blur-[120px] mix-blend-screen animate-float"></div>
        <div class="absolute bottom-[-10%] right-[-10%] w-[600px] h-[600px] bg-purple-600/20 rounded-full blur-[120px] mix-blend-screen animate-float" style="animation-delay: -3s;"></div>
    </div>

    <main  class="flex flex-col items-center justify-center min-h-screen px-4 text-center">
        <!-- 名字部分 -->
        <div class="relative group cursor-default">
            <!-- 装饰性的小圆点 -->
            <div class="absolute -top-6 left-1/2 transform -translate-x-1/2 w-1 h-1 bg-blue-400 rounded-full opacity-50 transition-all duration-500 group-hover:w-full group-hover:h-[1px] group-hover:top-full group-hover:mt-2 group-hover:bg-gradient-to-r group-hover:from-transparent group-hover:via-purple-400 group-hover:to-transparent"></div>
            
            <h1 class="text-6xl md:text-8xl font-bold tracking-tight mb-2 text-white">
                Wenda Leng
            </h1>
        </div>

        <!-- 标签行 -->
        <div class="mt-8 flex flex-col md:flex-row items-center justify-center space-y-4 md:space-y-0 md:space-x-6 text-lg md:text-xl font-light text-slate-300">
            
            <!-- 标签 1 -->
            <div class="group flex items-center space-x-2 transition-colors duration-300 hover:text-blue-400 cursor-default">
                <span class="w-1.5 h-1.5 bg-slate-500 rounded-full group-hover:bg-blue-400 transition-colors md:hidden"></span>
                <span>AI Enthusiast</span>
            </div>

            <span class="hidden md:inline-block text-slate-700 select-none">/</span>

            <!-- 标签 2 -->
            <div class="group flex items-center space-x-2 transition-colors duration-300 hover:text-purple-400 cursor-default">
                <span class="w-1.5 h-1.5 bg-slate-500 rounded-full group-hover:bg-purple-400 transition-colors md:hidden"></span>
                <span>Future Practitioner</span>
            </div>

            <span class="hidden md:inline-block text-slate-700 select-none">/</span>

            <!-- 标签 3 -->
            <div class="group flex items-center space-x-2 transition-colors duration-300 hover:text-pink-400 cursor-default">
                <!-- <span class="w-1.5 h-1.5 bg-slate-500 rounded-full group-hover:bg-pink-400 transition-colors md:hidden"></span> -->
                <span class="w-1.5 h-1.5 bg-slate-500 rounded-full group-hover:bg-pink-400 transition-colors md:hidden"></span>
                <span>On the way</span>
            </div>
        </div>
    </main>

    <style>
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>

    <script>
        // 简单的入场动画增强
        document.addEventListener('DOMContentLoaded', () => {
            const tags = document.querySelectorAll('.group');
            tags.forEach((tag, index) => {
                tag.style.opacity = '0';
                tag.style.transform = 'translateY(10px)';
                tag.style.transition = 'all 0.6s ease-out';
                setTimeout(() => {
                    tag.style.opacity = '1';
                    tag.style.transform = 'translateY(0)';
                }, 300 + (index * 150));
            });
        });
    </script>
</body>
