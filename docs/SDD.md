# SDD — Profil GitHub

## État technique constaté
GitHub affiche README.md comme page de profil. Les assets statiques sont versionnés ; .github/workflows/metrics.yml actualise les métriques sur planification ou déclenchement manuel, avec permission contents:write. Aucun backend applicatif.

## Composants et flux
édition du README → revue Markdown et liens → PR → affichage sur GitHub. Les sources de vérité sont les fichiers réellement présents, puis README.md ; ne pas créer une seconde définition concurrente des contenus.

## Correspondance exigences
- **REQ-001** — Relire les contenus visibles, leurs sources et les chemins de fichiers ; consigner les divergences.
- **REQ-002** — Contrôler les liens et les ressources utilisés par le visiteur ; ne pas annoncer de succès sans ouverture réelle.
- **REQ-003** — Vérifier les contraintes d'affichage et de publication pertinentes ; conserver une preuve de la revue.

## Données, sécurité et retour arrière
incohérences entre CV, portfolio et profil ; images externes indisponibles ; workflow Metrics avec droit d'écriture. Ne pas publier de secrets ou d'informations privées. Toute mutation Git est réversible par une PR ciblée ; ne pas réécrire l'historique. Le dépôt n'implique pas de base de données métier.

## Vérifications et déploiement
Vérifier d'abord les scripts présents et le diff. Vérifications pertinentes : affichage Markdown GitHub, liens, ressources et cohérence avec le CV. Aucun test automatisé n'a été exécuté dans cette mission. Aucun résultat CI n'est présumé. Ne pas déclencher d'Actions payantes ni de production sans autorisation.
