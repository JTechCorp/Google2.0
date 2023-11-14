<!DOCTYPE html>
<html>
<head>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            background-color: #121212; 
            font-family: Arial, sans-serif;
        }

        h1.google-name {
            font-size: 75px;
            margin-bottom: 20px;
            color: white;
        }

        .search-container {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
        }

        input.search-input {
            padding: 10px;
            font-size: 16px;
            border: 1px solid #d5d5d5;
            border-radius: 24px;
            width: 300px;
            margin-right: 10px;
            outline: none;
        }

        button.search-button {
            padding: 10px 20px;
            font-size: 16px;
            border: 1px solid #d5d5d5;
            border-radius: 24px;
            background-color: #ffffff;
            cursor: pointer;
            outline: none;
        }

    </style>
    <title>Google 2.0</title>
</head>
<body>
    <h1 class="google-name">Google 2.0</h1>
    <div class="search-container">
        <input class="search-input" type="text" id="input" placeholder="Search Google">
        <button class="search-button" onclick="searchGoogle()">Google Search</button>
    </div>
    <span id="result"></span>

    <script>
        function searchGoogle() {
            var inputValue = document.getElementById('input').value;
            var resultElement = document.getElementById('result');
            var resultLink = document.createElement('a');
    
            resultLink.setAttribute('class', 'result-link');
            resultLink.setAttribute('href', 'https://www.google.com/search?q=' + inputValue);
            
            // Open the link in the same tab
            window.location.href = resultLink.getAttribute('href');
    
            // Clear previous results
            while (resultElement.firstChild) {
                resultElement.removeChild(resultElement.firstChild);
            }
    
            // Append the new link
            resultElement.appendChild(resultLink);
    
            // Clear the input
            document.getElementById('input').value = '';
        }
    </script>
    
</body>
</html>


