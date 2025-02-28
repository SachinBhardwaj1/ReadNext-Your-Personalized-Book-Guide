# ReadNext - Your Personalized Book Guide

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ReadNext - Personalized Book Recommender</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f8f9fa;
            color: #333;
            margin: 0;
            padding: 0;
        }
        .container {
            width: 80%;
            margin: auto;
            padding: 20px;
        }
        h1 {
            text-align: center;
            color: #1e3a8a;
            font-size: 2.5em;
        }
        h2 {
            color: #2563eb;
            cursor: pointer;
            padding: 10px;
            border-radius: 5px;
            background-color: #e3eefe;
        }
        h2:hover {
            background-color: #c7dbfc;
        }
        .content {
            display: none;
            padding: 10px;
            border-left: 5px solid #2563eb;
            background-color: white;
            margin-top: 5px;
            border-radius: 5px;
        }
        p {
            font-size: 1.1em;
            line-height: 1.6;
        }
        .highlight {
            background-color: #fffbeb;
            padding: 10px;
            border-left: 5px solid #f59e0b;
        }
        .box {
            background: white;
            padding: 20px;
            margin: 20px 0;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .code {
            background-color: #e5e7eb;
            padding: 10px;
            border-radius: 5px;
            font-family: monospace;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 10px;
            text-align: left;
        }
        th {
            background-color: #1e3a8a;
            color: white;
        }
        .footer {
            text-align: center;
            margin-top: 30px;
            padding: 10px;
            font-size: 1.2em;
            color: #555;
        }
    </style>
    <script>
        function toggleContent(id) {
            var content = document.getElementById(id);
            if (content.style.display === "block") {
                content.style.display = "none";
            } else {
                content.style.display = "block";
            }
        }
    </script>
</head>
<body>

    <div class="container">
        <h1>📚 ReadNext: Your Personalized Book Guide 🚀</h1>

        <div class="box">
            <h2 onclick="toggleContent('whatIsReadNext')">🔍 What is ReadNext?</h2>
            <div id="whatIsReadNext" class="content">
                <p><strong>ReadNext</strong> is an AI-driven recommendation system that helps you discover your next favorite book. By analyzing user ratings and preferences, ReadNext suggests books based on the reading habits of similar users.</p>
                <p class="highlight">💡 Think of it as your **personal book whisperer**, guiding you to your next literary adventure!</p>
            </div>
        </div>

        <div class="box">
            <h2 onclick="toggleContent('howItWorks')">🔢 How the Model Works?</h2>
            <div id="howItWorks" class="content">
                <p>The model follows a structured approach:</p>
                <ul>
                    <li>📂 <strong>Loading the Data:</strong> Uses Ratings.csv and Books.csv.</li>
                    <li>📊 <strong>Building a User-Item Matrix:</strong> Organizes user ratings.</li>
                    <li>🔎 <strong>Finding Similar Users:</strong> Uses **cosine similarity**.</li>
                    <li>🎯 <strong>Scoring Books:</strong> Based on user preferences.</li>
                    <li>📖 <strong>Generating Top 5 Personalized Recommendations:</strong> Mapped with readable titles.</li>
                </ul>
            </div>
        </div>

        <div class="box">
            <h2 onclick="toggleContent('recommendations')">📜 Sample Recommendations</h2>
            <div id="recommendations" class="content">
                <table>
                    <tr>
                        <th>User ID</th>
                        <th>Book ISBN</th>
                        <th>Book Title</th>
                        <th>Score</th>
                    </tr>
                    <tr>
                        <td>12345</td>
                        <td>978-0451524935</td>
                        <td>1984</td>
                        <td>4.87</td>
                    </tr>
                    <tr>
                        <td>67890</td>
                        <td>978-0141439600</td>
                        <td>Pride and Prejudice</td>
                        <td>4.75</td>
                    </tr>
                </table>
            </div>
        </div>

        <div class="box">
            <h2 onclick="toggleContent('whyReadNext')">🎯 Why ReadNext?</h2>
            <div id="whyReadNext" class="content">
                <ul>
                    <li>📌 **Personalized Recommendations** – No generic lists!</li>
                    <li>📌 **Data-Driven Insights** – Uses real user behavior.</li>
                    <li>📌 **Fast & Scalable** – Handles large datasets efficiently.</li>
                    <li>📌 **Beyond Books** – Can be applied to movies, music, and more!</li>
                </ul>
            </div>
        </div>

        <div class="box">
            <h2 onclick="toggleContent('futureEnhancements')">🚀 Future Enhancements</h2>
            <div id="futureEnhancements" class="content">
                <ul>
                    <li>🔹 Hybrid model (content-based + collaborative filtering).</li>
                    <li>🔹 Real-time recommendation updates.</li>
                    <li>🔹 Handling new users (cold-start problem).</li>
                    <li>🔹 Interactive web-based UI.</li>
                </ul>
            </div>
        </div>

        <div class="footer">
            💡 <strong>Ready to discover your next favorite book? Let ReadNext be your guide! 📖✨</strong>
        </div>
    </div>

</body>
</html>