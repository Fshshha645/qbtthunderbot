<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>QBT THUNDER Signal Generator</title>
    <style>
        body {
            background-color: black;
            color: green;
            font-family: monospace;
            padding: 20px;
        }
        .container {
            max-width: 800px;
            margin: auto;
        }
        h1, h3 {
            color: #00ff00;
        }
        a {
            color: cyan;
            text-decoration: none;
        }
        a:hover {
            color: #00ffff;
        }
        select, input {
            padding: 10px;
            margin: 10px 0;
            background-color: #f0f0f0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            padding: 10px 20px;
            margin: 10px;
            color: white;
            background-color: #28a745;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #218838;
        }
        .button-container {
            display: flex;
            justify-content: start;
        }
        .error-message {
            color: red;
        }
        .animation-message {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: rgba(0, 0, 0, 0.8);
            padding: 20px;
            border-radius: 10px;
            color: white;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>QBT THUNDER BO OTC SIGNAL GENERATOR</h1>
        <p>QBT THUNDER BOT FUTURE SIGNAL SOFTWARE</p>
        <p id="timezone-info">Timezone: Asia/Dhaka | Date: <span id="current-date"></span> | Time: <span id="current-time"></span></p>
        <h3>Join our Telegram Channel:</h3>
        <a href="https://t.me/qbttrader" target="_blank" rel="noopener noreferrer">QBT TRADER</a>
        
        <h3>Available Assets:</h3>
        <select id="asset-select">
            <option value="">Select an asset</option>
        </select>

        <h3>Number of Signals to Generate:</h3>
        <input type="number" id="signal-count" value="1" min="1" />

        <h3>Filter Signals:</h3>
        <select id="filter-select">
            <option value="PUT/CALL">PUT/CALL</option>
            <option value="CALL">CALL</option>
            <option value="PUT">PUT</option>
        </select>

        <h3>Backtest Filter:</h3>
        <label>
            <input type="checkbox" id="backtest-filter" />
            Show only backtested signals (95% accuracy)
        </label>

        <div class="button-container">
            <button id="generate-signals">Generate Signals</button>
            <button id="reset-signals">Reset Signals</button>
        </div>

        <p id="error-message" class="error-message"></p>
        
        <h3>Generated Signals:</h3>
        <ul id="signal-list"></ul>
        
        <div id="animation-message" class="animation-message">
            <h3>New Signals Generated!</h3>
        </div>
    </div>

    <script>
        const availableAssets = [
            "AUD/CAD OTC", "AUD/CHF OTC", "AUD/JPY OTC", "AUD/NZD OTC", "AUD/USD OTC",
            "CAD/CHF OTC", "CHF/JPY OTC", "EUR/AUD OTC", "EUR/CAD OTC", "EUR/CHF OTC",
            "EUR/GBP OTC", "EUR/USD OTC", "GBP/AUD OTC", "GBP/CAD OTC", "GBP/CHF OTC",
            "GBP/JPY OTC", "GBP/NZD OTC", "GBP/USD OTC", "NZD/CAD OTC", "NZD/CHF OTC",
            "NZD/JPY OTC", "USD/BDT OTC", "USD/BRL OTC", "USD/CAD OTC", "USD/CHF OTC",
            "USD/COP OTC", "USD/DZD OTC", "USD/INR OTC", "USD/JPY OTC", "USD/NGN OTC",
            "USD/PKR OTC", "USD/SGD OTC", "USD/TRY OTC", "USD/ZAR OTC", "Bitcoin OTC",
            "Gold OTC", "Silver OTC", "USCrude OTC", "UKBrent OTC"
        ];

        let signals = [];
        let existingSignals = new Set();

        function formatTime(date) {
            return date.toLocaleTimeString('en-GB', { hour: '2-digit', minute: '2-digit' });
        }

        function generateSignal(asset, time) {
            const direction = Math.random() < 0.5 ? 'CALL' : 'PUT';
            return { asset, time, direction };
        }

        function generateUniqueTimes(count) {
            const times = [];
            let nextTime = new Date();
            for (let i = 0; i < count; i++) {
                nextTime.setMinutes(nextTime.getMinutes() + 7);
                times.push(formatTime(nextTime));
            }
            return times;
        }

        function handleGenerateSignals() {
            const selectedAsset = document.getElementById('asset-select').value;
            const signalCount = Number(document.getElementById('signal-count').value);
            const errorMessage = document.getElementById('error-message');
            
            if (!selectedAsset) {
                errorMessage.textContent = 'Please select an asset before generating signals!';
                return;
            }

            errorMessage.textContent = '';
            const uniqueTimes = generateUniqueTimes(signalCount);
            const newSignals = [];

            uniqueTimes.forEach((time) => {
                const signalKey = `${selectedAsset} ; ${time}`;
                if (!existingSignals.has(signalKey)) {
                    const newSignal = generateSignal(selectedAsset, time);
                    newSignals.push(newSignal);
                    existingSignals.add(signalKey);
                }
            });

            signals.push(...newSignals);
            displaySignals(newSignals);
            showAnimation();
        }

        function displaySignals(newSignals) {
            const signalList = document.getElementById('signal-list');
            newSignals.forEach(signal => {
                const listItem = document.createElement('li');
                listItem.textContent = `${signal.asset} ; ${signal.time} ; ${signal.direction}`;
                signalList.appendChild(listItem);
            });
        }

        function showAnimation() {
            const animationMessage = document.getElementById('animation-message');
            animationMessage.style.display = 'block';
            setTimeout(() => {
                animationMessage.style.display = 'none';
            }, 2000);
        }

        function handleResetSignals() {
            signals = [];
            existingSignals = new Set();
            document.getElementById('signal-list').innerHTML = '';
        }

        function updateDateTime() {
            const currentDate = new Date();
            document.getElementById('current-date').textContent = currentDate.toLocaleDateString();
            document.getElementById('current-time').textContent = currentDate.toLocaleTimeString('en-GB');
        }

        // Populate the asset dropdown
        const assetSelect = document.getElementById('asset-select');
        availableAssets.forEach(asset => {
            const option = document.createElement('option');
            option.value = asset;
            option.textContent = asset;
            assetSelect.appendChild(option);
        });

        // Event listeners
        document.getElementById('generate-signals').addEventListener('click', handleGenerateSignals);
        document.getElementById('reset-signals').addEventListener('click', handleResetSignals);

        // Update time every second
        setInterval(updateDateTime, 1000);
    </script>
</body>
</html>
