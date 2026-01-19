<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IMPÉRIO CITY | PROTOCOLO GÊNESE</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Rajdhani:wght@300;500;700&display=swap" rel="stylesheet">
    <style>
        /* --- CSS (ESTILO) --- */
        :root {
            --p: #bc00ff; /* Roxo Neon */
            --y: #ffee00; /* Amarelo Elétrico */
            --dark: #030008;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; cursor: crosshair; }

        body {
            background: var(--dark);
            color: #e0e0e0;
            font-family: 'Rajdhani', sans-serif;
            line-height: 1.4;
            overflow-x: hidden;
        }

        /* Fundo de Grade e Partículas */
        .bg-effects { position: fixed; inset: 0; z-index: -1; opacity: 0.4; }
        .grid { 
            position: absolute; inset: 0; 
            background-image: linear-gradient(#1a0033 1px, transparent 1px), linear-gradient(90deg, #1a0033 1px, transparent 1px); 
            background-size: 30px 30px; 
        }

        /* Loader */
        #loader {
            position: fixed; inset: 0; background: var(--dark); z-index: 1000;
            display: flex; flex-direction: column; align-items: center; justify-content: center;
            transition: opacity 1s ease;
        }
        .spinner {
            width: 40px; height: 40px; border: 3px solid var(--p);
            border-top-color: var(--y); border-radius: 50%;
            animation: spin 1s infinite linear;
        }
        @keyframes spin { to { transform: rotate(360deg); } }
        .loader-text {
            color: var(--p); font-family: 'Orbitron'; font-size: 0.9rem; margin-top: 15px;
            animation: pulse-text 1.5s infinite alternate;
        }
        @keyframes pulse-text { 0% { opacity: 0.5; } 100% { opacity: 1; } }

        /* Título H1 Roxo Neon */
        .hero { min-height: 80vh; display: flex; flex-direction: column; align-items: center; justify-content: center; padding: 40px 20px; }
        .glitch {
            font-family: 'Orbitron'; font-size: 3.5rem; 
            color: var(--p); 
            text-shadow: 0 0 10px var(--p), 0 0 20px var(--p), 0 0 5px var(--y);
            letter-spacing: 8px; text-transform: uppercase;
            animation: glitch-effect 1.5s infinite alternate;
            text-align: center;
        }
        @keyframes glitch-effect {
            0% { transform: translate(0); }
            20% { transform: translate(-2px, 1px); text-shadow: 2px 0 var(--y); }
            40% { transform: translate(2px, -1px); }
            100% { transform: translate(0); }
        }

        .status-box { color: var(--y); font-size: 0.8rem; letter-spacing: 2px; margin-top: 10px; }
        .pulse { display: inline-block; width: 8px; height: 8px; background: var(--y); border-radius: 50%; margin-right: 8px; animation: status-pulse 1.5s infinite; }
        @keyframes status-pulse { 0% { box-shadow: 0 0 0 0px rgba(255, 238, 0, 0.7); } 100% { box-shadow: 0 0 0 10px rgba(255, 238, 0, 0); } }

        .bio-panel {
            background: rgba(188, 0, 255, 0.05); border: 1px solid rgba(188, 0, 255, 0.3);
            padding: 15px 25px; max-width: 500px; margin-top: 20px; font-size: 0.9rem; color: #aaa; text-align: center;
        }

        /* Painel de Mensagem dos Donos */
        .dev-message-panel {
            background: rgba(255, 255, 255, 0.01); backdrop-filter: blur(5px);
            border: 1px solid var(--y); padding: 20px 30px; max-width: 600px; margin-top: 40px;
            clip-path: polygon(5% 0, 100% 0, 95% 100%, 0 100%);
            box-shadow: 0 0 20px rgba(255, 238, 0, 0.05);
        }
        .dev-tag { font-family: 'Orbitron'; color: var(--p); font-size: 0.7rem; text-align: right; border-bottom: 1px solid rgba(188, 0, 255, 0.2); margin-bottom: 10px; }
        .dev-message { color: #fff; font-size: 0.85rem; line-height: 1.6; text-align: left; min-height: 50px; }

        /* Container e Cards */
        .container { max-width: 900px; margin: 0 auto; padding: 0 20px; }
        .section-title { font-family: 'Orbitron'; font-size: 1.2rem; color: var(--y); margin: 60px 0 30px; text-align: center; text-transform: uppercase; }

        .nav-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 15px; }
        .cyber-card {
            background: rgba(255, 255, 255, 0.02); border: 1px solid rgba(188, 0, 255, 0.2);
            padding: 25px; text-align: center; text-decoration: none; color: white; transition: 0.3s;
        }
        .cyber-card:hover { border-color: var(--y); background: rgba(188, 0, 255, 0.08); transform: translateY(-5px); }
        .cyber-card h2 { font-family: 'Orbitron'; font-size: 1rem; color: var(--y); }

        /* Regras Estilo Terminal */
        .rules-box { background: rgba(0, 0, 0, 0.5); border: 1px solid #1a1a1a; font-size: 0.85rem; margin-bottom: 50px; }
        .rule-line { padding: 12px; border-bottom: 1px dashed #1a0033; display: flex; gap: 10px; }
        .rule-line b { color: var(--y); }

        /* Footer / IB Decorado */
        .footer-module { margin-top: 80px; padding: 60px 20px; text-align: center; }
        .auth-card {
            display: inline-block; background: #000; border: 1px solid var(--p); padding: 1px;
            clip-path: polygon(5% 0, 100% 0, 95% 100%, 0 100%);
        }
        .auth-header { background: var(--p); color: #000; font-family: 'Orbitron'; font-size: 0.7rem; padding: 5px 30px; font-weight: bold; }
        .auth-body { padding: 25px 40px; }
        .ib-name, .dev-name { font-family: 'Orbitron'; font-size: 1rem; color: var(--y); text-shadow: 0 0 8px var(--y); }
        .divider { height: 1px; background: rgba(188, 0, 255, 0.3); margin: 15px auto; width: 50%; }
        small { font-size: 0.6rem; color: #888; text-transform: uppercase; letter-spacing: 2px; }

        @media (max-width: 600px) { .glitch { font-size: 2rem; } }
    </style>
</head>
<body>

    <div id="loader">
        <div class="spinner"></div>
        <div class="loader-text">SYNCING_IMPÉRIO_SYSTEMS...</div>
    </div>

    <div class="bg-effects">
        <div class="grid"></div>
        <canvas id="particle-canvas"></canvas>
    </div>

    <main class="content">
        <header class="hero">
            <h1 class="glitch" data-text="IMPÉRIO CITY">IMPÉRIO CITY</h1>
            <div class="status-box">
                <span class="pulse"></span> STATUS: OPERACIONAL // USER: ITZ_LOIRIN12344
            </div>
            
            <div class="bio-panel">
                <p id="type-text">></p>
            </div>

            <div class="dev-message-panel">
                <div class="dev-tag">[TRANSMISSÃO_ADMIN_LOG]</div>
                <p class="dev-message" id="dev-msg-content"></p>
            </div>
        </header>

        <div class="container">
            <h2 class="section-title">TERMINAIS DE ACESSO</h2>
            <div class="nav-grid">
                <a href="https://discord.gg/rFCVAYKp" target="_blank" class="cyber-card">
                    <h2>DISCORD</h2>
                    <span style="font-size: 0.7rem; color: var(--p);">CONECTAR_ESTAÇÃO</span>
                </a>
                <a href="https://www.tiktok.com/@imprio.city1?_r=1&_t=ZS-93CoXd1Gpgj" target="_blank" class="cyber-card">
                    <h2>TIKTOK</h2>
                    <span style="font-size: 0.7rem; color: var(--p);">ACESSAR_DADOS_VISUAIS</span>
                </a>
            </div>

            <h2 class="section-title">PROTOCOLOS DE REDE (REGRAS)</h2>
            <div class="rules-box" id="rules-list"></div>
        </div>

        <footer class="footer-module">
            <div class="auth-card">
                <div class="auth-header">REGISTRO DE AUTENTICAÇÃO</div>
                <div class="auth-body">
                    <small>IB / INSPIRAÇÃO:</small>
                    <div class="ib-name">mini dogge-LOGAM-KING_DOUGH618</div>
                    <div class="divider"></div>
                    <small>MASTER DEVELOPER:</small>
                    <div class="dev-name">itz_loirin12344</div>
                </div>
            </div>
            <div style="margin-top: 30px; font-size: 0.7rem; color: var(--p); letter-spacing: 2px;">👑 RESPEITO • ORGANIZAÇÃO • RP REAL 👑</div>
        </footer>
    </main>

    <script>
        /* --- JAVASCRIPT --- */
        document.addEventListener('DOMContentLoaded', () => {
            // Loader
            setTimeout(() => {
                document.getElementById('loader').style.opacity = '0';
                setTimeout(() => document.getElementById('loader').remove(), 1000);
            }, 2000);

            // Digitação da Bio
            const bioText = "ESTABELECENDO ACESSO AO NÚCLEO... BEM-VINDO AO FUTURO DO ROLEPLAY BRASILEIRO. REGRAS CARREGADAS.";
            let bioIdx = 0;
            function typeBio() {
                if (bioIdx < bioText.length) {
                    document.getElementById('type-text').innerHTML += bioText.charAt(bioIdx);
                    bioIdx++;
                    setTimeout(typeBio, 40);
                }
            }
            setTimeout(typeBio, 2500);

            // Digitação Mensagem dos Donos
            const devMessage = "MENSAGEM_ADMIN: NOSSO OBJETIVO É CONSTRUIR UMA COMUNIDADE FORTE E UM RP INOVADOR. ESTE PORTAL É O INÍCIO DA NOSSA ERA DIGITAL. CONTE CONOSCO. ATENC.: ITZ_LOIRIN12344.";
            let devIdx = 0;
            function typeDev() {
                if (devIdx < devMessage.length) {
                    document.getElementById('dev-msg-content').innerHTML += devMessage.charAt(devIdx);
                    devIdx++;
                    setTimeout(typeDev, 35);
                }
            }
            setTimeout(typeDev, 6000);

            // Regras
            const regras = [
                "Respeito acima de tudo - Proibido xingar ou discriminar.",
                "Proibido conteúdo impróprio (+18, Gore, Racismo).",
                "Sem spam ou flood de mensagens e emojis.",
                "Sem divulgação externa sem permissão da staff.",
                "Respeite as decisões da hierarquia Staff.",
                "RP sério obrigatório - Anti-RP resulta em punição.",
                "Uso correto de todos os canais de texto e voz.",
                "Nickname e foto adequados para o ambiente.",
                "Zero tolerância para Hacks e Exploits.",
                "Denúncias apenas com provas em vídeo ou print."
            ];
            const rList = document.getElementById('rules-list');
            regras.forEach((r, i) => {
                const line = document.createElement('div');
                line.className = 'rule-line';
                line.innerHTML = `<b>[${String(i+1).padStart(2, '0')}]</b> ${r}`;
                rList.appendChild(line);
            });

            // Canvas Partículas
            const canvas = document.getElementById('particle-canvas');
            const ctx = canvas.getContext('2d');
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
            let particles = [];
            class Particle {
                constructor() {
                    this.x = Math.random() * canvas.width;
                    this.y = Math.random() * canvas.height;
                    this.speed = Math.random() * 0.5 + 0.1;
                }
                update() {
                    this.y -= this.speed;
                    if (this.y < 0) this.y = canvas.height;
                }
                draw() {
                    ctx.fillStyle = "rgba(188, 0, 255, 0.3)";
                    ctx.fillRect(this.x, this.y, 1.5, 1.5);
                }
            }
            for(let i=0; i<100; i++) particles.push(new Particle());
            function animate() {
                ctx.clearRect(0,0, canvas.width, canvas.height);
                particles.forEach(p => { p.update(); p.draw(); });
                requestAnimationFrame(animate);
            }
            animate();
        });
    </script>
</body>
</html>
