<html><head>
<meta http-equiv="content-type" content="text/html; charset=UTF-8">
        <title>niro_pain Chat</title>
        <style>
            body { font-family: monospace; background: #111; color: #0f0; padding: 20px; }
            pre { white-space: pre-wrap; font-size: 12px; }
            .chatbox { border-top: 1px solid #0f0; margin-top: 1em; padding-top: 1em; }
            input, textarea { width: 100%; background: #222; color: #0f0; border: 1px solid #0f0; padding: 5px; }
            input[type=submit] { width: auto; margin-top: 5px; }
        </style>
    </head>
    <body>
        <h2>Willkommen bei niro_pain</h2>
        <pre>⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠸⣶⣦⡄⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⢀⣀⣀⣀⡀⢀⠀⢹⣿⣿⣆⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠙⠻⣿⣿⣷⣄⠨⣿⣿⣿⡌⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠘⣿⣿⣿⣷⣿⣿⣿⣿⣿⣶⣦⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⣠⣴⣾⣿⣮⣝⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠈⠉⠙⠻⢿⣿⣿⣿⣿⣿⣿⠟⣹⣿⡿⢿⣿⣿⣬⣶⣶⡶⠦⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⣀⣢⣙⣻⢿⣿⣿⣿⠎⢸⣿⠕⢹⣿⣿⡿⣛⣥⣀⣀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠈⠉⠛⠿⡏⣿⡏⠿⢄⣜⣡⠞⠛⡽⣸⡿⣟⡋⠉⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠰⠾⠿⣿⠁⠀⡄⠀⠀⠰⠾⠿⠛⠓⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⣀⠠⢐⢉⢷⣀⠛⠠⠐⠐⠠⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⣀⣠⣴⣶⣿⣧⣾⠡⠼⠎⢎⣋⡄⠆⠀⠱⡄⢉⠃⣦⡤⡀⠀⠀⠀⠀
⠀⠀⠐⠙⠻⢿⣿⣿⣿⣿⣿⣿⣄⡀⠀⢩⠀⢀⠠⠂⢀⡌⠀⣿⡇⠟⠀⠀⢄⠀
⠀⣴⣇⠀⡇⠀⠸⣿⣿⣿⣿⣽⣟⣲⡤⠀⣀⣠⣴⡾⠟⠀⠀⠟⠀⠀⠀⠀⡰⡀
⣼⣿⠋⢀⣇⢸⡄⢻⣟⠻⣿⣿⣿⣿⣿⣿⠿⡿⠟⢁⠀⠀⠀⠀⠀⢰⠀⣠⠀⠰
⢸⣿⡣⣜⣿⣼⣿⣄⠻⡄⡀⠉⠛⠿⠿⠛⣉⡤⠖⣡⣶⠁⠀⠀⠀⣾⣶⣿⠐⡀
⣾⡇⠈⠛⠛⠿⣿⣿⣦⠁⠘⢷⣶⣶⡶⠟⢋⣠⣾⡿⠃⠀⠀⠀⠰⠛⠉⠉⠀⠀
<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <title>Öffentliche Pinnwand</title>
  <style>
    body { font-family: Arial; background: #f4f4f4; padding: 20px; }
    #posts { background: white; padding: 10px; border-radius: 8px; max-width: 600px; margin-top: 20px; }
    .post { border-bottom: 1px solid #ddd; padding: 10px 0; }
    .post:last-child { border-bottom: none; }
    .nickname { font-weight: bold; }
  </style>
</head>
<body>

  <h1>📝 Öffentliche Pinnwand</h1>

  <form id="postForm">
    <input type="text" id="nickname" placeholder="Dein Nickname" required>
    <br><br>
    <textarea id="message" placeholder="Deine Nachricht" rows="4" cols="50" required></textarea>
    <br><br>
    <button type="submit">Posten</button>
  </form>

  <div id="posts"></div>

  <script>
    const form = document.getElementById('postForm');
    const postsDiv = document.getElementById('posts');

    form.addEventListener('submit', function(e) {
      e.preventDefault();
      const nickname = document.getElementById('nickname').value.trim();
      const message = document.getElementById('message').value.trim();

      if (nickname && message) {
        const post = document.createElement('div');
        post.className = 'post';
        post.innerHTML = `<span class="nickname">${nickname}</span>: ${message}`;
        postsDiv.prepend(post); // neue Beiträge oben
        form.reset();
      }
    });
  </script>

</body>
</html>

