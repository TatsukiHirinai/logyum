# Demineur X City Builder

## Gameplay

pas de niveau juste un énorme plateau, idle, city builder, boutique permettant l'achat d'objet bonus ou d'équipements, map avec différentes zones/biomes, objet achetable pour transformer une case numéro en vierge, pour bombe autre objet plus rare et prends du temps, vue du dessus

Construction possible que sur case vierge !(numéro || drapeau || découverte); déblocage de certains perso après nb de case découverte/objectif fait (ordre : markadur, ogahon, manhund), markadur = marché (consommable), ogahon = rituel/"artefact" (bonus permanent), manhund = expédition (auto découvrir case); deux "vues", vue simpliste (couleurs et formes) lorsque déminage, vue "jolie" lorsque citybuilding/autre; creuser coûte des pièces, et on obtient des pièces grâce au city builder => à approfondir, car pb : si plus d'argent pas de découverte de case, si pas de découverte de case pas de tour passé, si pas de tour passé pas d'entrée d'argent => bloqué

Système de jours : un jour = un "tour" = X cases creusées, e.g(une expédition manhund par jour, x jours pour découvrir effet artefact ogahon, x jours refill marché);

Système de vie : début avec 100pv, une bombe enlève 25 donc quatres chances, amélioration possible à l'achat au près du markadur ou de l'ogahon

Gameover : 0vie, possibilité de reprendre à une sauvegarde, remaniement des bombes !(flaggé || "découverte") car sinon trop facile => à voir en vrai, car compliqué niveau code je pense + un peu bizarre lore wise

Port : sera disponible à la construction à partir d'un moment x, il permettra d'accueillir de nouveaux objets, de nouveaux habitant/travailleur, début de l'endgame et du vrai city builder

Fin : toutes les mines découvertes + tout les bâtiments important construit, déblocage du mode infini map sans bord (à voir), cutscene de fin découverte de l'artefact protégé, deux fins possibles, le laisser en place et devenir le protecteur de cet artefact ou le prendre et s'en servir comme arme. //à voir, pas sûr =>// Si on le protège la partie city builder est entrecoupé de combat avec des envahisseurs qui veulent récupérer l'artefact, nouveau gameplay, formation d'une armée etc. Si on l'utilise comme arme on peut envoyer des convois pour conquérir des terres et recevoir de l'argent tout les x tours + une malédiction qui détruit X cases par tour

## Style graphique

simpliste, "cartoon", voir avec Pau' si elle peut m'aider à faire les sprites sauf ceux des perso

## Histoire

découverte d'une île des terres lointaines (uncharted lands) => ancienne bataille, dernier recours de la population pour protéger un objet précieux (jsp qwa), ère 7, expédition composé majoritairement de nakkard, un groupe de manhund mercenaire, un ogahon et trois markadur. Expédition de plusieurs navires, cinquantaine de personnes, partit à la découverte des uncharted lands, malheureusement tempête => naufrage sur l'île, découverte que c'est miné, grâce à une stèle, avec la légende de l'artefact, création d'un détecteur de mines approximatif par l'ogahon et un nakkard ingénieur. L'objet précieux est sous terre, l'entrée est au milieu de la map mais doit être ouverte par des mécanismes aux quatre coins de la map. Sous terre une grande map, pas de city-building ici, mais fourré d'or et d'objets, une centaine de case, quand toutes les bombes découvertes ça donne un indice sur la position de l'objet précieux, qui est détecté comme une bombe par le détecteur.

## Programmation

Game engine : Godot

Code :
-le multi-langue : [https://gamedev.stackexchange.com/questions/66727/working-with-multiple-language-text-files-in-multilingual-games](https://gamedev.stackexchange.com/questions/66727/working-with-multiple-language-text-files-in-multilingual-games); partir sur le principe du .csv avec id + chaque colonne = une langue

À voir : un jour = 1min, creuser une case prends 30s + argent, temps améliorable; mettre l'aspect du jeu plus sur le city builder, donc nourriture divertissement habitations etc mais pour débloquer des bouts de maps et des nouveaux emplacements il faut creuser; pas de système de bar de vie mais quand se prends une bombe perds beaucoup d'argent et nb habitant mis pour creuser; les cases ont plusieurs types : terre riche (nourriture), terre rocheuse (pierre), terre boisée (bois), terre neutre (infrastructures neutre, habitation, divertissements, etc),