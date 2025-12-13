PulseWeaveVerse 🧵🌍

Prototype Demo: https://poe.com/PulseWeaveVerse

Project Overview
PulseWeaveVerse is a futuristic data intelligence dashboard that visualizes the relationship between human sentiment and infrastructure performance across global regions.

Three Modes:

SENSE Mode - Generative data art visualization with particle systems, flowing waves, and real-time metric displays
DECIDE Mode - Operational dashboard with KPI cards, time-series charts, correlation matrix, and alert system
EXPLORE Mode - Interactive 3D globe (Three.js) showing regional data with selectable data layers
Key Features
Feature	Description
Real-time Data Simulation	DataFabric system simulates live sentiment, latency, traffic, and uptime metrics
Generative Art Canvas	Particle system and wave animations that respond to data values
Correlation Matrix	Interactive 4x4 matrix showing metric correlations with color-coded cells
3D Globe	Three.js-powered interactive globe with regional markers and pulse animations
AI Insights	Integrates with Poe API (GPT-5.1) for intelligent data analysis, with local fallback
Responsive Design	Adapts to mobile/tablet with collapsible panels and reorganized grid
Dark Mode	Full dark theme with system preference detection
Accessibility	ARIA labels, keyboard navigation (Alt+1/2/3), focus states
Tech Stack
HTML5/CSS3 - Semantic markup with CSS Grid/Flexbox
Vanilla JavaScript - No framework dependencies
Three.js - 3D globe visualization
Google Fonts - JetBrains Mono (monospace) + Outfit (UI)
CSS Custom Properties - Theming with accent colors and transitions
File Details
Single file architecture: index.html (2,405 lines)

Lines 1-1106: CSS styles with dark mode support
Lines 1107-1362: HTML structure with all three modes
Lines 1364-2403: JavaScript modules (DataFabric, SenseMode, DecideMode, ExploreMode, AIEngine, App)
The application is fully self-contained and ready to run as a Poe Canvas App!

PulseWeaveVerse is a multi-modal data experience that weaves together human sentiment and machine infrastructure signals into a single living system—expressed as art, analytics, and immersive worlds.

It is built to demonstrate how unrelated data sources, when woven together, can reveal invisible global dynamics.

✨ What Is PulseWeaveVerse?

PulseWeaveVerse merges three experiences into one adaptive application:

Mode	Experience	Purpose
🎨 Sense	Generative data art	Feel global emotional + system states
🧭 Decide	Ops & risk dashboard	Act on sentiment-driven system risk
🌍 Explore	MR / VR globe	Navigate data spatially and immersively
All modes run on a shared data fabric, ensuring consistency while allowing radically different expressions.

🧠 Core Insight

Human emotion is an invisible load on digital infrastructure.
PulseWeaveVerse makes this load:

Visible as art
Measurable as risk
Navigable as a world
🧩 The Data Weave (Unrelated Sources)

Human Signal Layer

Global sentiment streams (social + news)
Emotion keyword trends
Sentiment volatility index
Machine Signal Layer

Cloud uptime & incident metrics
Network congestion & latency
Blockchain / compute stress indicators
The Magic

PulseWeaveVerse correlates these layers to reveal:

Emotional shockwaves before outages
Infrastructure strain during global events
Hidden feedback loops between people and systems
🎛️ Experience Modes

🎨 SENSE — Data-as-Art

Flowing threads and woven fibers
Color, motion, and tension driven by live data
No charts, no numbers — pure perception
Use cases:
Museums, installations, opening demos, ambient displays

🧭 DECIDE — Ops & Sentiment Risk

Sentiment volatility vs system stress
Correlation heatmaps
Predictive risk scoring
AI-generated explanations
Use cases:
SRE teams, platform ops, digital risk monitoring

🌍 EXPLORE — MR / VR Globe

3D Earth with emotional atmospheres
Infrastructure visualized as neural grids
Correlations as shockwaves and gravity wells
Use cases:
Strategy, education, immersive demos, future-facing storytelling

⚙️ Built With Kiro

PulseWeaveVerse deeply leverages Kiro’s core capabilities:

📐 Spec-Driven Development

Single canonical data specification
Mode-specific rendering specs
Zero duplication across experiences
🤖 Agent Steering

Agent	Role
Ingest Agent	Normalize data streams
Correlation Agent	Detect cross-layer patterns
Visual Agent	Adapt visuals per mode
Risk Agent	Predict operational impact
Narrator Agent	Generate human-readable insights
🔄 Automated Workflows

Scheduled data refresh
Alert-triggered visual changes
Auto-regenerated insights and summaries
🏗️ High-Level Architecture

+    1 <!DOCTYPE html>
+    2 <html lang="en">
+    3 <head>
+    4     <meta charset="UTF-8">
+    5     <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
+    6     <title>PulseWeaveVerse | Kiro-Powered</title>
+    7     <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Ccircle cx='50' cy='50' r='40' fill='none' stroke='%2300f5d4' stroke-width='4'/%3E%3Ccircle cx='50' cy='50' r='12' fill='%2300f5d4'/%3E%3C/svg%3E">
+    8     <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;500;600&family=Outfit:wght@200;300;400;500;600;700&display=swap" rel="stylesheet">
+    9     <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
+   10     <style>
+   11         :root {
+   12             --bg-void: #0a0a0f;
+   13             --bg-surface: #12121a;
+   14             --bg-elevated: #1a1a25;
+   15             --accent-pulse: #00f5d4;
+   16             --accent-heat: #ff006e;
+   17             --accent-data: #8338ec;
+   18             --accent-warn: #fb5607;
+   19             --accent-calm: #3a86ff;
+   20             --accent-kiro: #10b981;
+   21             --text-primary: #f0f0f5;
+   22             --text-secondary: #8888a0;
+   23             --text-muted: #555566;
+   24             --glow-pulse: 0 0 30px rgba(0, 245, 212, 0.4);
+   25             --glow-heat: 0 0 30px rgba(255, 0, 110, 0.4);
+   26             --glow-kiro: 0 0 20px rgba(16, 185, 129, 0.4);
+   27             --border-subtle: rgba(255, 255, 255, 0.06);
+   28             --transition-smooth: cubic-bezier(0.4, 0, 0.2, 1);
+   29         }
+   30 
+   31         .dark { --bg-void: #0a0a0f; }
+   32 
+   33         * { margin: 0; padding: 0; box-sizing: border-box; }
+   34 
+   35         html, body {
+   36             width: 100%;
+   37             height: 100%;
+   38             overflow: hidden;
+   39             background: var(--bg-void);
+   40             font-family: 'Outfit', sans-serif;
+   41             color: var(--text-primary);
+   42             -webkit-font-smoothing: antialiased;
+   43         }
+   44 
+   45         #app {
+   46             width: 100%;
+   47             height: 100%;
+   48             display: flex;
+   49             flex-direction: column;
+   50             position: relative;
+   51         }
+   52 
+   53         /* Header */
+   54         .header {
+   55             position: fixed;
+   56             top: 0;
+   57             left: 0;
+   58             right: 0;
+   59             z-index: 100;
+   60             padding: 16px 24px;
+   61             display: flex;
+   62             justify-content: space-between;
+   63             align-items: center;
+   64             background: linear-gradient(180deg, rgba(10, 10, 15, 0.95) 0%, rgba(10, 10, 15, 0.8) 50%, transparent 100%);
+   65             pointer-events: none;
+   66         }
+   67 
+   68         .header > * { pointer-events: auto; }
+   69 
+   70         .logo {
+   71             display: flex;
+   72             align-items: center;
+   73             gap: 12px;
+   74             cursor: pointer;
+   75             transition: transform 0.3s var(--transition-smooth);
+   76         }
+   77 
+   78         .logo:hover { transform: scale(1.02); }
+   79 
+   80         .logo-icon {
+   81             width: 36px;
+   82             height: 36px;
+   83             position: relative;
+   84         }
+   85 
+   86         .logo-icon::before {
+   87             content: '';
+   88             position: absolute;
+   89             inset: 0;
+   90             border: 2px solid var(--accent-pulse);
+   91             border-radius: 50%;
+   92             animation: logoPulse 2s ease-in-out infinite;
+   93         }
+   94 
+   95         .logo-icon::after {
+   96             content: '';
+   97             position: absolute;
+   98             top: 50%;
+   99             left: 50%;
+  100             width: 12px;
+  101             height: 12px;
+  102             background: var(--accent-pulse);
+  103             border-radius: 50%;
+  104             transform: translate(-50%, -50%);
+  105             box-shadow: var(--glow-pulse);
+  106         }
+  107 
+  108         @keyframes logoPulse {
+  109             0%, 100% { transform: scale(1); opacity: 1; }
+  110             50% { transform: scale(1.15); opacity: 0.7; }
+  111         }
+  112 
+  113         .logo-text {
+  114             font-family: 'JetBrains Mono', monospace;
+  115             font-size: 14px;
+  116             font-weight: 500;
+  117             letter-spacing: 2px;
+  118             color: var(--text-primary);
+  119         }
+  120 
+  121         .logo-text span { color: var(--accent-pulse); }
+  122 
+  123         .kiro-badge {
+  124             font-size: 9px;
+  125             background: linear-gradient(135deg, var(--accent-kiro), #059669);
+  126             color: white;
+  127             padding: 3px 8px;
+  128             border-radius: 4px;
+  129             margin-left: 8px;
+  130             font-weight: 600;
+  131             letter-spacing: 1px;
+  132             box-shadow: var(--glow-kiro);
+  133         }
+  134 
+  135         /* Mode Switcher */
+  136         .mode-switcher {
+  137             display: flex;
+  138             background: var(--bg-surface);
+  139             border-radius: 10px;
+  140             padding: 4px;
+  141             border: 1px solid var(--border-subtle);
+  142             box-shadow: 0 4px 24px rgba(0, 0, 0, 0.3);
+  143         }
+  144 
+  145         .mode-btn {
+  146             background: transparent;
+  147             border: none;
+  148             padding: 10px 20px;
+  149             font-family: 'JetBrains Mono', monospace;
+  150             font-size: 12px;
+  151             font-weight: 500;
+  152             letter-spacing: 1px;
+  153             color: var(--text-secondary);
+  154             cursor: pointer;
+  155             border-radius: 7px;
+  156             transition: all 0.3s var(--transition-smooth);
+  157             display: flex;
+  158             align-items: center;
+  159             gap: 8px;
+  160             position: relative;
+  161         }
+  162 
+  163         .mode-btn:hover {
+  164             color: var(--text-primary);
+  165             background: var(--bg-elevated);
+  166         }
+  167 
+  168         .mode-btn.active {
+  169             background: var(--accent-pulse);
+  170             color: var(--bg-void);
+  171             box-shadow: 0 2px 12px rgba(0, 245, 212, 0.4);
+  172         }
+  173 
+  174         .mode-btn.active[data-mode="sense"] {
+  175             background: linear-gradient(135deg, var(--accent-data), #6b21a8);
+  176             color: white;
+  177         }
+  178         .mode-btn.active[data-mode="decide"] {
+  179             background: linear-gradient(135deg, var(--accent-calm), #1d4ed8);
+  180             color: white;
+  181         }
+  182         .mode-btn.active[data-mode="explore"] {
+  183             background: linear-gradient(135deg, var(--accent-pulse), #0d9488);
+  184             color: var(--bg-void);
+  185         }
+  186         .mode-btn.active[data-mode="specs"] {
+  187             background: linear-gradient(135deg, var(--accent-kiro), #059669);
+  188             color: white;
+  189         }
+  190         .mode-btn.active[data-mode="workflows"] {
+  191             background: linear-gradient(135deg, var(--accent-warn), #d97706);
+  192             color: white;
+  193         }
+  194 
+  195         .mode-icon {
+  196             width: 16px;
+  197             height: 16px;
+  198             opacity: 0.9;
+  199             flex-shrink: 0;
+  200         }
+  201 
+  202         /* Status */
+  203         .status {
+  204             display: flex;
+  205             align-items: center;
+  206             gap: 16px;
+  207         }
+  208 
+  209         .live-indicator {
+  210             display: flex;
+  211             align-items: center;
+  212             gap: 8px;
+  213             font-family: 'JetBrains Mono', monospace;
+  214             font-size: 11px;
+  215             color: var(--accent-pulse);
+  216             background: rgba(0, 245, 212, 0.1);
+  217             padding: 6px 12px;
+  218             border-radius: 6px;
+  219             border: 1px solid rgba(0, 245, 212, 0.2);
+  220         }
+  221 
+  222         .live-dot {
+  223             width: 8px;
+  224             height: 8px;
+  225             background: var(--accent-pulse);
+  226             border-radius: 50%;
+  227             animation: livePulse 1.5s ease-in-out infinite;
+  228             box-shadow: 0 0 8px var(--accent-pulse);
+  229         }
+  230 
+  231         @keyframes livePulse {
+  232             0%, 100% { opacity: 1; transform: scale(1); }
+  233             50% { opacity: 0.5; transform: scale(0.8); }
+  234         }
+  235 
+  236         .ai-btn {
+  237             background: linear-gradient(135deg, var(--accent-data), var(--accent-heat));
+  238             border: none;
+  239             padding: 10px 16px;
+  240             border-radius: 8px;
+  241             font-family: 'JetBrains Mono', monospace;
+  242             font-size: 11px;
+  243             font-weight: 500;
+  244             color: white;
+  245             cursor: pointer;
+  246             display: flex;
+  247             align-items: center;
+  248             gap: 8px;
+  249             transition: all 0.3s var(--transition-smooth);
+  250             box-shadow: 0 4px 16px rgba(131, 56, 236, 0.3);
+  251         }
+  252 
+  253         .ai-btn:hover {
+  254             transform: translateY(-2px);
+  255             box-shadow: 0 8px 24px rgba(131, 56, 236, 0.5);
+  256         }
+  257 
+  258         /* Mode Containers */
+  259         .mode-container {
+  260             position: absolute;
+  261             inset: 0;
+  262             opacity: 0;
+  263             visibility: hidden;
+  264             transition: opacity 0.5s var(--transition-smooth), visibility 0.5s, transform 0.5s var(--transition-smooth);
+  265             transform: scale(0.98);
+  266         }
+  267 
+  268         .mode-container.active {
+  269             opacity: 1;
+  270             visibility: visible;
+  271             transform: scale(1);
+  272         }
+  273 
+  274         /* SENSE Mode */
+  275         #sense-mode { background: var(--bg-void); }
+  276         #sense-canvas { width: 100%; height: 100%; }
+  277 
+  278         .sense-overlay {
+  279             position: absolute;
+  280             bottom: 24px;
+  281             left: 24px;
+  282             right: 24px;
+  283             display: flex;
+  284             justify-content: space-between;
+  285             align-items: flex-end;
+  286             pointer-events: none;
+  287         }
+  288 
+  289         .sense-metrics {
+  290             display: flex;
+  291             flex-direction: column;
+  292             gap: 10px;
+  293             background: rgba(18, 18, 26, 0.8);
+  294             backdrop-filter: blur(12px);
+  295             padding: 16px 20px;
+  296             border-radius: 12px;
+  297             border: 1px solid var(--border-subtle);
+  298         }
+  299 
+  300         .sense-metric {
+  301             font-family: 'JetBrains Mono', monospace;
+  302             font-size: 11px;
+  303             color: var(--text-secondary);
+  304             display: flex;
+  305             align-items: center;
+  306             gap: 12px;
+  307         }
+  308 
+  309         .sense-metric span:first-child { width: 70px; }
+  310 
+  311         .metric-bar {
+  312             width: 100px;
+  313             height: 6px;
+  314             background: var(--bg-elevated);
+  315             border-radius: 3px;
+  316             overflow: hidden;
+  317         }
+  318 
+  319         .metric-fill {
+  320             height: 100%;
+  321             border-radius: 3px;
+  322             transition: width 0.5s var(--transition-smooth);
+  323         }
+  324 
+  325         .sense-legend {
+  326             display: flex;
+  327             gap: 20px;
+  328             background: rgba(18, 18, 26, 0.8);
+  329             backdrop-filter: blur(12px);
+  330             padding: 12px 16px;
+  331             border-radius: 10px;
+  332             border: 1px solid var(--border-subtle);
+  333         }
+  334 
+  335         .legend-item {
+  336             display: flex;
+  337             align-items: center;
+  338             gap: 8px;
+  339             font-family: 'JetBrains Mono', monospace;
+  340             font-size: 10px;
+  341             color: var(--text-muted);
+  342         }
+  343 
+  344         .legend-dot {
+  345             width: 8px;
+  346             height: 8px;
+  347             border-radius: 50%;
+  348             box-shadow: 0 0 8px currentColor;
+  349         }
+  350 
+  351         /* DECIDE Mode */
+  352         #decide-mode {
+  353             background: var(--bg-void);
+  354             padding: 80px 24px 24px;
+  355             overflow-y: auto;
+  356         }
+  357 
+  358         .dashboard-grid {
+  359             display: grid;
+  360             grid-template-columns: repeat(4, 1fr);
+  361             grid-template-rows: auto auto 1fr;
+  362             gap: 16px;
+  363             max-width: 1600px;
+  364             margin: 0 auto;
+  365             height: calc(100vh - 104px);
+  366         }
+  367 
+  368         .card {
+  369             background: var(--bg-surface);
+  370             border: 1px solid var(--border-subtle);
+  371             border-radius: 14px;
+  372             padding: 20px;
+  373             display: flex;
+  374             flex-direction: column;
+  375             transition: transform 0.2s, box-shadow 0.2s;
+  376         }
+  377 
+  378         .card:hover {
+  379             transform: translateY(-2px);
+  380             box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
+  381         }
+  382 
+  383         .card-header {
+  384             display: flex;
+  385             justify-content: space-between;
+  386             align-items: center;
+  387             margin-bottom: 16px;
+  388         }
+  389 
+  390         .card-title {
+  391             font-family: 'JetBrains Mono', monospace;
+  392             font-size: 11px;
+  393             font-weight: 500;
+  394             letter-spacing: 1px;
+  395             color: var(--text-secondary);
+  396             text-transform: uppercase;
+  397         }
+  398 
+  399         .card-badge {
+  400             font-family: 'JetBrains Mono', monospace;
+  401             font-size: 10px;
+  402             padding: 4px 10px;
+  403             border-radius: 5px;
+  404             background: var(--bg-elevated);
+  405         }
+  406 
+  407         .kpi-card { grid-column: span 1; }
+  408 
+  409         .kpi-value {
+  410             font-family: 'Outfit', sans-serif;
+  411             font-size: 42px;
+  412             font-weight: 300;
+  413             line-height: 1;
+  414             margin-bottom: 8px;
+  415         }
+  416 
+  417         .kpi-label {
+  418             font-size: 13px;
+  419             color: var(--text-secondary);
+  420         }
+  421 
+  422         .kpi-change {
+  423             display: flex;
+  424             align-items: center;
+  425             gap: 6px;
+  426             font-family: 'JetBrains Mono', monospace;
+  427             font-size: 11px;
+  428             margin-top: 12px;
+  429             padding: 6px 10px;
+  430             border-radius: 6px;
+  431             width: fit-content;
+  432         }
+  433 
+  434         .kpi-change.positive { color: var(--accent-pulse); background: rgba(0, 245, 212, 0.1); }
+  435         .kpi-change.negative { color: var(--accent-heat); background: rgba(255, 0, 110, 0.1); }
+  436         .kpi-change.neutral { color: var(--text-secondary); background: var(--bg-elevated); }
+  437 
+  438         .chart-card { grid-column: span 2; }
+  439         .chart-container { flex: 1; position: relative; min-height: 200px; }
+  440         .chart-canvas { width: 100%; height: 100%; }
+  441 
+  442         .correlation-card { grid-column: span 2; grid-row: span 2; }
+  443 
+  444         .correlation-header-labels {
+  445             font-size: 10px;
+  446             color: var(--text-muted);
+  447             margin-bottom: 12px;
+  448             font-family: 'JetBrains Mono', monospace;
+  449             display: flex;
+  450             gap: 4px;
+  451         }
+  452 
+  453         .correlation-header-labels span { flex: 1; text-align: center; }
+  454 
+  455         .correlation-matrix {
+  456             flex: 1;
+  457             display: grid;
+  458             grid-template-columns: repeat(4, 1fr);
+  459             gap: 6px;
+  460         }
+  461 
+  462         .correlation-cell {
+  463             aspect-ratio: 1;
+  464             border-radius: 6px;
+  465             display: flex;
+  466             align-items: center;
+  467             justify-content: center;
+  468             font-family: 'JetBrains Mono', monospace;
+  469             font-size: 11px;
+  470             font-weight: 500;
+  471             color: white;
+  472             cursor: pointer;
+  473             transition: transform 0.2s, box-shadow 0.2s;
+  474         }
+  475 
+  476         .correlation-cell:hover {
+  477             transform: scale(1.08);
+  478             box-shadow: 0 4px 16px rgba(0, 0, 0, 0.4);
+  479             z-index: 1;
+  480         }
+  481 
+  482         .alerts-card { grid-column: span 2; grid-row: span 2; }
+  483 
+  484         .alerts-list {
+  485             flex: 1;
+  486             overflow-y: auto;
+  487             display: flex;
+  488             flex-direction: column;
+  489             gap: 10px;
+  490         }
+  491 
+  492         .alert-item {
+  493             display: flex;
+  494             gap: 12px;
+  495             padding: 14px;
+  496             background: var(--bg-elevated);
+  497             border-radius: 10px;
+  498             border-left: 4px solid;
+  499             animation: alertSlide 0.3s var(--transition-smooth);
+  500             cursor: pointer;
+  501             transition: transform 0.2s, background 0.2s;
+  502         }
+  503 
+  504         .alert-item:hover {
+  505             transform: translateX(4px);
+  506             background: rgba(26, 26, 37, 0.8);
+  507         }
+  508 
+  509         @keyframes alertSlide {
+  510             from { opacity: 0; transform: translateX(-10px); }
+  511             to { opacity: 1; transform: translateX(0); }
+  512         }
+  513 
+  514         .alert-item.critical { border-color: var(--accent-heat); }
+  515         .alert-item.warning { border-color: var(--accent-warn); }
+  516         .alert-item.info { border-color: var(--accent-calm); }
+  517 
+  518         .alert-icon {
+  519             width: 24px;
+  520             height: 24px;
+  521             border-radius: 50%;
+  522             display: flex;
+  523             align-items: center;
+  524             justify-content: center;
+  525             font-size: 12px;
+  526             font-weight: 600;
+  527             flex-shrink: 0;
+  528         }
+  529 
+  530         .alert-item.critical .alert-icon { background: rgba(255, 0, 110, 0.2); color: var(--accent-heat); }
+  531         .alert-item.warning .alert-icon { background: rgba(251, 86, 7, 0.2); color: var(--accent-warn); }
+  532         .alert-item.info .alert-icon { background: rgba(58, 134, 255, 0.2); color: var(--accent-calm); }
+  533 
+  534         .alert-content { flex: 1; min-width: 0; }
+  535         .alert-title { font-size: 13px; font-weight: 500; margin-bottom: 4px; }
+  536         .alert-desc { font-size: 12px; color: var(--text-secondary); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
+  537         .alert-time { font-family: 'JetBrains Mono', monospace; font-size: 10px; color: var(--text-muted); flex-shrink: 0; }
+  538 
+  539         /* EXPLORE Mode */
+  540         #explore-mode { background: var(--bg-void); }
+  541         #globe-container { width: 100%; height: 100%; cursor: grab; }
+  542         #globe-container:active { cursor: grabbing; }
+  543 
+  544         .explore-panel {
+  545             position: absolute;
+  546             top: 80px;
+  547             right: 24px;
+  548             width: 320px;
+  549             background: rgba(18, 18, 26, 0.92);
+  550             backdrop-filter: blur(20px);
+  551             border: 1px solid var(--border-subtle);
+  552             border-radius: 16px;
+  553             padding: 20px;
+  554             max-height: calc(100vh - 120px);
+  555             overflow-y: auto;
+  556             box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
+  557         }
+  558 
+  559         .panel-section { margin-bottom: 24px; }
+  560         .panel-section:last-child { margin-bottom: 0; }
+  561 
+  562         .panel-title {
+  563             font-family: 'JetBrains Mono', monospace;
+  564             font-size: 10px;
+  565             font-weight: 500;
+  566             letter-spacing: 2px;
+  567             color: var(--text-muted);
+  568             text-transform: uppercase;
+  569             margin-bottom: 12px;
+  570         }
+  571 
+  572         .region-list { display: flex; flex-direction: column; gap: 8px; }
+  573 
+  574         .region-item {
+  575             display: flex;
+  576             align-items: center;
+  577             justify-content: space-between;
+  578             padding: 12px 14px;
+  579             background: var(--bg-elevated);
+  580             border-radius: 10px;
+  581             cursor: pointer;
+  582             transition: all 0.2s var(--transition-smooth);
+  583             border: 1px solid transparent;
+  584         }
+  585 
+  586         .region-item:hover {
+  587             background: var(--bg-surface);
+  588             transform: translateX(4px);
+  589             border-color: var(--border-subtle);
+  590         }
+  591 
+  592         .region-info { display: flex; align-items: center; gap: 12px; }
+  593 
+  594         .region-dot {
+  595             width: 10px;
+  596             height: 10px;
+  597             border-radius: 50%;
+  598             box-shadow: 0 0 8px currentColor;
+  599         }
+  600 
+  601         .region-name { font-size: 13px; font-weight: 500; }
+  602         .region-stats { text-align: right; }
+  603         .region-sentiment { font-family: 'JetBrains Mono', monospace; font-size: 14px; font-weight: 600; }
+  604         .region-trend { font-size: 11px; color: var(--text-secondary); display: flex; align-items: center; gap: 4px; justify-content: flex-end; }
+  605 
+  606         .data-layer-toggle { display: flex; flex-wrap: wrap; gap: 8px; }
+  607 
+  608         .layer-btn {
+  609             flex: 1;
+  610             min-width: calc(50% - 4px);
+  611             padding: 12px 12px;
+  612             background: var(--bg-elevated);
+  613             border: 1px solid var(--border-subtle);
+  614             border-radius: 8px;
+  615             font-family: 'JetBrains Mono', monospace;
+  616             font-size: 10px;
+  617             color: var(--text-secondary);
+  618             cursor: pointer;
+  619             transition: all 0.2s var(--transition-smooth);
+  620             text-align: center;
+  621         }
+  622 
+  623         .layer-btn:hover {
+  624             border-color: var(--text-muted);
+  625             background: var(--bg-surface);
+  626             color: var(--text-primary);
+  627         }
+  628 
+  629         .layer-btn.active {
+  630             background: linear-gradient(135deg, var(--accent-pulse), #0d9488);
+  631             border-color: var(--accent-pulse);
+  632             color: var(--bg-void);
+  633             box-shadow: 0 2px 12px rgba(0, 245, 212, 0.3);
+  634         }
+  635 
+  636         /* SPECS Mode - Kiro Spec-Driven Development */
+  637         #specs-mode {
+  638             background: var(--bg-void);
+  639             padding: 80px 24px 24px;
+  640             overflow-y: auto;
+  641         }
+  642 
+  643         .specs-container {
+  644             max-width: 1400px;
+  645             margin: 0 auto;
+  646             display: grid;
+  647             grid-template-columns: 350px 1fr;
+  648             gap: 24px;
+  649             height: calc(100vh - 104px);
+  650         }
+  651 
+  652         .specs-sidebar {
+  653             background: var(--bg-surface);
+  654             border: 1px solid var(--border-subtle);
+  655             border-radius: 14px;
+  656             padding: 20px;
+  657             overflow-y: auto;
+  658         }
+  659 
+  660         .specs-main {
+  661             background: var(--bg-surface);
+  662             border: 1px solid var(--border-subtle);
+  663             border-radius: 14px;
+  664             padding: 24px;
+  665             overflow-y: auto;
+  666         }
+  667 
+  668         .spec-section-title {
+  669             font-family: 'JetBrains Mono', monospace;
+  670             font-size: 11px;
+  671             font-weight: 600;
+  672             letter-spacing: 2px;
+  673             color: var(--accent-kiro);
+  674             text-transform: uppercase;
+  675             margin-bottom: 16px;
+  676             display: flex;
+  677             align-items: center;
+  678             gap: 8px;
+  679         }
+  680 
+  681         .spec-section-title::before {
+  682             content: '';
+  683             width: 8px;
+  684             height: 8px;
+  685             background: var(--accent-kiro);
+  686             border-radius: 2px;
+  687         }
+  688 
+  689         .spec-list { display: flex; flex-direction: column; gap: 8px; }
+  690 
+  691         .spec-item {
+  692             padding: 14px 16px;
+  693             background: var(--bg-elevated);
+  694             border-radius: 10px;
+  695             cursor: pointer;
+  696             transition: all 0.2s var(--transition-smooth);
+  697             border: 2px solid transparent;
+  698         }
+  699 
+  700         .spec-item:hover { background: rgba(26, 26, 37, 0.8); border-color: var(--border-subtle); }
+  701         .spec-item.active { border-color: var(--accent-kiro); background: rgba(16, 185, 129, 0.1); }
+  702 
+  703         .spec-item-header {
+  704             display: flex;
+  705             justify-content: space-between;
+  706             align-items: center;
+  707             margin-bottom: 6px;
+  708         }
+  709 
+  710         .spec-item-name {
+  711             font-family: 'JetBrains Mono', monospace;
+  712             font-size: 13px;
+  713             font-weight: 500;
+  714             color: var(--text-primary);
+  715         }
+  716 
+  717         .spec-item-status {
+  718             font-size: 9px;
+  719             padding: 3px 8px;
+  720             border-radius: 4px;
+  721             font-weight: 600;
+  722             letter-spacing: 0.5px;
+  723         }
+  724 
+  725         .spec-item-status.valid { background: rgba(16, 185, 129, 0.2); color: var(--accent-kiro); }
+  726         .spec-item-status.warning { background: rgba(251, 86, 7, 0.2); color: var(--accent-warn); }
+  727         .spec-item-status.error { background: rgba(255, 0, 110, 0.2); color: var(--accent-heat); }
+  728 
+  729         .spec-item-desc {
+  730             font-size: 12px;
+  731             color: var(--text-secondary);
+  732         }
+  733 
+  734         .spec-editor {
+  735             height: 100%;
+  736             display: flex;
+  737             flex-direction: column;
+  738         }
+  739 
+  740         .spec-editor-header {
+  741             display: flex;
+  742             justify-content: space-between;
+  743             align-items: center;
+  744             margin-bottom: 20px;
+  745             padding-bottom: 16px;
+  746             border-bottom: 1px solid var(--border-subtle);
+  747         }
+  748 
+  749         .spec-editor-title {
+  750             font-size: 20px;
+  751             font-weight: 600;
+  752             display: flex;
+  753             align-items: center;
+  754             gap: 12px;
+  755         }
+  756 
+  757         .spec-editor-actions { display: flex; gap: 10px; }
+  758 
+  759         .spec-action-btn {
+  760             padding: 10px 18px;
+  761             border-radius: 8px;
+  762             font-family: 'JetBrains Mono', monospace;
+  763             font-size: 11px;
+  764             font-weight: 500;
+  765             cursor: pointer;
+  766             transition: all 0.2s var(--transition-smooth);
+  767             border: 1px solid var(--border-subtle);
+  768             background: var(--bg-elevated);
+  769             color: var(--text-secondary);
+  770         }
+  771 
+  772         .spec-action-btn:hover { background: var(--bg-surface); color: var(--text-primary); border-color: var(--text-muted); }
+  773         .spec-action-btn.primary { background: linear-gradient(135deg, var(--accent-kiro), #059669); border: none; color: white; }
+  774         .spec-action-btn.primary:hover { transform: translateY(-2px); box-shadow: 0 4px 16px rgba(16, 185, 129, 0.4); }
+  775 
+  776         .spec-code-block {
+  777             flex: 1;
+  778             background: rgba(0, 0, 0, 0.3);
+  779             border-radius: 10px;
+  780             padding: 20px;
+  781             font-family: 'JetBrains Mono', monospace;
+  782             font-size: 13px;
+  783             line-height: 1.7;
+  784             color: var(--text-secondary);
+  785             overflow-y: auto;
+  786             white-space: pre-wrap;
+  787             border: 1px solid var(--border-subtle);
+  788         }
+  789 
+  790         .spec-code-block .keyword { color: var(--accent-data); }
+  791         .spec-code-block .type { color: var(--accent-kiro); }
+  792         .spec-code-block .string { color: var(--accent-warn); }
+  793         .spec-code-block .number { color: var(--accent-pulse); }
+  794         .spec-code-block .comment { color: var(--text-muted); font-style: italic; }
+  795         .spec-code-block .property { color: var(--accent-calm); }
+  796 
+  797         /* WORKFLOWS Mode - Automated Workflows */
+  798         #workflows-mode {
+  799             background: var(--bg-void);
+  800             padding: 80px 24px 24px;
+  801             overflow-y: auto;
+  802         }
+  803 
+  804         .workflows-container {
+  805             max-width: 1400px;
+  806             margin: 0 auto;
+  807             display: flex;
+  808             flex-direction: column;
+  809             gap: 24px;
+  810         }
+  811 
+  812         .workflows-header {
+  813             display: flex;
+  814             justify-content: space-between;
+  815             align-items: center;
+  816         }
+  817 
+  818         .workflows-title {
+  819             font-size: 24px;
+  820             font-weight: 600;
+  821             display: flex;
+  822             align-items: center;
+  823             gap: 12px;
+  824         }
+  825 
+  826         .workflow-stats {
+  827             display: flex;
+  828             gap: 24px;
+  829         }
+  830 
+  831         .workflow-stat {
+  832             text-align: center;
+  833             padding: 12px 20px;
+  834             background: var(--bg-surface);
+  835             border-radius: 10px;
+  836             border: 1px solid var(--border-subtle);
+  837         }
+  838 
+  839         .workflow-stat-value {
+  840             font-family: 'JetBrains Mono', monospace;
+  841             font-size: 24px;
+  842             font-weight: 600;
+  843         }
+  844 
+  845         .workflow-stat-label {
+  846             font-size: 11px;
+  847             color: var(--text-secondary);
+  848             text-transform: uppercase;
+  849             letter-spacing: 1px;
+  850         }
+  851 
+  852         .workflows-grid {
+  853             display: grid;
+  854             grid-template-columns: repeat(auto-fill, minmax(400px, 1fr));
+  855             gap: 16px;
+  856         }
+  857 
+  858         .workflow-card {
+  859             background: var(--bg-surface);
+  860             border: 1px solid var(--border-subtle);
+  861             border-radius: 14px;
+  862             padding: 20px;
+  863             transition: all 0.2s var(--transition-smooth);
+  864         }
+  865 
+  866         .workflow-card:hover {
+  867             transform: translateY(-2px);
+  868             box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
+  869             border-color: var(--accent-warn);
+  870         }
+  871 
+  872         .workflow-card-header {
+  873             display: flex;
+  874             justify-content: space-between;
+  875             align-items: flex-start;
+  876             margin-bottom: 16px;
+  877         }
+  878 
+  879         .workflow-card-title {
+  880             font-size: 16px;
+  881             font-weight: 600;
+  882             margin-bottom: 4px;
+  883         }
+  884 
+  885         .workflow-card-desc {
+  886             font-size: 12px;
+  887             color: var(--text-secondary);
+  888         }
+  889 
+  890         .workflow-status {
+  891             display: flex;
+  892             align-items: center;
+  893             gap: 6px;
+  894             padding: 6px 12px;
+  895             border-radius: 6px;
+  896             font-family: 'JetBrains Mono', monospace;
+  897             font-size: 10px;
+  898             font-weight: 600;
+  899         }
+  900 
+  901         .workflow-status.running {
+  902             background: rgba(16, 185, 129, 0.2);
+  903             color: var(--accent-kiro);
+  904         }
+  905 
+  906         .workflow-status.paused {
+  907             background: rgba(251, 86, 7, 0.2);
+  908             color: var(--accent-warn);
+  909         }
+  910 
+  911         .workflow-status.idle {
+  912             background: var(--bg-elevated);
+  913             color: var(--text-secondary);
+  914         }
+  915 
+  916         .workflow-status-dot {
+  917             width: 6px;
+  918             height: 6px;
+  919             border-radius: 50%;
+  920             background: currentColor;
+  921         }
+  922 
+  923         .workflow-status.running .workflow-status-dot {
+  924             animation: statusPulse 1s ease-in-out infinite;
+  925         }
+  926 
+  927         @keyframes statusPulse {
+  928             0%, 100% { opacity: 1; }
+  929             50% { opacity: 0.4; }
+  930         }
+  931 
+  932         .workflow-steps {
+  933             display: flex;
+  934             flex-direction: column;
+  935             gap: 8px;
+  936             margin-bottom: 16px;
+  937         }
+  938 
+  939         .workflow-step {
+  940             display: flex;
+  941             align-items: center;
+  942             gap: 12px;
+  943             padding: 10px 14px;
+  944             background: var(--bg-elevated);
+  945             border-radius: 8px;
+  946             font-size: 12px;
+  947         }
+  948 
+  949         .workflow-step-icon {
+  950             width: 24px;
+  951             height: 24px;
+  952             border-radius: 6px;
+  953             display: flex;
+  954             align-items: center;
+  955             justify-content: center;
+  956             font-size: 12px;
+  957             flex-shrink: 0;
+  958         }
+  959 
+  960         .workflow-step-icon.trigger { background: rgba(131, 56, 236, 0.2); color: var(--accent-data); }
+  961         .workflow-step-icon.action { background: rgba(58, 134, 255, 0.2); color: var(--accent-calm); }
+  962         .workflow-step-icon.output { background: rgba(0, 245, 212, 0.2); color: var(--accent-pulse); }
+  963 
+  964         .workflow-step-content { flex: 1; }
+  965         .workflow-step-name { font-weight: 500; margin-bottom: 2px; }
+  966         .workflow-step-detail { font-size: 11px; color: var(--text-muted); }
+  967 
+  968         .workflow-step-status {
+  969             font-family: 'JetBrains Mono', monospace;
+  970             font-size: 10px;
+  971             color: var(--text-muted);
+  972         }
+  973 
+  974         .workflow-step-status.complete { color: var(--accent-kiro); }
+  975         .workflow-step-status.running { color: var(--accent-warn); }
+  976 
+  977         .workflow-actions {
+  978             display: flex;
+  979             gap: 10px;
+  980             padding-top: 16px;
+  981             border-top: 1px solid var(--border-subtle);
+  982         }
+  983 
+  984         .workflow-action-btn {
+  985             flex: 1;
+  986             padding: 10px;
+  987             border-radius: 8px;
+  988             font-family: 'JetBrains Mono', monospace;
+  989             font-size: 11px;
+  990             font-weight: 500;
+  991             cursor: pointer;
+  992             transition: all 0.2s var(--transition-smooth);
+  993             border: 1px solid var(--border-subtle);
+  994             background: var(--bg-elevated);
+  995             color: var(--text-secondary);
+  996             text-align: center;
+  997         }
+  998 
+  999         .workflow-action-btn:hover { background: var(--bg-surface); color: var(--text-primary); }
+ 1000         .workflow-action-btn.run { background: linear-gradient(135deg, var(--accent-kiro), #059669); border: none; color: white; }
+ 1001         .workflow-action-btn.stop { background: linear-gradient(135deg, var(--accent-heat), #be185d); border: none; color: white; }
+ 1002 
+ 1003         /* Agent Steering Panel */
+ 1004         .agent-panel {
+ 1005             position: fixed;
+ 1006             top: 80px;
+ 1007             left: 24px;
+ 1008             width: 320px;
+ 1009             background: rgba(18, 18, 26, 0.95);
+ 1010             backdrop-filter: blur(20px);
+ 1011             border: 1px solid var(--border-subtle);
+ 1012             border-radius: 16px;
+ 1013             padding: 20px;
+ 1014             z-index: 90;
+ 1015             opacity: 0;
+ 1016             visibility: hidden;
+ 1017             transform: translateX(-20px);
+ 1018             transition: all 0.4s var(--transition-smooth);
+ 1019             box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
+ 1020         }
+ 1021 
+ 1022         .agent-panel.visible {
+ 1023             opacity: 1;
+ 1024             visibility: visible;
+ 1025             transform: translateX(0);
+ 1026         }
+ 1027 
+ 1028         .agent-panel-header {
+ 1029             display: flex;
+ 1030             justify-content: space-between;
+ 1031             align-items: center;
+ 1032             margin-bottom: 16px;
+ 1033             padding-bottom: 12px;
+ 1034             border-bottom: 1px solid var(--border-subtle);
+ 1035         }
+ 1036 
+ 1037         .agent-panel-title {
+ 1038             font-family: 'JetBrains Mono', monospace;
+ 1039             font-size: 12px;
+ 1040             font-weight: 600;
+ 1041             color: var(--accent-kiro);
+ 1042             display: flex;
+ 1043             align-items: center;
+ 1044             gap: 8px;
+ 1045         }
+ 1046 
+ 1047         .agent-panel-close {
+ 1048             background: var(--bg-elevated);
+ 1049             border: 1px solid var(--border-subtle);
+ 1050             color: var(--text-secondary);
+ 1051             cursor: pointer;
+ 1052             font-size: 16px;
+ 1053             width: 28px;
+ 1054             height: 28px;
+ 1055             border-radius: 6px;
+ 1056             display: flex;
+ 1057             align-items: center;
+ 1058             justify-content: center;
+ 1059             transition: all 0.2s;
+ 1060         }
+ 1061 
+ 1062         .agent-panel-close:hover { background: var(--accent-heat); border-color: var(--accent-heat); color: white; }
+ 1063 
+ 1064         .agent-config { display: flex; flex-direction: column; gap: 16px; }
+ 1065 
+ 1066         .agent-config-group { display: flex; flex-direction: column; gap: 8px; }
+ 1067 
+ 1068         .agent-config-label {
+ 1069             font-family: 'JetBrains Mono', monospace;
+ 1070             font-size: 10px;
+ 1071             font-weight: 500;
+ 1072             color: var(--text-muted);
+ 1073             text-transform: uppercase;
+ 1074             letter-spacing: 1px;
+ 1075         }
+ 1076 
+ 1077         .agent-config-select {
+ 1078             padding: 12px 14px;
+ 1079             background: var(--bg-elevated);
+ 1080             border: 1px solid var(--border-subtle);
+ 1081             border-radius: 8px;
+ 1082             color: var(--text-primary);
+ 1083             font-family: 'JetBrains Mono', monospace;
+ 1084             font-size: 12px;
+ 1085             cursor: pointer;
+ 1086             transition: all 0.2s;
+ 1087         }
+ 1088 
+ 1089         .agent-config-select:hover { border-color: var(--text-muted); }
+ 1090         .agent-config-select:focus { outline: none; border-color: var(--accent-kiro); }
+ 1091 
+ 1092         .agent-config-slider {
+ 1093             display: flex;
+ 1094             align-items: center;
+ 1095             gap: 12px;
+ 1096         }
+ 1097 
+ 1098         .agent-config-slider input[type="range"] {
+ 1099             flex: 1;
+ 1100             height: 6px;
+ 1101             border-radius: 3px;
+ 1102             background: var(--bg-elevated);
+ 1103             appearance: none;
+ 1104             cursor: pointer;
+ 1105         }
+ 1106 
+ 1107         .agent-config-slider input[type="range"]::-webkit-slider-thumb {
+ 1108             appearance: none;
+ 1109             width: 16px;
+ 1110             height: 16px;
+ 1111             border-radius: 50%;
+ 1112             background: var(--accent-kiro);
+ 1113             cursor: pointer;
+ 1114             box-shadow: 0 0 8px rgba(16, 185, 129, 0.4);
+ 1115         }
+ 1116 
+ 1117         .agent-config-value {
+ 1118             font-family: 'JetBrains Mono', monospace;
+ 1119             font-size: 12px;
+ 1120             color: var(--accent-kiro);
+ 1121             min-width: 40px;
+ 1122             text-align: right;
+ 1123         }
+ 1124 
+ 1125         .agent-steering-log {
+ 1126             background: rgba(0, 0, 0, 0.3);
+ 1127             border-radius: 8px;
+ 1128             padding: 12px;
+ 1129             max-height: 150px;
+ 1130             overflow-y: auto;
+ 1131             font-family: 'JetBrains Mono', monospace;
+ 1132             font-size: 10px;
+ 1133             line-height: 1.6;
+ 1134             color: var(--text-muted);
+ 1135         }
+ 1136 
+ 1137         .agent-log-entry { margin-bottom: 6px; }
+ 1138         .agent-log-entry .timestamp { color: var(--text-muted); }
+ 1139         .agent-log-entry .message { color: var(--text-secondary); }
+ 1140         .agent-log-entry.success .message { color: var(--accent-kiro); }
+ 1141         .agent-log-entry.warning .message { color: var(--accent-warn); }
+ 1142         .agent-log-entry.error .message { color: var(--accent-heat); }
+ 1143 
+ 1144         /* AI Panel */
+ 1145         .ai-panel {
+ 1146             position: fixed;
+ 1147             bottom: 24px;
+ 1148             left: 50%;
+ 1149             transform: translateX(-50%) translateY(100%);
+ 1150             width: 90%;
+ 1151             max-width: 600px;
+ 1152             background: rgba(18, 18, 26, 0.95);
+ 1153             backdrop-filter: blur(20px);
+ 1154             border: 1px solid var(--border-subtle);
+ 1155             border-radius: 16px;
+ 1156             padding: 20px;
+ 1157             z-index: 90;
+ 1158             opacity: 0;
+ 1159             visibility: hidden;
+ 1160             transition: all 0.4s var(--transition-smooth);
+ 1161             box-shadow: 0 -8px 32px rgba(0, 0, 0, 0.4);
+ 1162         }
+ 1163 
+ 1164         .ai-panel.visible {
+ 1165             opacity: 1;
+ 1166             visibility: visible;
+ 1167             transform: translateX(-50%) translateY(0);
+ 1168         }
+ 1169 
+ 1170         .ai-panel-header {
+ 1171             display: flex;
+ 1172             justify-content: space-between;
+ 1173             align-items: center;
+ 1174             margin-bottom: 16px;
+ 1175         }
+ 1176 
+ 1177         .ai-panel-title {
+ 1178             font-family: 'JetBrains Mono', monospace;
+ 1179             font-size: 12px;
+ 1180             font-weight: 500;
+ 1181             color: var(--accent-data);
+ 1182             display: flex;
+ 1183             align-items: center;
+ 1184             gap: 8px;
+ 1185         }
+ 1186 
+ 1187         .ai-panel-close {
+ 1188             background: var(--bg-elevated);
+ 1189             border: 1px solid var(--border-subtle);
+ 1190             color: var(--text-secondary);
+ 1191             cursor: pointer;
+ 1192             font-size: 16px;
+ 1193             width: 28px;
+ 1194             height: 28px;
+ 1195             border-radius: 6px;
+ 1196             display: flex;
+ 1197             align-items: center;
+ 1198             justify-content: center;
+ 1199             transition: all 0.2s;
+ 1200         }
+ 1201 
+ 1202         .ai-panel-close:hover { background: var(--accent-heat); border-color: var(--accent-heat); color: white; }
+ 1203 
+ 1204         .ai-panel-content {
+ 1205             font-size: 14px;
+ 1206             line-height: 1.7;
+ 1207             color: var(--text-secondary);
+ 1208         }
+ 1209 
+ 1210         .ai-panel-content strong { color: var(--text-primary); }
+ 1211 
+ 1212         .ai-loading { display: flex; align-items: center; gap: 12px; }
+ 1213         .ai-loading-dots { display: flex; gap: 4px; }
+ 1214 
+ 1215         .ai-loading-dots span {
+ 1216             width: 6px;
+ 1217             height: 6px;
+ 1218             background: var(--accent-data);
+ 1219             border-radius: 50%;
+ 1220             animation: dotPulse 1.4s ease-in-out infinite;
+ 1221         }
+ 1222 
+ 1223         .ai-loading-dots span:nth-child(2) { animation-delay: 0.2s; }
+ 1224         .ai-loading-dots span:nth-child(3) { animation-delay: 0.4s; }
+ 1225 
+ 1226         @keyframes dotPulse {
+ 1227             0%, 80%, 100% { transform: scale(0.6); opacity: 0.5; }
+ 1228             40% { transform: scale(1); opacity: 1; }
+ 1229         }
+ 1230 
+ 1231         /* VR Indicator */
+ 1232         .vr-indicator {
+ 1233             position: absolute;
+ 1234             bottom: 24px;
+ 1235             left: 24px;
+ 1236             display: flex;
+ 1237             align-items: center;
+ 1238             gap: 12px;
+ 1239             padding: 12px 16px;
+ 1240             background: rgba(18, 18, 26, 0.92);
+ 1241             backdrop-filter: blur(12px);
+ 1242             border-radius: 10px;
+ 1243             border: 1px solid var(--border-subtle);
+ 1244             font-family: 'JetBrains Mono', monospace;
+ 1245             font-size: 11px;
+ 1246             color: var(--text-secondary);
+ 1247         }
+ 1248 
+ 1249         .vr-status { display: flex; align-items: center; gap: 8px; }
+ 1250 
+ 1251         .vr-status-dot {
+ 1252             width: 8px;
+ 1253             height: 8px;
+ 1254             background: var(--accent-pulse);
+ 1255             border-radius: 50%;
+ 1256             box-shadow: 0 0 8px var(--accent-pulse);
+ 1257         }
+ 1258 
+ 1259         .vr-btn {
+ 1260             background: linear-gradient(135deg, var(--accent-pulse), #0d9488);
+ 1261             border: none;
+ 1262             padding: 10px 16px;
+ 1263             border-radius: 8px;
+ 1264             color: var(--bg-void);
+ 1265             font-family: 'JetBrains Mono', monospace;
+ 1266             font-size: 11px;
+ 1267             font-weight: 500;
+ 1268             cursor: pointer;
+ 1269             transition: all 0.2s var(--transition-smooth);
+ 1270             box-shadow: 0 2px 12px rgba(0, 245, 212, 0.3);
+ 1271         }
+ 1272 
+ 1273         .vr-btn:hover { transform: translateY(-2px); box-shadow: 0 4px 20px rgba(0, 245, 212, 0.5); }
+ 1274 
+ 1275         /* Toast */
+ 1276         .toast {
+ 1277             position: fixed;
+ 1278             bottom: 100px;
+ 1279             left: 50%;
+ 1280             transform: translateX(-50%) translateY(20px);
+ 1281             background: var(--bg-surface);
+ 1282             border: 1px solid var(--border-subtle);
+ 1283             padding: 14px 24px;
+ 1284             border-radius: 10px;
+ 1285             font-size: 13px;
+ 1286             color: var(--text-primary);
+ 1287             z-index: 1000;
+ 1288             opacity: 0;
+ 1289             visibility: hidden;
+ 1290             transition: all 0.3s var(--transition-smooth);
+ 1291             box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
+ 1292             display: flex;
+ 1293             align-items: center;
+ 1294             gap: 10px;
+ 1295         }
+ 1296 
+ 1297         .toast.visible {
+ 1298             opacity: 1;
+ 1299             visibility: visible;
+ 1300             transform: translateX(-50%) translateY(0);
+ 1301         }
+ 1302 
+ 1303         .toast-icon {
+ 1304             width: 20px;
+ 1305             height: 20px;
+ 1306             border-radius: 50%;
+ 1307             display: flex;
+ 1308             align-items: center;
+ 1309             justify-content: center;
+ 1310             background: rgba(0, 245, 212, 0.2);
+ 1311             color: var(--accent-pulse);
+ 1312             font-size: 12px;
+ 1313         }
+ 1314 
+ 1315         /* Responsive */
+ 1316         @media (max-width: 1024px) {
+ 1317             .dashboard-grid { grid-template-columns: repeat(2, 1fr); }
+ 1318             .explore-panel { width: 280px; right: 16px; }
+ 1319             .specs-container { grid-template-columns: 1fr; }
+ 1320             .specs-sidebar { display: none; }
+ 1321             .workflows-grid { grid-template-columns: 1fr; }
+ 1322             .mode-btn span { display: none; }
+ 1323             .mode-btn { padding: 10px 14px; }
+ 1324         }
+ 1325 
+ 1326         @media (max-width: 768px) {
+ 1327             .header { padding: 12px 16px; }
+ 1328             .logo-text { font-size: 11px; letter-spacing: 1px; }
+ 1329             .kiro-badge { display: none; }
+ 1330             .mode-switcher { padding: 3px; }
+ 1331             .mode-btn { padding: 10px 14px; }
+ 1332             .status { gap: 8px; }
+ 1333             .live-indicator { display: none; }
+ 1334             .ai-btn span { display: none; }
+ 1335             .ai-btn { padding: 10px; }
+ 1336 
+ 1337             #decide-mode, #specs-mode, #workflows-mode { padding: 72px 16px 16px; }
+ 1338             .dashboard-grid { grid-template-columns: 1fr; height: auto; padding-bottom: 24px; gap: 12px; }
+ 1339             .kpi-card, .chart-card, .correlation-card, .alerts-card { grid-column: span 1; grid-row: span 1; }
+ 1340 
+ 1341             .explore-panel {
+ 1342                 position: fixed;
+ 1343                 top: auto;
+ 1344                 bottom: 0;
+ 1345                 left: 0;
+ 1346                 right: 0;
+ 1347                 width: 100%;
+ 1348                 max-height: 50vh;
+ 1349                 border-radius: 20px 20px 0 0;
+ 1350                 padding: 24px 20px;
+ 1351             }
+ 1352 
+ 1353             .ai-panel, .agent-panel { width: calc(100% - 32px); }
+ 1354             .agent-panel { left: 16px; top: auto; bottom: 16px; }
+ 1355 
+ 1356             .sense-overlay { flex-direction: column; gap: 12px; bottom: 16px; left: 16px; right: 16px; }
+ 1357             .sense-metrics, .sense-legend { width: 100%; }
+ 1358             .sense-legend { justify-content: center; flex-wrap: wrap; gap: 12px; }
+ 1359             .vr-indicator { bottom: 16px; left: 16px; }
+ 1360         }
+ 1361 
+ 1362         /* Scrollbar */
+ 1363         ::-webkit-scrollbar { width: 6px; height: 6px; }
+ 1364         ::-webkit-scrollbar-track { background: var(--bg-surface); border-radius: 3px; }
+ 1365         ::-webkit-scrollbar-thumb { background: var(--text-muted); border-radius: 3px; }
+ 1366         ::-webkit-scrollbar-thumb:hover { background: var(--text-secondary); }
+ 1367 
+ 1368         button:focus-visible, .region-item:focus-visible, .correlation-cell:focus-visible, .spec-item:focus-visible, .workflow-card:focus-visible {
+ 1369             outline: 2px solid var(--accent-pulse);
+ 1370             outline-offset: 2px;
+ 1371         }
+ 1372     </style>
+ 1373 </head>
+ 1374 <body>
+ 1375     <div id="app">
+ 1376         <!-- Header -->
+ 1377         <header class="header">
+ 1378             <div class="logo" id="logo" tabindex="0" role="button" aria-label="PulseWeaveVerse Home">
+ 1379                 <div class="logo-icon"></div>
+ 1380                 <div class="logo-text">PULSEWEAVE<span>VERSE</span></div>
+ 1381                 <span class="kiro-badge">KIRO</span>
+ 1382             </div>
+ 1383 
+ 1384             <nav class="mode-switcher" role="tablist" aria-label="Application modes">
+ 1385                 <button class="mode-btn active" data-mode="sense" role="tab" aria-selected="true">
+ 1386                     <svg class="mode-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
+ 1387                         <circle cx="12" cy="12" r="3"/>
+ 1388                         <path d="M12 2v4m0 12v4M2 12h4m12 0h4"/>
+ 1389                     </svg>
+ 1390                     <span>SENSE</span>
+ 1391                 </button>
+ 1392                 <button class="mode-btn" data-mode="decide" role="tab" aria-selected="false">
+ 1393                     <svg class="mode-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
+ 1394                         <rect x="3" y="3" width="7" height="7" rx="1"/>
+ 1395                         <rect x="14" y="3" width="7" height="7" rx="1"/>
+ 1396                         <rect x="3" y="14" width="7" height="7" rx="1"/>
+ 1397                         <rect x="14" y="14" width="7" height="7" rx="1"/>
+ 1398                     </svg>
+ 1399                     <span>DECIDE</span>
+ 1400                 </button>
+ 1401                 <button class="mode-btn" data-mode="explore" role="tab" aria-selected="false">
+ 1402                     <svg class="mode-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
+ 1403                         <circle cx="12" cy="12" r="10"/>
+ 1404                         <path d="M2 12h20M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/>
+ 1405                     </svg>
+ 1406                     <span>EXPLORE</span>
+ 1407                 </button>
+ 1408                 <button class="mode-btn" data-mode="specs" role="tab" aria-selected="false">
+ 1409                     <svg class="mode-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
+ 1410                         <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/>
+ 1411                         <polyline points="14 2 14 8 20 8"/>
+ 1412                         <line x1="16" y1="13" x2="8" y2="13"/>
+ 1413                         <line x1="16" y1="17" x2="8" y2="17"/>
+ 1414                     </svg>
+ 1415                     <span>SPECS</span>
+ 1416                 </button>
+ 1417                 <button class="mode-btn" data-mode="workflows" role="tab" aria-selected="false">
+ 1418                     <svg class="mode-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
+ 1419                         <polyline points="16 3 21 3 21 8"/>
+ 1420                         <line x1="4" y1="20" x2="21" y2="3"/>
+ 1421                         <polyline points="21 16 21 21 16 21"/>
+ 1422                         <line x1="15" y1="15" x2="21" y2="21"/>
+ 1423                         <line x1="4" y1="4" x2="9" y2="9"/>
+ 1424                     </svg>
+ 1425                     <span>WORKFLOWS</span>
+ 1426                 </button>
+ 1427             </nav>
+ 1428 
+ 1429             <div class="status">
+ 1430                 <div class="live-indicator" aria-live="polite">
+ 1431                     <div class="live-dot"></div>
+ 1432                     <span>STREAMING</span>
+ 1433                 </div>
+ 1434                 <button class="ai-btn" id="ai-insights-btn" aria-label="Open AI Insights panel">
+ 1435                     <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
+ 1436                         <path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"/>
+ 1437                     </svg>
+ 1438                     <span>AI INSIGHTS</span>
+ 1439                 </button>
+ 1440             </div>
+ 1441         </header>
+ 1442 
+ 1443         <!-- SENSE Mode -->
+ 1444         <section id="sense-mode" class="mode-container active" role="tabpanel">
+ 1445             <canvas id="sense-canvas"></canvas>
+ 1446             <div class="sense-overlay">
+ 1447                 <div class="sense-metrics">
+ 1448                     <div class="sense-metric">
+ 1449                         <span>SENTIMENT</span>
+ 1450                         <div class="metric-bar">
+ 1451                             <div class="metric-fill" id="sentiment-bar" style="width: 72%; background: linear-gradient(90deg, var(--accent-pulse), #0d9488);"></div>
+ 1452                         </div>
+ 1453                         <span id="sentiment-val">72%</span>
+ 1454                     </div>
+ 1455                     <div class="sense-metric">
+ 1456                         <span>LATENCY</span>
+ 1457                         <div class="metric-bar">
+ 1458                             <div class="metric-fill" id="latency-bar" style="width: 28%; background: linear-gradient(90deg, var(--accent-calm), #1d4ed8);"></div>
+ 1459                         </div>
+ 1460                         <span id="latency-val">28ms</span>
+ 1461                     </div>
+ 1462                     <div class="sense-metric">
+ 1463                         <span>TRAFFIC</span>
+ 1464                         <div class="metric-bar">
+ 1465                             <div class="metric-fill" id="traffic-bar" style="width: 85%; background: linear-gradient(90deg, var(--accent-data), #6b21a8);"></div>
+ 1466                         </div>
+ 1467                         <span id="traffic-val">8.5K/s</span>
+ 1468                     </div>
+ 1469                 </div>
+ 1470                 <div class="sense-legend">
+ 1471                     <div class="legend-item">
+ 1472                         <div class="legend-dot" style="background: var(--accent-pulse); color: var(--accent-pulse);"></div>
+ 1473                         <span>Positive Sentiment</span>
+ 1474                     </div>
+ 1475                     <div class="legend-item">
+ 1476                         <div class="legend-dot" style="background: var(--accent-heat); color: var(--accent-heat);"></div>
+ 1477                         <span>Negative Sentiment</span>
+ 1478                     </div>
+ 1479                     <div class="legend-item">
+ 1480                         <div class="legend-dot" style="background: var(--accent-data); color: var(--accent-data);"></div>
+ 1481                         <span>Infrastructure Load</span>
+ 1482                     </div>
+ 1483                 </div>
+ 1484             </div>
+ 1485         </section>
+ 1486 
+ 1487         <!-- DECIDE Mode -->
+ 1488         <section id="decide-mode" class="mode-container" role="tabpanel">
+ 1489             <div class="dashboard-grid">
+ 1490                 <div class="card kpi-card">
+ 1491                     <div class="card-header">
+ 1492                         <span class="card-title">Global Sentiment</span>
+ 1493                         <span class="card-badge" style="color: var(--accent-pulse);">● Live</span>
+ 1494                     </div>
+ 1495                     <div class="kpi-value" style="color: var(--accent-pulse);" id="kpi-sentiment">72.4</div>
+ 1496                     <div class="kpi-label">Composite Index</div>
+ 1497                     <div class="kpi-change positive" id="kpi-sentiment-change-container">
+ 1498                         <span>↑</span>
+ 1499                         <span id="kpi-sentiment-change">+3.2% from yesterday</span>
+ 1500                     </div>
+ 1501                 </div>
+ 1502 
+ 1503                 <div class="card kpi-card">
+ 1504                     <div class="card-header">
+ 1505                         <span class="card-title">Avg Latency</span>
+ 1506                         <span class="card-badge" id="latency-badge" style="color: var(--accent-calm);">OPTIMAL</span>
+ 1507                     </div>
+ 1508                     <div class="kpi-value" style="color: var(--accent-calm);" id="kpi-latency">28<span style="font-size: 20px;">ms</span></div>
+ 1509                     <div class="kpi-label">P95 Response Time</div>
+ 1510                     <div class="kpi-change positive" id="kpi-latency-change-container">
+ 1511                         <span>↓</span>
+ 1512                         <span id="kpi-latency-change">-12ms improvement</span>
+ 1513                     </div>
+ 1514                 </div>
+ 1515 
+ 1516                 <div class="card kpi-card">
+ 1517                     <div class="card-header">
+ 1518                         <span class="card-title">Uptime</span>
+ 1519                         <span class="card-badge" style="color: var(--accent-pulse);">SLA MET</span>
+ 1520                     </div>
+ 1521                     <div class="kpi-value" style="color: var(--text-primary);" id="kpi-uptime">99.97<span style="font-size: 20px;">%</span></div>
+ 1522                     <div class="kpi-label">30-Day Rolling</div>
+ 1523                     <div class="kpi-change positive">
+ 1524                         <span>↑</span>
+ 1525                         <span>0.02% above target</span>
+ 1526                     </div>
+ 1527                 </div>
+ 1528 
+ 1529                 <div class="card kpi-card">
+ 1530                     <div class="card-header">
+ 1531                         <span class="card-title">Active Regions</span>
+ 1532                         <span class="card-badge">GLOBAL</span>
+ 1533                     </div>
+ 1534                     <div class="kpi-value" id="kpi-regions">6</div>
+ 1535                     <div class="kpi-label">Data Centers Online</div>
+ 1536                     <div class="kpi-change neutral">
+ 1537                         <span>→</span>
+ 1538                         <span>All systems nominal</span>
+ 1539                     </div>
+ 1540                 </div>
+ 1541 
+ 1542                 <div class="card chart-card">
+ 1543                     <div class="card-header">
+ 1544                         <span class="card-title">Sentiment Over Time</span>
+ 1545                         <span class="card-badge">24H</span>
+ 1546                     </div>
+ 1547                     <div class="chart-container">
+ 1548                         <canvas id="sentiment-chart" class="chart-canvas"></canvas>
+ 1549                     </div>
+ 1550                 </div>
+ 1551 
+ 1552                 <div class="card chart-card">
+ 1553                     <div class="card-header">
+ 1554                         <span class="card-title">Infrastructure Load</span>
+ 1555                         <span class="card-badge">REAL-TIME</span>
+ 1556                     </div>
+ 1557                     <div class="chart-container">
+ 1558                         <canvas id="infra-chart" class="chart-canvas"></canvas>
+ 1559                     </div>
+ 1560                 </div>
+ 1561 
+ 1562                 <div class="card correlation-card">
+ 1563                     <div class="card-header">
+ 1564                         <span class="card-title">Correlation Matrix</span>
+ 1565                         <span class="card-badge">LIVE</span>
+ 1566                     </div>
+ 1567                     <div class="correlation-header-labels">
+ 1568                         <span>SENT</span>
+ 1569                         <span>LAT</span>
+ 1570                         <span>TRAF</span>
+ 1571                         <span>UPT</span>
+ 1572                     </div>
+ 1573                     <div class="correlation-matrix" id="correlation-matrix" role="grid"></div>
+ 1574                 </div>
+ 1575 
+ 1576                 <div class="card alerts-card">
+ 1577                     <div class="card-header">
+ 1578                         <span class="card-title">Active Alerts</span>
+ 1579                         <span class="card-badge" id="alert-count">3 Active</span>
+ 1580                     </div>
+ 1581                     <div class="alerts-list" id="alerts-list" role="log" aria-live="polite"></div>
+ 1582                 </div>
+ 1583             </div>
+ 1584         </section>
+ 1585 
+ 1586         <!-- EXPLORE Mode -->
+ 1587         <section id="explore-mode" class="mode-container" role="tabpanel">
+ 1588             <div id="globe-container"></div>
+ 1589 
+ 1590             <div class="explore-panel">
+ 1591                 <div class="panel-section">
+ 1592                     <div class="panel-title">Data Layers</div>
+ 1593                     <div class="data-layer-toggle" role="group">
+ 1594                         <button class="layer-btn active" data-layer="sentiment">SENTIMENT</button>
+ 1595                         <button class="layer-btn" data-layer="latency">LATENCY</button>
+ 1596                         <button class="layer-btn" data-layer="traffic">TRAFFIC</button>
+ 1597                         <button class="layer-btn" data-layer="correlation">CORRELATION</button>
+ 1598                     </div>
+ 1599                 </div>
+ 1600 
+ 1601                 <div class="panel-section">
+ 1602                     <div class="panel-title">Regional Overview</div>
+ 1603                     <div class="region-list" id="region-list" role="list"></div>
+ 1604                 </div>
+ 1605             </div>
+ 1606 
+ 1607             <div class="vr-indicator">
+ 1608                 <div class="vr-status">
+ 1609                     <div class="vr-status-dot"></div>
+ 1610                     <span>MR/VR Ready</span>
+ 1611                 </div>
+ 1612                 <button class="vr-btn" id="vr-mode-btn">Enter Immersive</button>
+ 1613             </div>
+ 1614         </section>
+ 1615 
+ 1616         <!-- SPECS Mode - Kiro Spec-Driven Development -->
+ 1617         <section id="specs-mode" class="mode-container" role="tabpanel">
+ 1618             <div class="specs-container">
+ 1619                 <aside class="specs-sidebar">
+ 1620                     <div class="spec-section-title">Specifications</div>
+ 1621                     <div class="spec-list" id="spec-list"></div>
+ 1622                 </aside>
+ 1623                 <main class="specs-main">
+ 1624                     <div class="spec-editor" id="spec-editor"></div>
+ 1625                 </main>
+ 1626             </div>
+ 1627         </section>
+ 1628 
+ 1629         <!-- WORKFLOWS Mode - Automated Workflows -->
+ 1630         <section id="workflows-mode" class="mode-container" role="tabpanel">
+ 1631             <div class="workflows-container">
+ 1632                 <div class="workflows-header">
+ 1633                     <h1 class="workflows-title">
+ 1634                         <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="var(--accent-warn)" stroke-width="2">
+ 1635                             <polyline points="16 3 21 3 21 8"/>
+ 1636                             <line x1="4" y1="20" x2="21" y2="3"/>
+ 1637                             <polyline points="21 16 21 21 16 21"/>
+ 1638                             <line x1="15" y1="15" x2="21" y2="21"/>
+ 1639                             <line x1="4" y1="4" x2="9" y2="9"/>
+ 1640                         </svg>
+ 1641                         Automated Workflows
+ 1642                     </h1>
+ 1643                     <div class="workflow-stats">
+ 1644                         <div class="workflow-stat">
+ 1645                             <div class="workflow-stat-value" style="color: var(--accent-kiro);" id="workflows-running">3</div>
+ 1646                             <div class="workflow-stat-label">Running</div>
+ 1647                         </div>
+ 1648                         <div class="workflow-stat">
+ 1649                             <div class="workflow-stat-value" style="color: var(--accent-warn);" id="workflows-paused">1</div>
+ 1650                             <div class="workflow-stat-label">Paused</div>
+ 1651                         </div>
+ 1652                         <div class="workflow-stat">
+ 1653                             <div class="workflow-stat-value" id="workflows-total">6</div>
+ 1654                             <div class="workflow-stat-label">Total</div>
+ 1655                         </div>
+ 1656                     </div>
+ 1657                 </div>
+ 1658                 <div class="workflows-grid" id="workflows-grid"></div>
+ 1659             </div>
+ 1660         </section>
+ 1661 
+ 1662         <!-- Agent Steering Panel -->
+ 1663         <div class="agent-panel" id="agent-panel" role="dialog">
+ 1664             <div class="agent-panel-header">
+ 1665                 <div class="agent-panel-title">
+ 1666                     <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
+ 1667                         <circle cx="12" cy="12" r="3"/>
+ 1668                         <path d="M12 2v4m0 12v4M2 12h4m12 0h4"/>
+ 1669                     </svg>
+ 1670                     AGENT STEERING
+ 1671                 </div>
+ 1672                 <button class="agent-panel-close" id="agent-panel-close">×</button>
+ 1673             </div>
+ 1674             <div class="agent-config">
+ 1675                 <div class="agent-config-group">
+ 1676                     <label class="agent-config-label">Agent Model</label>
+ 1677                     <select class="agent-config-select" id="agent-model">
+ 1678                         <option value="gpt5">GPT-5.1</option>
+ 1679                         <option value="claude">Claude-Sonnet-4.5</option>
+ 1680                         <option value="gemini">Gemini-3.0-Pro</option>
+ 1681                     </select>
+ 1682                 </div>
+ 1683                 <div class="agent-config-group">
+ 1684                     <label class="agent-config-label">Autonomy Level</label>
+ 1685                     <div class="agent-config-slider">
+ 1686                         <input type="range" min="0" max="100" value="70" id="agent-autonomy">
+ 1687                         <span class="agent-config-value" id="agent-autonomy-value">70%</span>
+ 1688                     </div>
+ 1689                 </div>
+ 1690                 <div class="agent-config-group">
+ 1691                     <label class="agent-config-label">Focus Area</label>
+ 1692                     <select class="agent-config-select" id="agent-focus">
+ 1693                         <option value="all">All Metrics</option>
+ 1694                         <option value="sentiment">Sentiment Analysis</option>
+ 1695                         <option value="performance">Performance Optimization</option>
+ 1696                         <option value="anomaly">Anomaly Detection</option>
+ 1697                     </select>
+ 1698                 </div>
+ 1699                 <div class="agent-config-group">
+ 1700                     <label class="agent-config-label">Steering Log</label>
+ 1701                     <div class="agent-steering-log" id="agent-log"></div>
+ 1702                 </div>
+ 1703             </div>
+ 1704         </div>
+ 1705 
+ 1706         <!-- AI Panel -->
+ 1707         <div class="ai-panel" id="ai-panel" role="dialog">
+ 1708             <div class="ai-panel-header">
+ 1709                 <div class="ai-panel-title">
+ 1710                     <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
+ 1711                         <path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"/>
+ 1712                     </svg>
+ 1713                     AI INSIGHT ENGINE
+ 1714                 </div>
+ 1715                 <button class="ai-panel-close" id="ai-panel-close">×</button>
+ 1716             </div>
+ 1717             <div class="ai-panel-content" id="ai-panel-content">
+ 1718                 <div class="ai-loading">
+ 1719                     <div class="ai-loading-dots"><span></span><span></span><span></span></div>
+ 1720                     <span>Analyzing correlation patterns...</span>
+ 1721                 </div>
+ 1722             </div>
+ 1723         </div>
+ 1724 
+ 1725         <!-- Toast -->
+ 1726         <div class="toast" id="toast" role="alert">
+ 1727             <div class="toast-icon">ℹ</div>
+ 1728             <span id="toast-message"></span>
+ 1729         </div>
+ 1730     </div>
+ 1731 
+ 1732     <script>
+ 1733         // ============================================
+ 1734         // KIRO SPEC SYSTEM - Spec-Driven Development
+ 1735         // ============================================
+ 1736         const KiroSpecs = {
+ 1737             specifications: [
+ 1738                 {
+ 1739                     id: 'data-schema',
+ 1740                     name: 'DataSchema',
+ 1741                     status: 'valid',
+ 1742                     description: 'Core data structure specifications',
+ 1743                     spec: {
+ 1744                         version: '1.0.0',
+ 1745                         types: {
+ 1746                             Metric: {
+ 1747                                 value: 'number',
+ 1748                                 unit: 'string',
+ 1749                                 timestamp: 'Date',
+ 1750                                 source: 'Region'
+ 1751                             },
+ 1752                             Region: {
+ 1753                                 id: 'string',
+ 1754                                 name: 'string',
+ 1755                                 lat: 'number',
+ 1756                                 lng: 'number',
+ 1757                                 color: 'HexColor'
+ 1758                             },
+ 1759                             Alert: {
+ 1760                                 id: 'string',
+ 1761                                 type: "'critical' | 'warning' | 'info'",
+ 1762                                 title: 'string',
+ 1763                                 desc: 'string',
+ 1764                                 timestamp: 'Date'
+ 1765                             }
+ 1766                         },
+ 1767                         constraints: {
+ 1768                             'Metric.value': { min: 0, max: 100 },
+ 1769                             'Region.lat': { min: -90, max: 90 },
+ 1770                             'Region.lng': { min: -180, max: 180 }
+ 1771                         }
+ 1772                     }
+ 1773                 },
+ 1774                 {
+ 1775                     id: 'api-contract',
+ 1776                     name: 'APIContract',
+ 1777                     status: 'valid',
+ 1778                     description: 'API endpoint specifications',
+ 1779                     spec: {
+ 1780                         version: '1.0.0',
+ 1781                         endpoints: {
+ 1782                             '/metrics': {
+ 1783                                 method: 'GET',
+ 1784                                 response: 'MetricResponse',
+ 1785                                 rateLimit: '100/min'
+ 1786                             },
+ 1787                             '/regions': {
+ 1788                                 method: 'GET',
+ 1789                                 response: 'Region[]',
+ 1790                                 cache: '5min'
+ 1791                             },
+ 1792                             '/alerts': {
+ 1793                                 method: 'GET | POST',
+ 1794                                 response: 'Alert[]',
+ 1795                                 websocket: true
+ 1796                             }
+ 1797                         }
+ 1798                     }
+ 1799                 },
+ 1800                 {
+ 1801                     id: 'visualization-rules',
+ 1802                     name: 'VisualizationRules',
+ 1803                     status: 'valid',
+ 1804                     description: 'Data visualization specifications',
+ 1805                     spec: {
+ 1806                         version: '1.0.0',
+ 1807                         rules: {
+ 1808                             sentiment: {
+ 1809                                 colorScale: ['#ff006e', '#ffbe0b', '#00f5d4'],
+ 1810                                 thresholds: [30, 60, 100],
+ 1811                                 animation: 'smooth'
+ 1812                             },
+ 1813                             latency: {
+ 1814                                 colorScale: ['#00f5d4', '#ffbe0b', '#ff006e'],
+ 1815                                 thresholds: [30, 60, 100],
+ 1816                                 unit: 'ms'
+ 1817                             },
+ 1818                             correlation: {
+ 1819                                 colorPositive: '#00f5d4',
+ 1820                                 colorNegative: '#ff006e',
+ 1821                                 range: [-1, 1]
+ 1822                             }
+ 1823                         }
+ 1824                     }
+ 1825                 },
+ 1826                 {
+ 1827                     id: 'agent-config',
+ 1828                     name: 'AgentConfiguration',
+ 1829                     status: 'warning',
+ 1830                     description: 'AI agent behavior specifications',
+ 1831                     spec: {
+ 1832                         version: '1.0.0',
+ 1833                         agents: {
+ 1834                             insights: {
+ 1835                                 model: 'GPT-5.1',
+ 1836                                 temperature: 0.7,
+ 1837                                 maxTokens: 500,
+ 1838                                 systemPrompt: 'Analyze data and provide actionable insights'
+ 1839                             },
+ 1840                             anomaly: {
+ 1841                                 model: 'Claude-Sonnet-4.5',
+ 1842                                 sensitivity: 0.85,
+ 1843                                 alertThreshold: 2.5
+ 1844                             }
+ 1845                         },
+ 1846                         steering: {
+ 1847                             autonomyLevels: ['manual', 'assisted', 'autonomous'],
+ 1848                             defaultLevel: 'assisted',
+ 1849                             escalationRules: 'defined'
+ 1850                         }
+ 1851                     }
+ 1852                 },
+ 1853                 {
+ 1854                     id: 'workflow-schema',
+ 1855                     name: 'WorkflowSchema',
+ 1856                     status: 'valid',
+ 1857                     description: 'Automated workflow specifications',
+ 1858                     spec: {
+ 1859                         version: '1.0.0',
+ 1860                         workflow: {
+ 1861                             triggers: ['schedule', 'event', 'threshold', 'manual'],
+ 1862                             actions: ['notify', 'scale', 'analyze', 'export'],
+ 1863                             conditions: {
+ 1864                                 operators: ['>', '<', '==', '!=', 'contains'],
+ 1865                                 logic: ['AND', 'OR', 'NOT']
+ 1866                             }
+ 1867                         },
+ 1868                         execution: {
+ 1869                             maxParallel: 5,
+ 1870                             timeout: '5m',
+ 1871                             retryPolicy: { maxRetries: 3, backoff: 'exponential' }
+ 1872                         }
+ 1873                     }
+ 1874                 }
+ 1875             ],
+ 1876 
+ 1877             activeSpec: null,
+ 1878 
+ 1879             init() {
+ 1880                 this.renderSpecList();
+ 1881                 this.selectSpec(this.specifications[0]);
+ 1882             },
+ 1883 
+ 1884             renderSpecList() {
+ 1885                 const list = document.getElementById('spec-list');
+ 1886                 list.innerHTML = this.specifications.map(spec => `
+ 1887                     <div class="spec-item ${spec.id === this.activeSpec?.id ? 'active' : ''}" data-spec-id="${spec.id}" tabindex="0">
+ 1888                         <div class="spec-item-header">
+ 1889                             <span class="spec-item-name">${spec.name}</span>
+ 1890                             <span class="spec-item-status ${spec.status}">${spec.status.toUpperCase()}</span>
+ 1891                         </div>
+ 1892                         <div class="spec-item-desc">${spec.description}</div>
+ 1893                     </div>
+ 1894                 `).join('');
+ 1895 
+ 1896                 list.querySelectorAll('.spec-item').forEach(item => {
+ 1897                     item.addEventListener('click', () => {
+ 1898                         const spec = this.specifications.find(s => s.id === item.dataset.specId);
+ 1899                         this.selectSpec(spec);
+ 1900                     });
+ 1901                 });
+ 1902             },
+ 1903 
+ 1904             selectSpec(spec) {
+ 1905                 this.activeSpec = spec;
+ 1906                 this.renderSpecList();
+ 1907                 this.renderSpecEditor(spec);
+ 1908             },
+ 1909 
+ 1910             renderSpecEditor(spec) {
+ 1911                 const editor = document.getElementById('spec-editor');
+ 1912                 const formattedSpec = this.formatSpec(spec.spec);
+ 1913 
+ 1914                 editor.innerHTML = `
+ 1915                     <div class="spec-editor-header">
+ 1916                         <div class="spec-editor-title">
+ 1917                             <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="var(--accent-kiro)" stroke-width="2">
+ 1918                                 <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/>
+ 1919                                 <polyline points="14 2 14 8 20 8"/>
+ 1920                             </svg>
+ 1921                             ${spec.name}
+ 1922                         </div>
+ 1923                         <div class="spec-editor-actions">
+ 1924                             <button class="spec-action-btn" onclick="KiroSpecs.validateSpec('${spec.id}')">Validate</button>
+ 1925                             <button class="spec-action-btn" onclick="KiroSpecs.generateFromSpec('${spec.id}')">Generate</button>
+ 1926                             <button class="spec-action-btn primary" onclick="KiroSpecs.deploySpec('${spec.id}')">Deploy</button>
+ 1927                         </div>
+ 1928                     </div>
+ 1929                     <div class="spec-code-block">${formattedSpec}</div>
+ 1930                 `;
+ 1931             },
+ 1932 
+ 1933             formatSpec(spec, indent = 0) {
+ 1934                 const spaces = '  '.repeat(indent);
+ 1935                 let result = '';
+ 1936 
+ 1937                 if (typeof spec === 'object' && spec !== null) {
+ 1938                     if (Array.isArray(spec)) {
+ 1939                         result += '[';
+ 1940                         spec.forEach((item, i) => {
+ 1941                             result += `\n${spaces}  ${this.formatSpec(item, indent + 1)}`;
+ 1942                             if (i < spec.length - 1) result += ',';
+ 1943                         });
+ 1944                         result += `\n${spaces}]`;
+ 1945                     } else {
+ 1946                         result += '{';
+ 1947                         const keys = Object.keys(spec);
+ 1948                         keys.forEach((key, i) => {
+ 1949                             result += `\n${spaces}  <span class="property">${key}</span>: ${this.formatSpec(spec[key], indent + 1)}`;
+ 1950                             if (i < keys.length - 1) result += ',';
+ 1951                         });
+ 1952                         result += `\n${spaces}}`;
+ 1953                     }
+ 1954                 } else if (typeof spec === 'string') {
+ 1955                     if (spec.includes("'") || spec.includes('|')) {
+ 1956                         result += `<span class="type">${spec}</span>`;
+ 1957                     } else {
+ 1958                         result += `<span class="string">"${spec}"</span>`;
+ 1959                     }
+ 1960                 } else if (typeof spec === 'number') {
+ 1961                     result += `<span class="number">${spec}</span>`;
+ 1962                 } else if (typeof spec === 'boolean') {
+ 1963                     result += `<span class="keyword">${spec}</span>`;
+ 1964                 }
+ 1965 
+ 1966                 return result;
+ 1967             },
+ 1968 
+ 1969             validateSpec(specId) {
+ 1970                 const spec = this.specifications.find(s => s.id === specId);
+ 1971                 App.showToast(`✓ ${spec.name} validated successfully`);
+ 1972                 AgentSteering.log('success', `Spec validation: ${spec.name} passed all checks`);
+ 1973             },
+ 1974 
+ 1975             generateFromSpec(specId) {
+ 1976                 const spec = this.specifications.find(s => s.id === specId);
+ 1977                 App.showToast(`Generating code from ${spec.name}...`);
+ 1978                 AgentSteering.log('info', `Code generation initiated for ${spec.name}`);
+ 1979             },
+ 1980 
+ 1981             deploySpec(specId) {
+ 1982                 const spec = this.specifications.find(s => s.id === specId);
+ 1983                 App.showToast(`🚀 ${spec.name} deployed to production`);
+ 1984                 AgentSteering.log('success', `Deployment complete: ${spec.name} is now live`);
+ 1985             }
+ 1986         };
+ 1987 
+ 1988         // ============================================
+ 1989         // KIRO WORKFLOWS - Automated Workflows
+ 1990         // ============================================
+ 1991         const KiroWorkflows = {
+ 1992             workflows: [
+ 1993                 {
+ 1994                     id: 'anomaly-detection',
+ 1995                     name: 'Anomaly Detection Pipeline',
+ 1996                     description: 'Monitors metrics for anomalies and triggers alerts',
+ 1997                     status: 'running',
+ 1998                     steps: [
+ 1999                         { type: 'trigger', name: 'Metric Stream', detail: 'Real-time data ingestion', status: 'complete' },
+ 2000                         { type: 'action', name: 'Statistical Analysis', detail: 'Z-score calculation', status: 'running' },
+ 2001                         { type: 'output', name: 'Alert Generation', detail: 'Slack + Email notifications', status: 'pending' }
+ 2002                     ],
+ 2003                     lastRun: '2 min ago',
+ 2004                     executions: 1247
+ 2005                 },
+ 2006                 {
+ 2007                     id: 'sentiment-aggregation',
+ 2008                     name: 'Sentiment Aggregation',
+ 2009                     description: 'Aggregates regional sentiment data hourly',
+ 2010                     status: 'running',
+ 2011                     steps: [
+ 2012                         { type: 'trigger', name: 'Cron Schedule', detail: 'Every hour at :00', status: 'complete' },
+ 2013                         { type: 'action', name: 'Data Collection', detail: 'Query all regions', status: 'complete' },
+ 2014                         { type: 'action', name: 'AI Analysis', detail: 'GPT-5.1 summarization', status: 'running' },
+ 2015                         { type: 'output', name: 'Dashboard Update', detail: 'Refresh KPI cards', status: 'pending' }
+ 2016                     ],
+ 2017                     lastRun: '45 min ago',
+ 2018                     executions: 892
+ 2019                 },
+ 2020                 {
+ 2021                     id: 'auto-scaling',
+ 2022                     name: 'Infrastructure Auto-Scaling',
+ 2023                     description: 'Automatically scales resources based on traffic',
+ 2024                     status: 'running',
+ 2025                     steps: [
+ 2026                         { type: 'trigger', name: 'Traffic Threshold', detail: '> 10K req/s', status: 'complete' },
+ 2027                         { type: 'action', name: 'Capacity Check', detail: 'Query available resources', status: 'complete' },
+ 2028                         { type: 'output', name: 'Scale Decision', detail: 'Horizontal pod autoscaling', status: 'complete' }
+ 2029                     ],
+ 2030                     lastRun: '5 min ago',
+ 2031                     executions: 156
+ 2032                 },
+ 2033                 {
+ 2034                     id: 'report-generation',
+ 2035                     name: 'Daily Report Generation',
+ 2036                     description: 'Generates executive summary reports',
+ 2037                     status: 'paused',
+ 2038                     steps: [
+ 2039                         { type: 'trigger', name: 'Daily Schedule', detail: '08:00 UTC', status: 'pending' },
+ 2040                         { type: 'action', name: 'Data Compilation', detail: '24h metrics snapshot', status: 'pending' },
+ 2041                         { type: 'action', name: 'AI Report Writing', detail: 'Claude analysis', status: 'pending' },
+ 2042                         { type: 'output', name: 'PDF Export', detail: 'Email to stakeholders', status: 'pending' }
+ 2043                     ],
+ 2044                     lastRun: '1 day ago',
+ 2045                     executions: 365
+ 2046                 },
+ 2047                 {
+ 2048                     id: 'correlation-monitor',
+ 2049                     name: 'Correlation Monitor',
+ 2050                     description: 'Tracks metric correlations and alerts on changes',
+ 2051                     status: 'idle',
+ 2052                     steps: [
+ 2053                         { type: 'trigger', name: 'Correlation Change', detail: '> 0.1 delta', status: 'pending' },
+ 2054                         { type: 'action', name: 'Impact Analysis', detail: 'Causal inference', status: 'pending' },
+ 2055                         { type: 'output', name: 'Insight Dispatch', detail: 'Push to AI panel', status: 'pending' }
+ 2056                     ],
+ 2057                     lastRun: '3 hours ago',
+ 2058                     executions: 89
+ 2059                 },
+ 2060                 {
+ 2061                     id: 'spec-sync',
+ 2062                     name: 'Spec Synchronization',
+ 2063                     description: 'Syncs specifications with deployment',
+ 2064                     status: 'idle',
+ 2065                     steps: [
+ 2066                         { type: 'trigger', name: 'Spec Update', detail: 'Git webhook', status: 'pending' },
+ 2067                         { type: 'action', name: 'Validation', detail: 'Schema validation', status: 'pending' },
+ 2068                         { type: 'action', name: 'Code Generation', detail: 'TypeScript interfaces', status: 'pending' },
+ 2069                         { type: 'output', name: 'Deploy', detail: 'Staging environment', status: 'pending' }
+ 2070                     ],
+ 2071                     lastRun: '2 hours ago',
+ 2072                     executions: 234
+ 2073                 }
+ 2074             ],
+ 2075 
+ 2076             init() {
+ 2077                 this.render();
+ 2078                 this.updateStats();
+ 2079             },
+ 2080 
+ 2081             render() {
+ 2082                 const grid = document.getElementById('workflows-grid');
+ 2083                 grid.innerHTML = this.workflows.map(wf => `
+ 2084                     <div class="workflow-card" data-workflow-id="${wf.id}" tabindex="0">
+ 2085                         <div class="workflow-card-header">
+ 2086                             <div>
+ 2087                                 <div class="workflow-card-title">${wf.name}</div>
+ 2088                                 <div class="workflow-card-desc">${wf.description}</div>
+ 2089                             </div>
+ 2090                             <div class="workflow-status ${wf.status}">
+ 2091                                 <div class="workflow-status-dot"></div>
+ 2092                                 ${wf.status.toUpperCase()}
+ 2093                             </div>
+ 2094                         </div>
+ 2095                         <div class="workflow-steps">
+ 2096                             ${wf.steps.map(step => `
+ 2097                                 <div class="workflow-step">
+ 2098                                     <div class="workflow-step-icon ${step.type}">${step.type === 'trigger' ? '⚡' : step.type === 'action' ? '⚙' : '📤'}</div>
+ 2099                                     <div class="workflow-step-content">
+ 2100                                         <div class="workflow-step-name">${step.name}</div>
+ 2101                                         <div class="workflow-step-detail">${step.detail}</div>
+ 2102                                     </div>
+ 2103                                     <div class="workflow-step-status ${step.status}">${step.status === 'complete' ? '✓' : step.status === 'running' ? '◌' : '○'}</div>
+ 2104                                 </div>
+ 2105                             `).join('')}
+ 2106                         </div>
+ 2107                         <div class="workflow-actions">
+ 2108                             ${wf.status === 'running' 
+ 2109                                 ? `<button class="workflow-action-btn stop" onclick="KiroWorkflows.stop('${wf.id}')">Stop</button>`
+ 2110                                 : `<button class="workflow-action-btn run" onclick="KiroWorkflows.run('${wf.id}')">Run</button>`
+ 2111                             }
+ 2112                             <button class="workflow-action-btn" onclick="KiroWorkflows.configure('${wf.id}')">Configure</button>
+ 2113                             <button class="workflow-action-btn" onclick="KiroWorkflows.viewLogs('${wf.id}')">Logs</button>
+ 2114                         </div>
+ 2115                     </div>
+ 2116                 `).join('');
+ 2117             },
+ 2118 
+ 2119             updateStats() {
+ 2120                 const running = this.workflows.filter(w => w.status === 'running').length;
+ 2121                 const paused = this.workflows.filter(w => w.status === 'paused').length;
+ 2122                 document.getElementById('workflows-running').textContent = running;
+ 2123                 document.getElementById('workflows-paused').textContent = paused;
+ 2124                 document.getElementById('workflows-total').textContent = this.workflows.length;
+ 2125             },
+ 2126 
+ 2127             run(id) {
+ 2128                 const wf = this.workflows.find(w => w.id === id);
+ 2129                 wf.status = 'running';
+ 2130                 this.render();
+ 2131                 this.updateStats();
+ 2132                 App.showToast(`▶ ${wf.name} started`);
+ 2133                 AgentSteering.log('success', `Workflow started: ${wf.name}`);
+ 2134             },
+ 2135 
+ 2136             stop(id) {
+ 2137                 const wf = this.workflows.find(w => w.id === id);
+ 2138                 wf.status = 'idle';
+ 2139                 this.render();
+ 2140                 this.updateStats();
+ 2141                 App.showToast(`⏹ ${wf.name} stopped`);
+ 2142                 AgentSteering.log('warning', `Workflow stopped: ${wf.name}`);
+ 2143             },
+ 2144 
+ 2145             configure(id) {
+ 2146                 const wf = this.workflows.find(w => w.id === id);
+ 2147                 App.showToast(`Opening configuration for ${wf.name}...`);
+ 2148             },
+ 2149 
+ 2150             viewLogs(id) {
+ 2151                 const wf = this.workflows.find(w => w.id === id);
+ 2152                 App.showToast(`Viewing logs for ${wf.name}`);
+ 2153             }
+ 2154         };
+ 2155 
+ 2156         // ============================================
+ 2157         // AGENT STEERING - AI Agent Control
+ 2158         // ============================================
+ 2159         const AgentSteering = {
+ 2160             isOpen: false,
+ 2161             logs: [],
+ 2162 
+ 2163             init() {
+ 2164                 document.getElementById('agent-autonomy').addEventListener('input', (e) => {
+ 2165                     document.getElementById('agent-autonomy-value').textContent = e.target.value + '%';
+ 2166                     this.log('info', `Autonomy level adjusted to ${e.target.value}%`);
+ 2167                 });
+ 2168 
+ 2169                 document.getElementById('agent-model').addEventListener('change', (e) => {
+ 2170                     this.log('info', `Agent model switched to ${e.target.options[e.target.selectedIndex].text}`);
+ 2171                 });
+ 2172 
+ 2173                 document.getElementById('agent-focus').addEventListener('change', (e) => {
+ 2174                     this.log('info', `Focus area changed to ${e.target.options[e.target.selectedIndex].text}`);
+ 2175                 });
+ 2176 
+ 2177                 document.getElementById('agent-panel-close').addEventListener('click', () => this.close());
+ 2178 
+ 2179                 // Initial logs
+ 2180                 this.log('success', 'Agent steering initialized');
+ 2181                 this.log('info', 'Connected to GPT-5.1 model');
+ 2182                 this.log('info', 'Monitoring all metrics');
+ 2183             },
+ 2184 
+ 2185             toggle() {
+ 2186                 if (this.isOpen) this.close();
+ 2187                 else this.open();
+ 2188             },
+ 2189 
+ 2190             open() {
+ 2191                 this.isOpen = true;
+ 2192                 document.getElementById('agent-panel').classList.add('visible');
+ 2193             },
+ 2194 
+ 2195             close() {
+ 2196                 this.isOpen = false;
+ 2197                 document.getElementById('agent-panel').classList.remove('visible');
+ 2198             },
+ 2199 
+ 2200             log(type, message) {
+ 2201                 const timestamp = new Date().toLocaleTimeString([], { hour: '2-digit', minute: '2-digit', second: '2-digit' });
+ 2202                 this.logs.unshift({ type, message, timestamp });
+ 2203                 if (this.logs.length > 50) this.logs.pop();
+ 2204                 this.renderLogs();
+ 2205             },
+ 2206 
+ 2207             renderLogs() {
+ 2208                 const logEl = document.getElementById('agent-log');
+ 2209                 if (!logEl) return;
+ 2210                 logEl.innerHTML = this.logs.slice(0, 10).map(log => `
+ 2211                     <div class="agent-log-entry ${log.type}">
+ 2212                         <span class="timestamp">[${log.timestamp}]</span>
+ 2213                         <span class="message">${log.message}</span>
+ 2214                     </div>
+ 2215                 `).join('');
+ 2216             }
+ 2217         };
+ 2218 
+ 2219         // ============================================
+ 2220         // DATA FABRIC - Shared Data Specifications
+ 2221         // ============================================
+ 2222         const DataFabric = {
+ 2223             schema: {
+ 2224                 sentiment: { min: 0, max: 100, unit: '%', refresh: 2000 },
+ 2225                 latency: { min: 5, max: 200, unit: 'ms', refresh: 1000 },
+ 2226                 traffic: { min: 0, max: 15000, unit: 'req/s', refresh: 500 },
+ 2227                 uptime: { min: 99, max: 100, unit: '%', refresh: 5000 }
+ 2228             },
+ 2229 
+ 2230             regions: [
+ 2231                 { id: 'na', name: 'North America', lat: 40, lng: -100, color: '#00f5d4' },
+ 2232                 { id: 'eu', name: 'Europe', lat: 50, lng: 10, color: '#3a86ff' },
+ 2233                 { id: 'asia', name: 'Asia Pacific', lat: 35, lng: 105, color: '#8338ec' },
+ 2234                 { id: 'latam', name: 'Latin America', lat: -15, lng: -60, color: '#fb5607' },
+ 2235                 { id: 'mea', name: 'Middle East & Africa', lat: 25, lng: 45, color: '#ff006e' },
+ 2236                 { id: 'oceania', name: 'Oceania', lat: -25, lng: 135, color: '#ffbe0b' }
+ 2237             ],
+ 2238 
+ 2239             state: {
+ 2240                 global: { sentiment: 72, latency: 28, traffic: 8500, uptime: 99.97 },
+ 2241                 regional: {},
+ 2242                 timeSeries: { sentiment: [], latency: [], traffic: [] },
+ 2243                 correlations: {
+ 2244                     'sentiment-latency': -0.72,
+ 2245                     'sentiment-traffic': 0.45,
+ 2246                     'sentiment-uptime': 0.68,
+ 2247                     'latency-traffic': 0.81,
+ 2248                     'latency-uptime': -0.55,
+ 2249                     'traffic-uptime': -0.32
+ 2250                 },
+ 2251                 alerts: []
+ 2252             },
+ 2253 
+ 2254             init() {
+ 2255                 this.regions.forEach(region => {
+ 2256                     this.state.regional[region.id] = {
+ 2257                         sentiment: 60 + Math.random() * 30,
+ 2258                         latency: 15 + Math.random() * 50,
+ 2259                         traffic: 500 + Math.random() * 3000,
+ 2260                         uptime: 99.5 + Math.random() * 0.5
+ 2261                     };
+ 2262                 });
+ 2263 
+ 2264                 for (let i = 24; i >= 0; i--) {
+ 2265                     this.state.timeSeries.sentiment.push(65 + Math.random() * 20);
+ 2266                     this.state.timeSeries.latency.push(20 + Math.random() * 30);
+ 2267                     this.state.timeSeries.traffic.push(5000 + Math.random() * 5000);
+ 2268                 }
+ 2269 
+ 2270                 for (let i = 0; i < 3; i++) this.generateAlerts();
+ 2271             },
+ 2272 
+ 2273             update() {
+ 2274                 const { state } = this;
+ 2275                 state.global.sentiment = this.smoothUpdate(state.global.sentiment, 50, 90, 2);
+ 2276                 state.global.latency = this.smoothUpdate(state.global.latency, 15, 60, 3);
+ 2277                 state.global.traffic = this.smoothUpdate(state.global.traffic, 5000, 12000, 200);
+ 2278 
+ 2279                 this.regions.forEach(region => {
+ 2280                     const r = state.regional[region.id];
+ 2281                     r.sentiment = this.smoothUpdate(r.sentiment, 40, 95, 3);
+ 2282                     r.latency = this.smoothUpdate(r.latency, 10, 80, 5);
+ 2283                     r.traffic = this.smoothUpdate(r.traffic, 300, 4000, 100);
+ 2284                 });
+ 2285 
+ 2286                 state.timeSeries.sentiment.push(state.global.sentiment);
+ 2287                 state.timeSeries.sentiment.shift();
+ 2288                 state.timeSeries.latency.push(state.global.latency);
+ 2289                 state.timeSeries.latency.shift();
+ 2290                 state.timeSeries.traffic.push(state.global.traffic);
+ 2291                 state.timeSeries.traffic.shift();
+ 2292 
+ 2293                 Object.keys(state.correlations).forEach(key => {
+ 2294                     state.correlations[key] = Math.max(-1, Math.min(1, state.correlations[key] + (Math.random() - 0.5) * 0.05));
+ 2295                 });
+ 2296 
+ 2297                 if (Math.random() < 0.03) this.generateAlerts();
+ 2298                 return state;
+ 2299             },
+ 2300 
+ 2301             smoothUpdate(current, min, max, delta) {
+ 2302                 return Math.max(min, Math.min(max, current + (Math.random() - 0.5) * delta * 2));
+ 2303             },
+ 2304 
+ 2305             generateAlerts() {
+ 2306                 const alertTypes = [
+ 2307                     { type: 'critical', title: 'Latency Spike Detected', desc: 'EU-WEST-1 experiencing 3x normal latency' },
+ 2308                     { type: 'warning', title: 'Sentiment Drop Alert', desc: 'APAC region showing 15% sentiment decline' },
+ 2309                     { type: 'info', title: 'Traffic Surge Incoming', desc: 'Predicted 40% traffic increase in next 2 hours' },
+ 2310                     { type: 'critical', title: 'Correlation Anomaly', desc: 'Unusual inverse correlation detected in NA region' },
+ 2311                     { type: 'warning', title: 'Infrastructure Strain', desc: 'CPU utilization approaching threshold in 3 zones' },
+ 2312                     { type: 'info', title: 'Sentiment Recovery', desc: 'Global sentiment index recovering after morning dip' }
+ 2313                 ];
+ 2314                 const template = alertTypes[Math.floor(Math.random() * alertTypes.length)];
+ 2315                 this.state.alerts.unshift({ ...template, time: new Date().toLocaleTimeString([], { hour: '2-digit', minute: '2-digit' }), id: Date.now() });
+ 2316                 if (this.state.alerts.length > 8) this.state.alerts.pop();
+ 2317             },
+ 2318 
+ 2319             getCorrelation(m1, m2) {
+ 2320                 return this.state.correlations[[m1, m2].sort().join('-')] || 0;
+ 2321             }
+ 2322         };
+ 2323 
+ 2324         // ============================================
+ 2325         // SENSE MODE
+ 2326         // ============================================
+ 2327         const SenseMode = {
+ 2328             canvas: null, ctx: null, particles: [], waves: [],
+ 2329 
+ 2330             init() {
+ 2331                 this.canvas = document.getElementById('sense-canvas');
+ 2332                 this.ctx = this.canvas.getContext('2d');
+ 2333                 this.resize();
+ 2334                 window.addEventListener('resize', () => this.resize());
+ 2335                 this.createParticles();
+ 2336                 this.createWaves();
+ 2337             },
+ 2338 
+ 2339             resize() {
+ 2340                 this.canvas.width = window.innerWidth;
+ 2341                 this.canvas.height = window.innerHeight;
+ 2342                 this.createParticles();
+ 2343                 this.createWaves();
+ 2344             },
+ 2345 
+ 2346             createParticles() {
+ 2347                 this.particles = [];
+ 2348                 const count = Math.min(150, Math.floor(window.innerWidth / 10));
+ 2349                 for (let i = 0; i < count; i++) {
+ 2350                     this.particles.push({
+ 2351                         x: Math.random() * this.canvas.width,
+ 2352                         y: Math.random() * this.canvas.height,
+ 2353                         vx: (Math.random() - 0.5) * 0.5,
+ 2354                         vy: (Math.random() - 0.5) * 0.5,
+ 2355                         radius: 1.5 + Math.random() * 2.5,
+ 2356                         type: Math.random() < 0.6 ? 'sentiment' : (Math.random() < 0.5 ? 'latency' : 'traffic')
+ 2357                     });
+ 2358                 }
+ 2359             },
+ 2360 
+ 2361             createWaves() {
+ 2362                 this.waves = [];
+ 2363                 for (let i = 0; i < 3; i++) {
+ 2364                     this.waves.push({
+ 2365                         amplitude: 30 + i * 20,
+ 2366                         frequency: 0.002 + i * 0.001,
+ 2367                         phase: i * Math.PI / 3,
+ 2368                         speed: 0.02 - i * 0.005,
+ 2369                         y: this.canvas.height * (0.4 + i * 0.15)
+ 2370                     });
+ 2371                 }
+ 2372             },
+ 2373 
+ 2374             render(data) {
+ 2375                 const { ctx, canvas } = this;
+ 2376                 ctx.fillStyle = 'rgba(10, 10, 15, 0.12)';
+ 2377                 ctx.fillRect(0, 0, canvas.width, canvas.height);
+ 2378 
+ 2379                 this.waves.forEach((wave, i) => {
+ 2380                     wave.phase += wave.speed;
+ 2381                     ctx.beginPath();
+ 2382                     ctx.moveTo(0, wave.y);
+ 2383                     for (let x = 0; x <= canvas.width; x += 5) {
+ 2384                         ctx.lineTo(x, wave.y + Math.sin(x * wave.frequency + wave.phase) * wave.amplitude * (data.global.sentiment / 100));
+ 2385                     }
+ 2386                     ctx.strokeStyle = i === 0 ? 'rgba(0, 245, 212, 0.35)' : i === 1 ? 'rgba(131, 56, 236, 0.25)' : 'rgba(255, 0, 110, 0.18)';
+ 2387                     ctx.lineWidth = 2.5;
+ 2388                     ctx.stroke();
+ 2389                 });
+ 2390 
+ 2391                 const colors = { sentiment: data.global.sentiment > 60 ? '#00f5d4' : '#ff006e', latency: '#3a86ff', traffic: '#8338ec' };
+ 2392 
+ 2393                 this.particles.forEach(p => {
+ 2394                     p.vx += ((data.global.sentiment - 50) / 500) * (Math.random() - 0.5);
+ 2395                     p.vy += (data.global.latency / 1000) * (Math.random() - 0.5);
+ 2396                     p.vx *= 0.99; p.vy *= 0.99;
+ 2397                     p.x += p.vx; p.y += p.vy;
+ 2398                     if (p.x < 0) p.x = canvas.width; if (p.x > canvas.width) p.x = 0;
+ 2399                     if (p.y < 0) p.y = canvas.height; if (p.y > canvas.height) p.y = 0;
+ 2400 
+ 2401                     ctx.beginPath();
+ 2402                     ctx.arc(p.x, p.y, p.radius, 0, Math.PI * 2);
+ 2403                     ctx.fillStyle = colors[p.type];
+ 2404                     ctx.shadowColor = colors[p.type];
+ 2405                     ctx.shadowBlur = 8;
+ 2406                     ctx.fill();
+ 2407                     ctx.shadowBlur = 0;
+ 2408 
+ 2409                     this.particles.forEach(p2 => {
+ 2410                         const dist = Math.sqrt((p.x - p2.x) ** 2 + (p.y - p2.y) ** 2);
+ 2411                         if (dist < 100 && dist > 0) {
+ 2412                             ctx.beginPath();
+ 2413                             ctx.moveTo(p.x, p.y);
+ 2414                             ctx.lineTo(p2.x, p2.y);
+ 2415                             ctx.strokeStyle = `rgba(255, 255, 255, ${0.08 * (1 - dist / 100)})`;
+ 2416                             ctx.lineWidth = 0.5;
+ 2417                             ctx.stroke();
+ 2418                         }
+ 2419                     });
+ 2420                 });
+ 2421 
+ 2422                 document.getElementById('sentiment-bar').style.width = data.global.sentiment + '%';
+ 2423                 document.getElementById('sentiment-val').textContent = Math.round(data.global.sentiment) + '%';
+ 2424                 document.getElementById('latency-bar').style.width = Math.min(100, data.global.latency * 1.5) + '%';
+ 2425                 document.getElementById('latency-val').textContent = Math.round(data.global.latency) + 'ms';
+ 2426                 document.getElementById('traffic-bar').style.width = (data.global.traffic / 120) + '%';
+ 2427                 document.getElementById('traffic-val').textContent = (data.global.traffic / 1000).toFixed(1) + 'K/s';
+ 2428             }
+ 2429         };
+ 2430 
+ 2431         // ============================================
+ 2432         // DECIDE MODE
+ 2433         // ============================================
+ 2434         const DecideMode = {
+ 2435             init() {
+ 2436                 this.sentimentCtx = document.getElementById('sentiment-chart').getContext('2d');
+ 2437                 this.infraCtx = document.getElementById('infra-chart').getContext('2d');
+ 2438                 this.initCorrelationMatrix();
+ 2439             },
+ 2440 
+ 2441             initCorrelationMatrix() {
+ 2442                 const matrix = document.getElementById('correlation-matrix');
+ 2443                 const metrics = ['sentiment', 'latency', 'traffic', 'uptime'];
+ 2444                 const labels = ['SENT', 'LAT', 'TRAF', 'UPT'];
+ 2445                 matrix.innerHTML = '';
+ 2446                 metrics.forEach((m1, i) => {
+ 2447                     metrics.forEach((m2, j) => {
+ 2448                         const cell = document.createElement('div');
+ 2449                         cell.className = 'correlation-cell';
+ 2450                         cell.setAttribute('tabindex', '0');
+ 2451                         cell.addEventListener('click', () => {
+ 2452                             App.showToast(`${labels[i]} ↔ ${labels[j]}: ${(i === j ? 1 : DataFabric.getCorrelation(m1, m2)).toFixed(3)} correlation`);
+ 2453                         });
+ 2454                         matrix.appendChild(cell);
+ 2455                     });
+ 2456                 });
+ 2457             },
+ 2458 
+ 2459             render(data) {
+ 2460                 this.renderChart(this.sentimentCtx, data.timeSeries.sentiment, '#00f5d4');
+ 2461                 this.renderChart(this.infraCtx, data.timeSeries.traffic.map(t => t / 100), '#8338ec');
+ 2462                 this.renderCorrelationMatrix(data);
+ 2463                 this.renderAlerts(data.alerts);
+ 2464                 this.updateKPIs(data);
+ 2465             },
+ 2466 
+ 2467             renderChart(ctx, dataPoints, color) {
+ 2468                 const canvas = ctx.canvas;
+ 2469                 const rect = canvas.parentElement.getBoundingClientRect();
+ 2470                 canvas.width = rect.width; canvas.height = rect.height;
+ 2471                 const padding = { top: 20, right: 20, bottom: 30, left: 40 };
+ 2472                 const width = canvas.width - padding.left - padding.right;
+ 2473                 const height = canvas.height - padding.top - padding.bottom;
+ 2474                 ctx.clearRect(0, 0, canvas.width, canvas.height);
+ 2475                 if (dataPoints.length < 2) return;
+ 2476 
+ 2477                 const max = Math.max(...dataPoints) * 1.1;
+ 2478                 const min = Math.min(...dataPoints) * 0.9;
+ 2479                 const range = max - min || 1;
+ 2480 
+ 2481                 ctx.strokeStyle = 'rgba(255, 255, 255, 0.05)';
+ 2482                 for (let i = 0; i <= 4; i++) {
+ 2483                     const y = padding.top + (height / 4) * i;
+ 2484                     ctx.beginPath(); ctx.moveTo(padding.left, y); ctx.lineTo(canvas.width - padding.right, y); ctx.stroke();
+ 2485                 }
+ 2486 
+ 2487                 const gradient = ctx.createLinearGradient(0, padding.top, 0, canvas.height - padding.bottom);
+ 2488                 gradient.addColorStop(0, color + '40'); gradient.addColorStop(1, color + '00');
+ 2489                 ctx.beginPath(); ctx.moveTo(padding.left, canvas.height - padding.bottom);
+ 2490                 dataPoints.forEach((val, i) => ctx.lineTo(padding.left + (width / (dataPoints.length - 1)) * i, padding.top + height - ((val - min) / range) * height));
+ 2491                 ctx.lineTo(canvas.width - padding.right, canvas.height - padding.bottom);
+ 2492                 ctx.closePath(); ctx.fillStyle = gradient; ctx.fill();
+ 2493 
+ 2494                 ctx.beginPath();
+ 2495                 dataPoints.forEach((val, i) => {
+ 2496                     const x = padding.left + (width / (dataPoints.length - 1)) * i;
+ 2497                     const y = padding.top + height - ((val - min) / range) * height;
+ 2498                     if (i === 0) ctx.moveTo(x, y); else ctx.lineTo(x, y);
+ 2499                 });
+ 2500                 ctx.strokeStyle = color; ctx.lineWidth = 2.5; ctx.lineCap = 'round'; ctx.stroke();
+ 2501 
+ 2502                 const lastX = canvas.width - padding.right;
+ 2503                 const lastY = padding.top + height - ((dataPoints[dataPoints.length - 1] - min) / range) * height;
+ 2504                 ctx.beginPath(); ctx.arc(lastX, lastY, 6, 0, Math.PI * 2);
+ 2505                 ctx.fillStyle = color; ctx.shadowColor = color; ctx.shadowBlur = 12; ctx.fill(); ctx.shadowBlur = 0;
+ 2506                 ctx.beginPath(); ctx.arc(lastX, lastY, 3, 0, Math.PI * 2); ctx.fillStyle = '#fff'; ctx.fill();
+ 2507             },
+ 2508 
+ 2509             renderCorrelationMatrix(data) {
+ 2510                 const cells = document.querySelectorAll('.correlation-cell');
+ 2511                 const metrics = ['sentiment', 'latency', 'traffic', 'uptime'];
+ 2512                 cells.forEach((cell, index) => {
+ 2513                     const i = Math.floor(index / 4), j = index % 4;
+ 2514                     const corr = i === j ? 1 : DataFabric.getCorrelation(metrics[i], metrics[j]);
+ 2515                     const absCorr = Math.abs(corr);
+ 2516                     cell.style.background = `hsla(${corr >= 0 ? 170 : 340}, ${70 + absCorr * 20}%, ${35 + absCorr * 15}%, ${0.3 + absCorr * 0.5})`;
+ 2517                     cell.textContent = corr.toFixed(2);
+ 2518                 });
+ 2519             },
+ 2520 
+ 2521             renderAlerts(alerts) {
+ 2522                 const list = document.getElementById('alerts-list');
+ 2523                 const count = document.getElementById('alert-count');
+ 2524                 count.textContent = `${alerts.length} Active`;
+ 2525                 count.style.color = alerts.some(a => a.type === 'critical') ? 'var(--accent-heat)' : alerts.some(a => a.type === 'warning') ? 'var(--accent-warn)' : 'var(--text-secondary)';
+ 2526                 list.innerHTML = alerts.map(alert => `
+ 2527                     <div class="alert-item ${alert.type}" tabindex="0">
+ 2528                         <div class="alert-icon">${alert.type === 'critical' ? '!' : alert.type === 'warning' ? '⚠' : 'ℹ'}</div>
+ 2529                         <div class="alert-content"><div class="alert-title">${alert.title}</div><div class="alert-desc">${alert.desc}</div></div>
+ 2530                         <div class="alert-time">${alert.time}</div>
+ 2531                     </div>
+ 2532                 `).join('');
+ 2533             },
+ 2534 
+ 2535             updateKPIs(data) {
+ 2536                 document.getElementById('kpi-sentiment').textContent = data.global.sentiment.toFixed(1);
+ 2537                 const sentimentChange = document.getElementById('kpi-sentiment-change-container');
+ 2538                 sentimentChange.className = `kpi-change ${data.global.sentiment > 70 ? 'positive' : data.global.sentiment < 55 ? 'negative' : 'neutral'}`;
+ 2539                 sentimentChange.innerHTML = `<span>${data.global.sentiment > 70 ? '↑' : data.global.sentiment < 55 ? '↓' : '→'}</span><span>${data.global.sentiment > 70 ? 'Trending positive' : data.global.sentiment < 55 ? 'Below target' : 'Stable'}</span>`;
+ 2540 
+ 2541                 document.getElementById('kpi-latency').innerHTML = Math.round(data.global.latency) + '<span style="font-size: 20px;">ms</span>';
+ 2542                 const latencyBadge = document.getElementById('latency-badge');
+ 2543                 latencyBadge.textContent = data.global.latency < 35 ? 'OPTIMAL' : data.global.latency > 50 ? 'ELEVATED' : 'NORMAL';
+ 2544                 latencyBadge.style.color = data.global.latency < 35 ? 'var(--accent-pulse)' : data.global.latency > 50 ? 'var(--accent-warn)' : 'var(--accent-calm)';
+ 2545             }
+ 2546         };
+ 2547 
+ 2548         // ============================================
+ 2549         // EXPLORE MODE
+ 2550         // ============================================
+ 2551         const ExploreMode = {
+ 2552             scene: null, camera: null, renderer: null, globe: null, markers: [], rings: [], currentLayer: 'sentiment', isInitialized: false,
+ 2553 
+ 2554             init() {
+ 2555                 if (this.isInitialized) return;
+ 2556                 const container = document.getElementById('globe-container');
+ 2557                 const width = container.clientWidth, height = container.clientHeight;
+ 2558 
+ 2559                 this.scene = new THREE.Scene();
+ 2560                 this.scene.background = new THREE.Color(0x0a0a0f);
+ 2561                 this.camera = new THREE.PerspectiveCamera(45, width / height, 0.1, 1000);
+ 2562                 this.camera.position.z = 3;
+ 2563                 this.renderer = new THREE.WebGLRenderer({ antialias: true, alpha: true });
+ 2564                 this.renderer.setSize(width, height);
+ 2565                 this.renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2));
+ 2566                 container.appendChild(this.renderer.domElement);
+ 2567 
+ 2568                 this.globe = new THREE.Mesh(
+ 2569                     new THREE.SphereGeometry(1, 64, 64),
+ 2570                     new THREE.MeshBasicMaterial({ color: 0x1a1a25, wireframe: true, transparent: true, opacity: 0.4 })
+ 2571                 );
+ 2572                 this.scene.add(this.globe);
+ 2573                 this.globe.add(new THREE.Mesh(new THREE.SphereGeometry(0.98, 64, 64), new THREE.MeshBasicMaterial({ color: 0x00f5d4, transparent: true, opacity: 0.03 })));
+ 2574 
+ 2575                 this.createMarkers();
+ 2576                 window.addEventListener('resize', () => this.onResize());
+ 2577                 this.setupInteraction(container);
+ 2578                 this.renderRegionList();
+ 2579 
+ 2580                 document.querySelectorAll('.layer-btn').forEach(btn => {
+ 2581                     btn.addEventListener('click', () => {
+ 2582                         document.querySelectorAll('.layer-btn').forEach(b => b.classList.remove('active'));
+ 2583                         btn.classList.add('active');
+ 2584                         this.currentLayer = btn.dataset.layer;
+ 2585                         App.showToast(`Viewing ${btn.dataset.layer.toUpperCase()} layer`);
+ 2586                     });
+ 2587                 });
+ 2588 
+ 2589                 this.isInitialized = true;
+ 2590             },
+ 2591 
+ 2592             createMarkers() {
+ 2593                 DataFabric.regions.forEach(region => {
+ 2594                     const phi = (90 - region.lat) * (Math.PI / 180);
+ 2595                     const theta = (region.lng + 180) * (Math.PI / 180);
+ 2596                     const x = -Math.sin(phi) * Math.cos(theta), y = Math.cos(phi), z = Math.sin(phi) * Math.sin(theta);
+ 2597 
+ 2598                     const marker = new THREE.Mesh(new THREE.SphereGeometry(0.025, 16, 16), new THREE.MeshBasicMaterial({ color: region.color }));
+ 2599                     marker.position.set(x * 1.02, y * 1.02, z * 1.02);
+ 2600                     marker.userData = { region: region.id };
+ 2601                     this.globe.add(marker);
+ 2602                     this.markers.push(marker);
+ 2603 
+ 2604                     const ring = new THREE.Mesh(new THREE.RingGeometry(0.04, 0.06, 32), new THREE.MeshBasicMaterial({ color: region.color, transparent: true, opacity: 0.6, side: THREE.DoubleSide }));
+ 2605                     ring.position.copy(marker.position);
+ 2606                     ring.lookAt(0, 0, 0);
+ 2607                     this.globe.add(ring);
+ 2608                     this.rings.push(ring);
+ 2609                 });
+ 2610             },
+ 2611 
+ 2612             setupInteraction(container) {
+ 2613                 let isDragging = false, prev = { x: 0, y: 0 }, autoRotate = true;
+ 2614                 const start = (x, y) => { isDragging = true; autoRotate = false; prev = { x, y }; };
+ 2615                 const move = (x, y) => { if (!isDragging) return; this.globe.rotation.y += (x - prev.x) * 0.005; this.globe.rotation.x = Math.max(-Math.PI / 2, Math.min(Math.PI / 2, this.globe.rotation.x + (y - prev.y) * 0.005)); prev = { x, y }; };
+ 2616                 const end = () => { isDragging = false; setTimeout(() => autoRotate = true, 3000); };
+ 2617 
+ 2618                 container.addEventListener('mousedown', e => start(e.clientX, e.clientY));
+ 2619                 container.addEventListener('mousemove', e => move(e.clientX, e.clientY));
+ 2620                 container.addEventListener('mouseup', end);
+ 2621                 container.addEventListener('mouseleave', end);
+ 2622                 container.addEventListener('touchstart', e => { e.preventDefault(); start(e.touches[0].clientX, e.touches[0].clientY); }, { passive: false });
+ 2623                 container.addEventListener('touchmove', e => { e.preventDefault(); move(e.touches[0].clientX, e.touches[0].clientY); }, { passive: false });
+ 2624                 container.addEventListener('touchend', end);
+ 2625                 this.autoRotate = () => autoRotate;
+ 2626             },
+ 2627 
+ 2628             onResize() {
+ 2629                 const container = document.getElementById('globe-container');
+ 2630                 if (!container) return;
+ 2631                 this.camera.aspect = container.clientWidth / container.clientHeight;
+ 2632                 this.camera.updateProjectionMatrix();
+ 2633                 this.renderer.setSize(container.clientWidth, container.clientHeight);
+ 2634             },
+ 2635 
+ 2636             renderRegionList() {
+ 2637                 const list = document.getElementById('region-list');
+ 2638                 list.innerHTML = DataFabric.regions.map(region => {
+ 2639                     const data = DataFabric.state.regional[region.id];
+ 2640                     const trend = data.sentiment > 65 ? '↑' : data.sentiment < 50 ? '↓' : '→';
+ 2641                     return `<div class="region-item" data-region="${region.id}" tabindex="0">
+ 2642                         <div class="region-info"><div class="region-dot" style="background: ${region.color};"></div><div class="region-name">${region.name}</div></div>
+ 2643                         <div class="region-stats"><div class="region-sentiment" style="color: ${region.color}">${data.sentiment.toFixed(1)}</div><div class="region-trend">${trend} ${data.latency.toFixed(0)}ms</div></div>
+ 2644                     </div>`;
+ 2645                 }).join('');
+ 2646                 list.querySelectorAll('.region-item').forEach(item => item.addEventListener('click', () => {
+ 2647                     const region = DataFabric.regions.find(r => r.id === item.dataset.region);
+ 2648                     const data = DataFabric.state.regional[item.dataset.region];
+ 2649                     App.showToast(`${region.name}: Sentiment ${data.sentiment.toFixed(1)}%, Latency ${data.latency.toFixed(0)}ms`);
+ 2650                 }));
+ 2651             },
+ 2652 
+ 2653             render(data) {
+ 2654                 if (!this.isInitialized) return;
+ 2655                 if (this.autoRotate()) this.globe.rotation.y += 0.002;
+ 2656                 const time = Date.now() * 0.001;
+ 2657                 this.rings.forEach((ring, i) => { ring.scale.setScalar(1 + Math.sin(time * 2 + i) * 0.3); ring.material.opacity = 0.4 + Math.sin(time * 2 + i) * 0.2; });
+ 2658                 this.markers.forEach(marker => {
+ 2659                     if (marker.userData.region) {
+ 2660                         const rd = data.regional[marker.userData.region];
+ 2661                         if (rd) marker.scale.setScalar((0.015 + Math.min(this.currentLayer === 'latency' ? 1 - rd.latency / 100 : this.currentLayer === 'traffic' ? rd.traffic / 4000 : rd.sentiment / 100, 1) * 0.025) * 40);
+ 2662                     }
+ 2663                 });
+ 2664                 if (Math.random() < 0.05) this.renderRegionList();
+ 2665                 this.renderer.render(this.scene, this.camera);
+ 2666             }
+ 2667         };
+ 2668 
+ 2669         // ============================================
+ 2670         // AI ENGINE
+ 2671         // ============================================
+ 2672         const AIEngine = {
+ 2673             isOpen: false,
+ 2674 
+ 2675             init() {
+ 2676                 document.getElementById('ai-insights-btn').addEventListener('click', () => this.toggle());
+ 2677                 document.getElementById('ai-panel-close').addEventListener('click', () => this.close());
+ 2678                 document.addEventListener('keydown', e => { if (e.key === 'Escape' && this.isOpen) this.close(); });
+ 2679             },
+ 2680 
+ 2681             toggle() { this.isOpen ? this.close() : this.open();
