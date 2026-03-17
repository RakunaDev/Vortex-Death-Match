<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Vortex Deathmatch</title>

<style>
* { margin:0; padding:0; box-sizing:border-box; }

body {
  font-family: Arial, sans-serif;
  color: white;
  min-height:100vh;
  background-color: #000;
  background-image: url('https://www.denofgeek.com/wp-content/uploads/2020/05/GTA-5-feature-mod.jpg?fit=2560%2C1080');
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
  overflow-y: auto; /* FIX SCROLL */
}

/* Sidebar (ana majtas) */
nav {
  position:fixed;
  top:0;
  left:0;
  width:220px;
  height:100%;
  background:#000; /* E ZEZE */
  padding-top:20px;
  display:flex;
  flex-direction:column;
  align-items:center;
}

/* Titulli sipër */
nav .logo {
  font-size:20px;
  font-weight:bold;
  margin-bottom:30px;
}

/* Linkat */
nav span {
  cursor:pointer;
  font-size:18px;
  margin:10px 0;
  transition: 0.3s;
}

nav span:hover { color:#ff0000; }

/* Content */
#content {
  margin-left:240px;
  margin-top:50px;
  padding:25px;
  background: rgba(0,0,0,0.75);
  border-radius:12px;
  max-width:700px;
  font-size:18px;
  line-height:1.6;
}

/* Foto djathtas */
#serverPhoto {
  position:fixed;
  top:20px;
  right:20px;
  width:180px;
  height:180px;
  border-radius:12px;
  overflow:hidden;
  border:3px solid #ff0000;
}

#serverPhoto img {
  width:100%;
  height:100%;
  object-fit:cover;
}

a { color:#00f; }
a:hover { color:#0ff; }

ul { margin-left:20px; }
</style>
</head>

<body>

<!-- Sidebar -->
<nav>
  <div class="logo">Vortex DM</div>
  <span onclick="showContent('Rreth')">Rreth Vortex</span>
  <span onclick="showContent('Discord')">Discord</span>
  <span onclick="showContent('Rregullat')">Rregullat</span>
  <span onclick="showContent('Update')">Update</span>
</nav>

<!-- Content -->
<div id="content">
  <h2>Mirësevini në Vortex DeathMatch!</h2>
  <p>Kliko njërën nga menytë majtas për të parë informacionin.</p>
</div>

<!-- Logo djathtas -->
<div id="serverPhoto">
  <img src="https://cdn.discordapp.com/attachments/1461646065580249313/1482879548092715018/Vortex_Logo.png" alt="Server Logo">
</div>

<script>
function showContent(category) {
  let html = '';

  if(category === 'Rreth') {
    html = `<h2>Rreth Vortex DeathMatch</h2>

<p><strong>Vortex DeathMatch</strong> është një server i fokusuar në aksion të shpejtë dhe gameplay konkurrues.</p>

<p><strong>Serveri përmban:</strong></p>
<ul>
<li>Arena System</li>
<li>Gun Game</li>
<li>Custom Recoil</li>
<li>Vehicle Rent</li>
<li>Stats & Leaderboard</li>
<li>Loadout System</li>
<li>Fast Respawn</li>
</ul>`;
  }

  else if(category === 'Discord') {
    html = `<h2>Discord</h2>
    <a href="https://discord.gg/SjKyJxkqfk" target="_blank">Kliko për të hyrë</a>`;
  }

  else if(category === 'Rregullat') {
    html = `<h2>Rregullat</h2>
<ul>
<li>Respekto lojtarët</li>
<li>Jo cheats</li>
<li>Jo spam</li>
<li>Respekto adminët</li>
</ul>`;
  }

  else if(category === 'Update') {
    html = `<h2>Update</h2>
<ul>
<li>Arena e re</li>
<li>Gun Game update</li>
<li>Recoil fix</li>
<li>Whitelist reset</li>
</ul>`;
  }

  document.getElementById("content").innerHTML = html;
}
</script>

</body>
</html>
