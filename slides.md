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
layout: default
class: dark
---

# L'Impression 3D : C'est quoi ?
<p class="text-gray-400 text-xs italic">De l'idée à l'objet physique en quelques clics.</p>

<div class="grid grid-cols-2 gap-4 mt-4">
  
  <div v-click="1" class="bg-gray-800/50 p-4 rounded-xl border border-red-500/20 shadow-md">
    <div class="text-2xl mb-1 text-red-400"><carbon-cut /></div>
    <h2 class="text-lg font-bold text-red-400">Soustractif</h2>
    <p class="text-[13px] leading-tight text-gray-300">On <b>taille ou coupe</b> un bloc de matière. Génère beaucoup de déchets.</p>
    <p class="text-[11px] mt-2 text-gray-500 italic">Ex: Sculpture, Fraisage CNC.</p>
	<div class="mt-3 flex justify-center">
      <img src="https://www.gifsanimes.com/data/media/1816/sculpteur-image-animee-0015.gif" class="h-28 rounded-lg shadow-inner object-contain" alt="sculpture" />
    </div>
  </div>

  <div v-click="2" class="bg-gray-800/50 p-4 rounded-xl border border-green-500/20 shadow-md border-l-4">
    <div class="text-2xl mb-1 text-green-400"><carbon-add-alt /></div>
    <h2 class="text-lg font-bold text-green-400">Additif (3D)</h2>
    <p class="text-[13px] leading-tight text-gray-300">On <b>ajoute de la matière</b> couche par couche. Très peu de gaspillage.</p>
    <p class="text-[11px] mt-2 text-gray-500 italic">Ex: Dépôt de fil, Résine.</p>
	<div class="mt-3 flex justify-center">
      <img src="https://www.norck.fr/cdn/shop/files/Fused_Deposition_Modeling.gif?v=1670227182" class="h-28 rounded-lg shadow-inner object-contain" alt="3d printing" />
    </div>
  </div>

</div>

---
layout: default
---

# Un peu d'histoire... 🕰️
<p class="text-gray-400 text-xs mb-2 italic">Une technologie qui a mûri dans l'ombre en 3 dates.</p>

<div class="grid grid-cols-1 gap-3">

  <div v-click="1" class="bg-gray-800/60 p-3 rounded-xl border-l-4 border-blue-500 shadow-lg flex items-center gap-4">
    <div class="bg-blue-500/10 p-2 rounded-lg border border-blue-500/30 text-xl font-black text-blue-400 w-16 text-center">1984</div>
    <div>
      <h3 class="text-md font-bold text-blue-100 leading-none mb-1">Invention Française 🇫🇷 <span class="text-lg">🐓</span></h3>
      <p class="text-[13px] leading-tight text-gray-300">1er brevet déposé par 3 ingénieurs français. Abandonné car jugé <b>"sans avenir"</b> par leurs entreprises.</p>
    </div>
  </div>

  <div v-click="2" class="bg-gray-800/60 p-3 rounded-xl border-l-4 border-purple-500 shadow-lg flex items-center gap-4">
    <div class="bg-purple-500/10 p-2 rounded-lg border border-purple-500/30 text-xl font-black text-purple-400 w-16 text-center">1986</div>
    <div>
      <h3 class="text-md font-bold text-purple-100 leading-none mb-1">Chuck Hull (SLA)</h3>
      <p class="text-[13px] leading-tight text-gray-300">Brevète la <b>résine</b> aux USA et fonde <b>3D Systems</b>. C'est le début industriel de l'impression 3D.</p>
    </div>
  </div>

  <div v-click="3" class="bg-gray-800/60 p-3 rounded-xl border-l-4 border-orange-500 shadow-lg flex items-center gap-4">
    <div class="bg-orange-500/10 p-2 rounded-lg border border-orange-500/30 text-xl font-black text-orange-400 w-16 text-center">2005</div>
    <div>
      <h3 class="text-md font-bold text-orange-100 leading-none mb-1">Projet RepRap</h3>
      <p class="text-[13px] leading-tight text-gray-300">L'imprimante <b>auto-réplicante</b> et l'open-source. C'est ce qui a permis d'avoir des imprimantes chez nous.</p>
    </div>
  </div>

</div>

---
layout: default
---

# Le Projet RepRap : La Révolution 🧬
<p class="text-gray-400 text-sm mb-4 italic text-center">"Wealth without money" — Adrian Bowyer (2005)</p>

<div class="grid grid-cols-2 gap-6 mt-4">

  <div v-click="1" class="bg-gray-800/50 p-5 rounded-2xl border-t-4 border-orange-500 shadow-xl">
    <div class="flex items-center gap-3 mb-3 text-orange-400">
      <carbon-renew class="text-3xl" />
      <h2 class="text-xl font-bold text-white">L'Auto-Réplication</h2>
    </div>
    <p class="text-[14px] leading-relaxed text-gray-300">
      L'objectif était de créer une machine capable de <b>fabriquer ses propres pièces</b>. 
      <br><br>
      Si vous avez une RepRap, vous pouvez en "imprimer" une autre pour un ami. La technologie se diffuse comme un organisme biologique.
    </p>
  </div>

  <div v-click="2" class="bg-gray-800/50 p-5 rounded-2xl border-t-4 border-green-500 shadow-xl">
    <div class="flex items-center gap-3 mb-3 text-green-400">
      <carbon-network-4 class="text-3xl" />
      <h2 class="text-xl font-bold text-white">L'Héritage Open-Source</h2>
    </div>
    <ul class="text-[13px] space-y-2 text-gray-300">
      <li><b class="text-green-300">Démocratisation :</b> Passage de machines à 30 000€ à des kits à 200€.</li>
      <li><b class="text-green-300">Standardisation :</b> Naissance des logiciels (Marlin, Cura) et du format de filament 1.75mm.</li>
      <li><b class="text-green-300">Les Géants :</b> Sans RepRap, <b>Prusa</b> et <b>Creality</b> n'existeraient pas.</li>
    </ul>
  </div>

</div>

<div v-click="3" class="mt-8 p-4 bg-orange-900/10 border border-orange-500/20 rounded-xl text-center">
  <p class="text-sm text-orange-200">
    🚀 <b>En résumé :</b> C'est le passage de l'impression 3D "industrielle" à l'impression 3D "domestique".
  </p>
</div>

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
      <div class="text-sm text-black-400">Modélisation CAO<br>(Fusion, Blender)</div>
    </div>

  <div v-click="2" class="text-2xl text-gray-500 flex-shrink-0">➔</div>

  <div v-click="2" class="bg-gray-700/50 p-5 rounded-xl border border-gray-600 w-48 shadow-lg">
      <div class="text-4xl mb-3">📤</div>
      <div class="font-bold text-lg">2. Export</div>
      <div class="text-sm text-black-400">Fichier 3D<br>(.STL, .OBJ, .3MF)</div>
    </div>

  <div v-click="3" class="text-2xl text-gray-500 flex-shrink-0">➔</div>

  <div v-click="3" class="bg-gray-700/50 p-5 rounded-xl border border-gray-600 w-48 shadow-lg">
      <div class="text-4xl mb-3">🍰</div>
      <div class="font-bold text-lg">3. Slicing</div>
      <div class="text-sm text-black-400">Découpe G-Code<br>(Prusa, Cura)</div>
    </div>

  <div v-click="4" class="text-2xl text-gray-500 flex-shrink-0">➔</div>

  <div v-click="4" class="bg-gray-700/50 p-5 rounded-xl border border-gray-600 w-48 shadow-lg">
      <div class="text-4xl mb-3">🖨️</div>
      <div class="font-bold text-lg">4. Impression</div>
      <div class="text-sm text-black-400">Fabrication<br>(FDM / Résine)</div>
    </div>

</div>

---
layout: default
---

# Outils de Modélisation

<div class="grid grid-cols-5 items-center mt-10">

  <div v-click="1" class="text-center">
    <div class="bg-gray-700/30 p-4 rounded-xl border border-white/10">
      <img src="/assets/images/concept_2d.png" class="h-50 mx-auto object-contain" />
    </div>
    <p class="mt-2 text-blue-400 font-bold">1. Design 2D Initial</p>
  </div>

  <div v-click="2" class="text-center text-5xl text-gray-500 animate-pulse">
    ➔
  </div>

  <div v-click="3" class="text-center">
    <div class="bg-gray-700/30 p-4 rounded-xl border border-white/10">
      <img src="/assets/images/esquisse.png" class="h-50 mx-auto object-contain" />
    </div>
    <p class="mt-2 text-purple-400 font-bold">2. Esquisse</p>
  </div>

  <div v-click="4" class="text-center text-5xl text-gray-500 animate-pulse">
    ➔
  </div>

  <div v-click="5" class="text-center">
    <div class="bg-gray-700/30 p-4 rounded-xl border border-white/10">
      <img src="/assets/images/modele_3d.png" class="h-50 mx-auto object-contain" />
    </div>
    <p class="mt-2 text-purple-400 font-bold">3. Rendu 3D CAO</p>
  </div>

</div>
<div v-click="6" class="mt-6 p-3 bg-blue-900/20 rounded-lg border border-blue-500/20 text-center">
  <p class="text-gray-300 text-xs italic">💡 C'est le passage indispensable de l'esquisse conceptuelle 2D au modèle CAO 3D complet pour l'impression.</p>
</div>

<style>
@keyframes bounce-x {
  0%, 100% { transform: translateX(0); }
  50% { transform: translateX(5px); }
}
.animate-bounce-x {
  animation: bounce-x 1s infinite;
}
</style>

---

## 🏗️ Fusion 3601 (Autodesk)
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
*La stéréolithographie : précision microscopique*

<div class="pt-4 text-gray-300">
	<img src="/assets/images/resine.jpg" class="h-100 mx-auto object-contain" />
</div>

---

## Fonctionnement de l'impression


---
layout: default
---

## Le Workflow Résine : <span class="text-red-400">Attention, ça tache !</span>

<div class="grid grid-cols-4 gap-4 mt-8 px-4">

  <div v-click="1" class="text-center">
    <div class="bg-gray-800/50 p-4 rounded-xl border border-gray-700 w-40 h-40 mx-auto flex flex-col items-center justify-center shadow-lg">
      <div class="text-5xl mb-3">🧤</div>
      <div class="font-bold text-gray-200 text-sm">1. Préparation</div>
    </div>
    <p class="text-[10px] text-gray-400 mt-2 px-2">Gants & Masque obligatoires. La résine est toxique avant cuisson.</p>
  </div>

  <div v-click="2" class="text-center">
    <div class="bg-gray-800/50 p-4 rounded-xl border border-gray-700 w-40 h-40 mx-auto flex flex-col items-center justify-center shadow-lg border-b-4 border-b-purple-500">
      <div class="text-5xl mb-3">🏗️</div>
      <div class="font-bold text-purple-200 text-sm">2. Impression</div>
    </div>
    <p class="text-[10px] text-gray-400 mt-2 px-2">Le plateau descend dans le bac, la lumière UV projette l'image.</p>
  </div>

  <div v-click="3" class="text-center">
    <div class="bg-gray-800/50 p-4 rounded-xl border border-gray-700 w-40 h-40 mx-auto flex flex-col items-center justify-center shadow-lg border-b-4 border-b-blue-500">
      <div class="text-5xl mb-3">🧼</div>
      <div class="font-bold text-blue-200 text-sm">3. Nettoyage</div>
    </div>
    <p class="text-[10px] text-gray-400 mt-2 px-2">Bain d'Alcool Isopropylique (IPA) pour enlever la résine non-durcie.</p>
  </div>

  <div v-click="4" class="text-center">
    <div class="bg-gray-800/50 p-4 rounded-xl border border-gray-700 w-40 h-40 mx-auto flex flex-col items-center justify-center shadow-lg border-b-4 border-b-green-500">
      <div class="text-5xl mb-3">☀️</div>
      <div class="font-bold text-green-200 text-sm">4. Curing</div>
    </div>
    <p class="text-[10px] text-gray-400 mt-2 px-2">Exposition finale aux UV pour durcir la pièce à cœur.</p>
  </div>

</div>

---

## Guide  des Résines

<div class="space-y-3 mt-4 max-w-2xl mx-auto">

  <div v-click="1" class="flex items-center bg-purple-500/10 border border-purple-500/30 rounded-lg p-1 shadow-lg">
    <span class="text-4xl mr-5">🛡️</span>
    <div class="flex-grow">
      <h3 class="text-purple-300 font-bold m-0 text-sm uppercase">Standard / Eco</h3>
      <p class="m-0 text-[11px] text-gray-300">La plus courante. Cassante comme du verre. Bio-sourcée (Soja) pour moins d'odeur.</p>
    </div>
  </div>

  <div v-click="2" class="flex items-center bg-blue-500/10 border border-blue-500/30 rounded-lg p-1 shadow-lg">
    <span class="text-4xl mr-5">👟</span>
    <div class="flex-grow">
      <h3 class="text-blue-300 font-bold m-0 text-sm uppercase">Flexible / Élastique</h3>
      <p class="m-0 text-[11px] text-gray-300">Propriétés proches du caoutchouc. Pour joints, coques, amortisseurs.</p>
    </div>
  </div>

  <div v-click="3" class="flex items-center bg-red-500/10 border border-red-500/30 rounded-lg p-1 shadow-lg">
    <span class="text-4xl mr-5">🧱</span>
    <div class="flex-grow">
      <h3 class="text-red-300 font-bold m-0 text-sm uppercase">Tough / ABS-Like</h3>
      <p class="m-0 text-[11px] text-gray-300">Plus résistante aux chocs et à la flexion que la standard. Pièces fonctionnelles.</p>
    </div>
  </div>

  <div v-click="4" class="flex items-center bg-green-500/10 border border-green-500/30 rounded-lg p-1 shadow-lg hover:scale-105 transition-transform">
    <span class="text-4xl mr-5">💧</span>
    <div class="flex-grow">
      <h3 class="text-green-300 font-bold m-0 text-sm uppercase">Water Washable</h3>
      <p class="m-0 text-[11px] text-gray-300 font-bold text-green-100">Plus besoin d'Alcool ! Se nettoie simplement à l'eau.</p>
    </div>
  </div>

</div>

---
layout: default
---

## Résumé : La Résine est-elle pour vous ?

<div class="grid grid-cols-2 gap-6 mt-8 px-6">

  <div v-click="1" class="bg-gray-800 p-6 rounded-3xl border-2 border-green-500/30 shadow-[0_0_20px_rgba(34,197,94,0.05)]">
    <h2 class="text-3xl font-bold text-green-400 text-center mb-6">✅ Avantages</h2>
    <ul class="text-sm space-y-4 text-gray-200">
      <li>💎 **Détails infinis :** Parfait pour figurines, bijoux, dentaire.</li>
      <li>✨ **Surface lisse :** Pas de lignes de couches visibles à l'œil nu.</li>
      <li>🚀 **Vitesse (MSLA) :** Temps constant par couche.</li>
    </ul>
  </div>

  <div v-click="2" class="bg-gray-800 p-6 rounded-3xl border-2 border-red-500/30 shadow-[0_0_20px_rgba(239,68,68,0.05)]">
    <h2 class="text-3xl font-bold text-red-400 text-center mb-6">❌ Inconvénients</h2>
    <ul class="text-sm space-y-4 text-gray-200">
      <li>☣️ **Toxicité & Odeur :** Nécessite protection et ventilation.</li>
      <li>🛠️ **Post-traitement lourd :** Nettoyage et Curing obligatoires.</li>
      <li>🧪 **Matériau fragile :** La résine standard est très cassante.</li>
    </ul>
  </div>

</div>

---

## Outil de découpage

---

## Timelapse

<div class="flex flex-col items-center justify-center mt-4">
  
  <div class="relative p-1 bg-gradient-to-tr from-blue-500 to-purple-500 rounded-2xl shadow-[0_0_30px_rgba(59,130,246,0.2)]">
    
<video 
      controls 
      autoplay 
      muted 
      loop 
      class="w-full max-w-2xl rounded-xl"
    >
      <source src="https://packaged-media.redd.it/j1b91ntgckb91/pb/m2-res_360p.mp4?m=DASHPlaylist.mpd&var=sgpssan&v=1&e=1774414800&s=f689a1c9b8b781b718f54c350f92eea93ac60f47" type="video/mp4" />
    </video>
</div>
</div>

---

# L'impresion filaire
*Fused Deposition Modeling : Le dépôt de fil fondu*

<div class="pt-4 text-gray-300">
	<img src="/assets/images/resine.jpg" class="h-100 mx-auto object-contain" />
</div>

---

## Fonctionnement de l'impression

<div class="grid grid-cols-2 gap-6 mt-6 px-4">

  <div v-click="1" class="bg-gray-800/60 p-4 rounded-2xl border-t-4 border-orange-500 shadow-xl">
    <h3 class="text-orange-400 font-bold mb-2 flex items-center gap-2">⚙️ L'Extrudeur</h3>
    <p class="text-[12px] text-gray-300">
      C'est le "moteur". Il pousse le fil vers la tête d'impression.
      <br><br>
      <span class="text-[10px] text-gray-500 italic">Types : Bowden (déporté) ou Direct Drive (sur la tête).</span>
    </p>
  </div>

  <div v-click="2" class="bg-gray-800/60 p-4 rounded-2xl border-t-4 border-blue-500 shadow-xl">
    <h3 class="text-blue-400 font-bold mb-2 flex items-center gap-2">🌡️ Le Hotend & Buse</h3>
    <p class="text-[12px] text-gray-300">
      L'endroit où la magie opère. La buse (souvent 0.4mm) dépose le plastique avec précision.
      <br><br>
      <span class="text-[10px] text-gray-500 italic">Matériaux : Laiton (standard) ou Acier trempé (carbone).</span>
    </p>
  </div>

</div>

---
layout: default
---

## Guide des Matériaux (FDM)

<div style="display: flex; flex-direction: column; gap: 8px; margin-top: 5px;">

  <div v-click="1" style="display: flex; align-items: center; background: rgba(34, 197, 94, 0.1); border: 1px solid #22c55e; border-radius: 10px; padding: 8px 20px;">
    <span style="font-size: 2.2rem; margin-right: 20px;">🌱</span>
    <div style="flex-grow: 1;">
      <h3 style="color: #4ade80; margin: 0; font-size: 1.1rem;">PLA (Acide Polylactique)</h3>
      <p style="margin: 0; font-size: 0.8rem;"><b>Usages : </b> Figurines, prototypes rapides, maquettes d'architecture, boîtes de rangement.</p>
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

  <div v-click="5" style="display: flex; align-items: center; background: rgba(168, 85, 247, 0.08); border: 1px solid #c084fc; border-radius: 10px; padding: 8px 20px;">
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
layout: default
---

## Résumé : Le filaire est-elle pour vous ?

<div class="grid grid-cols-2 gap-6 mt-8 px-6">

  <div v-click="1" class="bg-gray-800 p-5 rounded-3xl border-2 border-green-500/30 shadow-[0_0_20px_rgba(34,197,94,0.05)]">
    <h2 class="text-2xl font-bold text-green-400 text-center mb-4">✅ Avantages</h2>
    <ul class="text-xs space-y-3 text-gray-200">
      <li>💰 **Coût :** Machines et matériaux très abordables.</li>
      <li>🛠️ **Volume :** Permet d'imprimer de très grandes pièces.</li>
      <li>🌈 **Diversité :** PLA, PETG, ABS, Bois, Carbone, Flex...</li>
      <li>🧼 **Propreté :** Pas de produits chimiques ou de gants.</li>
    </ul>
  </div>

  <div v-click="2" class="bg-gray-800 p-5 rounded-3xl border-2 border-red-500/30 shadow-[0_0_20px_rgba(239,68,68,0.05)]">
    <h2 class="text-2xl font-bold text-red-400 text-center mb-4">❌ Inconvénients</h2>
    <ul class="text-xs space-y-3 text-gray-200">
      <li>➰ **Esthétique :** Les stries (couches) sont visibles.</li>
      <li>📐 **Géométrie :** Nécessite souvent des "supports" pour le vide.</li>
      <li>⏱️ **Vitesse :** Plus il y a de détails, plus c'est lent.</li>
    </ul>
  </div>

</div>

---

## Outil de découpage

---

## Timelapse

---

# H2C, l'imprimante IPPON


<div class="pt-4 text-gray-300">
	<img src="/assets/images/H2C.jpg" class="h-100 mx-auto object-contain" />
</div>

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
