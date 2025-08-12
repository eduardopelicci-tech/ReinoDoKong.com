<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Ilha da Caveira - Monstros</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Nosifer&display=swap');

  * { margin: 0; padding: 0; box-sizing: border-box; }
  body {
    background: url('https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=1470&q=80') no-repeat center center fixed;
    background-size: cover;
    color: #f0f0f0;
    font-family: Arial, sans-serif;
    min-height: 100vh;
    display: flex; flex-direction: column;
  }

  header {
    background: rgba(0,0,0,0.8); padding: 1rem 2rem; text-align: center;
    font-family: 'Nosifer', cursive; font-size: 2.8rem; letter-spacing: .15em;
    text-shadow: 2px 2px 6px #000;
  }

  nav { background: rgba(0,0,0,0.7); padding: .5rem 1rem; text-align:center; }
  nav a {
    color: #d1a54a; text-decoration:none; font-weight:bold; margin:0 .6rem; font-size:1.05rem;
    transition: color .25s; cursor:pointer;
  }
  nav a:hover { color:#f7e06e; }

  main {
    flex-grow:1; background: rgba(0,0,0,0.6); padding: 2rem;
    display: grid; grid-template-columns: repeat(auto-fit,minmax(250px,1fr)); gap:1.6rem;
  }

  .card {
    background: rgba(30,30,30,0.92); border:2px solid #7a5c1b; border-radius:10px; overflow:hidden;
    cursor:pointer; box-shadow:0 0 15px #7a5c1b; transition: transform .25s, box-shadow .25s;
  }
  .card:hover { transform: scale(1.04); box-shadow:0 0 30px #d1a54a; }
  .card img { width:100%; height:180px; object-fit:cover; display:block; }
  .card-content { padding:1rem; }
  .card-content h3 { font-family:'Nosifer',cursive; color:#d1a54a; margin-bottom:.4rem; font-size:1.4rem; text-shadow:1px 1px 3px #000; }
  .card-content p { color:#ccc; font-size:.95rem; line-height:1.3; }

  footer { background: rgba(0,0,0,0.8); text-align:center; padding:1rem; color:#aaa; font-size:.85rem; }

  /* Monster page */
  .monster-page { max-width:900px; margin:2rem auto; background: rgba(15,15,15,0.92); border-radius:12px; padding:2rem; box-shadow:0 0 30px #7a5c1b; }
  .monster-page img { width:100%; max-height:420px; object-fit:cover; border-radius:8px; margin-bottom:1.2rem; box-shadow:0 0 20px #d1a54a; }
  .monster-page h2 { font-family:'Nosifer',cursive; color:#d1a54a; font-size:2.2rem; margin-bottom:.8rem; text-align:center; text-shadow:2px 2px 5px #000; }
  .monster-page h3 { margin-top:1.2rem; color:#f7e06e; font-size:1.15rem; border-bottom:2px solid #d1a54a; padding-bottom:.35rem; }
  .monster-page p, .monster-page ul { color:#ddd; font-size:1rem; line-height:1.45; margin-bottom:.6rem; }
  .monster-page ul { margin-left:1.2rem; }

  .back-button { display:inline-block; margin-top:1.2rem; padding:.6rem 1rem; background:#d1a54a; color:#000; font-weight:700; border-radius:6px; text-decoration:none; box-shadow:0 0 10px #d1a54a; cursor:pointer; }
  .back-button:hover { background:#f7e06e; }

  @media (max-width:600px) {
    header { font-size:2rem; padding:1rem; }
    main { padding:1rem; gap:1rem; }
    .card img { height:140px; }
    .monster-page { padding:1rem; margin:1rem; }
  }
</style>
</head>
<body>

<header>A OITAVA MARAVILHA</header>

<nav>
  <a onclick="showHome(); return false;">Início</a>
  <a onclick="showMonster('kong1'); return false;">Kong (1ª Temp.)</a>
  <a onclick="showMonster('kong2'); return false;">Kong (2ª Temp.)</a>
  <a onclick="showMonster('thalzor'); return false;">Thal'Zor</a>
  <a onclick="showMonster('bonecrawler'); return false;">Bonecrawler</a>
  <a onclick="showMonster('primattus'); return false;">Primattus Golem</a>
  <a onclick="showMonster('drex'); return false;">D-Rex</a>
</nav>

<main id="main-content">

  <!-- Home / cards -->
  <section id="home-page">
    <div class="card" onclick="showMonster('kong1')">
      <img src="file:///H:/EA%20FC%202025/kong_jovem2.png" alt="Kong 1ª temporada" />
      <div class="card-content">
        <h3>Kong (1ª Temporada)</h3>
        <p>Filhote em crescimento que jurou ser rei — curioso, ágil e feroz quando provocado.</p>
      </div>
    </div>

    <div class="card" onclick="showMonster('kong2')">
      <img src="file:///C:/Users/gabri/OneDrive/Imagens/Capturas%20de%20tela/Captura%20de%20tela%202025-08-11%20225347.png" alt="Kong 2ª temporada placeholder" />
      <div class="card-content">
        <h3>Kong (2ª Temporada)</h3>
        <p>Ficha da segunda temporada — Em breve...</p>
      </div>
    </div>

    <div class="card" onclick="showMonster('thalzor')">
      <img src="file:///C:/Users/gabri/OneDrive/Imagens/Capturas%20de%20tela/Captura%20de%20tela%202025-08-11%20225515.png" alt="Thal'Zor" />
      <div class="card-content">
        <h3>Thal'Zor</h3>
        <p>Dinossauro alfa brutal e impiedoso, atual rei da Ilha da Caveira.</p>
      </div>
    </div>

    <div class="card" onclick="showMonster('bonecrawler')">
      <img src="file:///C:/Users/gabri/OneDrive/Imagens/Capturas%20de%20tela/Captura%20de%20tela%202025-08-11%20225134.png" alt="Bonecrawler" />
      <div class="card-content">
        <h3>Bonecrawler</h3>
        <p>Skull Crawler que evoluiu até ter estrutura óssea reforçada — líder solitário e temido.</p>
      </div>
    </div>

    <div class="card" onclick="showMonster('primattus')">
      <img src="file:///C:/Users/gabri/OneDrive/Imagens/Capturas%20de%20tela/Captura%20de%20tela%202025-08-11%20225705.png" alt="Primattus Golem placeholder" />
      <div class="card-content">
        <h3>Primattus Golem</h3>
        <p>Golem rochoso antigo, quase tão grande quanto Kong — guardião petrificado ressurgindo.</p>
      </div>
    </div>

    <div class="card" onclick="showMonster('drex')">
      <img src="file:///C:/Users/gabri/OneDrive/Imagens/Capturas%20de%20tela/Captura%20de%20tela%202025-08-11%20230437.png" alt="D-Rex placeholder" />
      <div class="card-content">
        <h3>D-Rex</h3>
        <p>Ficha em breve...</p>
      </div>
    </div>
  </section>

  <!-- Páginas individuais -->

  <!-- Kong 1ª temporada -->
  <section id="monster-kong1" class="monster-page" style="display:none;">
    <h2>King Kong (1ª Temporada)</h2>
    <img src="file:///H:/EA%20FC%202025/kong_jovem.png.png" alt="Kong 1ª temporada" />
    <h3>Ficha</h3>
    <p><strong>Nome:</strong> King Kong<br/>
       <strong>Idade:</strong> 3 anos<br/>
       <strong>Altura:</strong> Início: 8 m • Final: 13 m<br/>
       <strong>Peso:</strong> ~15 a 25 toneladas<br/>
       <strong>Espécie:</strong> Titanus Kong<br/>
       <strong>Afiliação:</strong> Protetor parcial da Ilha da Caveira (em desenvolvimento)<br/>
       <strong>Status:</strong> Vivo</p>

    <h3>História</h3>
    <p>Antes de Kong nascer, Kratos governava a ilha. Thal'Zor liderou uma rebelião que matou Mara (mãe de Kong) e Kratos. Kong, escondido, testemunhou a morte dos pais e jurou se tornar rei. Cresceu sozinho, aprendendo a sobreviver, caçar e lutar.</p>

    <h3>Aparência</h3>
    <p>Mais magro, músculos em formação, pelagem lisa e olhos totalmente amarelos (sem pupilas visíveis).</p>

    <h3>Personalidade</h3>
    <p>Curioso, explorador, inteligente para sua idade, imaturo em momentos de raiva. Extremamente protetor com o que gosta; perde o controle ao ver algo querido destruído.</p>

    <h3>Habilidades</h3>
    <ul>
      <li>Força juvenil — derruba criaturas maiores.</li>
      <li>Agilidade superior à versão adulta.</li>
      <li>Inteligência tática (analisa antes de atacar).</li>
      <li>Grande mobilidade e escalada.</li>
    </ul>

    <h3>Comportamento</h3>
    <p>Patrulha áreas pequenas do território, enfrenta ameaças diretas e demonstra aprendizado contínuo com cada luta.</p>

    <a class="back-button" onclick="showHome(); return false;">Voltar</a>
  </section>

  <!-- Kong 2ª temporada (em breve) -->
  <section id="monster-kong2" class="monster-page" style="display:none;">
    <h2>Kong (2ª Temporada)</h2>
    <img src="file:///C:/Users/gabri/OneDrive/Imagens/Capturas%20de%20tela/Captura%20de%20tela%202025-08-11%20043207.png" alt="Kong 2ª temporada" />
    <p>Ficha da segunda temporada — Em breve...</p>
    <a class="back-button" onclick="showHome(); return false;">Voltar</a>
  </section>

  <!-- Thal'Zor -->
  <section id="monster-thalzor" class="monster-page" style="display:none;">
    <h2>Thal'Zor</h2>
    <img src="file:///C:/Users/gabri/OneDrive/Imagens/Capturas%20de%20tela/Captura%20de%20tela%202025-08-11%20222456.png" alt="Thal'Zor" />
    <h3>História</h3>
    <p>Dinossauro alfa brutal que liderou rebeliões e destruiu a antiga ordem da ilha.</p>
    <h3>Ficha Técnica</h3>
    <p><strong>Espécie:</strong> Dinossauro alfa<br/>
       <strong>Altura:</strong> ~14 metros<br/>
       <strong>Personalidade:</strong> Impiedoso, brutal, dominante</p>
    <a class="back-button" onclick="showHome(); return false;">Voltar</a>
  </section>

  <!-- Bonecrawler -->
  <section id="monster-bonecrawler" class="monster-page" style="display:none;">
    <h2>Bonecrawler</h2>
    <img src="file:///C:/Users/gabri/OneDrive/Imagens/Capturas%20de%20tela/Captura%20de%20tela%202025-08-11%20202529.png" alt="Bonecrawler" />
    <h3>Ficha Técnica</h3>
    <p><strong>Espécie:</strong> Skull Crawler osseus (variação evoluída)<br/>
       <strong>Altura:</strong> 27 metros<br/>
       <strong>Peso:</strong> 65 toneladas</p>

    <h3>História</h3>
    <p>Os nativos falam de um “demônio branco” que vive nas profundezas. O Bonecrawler é uma evolução rara de Skull Crawler que perdeu carne e desenvolveu ossos externos reforçados. Lidera pequenos grupos, respeitado pela força, mas vigiado até pelo Alpha.</p>

    <h3>Aparência</h3>
    <p>Estrutura esquelética exposta, ossos marfim, olhos âmbar, ossos reforçados nas áreas de impacto; movimentos mais lentos, porém devastadores.</p>

    <h3>Comportamento</h3>
    <p>Territorial, embosca de locais elevados ou debaixo da terra; liderança instintiva sobre grupos menores; solitário por natureza.</p>

    <h3>Habilidades</h3>
    <ul>
      <li>Força aumentada — capaz de esmagar rochas.</li>
      <li>Resistência óssea — resistente a projéteis.</li>
      <li>Garras afiadas — cortam madeira e perfuram metal leve.</li>
      <li>Emboscada — mantém padrão furtivo na caçada.</li>
    </ul>

    <a class="back-button" onclick="showHome(); return false;">Voltar</a>
  </section>

  <!-- Primattus Golem -->
  <section id="monster-primattus" class="monster-page" style="display:none;">
    <h2>Primattus Golem</h2>
    <img src="file:///C:/Users/gabri/OneDrive/Imagens/Capturas%20de%20tela/Captura%20de%20tela%202025-08-11%20202849.png" alt="Primattus Golem" />
    <h3>Ficha Técnica</h3>
    <p><strong>Espécie:</strong> Primattus Golem<br/>
       <strong>Altura:</strong> 31 metros<br/>
       <strong>Peso estimado:</strong> ~1.200 toneladas</p>

    <h3>História</h3>
    <p>Antiga espécie que moldava a ilha como santuário. Reproduz lento e foi dizimada por guerras prolongadas. O último entrou em hibernação pétrea e agora desperta, atraído pelo retorno dos Skullcrawlers e pela presença de Kong — que ele vê como intruso.</p>

    <h3>Personalidade & Comportamento</h3>
    <p>Estratégico, calmo e implacável em combate; estilo de luta direto, aproveitando massa e resistência; objetivo: erradicar não-Primattus da ilha.</p>

    <h3>Habilidades</h3>
    <ul>
      <li>Força bruta colossal — esmagamento de rochas.</li>
      <li>Resistência natural — pele rochosa protege de impactos e armas convencionais.</li>
      <li>Ancoragem de combate — pode fincar-se e tornar-se quase inamovível.</li>
      <li>Camuflagem parcial — musgo e vegetação ajudam a esconder-se.</li>
    </ul>

    <a class="back-button" onclick="showHome(); return false;">Voltar</a>
  </section>

  <!-- D-Rex (placeholder) -->
  <section id="monster-drex" class="monster-page" style="display:none;">
    <h2>D-Rex</h2>
    <img src="file:///C:/Users/gabri/OneDrive/Imagens/Capturas%20de%20tela/Captura%20de%20tela%202025-08-11%20230320.png" alt="D-Rex placeholder" />
    <p>Ficha do D-Rex — Em breve...</p>
    <a class="back-button" onclick="showHome(); return false;">Voltar</a>
  </section>

</main>

<footer>© 2025 Série A Oitava Maravilha - Criado por Eduardo Pelicci</footer>

<script>
  function showHome() {
    document.getElementById('home-page').style.display = 'grid';
    const ids = ['monster-kong1','monster-kong2','monster-thalzor','monster-bonecrawler','monster-primattus','monster-drex'];
    ids.forEach(id => { const el = document.getElementById(id); if (el) el.style.display = 'none'; });
  }

  function showMonster(name) {
    showHome();
    const map = {
      'kong1': 'monster-kong1',
      'kong2': 'monster-kong2',
      'thalzor': 'monster-thalzor',
      'bonecrawler': 'monster-bonecrawler',
      'primattus': 'monster-primattus',
      'drex': 'monster-drex'
    };
    const id = map[name];
    if (id) document.getElementById(id).style.display = 'block';
  }

  // mostra por padrão a home
  showHome();
</script>

</body>
</html>
