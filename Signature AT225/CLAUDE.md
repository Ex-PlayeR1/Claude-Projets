# Signature AT225

Générateur de signature email pour AT225 : une page HTML autonome (`generateur-signature.html`) avec formulaire de saisie et aperçu, thème clair/sombre.

## État du projet

- [generateur-signature.html](generateur-signature.html) — générateur de signature email AT225.
- [tombola-journaliers.html](tombola-journaliers.html) — tirage au sort quinzomadaire pour les journaliers ayant travaillé plus de 80h (voir section dédiée ci-dessous).
- Pas de build, pas de dépendances — fichiers HTML/CSS/JS statiques à ouvrir directement dans un navigateur.

## Tombola des journaliers (tombola-journaliers.html)

Page de tirage au sort pour récompenser en goodies (T-shirt, casquette, mug AT225) les journaliers de Dorado Ivory SA (Toumodi) ayant dépassé 80h travaillées sur la quinzaine. Contient des données personnelles (noms, heures) — le dépôt est privé.

- Données extraites manuellement des factures AT225 (dossier `Factures Dorado v2.0/<quinzaine>/AT225 Facture *.xlsx`, colonnes Description + Total Heures), puis codées en dur dans le tableau `eligibles` en tête du `<script>`.
- Dernière quinzaine traitée : **01/07 au 15/07/2026** (35 éligibles).
- Tirage en 3 gagnants, révélés dans l'ordre 3ᵉ place → 2ᵉ place → grand gagnant, avec effets sonores synthétisés (Web Audio API) et visuels en crescendo (confettis, flash, spotlight).
- Publié en Artifact (lien à partager depuis le menu de partage de la page — reste privé sinon).
- Les icônes de lots (mug/casquette/T-shirt) sont des illustrations SVG stylisées, pas de vraies photos produit — à remplacer si le client fournit des photos réelles.
- Pour la prochaine quinzaine : relire les nouvelles factures AT225, refaire l'extraction (>80h), régénérer le tableau `eligibles`, republier.

## Notes de synchronisation multi-PC

Ce dépôt est utilisé depuis plusieurs ordinateurs. L'historique de conversation Claude Code n'est **pas** synchronisé entre machines (stockage local par PC). Pour garder le contexte à jour :
- Committer et pousser (`git push`) après chaque session de travail
- Noter ici les décisions ou l'état d'avancement importants avant de changer de machine
- Sur l'autre PC, faire `git pull` avant de reprendre le travail
