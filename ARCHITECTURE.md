# Architecture — Forms

## Vue d’ensemble

**Forms** est une application web autonome contenue dans `forms.html`. Elle utilise HTML, CSS, JavaScript natif et Canvas 2D, sans bibliothèque externe.

## Interface

L’interface comprend :

- le titre **Forms** ;
- le bouton `FR / EN` ;
- le sélecteur de forme ;
- le Canvas de rendu ;
- le panneau de réglages dynamique ;
- le pied de page Eigrutel BD Academy.

## Formes

Identifiants internes :

```text
box
cylinder
sphere
cone
pyramid
```

Correspondances :

| Identifiant | Français | English |
|---|---|---|
| `box` | Boîte | Box |
| `cylinder` | Cylindre | Cylinder |
| `sphere` | Sphère | Sphere |
| `cone` | Cône | Cone |
| `pyramid` | Pyramide | Pyramid |

## État

L’objet `App` centralise le Canvas, la forme active, la langue, les valeurs par défaut, l’état courant des formes et les contrôles.

## Projection

Fonctions principales :

- `rad()` : degrés vers radians ;
- `rotate()` : rotations X/Y/Z ;
- `project()` : projection perspective ;
- `stageState()` : état de vue ;
- `canvasSize()` : adaptation du Canvas.

## Rendu

Chaque forme possède sa fonction :

```text
drawBox()
drawCylinder()
drawSphere()
drawCone()
drawPyramid()
```

## Interface dynamique

`buildUI()` reconstruit les réglages selon la forme active. `addRange()`, `addCheck()` et `card()` créent les commandes.

## Internationalisation

`I18N` contient les libellés français et anglais. Le français est la langue par défaut. Le changement de langue conserve la forme et les réglages actifs et ne recharge pas la page.

## Interactions

- Pointer Events pour souris, tactile et stylet ;
- glisser pour tourner ;
- molette pour zoomer ;
- double-clic pour réinitialiser ;
- clavier pour rotation, pose aléatoire et réinitialisation.

## Responsive

Deux colonnes sur écran large, puis Canvas et réglages empilés sous 880 px. Ajustements supplémentaires sous 600 px.

## Données et confidentialité

Aucun compte, aucune base distante, aucun envoi de données utilisateur.

## Arborescence

```text
eigrutel-forms/
├── index.html
├── forms.html
├── README.md
├── NOTICE.md
├── LICENSE.md
├── CHANGELOG.md
├── ARCHITECTURE.md
└── docs/
    └── images/
        └── README.md
```

## Version documentée

**Forms 1.0.0 — 9 août 2026**

Programme conçu et développé par **Simon Léturgie** dans le cadre d’**Eigrutel BD Academy**.
