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

body {
  font-family: Arial, sans-serif;
  background-color: #111;
  color: #eee;
  text-align: center;
  margin: 0;
  padding: 0;
}

h1 {
  background-color: #222;
  padding: 20px;
  margin: 0;
  font-size: 28px;
  color: #00ffcc;
}

.chat-container {
  height: 400px;
  overflow-y: auto;
  border: 1px solid #444;
  margin: 20px;
  padding: 10px;
  background-color: #1e1e1e;
  text-align: left;
}

.message {
  margin: 5px 0;
  padding: 8px;
  border-radius: 10px;
  max-width: 70%;
}

.user-1 {
  background-color: #00ffcc;
  color: black;
  align-self: flex-start;
}

.user-2 {
  background-color: #ff00cc;
  color: white;
  align-self: flex-end;
  text-align: right;
}

.input-area {
  padding: 10px;
  background-color: #222;
}

input, select, button {
  padding: 8px;
  font-size: 16px;
  margin: 5px;
}

function sendMessage() {
  const chatBox = document.getElementById('chat');
  const message = document.getElementById('message').value.trim();
  const user = document.getElementById('user').value;

  if (message === "") return;

  const msgDiv = document.createElement('div');
  msgDiv.classList.add('message');

  if (user === "👤 Ghost") {
    msgDiv.classList.add('user-1');
    msgDiv.innerText = `${user}: ${message}`;
  } else {
    msgDiv.classList.add('user-2');
    msgDiv.innerText = `${user}: ${message}`;
  }

  chatBox.appendChild(msgDiv);
  document.getElementById('message').value = "";
  chatBox.scrollTop = chatBox.scrollHeight;
}
