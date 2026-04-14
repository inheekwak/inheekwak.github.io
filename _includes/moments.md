---
layout: default
title: Moments
permalink: /moments/
---

<style>
  .moment-container {
    margin-top: 30px;
  }
  .location-section {
    margin-bottom: 50px;
  }
  .location-title {
    font-family: 'Crimson Pro', serif;
    font-size: 1.8rem;
    border-bottom: 1px solid #ddd;
    padding-bottom: 10px;
    margin-bottom: 20px;
    color: #13294B; /* Matching your navbar color */
  }
  .gallery-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 20px;
  }
  .gallery-item {
    background: #fff;
    border: 1px solid #eee;
    border-radius: 12px;
    overflow: hidden;
    transition: transform 0.3s ease;
    box-shadow: 0 2px 5px rgba(0,0,0,0.05);
  }
  .gallery-item:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.1);
  }
  .gallery-item img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    display: block;
  }
  .gallery-caption {
    padding: 12px;
    font-size: 0.9rem;
    color: #555;
    text-align: center;
  }
</style>

<div class="moment-container">

  <div class="location-section">
    <h2 class="location-title">Alexandria, Virginia</h2>
    <div class="gallery-grid">
      <div class="gallery-item">
        <img src="{{ '/assets/img/moment/va-1.jpg' | relative_url }}" alt="Old Town">
        <div class="gallery-caption">Quiet walks in Old Town Alexandria.</div>
      </div>
      <div class="gallery-item">
        <img src="{{ '/assets/img/moment/va-2.jpg' | relative_url }}" alt="Shenandoah">
        <div class="gallery-caption">Nature getaway in Shenandoah.</div>
      </div>
    </div>
  </div>

  <div class="location-section">
    <h2 class="location-title">Omaha, Nebraska</h2>
    <div class="gallery-grid">
      <div class="gallery-item">
        <img src="{{ '/assets/img/moment/omaha-1.jpg' | relative_url }}" alt="Boys Town">
        <div class="gallery-caption">Institute for Human Neuroscience.</div>
      </div>
    </div>
  </div>

  <div class="location-section">
    <h2 class="location-title">Seoul, South Korea</h2>
    <div class="gallery-grid">
      <div class="gallery-item">
        <img src="{{ '/assets/img/moment/seoul-1.jpg' | relative_url }}" alt="Seoul City">
        <div class="gallery-caption">Hometown memories in Seoul.</div>
      </div>
    </div>
  </div>

</div>
