<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Gamer Logbuch Pro</title>
    <style>
        :root {
            --bg: #0f1012;
            --card-bg: rgba(45, 47, 54, 0.6);
            --accent: #7289da;
            --text: #ffffff;
            --text-dim: #a0a0a0;
            --glass: rgba(255, 255, 255, 0.03);
        }

        body {
            background: radial-gradient(circle at top, #1a1c24 0%, #0f1012 100%);
            color: var(--text);
            font-family: 'Segoe UI', Roboto, sans-serif;
            margin: 0;
            display: flex;
            justify-content: center;
            min-height: 100vh;
        }

        .app-container {
            width: 100%;
            max-width: 480px;
            padding: 20px;
            box-sizing: border-box;
            padding-bottom: 100px;
        }

        /* Header & Icon */
        header {
            text-align: center;
            margin-bottom: 30px;
            animation: fadeIn 1s ease;
        }

        .logo-container {
            width: 140px;
            height: 60px;
            margin: 0 auto 10px;
            display: flex;
            justify-content: space-between;
        }

        .logo-half {
            width: 60px;
            height: 100%;
            border: 3px solid;
            border-radius: 15px 15px 25px 25px;
            box-shadow: 0 0 15px rgba(255,255,255,0.1);
        }

        .l-half { border-color: #00fbff; filter: drop-shadow(0 0 8px #00fbff); }
        .r-half { border-color: #b042ff; filter: drop-shadow(0 0 8px #b042ff); }

        /* Karten & Design */
        .card {
            background: var(--card-bg);
            backdrop-filter: blur(10px);
            border: 1px solid var(--glass);
            border-radius: 16px;
            padding: 16px;
            margin-bottom: 15px;
            transition: transform 0.2s, box-shadow 0.2s;
            animation: slideIn 0.4s ease-out;
        }

        .card:active { transform: scale(0.98); }

        .hero-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 10px;
        }

        .ilvl-badge {
            background: rgba(0,0,0,0.3);
            padding: 4px 8px;
            border-radius: 6px;
            font-size: 12px;
            color: #ffd700;
            border: 1px solid rgba(255,215,0,0.3);
        }

        /* Weekly Progress */
        .progress-container {
            margin: 20px 0;
            background: rgba(0,0,0,0.2);
            border-radius: 10px;
            height: 8px;
            overflow: hidden;
        }

        .progress-bar {
            height: 100%;
            background: linear-gradient(90deg, #7289da, #00fbff);
            width: 0%;
            transition: width 0.5s ease;
        }

        /* Inputs */
        .input-group {
            background: rgba(0,0,0,0.2);
            padding: 15px;
            border-radius: 12px;
            margin-bottom: 25px;
        }

        input, select {
            width: 100%;
            background: #1a1c24;
            border: 1px solid #333;
            color: white;
            padding: 12px;
            border-radius: 8px;
            margin-bottom: 10px;
            box-sizing: border-box;
        }

        .btn {
            width: 100%;
            background: var(--accent);
            border: none;
            color: white;
            padding: 14px;
            border-radius: 8px;
            font-weight: bold;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(114, 137, 218, 0.3);
        }

        /* Animations */
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
        @keyframes slideIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

        .delete-btn { color: #ff4d4d; font-size: 12px; cursor: pointer; float: right; }
        
        .tab-btn { flex: 1; text-align: center; padding: 15px; cursor: pointer; color: var(--text-dim); }
        .tab-btn.active { color: white; border-bottom: 3px solid var(--accent); }

        .nav { position: fixed; bottom: 0; left: 0; right: 0; background: #16171d; display: flex; border-top: 1px solid #333; }
        .hidden { display: none; }
    </style>
</head>
<body>

<div class="app-container">
    <header>
        <div class="logo-container">
            <div class="logo-half l-half"></div>
            <div class="logo-half r-half"></div>
        </div>
        <h1 style="font-size: 1.5rem; margin: 0; letter-spacing: 2px;">HERO LOG</h1>
    </header>

    <div id="view-heroes">
        <div class="input-group">
            <input type="text" id="h-name" placeholder="Name des Helden">
            <input type="number" id="h-ilvl" placeholder="iLvl (z.B. 615)">
            <select id="h-class">
                <option value="#f48cba">Paladin</option>
                <option value="#c69b6d">Krieger</option>
                <option value="#3fc7eb">Magier</option>
                <option value="#ff7c0a">Druide</option>
                <option value="#a330c9">Dämonenjäger</option>
                <option value="#c41e3a">Todesritter</option>
            </select>
            <button class="btn" onclick="saveHero()">Held hinzufügen</button>
        </div>
        <div id="hero-list"></div>
    </div>

    <div id="view-goals" class="hidden">
        <h3>Weekly Progress</h3>
        <div class="progress-container"><div id="p-bar" class="progress-bar"></div></div>
        <div id="todo-list">
            </div>
    </div>

    <div class="nav">
        <div class="tab-btn active" onclick="show('view-heroes', this)">HELDEN</div>
        <div class="tab-btn" onclick="show('view-goals', this)">ZIELE</div>
    </div>
</div>

<script>
    let heroes = JSON.parse(localStorage.getItem('h_data')) || [];
    let todos = JSON.parse(localStorage.getItem('t_data')) || [
        {txt: "Weltboss besiegt", done: false},
        {txt: "M+ Key gelaufen", done: false},
        {txt: "Raid Clear", done: false},
        {txt: "Weekly Quest", done: false}
    ];

    function show(id, el) {
        document.getElementById('view-heroes').classList.add('hidden');
        document.getElementById('view-goals').classList.add('hidden');
        document.getElementById(id).classList.remove('hidden');
        document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
        el.classList.add('active');
        if(id === 'view-goals') renderTodos();
    }

    function saveHero() {
        const name = document.getElementById('h-name').value;
        const ilvl = document.getElementById('h-ilvl').value || '???';
        const color = document.getElementById('h-class').value;
        if(!name) return;
        heroes.push({name, ilvl, color});
        localStorage.setItem('h_data', JSON.stringify(heroes));
        document.getElementById('h-name').value = '';
        renderHeroes();
    }

    function renderHeroes() {
        const container = document.getElementById('hero-list');
        container.innerHTML = '';
        heroes.forEach((h, i) => {
            const card = document.createElement('div');
            card.className = 'card';
            card.style.borderLeft = `4px solid ${h.color}`;
            card.style.boxShadow = `0 4px 20px ${h.color}22`;
            card.innerHTML = `
                <div class="hero-header">
                    <strong>${h.name}</strong>
                    <span class="ilvl-badge">${h.ilvl} iLvl</span>
                </div>
                <span class="delete-btn" onclick="delHero(${i})">Löschen</span>
            `;
            container.appendChild(card);
        });
    }

    function delHero(i) {
        heroes.splice(i, 1);
        localStorage.setItem('h_data', JSON.stringify(heroes));
        renderHeroes();
    }

    function renderTodos() {
        const container = document.getElementById('todo-list');
        container.innerHTML = '';
        let doneCount = 0;
        todos.forEach((t, i) => {
            if(t.done) doneCount++;
            const item = document.createElement('div');
            item.className = 'card';
            item.style.display = 'flex';
            item.style.justifyContent = 'space-between';
            item.innerHTML = `<span>${t.txt}</span><input type="checkbox" ${t.done?'checked':''} onchange="toggleTodo(${i})">`;
            container.appendChild(item);
        });
        document.getElementById('p-bar').style.width = (doneCount / todos.length * 100) + '%';
    }

    function toggleTodo(i) {
        todos[i].done = !todos[i].done;
        localStorage.setItem('t_data', JSON.stringify(todos));
        renderTodos();
    }

    renderHeroes();
</script>
</body>
</html>
