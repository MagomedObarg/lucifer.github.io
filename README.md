<!DOCTYPE html>
<html>
<head>
    <title>Telegram Web App</title>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
</head>
<body>
    <h1>Привет из Web App!</h1>
    <button onclick="sendData()">Отправить данные боту</button>

    <script>
        let tg = window.Telegram.WebApp;
        tg.ready();

        function sendData() {
            let data = {
                "name": "John Doe",
                "email": "john@example.com"
            };
            tg.sendData(JSON.stringify(data));
        }
    </script>
</body>
</html>
