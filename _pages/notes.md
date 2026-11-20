---
layout: page
title: notes
permalink: /notes/
nav: true
nav_order: 4
---

<div class="notes-container">
  {% if site.notes.size > 0 %}
    <ul class="notes-list list-unstyled p-0 m-0">
      {% assign sorted_notes = site.notes | sort: "date" | reverse %}
      {% for note in sorted_notes %}
      <li class="note-item py-3 border-bottom" style="border-color: var(--global-divider-color) !important;">
        <div class="d-flex justify-content-between align-items-baseline flex-wrap">
          <h4 class="note-title mb-1">
            <a href="{{ note.url | relative_url }}" class="text-decoration-none font-weight-bold" style="color: var(--global-theme-color);">
              {{ note.title }}
            </a>
          </h4>
          {% if note.date %}
          <span class="note-date text-muted small">
            <i class="fa-regular fa-calendar fa-sm mr-1"></i>{{ note.date | date: "%b %d, %Y" }}
          </span>
          {% endif %}
        </div>

        {% if note.description %}
        <p class="note-description mb-2 text-muted" style="font-size: 0.95rem;">
          {{ note.description }}
        </p>
        {% endif %}

        <div class="note-footer d-flex flex-wrap align-items-center justify-content-between">
          <div class="note-badges d-flex flex-wrap align-items-center">
            {% if note.course %}
            <span class="badge badge-info mr-2">{{ note.course }}</span>
            {% endif %}
            {% if note.category %}
            <span class="badge badge-secondary mr-2">{{ note.category }}</span>
            {% endif %}
            {% for tag in note.tags %}
            <span class="text-muted small mr-2">#{{ tag }}</span>
            {% endfor %}
          </div>

          <div class="note-download-links small mt-2 mt-sm-0">
            {% if note.pdf %}
            <a href="{{ note.pdf | relative_url }}" class="text-muted mr-3 text-decoration-none" download title="Download PDF">
              <i class="fa-solid fa-file-pdf text-danger mr-1"></i>PDF
            </a>
            {% endif %}
            {% if note.tex %}
            <a href="{{ note.tex | relative_url }}" class="text-muted text-decoration-none" download title="Download TeX">
              <i class="fa-solid fa-file-code text-primary mr-1"></i>TeX
            </a>
            {% endif %}
          </div>
        </div>
      </li>
      {% endfor %}
    </ul>
  {% else %}
    <p class="text-muted">No notes published yet. Add <code>.md</code> files inside the <code>_notes/</code> directory to display them here.</p>
  {% endif %}
</div>
