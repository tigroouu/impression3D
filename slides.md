---
theme: seriph
background: https://source.unsplash.com/featured/?3d-printing
class: text-center
highlighter: shiki
lineNumbers: true
drawings:
  persist: false
transition: slide-left
title: L'Impression 3D - Du Prototype à la Révolution
---

# L'Impression 3D
## La fabrication additive au service de l'innovation

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer hover:bg-white hover:bg-opacity-10">
    Appuyez sur Espace pour commencer <carbon:arrow-right class="inline"/>
  </span>
</div>

---
layout: two-cols
transition: slide-up
---

# Sommaire

<Toc text-sm minDepth="1" maxDepth="2" />

---
transition: fade-out
---

## Qu'est-ce que l'impression 3D ?

L'impression 3D, ou **fabrication additive**, consiste à créer des objets réels par superposition de couches successives.

* **Soustraction (Traditionnel):** On part d'un bloc et on enlève de la matière (usinage).
* **Addition (3D):** On dépose uniquement la matière nécessaire.

> "L'impression 3D permet de passer du bit à l'atome en quelques heures."

---
layout: default
---

# Les Technologies d'Impression 3D

<div class="grid grid-cols-3 gap-6">

  <div v-click="1" class="bg-gray-800 p-6 rounded-2xl border-t-4 border-blue-500 shadow-xl text-center">
      <div class="text-5xl mb-4 text-blue-400">🧵</div>
      <h2 class="text-2xl font-bold mb-2">FDM / FFF</h2>
      <p class="text-sm text-gray-400 mb-4 italic text-center">Dépôt de filament plastique fondu à travers une buse.</p>
      <ul class="text-left text-sm space-y-2">
        <li class="text-green-400">✅ Économique et robuste</li>
        <li class="text-green-400">✅ Large choix de matériaux</li>
        <li class="text-red-400">❌ Couches visibles</li>
      </ul>
  </div>

  <div v-click="2" class="bg-gray-800 p-6 rounded-2xl border-t-4 border-purple-500 shadow-xl text-center">
      <div class="text-5xl mb-4 text-purple-400">🧪</div>
      <h2 class="text-2xl font-bold mb-2">SLA / MSLA</h2>
      <p class="text-sm text-gray-400 mb-4 italic text-center">Résine liquide durcie par laser UV</p>
      <ul class="text-left text-sm space-y-2">
        <li class="text-green-400">✅ Précision microscopique</li>
        <li class="text-green-400">✅ État de surface lisse</li>
        <li class="text-red-400">❌ Post-traitement salissant</li>
      </ul>
  </div>

  <div v-click="3" class="bg-gray-800 p-6 rounded-2xl border-t-4 border-orange-500 shadow-xl text-center">
      <div class="text-5xl mb-4 text-orange-400">🏜️</div>
      <h2 class="text-2xl font-bold mb-2">SLS</h2>
      <p class="text-sm text-gray-400 mb-4 italic text-center">Poudre (nylon/métal) fusionnée par laser</p>
      <ul class="text-left text-sm space-y-2">
        <li class="text-green-400">✅ Pas besoin de supports</li>
        <li class="text-green-400">✅ Pièces complexes / indus</li>
        <li class="text-red-400">❌ Coût très élevé</li>
      </ul>
  </div>

</div>

---
layout: default
---

# Workflow Standard de l'Impression 3D

<div class="flex items-center justify-center gap-2 mt-10">

  <div v-click="1" class="bg-gray-700/50 p-5 rounded-xl border border-gray-600 w-48 shadow-lg">
      <div class="text-4xl mb-3">📐</div>
      <div class="font-bold text-lg">1. Conception</div>
      <div class="text-sm text-gray-400">Modélisation CAO<br>(Fusion, Blender)</div>
    </div>

  <div v-click="2" class="text-2xl text-gray-500 flex-shrink-0">➔</div>

  <div v-click="2" class="bg-gray-700/50 p-5 rounded-xl border border-gray-600 w-48 shadow-lg">
      <div class="text-4xl mb-3">📤</div>
      <div class="font-bold text-lg">2. Export</div>
      <div class="text-sm text-gray-400">Fichier 3D<br>(.STL, .OBJ, .3MF)</div>
    </div>

  <div v-click="3" class="text-2xl text-gray-500 flex-shrink-0">➔</div>

  <div v-click="3" class="bg-gray-700/50 p-5 rounded-xl border border-gray-600 w-48 shadow-lg">
      <div class="text-4xl mb-3">🍰</div>
      <div class="font-bold text-lg">3. Slicing</div>
      <div class="text-sm text-gray-400">Découpe G-Code<br>(Prusa, Cura)</div>
    </div>

  <div v-click="4" class="text-2xl text-gray-500 flex-shrink-0">➔</div>

  <div v-click="4" class="bg-gray-700/50 p-5 rounded-xl border border-gray-600 w-48 shadow-lg">
      <div class="text-4xl mb-3">🖨️</div>
      <div class="font-bold text-lg">4. Impression</div>
      <div class="text-sm text-gray-400">Fabrication<br>(FDM / Résine)</div>
    </div>

</div>

---

# Outils de Modélisation

---

## 🏗️ Fusion 360 (Autodesk)
*Le standard industriel "Cloud-Native"*


**Description :**
Solution CAO/FAO professionnelle tout-en-un, idéale pour concevoir des mécanismes complexes avec un historique de construction.

<div class="grid grid-cols-2 gap-4">
<div>

**Points Forts :**
- ✅ **Paramétrique & Historique** : Modifiez une cote au début de votre projet, tout le reste s'adapte.
- ✅ **Tout-en-un** : Modélisation, rendu, simulation (stress test) et FAO (usinage).
- ✅ **Courbe d'apprentissage** : Plus intuitive que les logiciels CAO classiques.
- ✅ **Gratuit pour les amateurs** (sous conditions de revenus).
</div>
<div>

**Points Faibles :**
- ❌ **Modèle Cloud** : Connexion internet quasi-obligatoire pour enregistrer.
- ❌ **Limitations de la version gratuite** : Nombre de documents actifs limité à 10.
- ❌ **Logiciel Propriétaire** : Vos fichiers dépendent des serveurs d'Autodesk.
</div>
</div>

---

## 🎨 Blender
*La liberté artistique absolue*

**Description :**
Logiciel de création 3D polyvalent, parfait pour le design organique, la sculpture numérique et le rendu visuel de haute qualité.

<div class="grid grid-cols-2 gap-4">
<div>

**Points Forts :**
- ✅ **Open Source & Gratuit** : Pas d'abonnement, pas de limites, pour toujours.
- ✅ **Modélisation Organique** : Imbattable pour les figurines, les visages ou les textures.
- ✅ **Sculpting 3D** : Permet de "pétrir" la matière numérique comme de l'argile.
- ✅ **Communauté immense** : Des milliers de tutoriels gratuits disponibles.
</div>
<div>

**Points Faibles :**
- ❌ **Précision dimensionnelle** : Plus difficile de faire de la mécanique pure (pas de CAO native).
- ❌ **Courbe d'apprentissage** : Interface dense qui peut effrayer au début.
- ❌ **Pas d'historique de fonctions** : Difficile de revenir en arrière sur une dimension précise.
</div>
</div>
---

## ⚙️ FreeCAD
*La CAO 100% Libre et locale*

**Description :**
Logiciel de conception paramétrique open-source, idéal pour l'ingénierie sans abonnement.

<div class="grid grid-cols-2 gap-8 mt-4">
<div>

**Points Forts :**
- ✅ **Souveraineté des données** : Vos fichiers restent sur votre PC, aucun cloud requis.
- ✅ **Extensible** : Système de "Workbenches" (ateliers) très puissants pour l'architecture, la robotique, etc.
- ✅ **Paramétrique réel** : Gestion via tableur (Spreadsheet) pour des designs ultra-précis.
- ✅ **Léger** : Tourne sur des configurations modestes.
</div>
<div>

**Points Faibles :**
- ❌ **Interface austère** : Design daté et ergonomie parfois frustrante.
- ❌ **Bugs historiques** : Le fameux "Topological Naming Issue" (qui peut casser votre modèle en cas de modification profonde).
- ❌ **Apprentissage rude** : Demande de la rigueur et de la patience.
</div>
</div>
---

## Outil IA

---

# L'impresion résine

---
## Fonctionnement de l'impression
---

## Type de résine

---

## Outil de découpage

---

## Timelapse

---

# L'impresion filaire

---

## Fonctionnement de l'impression

---
layout: default
---

# Guide des Matériaux (FDM)
### Propriétés, Températures et Applications Réelles

<div style="display: flex; flex-direction: column; gap: 8px; margin-top: 5px;">

  <div v-click="1" style="display: flex; align-items: center; background: rgba(34, 197, 94, 0.1); border: 1px solid #22c55e; border-radius: 10px; padding: 8px 20px;">
    <span style="font-size: 2.2rem; margin-right: 20px;">🌱</span>
    <div style="flex-grow: 1;">
      <h3 style="color: #4ade80; margin: 0; font-size: 1.1rem;">PLA (Acide Polylactique)</h3>
      <p style="margin: 0; font-size: 0.8rem;"><b>Usages :</b> Figurines, prototypes rapides, maquettes d'architecture, boîtes de rangement.</p>
    </div>
    <div style="font-family: monospace; font-size: 0.75rem; text-align: right; border-left: 1px solid #22c55e; padding-left: 15px; min-width: 140px;">
      Buse : <b>190-220°C</b><br>Plateau : <b>40-60°C</b>
    </div>
  </div>

  <div v-click="2" style="display: flex; align-items: center; background: rgba(59, 130, 246, 0.1); border: 1px solid #3b82f6; border-radius: 10px; padding: 8px 20px;">
    <span style="font-size: 2.2rem; margin-right: 20px;">💧</span>
    <div style="flex-grow: 1;">
      <h3 style="color: #60a5fa; margin: 0; font-size: 1.1rem;">PETG (Polyéthylène)</h3>
      <p style="margin: 0; font-size: 0.8rem;"><b>Usages :</b> Supports de caméras, pièces mécaniques, jardinières (résistant UV), clips de fixation.</p>
    </div>
    <div style="font-family: monospace; font-size: 0.75rem; text-align: right; border-left: 1px solid #3b82f6; padding-left: 15px; min-width: 140px;">
      Buse : <b>230-250°C</b><br>Plateau : <b>70-85°C</b>
    </div>
  </div>

  <div v-click="3" style="display: flex; align-items: center; background: rgba(239, 68, 68, 0.1); border: 1px solid #ef4444; border-radius: 10px; padding: 8px 20px;">
    <span style="font-size: 2.2rem; margin-right: 20px;">🔥</span>
    <div style="flex-grow: 1;">
      <h3 style="color: #f87171; margin: 0; font-size: 1.1rem;">ABS / ASA (Technique)</h3>
      <p style="margin: 0; font-size: 0.8rem;"><b>Usages :</b> Pièces moteur, coques de drones, mobilier de jardin (ASA), outillage résistant à la chaleur.</p>
    </div>
    <div style="font-family: monospace; font-size: 0.75rem; text-align: right; border-left: 1px solid #ef4444; padding-left: 15px; min-width: 140px;">
      Buse : <b>240-270°C</b><br>Plateau : <b>90-110°C</b>
    </div>
  </div>

  <div v-click="4" style="display: flex; align-items: center; background: rgba(249, 115, 22, 0.1); border: 1px solid #f97316; border-radius: 10px; padding: 8px 20px;">
    <span style="font-size: 2.2rem; margin-right: 20px;">👟</span>
    <div style="flex-grow: 1;">
      <h3 style="color: #fb923c; margin: 0; font-size: 1.1rem;">TPU (Polyuréthane)</h3>
      <p style="margin: 0; font-size: 0.8rem;"><b>Usages :</b> Pneus de modélisme, joints d'étanchéité, coques de téléphone, semelles de chaussures.</p>
    </div>
    <div style="font-family: monospace; font-size: 0.75rem; text-align: right; border-left: 1px solid #f97316; padding-left: 15px; min-width: 140px;">
      Buse : <b>210-235°C</b><br>Plateau : <b>0-50°C</b>
    </div>
  </div>

  <div v-click="5" style="display: flex; align-items: center; background: rgba(168, 85, 247, 0.08); border: 1px solid #ef4444; border-radius: 10px; padding: 8px 20px;">
    <span style="font-size: 2.2rem; margin-right: 20px;">⚙️</span>
    <div style="flex-grow: 1;">
      <h3 style="color: #c084fc; margin: 0; font-size: 1.1rem;">Nylon (Polyamide)</h3>
      <p style="margin: 0; font-size: 0.75rem;"><b>Usages :</b> Engrenages, charnières, pièces à forte friction.</p>
    </div>
    <div style="font-family: monospace; font-size: 0.75rem; text-align: right; border-left: 1px solid #a855f7; padding-left: 15px; min-width: 140px;">
      Buse : <b>240-270°C</b><br>Plateau : <b>70-100°C</b>
    </div>
  </div>

</div>

---

## Outil de découpage

---

## Timelapse

---

# H2C, l'imprimante IPPON

---

## Comment y acceder
Avant tout il faut installer le logiciel Bambu Lab Studio

Une fois le logiciel pret indiquez les informations suivantes
login : imprimante3D@ippon.Fr
mot de passe : Ippon2026!

Un code sera alors envoyé à l'adresse email ci dessous, merci de prendre contact avec Pascal, Jolan ou moi-meme pour obtenir ce code

---

## Que peut on imprimer et quand?
Avant tout priorité au marketing.

On peut ce que l'on souhaite dans la mesure du raisonnable. 
Pas d'impression trop longue, trop complexe ou tendancieuse. 
On peut tester des choses mais pas n'importe quoi

Si ils ont besoin de faire un test ils doivent avoir accès a l'imprimante. 
En dehors de ca nous imprimons durant les heures de travail 8h - 19h et seulement en jour ouvré (lundi au vendredi) tout simplement pour eviter les risques d'incendie

---

# Bibliotheque 3D

---

## 🏛️ Thingiverse (Ultimaker)
*L'archive historique de l'impression 3D*

<div class="grid grid-cols-2 gap-4">
<div>

**Description :**
La plus ancienne et vaste bibliothèque de fichiers STL au monde. Un passage obligé pour tout maker.

**Points Forts :**
- ✅ **Base de données colossale** (+2,5M modèles).
- ✅ **100% Gratuit** : Pas de modèles payants cachés.
- ✅ **Standard** : Tous les logiciels tiers s'y connectent.

</div>
<div>

**Points Faibles :**
- ❌ **Interface vieillissante** et moteur de recherche capricieux.
- ❌ **Qualité inégale** : Beaucoup de fichiers corrompus ou non testés.
- ❌ **Passivité** : Peu d'incitations pour les créateurs.

</div>
</div>

---

## 🏆 Printables (Prusa Research)
*L'excellence communautaire et qualitative*

**Description :**
Lancée par Prusa, cette plateforme mise sur la qualité des modèles et l'engagement des utilisateurs.

<div class="grid grid-cols-2 gap-4">
<div>

**Points Forts :**
- ✅ **Système de récompenses** : Gagnez du filament gratuit via les *Prusameters*.
- ✅ **Concours thématiques** : Très stimulants pour la création.
- ✅ **Fichiers de qualité** : Documentation souvent très complète.

</div>
<div>

**Points Faibles :**
- ❌ **Modération stricte** : Plus difficile de poster du contenu "rapide".
- ❌ **Moins de volume** que Thingiverse (mais mieux trié).

</div>
</div>

---

## ⚡ MakerWorld (Bambu Lab)
*L'impression en un clic (Cloud-Native)*

**Description :**
La plateforme qui a cassé les codes en intégrant le "One-Click Print" via l'application Bambu Handy.

<div class="grid grid-cols-2 gap-4">
<div>

**Points Forts :**
- ✅ **Intégration matérielle** : Paramètres d'impression pré-réglés.
- ✅ **Économie généreuse** : Système de *Boosts* et points très rentables.
- ✅ **Aperçus 3D fluides** : Technologie web très moderne.

</div>
<div>

**Points Faibles :**
- ❌ **Enclos propriétaire** : Très optimisé pour Bambu Lab, moins pour les autres.
- ❌ **Contenu "Fast-Print"** : Beaucoup de gadgets inutiles au détriment de l'ingénierie.

</div>
</div>

---

## 🚀 MakerOnline (Anycubic)
*L'outsider en pleine ascension*

**Description :**
La réponse d'Anycubic pour centraliser sa communauté et offrir des services cloud similaires à ses concurrents.

<div class="grid grid-cols-2 gap-4">
<div>

**Points Forts :**
- ✅ **Forte croissance** : Beaucoup de nouveaux modèles chaque jour.
- ✅ **Événements** : Nombreux concours avec des imprimantes à gagner.
- ✅ **Simplicité** : Interface claire et facile à prendre en main.

</div>
<div>

**Points Faibles :**
- ❌ **Communauté plus restreinte** par rapport aux trois géants.
- ❌ **Doublons** : Beaucoup de modèles importés d'autres plateformes.

</div>
</div>
