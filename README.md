<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>林云网 - 下载中心</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <style>
        /* 林云网品牌渐变 */
        .bg-gradient-linyun {
            background: linear-gradient(135deg, #003366 0%, #0066CC 50%, #0099FF 100%);
        }
        .btn-download {
            position: relative;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 1rem 2.5rem;
            font-size: 1.125rem;
            font-weight: 500;
            color: white;
            border-radius: 9999px;
            background: linear-gradient(to right, #0099FF, #0066CC);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
            overflow: hidden;
            transition: all 0.3s ease;
        }
        .btn-download::after {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
            transition: all 0.6s ease;
        }
        .btn-download:hover::after {
            left: 100%;
        }
        .btn-download:hover {
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
            transform: scale(1.05);
        }
        .logo-container {
            width: 6rem;
            height: 6rem;
            margin: 0 auto 2rem;
            border-radius: 1rem;
            background: white;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }
        .wave-shape {
            animation: wave 8s linear infinite;
        }
        @keyframes wave {
            0% { clip-path: polygon(0 100%, 100% 100%, 100% 0, 0 40%); }
            50% { clip-path: polygon(0 100%, 100% 100%, 100% 0, 0 30%); }
            100% { clip-path: polygon(0 100%, 100% 100%, 100% 0, 0 40%); }
        }
        .bg-dark {
            background-color: #003366;
        }
    </style>
</head>
<body class="m-0 p-0 font-sans bg-white antialiased opacity-0 transition-opacity duration-500">
    <!-- 顶部渐变背景区域 -->
    <div class="w-full min-h-[500px] bg-gradient-linyun flex flex-col items-center justify-center relative overflow-hidden">
        <!-- 装饰光点 -->
        <div class="absolute inset-0 overflow-hidden">
            <div class="absolute top-20 left-10 w-40 h-40 bg-white/10 rounded-full blur-3xl"></div>
            <div class="absolute bottom-20 right-10 w-60 h-60 bg-white/10 rounded-full blur-3xl"></div>
        </div>
        
        <!-- 波浪装饰 -->
        <div class="absolute bottom-0 left-0 w-full h-24 bg-white wave-shape"></div>
        
        <!-- LOGO -->
        <div class="logo-container z-10">
            <img src="https://p11-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/46f772983081433c8301ba3128d836ad.png~tplv-a9rns2rl98-24:720:720.png?rcl=20251212132808FE14A91F2136CEFEF7BF&rk3s=8e244e95&rrcfp=8a172a1a&x-expires=1766122089&x-signature=l6eoA15SbiNDdK9SBSegvuVls4U%3D" 
                 alt="林云网LOGO" class="w-full h-full object-contain p-2">
        </div>
        
        <!-- 标题 -->
        <h1 class="text-[36px] md:text-[42px] font-medium text-white mb-12 z-10 tracking-wider">林云网</h1>
    </div>

    <!-- 下载按钮区域 -->
    <div class="w-full flex flex-col items-center justify-center py-20 px-4">
        <!-- 安卓下载按钮 -->
        <a href="https://github.com/hcncnn45/PakePlus-Android-v2.1.3/releases/download/bfbcaadfcdd/bfbcaadfcdd-v1.0.1.apk" 
           class="btn-download mb-8 w-full max-w-xs" download>
            <i class="fa fa-android mr-3 text-xl"></i>
            安卓下载
        </a>
        
        <!-- Windows下载按钮 -->
        <a href="https://github.com/hcncnn45/PakePlus-v2.1.3/releases/download/bfbcaadfcdd/bfbcaadfcdd_1.0.1_x64-setup.exe" 
           class="btn-download w-full max-w-xs" download>
            <i class="fa fa-windows mr-3 text-xl"></i>
            Windows下载
        </a>
        
        <!-- 版本信息 -->
        <div class="mt-10 text-center text-gray-500 text-sm">
            <p class="flex flex-wrap items-center justify-center gap-2">
                <i class="fa fa-info-circle mr-2 text-blue-500"></i>
                <span>当前版本：1.0.1</span>
                <span>|</span>
                <span>安卓包大小：约8MB</span>
                <span>|</span>
                <span>Windows包大小：约10MB</span>
            </p>
        </div>
    </div>

    <!-- 页脚 -->
    <footer class="w-full py-8 text-center text-gray-600 text-sm border-t border-gray-100">
        <p>© 2025 林云网 版权所有</p>
        <p class="mt-2 text-gray-400">轻量级网页打包工具 | 简单 · 高效 · 便捷</p>
    </footer>

    <script>
        // 页面加载显示
        window.addEventListener('load', () => {
            document.body.classList.add('opacity-100');
        });

        // 下载按钮交互
        document.querySelectorAll('.btn-download').forEach(btn => {
            btn.addEventListener('click', function(e) {
                if (this.classList.contains('loading')) return;
                
                this.classList.add('loading', 'opacity-80');
                const originalHTML = this.innerHTML;
                const platformIcon = this.querySelector('i').className;
                
                this.innerHTML = `<i class="${platformIcon} mr-3 text-xl"></i>下载中...`;
                
                setTimeout(() => {
                    this.innerHTML = originalHTML;
                    this.classList.remove('loading', 'opacity-80');
                }, 3000);
            });
        });

        // LOGO滚动效果
        window.addEventListener('scroll', () => {
            const logo = document.querySelector('.logo-container');
            const scrollY = window.scrollY;
            logo.classList.toggle('scale-95', scrollY > 50);
            logo.classList.toggle('scale-100', scrollY <= 50);
        });

        // 下载提示
        function showDownloadToast(platform) {
            const toast = document.createElement('div');
            toast.className = 'fixed bottom-6 left-1/2 -translate-x-1/2 bg-dark text-white px-6 py-3 rounded-lg shadow-2xl z-50';
            toast.innerHTML = `<i class="fa fa-download mr-2"></i>已开始下载${platform}版本`;
            document.body.appendChild(toast);
            
            setTimeout(() => {
                toast.classList.add('opacity-0', 'transition-opacity', 'duration-500');
                setTimeout(() => toast.remove(), 500);
            }, 2000);
        }

        // 绑定提示
        document.querySelectorAll('.btn-download').forEach(btn => {
            btn.addEventListener('click', function() {
                const platform = this.textContent.includes('安卓') ? '安卓' : 'Windows';
                setTimeout(() => showDownloadToast(platform), 500);
            });
        });
    </script>
</body>
</html>
