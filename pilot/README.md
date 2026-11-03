# Pilote EM Signature Manager — 1 collaborateur

Branche de préparation, **sans modification des signatures Gmail ni de la branche main**.

## Référence graphique
Figma : https://www.figma.com/design/K4fXSmSlt3X4EuTh3SjcoN/EM?node-id=1009-24629

- Largeur totale : **346 px**
- Logo : **71 × 39 px**
- Colonne des coordonnées : **240 px**
- Pictogrammes des coordonnées : **10 × 10 px**
- Bandeau inférieur : **320 × environ 40 px**
- Typographie : Arial/Helvetica de repli (Helvetica dans Figma), nom 13 px, poste 10 px
- Couleurs : #101828, #667085, #125ED4, #EBEBEB

## Fichiers à fournir (PNG publics, pas de SVG intégrés au mail)
Déposer dans `assets/signature/` :
- `logo-em.png` — logo exporté de Figma, 142 × 78 px (affiché 71 × 39)
- `linkedin.png` — bloc LinkedIn, affiché à 71 px de largeur
- `expertises.png` — pictogrammes métiers, affichés à 71 px
- `mail.png`, `web.png`, `phone.png`, `location.png` — pictogrammes affichés à 10 × 10 px
- `bandeau-inferieur.png` — bloc de 320 × 40 px, idéalement export 640 × 80 px

Les assets graphiques doivent correspondre aux éléments **visibles** du composant Figma. Le fond et le bandeau éventuels issus de Signitic ne doivent pas être utilisés sans vérification. Pour conserver exactement le rendu, exporter les illustrations depuis Figma au lieu de les redessiner.

## Champs dynamiques
`{{PRENOM}}`, `{{NOM}}`, `{{POSTE}}`, `{{ASSET_BASE}}`, `{{LINKEDIN_URL}}`, `{{CONTACT_ROWS}}`.

`{{CONTACT_ROWS}}` sera généré côté Apps Script sous forme de tables HTML pour email / site / mobile / fixe / localisation, avec échappement du texte et validation des liens. Les champs absents pourront être masqués.

**Ne pas écrire les noms, emails, numéros ou clés d'accès du collaborateur pilote dans GitHub** : le dépôt est public. Ces données resteront dans le Google Sheet privé.

## Validation du pilote
1. Héberger les PNG en HTTPS sur GitHub Pages, vérifier leurs URL publiques.
2. Générer un aperçu avec le collaborateur pilote à partir du Google Sheet privé.
3. Tester l'affichage (Gmail Web Chrome/Safari et applications Android/iPhone).
4. Sauvegarder la signature Gmail avant toute publication.
5. Déployer sur **un seul compte explicitement autorisé** ; exclure les comptes Signitic.
6. Comparer captures Gmail au composant Figma, corriger, puis prévoir le lot de 12.

La branche est un **socle technique**, pas un HTML final tant que les PNG originaux n'ont pas été intégrés et testés.
