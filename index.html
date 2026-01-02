<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>年度存錢計畫</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@400;500;700;900&display=swap');

        :root {
            --bg-page: #f4f1ee;
            --header-brown: #8d6e63;
            --text-dark: #5d4037;
            --accent-brown: #a1887f;
            --white: #ffffff;
        }

        body {
            background-color: var(--bg-page);
            font-family: 'Noto Sans TC', sans-serif;
            letter-spacing: 0.02em;
            display: flex;
            justify-content: center;
            color: var(--text-dark);
            margin: 0;
            padding: 0;
            /* 確保 body 可以滾動 */
            overflow-y: auto;
            min-height: 100vh;
        }

        .app-container {
            width: 100%;
            max-width: 420px; 
            /* 移除固定高度限制，讓內容自然撐開 */
            background: var(--white);
            box-shadow: 0 10px 30px rgba(93, 64, 55, 0.1);
            display: flex;
            flex-direction: column;
        }

        .header-banner {
            background-color: var(--header-brown);
            padding: 2.5rem 1.5rem;
            text-align: center;
            color: var(--white);
        }

        .header-banner h1 {
            font-size: 2rem; 
            font-weight: 900;
            margin-bottom: 0rem;
        }

        .content-body {
            padding: 1.25rem;
            flex-grow: 1;
        }

        .stats-panel {
            background-color: #faf9f8;
            border-radius: 16px;
            padding: 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.25rem;
            border: 1px solid #efebe9;
        }

        .stat-group {
            flex: 1;
            text-align: center;
        }

        .stat-label {
            font-size: 0.65rem;
            font-weight: 700;
            color: var(--accent-brown);
            margin-bottom: 2px;
        }

        .stat-value {
            font-size: 1.1rem;
            font-weight: 900;
            color: var(--header-brown);
        }

        .calendar-grid {
            display: grid;
            grid-template-columns: repeat(7, 1fr);
            gap: 6px;
            background: var(--white);
        }

        .day-cell {
            aspect-ratio: 1 / 1.6; 
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: flex-start;
            padding-top: 6px;
            border-radius: 8px;
            border: 1px solid #f5f2f0;
            cursor: pointer;
            background: #ffffff;
            transition: all 0.2s;
        }

        .day-cell.has-value {
            background-color: var(--header-brown);
            color: var(--white);
            border-color: var(--header-brown);
        }

        .day-num {
            font-size: 0.85rem; 
            font-weight: 700;
            color: var(--accent-brown);
            margin-bottom: 4px;
        }

        .day-cell.has-value .day-num {
            color: rgba(255,255,255,0.6);
        }

        .day-amount {
            font-size: 0.8rem;
            font-weight: 700;
            writing-mode: vertical-lr; 
            letter-spacing: 1px;
        }

        .progress-bar-bg {
            height: 8px;
            background: #efebe9;
            border-radius: 4px;
            overflow: hidden;
            margin-top: 4px;
        }

        .progress-bar-fill {
            height: 100%;
            background: var(--header-brown);
            transition: width 0.8s ease-out;
        }

        .backup-section {
            padding: 1.5rem 1.25rem 3rem;
            background: #fafafa;
            border-top: 1px solid #eee;
            /* 增加底部邊距，確保在手機瀏覽器上不會被導覽列遮住 */
            margin-top: auto;
        }

        .backup-btn {
            width: 100%;
            padding: 0.8rem; /* 略微加大按鈕方便點擊 */
            border-radius: 12px;
            font-size: 0.85rem;
            font-weight: 700;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 6px;
            margin-bottom: 0.75rem;
        }

        #toast {
            position: fixed;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            background: rgba(93, 64, 55, 0.95);
            color: white;
            padding: 10px 20px;
            border-radius: 12px;
            font-size: 0.85rem;
            font-weight: bold;
            z-index: 1000;
            display: none;
        }
    </style>
</head>
<body>
    <div id="toast">已複製</div>

    <div class="app-container">
        <header class="header-banner">
            <div class="flex items-center justify-center gap-6">
                <button id="prev-year" class="opacity-40 hover:opacity-100 p-2">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"><path d="m15 18-6-6 6-6"/></svg>
                </button>
                <h1 id="year-display">2026</h1>
                <button id="next-year" class="opacity-40 hover:opacity-100 p-2">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"><path d="m9 18 6-6-6-6"/></svg>
                </button>
            </div>
        </header>

        <div class="content-body">
            <div class="stats-panel">
                <div class="stat-group">
                    <span class="stat-label">年度累積</span>
                    <p id="total-annual" class="stat-value">$ 0</p>
                </div>
                <div class="w-[1px] h-6 bg-stone-200 mx-2"></div>
                <div class="stat-group">
                    <span id="month-label" class="stat-label">1月統計</span>
                    <p id="total-monthly" class="stat-value">$ 0</p>
                </div>
            </div>

            <div class="mb-6">
                <div class="flex justify-between items-end mb-1 px-1">
                    <div>
                        <span class="stat-label text-[9px] opacity-70">存錢進度</span>
                        <p id="goal-display" class="text-[10px] font-bold text-stone-400">$ 100,000</p>
                    </div>
                    <span id="progress-percent" class="text-xs font-black text-stone-600">0%</span>
                </div>
                <div class="progress-bar-bg">
                    <div id="progress-bar" class="progress-bar-fill w-0"></div>
                </div>
                <button id="set-goal-btn" class="mt-3 text-[13px] font-bold text-stone-500 underline tracking-wide">自訂目標金額</button>
            </div>

            <div class="flex items-center justify-between mb-6 px-2">
                <button id="prev-month" class="text-stone-300 p-2 hover:bg-stone-50 rounded-full">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"><path d="m15 18-6-6 6-6"/></svg>
                </button>
                <h2 id="current-month-display" class="text-xl font-black text-stone-700">1月</h2>
                <button id="next-month" class="text-stone-300 p-2 hover:bg-stone-50 rounded-full">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"><path d="m9 18 6-6-6-6"/></svg>
                </button>
            </div>

            <div class="calendar-container">
                <div class="grid grid-cols-7 mb-3">
                    <div class="text-center text-[10px] font-black text-red-400">日</div>
                    <div class="text-center text-[10px] font-bold text-stone-300">一</div>
                    <div class="text-center text-[10px] font-bold text-stone-300">二</div>
                    <div class="text-center text-[10px] font-bold text-stone-300">三</div>
                    <div class="text-center text-[10px] font-bold text-stone-300">四</div>
                    <div class="text-center text-[10px] font-bold text-stone-300">五</div>
                    <div class="text-center text-[10px] font-black text-blue-400">六</div>
                </div>
                <div id="calendar-body" class="calendar-grid"></div>
            </div>
        </div>

        <div class="backup-section">
            <button id="export-btn" class="backup-btn bg-stone-100 text-stone-500 hover:bg-stone-200">
                複製備份代碼
            </button>
            <button id="import-btn" class="backup-btn bg-white border border-stone-100 text-stone-300 hover:text-stone-500">
                導入備份紀錄
            </button>
        </div>
    </div>

    <!-- Modals -->
    <div id="input-modal" class="fixed inset-0 bg-stone-900/40 backdrop-blur-sm hidden flex items-center justify-center p-6 z-50">
        <div class="bg-white rounded-[2rem] p-8 w-full max-w-[300px] text-center">
            <h3 id="modal-date-title" class="text-base font-bold mb-4">1月 1日</h3>
            <input type="number" id="savings-amount" placeholder="0" class="w-full bg-stone-50 border-none rounded-2xl px-4 py-4 mb-6 text-2xl font-black text-center outline-none">
            <div class="flex gap-2">
                <button id="cancel-btn" class="flex-1 py-3 text-stone-300 font-bold">取消</button>
                <button id="save-btn" class="flex-1 py-3 bg-[#8d6e63] text-white rounded-xl font-bold">儲存</button>
            </div>
        </div>
    </div>

    <div id="goal-modal" class="fixed inset-0 bg-stone-900/40 backdrop-blur-sm hidden flex items-center justify-center p-6 z-50">
        <div class="bg-white rounded-[2rem] p-8 w-full max-w-[300px] text-center">
            <h3 class="text-base font-bold mb-4">設定年度目標</h3>
            <input type="number" id="goal-amount-input" class="w-full bg-stone-50 border-none rounded-xl px-4 py-4 mb-6 text-center text-xl font-bold outline-none">
            <div class="flex gap-2">
                <button id="goal-cancel-btn" class="flex-1 py-3 text-stone-300 font-bold">取消</button>
                <button id="goal-save-btn" class="flex-1 py-3 bg-[#5d4037] text-white rounded-xl font-bold">設定</button>
            </div>
        </div>
    </div>

    <div id="import-modal" class="fixed inset-0 bg-stone-900/40 backdrop-blur-sm hidden flex items-center justify-center p-6 z-50">
        <div class="bg-white rounded-[2rem] p-8 w-full max-w-[300px] text-center">
            <h3 class="text-base font-bold mb-2">導入數據</h3>
            <textarea id="import-text" placeholder="貼上代碼..." class="w-full bg-stone-50 border-none rounded-xl px-4 py-3 mb-4 h-24 text-[10px] outline-none"></textarea>
            <div class="flex gap-2">
                <button id="import-cancel-btn" class="flex-1 py-3 text-stone-300 font-bold">取消</button>
                <button id="import-confirm-btn" class="flex-1 py-3 bg-[#5d4037] text-white rounded-xl font-bold">導入</button>
            </div>
        </div>
    </div>

    <script>
        let state = {
            year: new Date().getFullYear(),
            month: new Date().getMonth(),
            savings: JSON.parse(localStorage.getItem('sl_savings_v2')) || {},
            goal: parseInt(localStorage.getItem('sl_goal_v2')) || 100000
        };

        const monthNames = ["1月", "2月", "3月", "4月", "5月", "6月", "7月", "8月", "9月", "10月", "11月", "12月"];
        let selectedKey = '';

        const elements = {
            calendar: document.getElementById('calendar-body'),
            year: document.getElementById('year-display'),
            month: document.getElementById('current-month-display'),
            monthLabel: document.getElementById('month-label'),
            totalAnnual: document.getElementById('total-annual'),
            totalMonthly: document.getElementById('total-monthly'),
            goal: document.getElementById('goal-display'),
            progress: document.getElementById('progress-bar'),
            percent: document.getElementById('progress-percent'),
            inputModal: document.getElementById('input-modal'),
            goalModal: document.getElementById('goal-modal'),
            importModal: document.getElementById('import-modal'),
            toast: document.getElementById('toast')
        };

        function init() {
            render();
            document.getElementById('prev-year').onclick = () => { state.year--; render(); };
            document.getElementById('next-year').onclick = () => { state.year++; render(); };
            document.getElementById('prev-month').onclick = () => moveMonth(-1);
            document.getElementById('next-month').onclick = () => moveMonth(1);
            document.getElementById('set-goal-btn').onclick = () => { 
                elements.goalModal.classList.remove('hidden'); 
                document.getElementById('goal-amount-input').value = state.goal;
            };
            document.getElementById('goal-cancel-btn').onclick = () => elements.goalModal.classList.add('hidden');
            document.getElementById('goal-save-btn').onclick = saveGoal;
            document.getElementById('cancel-btn').onclick = () => elements.inputModal.classList.add('hidden');
            document.getElementById('save-btn').onclick = saveSavings;
            document.getElementById('export-btn').onclick = exportData;
            document.getElementById('import-btn').onclick = () => elements.importModal.classList.remove('hidden');
            document.getElementById('import-cancel-btn').onclick = () => elements.importModal.classList.add('hidden');
            document.getElementById('import-confirm-btn').onclick = importData;
        }

        function showToast(text) {
            elements.toast.innerText = text;
            elements.toast.style.display = 'block';
            setTimeout(() => { elements.toast.style.display = 'none'; }, 2000);
        }

        function moveMonth(dir) {
            state.month += dir;
            if (state.month < 0) { state.month = 11; state.year--; }
            else if (state.month > 11) { state.month = 0; state.year++; }
            render();
        }

        function render() {
            elements.year.innerText = state.year;
            elements.month.innerText = monthNames[state.month];
            elements.monthLabel.innerText = `${monthNames[state.month]}統計`;
            elements.calendar.innerHTML = '';
            
            const first = new Date(state.year, state.month, 1).getDay();
            const days = new Date(state.year, state.month + 1, 0).getDate();

            for(let i=0; i<first; i++) {
                const empty = document.createElement('div');
                empty.className = 'day-cell opacity-0 pointer-events-none';
                elements.calendar.appendChild(empty);
            }

            for(let d=1; d<=days; d++) {
                const key = `${state.year}-${String(state.month+1).padStart(2,'0')}-${String(d).padStart(2,'0')}`;
                const val = state.savings[key] || 0;
                const cell = document.createElement('div');
                cell.className = `day-cell ${val > 0 ? 'has-value' : ''}`;
                cell.innerHTML = `
                    <span class="day-num">${d}</span>
                    <span class="day-amount">${val > 0 ? val : ''}</span>
                `;
                cell.onclick = () => {
                    selectedKey = key;
                    document.getElementById('modal-date-title').innerText = `${state.month+1}月 ${d}日`;
                    document.getElementById('savings-amount').value = state.savings[key] || '';
                    elements.inputModal.classList.remove('hidden');
                    setTimeout(() => document.getElementById('savings-amount').focus(), 150);
                };
                elements.calendar.appendChild(cell);
            }

            let annual = 0, monthly = 0;
            Object.entries(state.savings).forEach(([k, v]) => {
                if(k.startsWith(state.year)) annual += v;
                if(k.startsWith(`${state.year}-${String(state.month+1).padStart(2,'0')}`)) monthly += v;
            });

            elements.totalAnnual.innerText = `$${annual.toLocaleString()}`;
            elements.totalMonthly.innerText = `$${monthly.toLocaleString()}`;
            elements.goal.innerText = `年度目標 $${state.goal.toLocaleString()}`;
            
            const p = state.goal > 0 ? Math.min(Math.round((annual/state.goal)*100), 100) : 0;
            elements.progress.style.width = p + '%';
            elements.percent.innerText = p + '%';

            localStorage.setItem('sl_savings_v2', JSON.stringify(state.savings));
        }

        function saveSavings() {
            const v = parseFloat(document.getElementById('savings-amount').value);
            if (!isNaN(v) && v > 0) { state.savings[selectedKey] = v; } 
            else { delete state.savings[selectedKey]; }
            elements.inputModal.classList.add('hidden');
            render();
        }

        function saveGoal() {
            const v = parseInt(document.getElementById('goal-amount-input').value);
            if(!isNaN(v) && v > 0) { state.goal = v; localStorage.setItem('sl_goal_v2', v); }
            elements.goalModal.classList.add('hidden');
            render();
        }

        function exportData() {
            const data = { s: state.savings, g: state.goal };
            const str = btoa(encodeURIComponent(JSON.stringify(data)));
            const el = document.createElement('textarea');
            el.value = str;
            document.body.appendChild(el);
            el.select();
            document.execCommand('copy');
            document.body.removeChild(el);
            showToast("備份代碼已複製");
        }

        function importData() {
            const str = document.getElementById('import-text').value.trim();
            try {
                const data = JSON.parse(decodeURIComponent(atob(str)));
                state.savings = data.s || {};
                state.goal = data.g || 100000;
                localStorage.setItem('sl_savings_v2', JSON.stringify(state.savings));
                localStorage.setItem('sl_goal_v2', state.goal);
                elements.importModal.classList.add('hidden');
                render();
                showToast("導入成功");
            } catch(e) { showToast("代碼錯誤"); }
        }

        window.onload = init;
    </script>
</body>
</html>
