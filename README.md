

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Открытие сайта на текущей странице</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        label {
            display: block;
            margin-bottom: 10px;
        }
        input {
            width: 70%;
            padding: 8px;
            margin-bottom: 10px;
        }
        button {
            padding: 10px;
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
        }
        iframe {
            width: 100%;
            height: 500px;
            border: 1px solid #ccc;
        }
        .error {
            color: red;
            margin-top: 10px;
        }<
    </style>
</head>
<body>

    <label for="websiteInput">Введите ссылку на сайт:</label>
    <input type="text" id="websiteInput">
    <button onclick="openWebsite()">Открыть сайт</button>

    <div id="error" class="error"></div>
    
    <iframe id="websiteFrame" frameborder="0"></iframe>

    <script>
        function openWebsite() {
            var websiteUrl = document.getElementById('websiteInput').value;
            var errorDiv = document.getElementById('error');

            if (websiteUrl.trim() !== '') {
                // Очищаем сообщение об ошибке
                errorDiv.textContent = '';

                // Устанавливаем URL в iframe
                document.getElementById('websiteFrame').src = websiteUrl;
            } else {
                errorDiv.textContent = 'Пожалуйста, введите ссылку на сайт.';
            }
        }
    </script>

    <p>&copy; 2024 Разработчик  Dylan9332789Z Все права защищены. | <span id="companyLink"></span></p>
    
