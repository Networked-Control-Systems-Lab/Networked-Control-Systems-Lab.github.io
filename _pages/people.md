---
permalink: /people/
title: "People"
description: ""
author_profile: false
redirect_from: 
  - /people.html
---

<style>
.grid-container {
    display: grid;
    gap: 20px;
    justify-content: center;
}

.principal-investigator {
    display: flex;
    align-items: center;
    font-size: 1.2em;
    font-weight: bold;
    background-color: #f8f8f8;
    padding: 20px;
    border-radius: 10px;
    margin-bottom: 20px;
}

.principal-investigator img {
    width: 200px;
    height: auto;
    border-radius: 10px;
    margin-right: 20px;
}

.postdocs-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(200px, 1fr));
    gap: 20px;
    text-align: center;
}

.graduate-grid {
    display: grid;
    grid-template-columns: repeat(4, minmax(200px, 1fr)); 
    gap: 20px; 
    background: none; 
    padding: 0;
}

.person-box {
    background: none; 
    padding: 0; 
    text-align: center;
    border-radius: 0;
}

.person-box img {
    border: 2px solid #f0f0f0; 
    border-radius: 10px;
}
  
.read-more {
    color: blue;
    cursor: pointer;
    font-size: 0.9em;
    display: block;
    margin-top: 5px;
}

.full-bio {
    display: none;
    font-size: 0.9em;
}
</style>

<script>
function toggleBio(id) {
    var shortBio = document.getElementById("short-" + id);
    var fullBio = document.getElementById("full-" + id);
    var button = document.getElementById("btn-" + id);

    if (fullBio.style.display === "none") {
        fullBio.style.display = "block";
        shortBio.style.display = "none";
        button.innerText = "Show Less";
    } else {
        fullBio.style.display = "none";
        shortBio.style.display = "inline";
        button.innerText = "Expand More";
    }
}
</script>

## Principal Investigator
<div class="principal-investigator">
  <img src="/images/tanaka-199x300.jpg" alt="profile image">
  <p>
    <strong>Dr. Takashi Tanaka</strong><br>
    <span id="short-tanaka">Dr. Tanaka joined the department as an Assistant Professor in 2017...</span>
    <span id="full-tanaka" class="full-bio">
      Before moving to UT, he held a postdoctoral researcher position at KTH Royal Institute of Technology, Sweden. From 2012 to 2015, he was a postdoctoral associate at MIT, USA. Dr. Tanaka received his M.S. and Ph.D. degrees in Aerospace Engineering from UIUC, USA, in 2009 and 2012, respectively. Prior to his graduate studies, he received his B.S. degree in Aerospace Engineering from the University of Tokyo, Japan. Dr. Tanaka is a recipient of the IEEE CDC best student paper award in 2011.
    </span>
    <span id="btn-tanaka" class="read-more" onclick="toggleBio('tanaka')">Expand More</span>
  </p>
</div>

---

## Postdoctoral Researchers
<div class="postdocs-grid">
  <div class="person-box">
    <img src="/images/profile_zoom-1-240x300.png" alt="profile image">
    <p>
      <strong>Kaoru Teranishi</strong><br>
      <span id="short-kaoru">Dr. Teranishi is a JSPS Overseas Research Fellow...</span>
      <span id="full-kaoru" class="full-bio">
        of the Japan Society for the Promotion of Science and a Research Affiliate Postdoctoral in the Oden Institute for Computational Engineering and Sciences at UT Austin. He received his Ph.D. in mechanical and intelligent systems engineering from the University of Electro-Communications, Tokyo, Japan, in 2024. <a href="https://kaoruteranishi.xyz/">Website</a>
      </span>
      <span id="btn-kaoru" class="read-more" onclick="toggleBio('kaoru')">Expand More</span>
    </p>
  </div>

    <!-- can add more postdocs below using the same format -->
</div>

---

## Graduate Students
<div class="graduate-grid">

  <div class="person-box">
    <img src="/images/apurva.jpg" alt="profile image">
    <p><strong>Apurva Patil</strong><br>
      <span id="short-apurva">PhD student in Mechanical Engineering...</span>
      <span id="full-apurva" class="full-bio">
        My research interests lie in robotics, path-planning, and perception. I completed my bachelor's from College of Engineering Pune in India. In my free time, I enjoy swimming and listening to music. <a href="https://patil-apurva.github.io/portfolio/">Website</a>
      </span>
      <span id="btn-apurva" class="read-more" onclick="toggleBio('apurva')">Expand More</span>
    </p>
  </div>

  <div class="person-box">
    <img src="/images/ronnie.jpg" alt="profile image">
    <p><strong>Ronald Ogden</strong><br>
      <span id="short-ronnie">PhD student in Aerospace Engineering...</span>
      <span id="full-ronnie" class="full-bio">
        My research interests include event-based estimation and stochastic control. Prior to coming to UT, I was a flight test engineer at Wisk Aero, where I tested autonomous eVTOL aircraft. In my free time, I enjoy climbing, language learning, and puzzle solving.
      </span>
      <span id="btn-ronnie" class="read-more" onclick="toggleBio('ronnie')">Expand More</span>
    </p>
  </div>

  <div class="person-box">
    <img src="/images/vrushab.jpg" alt="profile image">
    <p><strong>Vrushabh Zinage</strong><br>
      <span id="short-vrushab">Graduate student in Aerospace Engineering...</span>
      <span id="full-vrushab" class="full-bio">
        My research interests lie in the intersection of robotics, motion planning, and control theory. Prior to joining UT, I completed my Bachelor's in Aerospace Engineering from IIT Madras in India. In my free time, I enjoy watching cricket, listening to music, stargazing, and watching movies.
      </span>
      <span id="btn-vrushab" class="read-more" onclick="toggleBio('vrushab')">Expand More</span>
    </p>
  </div>

  <div class="person-box">
    <img src="/images/jihoon.jpeg" alt="profile image">
  <p><strong>Jihoon Suh</strong><br>
    <span id="short-jihoon">Graduate student in Aerospace Engineering...</span>
    <span id="full-jihoon" class="full-bio">
      I am a PhD student in the Department of Aerospace Engineering at the University of Texas at Austin. My current research is on encrypted control, where the objective is to protect the privacy of sensitive data such as personal, financial, or strategically valuable information while they are being processed by a control system. I completed my Bachelor's at UT Austin, and I served in the US Army for 6 years as a member of MAVNI. In my free time, I enjoy playing Tennis, camping, and stargazing. <a href="https://jsuh9.github.io/">Website</a>
    </span>
    <span id="btn-jihoon" class="read-more" onclick="toggleBio('jihoon')">Expand More</span>
  </p>

  <div class="person-box">
    <img src="/images/moses.jpg" alt="profile image">
    <p><strong>Moses Hansen</strong><br>
      <span id="short-moses">PhD student in Aerospace Engineering...</span>
      <span id="full-moses" class="full-bio">
        My research interests include leveraging deep reinforcement learning methods as well as classical control theory to optimize decision-making in competitive, multi-agent scenarios. In my spare time, I enjoy hiking, being outdoors, and cooking.
      </span>
      <span id="btn-moses" class="read-more" onclick="toggleBio('moses')">Expand More</span>
    </p>
  </div>
    <!-- can add more postdocs below using the same format -->
</div>

## Alumni
<div class="alumni">
  <ul>
    <li>Michael Hibbard (Graduated with PhD in 2024, currently at Starfish Space)</li>
    <li>Hyunho Jung (Graduated with PhD in 2024, currently at the Republic of Korea Air Force (ROKAF))</li>
    <li>Ali Reza Pedram (Graduated with PhD in 2023, currently at Georgia Tech)</li>
    <li>Binghan He (Postdoc researcher until 2022, currently at UC Berkeley)</li>
    <li>Riku Funada (Postdoc researcher until 2020, currently at Tokyo Institute of Technology)</li>
    <li>Jeb Stefan (Graduated with M.S. in 2019, currently at Odyssey Space Research)</li>
  </ul>
</div>
