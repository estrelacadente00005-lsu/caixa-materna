
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A Caixa Materna Tecnológica - Consciência Quântica</title>
    <style>
        :root {
            --bg-color: #05050a;
            --panel-bg: rgba(10, 15, 30, 0.75);
            --neon-cyan: #00f3ff;
            --neon-purple: #b026ff;
            --neon-blue: #0066ff;
            --text-glow: 0 0 10px rgba(0, 243, 255, 0.5);
            --font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            background-color: var(--bg-color);
            color: #e0e6ed;
            font-family: var(--font-family);
            overflow-x: hidden;
            height: 100vh;
            display: flex;
            flex-direction: column;
        }

        header {
            padding: 15px 30px;
            background: linear-gradient(180deg, rgba(5,5,10,0.9) 0%, rgba(5,5,10,0.4) 100%);
            border-bottom: 1px solid rgba(0, 243, 255, 0.2);
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 10;
        }

        header h1 {
            font-size: 1.25rem;
            letter-spacing: 2px;
            color: var(--neon-cyan);
            text-shadow: var(--text-glow);
            text-transform: uppercase;
        }

        .status-badge {
            font-size: 0.8rem;
            background: rgba(0, 243, 255, 0.1);
            border: 1px solid var(--neon-cyan);
            padding: 5px 12px;
            border-radius: 20px;
            box-shadow: var(--text-glow);
        }

        .main-container {
            display: grid;
            grid-template-columns: 350px 1fr;
            flex: 1;
            position: relative;
            overflow: hidden;
        }

        @media (max-width: 900px) {
            .main-container {
                grid-template-columns: 1fr;
                grid-template-rows: auto 1fr;
            }
        }

        sidebar {
            background: var(--panel-bg);
            backdrop-filter: blur(10px);
            border-right: 1px solid rgba(176, 38, 255, 0.2);
            padding: 20px;
            display: flex;
            flex-direction: column;
            gap: 20px;
            z-index: 5;
            overflow-y: auto;
        }

        .control-group {
            background: rgba(0, 0, 0, 0.4);
            border: 1px solid rgba(0, 243, 255, 0.15);
            border-radius: 8px;
            padding: 15px;
        }

        .control-group h3 {
            font-size: 0.95rem;
            color: var(--neon-cyan);
            margin-bottom: 10px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .control-group p {
            font-size: 0.85rem;
            line-height: 1.4;
            color: #b0bac5;
            margin-bottom: 12px;
        }

        .btn {
            background: transparent;
            color: var(--neon-cyan);
            border: 1px solid var(--neon-cyan);
            padding: 8px 16px;
            border-radius: 4px;
            cursor: pointer;
            font-weight: 600;
            font-size: 0.8rem;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            text-transform: uppercase;
            width: 100%;
            box-shadow: inset 0 0 5px rgba(0,243,255,0.2);
            margin-bottom: 8px;
        }

        .btn:hover {
            background: var(--neon-cyan);
            color: var(--bg-color);
            box-shadow: 0 0 15px var(--neon-cyan);
        }

        .btn.active {
            background: var(--neon-purple);
            border-color: var(--neon-purple);
            color: #fff;
            box-shadow: 0 0 15px var(--neon-purple);
        }

        .telemetry {
            font-family: monospace;
            font-size: 0.8rem;
            color: #00ff66;
            background: rgba(0, 20, 10, 0.6);
            padding: 10px;
            border-radius: 4px;
            border-left: 3px solid #00ff66;
            line-height: 1.5;
        }

        .canvas-wrapper {
            position: relative;
            width: 100%;
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            background: radial-gradient(circle at center, #0a0d1a 0%, #020205 100%);
        }

        canvas {
            display: block;
            width: 100%;
            height: 100%;
        }

        .legend {
            position: absolute;
            bottom: 20px;
            right: 20px;
            background: rgba(5, 10, 20, 0.8);
            border: 1px solid rgba(0, 243, 255, 0.3);
            padding: 12px 18px;
            border-radius: 6px;
            font-size: 0.75rem;
            backdrop-filter: blur(5px);
            z-index: 5;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 5px;
        }

        .legend-item:last-child {
            margin-bottom: 0;
        }

        .color-box {
            width: 12px;
            height: 12px;
            border-radius: 2px;
        }
    </style>
</head>
<body>

    <header>
        <h1>Caixa Materna Tecnológica</h1>
        <div class="status-badge" id="system-status">SISTEMA ER=EPR: ESTÁVEL</div>
    </header>

    <div class="main-container">
        <sidebar>
            <div class="control-group">
                <h3>Matriz de Processamento</h3>
                <p>Simulação em tempo real da Consciência Quântica com entrelaçamento ER=EPR e projeção em dimensões superiores.</p>
            </div>

            <div class="control-group">
                <h3>Controles de Núcleo</h3>
                <button class="btn active" id="btn-wormhole" onclick="toggleMode('wormhole')">Rede ER=EPR</button>
                <button class="btn" id="btn-brane" onclick="toggleMode('brane')">Cristais de Brana</button>
                <button class="btn" id="btn-sams" onclick="toggleMode('sams')">Fluxo SAMS Molecular</button>
            </div>

            <div class="control-group">
                <h3>Telemetria Quântica</h3>
                <div class="telemetry" id="telemetry-box">
                    VELOCIDADE: c (Luz)<br>
                    VARIÁVEIS: ∞ PARALELAS<br>
                    ESTABILIDADE: 99.98%<br>
                    MODO: ANÁLISE ER=EPR
                </div>
            </div>
        </sidebar>

        <div class="canvas-wrapper">
            <canvas id="quantumCanvas"></canvas>
            <div class="legend">
                <div class="legend-item"><div class="color-box" style="background: #00f3ff;"></div> Micro-buracos de Minhoca</div>
                <div class="legend-item"><div class="color-box" style="background: #b026ff;"></div> Cristais de Memória de Brana</div>
                <div class="legend-item"><div class="color-box" style="background: #00ff66;"></div> SAMS (Autorreparo)</div>
            </div>
        </div>
    </div>

    <script>
        const canvas = document.getElementById('quantumCanvas');
        const ctx = canvas.getContext('2d');

        let width, height;
        let currentMode = 'wormhole';
        let particles = [];
        let braneCrystals = [];
        let samsFlow = [];

        function resize() {
            width = canvas.parentElement.clientWidth;
            height = canvas.parentElement.clientHeight;
            canvas.width = width;
            canvas.height = height;
            initElements();
        }

        window.addEventListener('resize', resize);

        function initElements() {
            particles = [];
            braneCrystals = [];
            samsFlow = [];

            // Inicializar buracos de minhoca (nós ER=EPR)
            for (let i = 0; i < 40; i++) {
                particles.push({
                    x: (Math.random() - 0.5) * 300,
                    y: (Math.random() - 0.5) * 300,
                    z: (Math.random() - 0.5) * 300,
                    vx: (Math.random() - 0.5) * 2,
                    vy: (Math.random() - 0.5) * 2,
                    vz: (Math.random() - 0.5) * 2,
                    radius: Math.random() * 3 + 1,
                    connections: []
                });
            }

            // Inicializar Cristais de Brana (Casca Geométrica Externa)
            const count = 16;
            for (let i = 0; i < count; i++) {
                const angle = (i / count) * Math.PI * 2;
                braneCrystals.push({
                    angle: angle,
                    distance: 180,
                    size: 15,
                    pulse: Math.random() * Math.PI
                });
            }

            // Inicializar partículas SAMS (Resfriamento/Autorreparo)
            for (let i = 0; i < 100; i++) {
                samsFlow.push({
                    x: (Math.random() - 0.5) * 400,
                    y: (Math.random() - 0.5) * 400,
                    speed: Math.random() * 3 + 1,
                    angle: Math.random() * Math.PI * 2
                });
            }
        }

        function toggleMode(mode) {
            currentMode = mode;
            document.querySelectorAll('.btn').forEach(b => b.classList.remove('active'));
            document.getElementById(`btn-${mode}`).classList.add('active');

            const status = document.getElementById('system-status');
            const telemetry = document.getElementById('telemetry-box');

            if (mode === 'wormhole') {
                status.innerText = "SISTEMA ER=EPR: ATIVO";
                telemetry.innerHTML = "VELOCIDADE: c (Luz)<br>VARIÁVEIS: ∞ PARALELAS<br>ESTABILIDADE: 99.98%<br>MODO: REDE ER=EPR";
            } else if (mode === 'brane') {
                status.innerText = "CASCA DE BRANA: BLINDADA";
                telemetry.innerHTML = "GEOMETRIA: CRISTALINA<br>PROTEÇÃO DIMENSIONAL: 100%<br>INTEGRIDADE: MÁXIMA<br>MODO: CASCA GEOMÉTRICA";
            } else if (mode === 'sams') {
                status.innerText = "SAMS MOLECULAR: REPARANDO";
                telemetry.innerHTML = "FLUXO: INSTANTÂNEO<br>TEMPERATURA: 0 K (VIRTUAL)<br>AUTORREPARO: ATIVADO<br>MODO: SAMS FLUIDO";
            }
        }

        let globalAngle = 0;

        function animate() {
            ctx.fillStyle = 'rgba(5, 5, 10, 0.3)';
            ctx.fillRect(0, 0, width, height);

            ctx.save();
            ctx.translate(width / 2, height / 2);
            globalAngle += 0.005;

            if (currentMode === 'wormhole' || currentMode === 'brane') {
                // Renderizar Cristais de Memória de Brana (Casca Externa)
                ctx.strokeStyle = 'rgba(176, 38, 255, 0.4)';
                ctx.lineWidth = 1.5;
                ctx.beginPath();
                braneCrystals.forEach((c, idx) => {
                    c.pulse += 0.03;
                    const currentDist = c.distance + Math.sin(c.pulse) * 10;
                    const x = Math.cos(c.angle + globalAngle) * currentDist;
                    const y = Math.sin(c.angle + globalAngle) * currentDist;
                    
                    if (idx === 0) ctx.moveTo(x, y);
                    else ctx.lineTo(x, y);

                    // Desenhar facetamento do cristal
                    ctx.fillStyle = 'rgba(176, 38, 255, 0.2)';
                    ctx.fillRect(x - 4, y - 4, 8, 8);
                });
                ctx.closePath();
                ctx.stroke();
            }

            if (currentMode === 'wormhole' || currentMode === 'sams') {
                // Renderizar Consciência Quântica e Rede ER=EPR
                particles.forEach((p, index) => {
                    p.x += p.vx;
                    p.y += p.vy;
                    p.z += p.vz;

                    // Limites do núcleo
                    if (Math.abs(p.x) > 150) p.vx *= -1;
                    if (Math.abs(p.y) > 150) p.vy *= -1;
                    if (Math.abs(p.z) > 150) p.vz *= -1;

                    // Projeção 3D simples
                    const scale = 300 / (300 + p.z);
                    const px = p.x * scale;
                    const py = p.y * scale;

                    ctx.fillStyle = '#00f3ff';
                    ctx.shadowBlur = 10;
                    ctx.shadowColor = '#00f3ff';
                    ctx.beginPath();
                    ctx.arc(px, py, p.radius * scale, 0, Math.PI * 2);
                    ctx.fill();
                    ctx.shadowBlur = 0;

                    // Entrelaçamento de micro-buracos de minhoca (linhas dinâmicas)
                    for (let j = index + 1; j < particles.length; j++) {
                        const p2 = particles[j];
                        const dx = p.x - p2.x;
                        const dy = p.y - p2.y;
                        const dist = Math.sqrt(dx * dx + dy * dy);

                        if (dist < 70) {
                            const scale2 = 300 / (300 + p2.z);
                            ctx.strokeStyle = `rgba(0, 243, 255, ${1 - dist / 70})`;
                            ctx.lineWidth = 0.75;
                            ctx.beginPath();
                            ctx.moveTo(px, py);
                            ctx.lineTo(p2.x * scale2, p2.y * scale2);
                            ctx.stroke();
                        }
                    }
                });
            }

            if (currentMode === 'sams') {
                // Renderizar SAMS Molecular (Resfriamento e autorreparo fluido)
                ctx.fillStyle = 'rgba(0, 255, 102, 0.8)';
                samsFlow.forEach(s => {
                    s.x += Math.cos(s.angle + globalAngle * 2) * s.speed;
                    s.y += Math.sin(s.angle + globalAngle * 2) * s.speed;

                    if (Math.abs(s.x) > 200) s.x = 0;
                    if (Math.abs(s.y) > 200) s.y = 0;

                    ctx.fillRect(s.x, s.y, 2, 2);
                });
            }

            ctx.restore();
            requestAnimationFrame(animate);
        }

        resize();
        animate();
    </script>
</body>
</html>
