---
layout: default
title: "QUỐC MẠNH — personal archive"
---
<div class="browser">
  <div class="browser-title">Netscape — [Quốc Mạnh's Page]</div>
  <div class="address">https://qmarchive.github.io/</div>
</div>

<div class="shell">
  <aside class="sidebar">
    <div class="brand">QUỐC MẠNH</div>
    <div class="tagline">notes from somewhere<br>in Hanoi.</div>
    <nav>
      <a href="{{ '/' | relative_url }}">home</a>
      <a href="{{ '/writings/' | relative_url }}">writings</a>
      <a href="{{ '/photographs/' | relative_url }}">photographs</a>
      <a href="{{ '/notes/' | relative_url }}">notes</a>
      <a href="{{ '/about/' | relative_url }}">about</a>
    </nav>
    <div class="quote-side">some<br>places<br>stay with you<br>forever.</div>
    <div class="visitor">Yahoo!<br>360°<br><small>Member</small></div>
    <div class="visitors">visitors<br>001284<br><small>● ONLINE</small><br>Since 21.09.2026</div>
  </aside>

  <main class="main">
    <section class="hero">
      <div class="hero-img" aria-label="Hanoi at night"></div>
      <div class="hero-caption">“Có những ngày chẳng có gì đặc biệt,<br>nhưng tôi vẫn muốn nhớ về nó.”</div>
    </section>

    <section class="home-grid">
      <div>
        <div class="section-title">RECENTLY WRITTEN <a href="{{ '/writings/' | relative_url }}">→ more writings</a></div>
        {% for post in site.posts limit:7 %}
        <div class="entry">
          <span>{{ post.date | date: "%d.%m.%Y" }}</span>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </div>
        {% endfor %}
      </div>
      <div>
        <div class="section-title">NOTES <a href="{{ '/notes/' | relative_url }}">→ more</a></div>
        {% assign notes = site.notes | sort: "date" | reverse %}
        {% for note in notes limit:4 %}
        <div class="note"><small>{{ note.date | date: "%d.%m.%Y" }}</small><br>{{ note.title }}</div>
        {% endfor %}
      </div>
    </section>

    <section class="photos">
      <div class="section-title">PHOTOGRAPHS <a href="{{ '/photographs/' | relative_url }}">→ more photographs</a></div>
      <div class="photo-grid">
        {% for photo in site.photos limit:4 %}
        <a href="{{ photo.url | relative_url }}" class="photo-card">
          {% if photo.image %}<img src="{{ photo.image | relative_url }}" alt="{{ photo.title }}">{% endif %}
          <span>{{ photo.title }}</span>
        </a>
        {% endfor %}
      </div>
    </section>
  </main>

  <aside class="rightbar">
    <div class="clock" id="clock">21/09/2026<br>17:57:47<br>Hanoi, Vietnam</div>
    <div class="right-quote">Có những đêm ta chỉ muốn ngồi yên và để thời gian trôi.</div>
    <div class="polaroid">
      <div class="polaroid-img"></div>
      <div>Hanoi, always.</div>
    </div>
    <div class="archive-note">Hanoi<br>1999 — 2026<br>and beyond.</div>
  </aside>
</div>

<script>
(function(){
  const el=document.getElementById('clock');
  function tick(){
    const d=new Date();
    const p=n=>String(n).padStart(2,'0');
    el.innerHTML=p(d.getDate())+'/'+p(d.getMonth()+1)+'/'+d.getFullYear()+'<br>'+
      p(d.getHours())+':'+p(d.getMinutes())+':'+p(d.getSeconds())+'<br>Hanoi, Vietnam';
  }
  tick(); setInterval(tick,1000);
})();
</script>
