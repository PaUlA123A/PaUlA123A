<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Vēstules un Attēli</title>
<style>
  body {
    font-family: Arial, sans-serif;
  }
  .italic-text {
    font-style: italic;
    color: black;
    text-transform: uppercase; /* Pārveido teikumu lielos burtos */
  }
  .container {
    max-width: 500px; /* Main container width */
    margin: 0 auto; /* Center the container horizontally */
  }
  .overlay img {
    max-width: 100%; /* Samazina pirmo attēlu platību */
    height: auto; /* Maintain aspect ratio */
    display: block; /* Centrē attēlu */
    margin: 0 auto 20px; /* Centrē attēlu horizontāli un pievieno atstarpi zem attēla */
  }
  #canvaContainer img {
    max-width: 100%; /* Padara Canva attēlu par centru un ierobežo tā izmērus */
    max-height: 500px; /* Norāda maksimālo augstumu, lai attēls nebūtu bezgalīgs */
    display: block; /* Centrē attēlu */
    margin: 0 auto; /* Centrē attēlu horizontāli */
  }
  .additional-text {
    margin-top: 20px; /* Pievieno atstarpi starp attēlu un tekstu */
  }
</style>
</head>
<body>

<div class="container" onclick="toggleImage()">
  <div class="overlay">
    <p class="italic-text">ČAU, KARĪNA, TEV PIENĀKUSI VĒSTULE!</p>
    <p class="additional-text">Spied uz vēstules, lai redzētu pārsteigumu!</p>
    <img src="https://i.ibb.co/3kzJgjV/Baby-Blue-Rec-Envelope-Front.jpg" alt="Aploksnes attēls">
  </div>
</div>
<div id="canvaContainer" style="display: none;">
  <img src="https://i.ibb.co/kxQp79M/Blue-Floral-Wedding-Invitation.png" alt="Otrais attēls">
</div>

<script>
  function toggleImage() {
    var container = document.querySelector('.container');
    var canvaContainer = document.getElementById('canvaContainer');
    container.classList.add('clicked');
    canvaContainer.style.display = 'block';
    var overlay = document.querySelector('.overlay');
    overlay.style.display = 'none';
  }
</script>

</body>
</html>
