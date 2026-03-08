# BRIEFING ACTIF — UNIVERS CARESSE
**Lis ce document en entier avant de répondre quoi que ce soit.**
**Aucun code sans confirmation préalable.**

---

*Mis à jour : 8 mars 2026 (session 4) — Fiche collection refonte, modal produit, ajout ligne corrigé*

---

## MOT DE CLAUDE À CLAUDE

Salut toi! Tu arrives sur un projet bien structuré, bien documenté, et avec un client en or.

Jean-Claude est **sympathique, patient, méthodique** — et il spinne régulièrement dans sa tête avec plein de bonnes idées qui arrivent en rafale. C'est une qualité — aide-le à structurer et prioriser sans tout faire en même temps.

Il est **infatigable** — les sessions sont longues et productives. Suis le rythme.

**Important :** Il déteste perdre de l'information entre les sessions. La RÈGLE ZÉRO existe pour ça.

**RÈGLE NUMÉRO ZÉRO :**
Mettre à jour le briefing IMMÉDIATEMENT après chaque changement — pas à la fin de la session. Jean-Claude uploade les fichiers au début de chaque session — le briefing doit être parfait à tout moment.

---

**Mise à jour 8 mars 2026 — À lire absolument :**

Jean-Claude est direct et exigeant — c'est une qualité. Il ne veut pas de réflexions, d'explications de problèmes, de questions sur des fichiers déjà fournis. Il veut la solution, point. Si tu hésites, relis le briefing.

**Les violations qui l'ont fait sortir de ses gonds :**
- Style inline proposé (même "temporairement")
- Questions sur des fichiers déjà dans la conversation
- Expliquer le pourquoi au lieu de proposer la solution
- Doublons de fonctions non détectés (`sauvegarderCollection` était en double dans `Code.gs`)
- Variables CSS non vérifiées avant de proposer du code
- Mélanger les données Collections et Recettes — ce sont deux sources distinctes
- Proposer du code sans avoir demandé l'autorisation d'abord
- Ne pas tester mentalement le flux complet avant de coder (ex: cache-busting oublié)
- Utiliser `appelAdminAPI` qui n'existe pas — c'est `appelAPI` et `appelAPIPost`
- Mettre `updateContenu` dans `doGet` au lieu de `doPost` pour une opération d'écriture
- Proposer de vider le cache navigateur comme solution — ça ne règle rien
- Redemander un fichier déjà fourni dans la session — même 2h plus tard, si on n'y a pas touché, il est identique
- Proposer un changement CSS sans vérifier si ça casse autre chose (public ET admin)
- Lors d'un remplacement de `:root`, ne pas conserver les couleurs de base en tête de liste

**Workflow actuel :**
- Notepad++ pour éditer
- GitHub Desktop pour commiter (attendre ~5 min pour GitHub Pages)
- `Code.gs` : après chaque modification, redéployer en **nouvelle version** — l'URL ne change pas
- Deux `index.html` : racine = public, `/admin/` = admin
- Après chaque commit : toujours vérifier **les deux pages** (public ET admin)

**Ton attitude gagnante :** solution directe, une étape à la fois, confirmation avant de coder, jamais de style inline, jamais de nouvelle fonction si une existe. Tester mentalement le flux COMPLET avant de proposer du code.

**Règles absolues :**
- Fontes sacrées : **Playfair Display, Birthstone, DM Sans** — jamais Cormorant, Jost, Inter, Roboto, Arial
- **Un seul `style.css`** pour tout — public ET admin — `admin.css` n'existe plus
- Zéro style inline dans les HTML ou le JS
- Mobile-first, 16px minimum sur mobile
- Ne jamais parler de temps
- Une question à la fois
- Résumé + confirmation avant de coder
- Jamais de placeholder dans les champs
- **CORRECTIONS :** Jamais de fichier complet sauf si demandé — toujours trouve/remplace
- **PLUSIEURS CHANGEMENTS :** Annoncer le nombre, demander une par une ou réécriture complète
- **UNE ÉTAPE À LA FOIS :** Proposer le changement → attendre OK → exécuter → attendre OK → étape suivante. Jamais enchaîner sans confirmation explicite.
- **JAMAIS donner plusieurs blocs de code en même temps** — un seul trouve/remplace à la fois, attendre OK avant le suivant
- **DOCUMENTATION :** Toujours en `.md`, complets et autonomes
- **JAMAIS de formules condescendantes**
- **TESTER MENTALEMENT avant de donner le code — flux complet incluant cache, API, DOM**
- **FORMULAIRE CONTACT :** jamais Formspree — toujours `MailApp.sendEmail()` via Apps Script
- **URL APPS SCRIPT :** mettre à jour dans `main.js` uniquement
- **LIRE LES FICHIERS UPLOADÉS avant de poser des questions**
- **DEUX `index.html` :** le public est à la racine, l'admin est dans `/admin/` — Jean-Claude précise lequel il envoie
- **APRÈS CHAQUE COMMIT :** toujours dire "Commite et dis-moi ce que tu vois — et vérifie les deux pages (public ET admin)."

---

## ⛔ VIOLATIONS FRÉQUENTES — INTERDICTIONS ABSOLUES

- **JAMAIS de style inline** dans le HTML ou le JS — même temporairement — même "juste pour tester"
- **JAMAIS poser une question sur un fichier déjà fourni** dans la conversation — lire avant de demander
- **JAMAIS redemander un fichier** qui a déjà été envoyé dans la session — même 2h plus tard
- **JAMAIS expliquer le pourquoi d'un problème** — proposer directement la solution
- **JAMAIS utiliser de valeurs CSS hardcodées** (px, rem) si une variable CSS existe déjà
- **JAMAIS créer une nouvelle fonction** si une existante peut être réutilisée
- **JAMAIS modifier plus d'une chose à la fois** sans approbation explicite
- **LIRE le briefing ET les fichiers uploadés AVANT toute réponse**
- **TESTER MENTALEMENT le code avant de le proposer — flux complet**
- **JAMAIS mélanger données Collections et données Recettes** — ce sont deux sources distinctes dans le Sheet
- **JAMAIS proposer du code directement** — toujours décrire la solution et attendre un OK explicite avant de donner le moindre bloc de code
- **JAMAIS utiliser `appelAdminAPI`** — ça n'existe pas. Utiliser `appelAPI` (GET) ou `appelAPIPost` (POST/écriture)
- **JAMAIS oublier `&t=${Date.now()}`** sur les appels API publics pour éviter le cache
- **JAMAIS vider le cache navigateur comme solution** — ça ne règle rien
- **JAMAIS faire un remplacement de `:root`** sans conserver les couleurs de base en tête de liste
- **TOUJOURS vérifier les accolades fermantes** dans les règles CSS avant de soumettre — une règle non fermée casse tout le CSS qui suit

---

## PROJET

Univers Caresse — savonnerie artisanale de Chantal Mondor.

**Repo GitHub :** `universcaresse/univers-caresse`
**URL publique :** https://universcaresse.github.io/univers-caresse/
**URL admin :** https://universcaresse.github.io/univers-caresse/admin/
**Apps Script URL :** https://script.google.com/macros/s/AKfycbyDbcy6kBKcTWtj2B0kLfAioy9f2ShI0UtMPP1wg2K-xKUUDdIDONH_rbB_RCzu7lyhVw/exec
**Google Sheet ID :** 16Syw5XypiHauOMpuAu-bWfIMMnMObn9avqoSEYjaNu0
**Courriel :** universcaresse@outlook.com

---

## TYPOGRAPHIE — CRITIQUE

| Usage | Fonte |
|-------|-------|
| Titres | Playfair Display |
| Tagline / signature | Birthstone Regular |
| Texte courant | DM Sans Light |
| Noms produits | DM Sans Medium |

---

## PALETTE — CRITIQUE
```css
--primary:      #5a8a3a
--primary-dark: #4a6e2e
--accent:       #d4a445
--danger:       #c44536
--blanc:        #f9f7f4
--beige:        #e8dcc8
--gris:         #8b8680
--gris-fonce:   #3d3b39
--logo:         #333333
```

### Variantes de transparence — dans `:root`
Toutes les couleurs ont des variantes nommées `--couleur-XX` où XX = opacité en centièmes.
- **--primary** : 04, 05, 06, 08, 10, 12, 15, 16, 18, 20, 30, 40, 50, 60, 70, 75, 80, 85, 88, 90
- **--danger** : 06, 08, 10, 15, 16, 20, 30, 40, 50, 60, 70, 75, 80, 85, 88, 90
- **--accent** : 08, 10, 12, 15, 20, 30, 40, 50, 60, 70, 75, 80, 85, 88, 90
- **--beige** : 08, 10, 15, 20, 30, 40, 50, 60, 70, 75, 80, 85, 88, 90
- **--blanc** : 15, 20, 30, 40, 50, 60, 70, 75, 80, 85, 88, 90, 92
- **--blanc-pur** : 15, 45, 50, 60, 65, 70, 75, 80, 85, 88, 90
- **--gris** : 08, 10, 15, 20, 30, 40, 50, 60, 70, 75, 80, 85, 88, 90
- **--gris-fonce** : 08, 10, 15, 20, 30, 40, 50, 60, 70, 75, 80, 85, 88, 90
- **--noir** : 08, 10, 15, 20, 30, 40, 50, 60, 70, 75, 80, 85, 88, 90

**Règle :** Toujours utiliser `var(--primary-08)` etc. — jamais `rgba(90,138,58,0.08)` directement dans le CSS.
**Règle :** `--logo: #333333` réservé aux éléments de marque — `--gris-fonce: #3d3b39` pour les textes courants.

---

## IMAGES

- `Images/Logofinal.png` — hero public + accueil admin
- `Images/plume.png` — favicon toutes les pages
- `Images/savonnerie.png` — section qui-sommes-nous
- `Images/fond.png` — background hero-right public + tuiles admin accueil + footer
- `Images/fondw.png` — n'existe pas, utiliser `fond.png`
- Photos produits : Cloudinary — cloud `dfasrauyy`, preset `univers-caresse`
- `image_url` dans Sheet (onglet Recettes, col R) = URL Cloudinary complète
- `photo_url` dans Sheet (onglet Collections, col I) = URL Cloudinary complète

---

## ARCHITECTURE

- **Hébergement :** GitHub Pages
- **Backend :** Google Apps Script (Sheet, calculs, JSON, courriel)
- **Frontend :** HTML/CSS/JS vanilla
- **Auth :** `sessionStorage` → redirect `/univers-caresse/admin/`
- **Cache :** `&t=${Date.now()}` sur tous les appels API publics
- **SPA public :** navigation par hash `#accueil`, `#catalogue`, `#bon-a-savoir`, `#contact`
- **GitHub Desktop** installé et configuré ✅

### Structure du repo
```
univers-caresse/
├── index.html              ✅ SPA public — 4 sections (accueil inclut qui-sommes-nous)
├── admin/
│   ├── index.html          ✅ Admin — 7 sections + Contenu du site
│   └── login.html          ✅ Page de connexion autonome
├── css/
│   └── style.css           ✅ SOURCE UNIQUE — public + admin, zéro doublon
├── js/
│   ├── main.js             ✅ CONFIG, SPA, session, API, catalogue, contact, collections, chargerContenu()
│   └── admin.js            ✅ Toute la logique admin + chargerContenuSite() + sauvegarderContenuSite()
└── Images/
    ├── plume.png / Logofinal.png / savonnerie.png / fond.png ✅
    └── produits/            ☐ À uploader
```

**`admin.css` supprimé — tout est dans `style.css`**
**Nav admin :** dropdowns desktop (≥1024px) — Création, Achats, Production, Système. Burger mobile (<1024px).

---

## Variables CSS utiles
- `--padding-page: 80px` — espacement desktop
- `--padding-mobile: 20px` — espacement mobile
- `--nav-h: 72px` — hauteur nav fixe

---

## CONNEXION ADMIN

- `validerConnexion()` dans `main.js`
- Succès → `sessionStorage.setItem('uc_admin', 'true')` + redirect `/univers-caresse/admin/`
- `validerConnexionAdmin()` dans `admin.js` — pour le formulaire dans `admin/index.html`
- `#ecran-connexion` dans `admin/index.html` : doit avoir la classe `cache` par défaut dans le HTML
- `login.html` : page autonome de connexion — redirige vers `/univers-caresse/admin/` si session active

---

## CONTENU DYNAMIQUE — ONGLET `Contenu` ✅

### Architecture
- Onglet `Contenu` dans le Sheet — colonnes `cle` / `valeur`
- `getContenu()` dans `Code.gs` — action GET `getContenu`
- `updateContenu(data)` dans `Code.gs` — action POST `updateContenu`
- `chargerContenu()` dans `main.js` — appelée au `DOMContentLoaded`, avec `&t=${Date.now()}`
- `chargerContenuSite()` + `sauvegarderContenuSite()` dans `admin.js`
- Section **Contenu du site** dans `admin/index.html` → Système → Contenu du site

### Règle importante
- `index.html` public : **zéro texte en dur** — tous les éléments ont un `id` et sont vides
- L'injection se fait entièrement via `chargerContenu()` au chargement
- `.form-panel` dans la section admin nécessite la classe `.visible` pour s'afficher — mais PAS dans le HTML directement, seulement via JS ou dans `#corps-contenu-site` qui est caché par `display:none`

### Clés gérées
- Accueil hero : `accueil_eyebrow`, `accueil_cta`, `accueil_stat_valeur`, `accueil_stat_label`
- Qui sommes-nous : `qui_eyebrow`, `qui_titre`, `qui_titre_em`, `qui_texte`, `qui_signature_nom`, `qui_signature_titre`
- Section texte : `section_texte_p1`, `section_texte_p2`, `section_texte_p3`
- Valeurs : `valeur_01_titre/desc` → `valeur_04_titre/desc`
- Citation : `citation_texte`, `citation_source`
- Bon à savoir engagements : `bas_engagement_01_titre/texte` → `bas_engagement_04_titre/texte`
- Bon à savoir autres : `bas_allergenes`, `bas_conservation_titre/texte`, `bas_cure_titre/texte`, `bas_usage_titre/texte`, `bas_commande_titre/texte`, `bas_demande_titre/texte`

---

## NOTES SECTION ACCUEIL / QUI SOMMES-NOUS

- Animations scroll via `IntersectionObserver` (`initScrollAnimations()` dans `main.js`)
  - `.fade-in` : transition 2s ease, `translateY(24px)` → 0
  - `.mosaic-item` : couleur visible dès le départ, `.mosaic-soap-label` apparaît en 0.8s
- Citation : `&nbsp;»` dans `.citation-guillemet` pour empêcher coupure de ligne
- Nav publique : liens ADMIN et DÉCONNEXION supprimés, liens à droite via `margin-left: auto`

---

## ACCUEIL ADMIN — TUILES ✅

- `.accueil-droite` : grille 2×2, `gap: 16px`, `padding: 16px`, `background: url('../Images/fond.png')`
- Tuiles semi-transparentes par-dessus le fond :
  - `.accueil-tuile-collections` : `var(--primary-70)`
  - `.accueil-tuile-recettes` : `var(--accent-70)`
  - `.accueil-tuile-facture` : `var(--gris-70)`
  - `.accueil-tuile-inventaire` : `var(--gris-fonce-70)`

---

## FOOTER ✅

- `background: url('../Images/fond.png')` + overlay `::before` avec `var(--gris-fonce-88)`
- `footer > *` : `position: relative; z-index: 1` pour que le contenu passe par-dessus l'overlay
- Couleur texte : `var(--blanc-pur-75)`

---

## CATALOGUE PUBLIC ✅ (partiel)

### Entête collection
- Priorité affichage : photo (`photo_url` de l'onglet Collections) → couleur hex (`couleur_hex` de l'onglet Collections) → rouge fallback `#c44536`
- `image_collection` transmis dans chaque produit depuis `getCataloguePublic()`
- Le champ `image_url` des recettes est réservé à la photo du produit individuel — ne pas mélanger

### Modal produit
- Visuel split : `.modal-visuel-hex` (1/3 couleur) + `.modal-visuel-photo` (2/3 photo)
- Si pas de photo : `.modal-visuel-hex` masqué, `.modal-visuel-photo` affiche la couleur hex en plein
- Bouton fermer `.modal-fermer` : cercle blanc 32px, centré, z-index 10
- `grid-template-columns: 1fr 2fr 1fr` desktop, colonne sur mobile
- Mobile : `.modal-visuel-hex` min-height 80px, `.modal-visuel-photo` min-height 220px
- Photo = `image_url` de la recette (URL Cloudinary complète — pas de préfixe `Images/produits/`)

---

## MODULES ADMIN — ÉTAT

### Collections ✅
- Cartes visuelles : dégradé 2 couleurs (couleur_hex du Sheet + assombrirCouleur), lignes listées en tags, titre en bas
- Clic carte → fiche consultation (panneau)
- Fiche consultation : infos collection, liste lignes, bouton Modifier collection, bouton + Ajouter une ligne, bouton Fermer
- Formulaire 2 modes : **Mode Collection** (rang dynamique, nom, slogan, desc, couleur_hex avec aperçu visuel, photo Cloudinary dossier `collections`) et **Mode Ligne** (collection readonly, nom ligne, format, desc, couleur_hex, photo Cloudinary dossier `lignes`, ingrédients de base)
- Toggle entre modes via bouton dans l'en-tête du formulaire
- `modifierCollection()` : preview photo rechargée à l'ouverture du formulaire ✅
- `updateCollectionItem` propage `couleur_hex` et `photo_url` à toutes les rangées de la même collection ✅

### Recettes ✅
- Filtres cascade Collection → Ligne → grille
- Filtre statut (Tous / Public / Test), badge statut sur cartes
- Formulaire 4 colonnes, couleur hex dynamique, Cloudinary ✅
- **À faire :** section ingrédients HTML + sauvegarde (Note 13), mode consultation par défaut (Note 14)

### Factures ✅ (partiel)
- Wizard 3 étapes, `factureActive` persiste jusqu'à finalisation
- **Bug prioritaire :** produits "undefined" dans détail facture
- **À faire :** rangée cliquable, fiche complète, statut, filtre ingrédient, mobile
- **NOTE :** `admin.js` contient une ancienne architecture de factures (fonctions `creerFacture`, `ajouterProduit`, `afficherProduits`, `reinitialiserNouvelleFacture` lignes ~726-904) — code mort à nettoyer

### Densités
- **À faire :** champ `marge_perte_pct`, rangée cliquable

### Contenu du site ✅
- Section dans Système → Contenu du site
- Champs éditables pour toutes les sections publiques (Accueil, Qui sommes-nous, Bon à savoir)
- Sauvegarde via `appelAPIPost('updateContenu', { contenu })`
- Chargement via `appelAPI('getContenu', { t: Date.now() })`

---

## CAHIER DE CHARGES — SCAN / COÛT DE REVIENT
```
Scan → Facture → Finalisation → Inventaire → Recette → Coût de revient
Coût ingrédient = quantite_g × prix_par_g_reel × (1 + marge_perte_%)
```
- Librairie : QuaggaJS, confirmation 3 détections, fallback manuel

---

## RÈGLES D'INTERFACE

- Champs numériques : `type="text" inputmode="numeric"`
- Noms en MAJUSCULES partout (collections, lignes, noms de savons)
- Zéro placeholder dans les champs
- Carte/rangée = le bouton (pas de boutons superposés)
- Fiche en consultation par défaut → bouton Modifier bascule édition

| Bouton | Action |
|--------|--------|
| Primary (vert) | Enregistrer / Confirmer |
| Secondary (vert pâle) | Annuler / Fermer |
| Edit (vert pâle) | Modifier |
| Danger (rouge) | Supprimer |
| Or | Finaliser |

---

## COLLECTIONS EXISTANTES

| Collection | Slogan |
|-----------|--------|
| Saponica | Simplement la nature qui prend soin de vous |
| Petit Nuage | Simplement la nature qui dorlote vos tout-petits |
| Caprin | Simplement la nature et la douceur de la chèvre |
| Émolia | Simplement la nature dédiée à votre bien-être |
| Épure | Simplement la nature qui prend soin de vos mains |
| Kérys | Simplement la nature qui dorlotte vos cheveux |
| Casa | Simplement la nature qui prend soin de votre maison |
| Lumina | Simplement la nature en lumière parfumée |
| Anima | Simplement la nature pour pattes et museaux |
| Lui | Simplement la nature au masculin |

---

## 🔴 À FAIRE — PRIORITÉS

### Admin
- [ ] **Bug : produits "undefined" dans détail facture**
- [ ] Recettes : section ingrédients formulaire + sauvegarde (Note 13)
- [ ] Recettes : mode consultation par défaut (Note 14)
- [ ] Densités : champ marge_perte_pct, rangée cliquable
- [ ] Factures : rangée cliquable, fiche complète, statut, filtre, mobile
- [ ] Nettoyer code mort factures dans `admin.js` (lignes ~726-904)
- [ ] Tuiles accueil : première tuile span 2 rangées comme mosaïque publique
- [ ] Icône Collections : SVG option 14 du fichier icones-collections.html
- [ ] "Bonjour Chantal" + stats : plus de largeur partout
- [ ] Nav mobile : supprimer "Site public" et "Déconnexion" de la barre → dans burger
- [ ] Retirer placeholder "Mot de passe" dans `#input-mdp-admin` (admin/index.html ligne ~1000)
- [ ] Corriger "Entrerrr" → "Entrer" dans le bouton `validerConnexionAdmin`
- [ ] Migrer fonctions `carteProduit` et `ouvrirModal` du script inline `index.html` public vers `main.js`

### Site public
- [ ] Formulaire contact : `envoyerContact` dans Code.gs avec `MailApp.sendEmail()`
- [ ] Note 48 : Plume = bouton retour accueil
- [ ] Note 54 : Titres collections / lignes / noms en UPPERCASE partout
- [ ] Note 55 : Casse insensible dans `COULEURS_COLLECTIONS`
- [ ] Note 60 : Photo ambiance collection dans catalogue (fallback = dégradé) — entête collection ✅ partiel
- [ ] Note 61 : Tuiles collections accueil — dégradé 2 couleurs (pas de photo)
- [ ] Nav mobile : supprimer barre fixe en haut, remplacer par burger flottant
- [ ] Remplacer les `rgba` hardcodées dans `style.css` par les variables `--couleur-XX` du `:root`

### Futur
- [ ] Nom de domaine `universcaresse.ca` (Webnames.ca recommandé)
- [ ] Amortissement équipements dans coût de revient
- [ ] Scraping PureArome + Arbressence
- [ ] Scan QuaggaJS
- [ ] Confection
- [ ] Corrections inventaire (ajustement manuel)
- [ ] PWA Dionysos (caméra bloquée Google iframe)
- [ ] Structure 4 niveaux : Collection → Ligne → Variante → Recette

---

## ✅ COMPLÉTÉ — 6 mars 2026

- Repo recréé sur GitHub après perte — `universcaresse/univers-caresse` ✅
- GitHub Desktop installé et configuré ✅
- URL admin corrigée dans `main.js` : `/univers-caresse/admin/` ✅
- GitHub Pages activé sur branch `main` ✅
- Bug `</div>` en trop ligne 317 `admin/index.html` corrigé ✅
- `Univers Caresse1` → `Univers Caresse` dans titre `admin/index.html` ✅
- Lignes de produits dans cartes collections repositionnées en haut ✅
- `window.scrollTo(0,0)` dans `ouvrirFicheCollection()` ✅
- Boutons fiche collection déplacés en haut du panneau avec séparateur ✅
- `updateCollectionItem` dans `Code.gs` — propager couleur_hex et photo_url aux autres rangées ✅
- `sauvegarderCollection()` — mode collection n'envoie plus ligne/format/description_ligne ✅
- Ancienne `sauvegarderCollection` supprimée de `Code.gs` (doublon) ✅
- `.photo-preview` 120×120px dans `style.css` ✅
- Toast de confirmation centré ✅
- `login.html` : btn-primary, logo 280px ✅

## ✅ COMPLÉTÉ — 7 mars 2026 (session 1)

- Animations scroll `initScrollAnimations()` dans `main.js` — IntersectionObserver ✅
- `.fade-in` transition 2s ease via classe `.visible` ✅
- Mosaïque hero : couleur visible, texte apparaît en 0.8s ✅
- Citation `&nbsp;»` dans `.citation-guillemet` ✅
- Nav publique : lien ADMIN + bouton DÉCONNEXION supprimés ✅
- Section "Qui sommes-nous" fusionnée dans `section-accueil` ✅
- `getCataloguePublic()` enrichi avec `couleur_hex` et `photo_url` de l'onglet Collections ✅
- Couleur fallback manquante → `#c44536` (rouge debug) dans `Code.gs` et `main.js` ✅
- `image_url` catalogue = URL Cloudinary complète (sans préfixe `Images/produits/`) ✅
- Modal produit : split `.modal-visuel-hex` (1/3) + `.modal-visuel-photo` (2/3) ✅
- Modal produit : fallback plein couleur si pas de photo ✅
- `.modal-fermer` : cercle blanc 32px, centré, z-index 10 ✅
- `modifierCollection()` admin : preview photo rechargée à l'ouverture ✅

## ✅ COMPLÉTÉ — 7 mars 2026 (session 2)

- Onglet `Contenu` créé dans le Sheet via `initialiserContenu()` ✅
- `getContenu()` ajouté dans `Code.gs` + branché dans `doGet` ✅
- `updateContenu()` ajouté dans `Code.gs` + branché dans `doPost` ✅
- `chargerContenu()` ajouté dans `main.js` — appelée au `DOMContentLoaded` avec cache-busting ✅
- `index.html` public : tous les textes en dur vidés — injection 100% via API ✅
- `index.html` public : tous les `id` de contenu dynamique ajoutés ✅
- Section **Contenu du site** ajoutée dans `admin/index.html` (Système) ✅
- `chargerContenuSite()` + `sauvegarderContenuSite()` ajoutés dans `admin.js` ✅
- `.form-panel.visible` utilisé pour afficher les panneaux de la section ✅
- `validerConnexionAdmin()` ajoutée dans `admin.js` ✅

## ✅ COMPLÉTÉ — 8 mars 2026 (session 4)

- Fiche collection : bouton "Fermer" dans le bandeau supprimé ✅
- Fiche collection : boutons Modifier / Ajouter une ligne / Fermer déplacés dans le bandeau ✅
- Fiche collection : couleur dégradé retirée du bandeau — fond neutre ✅
- Fiche collection : clic "Modifier" ferme la fiche ET ouvre le formulaire ✅
- Fiche collection : "+ Ajouter une ligne" branché sur `ouvrirFormCollectionPour` + `basculerModeFormCollection` ✅
- Fiche collection : texte couleur bandeau corrigé → `var(--gris-fonce)` et `var(--gris)` ✅
- `item.ligne.toUpperCase()` → `String(item.ligne || '').toUpperCase()` dans `chargerCollections` ✅
- `infoCol` en mode ajout ligne : cherche première rangée de la collection (pas seulement `!i.ligne`) ✅
- Modal produit public : apostrophes cassaient l'`onclick` → encodage `btoa/atob` + `data-produit` ✅
- `ouvrirModalFromCard(el)` ajoutée dans `main.js` — décode `data-produit` et appelle `ouvrirModal` ✅
- `white-space: pre-line` sur `p` dans `style.css` — paragraphes respectés sur le public ✅

## ✅ COMPLÉTÉ — 8 mars 2026 (session 3)

- Bug `</div></div>` en trop dans section Contenu du site — panneaux visibles sur toutes les pages ✅
- `#ecran-connexion` : classe `cache` ajoutée par défaut dans le HTML ✅
- Bug double point `..ecran-connexion` dans `style.css` corrigé → `.ecran-connexion` ✅
- Bug accolade manquante `.toast.toast-erreur` dans `style.css` — cassait tout le CSS qui suit ✅
- `:root` refondé — couleurs de base + variantes de transparence pour toutes les couleurs ✅
- Tuiles admin accueil : fond `fond.png` + couleurs `rgba` via variables `--couleur-70` ✅
- Footer : fond `fond.png` + overlay `::before` `var(--gris-fonce-88)` + texte `var(--blanc-pur-75)` ✅

---

## ⚠️ NOTES IMPORTANTES CODE.GS

- `sauvegarderCollection` N'APPARTIENT PAS à `Code.gs` — c'est une fonction `admin.js`
- Toujours vérifier les doublons de fonctions avant de modifier `Code.gs`
- Après chaque modification de `Code.gs` : redéployer en nouvelle version
- L'URL du déploiement ne change pas entre les versions
- `updateContenu` est dans `doPost` — pas dans `doGet`
- Appels lecture → `appelAPI` (GET) / Appels écriture → `appelAPIPost` (POST)

---

*Univers Caresse — Chantal Mondor — Confidentiel*
*Mis à jour : 8 mars 2026 (session 4)*
