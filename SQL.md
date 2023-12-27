## Récupérer 15 lignes
SELECT * FROM viewing LIMIT 15;


## Sélectionner toutes données, rangées dans un ordre aléatoire
SELECT * FROM viewing ORDER BY random();

## Récupérer 15 lignes de manière aléatoire 
SELECT * FROM viewing ORDER BY random() LIMIT 15;

## Récupérer la moyenne d'age, classée par pays
SELECT viewer_country, AVG(viewer_age_group) AS moyenne_age FROM viewing GROUP BY viewer_country ORDER BY moyenne_age;

## Récupérer le nombre d'épisodes regardés, classé par tranche d'âge, et rangé par tranche d'age décroissant
SELECT COUNT(*) AS visionnages, viewer_age_group FROM viewing GROUP BY viewer_age_group ORDER BY viewer_age_group DESC;

## Récupérer le nombre de visionnages par an
SELECT EXTRACT(year FROM viewing_date) as date, COUNT(*) AS visionnages FROM viewing GROUP BY date ORDER BY date;