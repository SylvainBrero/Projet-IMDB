# Projet-IMDB

## Fonctionnement :

Ce projet personnel, toujours en cours de réalisation, s'articule autour de la construction, via du scraping, d'une liste de film pouvant m'intéresser. Pour cela, un premier scraping du site "subscene" (site mettant à disposition des sous-titres) permet de mettre en évidence les nouveaux films disponibles en téléchargement, filtrés selon leur popularité et leur langue.

![Scraping_Subscene](https://i.imgur.com/TOPVKaf.png)

On constitue alors une liste de ces nouveaux films populaires, qu'on va compléter avec de nouvelles informations scrapées sur le site IMDB, telles que sa note, son genre et sa durée.

![Scraping_IMDB](https://i.imgur.com/07KsSaU.png)

On complètera ce tableau avec les liens vers IMDB et Subscene, afin d'avoir un accès direct aux informations sources.
Enfin, on utilisera SendGrid pour s'envoyer via email le tableau des sorties de la semaine, auquel on joindra un tableau Excel de la database à la date de l'email.

![Resultat](https://imgur.com/G1pnWf0.png)

Une partie "Log" a été implémentée afin de détecter et rapidement identifier tout problème dans le processus global de scraping et de rassemblement et traitement de ces données.


## Méthodologie et outils :

Acquisition : 
  - Firefox (geckodriver - Selenium)
  - Scraping (Python - Webscraping.ai)

On simule, via l'outil Geckodriver, un navigateur Firefox via lequel on chargera l'url souhaitée avant de scraper les données de cette page. On passe aussi par un outil de wbscraping afin d'éviter toute problématique CloudFlare parfois active sur la page en question.

Transformation :
  - Python (pandas - BeautifulSoup)

Les données récupérées sont traitées sous Python via les fonctionnalités BeautifulSoup et mises en forme dans un tableau récapitulatif.

Restitution:
  - Mailing (Sendgrid)

On utilise un service de mailing afin de pouvoir distribuer en toute simplicité un rapport mail suite à chaque exécution du script.
