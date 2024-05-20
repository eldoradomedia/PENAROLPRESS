---
layout: default
title: PARTIDOS COMPLETOS DE PEÑAROL
sub-title: Temporada 2024
author: CAPPER
---

<div class="mt-5 mb-4 dyuthi_regular black-title top-top-style">
    <h1 class="text-success kustom_culture">
        <span>{{ page.title }}</span>
        <img src="{{ site.url }}/images/cx12.png" height="33px;">
    </h1>
    <hr>
    <strong>{{ page.sub-title }}</strong>
    
</div>
<div class="container-fluid cover">
    <button class="left" onclick="leftScroll()">
        <i class="fas fa-angle-double-left"></i>
    </button>
    <div class="scroll-images">
        {% for post in site.categories.partidos-completos %}
           <div class="child">
            <div class="card container-fluid m-4 bg-dark">
                <div class="card-header text-center dyuthi_regular">
                    <p>Jornada {{ post.jornada }} · {{ post.torneo }}</p>
                </div>
                <img src="{{ site.url }}/{{ post.image }}" width="100%">
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

<div class="mt-5 mb-4 dyuthi_regular top-top-style">
    <h2 class="text-success kustom_culture">
        <span>Noticias</span>
        <img src="{{ site.url }}/images/referi.png" height="25px;">
    </h2>
    <hr>
    <strong>Temporada 2024</strong>
    
</div>

   <div class="row">
      {% for post in site.categories.noticias limit: 30 %}
      <div class="col aire">
        <div class="container-fluid">
            <div class="card m-2" style="width: 250px;border: 0;">
                <img src="{{ post.image }}" width="100%">
                <div class="card-body kustom_culture">
                  <h6>{{ post.title | truncatewords: 12 }}</h6>
                  <a href="{{ site.url }}/{{ post.url }}" class="btn btn-success kustom_culture">ver contenido </a>
                </div>
            </div>
        </div>
      </div>
      {% endfor %}
    </div>





