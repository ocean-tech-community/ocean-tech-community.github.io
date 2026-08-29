# Ocean Tech — instructions pour les agents

Ce fichier est la mémoire de travail du dépôt. Lis-le avant toute modification
et applique-le par défaut, sauf instruction explicite plus récente de l’équipe.

## Communication avec l’équipe

- Le site et les échanges sont en français. Rédige en français, avec un ton
  direct, chaleureux et concret.
- Prends des initiatives raisonnables et explique brièvement ce qui a été
  modifié. Ne redemande pas une précision qui peut être déduite du dépôt.
- En cas d’ambiguïté qui changerait réellement le périmètre, pose une question
  courte avant d’agir.

## Intention produit et éditoriale

Ocean Tech est la communauté tech & produit de la côte basco-landaise. Le site
doit faciliter la participation, les prises de parole et les partenariats
locaux, avec une communication inclusive et sans posture marketing excessive.

- Tutoyer la personne qui lit.
- Utiliser une écriture inclusive naturelle (`participant·es`, `curieux·ses`)
  sans la rendre lourde.
- Mettre en avant les expériences concrètes, les échanges entre pairs et
  l’accessibilité : venir seul·e et ne pas être expert·e sont parfaitement OK.
- Ne pas confondre les formats : apéros informels, soirées avec talks, Labs de
  pratique entre pairs.
- Vérifier les dates, lieux, partenaires, chiffres et URLs avant de les publier.
  Ne pas inventer d’informations événementielles ou de promesses de sponsoring.

## Conventions du projet

- Le site est un site statique Hugo. Les sources sont dans `content/`,
  `layouts/`, `static/`, `i18n/fr.yaml` et `hugo.yaml`.
- Ne jamais modifier `public/` manuellement : c’est le résultat de la build.
- Mettre les textes réutilisés de l’interface dans `i18n/fr.yaml` plutôt que de
  les dupliquer dans les layouts.
- Réutiliser les partials et shortcodes existants avant de créer du HTML ou des
  liens dupliqués.
- Conserver la navigation, le rendu mobile, les libellés ARIA et les attributs
  de sécurité des liens externes (`noopener noreferrer`).
- Préserver les métadonnées SEO et les données structurées dans
  `layouts/_default/baseof.html`.
- Ne pas ajouter une dépendance JavaScript ou un service externe pour résoudre
  une interaction simple.

## Contenu et événements

- Les pages éditoriales se trouvent dans `content/*.md`.
- Les événements sont dans `content/evenements/*.md` ; leurs photos vont dans
  `static/images/events/` avec un texte alternatif descriptif.
- Pour un nouvel événement, fournir au minimum titre, description, date et
  métadonnées `event`. Ajouter talks, intervenant·es et galerie seulement quand
  ces informations sont disponibles et validées.
- Garder les appels à l’action cohérents : rejoindre la communauté, s’inscrire
  au prochain rendez-vous, proposer un sujet ou devenir partenaire.

## Qualité et livraison

- Préserver les changements existants qui ne concernent pas la demande.
- Utiliser `apply_patch` pour les modifications de fichiers.
- Pour lancer le site localement avec rechargement automatique, exécuter
  `hugo server --buildDrafts`, puis ouvrir l’URL affichée par Hugo
  (habituellement `http://localhost:1313/`).
- Après une modification, lancer une vérification proportionnée au changement ;
  pour le site, préférer une build Hugo lorsqu’elle est disponible.
- Signaler clairement les limites, hypothèses ou éléments restant à valider.
- Ne pas committer, pousser, déployer ou modifier une configuration externe sans
  demande explicite.
