---
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
                    {% assign foundImage = 0 %}
                    {% assign images = post.content | split:"<img " %}
                    {% for image in images %}
                        {% if image contains 'src' %}
                            {% if foundImage == 0 %}
                            {% assign html = image | split:"/>" | first %}
                            {% assign tags = html | split:" " %}
                            {% for tag in tags %}
                                {% if tag contains 'src' %}
                                <img class="entry-image" alt="Imagen Bitácora" {{ tag }} />
                                {% endif %}
                            {% endfor %}
                            {% assign foundImage = 1 %}
                            {% break %}
                            {% endif %}
                        {% endif %}
                    {% endfor %}
                    {% if foundImage == 0 %}
                    <img class="entry-image" alt="Imagen Bitácora" src="/assets/images/journeylog/Vital_Strike_SoC.jpg" />
                    {% endif %}
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