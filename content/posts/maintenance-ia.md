+++
publishDate = "2026-04-19T10:00:00+02:00"
draft = false
title = "Ce que l'IA ne vous dit pas sur la maintenance logicielle"
categories = [ "Tech", "IA", "Gestion de projet" ]
tags = [ "IA", "Maintenance", "Logiciel", "Risque", "Développement" ]
+++

# Ce que l'IA ne vous dit pas sur la maintenance logicielle

## Le mythe du logiciel pas cher

On entend partout la même promesse : avec l'IA, créer un logiciel n'a jamais été aussi simple, aussi rapide, aussi peu coûteux. Et c'est vrai. Il est devenu possible, en quelques heures, de générer une application fonctionnelle qui aurait pris des semaines à écrire il y a encore cinq ans. Les barrières à l'entrée se sont effondrées. Des personnes sans formation technique produisent des outils qui fonctionnent, des scripts qui automatisent des tâches répétitives, des interfaces qui répondent à un besoin précis.

Mais voilà le piège : **créer un logiciel n'a jamais été la partie chère.**

La partie chère, ça a toujours été autre chose. C'est avoir confiance en lui. C'est savoir quels tests écrire et, surtout, lesquels ne pas écrire. C'est comprendre quels comportements sont critiques pour le business et lesquels sont des détails cosmétiques. Et par-dessus tout, c'est le maintenir dans le temps.

Ces questions ne changent pas avec l'IA. Elles s'aggravent.

## Ce qui coûte vraiment cher : des bons tests, pas des tests

Voici une idée reçue à corriger immédiatement : écrire des tests avec l'IA n'est pas cher. C'est même l'une des premières choses que les gens font. Vous demandez à l'IA de générer un module, vous lui demandez aussitôt d'écrire les tests qui vont avec, et en cinq minutes vous avez une suite de tests qui s'exécute, qui passe au vert, et qui donne une impression rassurante de maîtrise.

Le problème, c'est que ces tests ne coûtent rien parce qu'ils ne valent souvent pas grand-chose.

C'est exactement comme écrire de la documentation. Écrire de la doc, c'est facile. Tout le monde peut produire un texte qui décrit ce que fait un programme. Mais écrire une **bonne** documentation — claire, concise, qui explique exactement ce qu'il faut comprendre, pas plus, pas moins — c'est une autre paire de manches. Une mauvaise doc donne l'illusion d'avoir expliqué quelque chose, alors qu'elle ne fait que décrire ce que le lecteur voit déjà dans le code.

Les tests, c'est pareil. Un bon test ne vérifie pas que le code fait ce qu'on lui a demandé de faire — ça, c'est trivial. Un bon test capture une règle métier critique, un cas limite qui coûte cher quand il échoue, une invariant que le business ne peut pas se permettre de violer. Il est écrit par quelqu'un qui comprend non seulement le code, mais aussi ce qui se passe quand ce code se trompe dans la vraie vie.

**La confiance dans un logiciel, ça se construit avec du temps, de l'expérience et des retours du terrain.** Aucun outil ne peut faire ça à votre place.

## Un avantage inattendu : la maquette comme outil de dialogue

Mais l'IA a un côté franchement positif qu'on sous-estime souvent, et il concerne précisément ce problème de compréhension du besoin.

Pendant longtemps, le dialogue entre un décideur et un développeur ressemblait à ceci : le décideur explique ce qu'il veut en termes métier, le développeur traduit en termes techniques, et au bout de trois semaines de développement, le décideur découvre que ce qu'il a obtenu n'est pas exactement ce qu'il avait en tête. Ce cycle — spécifier, développer, décevoir, recadrer — était une des grandes sources de gaspillage dans les projets informatiques.

![Tree swing cartoon — ce que le client voulait vs ce que chaque équipe a compris](/images/tree-swing.svg)
*Le [tree swing cartoon](https://en.wikipedia.org/wiki/Tree_swing_cartoon) — la métaphore classique de l'écart entre ce que le client veut et ce qui est livré. Redrobsche, [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).*

L'IA change profondément cette dynamique. Aujourd'hui, un décideur peut arriver en réunion avec une maquette fonctionnelle qu'il a générée lui-même. Pas une présentation PowerPoint, pas un wireframe approximatif — **une interface qui fait ce qu'il imagine, qui répond à ses clics, qui affiche ses données**. Il a passé une après-midi dessus, il a ajusté, il a itéré, et il arrive avec quelque chose de concret.

Ce changement est considérable pour le développeur. Au lieu de devoir deviner le besoin à partir d'une description verbale, il voit le besoin. Il peut interagir avec la maquette, comprendre ce qui est vraiment important pour l'utilisateur et ce qui est secondaire. Et surtout, il peut avoir une **vraie conversation sur les coûts et les risques**.

"Cette fonctionnalité que vous avez mise là — elle est jolie, mais elle implique de synchroniser en temps réel avec trois systèmes différents. C'est la partie la plus complexe du projet, et aussi la plus fragile. Est-ce que c'est crucial pour vous, ou est-ce qu'une mise à jour toutes les heures ferait l'affaire ?" Ce genre de discussion, qui auparavant se tenait dans le vide ou après une première livraison décevante, peut maintenant avoir lieu avant d'écrire la moindre ligne de code de production.

La maquette IA devient ainsi un **outil de négociation**. Elle permet d'identifier ensemble ce qui est essentiel et ce qui est accessoire, de voir où se trouvent les risques techniques avant d'y être confronté, et de prendre des décisions éclairées sur ce qu'on choisit de construire solidement et ce qu'on accepte de faire de façon plus légère.

## L'IA produit plus, donc il y a plus à maintenir

Il y a un paradoxe au cœur de la révolution IA en développement logiciel : plus vous pouvez créer facilement, plus vous créez. Et plus vous créez, plus vous avez à maintenir.

C'est mathématiquement inévitable. Un développeur seul qui, auparavant, pouvait produire raisonnablement deux ou trois fonctionnalités par mois en produit maintenant dix ou quinze. C'est fantastique. Mais cette vélocité a un prix silencieux : la surface logicielle à maintenir est cinq fois plus grande qu'elle ne l'aurait été, et elle le reste.

Et l'IA, elle, **ne sait pas maintenir un logiciel.**

Maintenir un logiciel, c'est comprendre l'intention originale d'un bout de code. C'est savoir pourquoi telle contrainte existe, quelle décision passée a conduit à tel choix d'architecture, quel bug avait motivé ce contournement bizarre à la ligne 347. C'est une activité profondément humaine, faite de mémoire, de contexte, de compromis assumés.

L'IA peut lire du code, le modifier, mais elle repart de zéro à chaque session — sans l'histoire des décisions qui donnent du sens au présent.

Résultat : elle va souvent proposer la solution la plus simple localement, sans voir les implications globales. Elle va "réparer" quelque chose en cassant subtilement autre chose. Elle va introduire des inconsistances qui ne se voient pas tout de suite mais qui s'accumulent.

## Deux chemins, deux risques

Face à cette réalité, deux stratégies émergent. Aucune n'est parfaite, et c'est normal : **c'est de la gestion du risque, pas de la recherche de la solution idéale.**

### Le logiciel jetable : pratique mais fragile

La première option, c'est d'accepter que certains logiciels ne seront pas maintenus. On les crée pour répondre à un besoin précis, on les utilise, et quand ils tombent en panne ou deviennent obsolètes, on en crée de nouveaux.

C'est une stratégie valide, à condition de respecter deux critères. D'abord, **l'outil doit être petit et son résultat facilement vérifiable.** Si vous automatisez l'export d'un rapport hebdomadaire, vous voyez tout de suite si le résultat est correct ou non : vous comparez avec la version manuelle, vous constatez l'anomalie. Il n'y a pas besoin d'une suite de tests sophistiquée quand l'humain peut valider en trente secondes.

Ensuite, **l'enjeu doit être proportionné.** Un outil qui fait gagner deux heures par semaine à un employé, mais dont la panne n'a aucune conséquence critique, est un excellent candidat au logiciel jetable. Un outil qui calcule des factures, qui pilote un stock, qui communique avec des clients ? C'est une autre catégorie.

Le logiciel jetable, c'est comme les outils de chantier temporaires : on les fabrique vite, on s'en sert, on les jette. Personne ne s'offusque si une passerelle de bois disparaît quand le chantier est fini. Mais personne ne construit un pont en bois non plus.

### Ne pas maintenir : quatre problèmes concrets

Opter délibérément pour le non-maintien, c'est cependant accepter trois réalités inconfortables.

**Premièrement, l'évolution devient impossible.** Un logiciel qu'on ne maintient pas, c'est un logiciel figé. Le jour où votre processus change, où votre client a une nouvelle exigence, où la réglementation évolue, vous devez tout recommencer. Et si les connaissances qui avaient guidé la première version ne sont pas documentées, vous repartez vraiment de zéro.

**Deuxièmement, les failles de sécurité s'accumulent en silence.** Un logiciel non maintenu, c'est un logiciel qui n'a pas reçu ses correctifs de sécurité. Les bibliothèques vieillissent, les vulnérabilités se publient, les attaquants les connaissent. Ce n'est pas une question de malchance — c'est une question de temps. Et contrairement à une panne fonctionnelle visible, une faille exploitée peut passer des mois sans se voir.

**Troisièmement, la panne ne vous préviendra pas.** Les logiciels non maintenus ne tombent pas en panne proprement. Ils dérivaient silencieusement, produisant des résultats légèrement faux pendant des semaines, avant qu'une anomalie plus visible attire l'attention. Et la panne ne surviendra jamais au bon moment — jamais un lundi matin calme, toujours un vendredi soir avant un long week-end, toujours en plein pic d'activité, toujours quand la personne qui connaissait le sujet est en vacances.

**Quatrièmement, ce sera "la faute de l'informatique".** C'est le risque le plus insidieux. Quand un logiciel non maintenu lâche, les utilisateurs ne se souviennent pas qu'il n'était pas censé durer éternellement. Ils se souviennent qu'on leur avait promis un outil, et que l'outil ne marche plus. L'informatique devient le bouc émissaire d'une décision de gestion parfaitement raisonnable mais mal communiquée. Et personne ne dit jamais "on avait décidé de ne pas maintenir ça, c'est un choix assumé" — parce que cette décision n'avait souvent pas été formalisée.

## Ne pas mettre tous les œufs dans le même panier

La vraie leçon, c'est que l'IA dans le développement logiciel obéit aux mêmes lois que n'importe quel autre domaine de gestion du risque : **on ne met pas tous les œufs dans le même panier.**

Cela signifie plusieurs choses pratiques.

D'abord, **distinguer soigneusement les logiciels critiques des outils périphériques.** Les premiers méritent une vraie démarche de qualité : tests, documentation, revue de code humaine, stratégie de maintenance. Les seconds peuvent être traités de façon plus légère, avec une date de péremption assumée et communiquée.

Ensuite, **garder des humains dans la boucle sur les parties qui comptent.** L'IA peut accélérer la production, mais elle ne remplace pas le jugement sur ce qui est important. Un développeur expérimenté qui passe une heure à relire le code critique généré par l'IA vaut infiniment plus qu'une confiance aveugle dans la qualité du résultat.

Aussi, **documenter les décisions, pas seulement le code.** Le code dit ce que fait le programme. La documentation doit dire pourquoi il le fait ainsi, et dans quelles conditions cette décision devrait être révisée. C'est la seule chose qui permette à un humain — ou à une IA future — de maintenir intelligemment ce qui a été construit.

Enfin, **traiter l'accumulation de logiciels comme un bilan.** Si vous produisez cinq fois plus qu'avant, posez-vous régulièrement la question : qu'est-ce qui est encore vivant et utile ? Qu'est-ce qui peut être archivé ou décommissionné proprement ? La dette technique avec l'IA ne disparaît pas — elle s'accumule différemment, plus vite et plus discrètement.

## Une nouvelle compétence à développer

La promesse de l'IA dans le développement logiciel est réelle. Elle démocratise la création, elle accélère l'expérimentation, elle permet à des équipes réduites d'accomplir des choses remarquables. Mais elle crée aussi une illusion dangereuse : que la partie difficile du logiciel, c'est de l'écrire.

Le problème difficile a toujours été ailleurs. Il était dans la compréhension du métier. Dans la décision de quoi tester et de quoi ne pas tester. Dans la maintenance dans le temps d'un système qui évolue avec les besoins humains. Et dans la gestion honnête des risques qu'on accepte et de ceux qu'on refuse.

**L'IA change l'équation de la création, pas celle de la responsabilité.**

La nouvelle compétence à développer, ce n'est pas de savoir utiliser ChatGPT ou GitHub Copilot pour écrire du code — ça, ça s'apprend en quelques jours. C'est de savoir, face à un outil généré rapidement, poser les bonnes questions : cet outil, je vais le maintenir ou non ? Si oui, qui ? Avec quels moyens ? Si non, quelles sont les conséquences acceptables de sa dégradation, et les ai-je communiquées clairement ?

Ce ne sont pas des questions techniques. Ce sont des questions de pilotage, de stratégie, de communication. Et elles n'ont pas changé avec l'IA.

Ce qui a changé, c'est qu'elles deviennent urgentes beaucoup plus tôt dans le cycle de vie d'un projet. Parce que le projet, maintenant, peut exister dès le lendemain matin.
