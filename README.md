# Petrified-Wedding-of-the-Himalayas-A-Digital-Archaeological-Preservation-Project-of-Ghora-Gali-Gool
This project digitally documents Ghora Gali, an archaeological site in the Himalayan mountains of Indian Occupied Kashmir featuring around 200 stone sculptures. Despite its historical and cultural significance, Ghora Gali remains largely unrecorded and at risk of erasure. 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ghora Gali - Petrified Wedding of the Himalayas</title>
<style>

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  font-family: Georgia, serif;
  background-color: #111;
  color: #ddd;
  font-size: 18px;
  line-height: 1.8;
}

.navbar {
  position: fixed;
  top: 0;
  width: 100%;
  background-color: #1a1a1a;
  padding: 15px 0;
  text-align: center;
  z-index: 1000;
  border-bottom: 2px solid #8b6914;
}

.navbar a {
  color: #d4a843;
  text-decoration: none;
  margin: 0 15px;
  font-family: Arial, sans-serif;
  font-size: 13px;
  font-weight: bold;
  letter-spacing: 1px;
  text-transform: uppercase;
}

.navbar a:hover { color: #ffffff; }

.hero {
  height: 100vh;
  background-color: #000;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 20px;
}

.hero-tag {
  font-family: Arial, sans-serif;
  font-size: 11px;
  letter-spacing: 5px;
  text-transform: uppercase;
  color: #8b6914;
  margin-bottom: 25px;
}

.hero h1 {
  font-size: 54px;
  color: #f0e6d0;
  line-height: 1.2;
  margin-bottom: 20px;
}

.hero h1 span { color: #d4a843; font-style: italic; }

.hero p {
  font-size: 16px;
  color: #aaa;
  font-family: Arial, sans-serif;
  letter-spacing: 2px;
  margin-bottom: 8px;
}

.hero .author {
  font-style: italic;
  color: #d4a843;
  font-size: 20px;
  margin-top: 20px;
}

.arrow {
  margin-top: 50px;
  font-size: 28px;
  color: #8b6914;
  animation: bounce 2s infinite;
}

@keyframes bounce {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(10px); }
}

.section {
  max-width: 900px;
  margin: 0 auto;
  padding: 80px 30px;
  border-bottom: 1px solid #333;
}

.section-tag {
  font-family: Arial, sans-serif;
  font-size: 11px;
  letter-spacing: 4px;
  text-transform: uppercase;
  color: #8b6914;
  margin-bottom: 15px;
  display: block;
}

h2 {
  font-size: 30px;
  color: #d4a843;
  font-weight: normal;
  margin-bottom: 25px;
}

p { color: #ccc; margin-bottom: 20px; }

.abstract {
  border-left: 4px solid #8b6914;
  padding-left: 25px;
  font-style: italic;
  color: #bbb;
  margin-bottom: 40px;
}

.quote {
  text-align: center;
  border-top: 1px solid #444;
  border-bottom: 1px solid #444;
  padding: 30px 20px;
  margin: 40px 0;
  font-size: 22px;
  color: #d4a843;
  font-style: italic;
}

.goals { list-style: none; margin: 20px 0; }
.goals li {
  padding: 12px 0 12px 30px;
  border-bottom: 1px solid #333;
  color: #ccc;
  position: relative;
}
.goals li:before {
  content: "▶";
  position: absolute;
  left: 0;
  color: #8b6914;
  font-size: 10px;
  top: 16px;
}

/* CATEGORY TABS */
.tabs {
  display: flex;
  gap: 5px;
  margin-bottom: 25px;
  flex-wrap: wrap;
}

.tab-btn {
  padding: 10px 18px;
  background-color: #222;
  border: 1px solid #444;
  color: #aaa;
  cursor: pointer;
  font-family: Arial, sans-serif;
  font-size: 12px;
  letter-spacing: 1px;
  text-transform: uppercase;
}

.tab-btn:hover { background-color: #333; color: #fff; }
.tab-btn.active { background-color: #8b6914; border-color: #8b6914; color: #fff; }

/* GALLERY */
.gallery {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 8px;
}

.gallery-item {
  position: relative;
  height: 220px;
  overflow: hidden;
  border: 1px solid #444;
  cursor: pointer;
  background-color: #1a1a1a;
}

.gallery-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
  transition: transform 0.4s;
}

.gallery-item:hover img { transform: scale(1.06); }

.gallery-item .cap {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(0,0,0,0.8);
  color: #d4a843;
  font-size: 11px;
  font-family: Arial, sans-serif;
  padding: 8px 10px;
  transform: translateY(100%);
  transition: transform 0.3s;
}

.gallery-item:hover .cap { transform: translateY(0); }

.gallery-item .cat-badge {
  position: absolute;
  top: 8px;
  left: 8px;
  background-color: rgba(139,105,20,0.9);
  color: #fff;
  font-size: 10px;
  font-family: Arial, sans-serif;
  padding: 3px 8px;
  letter-spacing: 1px;
}

/* LIGHTBOX */
.lightbox {
  display: none;
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background-color: rgba(0,0,0,0.97);
  z-index: 9999;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.lightbox.show { display: flex; }

.lightbox img {
  max-width: 80%;
  max-height: 75vh;
  border: 1px solid #444;
  object-fit: contain;
}

.lb-caption {
  color: #d4a843;
  font-family: Arial, sans-serif;
  font-size: 14px;
  margin-top: 15px;
  text-align: center;
  letter-spacing: 1px;
}

.lb-category {
  color: #8b6914;
  font-family: Arial, sans-serif;
  font-size: 11px;
  margin-top: 5px;
  text-align: center;
  letter-spacing: 2px;
  text-transform: uppercase;
}

.lb-close {
  position: absolute;
  top: 20px; right: 30px;
  font-size: 42px;
  color: #aaa;
  cursor: pointer;
  background: none;
  border: none;
}

.lb-close:hover { color: #fff; }

.lb-prev {
  position: absolute;
  left: 15px; top: 50%;
  transform: translateY(-50%);
  font-size: 52px;
  color: #aaa;
  cursor: pointer;
  background: none;
  border: none;
  padding: 10px;
}

.lb-next {
  position: absolute;
  right: 15px; top: 50%;
  transform: translateY(-50%);
  font-size: 52px;
  color: #aaa;
  cursor: pointer;
  background: none;
  border: none;
  padding: 10px;
}

.lb-prev:hover, .lb-next:hover { color: #fff; }

.lb-counter {
  position: absolute;
  top: 25px; left: 30px;
  color: #666;
  font-family: Arial, sans-serif;
  font-size: 13px;
}

/* SCULPTURE PAIRS SECTION */
.pairs-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 30px;
  margin-top: 30px;
}

.pair-card {
  border: 1px solid #333;
  background-color: #1a1a1a;
  overflow: hidden;
}

.pair-card-header {
  background-color: #222;
  padding: 12px 16px;
  border-bottom: 1px solid #333;
}

.pair-card-title {
  color: #d4a843;
  font-family: Arial, sans-serif;
  font-size: 13px;
  font-weight: bold;
  letter-spacing: 1px;
  text-transform: uppercase;
}

.pair-card-sub {
  color: #666;
  font-family: Arial, sans-serif;
  font-size: 11px;
  margin-top: 4px;
}

.pair-images {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 4px;
  padding: 8px;
}

.pair-images img {
  width: 100%;
  height: 140px;
  object-fit: cover;
  display: block;
  cursor: pointer;
  border: 1px solid #333;
  transition: opacity 0.3s;
}

.pair-images img:hover { opacity: 0.8; }

.pair-images.three-col {
  grid-template-columns: repeat(3, 1fr);
}

.pair-desc {
  padding: 12px 16px;
  font-family: Arial, sans-serif;
  font-size: 12px;
  color: #888;
  border-top: 1px solid #222;
  line-height: 1.6;
}

/* MAP */
.map-container {
  margin-top: 30px;
  border: 1px solid #444;
  overflow: hidden;
}

.map-container iframe {
  width: 100%;
  height: 400px;
  display: block;
  border: none;
}

.map-title {
  background-color: #1a1a1a;
  padding: 12px 16px;
  font-family: Arial, sans-serif;
  font-size: 11px;
  color: #666;
  letter-spacing: 2px;
  text-transform: uppercase;
}

/* TIMELINE */
.timeline { list-style: none; margin-top: 30px; }
.timeline li {
  display: grid;
  grid-template-columns: 160px 1fr;
  gap: 20px;
  padding: 20px 0;
  border-bottom: 1px solid #333;
}
.timeline li:last-child { border-bottom: none; }
.tl-date {
  font-family: Arial, sans-serif;
  font-size: 12px;
  color: #8b6914;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
  padding-top: 3px;
}
.tl-desc { color: #ccc; }

/* ACCORDION */
.accordion-item { border: 1px solid #333; margin-bottom: 8px; }
.accordion-header {
  background-color: #1a1a1a;
  padding: 15px 20px;
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #d4a843;
  font-family: Arial, sans-serif;
  font-size: 14px;
}
.accordion-header:hover { background-color: #222; }
.accordion-arrow { font-size: 12px; transition: transform 0.3s; }
.accordion-header.open .accordion-arrow { transform: rotate(180deg); }
.accordion-body {
  display: none;
  padding: 20px;
  color: #ccc;
  border-top: 1px solid #333;
  line-height: 1.8;
}
.accordion-body.open { display: block; }

/* BIBLIOGRAPHY */
.bib { list-style: none; margin-top: 20px; }
.bib li {
  padding: 12px 0 12px 25px;
  text-indent: -25px;
  border-bottom: 1px solid #222;
  color: #888;
  font-size: 15px;
  line-height: 1.7;
}
.bib li a { color: #d4a843; text-decoration: none; }
.bib li a:hover { text-decoration: underline; }

/* BACK TO TOP */
.back-to-top {
  position: fixed;
  bottom: 30px; right: 30px;
  background-color: #8b6914;
  color: #fff;
  border: none;
  width: 45px; height: 45px;
  font-size: 20px;
  cursor: pointer;
  display: none;
  z-index: 999;
}
.back-to-top:hover { background-color: #d4a843; color: #000; }

/* FOOTER */
footer {
  text-align: center;
  padding: 50px 20px;
  background-color: #0a0a0a;
  font-family: Arial, sans-serif;
  font-size: 12px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: #444;
  border-top: 1px solid #222;
}

/* RESPONSIVE */
@media (max-width: 700px) {
  .hero h1 { font-size: 32px; }
  .gallery { grid-template-columns: repeat(2, 1fr); }
  .pairs-grid { grid-template-columns: 1fr; }
  .timeline li { grid-template-columns: 1fr; gap: 5px; }
  .navbar a { margin: 0 8px; font-size: 11px; }
}

</style>
</head>
<body>

<button class="back-to-top" id="backToTop" onclick="window.scrollTo({top:0,behavior:'smooth'})">↑</button>

<!-- NAVIGATION -->
<div class="navbar">
  <a href="#about">About</a>
  <a href="#gallery">Photos</a>
  <a href="#sculptures">Sculptures</a>
  <a href="#methodology">Methodology</a>
  <a href="#location">Location</a>
  <a href="#timeline">Timeline</a>
  <a href="#bibliography">Bibliography</a>
</div>

<!-- HERO -->
<div class="hero">
  <p class="hero-tag">Digital Archaeological Preservation Project</p>
  <h1>Petrified Wedding<br><span>of the Himalayas</span></h1>
  <p>Ghora Gali Gool &nbsp;·&nbsp; Indian Occupied Kashmir</p>
  <p class="author">Ashfaq Ahmed</p>
  <div class="arrow">↓</div>
</div>

<!-- ABOUT -->
<div class="section" id="about">
  <span class="section-tag">Abstract</span>
  <div class="abstract">
    <p>This project digitally documents Ghora Gali, an archaeological site in the
    Himalayan mountains of Indian Occupied Kashmir featuring around 200 stone
    sculptures. Despite its historical and cultural significance, Ghora Gali
    remains largely unrecorded and at risk of erasure. Using photography,
    videography, GPS geotagging, and 3D modeling, this project creates an online
    archive preserving Ghora Gali's material history and local folklore.</p>
  </div>

  <h2 style="margin-top:40px;">Growing up, I was told never to go to Ghora Gali.</h2>

  <p>Ghora Gali — horse alley — Gool in Indian Occupied Kashmir is considered off
  limits, shrouded in local cautionary tales and folklore. My mother, like many
  others in my village who could not read or write but carried vast archives in
  their memories, would lower her voice whenever the name Ghora Gali came up.</p>

  <p>Folklore goes that in the Himalayan forests, long long ago, a wedding
  procession climbed the mountain pass: men, women and children on horses, drums
  echoing across the Pir Panjal range. Before they could reach their destination,
  the <strong style="color:#f0e6d0;">jinns</strong> — demons and spirits —
  arrived and overpowered the wedding party, turning everyone into stone.
  The wedding froze in time. The jinn never left.</p>

  <div class="quote">
    "At Ghora Gali, history did not end. It hardened and waited."
  </div>

  <p>Only later did I learn that Ghora Gali is one of the most significant
  archaeological sites in India, with around two hundred unique stone sculptures
  of mounted horsemen, referred to as the Horsemen of the Pir Panjal,
  Kashmir's Lost Hun Riders, or simply the Petrified Wedding.</p>

  <p>The goals of this project are:</p>
  <ul class="goals">
    <li>To digitally preserve Ghora Gali and the folktales associated with it.</li>
    <li>To make this archive freely available online for scholars worldwide.</li>
    <li>To petition the Archaeological Survey of India and UNESCO to declare
    Ghora Gali a World Heritage Site.</li>
  </ul>
</div>

<!-- PHOTO GALLERY -->
<div class="section" id="gallery">
  <span class="section-tag">Photo Archive</span>
  <h2>All 12 Photographs — Ghora Gali</h2>
  <p>Click any photo to open full screen. Use arrow keys or buttons to
  navigate. Filter by category using the buttons below.</p>

  <div class="tabs">
    <button class="tab-btn active" onclick="filterGallery('all',this)">All Photos</button>
    <button class="tab-btn" onclick="filterGallery('bride',this)">The Bride</button>
    <button class="tab-btn" onclick="filterGallery('warrior',this)">Warriors</button>
    <button class="tab-btn" onclick="filterGallery('horse',this)">Horses</button>
    <button class="tab-btn" onclick="filterGallery('wedding',this)">Wedding Scene</button>
    <button class="tab-btn" onclick="filterGallery('weathered',this)">Weathered</button>
    <button class="tab-btn" onclick="filterGallery('fragment',this)">Fragments</button>
  </div>

  <div class="gallery" id="mainGallery">

    <div class="gallery-item" data-category="bride" data-caption="Close-up face of female figure — The Bride — Ghora Gali">
      <img src="photo1.jpg" alt="Close-up face of female figure">
      <div class="cap">Close-up face — The Bride</div>
      <div class="cat-badge">The Bride</div>
    </div>

    <div class="gallery-item" data-category="bride" data-caption="Full body of female figure with jewellery and headdress — The Bride — Ghora Gali">
      <img src="photo2.jpg" alt="Full body female figure">
      <div class="cap">Full body — The Bride</div>
      <div class="cat-badge">The Bride</div>
    </div>

    <div class="gallery-item" data-category="wedding" data-caption="Wedding scene — multiple figures on horseback — Ghora Gali">
      <img src="photo3.jpg" alt="Wedding scene overview">
      <div class="cap">Wedding procession scene — overview</div>
      <div class="cat-badge">Wedding Scene</div>
    </div>

    <div class="gallery-item" data-category="warrior" data-caption="Standing warrior with helmet and decorated armour — Ghora Gali">
      <img src="photo4.jpg" alt="Standing warrior figure">
      <div class="cap">Standing warrior — helmeted figure</div>
      <div class="cat-badge">Warrior</div>
    </div>

    <div class="gallery-item" data-category="weathered" data-caption="Faint weathered engravings — horseman barely visible — Ghora Gali">
      <img src="photo5.jpg" alt="Weathered engravings">
      <div class="cap">Weathered engravings — near erasure</div>
      <div class="cat-badge">Weathered</div>
    </div>

    <div class="gallery-item" data-category="horse" data-caption="Large horse sculpture with decorative spiral patterns — Ghora Gali">
      <img src="photo6.jpg" alt="Large horse sculpture">
      <div class="cap">Large horse — spiral decorative patterns</div>
      <div class="cat-badge">Horse</div>
    </div>

    <div class="gallery-item" data-category="horse" data-caption="Two riders mounted on horse — Horsemen of the Pir Panjal — Ghora Gali">
      <img src="photo7.jpg" alt="Two riders on horse">
      <div class="cap">Two riders on horseback</div>
      <div class="cat-badge">Horse</div>
    </div>

    <div class="gallery-item" data-category="wedding" data-caption="Wedding scene — close up of riders — same slab as photo 3 — Ghora Gali">
      <img src="photo8.jpg" alt="Wedding scene close up">
      <div class="cap">Wedding scene — rider close-up</div>
      <div class="cat-badge">Wedding Scene</div>
    </div>

    <div class="gallery-item" data-category="warrior" data-caption="Warrior figure with geometric body armour — Ghora Gali">
      <img src="photo9.jpg" alt="Warrior with geometric armour">
      <div class="cap">Warrior — geometric body armour</div>
      <div class="cat-badge">Warrior</div>
    </div>

    <div class="gallery-item" data-category="weathered" data-caption="Heavily weathered flat stone with faint carvings — Ghora Gali">
      <img src="photo10.jpg" alt="Heavily weathered stone">
      <div class="cap">Heavily weathered — faint carvings</div>
      <div class="cat-badge">Weathered</div>
    </div>

    <div class="gallery-item" data-category="fragment" data-caption="Broken fragment — decorative border and feet visible — Ghora Gali">
      <img src="photo11.jpg" alt="Broken stone fragment">
      <div class="cap">Fragment — decorative border</div>
      <div class="cat-badge">Fragment</div>
    </div>

    <div class="gallery-item" data-category="fragment" data-caption="Broken horizontal slab — partial carving — Ghora Gali">
      <img src="photo12.jpg" alt="Broken horizontal slab">
      <div class="cap">Fragment — horizontal slab</div>
      <div class="cat-badge">Fragment</div>
    </div>

  </div>
</div>

<!-- LIGHTBOX -->
<div class="lightbox" id="lightbox">
  <span class="lb-counter" id="lb-counter"></span>
  <button class="lb-close" onclick="closeLightbox()">×</button>
  <button class="lb-prev" onclick="changePhoto(-1)">‹</button>
  <button class="lb-next" onclick="changePhoto(1)">›</button>
  <img id="lb-img" src="" alt="">
  <p class="lb-caption" id="lb-caption"></p>
  <p class="lb-category" id="lb-category"></p>
</div>

<!-- MATCHED SCULPTURES -->
<div class="section" id="sculptures">
  <span class="section-tag">Sculpture Analysis</span>
  <h2>Matched Sculptures — Same Stone, Different Angles</h2>
  <p>These groupings show how multiple photographs document the same
  individual stone sculpture from different angles and distances.</p>

  <div class="pairs-grid">

    <div class="pair-card">
      <div class="pair-card-header">
        <div class="pair-card-title">Sculpture 1 — The Bride</div>
        <div class="pair-card-sub">Same sculpture · 2 angles · Female figure</div>
      </div>
      <div class="pair-images">
        <img src="photo1.jpg" alt="Bride face" onclick="openFromPair('photo1.jpg','Close-up face — The Bride','The Bride')">
        <img src="photo2.jpg" alt="Bride body" onclick="openFromPair('photo2.jpg','Full body — The Bride','The Bride')">
      </div>
      <div class="pair-desc">
        Photo 1 shows the face close-up with ornate headdress and carved
        features. Photo 2 shows the full body with necklace and jewellery.
        Same stone, same carving style — this is the bride figure of the
        Petrified Wedding.
      </div>
    </div>

    <div class="pair-card">
      <div class="pair-card-header">
        <div class="pair-card-title">Sculpture 2 — The Wedding Slab</div>
        <div class="pair-card-sub">Same slab · 2 angles · Group procession</div>
      </div>
      <div class="pair-images">
        <img src="photo3.jpg" alt="Wedding scene" onclick="openFromPair('photo3.jpg','Wedding scene — overview','Wedding Scene')">
        <img src="photo8.jpg" alt="Wedding close up" onclick="openFromPair('photo8.jpg','Wedding scene — rider close-up','Wedding Scene')">
      </div>
      <div class="pair-desc">
        Photo 3 shows the full slab from above with multiple figures.
        Photo 8 shows the same slab closer, focusing on the two central
        mounted riders. This is the most complete wedding procession scene.
      </div>
    </div>

    <div class="pair-card">
      <div class="pair-card-header">
        <div class="pair-card-title">Sculpture 3 — The Horse and Riders</div>
        <div class="pair-card-sub">Possibly same sculpture · 2 angles</div>
      </div>
      <div class="pair-images">
        <img src="photo6.jpg" alt="Horse" onclick="openFromPair('photo6.jpg','Large horse — spiral patterns','Horse')">
        <img src="photo7.jpg" alt="Riders" onclick="openFromPair('photo7.jpg','Two riders on horseback','Horse')">
      </div>
      <div class="pair-desc">
        Photo 6 shows the large horse body with spiral and geometric
        decoration. Photo 7 shows two riders which may belong to the same
        horse sculpture. The decorative style and stone color match closely.
      </div>
    </div>

    <div class="pair-card">
      <div class="pair-card-header">
        <div class="pair-card-title">Sculpture 4 — The Warriors</div>
        <div class="pair-card-sub">Two separate warrior figures</div>
      </div>
      <div class="pair-images">
        <img src="photo4.jpg" alt="Warrior 1" onclick="openFromPair('photo4.jpg','Standing warrior — helmeted','Warrior')">
        <img src="photo9.jpg" alt="Warrior 2" onclick="openFromPair('photo9.jpg','Warrior — geometric armour','Warrior')">
      </div>
      <div class="pair-desc">
        Photo 4 shows a standing helmeted warrior with decorated upper body.
        Photo 9 shows a different warrior with geometric body armour pattern.
        These appear to be two separate sculptures of similar type.
      </div>
    </div>

    <div class="pair-card">
      <div class="pair-card-header">
        <div class="pair-card-title">Sculpture 5 — Weathered Stones</div>
        <div class="pair-card-sub">Near erasure · Urgent preservation needed</div>
      </div>
      <div class="pair-images">
        <img src="photo5.jpg" alt="Weathered 1" onclick="openFromPair('photo5.jpg','Weathered engravings — near erasure','Weathered')">
        <img src="photo10.jpg" alt="Weathered 2" onclick="openFromPair('photo10.jpg','Heavily weathered — faint carvings','Weathered')">
      </div>
      <div class="pair-desc">
        These two stones show the most severe weathering damage. Carvings
        are barely visible. These documents the urgency of digital
        preservation before these sculptures are completely lost.
      </div>
    </div>

    <div class="pair-card">
      <div class="pair-card-header">
        <div class="pair-card-title">Sculpture 6 — Broken Fragments</div>
        <div class="pair-card-sub">Separated pieces · May belong together</div>
      </div>
      <div class="pair-images">
        <img src="photo11.jpg" alt="Fragment 1" onclick="openFromPair('photo11.jpg','Fragment — decorative border','Fragment')">
        <img src="photo12.jpg" alt="Fragment 2" onclick="openFromPair('photo12.jpg','Fragment — horizontal slab','Fragment')">
      </div>
      <div class="pair-desc">
        Two broken stone fragments lying on the ground. The decorative
        border style on photo 11 and the horizontal slab in photo 12
        may once have been part of a larger complete sculpture.
      </div>
    </div>

  </div>
</div>

<!-- METHODOLOGY -->
<div class="section" id="methodology">
  <span class="section-tag">Methodology</span>
  <h2>How This Project Works</h2>
  <p>Click each section to expand.</p>

  <div class="accordion-item">
    <div class="accordion-header" onclick="toggleAccordion(this)">
      A. Digital Archaeology and 3D Modeling
      <span class="accordion-arrow">▼</span>
    </div>
    <div class="accordion-body">
      I photographed, videographed, and geotagged stone sculptures at Ghora
      Gali during my field visit. My ambition is to use these high-definition
      2D photographs to create 3D models of each sculpture type using SAM 3D
      or Copilot 3D. These models will be available in open formats enabling
      reuse across platforms and long-term preservation.
    </div>
  </div>

  <div class="accordion-item">
    <div class="accordion-header" onclick="toggleAccordion(this)">
      B. Static Digital Publishing
      <span class="accordion-arrow">▼</span>
    </div>
    <div class="accordion-body">
      This project is published as a static website hosted on GitHub Pages.
      Static websites are lightweight, stable, and sustainable. The website
      displays 2D photographs organized by sculpture category, with metadata
      and contextual information for each documented sculpture.
    </div>
  </div>

  <div class="accordion-item">
    <div class="accordion-header" onclick="toggleAccordion(this)">
      C. Structured Metadata
      <span class="accordion-arrow">▼</span>
    </div>
    <div class="accordion-body">
      Each documented sculpture is accompanied by structured metadata
      including a unique identifier, material and condition notes,
      iconographic description, stylistic and comparative notes such as
      Central Asian or Indo-Greek parallels, and sculpture category.
    </div>
  </div>

  <div class="accordion-item">
    <div class="accordion-header" onclick="toggleAccordion(this)">
      D. Critical Scholarly Paper
      <span class="accordion-arrow">▼</span>
    </div>
    <div class="accordion-body">
      Alongside technical documentation, the project will lead to a scholarly
      paper addressing the politics of archaeological neglect in Kashmir,
      bureaucratic regimes of preservation and abandonment, and digital
      heritage as counter-infrastructure.
    </div>
  </div>
</div>

<!-- LOCATION -->
<div class="section" id="location">
  <span class="section-tag">Location</span>
  <h2>Gool, Ramban District, Jammu and Kashmir</h2>
  <p>Ghora Gali is situated in the Pir Panjal range, in the Gool area of
  Ramban district, Indian administered Jammu and Kashmir — one of the most
  militarized and least accessible zones on earth.</p>
  <div class="map-container">
    <iframe
      src="https://www.openstreetmap.org/export/embed.html?bbox=74.5,33.0,75.5,33.8&amp;layer=mapnik&amp;marker=33.35,75.05"
      title="Map of Ghora Gali">
    </iframe>
    <div class="map-title">Ramban District · Jammu and Kashmir · India</div>
  </div>
</div>

<!-- TIMELINE -->
<div class="section" id="timeline">
  <span class="section-tag">Project Timeline</span>
  <h2>Phases of the Work</h2>
  <ul class="timeline">
    <li>
      <span class="tl-date">March 2026</span>
      <div class="tl-desc">Three-week field visit to Ghora Gali. High-definition
      photography of stone sculptures. GPS geotagging and database creation.</div>
    </li>
    <li>
      <span class="tl-date">June 2026</span>
      <div class="tl-desc">Tagging, categorization, and metadata creation.
      Generation of 3D models using SAM 3D.</div>
    </li>
    <li>
      <span class="tl-date">July 2026</span>
      <div class="tl-desc">Building and hosting the full archive website on
      GitHub Pages with embedded 3D models.</div>
    </li>
    <li>
      <span class="tl-date">August 2026</span>
      <div class="tl-desc">Scholarly paper submitted to South Asian and global
      academic conferences on digital heritage.</div>
    </li>
    <li>
      <span class="tl-date">September 2026 and beyond</span>
      <div class="tl-desc">Formal petition to the Archaeological Survey of India
      and UNESCO to declare Ghora Gali a World Heritage Site.</div>
    </li>
  </ul>
</div>

<!-- BIBLIOGRAPHY -->
<div class="section" id="bibliography">
  <span class="section-tag">Bibliography</span>
  <h2>Sources</h2>
  <ul class="bib">
    <li>Ingold, Tim. <em>Being Alive: Essays on Movement, Knowledge and Description.</em> London: Routledge, 2012.</li>
    <li>Live History India. "Mysterious Horsemen of Jammu and Kashmir." <em>Google Arts and Culture.</em> <a href="https://artsandculture.google.com/story/mysterious-horsemen-of-jammu-kashmir-live-history-india/GwVBxGLFdRSDLg" target="_blank">artsandculture.google.com</a></li>
    <li>Mathawan, Prashant. "Who Left These Ancient Sculptures of Horsemen around the Pir Panjal Range?" <em>Scroll.in,</em> April 6, 2018. <a href="https://scroll.in/magazine/872541/who-left-these-mysterious-sculptures-of-horsemen-around-the-pir-panjal-range" target="_blank">scroll.in</a></li>
    <li>Mignolo, Walter D. <em>The Darker Side of Western Modernity.</em> Durham, NC: Duke University Press, 2011.</li>
    <li>Mignolo, Walter D. <em>Local Histories/Global Designs.</em> Princeton, NJ: Princeton University Press, 2000.</li>
    <li>Mignolo, Walter D., and Catherine E. Walsh. <em>On Decoloniality.</em> Durham, NC: Duke University Press, 2018.</li>
    <li>Taylor, Diana. <em>The Archive and the Repertoire.</em> Durham, NC: Duke University Press, 2003.</li>
    <li>The Statesman. "Ancient Rock-Carved Warriors of Gool Losing Battle Against Time." December 1, 2025. <a href="https://asianews.network/ancient-rock-carved-warriors-of-gool-in-indian-administered-jammu-losing-battle-against-time/" target="_blank">asianews.network</a></li>
    <li>Trouillot, Michel-Rolph. <em>Silencing the Past.</em> Boston: Beacon Press, 1995.</li>
    <li>Smith, Laurajane. <em>Uses of Heritage.</em> London: Routledge, 2006.</li>
    <li>Stoler, Ann Laura. <em>Along the Archival Grain.</em> Princeton, NJ: Princeton University Press, 2008.</li>
  </ul>
</div>

<footer>
  2026 · Ashfaq Ahmed · Ghora Gali Digital Preservation Project
</footer>

<script>

/* BACK TO TOP */
window.onscroll = function() {
  var btn = document.getElementById('backToTop');
  if (document.body.scrollTop > 400 || document.documentElement.scrollTop > 400) {
    btn.style.display = 'block';
  } else {
    btn.style.display = 'none';
  }
};

/* GALLERY */
var currentPhoto = 0;
var visibleItems = [];

function buildGallery() {
  visibleItems = [];
  var items = document.querySelectorAll('#mainGallery .gallery-item');
  for (var i = 0; i < items.length; i++) {
    if (items[i].style.display !== 'none') {
      visibleItems.push(items[i]);
      items[i].onclick = makeHandler(i);
    }
  }
}

function makeHandler(index) {
  return function() {
    var realIndex = visibleItems.indexOf(this);
    if (realIndex === -1) return;
    currentPhoto = realIndex;
    var img = this.querySelector('img');
    var cap = this.getAttribute('data-caption');
    var cat = this.getAttribute('data-category');
    openLightbox(img.src, cap, cat);
  };
}

function openLightbox(src, caption, category) {
  document.getElementById('lb-img').src = src;
  document.getElementById('lb-caption').textContent = caption;
  document.getElementById('lb-category').textContent = category ? category.toUpperCase() : '';
  document.getElementById('lb-counter').textContent = (currentPhoto + 1) + ' / ' + visibleItems.length;
  document.getElementById('lightbox').className = 'lightbox show';
  document.body.style.overflow = 'hidden';
}

function openFromPair(src, caption, category) {
  document.getElementById('lb-img').src = src;
  document.getElementById('lb-caption').textContent = caption;
  document.getElementById('lb-category').textContent = category.toUpperCase();
  document.getElementById('lb-counter').textContent = '';
  document.getElementById('lightbox').className = 'lightbox show';
  document.body.style.overflow = 'hidden';
}

function closeLightbox() {
  document.getElementById('lightbox').className = 'lightbox';
  document.body.style.overflow = '';
}

function changePhoto(dir) {
  if (visibleItems.length === 0) return;
  currentPhoto = (currentPhoto + dir + visibleItems.length) % visibleItems.length;
  var item = visibleItems[currentPhoto];
  var img = item.querySelector('img');
  document.getElementById('lb-img').src = img.src;
  document.getElementById('lb-caption').textContent = item.getAttribute('data-caption');
  document.getElementById('lb-category').textContent = item.getAttribute('data-category').toUpperCase();
  document.getElementById('lb-counter').textContent = (currentPhoto + 1) + ' / ' + visibleItems.length;
}

document.addEventListener('keydown', function(e) {
  if (e.key === 'Escape') closeLightbox();
  if (e.key === 'ArrowLeft') changePhoto(-1);
  if (e.key === 'ArrowRight') changePhoto(1);
});

/* FILTER */
function filterGallery(category, btn) {
  var items = document.querySelectorAll('#mainGallery .gallery-item');
  for (var i = 0; i < items.length; i++) {
    if (category === 'all' || items[i].getAttribute('data-category') === category) {
      items[i].style.display = 'block';
    } else {
      items[i].style.display = 'none';
    }
  }
  var btns = document.querySelectorAll('.tab-btn');
  for (var j = 0; j < btns.length; j++) {
    btns[j].className = 'tab-btn';
  }
  btn.className = 'tab-btn active';
  buildGallery();
}

/* ACCORDION */
function toggleAccordion(header) {
  var body = header.nextElementSibling;
  if (body.className === 'accordion-body open') {
    body.className = 'accordion-body';
    header.className = 'accordion-header';
  } else {
    body.className = 'accordion-body open';
    header.className = 'accordion-header open';
  }
}

buildGallery();

</script>
</body>
</html>
