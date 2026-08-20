---
layout: default
title: Home
nav_order: 1
description: "Startseite der Chroniken der Schwertküste"
---

<div style="display: flex; gap: 25px; align-items: flex-start; flex-wrap: wrap;">

  <!-- LINKS: SEITENLEISTE / NAVIGATION -->
  <aside style="flex: 1; min-width: 220px; max-width: 280px; background: rgba(0,0,0,0.04); padding: 15px; border-radius: 8px; border-left: 4px solid #8c2a1c;">
    
    <h3 style="margin-top: 0;">📜 Chroniken</h3>
    <ul style="list-style: none; padding-left: 0; line-height: 1.8;">
      <li>📖 <a href="./chroniken/"><b>Alle Recaps</b></a></li>
      
      <!-- AUTOMATISCHE SCHLEIFE (NEUESTE ZUERST) -->
      {% assign recaps = site.html_pages | where_exp: "item", "item.path contains 'chroniken/'" | sort: "order" | reverse %}
      {% for recap in recaps %}
        {% if recap.title and recap.name != "index.md" %}
          <li>👉 <a href="{{ recap.url | relative_url }}">{{ recap.title }}</a></li>
        {% endif %}
      {% endfor %}
    </ul>

    <hr style="border: 0; border-top: 1px solid #ccc; margin: 15px 0;">

    <h3>🗝️ Archiv</h3>
    <ul style="list-style: none; padding-left: 0; line-height: 1.8;">
      <li>🗺️ <a href="./orte/">Orte & Schauplätze</a></li>
      <li>👤 <a href="./charaktere/">Personen & Helden</a></li>
      <li>📜 <a href="./archiv/">Briefe & Fundstücke</a></li>
    </ul>

  </aside>


  <!-- RECHTS: HAUPTINHALT -->
  <main style="flex: 3; min-width: 300px;">

    <h1>⚔️ Chroniken der Schwertküste</h1>

    <blockquote>
      📜 <i>„Ein Schicksal, geschmiedet im Schatten alter Legenden. Wer die Tiefen der Welt betritt, muss bereit sein, sich ihren Erinnerungen zu stellen.“</i>
    </blockquote>

    <h2>📍 Aktueller Status</h2>
    <p>Die Gruppe befindet sich derzeit in <b>Gullykin</b> und untersucht die Spuren rund um die <i>Firewine Bridge</i>.</p>

    <h2>⚔️ Die Helden</h2>
    <ul>
      <li><b><a href="./charaktere/charakter-1.md">Kyros</a></b> — Tiefling / Sorcerer</li>
      <li><b><a href="./charaktere/charakter-2.md">Quintherra</a></b> — Variant Aasimar / Bard</li>
      <li><b><a href="./charaktere/charakter-3.md">Fiona</a></b> — Human / Ranger</li>
      <li><b><a href="./charaktere/charakter-4.md">Ikarus</a></b> — Human / Wizard</li>
      <li><b><a href="./charaktere/charakter-5.md">Zricha</a></b> — Asimar / Cleric</li>
    </ul>

    <h2>📜 Letzter Bericht</h2>
    <p>In der letzten Sitzung drang die Gruppe tief unter die Hügel von Gullykin vor...</p>

  </main>

</div>
