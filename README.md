<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Happy Birthday, my love!</title>

  <!-- Google handwriting font -->
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet"/>

  <style>
    /* ----- GLOBAL STYLE ----- */
    :root {
      --bg: #fffaf0;
      --ink: #24324a;
      --accent: #ff6b81;
      --hint: #aa4a44;
    }
    *{box-sizing:border-box;margin:0;padding:0}
    body{
      background:var(--bg);
      color:var(--ink);
      font-family:'Pacifico',cursive;
      text-align:center;
      padding:2.5rem 1rem;
    }

    /* ----- LANDING SECTION ----- */
    h1{
      font-size:2.8rem;
      margin-bottom:.25em;
    }
    .hearts{color:var(--accent);font-size:1.6rem;animation:float 1.6s ease-in-out infinite}
    .click-me{color:var(--hint);font-size:1.15rem;margin-bottom:1.2rem}
    .main-doodle{
      width:230px;
      cursor:pointer;
      transition:transform .3s;
    }
    .main-doodle:hover{transform:scale(1.05)}

    /* ----- MENU SECTION ----- */
    #menu{
      display:none;
      flex-wrap:wrap;
      justify-content:center;
      gap:2.5rem;
      margin-top:2.8rem;
    }
    #menu img{
      width:80px;
      cursor:pointer;
      transition:transform .25s;
    }
    #menu img:hover{transform:scale(1.15)}

    @keyframes float{0%,100%{transform:translateY(0)}50%{transform:translateY(-6px)}}
  </style>
</head>
<body>

  <h1>Happy Birthday, my love! <span class="hearts">❤❤❤</span></h1>
  <div class="click-me">click me ↓</div>

  <!-- 👫 Your FIRST generated SVG doodle goes here -->
  <!-- Save the file as boy-girl-doodle.svg in the same folder -->
  <img src="boy-girl-doodle.svg" alt="Couple holding hands" class="main-doodle" onclick="showMenu()"/>

  <!-- Hidden menu that appears after the doodle is clicked -->
  <div id="menu">
    <!-- three tiny doodle‑buttons -->
    <img src="letter-doodle.svg"  alt="Letter"  onclick="go('letter.html')"/>
    <img src="reasons-doodle.svg" alt="23 Reasons" onclick="go('reasons.html')"/>
    <img src="album-doodle.svg"   alt="Album"  onclick="go('album.html')"/>
  </div>

  <script>
    function showMenu(){ document.getElementById('menu').style.display='flex'; }
    function go(page){ window.location.href = page; }
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Your Letter</title>
<link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet"/>
<style>
  body{background:#fffaf0;font-family:'Pacifico',cursive;color:#24324a;padding:2rem;line-height:1.6;max-width:700px;margin:auto}
  a{color:#ff6b81;text-decoration:none}
</style>
</head>
<body>
  <h1>My Letter to You 💌</h1>
  <p>…write your beautiful message here…</p>
  <p><a href="index.html">← back</a></p>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>23 Reasons I Love You</title>
<link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet"/>
<style>
  body{background:#fffaf0;font-family:'Pacifico',cursive;color:#24324a;padding:2rem;max-width:750px;margin:auto}
  ul{list-style:none;padding:0;margin-top:1.6rem}
  li{background:#fde7d7;padding:.8rem 1rem;border-radius:10px;margin:.5rem 0}
  li::before{content:"❤ ";color:#ff6b81}
  a{color:#ff6b81;text-decoration:none}
</style>
</head>
<body>
  <h1>23 Reasons Why I Love You</h1>
  <ul>
    <li>You make me feel safe</li>
    <li>You listen — truly listen</li>
    <li>Your smile melts away even the worst days</li>
    <!-- …continue all 23 here … -->
    <li>Because you’re you — and that’s all I ever needed</li>
  </ul>
  <p><a href="index.html">← back</a></p>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Our Album</title>
<link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet"/>
<style>
  body{background:#fffaf0;font-family:'Pacifico',cursive;color:#24324a;text-align:center;margin:0}
  #frame{max-width:100%;height:calc(100vh - 120px);object-fit:contain;margin-top:1rem}
  button{font-family:'Pacifico',cursive;font-size:1.2rem;padding:.4rem 1.2rem;margin:0 .6rem;border:none;background:#ff6b81;color:#fff;border-radius:10px;cursor:pointer}
</style>
</head>
<body>
  <h1>Our Little Photo Book 📖</h1>
  <img id="frame" src="photos/1.jpg" alt="album"/>
  <div style="margin:1rem">
    <button onclick="prev()">Prev</button>
    <button onclick="next()">Next</button>
  </div>
  <p><a href="index.html">← back</a></p>

  <script>
    const pics=["photos/1.jpg","photos/2.jpg","photos/3.jpg","photos/4.jpg"]; // add more paths if needed
    let i=0;
    function show(){document.getElementById('frame').src=pics[i];}
    function next(){i=(i+1)%pics.length;show();}
    function prev(){i=(i-1+pics.length)%pics.length;show();}
  </script>
</body>
</html>
