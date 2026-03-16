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
  height:100vh;
  background-color: #000; /* background plotësisht i zi */
  background-image: url('https://www.denofgeek.com/wp-content/uploads/2020/05/GTA-5-feature-mod.jpg?fit=2560%2C1080');
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
  display:flex;
  justify-content:flex-start;
  align-items:flex-start;
  overflow:hidden;
}

/* Navbar vertikal thjesht fjalë */
nav {
  position:fixed;
  top:50px;
  left:20px;
  display:flex;
  flex-direction:column;
  gap:15px;
}
nav span {
  cursor:pointer;
  font-size:22px;
  font-weight:bold;
  transition: 0.3s;
}
nav span:hover { color:#ff0000; }

/* Div permbajtja */
#content {
  margin-left:200px;
  margin-top:50px;
  padding:25px;
  background: rgba(0,0,0,0.75); /* pak transparencë për lexim më të mirë */
  border-radius:12px;
  min-width:500px;
  min-height:250px;
  font-size:18px; /* font më i madh për rregulla dhe lexim */
  line-height:1.6;
}

/* Foto serveri djathtas-lart */
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
#serverPhoto img { width:100%; height:100%; object-fit:cover; }

a { color:#00f; text-decoration: underline; }
a:hover { color:#0ff; }
ul { margin-left:20px; }
</style>
</head>
<body>

<!-- Navbar me fjale thjesht -->
<nav>
  <span onclick="showContent('Rreth')">Rreth Vortex</span>
  <span onclick="showContent('Discord')">Discord</span>
  <span onclick="showContent('Rregullat')">Rregullat</span>
  <span onclick="showContent('Update')">Update</span>
</nav>

<!-- Div ku shfaqet permbajtja -->
<div id="content">
  <h2>Mirësevini në Vortex DeathMatch!</h2>
  <p>Kliko njërën nga fjalët majtas për të parë informacionin.</p>
</div>

<!-- Foto serveri djathtas-lart -->
<div id="serverPhoto">
  <img src="https://cdn.discordapp.com/attachments/1461646065580249313/1482879548092715018/Vortex_Logo.png?ex=69b93772&is=69b7e5f2&hm=f8232a3e41a06a340b099b7828dbd9941870679e96bce5c2c231a0f7950318b6&" alt="Server Photo">
</div>

<script>
function showContent(category) {
  let html = '';
  if(category === 'Rreth') {
    html = `<h2>Rreth Vortex DeathMatch</h2>
            <p>Vortex DeathMatch është krijuar nga tre persona të talentuar: <strong>Riki</strong>, <strong>Rakuna</strong> dhe <strong>Amari</strong>. 
            <strong>Amari</strong> dhe <strong>Riki</strong> janë themeluesit e serverit, ndërsa <strong>Rakuna</strong> kontribuoi si developer duke ndihmuar në zhvillimin e scriptave dhe mekanikave të lojës.</p>
            <p>Qëllimi i Vortex DeathMatch është të ofrojë një eksperiencë unike multiplayer ku lojtarët mund të përballen në arenat tona me mekanika të avancuara si Gun Game, Recoil të rregulluar dhe shumë përditësime që përmirësojnë gameplay-in.</p>
            <p>Kur hyni në server, do të shihni fillimisht ekranin kryesor me opsionet për të zgjedhur Discord, rregullat dhe update-t më të fundit. Ky është vendi ku çdo lojtar mund të njihet me komunitetin dhe të mësojë rregullat para se të fillojë lojën.</p>`;
  } else if(category === 'Discord') {
    html = `<h2>Discord</h2>
            <p>Join Discord serverin tonë për info dhe bashkëpunim me lojtarë të tjerë dhe developer-at:</p>
            <a href="https://discord.gg/SjKyJxkqfk" target="_blank">Kliko për të hyrë në Discord</a>`;
  } else if(category === 'Rregullat') {
    html = `<h2>Rregullat</h2>
            <ul>
              <li>Respekto të gjithë lojtarët</li>
              <li>Jo cheats ose exploits</li>
              <li>Mos abuzo me chat-in</li>
              <li>Respekto vendimet e adminëve</li>
              <li>Mos përdor gjuhë fyese ose diskriminuese</li>
              <li>Respekto kohën e respawn-it dhe rregullat e arenave</li>
            </ul>`;
  } else if(category === 'Update') {
    html = `<h2>Update</h2>
            <p>Këtu do tregohet çdo update i ri në server:</p>
            <ul>
              <li>Arena e re është shtuar me grafikë të avancuar</li>
              <li>Gun Game është përditësuar me armë të reja dhe balans të përmirësuar</li>
              <li>Recoil në Strp është rregulluar për një gameplay më realist</li>
              <li>Roli Whitelist është resetuar, lojtarët duhet të aplikojnë përsëri</li>
              <li>Shtim i eventeve të veçanta dhe missions për lojtarët</li>
            </ul>`;
  }
  document.getElementById("content").innerHTML = html;
}
</script>

</body>
</html>
