<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI 時代物流行銷 vs 傳統行銷 | 典範轉移報告</title>
    <style>
        /* Retro-Futuristic Cyberpunk Theme */
        @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Noto+Sans+TC:wght@300;500;700&display=swap');

        :root {
            --bg-color: #0a0b10;
            --panel-bg: #121420;
            --neon-cyan: #00f0ff;
            --neon-magenta: #ff007f;
            --neon-green: #39ff14;
            --text-main: #e0e6ed;
            --text-dim: #8892b0;
            --grid-color: rgba(0, 240, 255, 0.03);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-main);
            font-family: 'Noto Sans TC', sans-serif;
            background-image: 
                linear-gradient(var(--grid-color) 1px, transparent 1px),
                linear-gradient(90deg, var(--grid-color) 1px, transparent 1px);
            background-size: 20px 20px;
            padding: 40px 20px;
            line-height: 1.6;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
        }

        /* Header Style */
        header {
            text-align: center;
            margin-bottom: 60px;
            border-bottom: 2px solid var(--neon-cyan);
            padding-bottom: 30px;
            position: relative;
            box-shadow: 0 10px 20px rgba(0, 240, 255, 0.1);
        }

        header::after {
            content: 'SYSTEM STATUS: ACTIVE';
            position: absolute;
            bottom: -25px;
            right: 10px;
            font-family: 'Orbitron', sans-serif;
            font-size: 0.75rem;
            color: var(--neon-green);
            letter-spacing: 2px;
        }

        h1 {
            font-family: 'Orbitron', 'Noto Sans TC', sans-serif;
            font-size: 2.5rem;
            color: #fff;
            text-shadow: 0 0 10px var(--neon-cyan), 0 0 20px var(--neon-cyan);
            margin-bottom: 15px;
            letter-spacing: 2px;
        }

        .subtitle {
            font-size: 1.1rem;
            color: var(--neon-magenta);
            font-family: 'Orbitron', sans-serif;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Core Philosophy Panel */
        .intro-panel {
            background: var(--panel-bg);
            border-left: 4px solid var(--neon-magenta);
            padding: 25px;
            margin-bottom: 40px;
            border-radius: 0 8px 8px 0;
            box-shadow: 5px 5px 15px rgba(0,0,0,0.5);
        }

        .intro-panel h2 {
            color: var(--neon-cyan);
            font-size: 1.4rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        /* Switch Control Tab */
        .toggle-container {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 40px;
        }

        .toggle-btn {
            background: transparent;
            border: 2px solid var(--neon-cyan);
            color: var(--neon-cyan);
            padding: 12px 30px;
            font-family: 'Orbitron', 'Noto Sans TC', sans-serif;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 0 10px rgba(0, 240, 255, 0.2);
            text-transform: uppercase;
        }

        .toggle-btn.active, .toggle-btn:hover {
            background: var(--neon-cyan);
            color: var(--bg-color);
            box-shadow: 0 0 20px var(--neon-cyan);
        }

        /* Main Content Viewports */
        .view-section {
            display: none;
            animation: fadeIn 0.5s ease-in-out forwards;
        }

        .view-section.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Grid Cards */
        .grid-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-bottom: 40px;
        }

        .card {
            background: var(--panel-bg);
            border: 1px solid rgba(255, 255, 255, 0.05);
            padding: 25px;
            border-radius: 4px;
            position: relative;
            transition: all 0.3s ease;
        }

        .card:hover {
            border-color: var(--neon-cyan);
            box-shadow: 0 0 15px rgba(0, 240, 255, 0.2);
            transform: translateY(-2px);
        }

        .card-tag {
            position: absolute;
            top: 15px;
            right: 15px;
            font-family: 'Orbitron', sans-serif;
            font-size: 0.7rem;
            padding: 2px 8px;
            border-radius: 3px;
        }

        .legacy .card-tag {
            background: rgba(255, 0, 127, 0.1);
            color: var(--neon-magenta);
            border: 1px solid var(--neon-magenta);
        }

        .ai-era .card-tag {
            background: rgba(0, 240, 255, 0.1);
            color: var(--neon-cyan);
            border: 1px solid var(--neon-cyan);
        }

        .card h3 {
            font-size: 1.25rem;
            margin-bottom: 15px;
            color: #fff;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            padding-bottom: 10px;
        }

        .card p {
            color: var(--text-dim);
            font-size: 0.95rem;
            line-height: 1.6;
        }

        .highlight-text {
            color: var(--neon-green);
            font-weight: bold;
        }

        /* Deep Case Study Section */
        .case-study {
            background: #16192b;
            border: 1px solid var(--neon-cyan);
            padding: 30px;
            border-radius: 8px;
            margin-top: 40px;
            box-shadow: 0 0 25px rgba(0, 240, 255, 0.1);
        }

        .case-study h2 {
            font-family: 'Orbitron', 'Noto Sans TC', sans-serif;
            color: var(--neon-cyan);
            margin-bottom: 20px;
            text-shadow: 0 0 5px var(--neon-cyan);
        }

        .case-item {
            margin-bottom: 25px;
            padding-bottom: 25px;
            border-bottom: 1px dashed rgba(0, 240, 255, 0.2);
        }

        .case-item:last-child {
            margin-bottom: 0;
            padding-bottom: 0;
            border-bottom: none;
        }

        .case-title {
            font-size: 1.2rem;
            color: #fff;
            margin-bottom: 10px;
            font-weight: bold;
        }

        /* Footer */
        footer {
            text-align: center;
            margin-top: 60px;
            color: var(--text-dim);
            font-family: 'Orbitron', sans-serif;
            font-size: 0.8rem;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            padding-top: 20px;
        }
    </style>
</head>
<body>

<div class="container">
    <header>
        <h1>LOGISTICS MARKETING DEEP DIVE</h1>
        <div class="subtitle">AI Era Paradigm Shift vs Legacy Marketing</div>
    </header>

    <div class="intro-panel">
        <h2><span>//</span> 核心變革思維：物流即行銷，供應鏈即體驗</h2>
        <p>在過去，物流是躲在幕後的「搬運工」，只要貨物準時抵達，工作就算完成。然而在 AI 技術爆發的今天，物流的角色早已躍升為企業的<span class="highlight-text">核心競爭力</span>。它不再只是後勤支援，而是品牌與客戶之間最真實、最感性的接觸點。AI 的價值在於消除等待的心理負擔，將冷冰冰的供應鏈轉化為溫暖的品牌承諾。</p>
    </div>

    <!-- Interactive View Control -->
    <div class="toggle-container">
        <button class="toggle-btn active" onclick="switchView('ai-era')">AI 時代物流行銷</button>
        <button class="toggle-btn" onclick="switchView('legacy')">傳統物流行銷</button>
    </div>

    <!-- AI Era Viewport -->
    <div id="ai-era" class="view-section ai-era active">
        <div class="grid-cards">
            <div class="card">
                <span class="card-tag">VALUE</span>
                <h3>核心賣點：彈性預測與動態履約</h3>
                <p>著重於系統抵抗不確定性的能力（彈性供應鏈）與運用 AI 調度運力的韌性。推銷的是<span class="highlight-text">「承諾與交付的精準度」</span>與黑天鵝免疫力。</p>
            </div>
            <div class="card">
                <span class="card-tag">DATA</span>
                <h3>數據角色：即時感測與預測型展示</h3>
                <p>將 AI 的<span class="highlight-text">「需求感測（Demand Sensing）」</span>能力化為行銷武器，在出貨旺季、動態補貨需求發生前，精準投放解決方案，主動為客戶規避延誤。</p>
            </div>
            <div class="card">
                <span class="card-tag">CX</span>
                <h3>客戶體驗：AI Agent 智能共感</h3>
                <p>利用生成式 AI 智能助理即時摘要跨國關務與異常警示，在貨主產生等待焦慮、提問之前，主動提供最佳替代方案與預期抵達時間。</p>
            </div>
            <div class="card">
                <span class="card-tag">ESG</span>
                <h3>品牌敘事：數據化綠色競爭力</h3>
                <p>透過 AI 演算法即時優化低碳路徑，提供清晰、可驗證的<span class="highlight-text">「範疇三」減碳數據儀表板</span>，助品牌主直接滿足國際綠色供應鏈法規要求。</p>
            </div>
        </div>
    </div>

    <!-- Legacy Viewport -->
    <div id="legacy" class="view-section legacy">
        <div class="grid-cards">
            <div class="card">
                <span class="card-tag">VALUE</span>
                <h3>核心賣點：標準資產被動推銷</h3>
                <p>強調「準時、安全、便宜」。行銷素材多圍繞於傳統硬體資產（如車隊數量、倉庫面積）與標準 SLA（服務水準協議）的削價競爭。</p>
            </div>
            <div class="card">
                <span class="card-tag">DATA</span>
                <h3>數據角色：後驗式歷史報告</h3>
                <p>數據多為「過去的到貨率」、「年度營收」等落後指標。行銷溝通往往流於標準商務開發（RFQ 投標），用過去的績效來被動證明實力。</p>
            </div>
            <div class="card">
                <span class="card-tag">CX</span>
                <h3>客戶體驗：單向被動告知</h3>
                <p>僅提供基礎的查單編號（Tracking ID），屬於客戶主動查詢、物流商才回覆的單向機制，缺乏對客戶等待焦慮的同理心。</p>
            </div>
            <div class="card">
                <span class="card-tag">ESG</span>
                <h3>品牌敘事：口號式表面綠化</h3>
                <p>宣傳訴求多停留在「我們改用電子發票、配合種樹」等邊緣化的環保包裝（Greenwashing），缺乏量化且具備法律效益的數據支持。</p>
            </div>
        </div>
    </div>

    <!-- Case Study Section -->
    <div class="case-study">
        <h2>// 實例深度分析 (CASE STUDIES)</h2>
        <div class="case-item">
            <div class="case-title" style="color: var(--neon-cyan);">亞馬遜 (Amazon) — 預測式發貨 (Anticipatory Shipping)</div>
            <p style="color: var(--text-dim);">傳統物流是「下單後才撈貨出貨」；Amazon 則運用 AI 專利算法分析使用者的瀏覽紀錄、購物車與停留時間。在消費者點擊購買前，系統便提前將商品運往距離該市場最近的衛星倉儲。這種極致的速度創造了傳統行銷無法比擬的「品牌驚艷體驗」。</p>
        </div>
        <div class="case-item">
            <div class="case-title" style="color: var(--neon-magenta);">全聯福利中心 — 智慧補貨與動態履約</div>
            <p style="color: var(--text-dim);">傳統連鎖通路在颱風或節慶時常因被動補貨導致貨架空空。全聯引進自動化物流中心並與氣象、歷史大數據連動，在風雨來臨前透過 AI 感測提早調配車隊與路線。當消費者在關鍵時刻看到滿滿的生鮮，便建立了極高的品牌依賴感。</p>
        </div>
    </div>

    <footer>
        <p>CONVERGENCE REPORT // LOGISTICS MARKETING PARADIGM SHIFT // YEAR 2026</p>
    </footer>
</div>

<script>
    function switchView(viewId) {
        // Remove active class from all sections
        document.querySelectorAll('.view-section').forEach(section => {
            section.classList.remove('active');
        });
        
        // Remove active class from all buttons
        document.querySelectorAll('.toggle-btn').forEach(btn => {
            btn.classList.remove('active');
        });

        // Add active class to target section and button
        document.getElementById(viewId).classList.add('active');
        event.currentTarget.classList.add('active');
    }
</script>

</body>
</html>
