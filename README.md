# HACKER
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
                        terminal: '#05FF00'
                    },
                    fontFamily: {
                        matrix: ['Courier New', 'monospace']
                    },
                    animation: {
                        'pulse-slow': 'pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                        'glow': 'glow 2s ease-in-out infinite alternate',
                        'matrix': 'matrix 10s linear infinite'
                    },
                    keyframes: {
                        glow: {
                            '0%': { 'text-shadow': '0 0 5px #fff, 0 0 10px #fff, 0 0 15px #00FF41, 0 0 20px #00FF41' },
                            '100%': { 'text-shadow': '0 0 10px #fff, 0 0 20px #fff, 0 0 30px #00FF41, 0 0 40px #00FF41' }
                        },
                        matrix: {
                            '0%': { 'background-position': '0 0' },
                            '100%': { 'background-position': '0 -2000px' }
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
        }
    </style>
</head>
<body class="bg-dark text-terminal font-matrix min-h-screen overflow-x-hidden">
    <!-- 背景矩阵效果容器 -->
    <div id="matrix-container" class="fixed inset-0 z-0 pointer-events-none"></div>

    <!-- 内容容器 -->
    <div class="relative z-10">
        <!-- 顶部导航 -->
        <nav class="fixed top-0 w-full z-50 glass-effect">
            <div class="container mx-auto px-4 py-3 flex justify-between items-center">
                <div class="text-primary text-2xl font-bold neon-text">CHINA HACKER</div>
                <div class="hidden md:flex space-x-8">
                    <a href="#home" class="hover:text-primary transition-colors duration-300">首页</a>
                    <a href="#services" class="hover:text-primary transition-colors duration-300">服务</a>
                    <a href="#skills" class="hover:text-primary transition-colors duration-300">技能</a>
                    <a href="#contact" class="hover:text-primary transition-colors duration-300">联系我</a>
                </div>
                <div class="md:hidden">
                    <button id="menu-toggle" class="text-primary">
                        <i class="fa fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
            <!-- 移动端菜单 -->
            <div id="mobile-menu" class="hidden md:hidden glass-effect">
                <div class="container mx-auto px-4 py-3 flex flex-col space-y-4">
                    <a href="#home" class="hover:text-primary transition-colors duration-300">首页</a>
                    <a href="#services" class="hover:text-primary transition-colors duration-300">服务</a>
                    <a href="#skills" class="hover:text-primary transition-colors duration-300">技能</a>
                    <a href="#contact" class="hover:text-primary transition-colors duration-300">联系我</a>
                </div>
            </div>
        </nav>

        <!-- 英雄区域 -->
        <section id="home" class="min-h-screen flex items-center justify-center relative pt-20">
            <div class="absolute inset-0 flex items-center justify-center">
                <div class="text-[150px] font-bold text-primary/10 opacity-20">HACKER</div>
            </div>
            <div class="container mx-auto px-4 z-10">
                <div class="max-w-4xl mx-auto text-center">
                    <div class="terminal-border rounded-lg p-8 relative overflow-hidden">
                        <div class="absolute top-0 right-0 m-2 flex space-x-2">
                            <div class="w-3 h-3 rounded-full bg-red-500"></div>
                            <div class="w-3 h-3 rounded-full bg-yellow-500"></div>
                            <div class="w-3 h-3 rounded-full bg-green-500"></div>
                        </div>
                        <h1 class="text-[clamp(2rem,5vw,4rem)] font-bold mb-6 neon-text animate-glow">
                            <span class="text-primary">中国红客</span>
                        </h1>
                        <p class="text-[clamp(1rem,2vw,1.5rem)] mb-8 leading-relaxed">
                            网络安全专家 | 免费电脑问题解决方案
                        </p>
                        <div class="flex justify-center space-x-4">
                            <a href="#services" class="px-6 py-3 border border-primary text-primary hover:bg-primary hover:text-dark transition-all duration-300 rounded-md">
                                了解服务
                            </a>
                            <a href="#contact" class="px-6 py-3 bg-primary text-dark hover:bg-opacity-80 transition-all duration-300 rounded-md">
                                联系我
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 服务区域 -->
        <section id="services" class="py-20 relative">
            <div class="container mx-auto px-4">
                <h2 class="text-[clamp(1.5rem,3vw,2.5rem)] font-bold mb-16 text-center neon-text">
                    <span class="text-primary">我的服务</span>
                </h2>
                
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- 服务卡片 1 -->
                    <div class="terminal-border rounded-lg p-6 hover:neon-border transition-all duration-500 transform hover:-translate-y-2">
                        <div class="text-primary text-4xl mb-4">
                            <i class="fa fa-shield"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">系统安全检测</h3>
                        <p class="text-gray-300 mb-4">全面扫描系统漏洞，检测恶意软件，保障你的电脑安全。</p>
                        <a href="#contact" class="text-primary hover:underline inline-flex items-center">
                            <span>免费咨询</span>
                            <i class="fa fa-arrow-right ml-2"></i>
                        </a>
                    </div>
                    
                    <!-- 服务卡片 2 -->
                    <div class="terminal-border rounded-lg p-6 hover:neon-border transition-all duration-500 transform hover:-translate-y-2">
                        <div class="text-primary text-4xl mb-4">
                            <i class="fa fa-wrench"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">系统故障修复</h3>
                        <p class="text-gray-300 mb-4">解决系统崩溃、蓝屏、启动问题等各类软硬件故障。</p>
                        <a href="#contact" class="text-primary hover:underline inline-flex items-center">
                            <span>免费咨询</span>
                            <i class="fa fa-arrow-right ml-2"></i>
                        </a>
                    </div>
                    
                    <!-- 服务卡片 3 -->
                    <div class="terminal-border rounded-lg p-6 hover:neon-border transition-all duration-500 transform hover:-translate-y-2">
                        <div class="text-primary text-4xl mb-4">
                            <i class="fa fa-bolt"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">系统优化加速</h3>
                        <p class="text-gray-300 mb-4">清理系统垃圾，优化系统配置，提升电脑运行速度。</p>
                        <a href="#contact" class="text-primary hover:underline inline-flex items-center">
                            <span>免费咨询</span>
                            <i class="fa fa-arrow-right ml-2"></i>
                        </a>
                    </div>
                    
                    <!-- 服务卡片 4 -->
                    <div class="terminal-border rounded-lg p-6 hover:neon-border transition-all duration-500 transform hover:-translate-y-2">
                        <div class="text-primary text-4xl mb-4">
                            <i class="fa fa-lock"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">数据恢复与加密</h3>
                        <p class="text-gray-300 mb-4">恢复丢失的数据，并提供安全的数据加密解决方案。</p>
                        <a href="#contact" class="text-primary hover:underline inline-flex items-center">
                            <span>免费咨询</span>
                            <i class="fa fa-arrow-right ml-2"></i>
                        </a>
                    </div>
                    
                    <!-- 服务卡片 5 -->
                    <div class="terminal-border rounded-lg p-6 hover:neon-border transition-all duration-500 transform hover:-translate-y-2">
                        <div class="text-primary text-4xl mb-4">
                            <i class="fa fa-desktop"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">软件安装与配置</h3>
                        <p class="text-gray-300 mb-4">专业安装各类软件，配置最佳使用环境。</p>
                        <a href="#contact" class="text-primary hover:underline inline-flex items-center">
                            <span>免费咨询</span>
                            <i class="fa fa-arrow-right ml-2"></i>
                        </a>
                    </div>
                    
                    <!-- 服务卡片 6 -->
                    <div class="terminal-border rounded-lg p-6 hover:neon-border transition-all duration-500 transform hover:-translate-y-2">
                        <div class="text-primary text-4xl mb-4">
                            <i class="fa fa-comments"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">网络安全咨询</h3>
                        <p class="text-gray-300 mb-4">提供专业的网络安全建议和防护策略。</p>
                        <a href="#contact" class="text-primary hover:underline inline-flex items-center">
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
                <h2 class="text-[clamp(1.5rem,3vw,2.5rem)] font-bold mb-16 text-center neon-text">
                    <span class="text-primary">专业技能</span>
                </h2>
                
                <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
                    <div>
                        <h3 class="text-xl font-bold mb-6 text-primary">技术能力</h3>
                        
                        <div class="space-y-6">
                            <div>
                                <div class="flex justify-between mb-2">
                                    <span>系统安全</span>
                                    <span>95%</span>
                                </div>
                                <div class="w-full bg-gray-700 rounded-full h-2">
                                    <div class="bg-primary h-2 rounded-full" style="width: 95%"></div>
                                </div>
                            </div>
                            
                            <div>
                                <div class="flex justify-between mb-2">
                                    <span>网络攻防</span>
                                    <span>90%</span>
                                </div>
                                <div class="w-full bg-gray-700 rounded-full h-2">
                                    <div class="bg-primary h-2 rounded-full" style="width: 90%"></div>
                                </div>
                            </div>
                            
                            <div>
                                <div class="flex justify-between mb-2">
                                    <span>病毒查杀</span>
                                    <span>98%</span>
                                </div>
                                <div class="w-full bg-gray-700 rounded-full h-2">
                                    <div class="bg-primary h-2 rounded-full" style="width: 98%"></div>
                                </div>
                            </div>
                            
                            <div>
                                <div class="flex justify-between mb-2">
                                    <span>数据恢复</span>
                                    <span>85%</span>
                                </div>
                                <div class="w-full bg-gray-700 rounded-full h-2">
                                    <div class="bg-primary h-2 rounded-full" style="width: 85%"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div>
                        <h3 class="text-xl font-bold mb-6 text-primary">服务优势</h3>
                        
                        <ul class="space-y-4">
                            <li class="flex items-start">
                                <div class="text-primary mr-3 mt-1">
                                    <i class="fa fa-check-circle"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold">免费咨询</h4>
                                    <p class="text-gray-300">提供专业的电脑问题咨询服务，不收取任何费用。</p>
                                </div>
                            </li>
                            
                            <li class="flex items-start">
                                <div class="text-primary mr-3 mt-1">
                                    <i class="fa fa-check-circle"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold">快速响应</h4>
                                    <p class="text-gray-300">24小时在线，快速响应您的需求。</p>
                                </div>
                            </li>
                            
                            <li class="flex items-start">
                                <div class="text-primary mr-3 mt-1">
                                    <i class="fa fa-check-circle"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold">远程协助</h4>
                                    <p class="text-gray-300">通过安全的远程协助工具，快速解决您的问题。</p>
                                </div>
                            </li>
                            
                            <li class="flex items-start">
                                <div class="text-primary mr-3 mt-1">
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
                <h2 class="text-[clamp(1.5rem,3vw,2.5rem)] font-bold mb-16 text-center neon-text">
                    <span class="text-primary">联系我</span>
                </h2>
                
                <div class="max-w-3xl mx-auto">
                    <div class="terminal-border rounded-lg p-8 glass-effect">
                        <h3 class="text-xl font-bold mb-6 text-primary">免费解决电脑问题</h3>
                        
                        <div class="mb-8">
                            <p class="mb-4">如果您遇到任何电脑问题，欢迎通过以下方式联系我，我将为您提供专业的解决方案。</p>
                            
                            <div class="flex items-center mb-4">
                                <div class="text-primary text-xl mr-4">
                                    <i class="fa fa-weixin"></i>
                                </div>
                                <div>
                                    <p class="font-bold">微信号</p>
                                    <div class="flex items-center">
                                        <span id="wechat-id" class="text-lg mr-4">XYAN0882</span>
                                        <button id="copy-btn" class="px-3 py-1 bg-primary text-dark rounded hover:bg-opacity-80 transition-colors duration-300">
                                            <i class="fa fa-copy mr-1"></i> 复制
                                        </button>
                                        <span id="copy-success" class="ml-4 text-green-400 hidden">已复制!</span>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="flex items-center">
                                <div class="text-primary text-xl mr-4">
                                    <i class="fa fa-comments"></i>
                                </div>
                                <div>
                                    <p class="font-bold">在线咨询</p>
                                    <p>扫描下方二维码添加微信，随时为您解答问题</p>
                                </div>
                            </div>
                        </div>
                        
                        <div class="text-center">
                            <div class="inline-block p-2 bg-white rounded-lg">
                                <img src="https://picsum.photos/200/200" alt="微信二维码" class="w-48 h-48">
                            </div>
                            <p class="mt-4 text-sm text-gray-400">扫描二维码添加微信</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 页脚 -->
        <footer class="py-8 border-t border-primary/20">
            <div class="container mx-auto px-4">
                <div class="text-center">
                    <p class="text-gray-400">© 2025 中国红客 | 网络安全专家</p>
                    <p class="text-sm text-gray-500 mt-2">仅用于技术交流，遵守中国法律法规</p>
                </div>
            </div>
        </footer>

        <!-- 终端效果 -->
        <div id="terminal" class="fixed bottom-0 left-0 w-full bg-dark/90 border-t border-primary/30 p-4 z-50 hidden">
            <div class="flex items-center mb-2">
                <span class="text-primary mr-2">root@china-hacker:~$</span>
                <input type="text" id="terminal-input" class="bg-transparent border-none outline-none text-terminal w-full" placeholder="输入命令...">
            </div>
            <div id="terminal-output" class="text-sm text-gray-300 max-h-40 overflow-y-auto"></div>
        </div>
    </div>

    <!-- JavaScript -->
    <script>
        // 移动端菜单切换
        document.getElementById('menu-toggle').addEventListener('click', function() {
            const mobileMenu = document.getElementById('mobile-menu');
            mobileMenu.classList.toggle('hidden');
        });

        // 平滑滚动
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
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
            const wechatId = document.getElementById('wechat-id').textContent;
            navigator.clipboard.writeText(wechatId).then(function() {
                const copySuccess = document.getElementById('copy-success');
                copySuccess.classList.remove('hidden');
                setTimeout(() => {
                    copySuccess.classList.add('hidden');
                }, 2000);
            });
        });

        // 终端效果
        const terminal = document.getElementById('terminal');
        const terminalInput = document.getElementById('terminal-input');
        const terminalOutput = document.getElementById('terminal-output');
        
        // 双击页面任何位置显示终端
        document.addEventListener('dblclick', function() {
            terminal.classList.toggle('hidden');
            if (!terminal.classList.contains('hidden')) {
                terminalInput.focus();
            }
        });
        
        // 终端命令处理
        terminalInput.addEventListener('keydown', function(e) {
            if (e.key === 'Enter') {
                const command = this.value.trim();
                addToTerminal(command);
                processCommand(command);
                this.value = '';
            }
        });
        
        function addToTerminal(text, isOutput = false) {
            const line = document.createElement('div');
            line.textContent = isOutput ? '> ' + text : 'root@china-hacker:~$ ' + text;
            line.className = isOutput ? 'text-green-400' : 'text-primary';
            terminalOutput.appendChild(line);
            terminalOutput.scrollTop = terminalOutput.scrollHeight;
        }
        
        function processCommand(command) {
            switch(command.toLowerCase()) {
                case 'help':
                    addToTerminal('可用命令: help, about, services, contact, clear', true);
                    break;
                case 'about':
                    addToTerminal('我是一名中国红客，专注于网络安全和电脑问题解决。', true);
                    addToTerminal('提供免费的电脑问题咨询和解决方案。', true);
                    break;
                case 'services':
                    addToTerminal('我的服务包括: 系统安全检测、故障修复、系统优化、数据恢复、软件安装配置和网络安全咨询。', true);
                    break;
                case 'contact':
                    addToTerminal('联系我: 微信号 XYAN0882', true);
                    break;
                case 'clear':
                    terminalOutput.innerHTML = '';
                    break;
                default:
                    addToTerminal(`命令未找到: ${command}。输入 'help' 获取可用命令列表。`, true);
            }
        }

        // 随机矩阵效果
        function createMatrixEffect() {
            const container = document.getElementById('matrix-container');
            const canvas = document.createElement('canvas');
            container.appendChild(canvas);
            canvas.style.width = '100%';
            canvas.style.height = '100%';
            
            const ctx = canvas.getContext('2d');
            let width, height;
            let matrix = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789@#$%^&*()_+{}:"<>?';
            matrix = matrix.split('');
            
            function resize() {
                width = container.clientWidth;
                height = container.clientHeight;
                canvas.width = width;
                canvas.height = height;
            }
            
            resize();
            window.addEventListener('resize', resize);
            
            const fontSize = 10;
            const columns = width / fontSize;
            const drops = [];
            
            for(let x = 0; x < columns; x++) {
                drops[x] = 1;
            }
            
            function draw() {
                ctx.fillStyle = 'rgba(0, 0, 0, 0.05)';
                ctx.fillRect(0, 0, width, height);
                
                ctx.fillStyle = '#00FF41';
                ctx.font = fontSize + 'px monospace';
                
                for(let i = 0; i < drops.length; i++) {
                    const text = matrix[Math.floor(Math.random() * matrix.length)];
                    ctx.fillText(text, i * fontSize, drops[i] * fontSize);
                    
                    if(drops[i] * fontSize > height && Math.random() > 0.975) {
                        drops[i] = 0;
                    }
                    
                    drops[i]++;
                }
            }
            
            setInterval(draw, 33);
        }
        
        // 页面加载完成后创建矩阵效果
        window.addEventListener('load', createMatrixEffect);
    </script>
</body>
</html>
    
