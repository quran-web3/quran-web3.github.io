---
layout: default
title: "Sneak Peek: Exploring Features on Our Temporary Vercel Deployment"
date: 2026-07-28
author: "Zamil"
category: "updates"
image: "images/blog-big.png"
---
<p class="dk pk ac">
  <span class="sj _j gk kk wm" style="float: left; font-size: 50px; line-height: 40px; padding-right: 10px; margin-top: 4px;">A</span>s we prepare for our ultimate goal of a fully decentralized launch on IPFS, the Quran-Web3.NFT project is currently hosted temporarily on Vercel. This testing phase is crucial for us to iron out bugs, improve user experience, and ensure everything runs smoothly. Let's dive into the core features you can try out right now!
</p>
<h2 class="sj ck fk kk wm ac">Intuitive Navigation & View Modes</h2>
<p class="dk pk ac">
  We want to ensure that accessing the Quran is as seamless as possible. The application features a straightforward tabbed navigation system that lets you jump exactly where you need to be.
</p>
<ul class="tc sf cg ac dk pk">
  <li>
    <div class="tc">
      <span class="mk ub gk bf">•</span>
      <p>Seamless navigation via <strong class="gk kk wm">"Surah"</strong>, <strong class="gk kk wm">"Verse"</strong>, <strong class="gk kk wm">"Juz"</strong>, and <strong class="gk kk wm">"Page"</strong> tabs.</p>
    </div>
  </li>
  <li>
    <div class="tc">
      <span class="mk ub gk bf">•</span>
      <p>Two primary reading modes tailored to your preference: <strong class="gk kk wm">Surah Mode</strong> and <strong class="gk kk wm">Page Mode</strong>.</p>
    </div>
  </li>
</ul>
<h2 class="sj ck fk kk wm ac">Deep Dive into "Page" Mode</h2>
<p class="dk pk ac">
  In "Page" mode, the layout is designed for deep study and reflection, presenting the Quran verse by verse. We have packed this mode with powerful tools for everyday readers and students of knowledge alike.
</p>
<ol class="tc sf cg ac dk pk">
  <li>
    <div class="tc">
      <span class="kk wm fk ub bf">1.</span>
      <p><strong class="gk kk wm">Audio & Qaris:</strong> Play audio for specific verses with a selection of 6 renowned Qaris (including Abdul Rahman Al-Sudais, Abu Bakr Al-Shatri, Fares Abbad, Maher Al-Muaiqly, Saad Al-Ghamdi, and Saud Al-Shuraim).</p>
    </div>
  </li>
  <li>
    <div class="tc">
      <span class="kk wm fk ub bf">2.</span>
      <p><strong class="gk kk wm">Study Tools:</strong> Access in-depth Tafsir (Ibn Kathir), bookmark verses for later, write personal notes, and easily copy or share verses with your community.</p>
    </div>
  </li>
  <li>
    <div class="tc">
      <span class="kk wm fk ub bf">3.</span>
      <p><strong class="gk kk wm">Customizable Display:</strong> Toggle transliteration on or off, switch between color-coded Tajweed and standard text, and easily zoom in or out to adjust the Arabic text size.</p>
    </div>
  </li>
  <li>
    <div class="tc">
      <span class="kk wm fk ub bf">4.</span>
      <p><strong class="gk kk wm">Global Translations:</strong> Read the meaning of the Quran in 12 different languages including English, Chinese, Hindi, Spanish, French, Portuguese, Indonesian, German, Japanese, Bengali, Russian, and Korean.</p>
    </div>
  </li>
</ol>
<h2 class="sj ck fk kk wm ac">"Surah" Mode & The Verse Repeater</h2>
<p class="dk pk ac">
  For those focusing on memorization (Hifz), our "Surah" mode includes a highly requested <strong class="gk kk wm">Verse Repeater</strong> feature. You can select a starting verse, an ending verse, and how many times you want the audio to loop.
</p>
<p class="dk pk ac">
  As a quick dev log update, here is a snippet of the HTML structure we used to build the Verse Repeater modal for Surah Al-Baqarah:
</p>
<h2 class="sj ck fk kk wm ac">Transparency: Our Data Sources</h2>
<p class="dk pk ac">
  In the spirit of Web3, transparency regarding where our data comes from is an absolute priority. We utilize verified and trusted sources for our Arabic texts, Tafsir, audio, and translations.
</p>
<div x-data="{ open: false }" markdown="0" class="hh rm _g ch pm sg ci ic" style="padding: 15px 20px;">
  <button @click="open = !open" class="vd tc un wf ph ab sj wj fk kk wm">
    <span>Click Here to View All Data Sources & Translations</span>
    <span x-text="open ? '−' : '+'" class="ck"></span>
  </button>
  <div x-show="open" x-transition class="lc bh ch pm dk pk" style="margin-top: 15px; padding-top: 15px;">
    <p><strong class="gk kk wm">Quran Text & Tafsir:</strong></p>
    <ul class="tc sf cg ac dk pk">
      <li><div class="tc"><span class="mk ub gk bf">•</span><p>Uthmanic Hafs (Arabic): Tanzil Quran Text</p></div></li>
      <li><div class="tc"><span class="mk ub gk bf">•</span><p>Indopak Naskh (Tajweed): Tarteel AI</p></div></li>
      <li><div class="tc"><span class="mk ub gk bf">•</span><p>Tafsir Ibn Kathir: <a href="https://github.com/spa5k/tafsir_api" target="_blank" style="color: #4E6BFF; text-decoration: none;">github.com/spa5k/tafsir_api</a></p></div></li>
      <li><div class="tc"><span class="mk ub gk bf">•</span><p>Surah Info (A. Maududi): quran.com</p></div></li>
    </ul>
    <p style="margin-top: 15px;"><strong class="gk kk wm">Audio Recitations (everyayah.com):</strong></p>
    <ul class="tc sf cg ac dk pk">
      <li><div class="tc"><span class="mk ub gk bf">•</span><p>Abdul Rahman Al-Sudais, Abu Bakr Al-Shatri, Fares Abbad, Maher Al-Muaiqly, Saad Al-Ghamdi, Saud Al-Shuraim</p></div></li>
    </ul>
    <p style="margin-top: 15px;"><strong class="gk kk wm">Translations (Sourced from QuranEnc.com & Tanzil.net):</strong></p>
    <p class="ak pk qk">Note: Translations marked with an asterisk (*) contain footnotes.</p>
    <ul class="tc sf cg ac dk pk">
      <li><div class="tc"><span class="mk ub gk bf">•</span><p>English: Rowwad Translation Center*, Hilali & Khan*, Saheeh International*</p></div></li>
      <li><div class="tc"><span class="mk ub gk bf">•</span><p>Indonesian: Indonesian Sabiq*, Ministry of Religious Affairs*, The Complex*</p></div></li>
      <li><div class="tc"><span class="mk ub gk bf">•</span><p>Spanish: Garcia, Spanish Montada eu*, Isa Garcia*, Spanish Montada Latin*</p></div></li>
      <li><div class="tc"><span class="mk ub gk bf">•</span><p>French: Hamidullah, French Montada*, Rachid Maach*</p></div></li>
      <li><div class="tc"><span class="mk ub gk bf">•</span><p>Chinese: Ma Jian (Traditional), Chinese Makin, Chinese Suliman</p></div></li>
      <li><div class="tc"><span class="mk ub gk bf">•</span><p>Hindi: Farooq Khan & Nadwi, Hindi Omari*</p></div></li>
      <li><div class="tc"><span class="mk ub gk bf">•</span><p>Portuguese: Helmi Nasr, El-Hayek</p></div></li>
      <li><div class="tc"><span class="mk ub gk bf">•</span><p>German: Bubenheim & Elyas, Rowwad Translation Center</p></div></li>
      <li><div class="tc"><span class="mk ub gk bf">•</span><p>Japanese: Ryoichi Mita, Japanese Saeed Sato*</p></div></li>
      <li><div class="tc"><span class="mk ub gk bf">•</span><p>Bengali (Zohurul Hoque), Russian (Abu Adel), Korean (Unknown)</p></div></li>
    </ul>
  </div>
</div>
<h3 class="sj zj fk kk wm ac">Try It Out and Share Your Feedback!</h3>
<p class="dk pk ac">
  We are building this project for the Ummah, and your feedback is incredibly valuable during this Vercel testing phase.
</p>
<blockquote class="hh rm _g ch pm sg ci ic" style="border-left: 4px solid #4E6BFF; padding-left: 20px;">
  <p class="dk pk ac">
    You can access and test the app right now at: <br>
    <a href="https://quran-web3-nft.vercel.app/" target="_blank" class="gk kk wm" style="color: #4E6BFF; text-decoration: none;">https://quran-web3-nft.vercel.app/</a>
  </p>
</blockquote>
<p class="dk pk ac">
  <strong class="gk kk wm">What do you think of the current features?</strong> Are there any specific tools, translations, or functionalities you would like us to add before the official IPFS launch? Drop a comment below or reach out to the community. Let's build the future of decentralized Quran accessibility together!
</p>
