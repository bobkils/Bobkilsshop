# Bobkilsshop
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Bobkils Shop</title>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <style>
        /* Жестко задаем темный фон и цвета */
        body {
            background-color: #181818; 
            color: #ffffff;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            text-align: center;
        }
        h2 { margin-bottom: 5px; }
        p { color: #aaaaaa; margin-bottom: 25px; }
        .btn {
            background-color: #2c2c2c;
            padding: 18px;
            margin: 12px auto;
            border-radius: 12px;
            font-size: 18px;
            font-weight: bold;
            width: 85%;
            cursor: pointer;
            box-shadow: 0 4px 6px rgba(0,0,0,0.4);
            border: 1px solid #444;
        }
        .btn:active { background-color: #555555; transform: scale(0.98); }
    </style>
</head>
<body>
    <h2>🛒 Bobkils Shop</h2>
    <p>Выбери страну для покупки:</p>

    <!-- Передаем названия стран точно так же, как они пишутся на ЛОЛЗе -->
    <div class="btn" onclick="buyItem('USA')">🇺🇸 США</div>
    <div class="btn" onclick="buyItem('Kazakhstan')">🇰🇿 Казахстан</div>
    <div class="btn" onclick="buyItem('Russia')">🇷🇺 Россия</div>
    <div class="btn" onclick="buyItem('Indonesia')">🇮🇩 Индонезия</div>

    <script>
        let tg = window.Telegram.WebApp;
        tg.expand(); // Открываем на весь экран
        tg.ready();  // Говорим Телеграму, что мы загрузились

        function buyItem(country) {
            tg.sendData(country); // Отправляем страну в бота
            tg.close(); // Сразу красиво закрываем сайт
        }
    </script>
</body>
</html>
