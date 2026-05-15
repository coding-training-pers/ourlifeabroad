---
layout: default
lang: en
title: Home
permalink: /en/

---

# Welcome to Our Life Abroad 🌍

We're Romain and [Name], a French couple who ditched the 9-to-5 to live differently.

**Our philosophy: slow travel**  
No rushing, no tourist checklists. We settle in each city for 1-2 months to live like locals.

## 📍 Currently in: Salta

## 🗺️ Our journey
- **Asia**: Bali, Vietnam, Thailand, Philippines  
- **Oceania**: 8 years in Australia  
- **South America**: Salta (Argentina), Asunción (Paraguay), Lima, Arequipa (Peru)...

---

## 📝 Latest Posts

{% assign posts_en = site.posts | where: "lang", "en" %}
{% for post in posts_en limit:5 %}
<div style="margin: 2rem 0; padding: 1.5rem; background: #f9f9f9; border-radius: 8px;">
  <h3><a href="{{ post.url | relative_url }}" style="color: #667eea; text-decoration: none;">{{ post.title }}</a></h3>
  <p style="color: #666; margin: 0.5rem 0;">{{ post.date | date: "%d/%m/%Y" }} • By {{ site.authors[post.author].name }}</p>
  <p>{{ post.excerpt | strip_html | truncate: 200 }}</p>
  <a href="{{ post.url | relative_url }}" style="color: #764ba2; font-weight: 500;">Read more →</a>
</div>
{% endfor %}