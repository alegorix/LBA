Sur une page HTML, vous pouvez afficher plusieurs types d'images, chacun ayant ses propres forces et faiblesses. Choisir le bon format est essentiel pour optimiser la qualité visuelle et la vitesse de chargement de votre site.

La balise HTML utilisée pour toutes les afficher est <img>, en spécifiant le chemin de l'image dans l'attribut src.

Voici les principaux formats d'images que vous pouvez utiliser :

## JPEG (ou JPG) - Joint Photographic Experts Group

C'est le format le plus courant pour les photographies et les images complexes avec de nombreuses couleurs et dégradés.

Compression : Il utilise une compression avec perte (lossy), ce qui signifie qu'il réduit la taille du fichier en supprimant des informations de l'image de manière imperceptible. Vous pouvez ajuster le niveau de compression pour trouver le bon équilibre entre la qualité et le poids du fichier.

Transparence : Ne supporte pas la transparence.

Idéal pour : 📸 Photos, images réalistes, bannières complexes.

## PNG - Portable Network Graphics

Le format PNG est le roi de la transparence et des images graphiques.

Compression : Il utilise une compression sans perte (lossless), ce qui veut dire qu'aucune information n'est perdue. La qualité de l'image est parfaitement préservée, mais les fichiers peuvent être plus lourds que les JPEG.

Transparence : Supporte la transparence alpha, ce qui permet d'avoir des arrière-plans transparents avec des bords lisses et des niveaux d'opacité variables.

Idéal pour : ✨ Logos, icônes, illustrations, graphiques, et toute image nécessitant un fond transparent.

## GIF - Graphics Interchange Format

Le GIF est principalement connu pour les animations simples.

Couleurs : Limité à une palette de 256 couleurs, ce qui le rend inadapté pour les photos complexes.

Animation : Permet de créer des animations courtes et en boucle.

Transparence : Supporte une transparence binaire (un pixel est soit totalement transparent, soit totalement opaque), ce qui peut créer des bords crénelés.

Idéal pour : 🎞️ Petites animations, "memes", icônes animées simples.

## SVG - Scalable Vector Graphics

Contrairement aux autres, le SVG n'est pas une image basée sur des pixels mais sur des vecteurs (des formes mathématiques).

Qualité : Il peut être agrandi ou rétréci à n'importe quelle taille sans aucune perte de qualité. Il est toujours parfaitement net.

Taille de fichier : Très léger pour des formes simples.

Interactivité : C'est en fait un fichier texte (XML) qui peut être modifié avec du CSS et du JavaScript pour créer des animations ou des interactions.

Idéal pour : ✒️ Logos, icônes, illustrations, diagrammes, et graphiques interactifs.

## Formats Modernes : WebP et AVIF

Ces formats plus récents ont été créés pour optimiser les performances web.

WebP : Développé par Google, il offre une compression (avec ou sans perte) bien meilleure que JPEG et PNG, ce qui permet d'avoir des images plus légères pour une qualité équivalente. Il supporte aussi la transparence et l'animation.

AVIF : Encore plus récent et performant que le WebP, il offre la meilleure compression disponible aujourd'hui.

Ces deux formats sont maintenant très bien supportés par tous les navigateurs modernes et sont fortement recommandés pour améliorer la vitesse de chargement de vos pages.

En résumé, le choix du format dépend de la nature de votre image :

Photo complexe ? → JPEG ou WebP.

Logo ou icône avec transparence ? → PNG ou SVG.

Animation simple ? → GIF.

Logo ou illustration qui doit être parfaitement net à toutes les tailles ? → SVG.
