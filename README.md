# Data-and-Analytics-Hub
This is my repositories hub
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Data & Analytics Lab</title>
    <style>
        body {
            margin: 0;
            display: flex;
            height: 100vh;
            font-family: Arial, sans-serif;
        }
        #left-frame {
            width: 20%;
            background-color: #f4f4f4;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 10px;
            box-shadow: 2px 0 5px rgba(0, 0, 0, 0.1);
        }
        #right-frame {
            width: 80%;
            flex-grow: 1;
            overflow: hidden;
        }
        #logo {
            width: 80%;
            margin-bottom: 20px;
        }
        select {
            width: 100%;
            padding: 10px;
            background-color: #e0e0e0;
            border-radius: 5px;
            font-size: 16px;
            margin-bottom: 20px;
        }
        button {
            padding: 10px 20px;
            margin: 10px 0;
            background-color: #007BFF;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #0056b3;
        }
        iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
    </style>
</head>
<body>
    <div id="left-frame">
        <img id="logo" src="https://raw.githubusercontent.com/atsuvovor/Data-and-Analytics-Hub/refs/heads/main/Logo.webp" alt="Data & Analytics Lab Logo">
        <select id="menu" onchange="changeIframeSource()">
            <option value="https://atsuvovor.github.io/Data-and-Analytics-Hub/">Home</option>
            <option value="https://data-governance.com">Data Governance</option>
            <option value="https://analytics-solutions.com">Analytics Solutions</option>
            <option value="https://custom-designs.com">Custom Designs</option>
        </select>
        <button onclick="refreshRightFrame()">Refresh</button>
    </div>
    <div id="right-frame">
        <iframe name="right-frame" src="https://atsuvovor.github.io/Data-and-Analytics-Hub/"></iframe>
    </div>

    <script>
        // Function to change the source of the iframe based on dropdown selection
        function changeIframeSource() {
            const selectedValue = document.getElementById('menu').value;
            const iframe = document.querySelector('iframe[name="right-frame"]');
            iframe.src = selectedValue;
        }

        // JavaScript function to refresh the right frame
        function refreshRightFrame() {
            const rightFrame = document.querySelector('iframe[name="right-frame"]');
            if (rightFrame.src) {
                rightFrame.contentWindow.location.reload();
            } else {
                alert('No content to refresh!');
            }
        }
    </script>
</body>
</html>
