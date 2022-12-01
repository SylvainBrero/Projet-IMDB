# Projet-IMDB

Ce projet personnel, toujours en cours de réalisation, s'articule autour de la construction, via du scraping, d'une liste de film pouvant m'intéresser. Pour cela, un premier scraping du site "subscene" (site mettant à disposition des sous-titres) permet de mettre en évidence les nouveaux films disponibles en téléchargement, filtrés selon leur popularité et leur langue.

![Scraping_Subscene](https://i.imgur.com/TOPVKaf.png)

On constitue alors une liste de ces nouveaux films populaires, qu'on va compléter avec de nouvelles informations scrapées sur le site IMDB, telles que sa note, son genre et sa durée.

![Scraping_IMDB](https://i.imgur.com/07KsSaU.png)

On complètera ce tableau avec les liens vers IMDB et Subscene, afin d'avoir un accès direct aux informations sources.
Enfin, on utilisera SendGrid pour s'envoyer via email le tableau des sorties de la semaine, auquel on joindra un tableau Excel de la database à la date de l'email.

![Resultat](https://imgur.com/G1pnWf0.png)
