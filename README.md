<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Form</title>
</head>
<body>
    <form id="loginForm">
        <label for="username">Пользователь:</label>
        <input type="text" id="username" name="username" required><br><br>
        <label for="password">Password:</label>
        <input type="password" id="password" name="password" required><br><br>
        <button type="button" onclick="submitForm()">Submit</button>
    </form>

    <script>
        Telegram.WebApp.ready();

        function submitForm() {
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;

            if (username && password) {
                // Отправка данных в WebApp
                Telegram.WebApp.sendData(JSON.stringify({ username, password }));
                alert('Data sent successfully!');
            } else {
                alert('Please fill all fields!');
            }
        }
    </script>
</body>
</html>
