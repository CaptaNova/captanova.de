---
layout: default
content-type: music
title: Musik
permalink: /musik/
---

<div class="intro">
  <p>Sakrale Musik muss nicht langweilig sein.
    Unsere Orchestrierungen und Arrangements sind stark von orchestraler Filmmusik beeinflusst und machen geistliches Liedgut auch jüngerem Publikum zugänglich.</p>
  <p>Alle hier aufgeführten Noten stehen unter der <a href="https://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International Lizenz (CC BY 4.0)</a> und dürfen somit frei verwendet und bearbeitet werden.</p>
</div>

<div class="panel-container">
  {% for item in site.data.sheet_music %}
    <div class="panel">
      <div class="panel-content">
        <h2>{{ item.title }}</h2>
        <h3>{{ item.subtitle | default: "&nbsp;" }}</h3>
        <ul>
          <li><svg class="feather"><use xlink:href="/assets/images/feather-sprite.svg#users"/></svg> {{ item.category }}</li>
          <li><svg class="feather"><use xlink:href="/assets/images/feather-sprite.svg#bar-chart"/></svg> {{ item.difficulty }}</li>
        </ul>
        <audio controls="" style="display: block; width: 100%;">
          <source src="https://github.com/CaptaNova/sheet-music/raw/master/{{ item.link }}/Audio.mp3" type="audio/mpeg">
          <source src="https://github.com/CaptaNova/sheet-music/raw/master/{{ item.link }}/Audio.ogg" type="audio/ogg">
          <p>Dein Browser unterstützt HTML5 audio nicht. Hier ist ein <a href="https://github.com/CaptaNova/sheet-music/raw/master/{{ item.link }}/Audio.mp3">Link zum Hörbeispiel</a>.</p>
        </audio>
        <a href="https://github.com/CaptaNova/sheet-music/raw/master/{{ item.link }}/Full_de.pdf" class="button" download>
          <span class="button-icon"><svg class="feather"><use xlink:href="/assets/images/feather-sprite.svg#download"/></svg></span>
          <span class="button-text">Noten herunterladen</span>
        </a>
      </div>
    </div>
  {% endfor %}
</div>
