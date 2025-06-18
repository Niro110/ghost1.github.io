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

            <div>
                
            </div>
        </div>
    
    
    </body></html>
