---
layout: archive
title: "Bookshelf"
permalink: /bookshelf/
author_profile: true
published: false
---

Here are some of the books I've been reading.

<div class="bookshelf-grid">
{% for book in site.data.books %}
  <div class="book-item">
    <div class="book-cover">
      {% if book.image and book.image != "" %}
        <img src="{{ book.image }}" alt="{{ book.title }}">
      {% else %}
        <div class="placeholder-cover">{{ book.title | slice: 0 }}</div>
      {% endif %}
    </div>
    <div class="book-details">
      <h3>{{ book.title }}</h3>
      <p class="author">by {{ book.author }}</p>
      {% if book.rating %}
        <p class="rating">Rating: {{ "★" | times: book.rating }}</p>
      {% endif %}
      {% if book.thoughts %}
        <p class="thoughts"><em>"{{ book.thoughts }}"</em></p>
      {% endif %}
    </div>
  </div>
{% endfor %}
</div>

<style>
.bookshelf-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 2rem;
  margin-top: 1rem;
}

.book-item {
  display: flex;
  gap: 1rem;
  background: #f9f9f9;
  padding: 1rem;
  border-radius: 8px;
}

.book-cover {
  flex-shrink: 0;
  width: 80px;
}

.book-cover img {
  width: 100%;
  height: auto;
  border-radius: 4px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.placeholder-cover {
  width: 80px;
  height: 120px;
  background: #ddd;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2rem;
  color: #888;
  border-radius: 4px;
}

.book-details h3 {
  margin: 0 0 0.5rem 0;
  font-size: 1.1rem;
}

.book-details .author {
  font-size: 0.9rem;
  color: #666;
  margin-bottom: 0.5rem;
}

.book-details .thoughts {
  font-size: 0.9rem;
  color: #444;
  margin-top: 0.5rem;
}
</style>
