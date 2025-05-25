# 红客联盟
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>中国红客 | 网络安全专家</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    
    <!-- Tailwind配置 -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#00FF41', // 科技绿
                        secondary: '#00FF00',
                        dark: '#0D0208',
                        accent: '#008F11',
                        terminal: '#05FF00',
                        chinaRed: '#DE2910', // 中国红
                        starYellow: '#FFFF00' // 五星黄
                    },
                    fontFamily: {
                        matrix: ['Courier New', 'monospace']
                    },
                    animation: {
                        'pulse-slow': 'pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                        'glow': 'glow 2s ease-in-out infinite alternate',
                        'matrix': 'matrix 10s linear infinite',
                        'fade-in': 'fadeIn 1.5s ease-in-out forwards',
                        'slide-up': 'slideUp 1s ease-out forwards',
                        'float': 'float 3s ease-in-out infinite',
                        'typewriter': 'typewriter 4s steps(40) 1s 1 normal both',
                        'blink': 'blink 1s infinite'
                    },
                    keyframes: {
                        glow: {
                            '0%': { 'text-shadow': '0 0 5px #fff, 0 0 10px #fff, 0 0 15px #00FF41, 0 0 20px #00FF41' },
                            '100%': { 'text-shadow': '0 0 10px #fff, 0 0 20px #fff, 0 0 30px #00FF41, 0 0 40px #00FF41' }
                        },
                        matrix: {
                            '0%': { 'background-position': '0 0' },
                            '100%': { 'background-position': '0 -2000px' }
                        },
                        fadeIn: {
                            '0%': { opacity: '0' },
                            '100%': { opacity: '1' }
                        },
                        slideUp: {
                            '0%': { transform: 'translateY(30px)', opacity: '0' },
                            '100%': { transform: 'translateY(0)', opacity: '1' }
                        },
                        float: {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(-10px)' }
                        },
                        typewriter: {
                            'from': { width: '0' },
                            'to': { width: '100%' }
                        },
                        blink: {
                            'from, to': { borderColor: 'transparent' },
                            '50%': { borderColor: '#00FF41' }
                        }
                    }
                }
            }
        }
    </script>
    
    <style type="text/tailwindcss">
        @layer utilities {
            .content-auto {
                content-visibility: auto;
            }
            .matrix-bg {
                background-image: url('data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyMDAgMjAwIj48cGF0aCBkPSJNMCwwIEwyMDAsMjAwIEwwLDIwMCBMMjAwLDAgWiIgZmlsbD0iIzBGMTQwRiIgb3BhY2l0eT0iMC4xIi8+PC9zdmc+');
                background-size: 100px 100px;
            }
            .terminal-border {
                border: 2px solid #00FF41;
                box-shadow: 0 0 10px #00FF41;
            }
            .neon-text {
                text-shadow: 0 0 5px #fff, 0 0 10px #fff, 0 0 15px #00FF41, 0 0 20px #00FF41;
            }
            .neon-border {
                box-shadow: 0 0 5px #00FF41, 0 0 10px #00FF41;
            }
            .glass-effect {
                backdrop-filter: blur(10px);
                background-color: rgba(13, 2, 8, 0.8);
            }
            .typing-container {
                display: inline-block;
            }
            .typing-text {
                overflow: hidden;
                border-right: 0.15em solid #00FF41;
                white-space: nowrap;
                margin: 0 auto;
                letter-spacing: 0.15em;
                animation: typing 3.5s steps(40, end), blink-caret 0.75s step-end infinite;
            }
            @keyframes typing {
                from { width: 0 }
                to { width: 100% }
            }
            @keyframes blink-caret {
                from, to { border-color: transparent }
                50% { border-color: #00FF41; }
            }
            .flag-wave {
                animation: wave 8s ease-in-out infinite;
                transform-origin: left center;
            }
            @keyframes wave {
                0% { transform: skewY(0deg); }
                25% { transform: skewY(1deg) rotateZ(0.5deg); }
                50% { transform: skewY(0deg); }
                75% { transform: skewY(-1deg) rotateZ(-0.5deg); }
                100% { transform: skewY(0deg); }
            }
            .mobile-flag {
                position: absolute;
                top: 10vh;
                right: 0;
                width: 40vw;
                height: auto;
                z-index: 0;
            }
            .desktop-flag {
                position: absolute;
                top: 0;
                right: 0;
                width: 30vw;
                height: auto;
                z-index: 0;
            }
            .text-gradient {
                background-clip: text;
                -webkit-background-clip: text;
                color: transparent;
                background-image: linear-gradient(90deg, #00FF41, #00FF00);
            }
            .hover-scale {
                transition: transform 0.3s ease;
            }
            .hover-scale:hover {
                transform: scale(1.03);
            }
        }
    </style>
</head>
<body class="bg-dark text-terminal font-matrix min-h-screen overflow-x-hidden opacity-0" id="main-body">
    <!-- 背景矩阵效果容器 -->
    <div id="matrix-container" class="fixed inset-0 z-0 pointer-events-none"></div>

    <!-- 内容容器 -->
    <div class="relative z-10">
        <!-- 顶部导航 -->
        <nav class="fixed top-0 w-full z-50 glass-effect opacity-0" id="main-nav">
            <div class="container mx-auto px-4 py-3 flex justify-between items-center">
                <div class="text-primary text-2xl font-bold neon-text">CHINA HACKER</div>
                <div class="hidden md:flex space-x-8">
                    <a href="#home" class="hover:text-primary transition-colors duration-300 hover-scale">首页</a>
                    <a href="#services" class="hover:text-primary transition-colors duration-300 hover-scale">服务</a>
                    <a href="#skills" class="hover:text-primary transition-colors duration-300 hover-scale">技能</a>
                    <a href="#contact" class="hover:text-primary transition-colors duration-300 hover-scale">联系我</a>
                </div>
                <div class="md:hidden">
                    <button id="menu-toggle" class="text-primary hover-scale">
                        <i class="fa fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
            <!-- 移动端菜单 -->
            <div id="mobile-menu" class="hidden md:hidden glass-effect">
                <div class="container mx-auto px-4 py-3 flex flex-col space-y-4">
                    <a href="#home" class="hover:text-primary transition-colors duration-300 hover-scale">首页</a>
                    <a href="#services" class="hover:text-primary transition-colors duration-300 hover-scale">服务</a>
                    <a href="#skills" class="hover:text-primary transition-colors duration-300 hover-scale">技能</a>
                    <a href="#contact" class="hover:text-primary transition-colors duration-300 hover-scale">联系我</a>
                </div>
            </div>
        </nav>

        <!-- 英雄区域 -->
        <section id="home" class="min-h-screen flex items-center justify-center relative pt-20 overflow-hidden">
            <!-- 中国国旗元素 - 优化位置 -->
            <div class="hidden md:block desktop-flag flag-wave opacity-90">
                <svg viewBox="0 0 300 200" class="w-full h-auto">
                    <!-- 红色背景 -->
                    <rect width="300" height="200" fill="#DE2910"/>
                    
                    <!-- 大五角星 -->
                    <path d="M100,50 L110,65 L128,65 L113,75 L118,93 L100,83 L82,93 L87,75 L72,65 L90,65 Z" fill="#FFFF00"/>
                    
                    <!-- 四颗小五角星 -->
                    <path d="M140,30 L144,37 L151,37 L146,41 L148,49 L140,45 L132,49 L134,41 L129,37 L136,37 Z" fill="#FFFF00"/>
                    <path d="M150,45 L154,52 L161,52 L156,56 L158,64 L150,60 L142,64 L144,56 L139,52 L146,52 Z" fill="#FFFF00"/>
                    <path d="M150,70 L154,77 L161,77 L156,81 L158,89 L150,85 L142,89 L144,81 L139,77 L146,77 Z" fill="#FFFF00"/>
                    <path d="M140,90 L144,97 L151,97 L146,101 L148,109 L140,105 L132,109 L134,101 L129,97 L136,97 Z" fill="#FFFF00"/>
                </svg>
            </div>
            
            <!-- 移动端国旗 -->
            <div class="md:hidden mobile-flag flag-wave opacity-90">
                <svg viewBox="0 0 300 200" class="w-full h-auto">
                    <!-- 红色背景 -->
                    <rect width="300" height="200" fill="#DE2910"/>
                    
                    <!-- 大五角星 -->
                    <path d="M100,50 L110,65 L128,65 L113,75 L118,93 L100,83 L82,93 L87,75 L72,65 L90,65 Z" fill="#FFFF00"/>
                    
                    <!-- 四颗小五角星 -->
                    <path d="M140,30 L144,37 L151,37 L146,41 L148,49 L140,45 L132,49 L134,41 L129,37 L136,37 Z" fill="#FFFF00"/>
                    <path d="M150,45 L154,52 L161,52 L156,56 L158,64 L150,60 L142,64 L144,56 L139,52 L146,52 Z" fill="#FFFF00"/>
                    <path d="M150,70 L154,77 L161,77 L156,81 L158,89 L150,85 L142,89 L144,81 L139,77 L146,77 Z" fill="#FFFF00"/>
                    <path d="M140,90 L144,97 L151,97 L146,101 L148,109 L140,105 L132,109 L134,101 L129,97 L136,97 Z" fill="#FFFF00"/>
                </svg>
            </div>
            
            <!-- 背景文字 -->
            <div class="absolute inset-0 flex items-center justify-center">
                <div class="text-[clamp(5rem,20vw,15rem)] font-bold text-primary/5 opacity-10">HACKER</div>
            </div>
            
            <!-- 中央内容 -->
            <div class="container mx-auto px-4 z-10 text-center">
                <div class="max-w-4xl mx-auto">
                    <div class="terminal-border rounded-lg p-8 relative overflow-hidden opacity-0 transform translate-y-10" id="hero-card">
                        <div class="absolute top-0 right-0 m-2 flex space-x-2">
                            <div class="w-3 h-3 rounded-full bg-red-500 animate-pulse"></div>
                            <div class="w-3 h-3 rounded-full bg-yellow-500 animate-pulse" style="animation-delay: 0.2s"></div>
                            <div class="w-3 h-3 rounded-full bg-green-500 animate-pulse" style="animation-delay: 0.4s"></div>
                        </div>
                        
                        <h1 class="text-[clamp(2rem,8vw,4rem)] font-bold mb-6 neon-text animate-glow opacity-0 typing-container" id="hero-title">
                            <span class="typing-text">中国红客</span>
                        </h1>
                        
                        <p class="text-[clamp(1rem,3vw,1.5rem)] mb-8 leading-relaxed opacity-0" id="hero-subtitle">
                            网络安全专家 | 免费电脑问题解决方案
                        </p>
                        
                        <div class="flex flex-col sm:flex-row justify-center gap-4 opacity-0" id="hero-buttons">
                            <a href="#services" class="px-6 py-3 border border-primary text-primary hover:bg-primary hover:text-dark transition-all duration-300 rounded-md transform hover:scale-105 hover-neon-border">
                                了解服务
                            </a>
                            <a href="#contact" class="px-6 py-3 bg-primary text-dark hover:bg-opacity-80 transition-all duration-300 rounded-md transform hover:scale-105 hover-neon-border">
                                联系我
                            </a>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- 底部波浪装饰 -->
            <div class="absolute bottom-0 left-0 w-full">
                <svg viewBox="0 0 1440 100" fill="none" xmlns="http://www.w3.org/2000/svg" class="w-full h-auto">
                    <path d="M0,32L48,42.7C96,53,192,75,288,74.7C384,75,480,53,576,48C672,43,768,53,864,58.7C960,64,1056,64,1152,58.7C1248,53,1344,43,1392,37.3L1440,32L1440,100L1392,100C1344,100,1248,100,1152,100C1056,100,960,100,864,100C768,100,672,100,576,100C480,100,384,100,288,100C192,100,96,100,48,100L0,100Z" fill="rgba(0, 255, 65, 0.1)"/>
                </svg>
            </div>
        </section>

        <!-- 服务区域 -->
        <section id="services" class="py-20 relative">
            <div class="container mx-auto px-4">
                <h2 class="text-[clamp(1.5rem,5vw,2.5rem)] font-bold mb-16 text-center neon-text opacity-0" id="services-title">
                    <span class="text-primary">我的服务</span>
                </h2>
                
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- 服务卡片 1 -->
                    <div class="terminal-border rounded-lg p-6 hover:neon-border transition-all duration-500 transform hover:-translate-y-2 opacity-0 service-card" data-delay="100">
                        <div class="text-primary text-4xl mb-4 animate-float">
                            <i class="fa fa-shield"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">系统安全检测</h3>
                        <p class="text-gray-300 mb-4">全面扫描系统漏洞，检测恶意软件，保障你的电脑安全。</p>
                        <a href="#contact" class="text-primary hover:underline inline-flex items-center hover-scale">
                            <span>免费咨询</span>
                            <i class="fa fa-arrow-right ml-2"></i>
                        </a>
                    </div>
                    
                    <!-- 服务卡片 2 -->
                    <div class="terminal-border rounded-lg p-6 hover:neon-border transition-all duration-500 transform hover:-translate-y-2 opacity-0 service-card" data-delay="200">
                        <div class="text-primary text-4xl mb-4 animate-float" style="animation-delay: 0.2s">
                            <i class="fa fa-wrench"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">系统故障修复</h3>
                        <p class="text-gray-300 mb-4">解决系统崩溃、蓝屏、启动问题等各类软硬件故障。</p>
                        <a href="#contact" class="text-primary hover:underline inline-flex items-center hover-scale">
                            <span>免费咨询</span>
                            <i class="fa fa-arrow-right ml-2"></i>
                        </a>
                    </div>
                    
                    <!-- 服务卡片 3 -->
                    <div class="terminal-border rounded-lg p-6 hover:neon-border transition-all duration-500 transform hover:-translate-y-2 opacity-0 service-card" data-delay="300">
                        <div class="text-primary text-4xl mb-4 animate-float" style="animation-delay: 0.4s">
                            <i class="fa fa-bolt"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">系统优化加速</h3>
                        <p class="text-gray-300 mb-4">清理系统垃圾，优化系统配置，提升电脑运行速度。</p>
                        <a href="#contact" class="text-primary hover:underline inline-flex items-center hover-scale">
                            <span>免费咨询</span>
                            <i class="fa fa-arrow-right ml-2"></i>
                        </a>
                    </div>
                    
                    <!-- 服务卡片 4 -->
                    <div class="terminal-border rounded-lg p-6 hover:neon-border transition-all duration-500 transform hover:-translate-y-2 opacity-0 service-card" data-delay="400">
                        <div class="text-primary text-4xl mb-4 animate-float" style="animation-delay: 0.6s">
                            <i class="fa fa-lock"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">数据恢复与加密</h3>
                        <p class="text-gray-300 mb-4">恢复丢失的数据，并提供安全的数据加密解决方案。</p>
                        <a href="#contact" class="text-primary hover:underline inline-flex items-center hover-scale">
                            <span>免费咨询</span>
                            <i class="fa fa-arrow-right ml-2"></i>
                        </a>
                    </div>
                    
                    <!-- 服务卡片 5 -->
                    <div class="terminal-border rounded-lg p-6 hover:neon-border transition-all duration-500 transform hover:-translate-y-2 opacity-0 service-card" data-delay="500">
                        <div class="text-primary text-4xl mb-4 animate-float" style="animation-delay: 0.8s">
                            <i class="fa fa-desktop"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">软件安装与配置</h3>
                        <p class="text-gray-300 mb-4">专业安装各类软件，配置最佳使用环境。</p>
                        <a href="#contact" class="text-primary hover:underline inline-flex items-center hover-scale">
                            <span>免费咨询</span>
                            <i class="fa fa-arrow-right ml-2"></i>
                        </a>
                    </div>
                    
                    <!-- 服务卡片 6 -->
                    <div class="terminal-border rounded-lg p-6 hover:neon-border transition-all duration-500 transform hover:-translate-y-2 opacity-0 service-card" data-delay="600">
                        <div class="text-primary text-4xl mb-4 animate-float" style="animation-delay: 1s">
                            <i class="fa fa-comments"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">网络安全咨询</h3>
                        <p class="text-gray-300 mb-4">提供专业的网络安全建议和防护策略。</p>
                        <a href="#contact" class="text-primary hover:underline inline-flex items-center hover-scale">
                            <span>免费咨询</span>
                            <i class="fa fa-arrow-right ml-2"></i>
                        </a>
                    </div>
                </div>
            </div>
        </section>

        <!-- 技能区域 -->
        <section id="skills" class="py-20 bg-gradient-to-b from-dark to-dark/90">
            <div class="container mx-auto px-4">
                <h2 class="text-[clamp(1.5rem,5vw,2.5rem)] font-bold mb-16 text-center neon-text opacity-0" id="skills-title">
                    <span class="text-primary">专业技能</span>
                </h2>
                
                <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
                    <div class="opacity-0" id="tech-skills">
                        <h3 class="text-xl font-bold mb-6 text-primary">技术能力</h3>
                        
                        <div class="space-y-6">
                            <div>
                                <div class="flex justify-between mb-2">
                                    <span>系统安全</span>
                                    <span>95%</span>
                                </div>
                                <div class="w-full bg-gray-700 rounded-full h-2 overflow-hidden">
                                    <div class="bg-primary h-full rounded-full" style="width: 0%" id="security-bar"></div>
                                </div>
                            </div>
                            
                            <div>
                                <div class="flex justify-between mb-2">
                                    <span>网络攻防</span>
                                    <span>90%</span>
                                </div>
                                <div class="w-full bg-gray-700 rounded-full h-2 overflow-hidden">
                                    <div class="bg-primary h-full rounded-full" style="width: 0%" id="network-bar"></div>
                                </div>
                            </div>
                            
                            <div>
                                <div class="flex justify-between mb-2">
                                    <span>病毒查杀</span>
                                    <span>98%</span>
                                </div>
                                <div class="w-full bg-gray-700 rounded-full h-2 overflow-hidden">
                                    <div class="bg-primary h-full rounded-full" style="width: 0%" id="virus-bar"></div>
                                </div>
                            </div>
                            
                            <div>
                                <div class="flex justify-between mb-2">
                                    <span>数据恢复</span>
                                    <span>85%</span>
                                </div>
                                <div class="w-full bg-gray-700 rounded-full h-2 overflow-hidden">
                                    <div class="bg-primary h-full rounded-full" style="width: 0%" id="recovery-bar"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="opacity-0" id="service-skills">
                        <h3 class="text-xl font-bold mb-6 text-primary">服务优势</h3>
                        
                        <ul class="space-y-4">
                            <li class="flex items-start group">
                                <div class="text-primary mr-3 mt-1 transition-transform duration-300 group-hover:rotate-12">
                                    <i class="fa fa-check-circle"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold">免费咨询</h4>
                                    <p class="text-gray-300">提供专业的电脑问题咨询服务，不收取任何费用。</p>
                                </div>
                            </li>
                            
                            <li class="flex items-start group">
                                <div class="text-primary mr-3 mt-1 transition-transform duration-300 group-hover:rotate-12">
                                    <i class="fa fa-check-circle"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold">快速响应</h4>
                                    <p class="text-gray-300">24小时在线，快速响应您的需求。</p>
                                </div>
                            </li>
                            
                            <li class="flex items-start group">
                                <div class="text-primary mr-3 mt-1 transition-transform duration-300 group-hover:rotate-12">
                                    <i class="fa fa-check-circle"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold">远程协助</h4>
                                    <p class="text-gray-300">通过安全的远程协助工具，快速解决您的问题。</p>
                                </div>
                            </li>
                            
                            <li class="flex items-start group">
                                <div class="text-primary mr-3 mt-1 transition-transform duration-300 group-hover:rotate-12">
                                    <i class="fa fa-check-circle"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold">隐私保护</h4>
                                    <p class="text-gray-300">严格保护您的隐私，不泄露任何个人信息。</p>
                                </div>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <!-- 联系区域 -->
        <section id="contact" class="py-20 relative">
            <div class="container mx-auto px-4">
                <h2 class="text-[clamp(1.5rem,5vw,2.5rem)] font-bold mb-16 text-center neon-text opacity-0" id="contact-title">
                    <span class="text-primary">联系我</span>
                </h2>
                
                <div class="max-w-3xl mx-auto">
                    <div class="terminal-border rounded-lg p-8 glass-effect opacity-0 hover-neon-border transition-all duration-500" id="contact-card">
                        <h3 class="text-xl font-bold mb-6 text-primary">免费解决电脑问题</h3>
                        
                        <div class="mb-8">
                            <p class="mb-4">如果您遇到任何电脑问题，欢迎通过以下方式联系我，我将为您提供专业的解决方案。</p>
                            
                            <div class="flex items-center mb-4 group">
                                <div class="text-primary text-xl mr-4 transition-transform duration-300 group-hover:scale-125">
                                    <i class="fa fa-weixin"></i>
                                </div>
                                <div>
                                    <p class="font-bold">微信号</p>
                                    <div class="flex items-center">
                                        <span id="wechat-id" class="text-lg mr-4">XYAN0882</span>
                                        <button id="copy-btn" class="px-3 py-1 bg-primary text-dark rounded hover:bg-opacity-80 transition-all duration-300 transform hover:scale-105">
                                            <i class="fa fa-copy mr-1"></i> 复制
                                        </button>
                                        <span id="copy-success" class="ml-4 text-green-400 hidden">已复制!</span>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="flex items-center mb-4 group">
                                <div class="text-primary text-xl mr-4 transition-transform duration-300 group-hover:scale-125">
                                    <i class="fa fa-qq"></i>
                                </div>
                                <div>
                                    <p class="font-bold">QQ号</p>
                                    <p class="text-lg">2281450074</p>
                                </div>
                            </div>
                            
                            <div class="flex items-center group">
                                <div class="text-primary text-xl mr-4 transition-transform duration-300 group-hover:scale-125">
                                    <i class="fa fa-envelope"></i>
                                </div>
                                <div>
                                    <p class="font-bold">电子邮箱</p>
                                    <p class="text-lg">2281450074@qq.COM</p>
                                </div>
                            </div>
                        </div>
                        
                        <!-- 中国五星红旗图标 -->
                        <div class="text-center">
                            <div class="flag-wave inline-block">
                                <svg viewBox="0 0 300 200" width="300" height="200">
                                    <!-- 红色背景 -->
                                    <rect width="300" height="200" fill="#DE2910"/>
                                    
                                    <!-- 大五角星 -->
                                    <path d="M100,50 L110,65 L128,65 L113,75 L118,93 L100,83 L82,93 L87,75 L72,65 L90,65 Z" fill="#FFFF00"/>
                                    
                                    <!-- 四颗小五角星 -->
                                    <path d="M140,30 L144,37 L151,37 L146,41 L148,49 L140,45 L132,49 L134,41 L129,37 L136,37 Z" fill="#FFFF00"/>
                                    <path d="M150,45 L154,52 L161,52 L156,56 L158,64 L150,60 L142,64 L144,56 L139,52 L146,52 Z" fill="#FFFF00"/>
                                    <path d="M150,70 L154,77 L161,77 L156,81 L158,89 L150,85 L142,89 L144,81 L139,77 L146,77 Z" fill="#FFFF00"/>
                                    <path d="M140,90 L144,97 L151,97 L146,101 L148,109 L140,105 L132,109 L134,101 L129,97 L136,97 Z" fill="#FFFF00"/>
                                </svg>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 页脚 -->
        <footer class="py-8 bg-dark border-t border-primary/20">
            <div class="container mx-auto px-4">
                <div class="text-center">
                    <p class="text-gray-400 mb-4">© 2025 中国红客. 保留所有权利.</p>
                    <div class="flex justify-center space-x-6 mb-4">
                        <a href="#" class="text-primary hover:neon-text transition-all duration-300">
                            <i class="fa fa-weixin text-xl"></i>
                        </a>
                        <a href="#" class="text-primary hover:neon-text transition-all duration-300">
                            <i class="fa fa-qq text-xl"></i>
                        </a>
                        <a href="#" class="text-primary hover:neon-text transition-all duration-300">
                            <i class="fa fa-envelope text-xl"></i>
                        </a>
                    </div>
                    <p class="text-gray-500 text-sm">中国红客致力于提供专业的网络安全服务，保护您的数字资产安全。</p>
                </div>
            </div>
        </footer>
    </div>

    <!-- JavaScript -->
    <script>
        // 生成矩阵背景效果
        function createMatrix() {
            const container = document.getElementById('matrix-container');
            const canvas = document.createElement('canvas');
            container.appendChild(canvas);
            canvas.width = container.offsetWidth;
            canvas.height = container.offsetHeight;
            
            const ctx = canvas.getContext('2d');
            const letters = '0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ';
            const fontSize = 10;
            const columns = canvas.width / fontSize;
            const drops = [];
            
            for (let x = 0; x < columns; x++) {
                drops[x] = 1;
            }
            
            function draw() {
                ctx.fillStyle = 'rgba(0, 0, 0, 0.05)';
                ctx.fillRect(0, 0, canvas.width, canvas.height);
                
                ctx.fillStyle = '#00FF41';
                ctx.font = fontSize + 'px monospace';
                
                for (let i = 0; i < drops.length; i++) {
                    const text = letters.charAt(Math.floor(Math.random() * letters.length));
                    ctx.fillText(text, i * fontSize, drops[i] * fontSize);
                    
                    if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
                        drops[i] = 0;
                    }
                    
                    drops[i]++;
                }
            }
            
            setInterval(draw, 33);
        }
        
        // 页面加载完成后执行
        document.addEventListener('DOMContentLoaded', function() {
            // 创建矩阵背景
            createMatrix();
            
            // 初始化入场动画
            setTimeout(() => {
                document.getElementById('main-body').classList.add('opacity-100', 'transition-opacity', 'duration-1000');
                
                setTimeout(() => {
                    const heroCard = document.getElementById('hero-card');
                    heroCard.classList.add('opacity-100', 'translate-y-0', 'transition-all', 'duration-1000');
                    
                    setTimeout(() => {
                        document.getElementById('hero-title').classList.add('opacity-100');
                        
                        setTimeout(() => {
                            document.getElementById('hero-subtitle').classList.add('opacity-100', 'transition-opacity', 'duration-1000');
                            
                            setTimeout(() => {
                                document.getElementById('hero-buttons').classList.add('opacity-100', 'transition-opacity', 'duration-1000');
                                
                                // 显示导航栏
                                setTimeout(() => {
                                    document.getElementById('main-nav').classList.add('opacity-100', 'transition-opacity', 'duration-1000');
                                }, 500);
                            }, 500);
                        }, 1000);
                    }, 500);
                }, 500);
            }, 300);
            
            // 服务卡片动画
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        const delay = entry.target.getAttribute('data-delay') || 0;
                        setTimeout(() => {
                            entry.target.classList.add('opacity-100', 'transition-opacity', 'duration-700');
                        }, delay);
                    }
                });
            }, { threshold: 0.1 });
            
            document.querySelectorAll('.service-card').forEach(card => {
                observer.observe(card);
            });
            
            // 滚动动画
            const scrollElements = [
                document.getElementById('services-title'),
                document.getElementById('skills-title'),
                document.getElementById('contact-title'),
                document.getElementById('tech-skills'),
                document.getElementById('service-skills'),
                document.getElementById('contact-card')
            ];
            
            const scrollObserver = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('opacity-100', 'transition-opacity', 'duration-1000');
                        
                        // 技能条动画
                        if (entry.target.id === 'tech-skills') {
                            setTimeout(() => {
                                document.getElementById('security-bar').style.width = '95%';
                                document.getElementById('network-bar').style.width = '90%';
                                document.getElementById('virus-bar').style.width = '98%';
                                document.getElementById('recovery-bar').style.width = '85%';
                                
                                document.querySelectorAll('#tech-skills .bg-primary').forEach(bar => {
                                    bar.classList.add('transition-all', 'duration-1500');
                                });
                            }, 300);
                        }
                    }
                });
            }, { threshold: 0.2 });
            
            scrollElements.forEach(element => {
                if (element) {
                    scrollObserver.observe(element);
                }
            });
            
            // 移动端菜单切换
            document.getElementById('menu-toggle').addEventListener('click', function() {
                const mobileMenu = document.getElementById('mobile-menu');
                mobileMenu.classList.toggle('hidden');
            });
            
            // 平滑滚动
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    
                    const targetId = this.getAttribute('href');
                    const targetElement = document.querySelector(targetId);
                    
                    if (targetElement) {
                        window.scrollTo({
                            top: targetElement.offsetTop - 80,
                            behavior: 'smooth'
                        });
                        
                        // 关闭移动端菜单
                        document.getElementById('mobile-menu').classList.add('hidden');
                    }
                });
            });
            
            // 复制微信号功能
            document.getElementById('copy-btn').addEventListener('click', function() {
                const textToCopy = document.getElementById('wechat-id').textContent;
                navigator.clipboard.writeText(textToCopy)
                    .then(() => {
                        const successMsg = document.getElementById('copy-success');
                        successMsg.classList.remove('hidden');
                        
                        setTimeout(() => {
                            successMsg.classList.add('hidden');
                        }, 2000);
                    })
                    .catch(err => {
                        console.error('复制失败: ', err);
                    });
            });
            
            // 监听滚动事件，改变导航栏样式
            window.addEventListener('scroll', function() {
                const nav = document.getElementById('main-nav');
                if (window.scrollY > 100) {
                    nav.classList.add('py-2', 'transition-all', 'duration-300');
                    nav.classList.remove('py-3');
                } else {
                    nav.classList.add('py-3');
                    nav.classList.remove('py-2', 'transition-all', 'duration-300');
                }
            });
        });
    </script>
</body>
</html>    
