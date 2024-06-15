---
layout: default
title: PARTIDOS
sub-title: Temporada 2024
author: CAPPER
---

<div class="mt-5 mb-4 black-title">
    <h1 class="text-success mb-0 pb-0 kustom_culture">
        <span>partidos</span><br>
    </h1>  
    <div class="warning">
        <li class="list-group-item extra-info">
            <i class="fas fa-microphone fa-fw" aria-hidden="true"></i><span> Goñi - Bardaquián · Oriental 770</span>
        </li>
    </div>
</div>
<div class="container-fluid cover">
    <button class="left" onclick="leftScroll()">
        <i class="fas fa-angle-double-left"></i>
    </button>
    <div class="scroll-images">
        {% for post in site.categories.partidos-completos %}
           <div class="child">
            <div class="card border-0 container-fluid m-4 bg-dark">
              <div class="card-header text-center">
                <span class="dyuthi_regular">{{ post.partido }}</span>
              </div>
              <div class="card-body rounded-0 card-text" style="padding: 0rem;">
                <a href="{{ site.url }}{{ post.url }}">
                    <img src="{{ site.url }}/{{ post.image }}" width="100%">
                </a>
              </div>
            </div>
           </div>
        {% endfor %}
    </div>
    <button class="right" onclick="rightScroll()">
        <i class="fas fa-angle-double-right"></i>
    </button>
</div>
<div class="mt-5 mb-4 black-title">
    <h1 class="text-success espacios-0 kustom_culture">
        <span>noticias</span><br>
    </h1> 
    <div class="warning">
        <li class="list-group-item extra-info">
            <i class="far fa-newspaper fa-fw" aria-hidden="true"></i><span> Referi · El Observador</span> <i class="fa fa-check fa-fw" aria-hidden="true"></i><span> «Peñarol»</span>
        </li>
    </div>
</div>
<div class="container-fluid">
   <div class="row">
      {% for post in site.categories.noticias limit: 6 %}
      <div class="col">
        <div class="card border-0 mb-4 bg-secondary" style="padding: 0.1rem; border-radius: 8px;width: 446px;"><!-- 286px; -->
            <div class="card-header dyuthi_regular bg-dark text-center">
                {{ post.date_es }}
            </div>
            <img src="{{ post.image }}" height="100%" width="100%">
            <div class="card-body card-text" style="padding: 0rem;">
                <div class="referi-news"><strong><p>{{ post.title }}</p></strong></div>
                    <a href="{{ site.url }}/{{ post.url }}" class="kustom_culture">ver contenido </a>
                </div>
            </div>
        </div>
      {% endfor %}
    </div>
    <div style='height: 300px;'></div>
</div>




