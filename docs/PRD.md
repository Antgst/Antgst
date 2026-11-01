# PRD — Profil GitHub

## Vision et public
Le dépôt spécial Antgst/Antgst porte la page de profil GitHub : README.md, visuels et métriques. Il présente le parcours, la stack, les projets et les liens de contact.

Public cible : recruteurs, collaborateurs techniques et visiteurs du profil. Le dépôt est un support personnel, pas un service multi-utilisateur.

## Exigences vérifiables
- **REQ-001 (P0)** — Afficher une présentation fidèle du parcours et des compétences, sans gonfler les années d'expérience ou la maîtrise technique. **Acceptation :** revue du fichier concerné et preuve de vérification avant livraison.
- **REQ-002 (P1)** — Conserver des liens de portfolio, CV et contact valides. **Acceptation :** revue du fichier concerné et preuve de vérification avant livraison.
- **REQ-003 (P1)** — Préserver la lisibilité Markdown/GitHub et l'accessibilité des visuels. **Acceptation :** revue du fichier concerné et preuve de vérification avant livraison.

## État et limites
Les fonctions décrites correspondent à la structure et au README observés sur main le 1er novembre 2026 ; leur fonctionnement en production n'a pas été testé durant cet audit. Le contenu doit rester cohérent avec les autres supports, sans synchronisation automatique présumée.

## Hors périmètre
Ne pas changer les informations biographiques sans source récente, ni modifier les projets liés ou les workflows de métriques.

## Risques et livraison
incohérences entre CV, portfolio et profil ; images externes indisponibles ; workflow Metrics avec droit d'écriture. Budget supplémentaire : 0 €. Toute modification doit passer par une branche et une PR ; distinguer validation documentaire, tests locaux et déploiement réel. Une PR ouverte n'est pas une livraison.
