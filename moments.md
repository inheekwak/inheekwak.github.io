---
layout: default
title: Moments
permalink: /moments/
---

<style>
  .moments-intro {
    margin-bottom: 14px;
    color: #555;
  }

  .map-wrap {
    position: relative;
    width: 100%;
    max-width: 920px;
    margin: 0 auto 24px auto;
  }

  .map-image {
    display: block;
    width: 100%;
    border: 1px solid #e5e5e5;
    border-radius: 10px;
  }

  .map-marker {
    position: absolute;
    width: 14px;
    height: 14px;
    margin-left: -7px;
    margin-top: -7px;
    border-radius: 50%;
    background: #e74d3c;
    border: 2px solid #fff;
    box-shadow: 0 0 0 1px rgba(0, 0, 0, 0.15);
    transition: transform 0.15s ease;
  }

  .map-marker:hover {
    transform: scale(1.15);
  }

  .map-marker .tooltip {
    position: absolute;
    left: 12px;
    top: -10px;
    min-width: 180px;
    max-width: 260px;
    background: #fff;
    color: #333;
    border: 1px solid #e2e2e2;
    border-radius: 8px;
    padding: 10px 12px;
    line-height: 1.35;
    box-shadow: 0 4px 14px rgba(0, 0, 0, 0.08);
    opacity: 0;
    pointer-events: none;
    transform: translateY(3px);
    transition: opacity 0.15s ease, transform 0.15s ease;
    z-index: 10;
  }

  .map-marker:hover .tooltip {
    opacity: 1;
    transform: translateY(0);
  }

  .map-marker .tooltip strong {
    display: block;
    margin-bottom: 4px;
  }

  .trip-list {
    margin-top: 12px;
    padding-left: 18px;
  }

  .trip-list li {
    margin-bottom: 7px;
  }
</style>

<p class="moments-intro">
  Click a marker on the world map to open the trip post for that place.
</p>

<div class="map-wrap">
  <img
    class="map-image"
    src="https://upload.wikimedia.org/wikipedia/commons/8/80/World_map_-_low_resolution.svg"
    alt="World map with trip markers"
  >

  {% for place in site.data.moments.main %}
    {% assign x = place.lng | plus: 180.0 | times: 100.0 | divided_by: 360.0 %}
    {% assign y = 90.0 | minus: place.lat | times: 100.0 | divided_by: 180.0 %}
    <a
      class="map-marker"
      href="{{ '/moments/' | append: place.slug | append: '/' | relative_url }}"
      style="left: {{ x }}%; top: {{ y }}%;"
      aria-label="Open trip post for {{ place.title }}"
    >
      <span class="tooltip">
        <strong>{{ place.title }}</strong>
        {{ place.excerpt }}
      </span>
    </a>
  {% endfor %}
</div>

<ul class="trip-list">
  {% for place in site.data.moments.main %}
    <li>
      <a href="{{ '/moments/' | append: place.slug | append: '/' | relative_url }}">{{ place.title }}</a>
    </li>
  {% endfor %}
</ul>
