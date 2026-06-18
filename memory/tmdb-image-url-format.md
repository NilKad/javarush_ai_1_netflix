---
name: tmdb-image-url-format
description: Правильний формат URL для зображень TMDb
metadata:
  type: reference
---

TMDb зображення потрібно брати з `image.tmdb.org`, а не `media.themoviedb.org`.
Формат: `https://image.tmdb.org/t/p/{розмір}/{poster_path}.jpg`
- w185, w300, w342, w500, w780 — доступні розміри
- `media.themoviedb.org/t/p/w300_and_h450_best` — не працює як зовнішнє посилання

**Why:** media.themoviedb.org — внутрішній CDN для сайту TMDb, він блокує зовнішні запити. image.tmdb.org — публічний CDN для API.

**How to apply:** Використовувати `https://image.tmdb.org/t/p/w300/` для постерів 200px і `https://image.tmdb.org/t/p/w780/` для фону hero.
