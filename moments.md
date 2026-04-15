---
layout: default
title: Moments
permalink: /moments/
locations:
  - title: "Alexandria, Virginia"
    images:
      - src: "/assets/img/moment/va-1.jpg"
        caption: "Quiet walks in Old Town Alexandria."
      - src: "/assets/img/moment/va-2.jpg"
        caption: "Nature getaway in Shenandoah."
      - src: "/assets/img/moment/va-3.jpg"
        caption: "Sunset on the river."
  - title: "Omaha, Nebraska"
    images:
      - src: "/assets/img/moment/omaha-1.jpg"
        caption: "Institute for Human Neuroscience."
  - title: "Seoul, South Korea"
    images:
      - src: "/assets/img/moment/seoul-1.jpg"
        caption: "Hometown memories in Seoul."
---

<style>
:root {
  --nav-height: 64px; /* adjust to your navbar height */
  --card-width: 280px;
  --card-height: 200px;
  --gap: 20px;
}

/* container spacing so nav doesn't cover content */
.moment-container {
  padding-top: calc(var(--nav-height) + 20px);
}

/* location heading won't be hidden when linked to */
.location-title {
  scroll-margin-top: calc(var(--nav-height) + 12px);
}

/* horizontal gallery */
.gallery-grid {
  display: flex;
  gap: var(--gap);
  overflow-x: auto;
  padding-bottom: 8px;
  -webkit-overflow-scrolling: touch;
  scroll-snap-type: x mandatory;
  scrollbar-width: thin;
}

/* each card is fixed width and won't shrink */
.gallery-item {
  flex: 0 0 var(--card-width);
  width: var(--card-width);
  height: auto;
  border-radius: 12px;
  overflow: hidden;
  background: #fff;
  border: 1px solid #eee;
  box-shadow: 0 2px 5px rgba(0,0,0,0.05);
  transition: transform 0.25s ease, box-shadow 0.25s ease;
  scroll-snap-align: start;
}

/* hover effect */
.gallery-item:hover {
  transform: translateY(-6px);
  box-shadow: 0 10px 20px rgba(0,0,0,0.1);
}

/* image sizing */
.gallery-item img {
  width: 100%;
  height: var(--card-height);
  object-fit: cover;
  display: block;
}

/* caption */
.gallery-caption {
  padding: 12px;
  font-size: 0.9rem;
  color: #555;
  text-align: center;
}

/* hide default scrollbar on WebKit but keep scrolling */
.gallery-grid::-webkit-scrollbar {
  height: 8px;
}
.gallery-grid::-webkit-scrollbar-thumb {
  background: rgba(0,0,0,0.15);
  border-radius: 999px;
}
</style>

<div class="moment-container">
  {% for loc in page.locations %}
    <div class="location-section">
      <h2 class="location-title">{{ loc.title }}</h2>
      <div class="gallery-grid" aria-label="Gallery for {{ loc.title }}">
        {% for img in loc.images %}
          <figure class="gallery-item">
            <img src="{{ img.src | relative_url }}" alt="{{ img.caption | escape }}">
            <figcaption class="gallery-caption">{{ img.caption }}</figcaption>
          </figure>
        {% endfor %}
      </div>
    </div>
  {% endfor %}
</div>
