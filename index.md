---
layout: default
title: PARTIDOS CA PEÑAROL
sub-title: Temporada 2024
author: CAPPER
---

<div class="mt-5 mb-4 black-title"> 
    <div class="referi-news">
        <li class="list-group-item extra-info espacios-0 kustom_culture">
            <h2>📺️partidos completos del CA Peñarol - temporada 2024</h2> 
            <h5>🎤relato: maximo goñi</h5>
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
                <span class="dyuthi_regular">{{ post.sub-title }}</span>
              </div>
              <div class="card-body rounded-0 card-text" style="padding: 0rem;">
                <a href="{{ site.url | relative_url }}{{ post.url }}">
                    <img src="{{ site.url | relative_url }}{{ post.image }}" width="100%">
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
<hr/>
<div class="mt-5 mb-4 black-title">
    <h5 class="text-success mb-0 pb-0 kustom_culture">
        <span>Diego Aguirre: 🗨️"Sequeira tendrá al menos 3 semanas de recuperación"</span><br>
    </h5>  
</div>
<iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/1873161462&color=d4aa00"></iframe>
<div class="mt-5 mb-4 black-title">
    <h5 class="text-success mb-0 pb-0 kustom_culture">
        <span>Dura crítica de José Luis Chilavert: 🗨️"A Alonso no lo vi defender a los jugadores uruguayos que dieron la cara"</span><br>
    </h5>  
</div>
<iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/1873931055&color=%23d4aa00&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe>
<hr/>
<div class="mt-5 mb-4 black-title"> 
    <div class="referi-news">
        <li class="list-group-item extra-info espacios-0 kustom_culture">
            <h2>🗞️noticias del CA Peñarol</h2> 
        </li>
    </div>
</div>
<div class="container-fluid">
   <div class="row">
      {% for post in site.categories.noticias limit: 24 %}
      <div class="col-md-4">
        <div class="card border-0 mb-4 bg-secondary" style="padding: 0.1rem; border-radius: 8px;display: inline-block;"><!-- 286px; -->
            <div class="card-header archivo bg-dark text-center">
                {{ post.date_es }}
            </div>
            <img src="{{ post.image }}" height="100%" width="100%">
            <div class="card-body card-text" style="padding: 0;">
                <div class="referi-news">
                    <strong>
                        <p>
                            {{ post.title }}
                        </p>
                    </strong>
                    <p>
                        <a href="{{ site.url | relative_url }}{{ post.url }}" style="font-weight: 0;" class="kustom_culture">ver contenido </a>
                    </p>
                </div>
            </div>
        </div>
        </div>
      {% endfor %}
    </div>
    
</div>
<div style='height: 300px;'></div>



