---
layout: default
title: Bitácora
---
<section class="journeylog" id="journeylog">
    <div class="container">
        <h2>Bitácora</h2>
        <div class="journeylog-container">
            {% for post in site.posts %}
            <article class="entry">
                <div>
                    <figure class="entry-imageContainer">
                        <img class="entry-image" src="/assets/images/journeylog/Vital_Strike_SoC.jpg" width="500" height="300"
                            alt="Imagen Bitácora" />
                    </figure>
                </div>
                <div class="entry-details">
                    <h3 class="entry-name">
                        {{ post.title }}
                    </h3>
                    <p class="entry-date">
                        <small><strong>Fecha: </strong>{{ post.date | date: "%d %B %Y" }}</small>
                    </p>
                    <div class="entry-excerpt">
                        {{ post.excerpt }}
                    </div>
                    <a class="entry-url" href="{{ post.url }}" >Leer más...</a>
                </div>
            </article>
            {% endfor %}
        </div>
    </div>
</section>