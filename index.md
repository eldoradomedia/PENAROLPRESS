---
layout: default
title: PARTIDOS CA PEÑAROL
sub-title: Temporada 2024
author: CAPPER
---

<div class="mt-5 mb-4 black-title">
  <h1 class="text-success mb-0 pb-0 kustom_culture 🙏🏿 👏🏿">
      <center><h2 style="color: #ffffe0;">partidos completos</h2></center>
  </h1> 
</div>

<div class="container-fluid cover">
    <button class="left" onclick="leftScroll()">
        <i class="fas fa-angle-double-left"></i>
    </button>
    <div class="scroll-images">
        {% for post in site.categories.partidos-completos %}
           <div class="child">
                <div class="container-fluid d-flex kustom_culture align-items-center justify-content-center ">
                    <div class="bronce">
                        <div>
                            <h2 class="justify-content-center kustom_culture">{{ post.torneo-corriente }}</h2>
                        </div>
                        <div class="text-center">
                            <span class="c justify-content-center ms-2">
                                <img src="{{ site.url | relative_url }}/images/{{ post.image-local }}" width="{{ post.width-local }}">
                            </span>
                            <span class="b justify-content-center ms-2">
                                <img src="{{ site.url | relative_url }}/images/{{ post.image-away }}" width="{{ post.width-away }}">
                            </span>
                        </div>
                        <div class="text-center text-success">
                            <a href="{{ site.url | relative_url }}{{ post.url }}" >
                                <h5 class="kustom_culture" style="background: #7a7459;color: #ffffe0;">ver online</h5>
                            </a>
                        </div>
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
  <h1 class="text-success mb-0 pb-0 kustom_culture 🙏🏿 👏🏿">
      <center><h2 style="color: #ffffe0;">noticias</h2></center>
  </h1> 
</div>
<div class="container-fluid">
   <div class="row">
      {% for post in site.categories.noticias limit: 15 %}
      <div class="col-md-4">
        <div class="card border-0 mb-4 bg-secondary align-items-center justify-content-center" style="padding: 0.1rem; border-radius: 8px;display: inline-block;"><!-- 286px; -->
            <img src="{{ post.image }}" height="100%" width="100%">
            <div class="card-body card-text" style="padding: 0;">
                <div class="referi-news">
                    <span style="font-size: 20px;">
                        {{ post.title }}
                    </span>
                    <p style="color: #917c6f;font-size: 14px;"> {{ post.date_es }}</p>
                    <div class="text-center text success">
                        <a href="{{ site.url | relative_url }}{{ post.url }}">
                            <h5 class="kustom_culture" style="background: #7a7459;color: #ffffe0;">ver online</h5>
                        </a>
                    </div>
                </div>
            </div>
        </div>
        </div>
      {% endfor %}
    </div>
    
</div>

<div style='height: 300px;'></div>



