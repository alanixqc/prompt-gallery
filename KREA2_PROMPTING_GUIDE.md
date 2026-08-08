# Guide — Écrire des prompts parfaits pour Krea 2

Synthèse de recherche (docs officielles Krea, fal.ai, guides tiers) sur la façon d'obtenir les meilleurs résultats avec **Krea 2** (Medium & Large). Sources en bas de page.

## 1. Philosophie générale : le "exploratory prompting"

Contrairement à beaucoup de modèles où il faut un prompt ultra-détaillé dès le départ, Krea 2 est conçu pour récompenser la curiosité plutôt que l'exhaustivité :

- **Commence volontairement vague** ("A cat riding a bicycle") : le modèle interprète ça comme une invitation à explorer plusieurs directions (photo réaliste, 3D, illustration rétro...).
- **Regarde ce qui revient, garde ce qui marche, pousse plus loin.** Le workflow recommandé : *start vague → voir où le modèle t'emmène → verrouiller ce qui plaît → ajouter de la spécificité (style, medium, lumière, composition)*.
- Plus tu ajoutes de détails, plus la plage de résultats se resserre — c'est un curseur volontaire, pas un défaut.

## 2. La structure "prompt stack"

Écris toujours dans cet ordre : **sujet → contexte → composition → lumière → style → crop**.

Traite le prompt comme un shot brief (note d'intention pour un photographe), pas comme une liste de mots-clés balancés en vrac.

**Exemple faible** (que des adjectifs d'ambiance, aucun sujet concret) :
> "beautiful cinematic aesthetic moody atmospheric photoreal masterpiece"

**Exemple fort** (sujet concret + cadrage clair) :
> "A weathered fisherman in an oilskin coat, standing on a wet harbor pier at dawn, distant trawlers soft in the background"

→ Des noms concrets et un cadrage clair battent toujours une pile d'adjectifs atmosphériques.

Autre exemple de la doc officielle (matière + rendu explicites plutôt que description générique) :
- ❌ "a photo of a frog"
- ✅ "frontal macro portrait, vibrant orange sticky toes gripping a dark leaf, pitch black background, sharp facial focus, dramatic lighting"

**Longueur** : pas besoin d'un pavé. 3 à 5 mots suffisent pour explorer ; le modèle reste capable de sortir des images de qualité avec un prompt minimal. Mais un prompt hiérarchisé (sujet, lieu, caméra, lumière, style, crop) donne un contrôle bien supérieur à une liste de synonymes.

## 3. La lumière = le principal levier de photoréalisme

Si le rendu est plat, **corrige la lumière en premier**, avant le style. Précise :
- **Qualité** : lumière douce/diffuse, lumière dure/directionnelle, golden hour
- **Direction** : face, côté, contre-jour, rim light, zénithale
- **Ambiance** : low-key, high-key, tungstène chaud, lumière du jour froide

## 4. Composition avant le style — langage caméra

Utilise du vocabulaire de prise de vue :
- **Cadrage** : portrait, plan large, close-up macro
- **Angle** : plongée, contre-plongée, hauteur des yeux, low-angle
- **Objectif/focale** : 35mm, 85mm, faible profondeur de champ
- **Placement** : règle des tiers, espace négatif, contrapposto (pose)

Ce langage se traduit directement en décisions de composition — plus efficace qu'une longue liste d'adjectifs de style.

## 5. Éviter les négations dans le prompt positif

Dans Krea, les négations sont souvent contre-productives : écrire **"no people"** augmente en fait la probabilité que le modèle dessine des gens (il doit "penser" au concept pour savoir ne pas le générer).

- N'utilise le negative prompt qu'en dernier recours, une fois qu'une pile positive claire échoue de façon répétée.
- Corriger l'ordre du prompt et la lumière est plus propre qu'une longue liste d'interdictions.

## 6. Itérer une variable à la fois

Une bonne itération ne change qu'**un seul champ** de la pile (ex : juste la lumière, ou juste le crop) pour isoler ce qui améliore réellement le résultat. Fixe le ratio d'aspect tôt, car il influence la composition dès le départ.

## 7. Rendu de texte dans l'image

Pour faire apparaître du texte lisible, **mets le texte entre guillemets** dans le prompt.

## 8. Les deux variantes du modèle

| | **Krea 2 Medium** | **Krea 2 Large** |
|---|---|---|
| Taille | Plus petit, rapide, économique | 2x+ plus gros que Medium |
| Post-training | Poussé → sorties stables et cohérentes | Plus "soft" → rendu plus brut, texturé |
| Points forts | Illustration, anime, peinture, styles artistiques expressifs | Photoréalisme, esthétique brute (grain, flou de mouvement, faible dynamique), photo éditoriale |
| Coût indicatif | ~0,030 $/image | ~0,060 $/image |

→ Pour du contenu type "photo smartphone réaliste / selfie" (le style dominant de ce classeur), **Krea 2 Large** est généralement le meilleur choix.

## 9. Référence de style (style transfer)

Krea 2 permet d'extraire palette, lignes, texture, lumière et composition d'une **image de référence** placée dans le slot "Style transfer", puis de les appliquer à une nouvelle scène. On peut :
- Régler l'intensité du transfert (0–100%)
- Combiner plusieurs références — Krea 2 les mélange

Utile pour garder une direction visuelle cohérente sur une série (ex : garder le même grain/lumière sur plusieurs prompts d'un même personnage).

## 10. Curseur de créativité

Un paramètre de créativité règle l'équilibre entre exécution littérale du prompt et apport interprétatif du modèle (plus de richesse esthétique, moins de contrôle strict). À monter quand on veut que le modèle "invente" davantage autour du prompt.

## 11. Checklist rapide

1. Sujet concret d'abord, adjectifs d'ambiance en dernier
2. Ordre : sujet → contexte → composition → lumière → style → crop
3. Lumière précise (qualité + direction + ambiance) avant tout réglage de style
4. Vocabulaire caméra (angle, focale, cadrage) plutôt que mots vagues
5. Pas de négations dans le prompt positif — negative prompt seulement en dernier recours
6. Une seule variable modifiée par itération
7. Guillemets autour du texte à faire apparaître dans l'image
8. Large pour photoréalisme/grain, Medium pour illustration/anime
9. Référence de style pour garder une cohérence visuelle sur une série

---

### Sources
- [Krea — Exploratory prompting in Krea 2](https://www.krea.ai/blog/explorative-prompting-krea-2)
- [fal.ai — Krea 2 Prompting Guide + Examples](https://fal.ai/learn/tools/krea-2-prompting-guide)
- [krea-ai/krea-2 — docs/prompting.md (GitHub)](https://github.com/krea-ai/krea-2/blob/main/docs/prompting.md)
- [krea2.co — How to Write Krea 2 Prompts for Photoreal, Cinematic Images](https://krea2.co/blog/krea-2-prompt-guide)
- [krea2.net — How to Use Krea 2: Prompts, Style References & Examples](https://krea2.net/how-to-use-krea-2)
- [INCRYPTED — What Krea 2 Can Do: The Best Prompts](https://incrypted.com/en/what-krea-2-can-do-best-prompts/)
