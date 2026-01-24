# MINDHerd - Dynamiques sociales équines


![Miniature du jeu](./assets/miniature.png)



# Description

Dans MINDHerd, vous incarnez un cheval au sein d’un troupeau sauvage évoluant dans un monde où chaque action, chaque choix, influence la cohésion, la survie et l’équilibre du troupeau. Vous serez confronté·e à des dilemmes; 

Fuir ou protéger ? Suivre ou guider ? Isoler ou rassembler ? Chacun de vos choix façonnera le destin du troupeau! 

**Vos objectifs :**

* Survivre aux aléas de la nature (tempêtes, sécheresses, prédateurs).
* Maintenir l'unité du groupe face aux tensions internes.
* Comprendre les mécanismes subtils de la hiérarchie et de la coopération animale.



## Mecaniques de jeu

Le jeu s'articule autour de la gestion de quatre jauges vitales. Si l'une d'entre elles tombe à **zéro**, le troupeau se disperse et la partie est perdue (Game Over).

 * **Autorité :** La capacité à imposer des décisions cruciales en situation de crise. Une autorité trop faible mène au chaos, trop forte à la tyrannie.<br>

 * **Confiance :** Le sentiment de sécurité des individus. Sans confiance, le stress augmente et les réactions deviennent imprévisibles.<br>

 * **Cohésion :** La force du lien social. C'est ce qui empêche le groupe d'éclater lors des migrations ou des attaques.<br> 

 * **Hiérarchie :** Le respect de l'ordre social établi, essentiel pour éviter les conflits internes permanents.<br>

![Miniature du jeu](./assets/interface.png)


### Profils des Chevaux

Le joueur peut choisir son avatar, influençant le style de jeu :

* **Le cheval noir (Moteur) :** Un leader naturel, fort en déplacement, mais parfois autoritaire.<br>

* **Le cheval bai (Sensible) :** Le liant social, attentif aux émotions et aux tensions, idéal pour la cohésion.<br>

* **Le cheval gris (Observateur) :** Vigilant et en retrait, il excelle dans la détection des dangers et l'anticipation.<br>


> *Note : Les couleurs de robe sont utilisées ici comme des archétypes visuels propres à l'espèce équine. Elles ne véhiculent aucune hiérarchie, n'ont aucune valeur morale, et ne constituent en aucun cas une analogie avec les dynamiques sociales humaines.*



# Installation et lancement

### Procédure

1. Clonez ce dépôt :
```bash
git clone  https://github.com/SIla25T/MINDherd.git 
```
2. Lancer un serveur local :
   
    * *Option A (VS Code) :* Installez l'extension "Live Server", faites un clic droit sur `index.html` et choisissez "Open with Live Server".
    * *Option B (Python) :* Ouvrez un terminal dans le dossier du projet(ex: cd /Users/username/Desktop/Titre) et tapez :
        ```bash
        python3 -m http.server 8000
        ```
3.  **Accéder au jeu :**
   Ouvrez votre navigateur à l'adresse `http://localhost:5500` (VS Code) ou `http://localhost:8000` (Python).



[🎮 Jouer à la version en ligne sur Itch.io](https://senailana.itch.io/mindherd)


## Dépendances et technologies utilisées



* **[Kaplay.js](https://kaplayjs.com/) (v3001) :** Une bibliothèque JavaScript performante et intuitive pour la création de jeux 2D. Elle gère ici le rendu graphique, la physique des sprites, la gestion des scènes et le système audio.

* **HTML5 / CSS :** Pour la structure et mise en page.

* **JavaScript :** Logique complète du jeu, gestion des états, algorithmes de mélange (Fisher-Yates) et manipulation du DOM.



### Outils de développement 


* **Visual Studio Code :** Environnement de développement intégré (IDE).
* **GitHub et GitHub Desktop :** Gestion de version et hébergement du code source.

  

### Utilisation d'IA (LLM)

* **Modèles mobilisés :** ChatGPT (GPT-4o) et Google Gemini (3.0).
* **Fins d'utilisation :** Pair-programming, débogage de la logique des jauges, et aide à la syntaxe Kaplay.js.
* **Prompts essentiels mobilisés :**
    * *"Comment implémenter un algorithme de Fisher-Yates en JavaScript pour mélanger un tableau d'événements aléatoires sans répétition immédiate ?"*
    * *"Je travaille avec Kaplay.js. Je dois gérer 4 jauges d'état (Autorité, Confiance, etc.) qui doivent être persistantes entre les scènes. Est-il préférable d'utiliser un objet global "state" passé en argument lors des .go('scene') ou d'utiliser le système de composants de Kaplay ?*
    * *"J'utilise des wait() et des loop() à l'intérieur de mes entités pour gérer leurs cycles d'animation. Si j'appelle destroy() sur une entité alors qu'un wait() est en cours, est-ce que la promesse est annulée ou risque-t-elle de déclencher une erreur en essayant d'accéder à un objet qui n'existe plus ? Comment sécuriser ce code ?"* 




## Sources et Crédits


Ce projet respecte les droits d'auteur et s'appuie sur une littérature scientifique. 


### Documentation éthologique

Les mécaniques de jeu sont basées sur les travaux suivants :

*  **Bourjade, M. (2007).** *Sociogenèse et expression des comportements individuels et collectifs chez le cheval.* Thèse de doctorat, Université Louis Pasteur.

Cette thèse démontre que le "chef" du troupeau n'est pas celui qui décide de tout. Elle a servi à modéliser les systèmes de déplacement et de prise de décision collective, justifiant pourquoi le leadership (suivre un initiateur) est parfois distinct de la hiérarchie pure (dominance/ autorité). En d'autres termes, elle démontre que les décisions de déplacement dans un troupeau sont souvent collectives et partagées. Le leadership n'est pas forcément lié à la dominance agressive, mais à la capacité d'entraîner les autres (affiliation).

*  **Jorgensen, G.H.M., et al. (2009).** *Grouping horses according to gender - Effects on aggression, spacing and injuries.* Applied Animal Behaviour Science. 

Cette étude sur la stabilité sociale a permis de calibrer les jauges de Cohésion et de Hiérarchie. Elle explique les conséquences (stress, agressivité, blessures) lorsqu'un nouveau membre arrive ou lorsque l'espace vital est menacé, rendant les situations de conflit du jeu plus réalistes.


### Assets Graphiques et Sonores

* **Musique et SFX :**
    * Sons d'ambiance et bruitages (hennissements, orages, loups) provenant de [Freesound.org](https://freesound.org/) et [Pixabay.com](https://pixabay.com/) 


* **Graphismes :**
    * Sprites des chevaux et arrière-plans adaptés depuis [OpenGameArt.org](https://opengameart.org/) et [Pngkit.com](https://www.pngkit.com/).

      
> Tous les assets utilisés sont annoncés comme libres de droits



## Contexte de développement

Ce projet a été développé dans le cadre du cours *Jeu vidéo 2D* dispensé par Isaac Pante (SLI, Lettres, UNIL). Ce jeu a été pensé dans le but de répondre à la thématique sur l’intelligence (IA), organisée pour la journée des mystères à l'UNIL. L’objectif était de proposer une approche alternative et sensible de la notion d’intelligence, en l’explorant à travers le médium du jeu vidéo.

Passionnée d’équitation, j’ai vu dans ce projet l’occasion de relier deux domaines qui m'entourent : le jeu vidéo et le monde équestre. Les chevaux sont des êtres extrêmement sensibles et intelligents, dotés de capacités cognitives complexes, notamment en matière de mémoire, d’apprentissage et de perception émotionnelle. Certaines études comparent d’ailleurs leur mémoire à celle d’animaux reconnus pour leurs capacités mnésiques élevées, comme l’éléphant.

À travers ce jeu, les chevaux ne sont pas représentés comme de simples entités mécaniques ou utilitaires, mais comme des individus réactifs à leur environnement, aux interactions et aux choix du joueur. Le projet vise ainsi à interroger les formes d’intelligence non humaines et à souligner l’importance de la relation, de l’adaptation et de la communication dans toute interaction impliquant des êtres sensibles. En mettant le joueur en situation de stress ou de conflit, le jeu permet de comprendre que les décisions d'un animal ne sont pas aléatoires, mais dictées par des impératifs de survie et de structure sociale. Le développement a nécessité une recherche documentaire approfondie pour garantir que les conséquences des choix dans le jeu reflètent, de manière simplifiée mais juste, la réalité biologique.








