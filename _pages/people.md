---
permalink: /people/
title: "People"
description: "Networked Control System lab member biographies"
keywords: "Takashi Tanaka, Kaoru Teranishi, Jihoon Suh, Moses Hansen, Dongheon Lee, Apurva Patil, Ronald Ogden, Rylie Anderson"
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
    font-size: 1.1em;
    font-weight: bold;
    background-color: #f8f8f8;
    padding: 15px;
    border-radius: 10px;
    margin-bottom: 15px;
}

.principal-investigator img {
    width: 160px;
    height: auto;
    border-radius: 10px;
    margin-right: 15px;
}

.postdocs-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(180px, 1fr));
    gap: 15px;
    text-align: center;
}

.postdocs-grid .person-box img {
    width: 140px;
    height: auto;
    border: 2px solid #f0f0f0;
    border-radius: 10px;
}

.postdocs-grid .person-box {
    font-size: 1em;
    padding: 10px;
}

.graduate-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 15px;
    background: none;
    padding: 0;
}

.undergrad-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 15px;
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
    width: 120px;
    height: auto;
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

.alumni ul {
    list-style-type: disc;
    padding-left: 20px;
    margin: 10px 0;
}

.alumni li {
    margin-bottom: 5px;
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
    <strong>Dr. Takashi Tanaka</strong><br><br>
    Takashi Tanaka is an Associate Professor at the School of Aeronautics and Astronautics and the Elmore Family School of Electrical and Computer Engineering at Purdue University.
He received his B.S. from the University of Tokyo and his M.S. and Ph.D. degrees in aerospace engineering from the University of Illinois at Urbana-Champaign.  Dr. Tanaka was a Postdoctoral Associate with the Laboratory for Information and Decision Systems at the Massachusetts Institute of Technology from 2012 to 2015, and a postdoctoral researcher at KTH Royal Institute of Technology from 2015 to 2017. He was an Assistant Professor in the Department of Aerospace Engineering and Engineering Mechanics at the University of Texas at Austin between 2017 and 2024, where he was an Associate Professor in 2024. Dr. Tanaka's research interests include control theory and its applications, most recently the information-theoretic perspectives of optimal control problems. He received the DARPA Young Faculty Award, the AFOSR Young Investigator Program Award, and the NSF Career Award.
  </p>
</div>

---

## Postdoctoral Researchers
<div class="postdocs-grid">
  <div class="person-box">
    <img src="/images/profile_zoom-1-240x300.png" alt="profile image">
    <p>
      <strong>Kaoru Teranishi</strong><br><br>
      <span id="short-kaoru">Dr. Teranishi is a JSPS Overseas Research Fellow...</span>
      <span id="full-kaoru" class="full-bio">
        of the Japan Society for the Promotion of Science and a visiting scholar at the School of Aeronautics and Astronautics at Purdue University. He received his Ph.D. in mechanical and intelligent systems engineering from the University of Electro-Communications, Tokyo, Japan, in 2024. <a href="https://kaoruteranishi.xyz/">Website</a>
      </span>
      <span id="btn-kaoru" class="read-more" onclick="toggleBio('kaoru')">Expand More</span>
    </p>
  </div>
</div>

---

## Graduate Students
<div class="graduate-grid">

  <div class="person-box">
    <img src="/images/jihoon.jpeg" alt="profile image">
    <p>
      <strong>Jihoon Suh</strong><br><br>
      <span id="short-jihoon">PhD student in AAE at Purdue...</span>
      <span id="full-jihoon" class="full-bio">
        My current research is on encrypted control, where the objective is to protect the privacy of sensitive data such as personal, financial, or strategically valuable information while they are being processed by a control system. I served in the US Army for 6 years. <a href="https://jsuh9.github.io/">Website</a>
      </span>
      <span id="btn-jihoon" class="read-more" onclick="toggleBio('jihoon')">Expand More</span>
    </p>
  </div>

  <div class="person-box">
    <img src="/images/ronnie.jpg" alt="profile image">
    <p>
      <strong>Ronald Ogden</strong><br><br>
      <span id="short-ronnie">PhD student in Aerospace Engineering at UT Austin...</span>
      <span id="full-ronnie" class="full-bio">
        My research interests include event-based estimation and stochastic control. Prior to coming to UT, I was a flight test engineer at Wisk Aero, where I tested autonomous eVTOL aircraft. In my free time, I enjoy climbing, language learning, and puzzle solving.
      </span>
      <span id="btn-ronnie" class="read-more" onclick="toggleBio('ronnie')">Expand More</span>
    </p>
  </div>

  <div class="person-box">
    <img src="/images/moses.jpg" alt="profile image">
    <p>
      <strong>Moses Hansen</strong><br><br>
      <span id="short-moses">PhD student in AAE at Purdue...</span>
      <span id="full-moses" class="full-bio">
        Moses is a PhD student in the School of Aeronautics and Astronautics at Purdue University. He earned his Bachelor’s degree in Mathematics from Brigham Young University in 2024, where he applied deep learning methods on the computer vision team in the Record Linking Lab. He also worked with the Air Force Research Laboratory, developing deep reinforcement learning techniques for competitive, high-stakes multi-agent satellite control scenarios. His current research combines information theory with classical control to design autonomous systems capable of deception-resistant path planning in competitive, multi-agent environments. In his free time, he enjoys cooking, lifting weights, and spending time outdoors.
      </span>
      <span id="btn-moses" class="read-more" onclick="toggleBio('moses')">Expand More</span>
    </p>
  </div>

  <div class="person-box">
    <img src="/images/sashank.jpg" alt="profile image">
    <p>
      <strong>Sashank Modali</strong><br><br>
      <span id="short-sashank">PhD student in AAE at Purdue...</span>
      <span id="full-sashank" class="full-bio">
        My research interests lie at the intersection of robotics, multi-agent systems, and stochastic control. Prior to joining Purdue, I completed my Bachelor's degree in Aerospace Engineering from IIT Madras, India. In my spare time, I enjoy playing squash and traveling.
      </span>
      <span id="btn-sashank" class="read-more" onclick="toggleBio('sashank')">Expand More</span>
    </p>
  </div>

  <div class="person-box">
    <img src="/images/dongheon.jpeg" alt="profile image">
    <p>
      <strong>Dongheon Lee</strong><br><br>
      <span id="short-dongheon">MS student in ECE at Purdue...</span>
      <span id="full-dongheon" class="full-bio">
        My research interests include task allocation and path planning for multi-agent systems. Prior to coming to Purdue, I worked as a software engineer at EpiSci and Applied Intuition, where I developed autonomous small UAV applications. In my free time, I enjoy playing soccer, running, and watching movies.
      </span>
      <span id="btn-dongheon" class="read-more" onclick="toggleBio('dongheon')">Expand More</span>
    </p>
  </div>

  <div class="person-box">
    <img src="/images/rylie.png" alt="profile image">
    <p>
      <strong>Rylie Anderson</strong><br><br>
      <span id="short-rylie">MS student in ECE at Purdue...</span>
      <span id="full-rylie" class="full-bio">
        My research interests are in control theory and aerospace. Prior to joining Purdue, I completed my Bachelor's in Computer Science at the US Air Force Academy. Outside of research and classes, I enjoy running, reading, and jiu-jitsu.
      </span>
      <span id="btn-rylie" class="read-more" onclick="toggleBio('rylie')">Expand More</span>
    </p>
  </div>

  <div class="person-box">
    <img src="/images/owen.PNG" alt="profile image">
    <p>
      <strong>Owen Bishop</strong><br><br>
      <span id="short-owen">MS student in AAE at Purdue...</span>
      <span id="full-owen" class="full-bio">
        My research interests are primarily focused on event-based sensing and transmission, with applications to control systems. I completed my Bachelor’s in Electrical Engineering from Purdue University. In my free time, I enjoy reading science-fiction and fantasy books, and playing board games.
      </span>
      <span id="btn-owen" class="read-more" onclick="toggleBio('owen')">Expand More</span>
    </p>
  </div>

</div>

---

## Undergraduate Students

<div class="undergrad-grid">
  <div class="person-box">
    <img src="/images/meg.png" alt="profile image">
    <p>
      <strong>Meg Kumar</strong><br><br>
      <span id="short-meg">Student in AAE at Purdue...</span>
      <span id="full-meg" class="full-bio">
        My name is Meg Kumar and I am a junior study aerospace engineering. In this lab, I am focusing on working with the pencil balancing project, specifically the mechanic side. I enjoy working with the physical system of the invented pendulum project, so I am developing robotic arms to assist with the balancing aspect. Another part of the project I am working on is the image processing with event cameras, to provide information to the system.
      </span>
      <span id="btn-meg" class="read-more" onclick="toggleBio('meg')">Expand More</span>
    </p>
  </div>

  <div class="person-box">
    <img src="/images/lucca.jpg" alt="profile image">
    <p>
      <strong>Lucca Mo</strong><br><br>
      <span id="short-lucca">Student in AAE at Purdue...</span>
      <span id="full-lucca" class="full-bio">
        I am studying the dynamics of a falling pencil as a model for an unstable control system. I am deriving the equations of motion and converting them into a state–space representation (A,B,C,D) to analyze stability, while also building MATLAB simulations to visualize how the pencil behaves over time, including plots of its angle response. I am preparing a poster for the Fall Undergraduate Research Conference to present the modeling and simulation results. In addition, I am contributing to the experimental side by helping with the setup and testing of the pencil-balancing apparatus, documenting my work with notes and photos.
      </span>
      <span id="btn-lucca" class="read-more" onclick="toggleBio('lucca')">Expand More</span>
    </p>
  </div>

  <div class="person-box">
    <img src="/images/ishaan.png" alt="profile image">
    <p>
      <strong>Ishaan Agrawal</strong><br><br>
      <span id="short-ishaan">Student in AAE at Purdue...</span>
      <span id="full-ishaan" class="full-bio">
        My research interests include optimal control for aerospace and autonomous systems; recently, I'm interested in how model predictive control can be adapted for security. I like soccer and astrophotography.
      </span>
      <span id="btn-ishaan" class="read-more" onclick="toggleBio('ishaan')">Expand More</span>
    </p>
  </div>

  <div class="person-box">
    <img src="/images/atharva.jpg" alt="profile image">
    <p>
      <strong>Atharva Awasthi</strong><br><br>
      <span id="short-atharva">Student in AAE at Purdue...</span>
      <span id="full-atharva" class="full-bio">
        My research interests include optimal control methods for trajectory and path planning, estimation, astrodynamics, and competitive systems. In my free time, I enjoy cooking, dancing, and playing board games.
      </span>
      <span id="btn-atharva" class="read-more" onclick="toggleBio('atharva')">Expand More</span>
    </p>
  </div>

  <div class="person-box">
    <img src="/images/austin.jpg" alt="profile image">
    <p>
      <strong>Austin Lika</strong><br><br>
      <span id="short-austin">Student in AAE at Purdue...</span>
      <span id="full-austin" class="full-bio">
        My research interests include optimal control methods for trajectory and path planning, estimation, astrodynamics, and competitive systems. In my free time, I enjoy cooking, dancing, and playing board games.
      </span>
      <span id="btn-austin" class="read-more" onclick="toggleBio('austin')">Expand More</span>
    </p>
  </div>
</div>

---

## Alumni
<div class="alumni">
  <ul>
    <li>Vrushabh Zinage (Graduated from UT Austin with PhD in 2025, currently at CalTech)</li>
    <li>Apurva Patil (Graduated from UT Austin with PhD in 2025, currently at Tensor Auto)</li>
    <li>Michael Hibbard (Graduated from UT Austin with PhD in 2024, currently at Starfish Space)</li>
    <li>Hyunho Jung (Graduated from UT Austin with PhD in 2024, currently at the Republic of Korea Air Force)</li>
    <li>Travis Cuvelier (Graduated from UT Austin with PhD in 2024, currently at MITRE Corporation)</li>
    <li>Ali Reza Pedram (Graduated from UT Austin  with PhD in 2023, currently at Georgia Tech)</li>
    <li>Binghan He (Postdoc researcher at UT Austin until 2022, currently Assistant Professor at The University of Texas at San Antonio</li>
    <li>Riku Funada (Postdoc researcher at UT Austin until 2020, currently Assistant Professor at Tokyo Institute of Technology)</li>
    <li>Jeb Stefan (Graduated from UT Austin with M.S. in 2019, currently at Odyssey Space Research)</li>
  </ul>
</div>
