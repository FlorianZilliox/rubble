# Box2D v3 en WebAssembly (box2d3-wasm 5.2.0, variante « compat »)

Copié tel quel depuis le paquet npm `box2d3-wasm` 5.2.0 (08/10/2026), licence MIT (`LICENSE.txt`) : Box2D d'Erin Catto, portage
WebAssembly d'Alex Birch et Erik Sombroek (https://github.com/Birch-san/box2d3-wasm).
- Seule la variante `compat` (sans SIMD ni threads) est embarquée, et importée directement partout (navigateur, Node, robots) :
  la même pour tous, donc le même résultat au bit près (`proto/recherche-moteur-physique.md` § 2.3).
- Rien d'autre du jeu n'y touche : tout passe par `src/js/moteur/physique.js`.
- Pour mettre à jour : remplacer les deux fichiers, puis `node outils/tests/regles/physique.mjs` (empreintes Node / Chrome identiques,
  mémoire stable) et `npm test`.
