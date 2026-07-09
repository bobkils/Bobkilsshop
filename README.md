<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Bobkils Shop</title>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <style>
        body { background-color: #181818; color: #ffffff; font-family: Arial, sans-serif; text-align: center; padding-top: 20px; }
        .btn { background-color: #2c2c2c; padding: 20px; margin: 15px auto; border-radius: 12px; font-size: 18px; font-weight: bold; width: 80%; border: 1px solid #444; }
    </style>
</head>
<body>
    <h2>🛒 Bobkils Shop</h2>
    <p>Выбери страну:</p>
    <div class="btn" onclick="buy('USA')">🇺🇸 США</div>
    <div class="btn" onclick="buy('Kazakhstan')">🇰🇿 Казахстан</div>
    <script>
        let tg = window.Telegram.WebApp;
        tg.expand();
        function buy(country) {
            tg.sendData(country);
            tg.close();
        }
    </script>
</body>
</html>
