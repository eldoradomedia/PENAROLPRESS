---
layout: default
title: Partidos de Peñarol
sub-title: Temporada 2024
author: elbostero.tk
---

<div class="mt-5 mb-4 dyuthi_regular">
    <h2 class="text-success kustom_culture">
        partidos completos de peñarol 
    </h2>
    <strong>Temporada 2024</strong>
    <hr>
</div>
<div class="cover">
    <button class="left" onclick="leftScroll()">
        <i class="fas fa-angle-double-left"></i>
    </button>
    <div class="scroll-images">
        {% for post in site.categories.partidos-completos %}
        <div class="child">
            <div class="card m-4">
                <div class="card-header text-center kustom_culture">
                    <h4>{{ post.torneo }}</h4>
                </div>
                <img src="{{ post.image | prepend: base.url }}" width="100%">
                <div class="card-body">
                    <h4 class="card-title kustom_culture">
                        {{ post.local }} X<br>
                        {{ post.visitante }}
                    </h4>
                    <h5 class="card-text dyuthi_regular">{{ post.subtitle }}</h5>
                    <a href="{{ site.url }}{{ post.url }}" class="btn btn-success kustom_culture">ver contenido </a>
                </div>
            </div>
        </div>
        {% endfor %}
    </div>
    <button class="right" onclick="rightScroll()">
        <i class="fas fa-angle-double-right"></i>
    </button>
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