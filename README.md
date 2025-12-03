# 📦 Floating Dock + Smart Iframe Modal

![Thumbnail](https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/amodernminimallayoutwithafloatingdockofcolorfulroundicons28patreonbloggergithub29ontherightsideofacleanwebpagemockup6676994054500999142.jpg)

A modern **floating dock with smart iframe modal** built for **bloggers, creators, and entrepreneurs**.  
This script allows you to showcase multiple links (Patreon, Blog, GitHub, etc.) inside a clean **expandable dock**,  
and each link opens in a **responsive modal iframe** without leaving your page.  

👉 **Perfect for Blogger, WordPress, or any HTML website.**

---

## 🌍 Live Preview  
🔗 [View Script in Action](https://beatzde4.blogspot.com/2025/08/introducing-floating-dock-with-smart.html)

---

## ✨ Features
- 🖱️ Expandable **floating dock** with icons & tooltips  
- 📑 Clean **modal iframe preview** (no page reloads)  
- 🎨 Modern CSS with animations and soft shadows  
- 📱 Fully responsive & mobile-friendly  
- 🔧 Easy to integrate into **Blogger, WordPress, or static HTML**  
- ⚡ Fast, lightweight, and customizable  

---

## 📥 Installation & Usage

1. **Copy the HTML code** from this repository.  
2. Paste it into your Blogger **HTML/JavaScript widget** or your site’s `<body>`.  
3. Update the links inside the dock (`Patreon`, `Blog`, `GitHub`) with your own URLs.  
4. Add the provided CSS and JavaScript sections (included in this repo) to your template or inside `<style>` and `<script>` tags.  

---

## 🛠 Example Dock Links
- Patreon Collections  
- Blog (Blogger Demo)  
- GitHub Repository  

Each link opens in a **modal iframe**, keeping users engaged on your site.  

---

## 📌 Use Cases
- 🎤 Creators showcasing Patreon or Gumroad collections  
- 📚 Bloggers embedding resource hubs  
- 👨‍💻 Developers linking project previews + GitHub repos  
- 💼 Entrepreneurs highlighting products/services without redirecting traffic  

---

## 🤝 Contributing
Feel free to fork this repo and make improvements!  
- Submit a pull request with your changes.  
- Report issues or suggestions in the **Issues** tab.  

---

## 📜 License
This project is licensed under the **MIT License** — free to use and modify.  

## [View Repo](https://github.com/debeatzgh1/-Floating-Dock-Smart-Iframe-Modal)
---
<!-- Floating Docs Carousel Widget -->
<style>
  /* Floating Container */
  #docs-carousel {
    position: fixed;
    top: 20px;
    right: 20px;
    width: 340px;
    max-height: 90vh;
    background: #fff;
    border-radius: 16px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.2);
    overflow: hidden;
    z-index: 9999;
    font-family: 'Segoe UI', sans-serif;
    animation: slideIn 0.8s ease-out;
  }

  @keyframes slideIn {
    from { transform: translateY(-50px); opacity: 0; }
    to { transform: translateY(0); opacity: 1; }
  }

  /* Carousel */
  .carousel-track {
    display: flex;
    transition: transform 0.5s ease-in-out;
  }

  .carousel-item {
    min-width: 100%;
    flex: 1 0 100%;
    text-align: center;
    padding: 10px;
  }

  .carousel-item img {
    width: 100%;
    height: 170px;
    object-fit: cover;
    border-radius: 12px;
    margin-bottom: 10px;
  }

  .carousel-item h3 {
    font-size: 16px;
    margin: 6px 0;
    color: #222;
  }

  .carousel-item p {
    font-size: 13px;
    color: #555;
    margin-bottom: 10px;
  }

  /* CTA Button */
  .cta-btn {
    display: inline-block;
    padding: 8px 14px;
    background: #16a34a;
    color: white;
    font-size: 13px;
    border-radius: 8px;
    text-decoration: none;
    transition: background 0.3s;
  }
  .cta-btn:hover {
    background: #15803d;
  }

  /* Controls */
  .carousel-controls {
    display: flex;
    justify-content: space-between;
    padding: 6px 12px;
  }

  .control-btn {
    background: #f3f4f6;
    border: none;
    padding: 6px 10px;
    border-radius: 50%;
    cursor: pointer;
    font-size: 14px;
    transition: background 0.3s;
  }
  .control-btn:hover {
    background: #e5e7eb;
  }

  /* Iframe modal */
  #iframe-modal {
    position: fixed;
    top: 0; left: 0;
    width: 100%; height: 100%;
    background: rgba(0,0,0,0.7);
    display: none;
    justify-content: center;
    align-items: center;
    z-index: 10000;
  }
  #iframe-modal iframe {
    width: 90%;
    height: 85%;
    border: none;
    border-radius: 12px;
    background: white;
  }
  #iframe-modal .close-btn {
    position: absolute;
    top: 20px; right: 30px;
    background: #ef4444;
    color: white;
    border: none;
    padding: 10px 14px;
    font-size: 14px;
    border-radius: 6px;
    cursor: pointer;
  }
</style>

<div id="docs-carousel">
  <div class="carousel-track">
    <!-- Item 1 -->
    <div class="carousel-item">
      <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/createatoolthatgeneratesiframeorcard-styleembedsforindividualbloggerpostscompletewiththumbnailtitleandreadmorebuttonforcross-blogpromotion754077096311972631.jpg" alt="Doc 1">
      <h3>Google Doc 1</h3>
      <p>Interactive document with detailed insights.</p>
      <a href="#" class="cta-btn" onclick="openIframe('https://docs.google.com/document/d/1-SLDt3imfmSn3bIldw_PkzJyhlunxQGE/preview')">Open in Frame</a>
    </div>
    <!-- Item 2 -->
    <div class="carousel-item">
      <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/createamodernandcleanthumbnailforawebdevelopmentproducttitledmodernhomepagestylingtemplatewithtailwindcss3420170625469385526.jpg" alt="Doc 2">
      <h3>Google Doc 2</h3>
      <p>Well-structured guide for projects and workflows.</p>
      <a href="#" class="cta-btn" onclick="openIframe('https://docs.google.com/document/d/1bEOxMCEmWALqqB0PUtaUxjA1-Wevdy1o/preview')">Open in Frame</a>
    </div>
    <!-- Item 3 -->
    <div class="carousel-item">
      <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/createacleanandmodernflat-stylethumbnailforaweb-basedtoolcalledhtmlpagegeneratorforblogger322282329178022614.jpg" alt="Doc 3">
      <h3>Google Doc 3</h3>
      <p>Compact strategy document with tips and ideas.</p>
      <a href="#" class="cta-btn" onclick="openIframe('https://docs.google.com/document/d/1s4xI5Fk2ZkGVZX0_NtTVHP0foeqs2re0/preview')">Open in Frame</a>
    </div>
    <!-- Item 4 -->
    <div class="carousel-item">
      <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/minimalistbusinessiconthemealaptopwithdollarsignsorgrowtharrows4197483127374475983.jpg" alt="Doc 4">
      <h3>Google Doc 4</h3>
      <p>Business-focused doc with monetization strategies.</p>
      <a href="#" class="cta-btn" onclick="openIframe('https://docs.google.com/document/d/1aBCDE12345abcdef/preview')">Open in Frame</a>
    </div>
    <!-- Item 5 -->
    <div class="carousel-item">
      <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/graphic-of-a-dollar-sign-surrounded-by-arrows-representing-the-flow-of-money-business-investment-and-cash-flow-management-free-vector526.jpg" alt="Doc 5">
      <h3>Google Doc 5</h3>
      <p>Insights into business investment & cash flow.</p>
      <a href="#" class="cta-btn" onclick="openIframe('https://docs.google.com/document/d/1fGHIJ67890klmnop/preview')">Open in Frame</a>
    </div>
    <!-- Item 6 -->
    <div class="carousel-item">
      <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/designamodernminimalisticdesignfeaturinganai-themedicon28likeabraincircuitorrobot29overlaidwithdebeatzgh.jpg" alt="Doc 6">
      <h3>Google Doc 6</h3>
      <p>AI-themed strategies and digital workflow guide.</p>
      <a href="#" class="cta-btn" onclick="openIframe('https://docs.google.com/document/d/1opQRST23456uvwxy/preview')">Open in Frame</a>
    </div>
    <!-- Item 7 -->
    <div class="carousel-item">
      <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/minimalistbusinessiconthemealaptopwithdollarsignsorgrowtharrows4197483127374475983.jpg" alt="Doc 7">
      <h3>Google Doc 7</h3>
      <p>Comprehensive digital marketing playbook.</p>
      <a href="#" class="cta-btn" onclick="openIframe('https://docs.google.com/document/d/1XYZABC98765lmnop/preview')">Open in Frame</a>
    </div>
    <!-- Item 8 -->
    <div class="carousel-item">
      <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/amodernminimallayoutwithafloatingdockofcolorfulroundicons28patreonbloggergithub29ontherightsideofacleanwebpagemockup6676994054500999142.jpg" alt="Doc 8">
      <h3>Google Doc 8</h3>
      <p>Creative floating dock styles for web projects.</p>
      <a href="#" class="cta-btn" onclick="openIframe('https://docs.google.com/document/d/1LMNOP54321qrstuv/preview')">Open in Frame</a>
    </div>
  </div>
  <div class="carousel-controls">
    <button class="control-btn" onclick="moveSlide(-1)">❮</button>
    <button class="control-btn" onclick="moveSlide(1)">❯</button>
  </div>
</div>

<!-- Iframe Modal -->
<div id="iframe-modal">
  <button class="close-btn" onclick="closeIframe()">✕ Close</button>
  <iframe src=""></iframe>
</div>

<script>
  let currentIndex = 0;
  const track = document.querySelector('.carousel-track');
  const items = document.querySelectorAll('.carousel-item');

  function moveSlide(dir) {
    currentIndex = (currentIndex + dir + items.length) % items.length;
    track.style.transform = `translateX(-${currentIndex * 100}%)`;
  }

  function openIframe(url) {
    document.querySelector('#iframe-modal iframe').src = url;
    document.getElementById('iframe-modal').style.display = 'flex';
  }

  function closeIframe() {
    document.getElementById('iframe-modal').style.display = 'none';
    document.querySelector('#iframe-modal iframe').src = '';
  }
</script>
