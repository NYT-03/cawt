<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>GhostChat</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <h1>👻 Ghost Live Chat</h1>
  <div class="chat-container" id="chat">
    <!-- Messages appear here -->
  </div>

  <div class="input-area">
    <select id="user">
      <option value="👤 Ghost">👤 Ghost</option>
      <option value="🧠 Hacker">🧠 Hacker</option>
    </select>
    <input type="text" id="message" placeholder="Type your message..." />
    <button onclick="sendMessage()">Send</button>
  </div>

  <script src="script.js"></script>
</body>
</html>

