---
layout: default
lang: fr
title: Accueil
---

# Bienvenue sur Notre Vie à l'Étranger 🌍

Nous sommes Romain et [Prénom], un couple français qui a quitté la routine métro-boulot-dodo pour vivre autrement.

**Notre philosophie : le slow travel**  
Pas de rush, pas de checklist touristique. On s'installe 1 à 2 mois par ville pour vivre comme des locaux.

## 📍 Actuellement : [Ta ville actuelle]

## 🗺️ Notre parcours
- **Asie** : Bali, Vietnam, Thaïlande, Philippines  
- **Océanie** : 8 ans en Australie  
- **Amérique du Sud** : Salta (Argentine), Asunción (Paraguay), Lima, Arequipa (Pérou)...

---

## 📝 Derniers Articles

{% assign posts_fr = site.posts | where: "lang", "fr" %}
{% for post in posts_fr limit:5 %}
<div style="margin: 2rem 0; padding: 1.5rem; background: #f9f9f9; border-radius: 8px;">
  <h3><a href="{{ post.url | relative_url }}" style="color: #667eea; text-decoration: none;">{{ post.title }}</a></h3>
  <p style="color: #666; margin: 0.5rem 0;">{{ post.date | date: "%d/%m/%Y" }} • Par {{ site.authors[post.author].name }}</p>
  <p>{{ post.excerpt | strip_html | truncate: 200 }}</p>
  <a href="{{ post.url | relative_url }}" style="color: #764ba2; font-weight: 500;">Lire la suite →</a>
</div>
{% endfor %}