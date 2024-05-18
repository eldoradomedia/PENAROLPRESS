---
layout: default
title: PARTIDOS PEÑAROL
sub-title: Temporada 2024
author: elbostero.tk
---

<div class="mt-5 mb-4 dyuthi_regular">
    <h2 class="text-success kustom_culture">
        <span>partidos</span>
        <img src="{{ site.url }}/images/cx12.png" height="25px;">
    </h2>
    <strong>Temporada 2024</strong>
    <hr>
</div>
<div class="container-fluid cover">
    <button class="left" onclick="leftScroll()">
        <i class="fas fa-angle-double-left"></i>
    </button>
    <div class="scroll-images">
        {% for post in site.categories.partidos-completos %}
           <div class="child">
            <div class="card cardfix m-4 bg-dark">
                <div class="card-header text-center dyuthi_regular">
                    <h6>Jornada {{ post.jornada }} · {{ post.torneo }}</h6>
                </div>
                <img src="{{ post.image | prepend: baseurl }}" width="100%">
                <div class="card-body">
                    <h4 class="card-title text-white kustom_culture">
                        {{ post.local }} X<br>
                        {{ post.visitante }}
                    </h4>
                    <h5 class="card-text text-white dyuthi_regular">{{ post.subtitle }}</h5>
                    <a href="{{ site.url }}/{{ post.url }}" class="btn btn-danger kustom_culture">ver contenido </a>
                </div>
            </div>
           </div>
        {% endfor %}
    </div>
    <button class="right" onclick="rightScroll()">
        <i class="fas fa-angle-double-right"></i>
    </button>
</div>

<div class="mt-5 mb-4 dyuthi_regular">
    <h2 class="text-success kustom_culture">
        <span>Noticias</span>
        <img src="{{ site.url }}/images/referi.png" height="15px;">
    </h2>
    <strong>Temporada 2024</strong>
    <hr>
</div>

   <div class="row">
      {% for post in site.categories.noticias limit: 12 %}
      <div class="col cards-padding">
        <div class="container-fluid">
            <div class="card m-2" style="width: 250px;border: 0;">
                <img src="{{ post.image | prepend: baseurl }}" width="100%">
                <div class="card-body kustom_culture">
                  <h6>{{ post.title | truncatewords: 12 }}</h6>
                  <a href="{{ post.url | prepend: baseurl }}" class="btn btn-success kustom_culture">ver contenido </a>
                </div>
            </div>
        </div>
      </div>
      {% endfor %}
    </div>


<script>
  document.addEventListener("DOMContentLoaded", function () {
  const scrollImages = document.querySelector(".scroll-images");
  const scrollLength = scrollImages.scrollWidth - scrollImages.clientWidth;
  const leftButton = document.querySelector(".left");
  const rightButton = document.querySelector(".right");
  function checkScroll() {
    const currentScroll = scrollImages.scrollLeft;
    if (currentScroll === 0) {
      leftButton.setAttribute("disabled", "true");
      rightButton.removeAttribute("disabled");
    } else if (currentScroll === scrollLength) {
      rightButton.setAttribute("disabled", "true");
      leftButton.removeAttribute("disabled");
    } else {
      leftButton.removeAttribute("disabled");
      rightButton.removeAttribute("disabled");
    }
  }
  scrollImages.addEventListener("scroll", checkScroll);
  window.addEventListener("resize", checkScroll);
  checkScroll();
  function leftScroll() {
    scrollImages.scrollBy({
      left: -300,
      behavior: "smooth"
    });
  }
  function rightScroll() {
    scrollImages.scrollBy({
      left: 300,
      behavior: "smooth"
    });
  }
  leftButton.addEventListener("click", leftScroll);
  rightButton.addEventListener("click", rightScroll);
});
 </script>

