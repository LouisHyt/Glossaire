# GLOSSAIRE

- [Général](#général)
- [Front-end](#front-end)
- [UX / UI](#ux-ui)
- [Architecture](#architecture)
- [Modélisation / Base de données](#modélisation---base-de-données)
- [Symfony](#symfony)
- [Sécurité](#sécurité)
- [RGPD](#rgpd)
- [SEO](#seo)
- [Gestion de projets / DevOps](#gestion-de-projets---devops)
- [English](#english)

## Général
**1.	Quel est l’environnement à installer pour exécuter un script PHP ? Citer 2 exemples de logiciels permettant ce contexte**

> Pour exécuter un script PHP, il faut installer un environnement comprenant un serveur web comme apache. Voici deux exemples :
> - Laragon
> - WampServer

**2.	Qu’est-ce qu’un algorithme ?**
> Un algorithme est une série d'instruction explicites exécutés à la suite pour résoudre un problème ou effectuer une action précise.

**3.	Qu’est-ce qu’une variable ? Par quel symbole est préfixée une variable en PHP ?**

> Une variable permet de stocker des valeurs en mémoire pouvant être modifiées et réutilisées. En PHP, une variable s'écrit avec le symbole `$` (par exemple : `$name`, `$age` etc).

**4.	Qu’est-ce que la portée d’une variable ?**
> La portée d'une variable définit à quel endroit celle-ci peut être utilisée. \
> Cette portée dépend grandement de l'endroit où la variable a été déclarée ainsi que son type de déclaration (let, var, const en javascript par exemple).

**5.	Qu’est-ce qu’une constante ? Quelle est la différence avec une variable ?**

> Une constante permet de stocker des valeurs ne pouvant pas être modifiée. Contrairement à une variable, sa valeur est définie et ne peut pas être réasignée.

**6.	Qu’est-ce qu’une superglobale, combien en existent-ils et donner un exemple d’utilisation**

> En PHP, les superglobale sont des variable prédéfinie par PHP et accessibles globalement dans l'application. Il en existe 9, par exemple:
> - `$_GET` : Pour récupérer les données envoyées par URL
> - `$_POST` : Pour récupérer les données envoyées via les requètes POST
> - `$_SESSION` : Pour récupérer oumanipuler la session active
> - `$_COOKIE` : Pour récupérer ou définir les cookies de l'utilisateur.
> - `$_SERVER` : Pour obtenir des informations sur le serveur

**7.	Quels sont les différents types (primitifs) que l’on peut associer à une variable en PHP ? Les citer et en donner des exemples**

> Les types primitifs en PHP sont :
> - Integer (entier) : `$age = 26`
> - Float/Double (décimal) : `$price = 19.99`
> - String (chaîne) : `$name = "Louis"`
> - Boolean (booléen) : `$isBanned = true`

**8.	Existe-t-il plusieurs types de tableaux en PHP, si oui lesquels ?**

> En PHP il existe 2 types de tableaux :
> - Les tableaux indexés : stockent directement des valeurs (`$array = [1, 2, 3]`). On y accède en spécifiant l'index (`$array[0]`)
> - Les tableaux associatifs : utilisent un système de clé / valeurs (`$user = ["name" => "Louis", "age" => 26]`). On y accède en utilisant la clé (`$user["name"]`)

**9.	Quelles sont les différentes structures de contrôles qu’il existe en algorithmie ? Donner un exemple pour chacune d’entre elles**

**10.	Quelle est la fonction PHP permettant de demander la longueur d’une chaîne de caractères ?**

> En PHP, on utilise la fonction `strlen()` pour connaître la longueur d'une chaîne de caractères.
> Exemple : `$length = strlen("Louis");`

**11.	Qu’est-ce qu’une session ? Quelle fonction permet de démarrer une session en PHP ? Donner un exemple d’utilisation en PHP**

> Une session permet de conserver des données utilisateur sur le serveur pendant la navigation. Pour démarrer une session on utilise la fonction `session_start()`.
>
>Exemple :
>```php
>session_start();
>$_SESSION['user'] = 'Louis';
>$_SESSION['flash'] = [
>  "success" => "user successfully created!"
>]
>```

**12.	Qu’est-ce qu’un cookie ? Donner un exemple d’utilisation en PHP**

>Un cookie est un fichier texte de taille limité émis par le serveur et stocké par le navigateur. Il permet de conserver certaines informations entre chaque visite/connexion.
>
>Exemple :
>```php
>setcookie("user", "Louis", time() + 60*60*24*30);  // Le cookie sera valide 30 jours
>if(isset($_COOKIE['user'])) {
>  // Opération
>}
>```

**13.	Quelle est la différence entre les instructions « require » et « include » en PHP**

> L'instruction require renverra une erreur et stoppera l'execution du script si le fichier n'existe pas ou ne peut pas être chargé.
> L'instruction include renverra quant à elle un simple avertissement et continuera l'exécution du script

**14.	Comment effectuer une redirection en PHP ?**

> Pour effectuer une redirection en PHP, on utilise la fonction `header('Location: mon-url)`

**15.	Définir la partie « front-end » et « back-end » d’une application**

**16.	Définir le contrôle de version ? Qu’est-ce que Git ?**

**17.	Qu’est-ce qu’un CMS ? Citer au moins 2 exemples**

**18.	Quelle est la différence entre un Bundler, Transpiler, Linter et Formatter ? Donnez des examples**

## Front-end
18.	Définir HTML

> HTML signifie **HyperText Markup Language**. C'est un langage de balisage permettant de structurer le contenu d'une page web.

19.	Définir CSS
    
> CSS signifie **Cascading Style Sheets**. C'est un langage de style permettant de définir l'apparence des élements HTML (par exemple la couleur, la taille, la position etc)

20.	Définir Javascript

> Le javascript est un langage permettant de gérer l'interaction ainsi que intégrer des fonctionnalités dynamique sur les sites web. 

22.	Définir JSON. Dans quel contexte ce format est-il utilisé ?

> JSON signifie **JavaScript Object Notation**. C'est un format permettant la structuration de données. Il est utilisé principalement pour le transfère d'informations entre le client et un serveur.

24.	Peut-on interpréter du Javascript côté serveur ? Si oui, comment ?

> Oui, le javascript peut être interpréter côté serveur avec des environnements comme NodeJS, Deno, Bun etc

26.	Qu’est-ce qu’un sélecteur CSS ?

> Un sélecteur CSS est un règle utilisée pour spécifier le ou les éléments à styliser.

28.	Quelle balise HTML permet de créer un lien hypertexte ?

> Pour créer un lien hypertexte, on utilise la balise `<a>` accompagné de son attribut `href`.
> Hypertext est un système permettant de relier différentes informations via des liens cliquables sur des documents ou des pages webs.

30.	Qu’est-ce qu’une requête AJAX ?

> AJAX signifie **Asynchronous JavaScript and XML**. Une requête Ajax permet au client de communiquer avec un serveur sans recharger la page.

32.	Quel sélecteur CSS permet de sélectionner tous les éléments d’une classe spécifique ? D’un identifiant spécifique ?

> Pour séléctionner tous les éléments d'une classe spécifique on utilisera le symbole `.`
> Pour ce qui est d'un identifiant, on utilisera le symbole `#`.
>Exemple :
>```css
>.card {
>  background-color: white;
>}
>
>#logo {
>  font-size: 1.25rem
>}
>```

34.	Définir le responsive design

> Le responsive design est le fait d'adapter l’apparence d’un site web aux différentes types d’écrans (ordinateurs, tablettes, mobiles).

36.	Qu’est-ce que le templating ?

> Le templating est une technique utilisant des templates (ou modèles) en HTML adin d'y injecter dynamiquement du contenu.

38.	Qu’est-ce qu’une fonction anonyme en Javascript ?

39.	Quelle méthode JavaScript est utilisée pour ajouter un élément à la fin d'un tableau ?

40.	Qu’est-ce qu’un « media query » ?

41.	Qu’est-ce qu’un pseudo élément en CSS ?

42.	Qu’est-ce que Bootstrap ? Donner d’autres exemples équivalent

43.	Quand un formulaire HTML est créé, quelles sont les 2 méthodes qui peuvent lui être associées ? Donner la différence entre ces 2 méthodes

## UX UI
35.	Quelle est la différence entre UX Design et UI Design ?

36.	Qu’est-ce qu’un wireframe ? 

37.	Qu’est-ce qu’un prototype ? 

38.	Qu’est-ce que la hiérarchie visuelle en UI Design ?

39.	Qu’est-ce que l’accessibilité en UX Design ? 

40.	Qu’est-ce qu’une grille de mise en page ?

41.	Qu’est-ce que la notion d’affordance en UX Design ?

42.	Qu’est-ce qu’un « mobile first design » ?

## Programmation orientée objet (POO)
43.	Donner une définition de la programmation orientée objet 

44.	Qu’est-ce qu’une classe ? Comment la déclare-t-on ?

45.	Qu’est-ce qu’un objet ?

46.	Définir la notion de propriété / attribut / méthode

47.	Qu’est-ce que la visibilité d’une propriété ou d’une méthode ? Citer les différents types de visibilité

48.	Quelle est la méthode spécifique utilisée pour créer un nouvel objet à partir d’une classe ?

49.	Qu’est-ce que l’encapsulation ?

50.	Que signifie « étendre une classe » ? Quelle est le concept clé mis en œuvre ? Donner un exemple

51.	Définir l’opérateur de résolution de portée

52.	Définir une méthode / propriété statique

53.	Définir le polymorphisme en POO

54.	Définir une méthode / classe abstraite ?

55.	Définir le chaînage de méthodes

56.	Qu’est-ce que la méthode __toString() ? Existe-t-il d’autres méthodes « magiques »

57.	Qu’est-ce qu’un « autoload » ?

58.	Comment appelle-t-on en français les « getters » et les « setters » ?

59.	Qu’est-ce que la sérialisation en PHP ? 

## Architecture 
60.	Qu’est-ce que l’architecture client / serveur ? Grâce à quel type de requête peut-on interroger le serveur. Définir l’acronyme de ce type de requête. Si on ajoute un « S » à cet acronyme, expliquer la différence

61.	Donner la définition d’un design pattern. Citer au moins 3 exemples de design pattern

62.	Qu’est-ce que l’architecture MVC ?

63.	Quel est le rôle de chaque couche du design pattern MVC : Model, View, Controller ?

64.	Quels sont les avantages de l’architecture MVC ?

65.	Existe-t-il des variantes à l’architecture MVC ?

66.	Qu’est-ce qu’une API ? Définir l’architecture REST

## Modélisation - Base de données
67.	Qu’est-ce que la modélisation de données ? Définir la méthode Merise

68.	Quelles sont les 3 étapes principales de la méthode Merise ? 

a.	Analyse, conception et réalisation
b.	Planification, exécution et contrôle
c.	Création, modification et suppression

69.	Qu’est-ce qu’un modèle conceptuel de données (MCD) en Merise ?

70.	Qu’est-ce qu’un modèle logique de données (MLD) en Merise ?

71.	Donner la définition des mots suivants :
a.	Entité
b.	Relation
c.	Cardinalité
d.	Clé primaire / clé étrangère

72.	Que devient une relation de type « Many To Many » dans le modèle logique de données ?

73.	Qu’est-ce qu’une base de données ?

74.	Définir les notions suivantes : 
a.	SQL
b.	MySQL
c.	SGBD (donner 2 exemples de SGBD)

75.	Dans une base de données, les données sont stockées dans des ___. Celles-ci sont constituées de lignes appelées ___ et de colonnes appelées ___

76.	Quelle est la différence entre une base de données relationnelle et non relationnelle ?

77.	Qu’est-ce qu’une jointure dans une base de données ? En existe-t-il plusieurs ? Si oui lesquelles ?

78.	A quoi sert une vue dans une base de données ?

79.	Qu’est-ce que l’intégrité référentielle dans une base de données ?

80.	Quelles sont les fonctions d’agrégation en SQL ?

81.	Qu’est-ce qu’un CRUD dans le contexte d’une base de données ?

82.	Quelles sont les clauses qui permettent de :
a.	Insérer un nouvel enregistrement dans une table
b.	Modifier un enregistrement dans une table
c.	Supprimer un enregistrement dans une table
d.	Supprimer la base de données
e.	Filtrer les résultats d’une requête SQL
f.	Trier les résultats d’une requête SELECT
g.	Regrouper les résultats d'une requête SELECT en fonction d'une colonne spécifique
h.	Concaténer 2 chaînes de caractères 

83.	Comment se connecter à une base de données en PHP ? Quelle est la classe native utilisée ?

## Symfony
84.	Qu’est-ce que Symfony ?

85.	Sur quel langage de programmation et design pattern repose Symfony ? 

86.	Quelle est la dernière version en date de Symfony ?

87.	Qu’est-ce qu’un bundle ? 

88.	Quel est le moteur de template utilisé par défaut dans Symfony ?

89.	Qu’est-ce qu’un ORM ? Quel est son utilité et comment s’appelle-t-il au sein de Symfony ?

90.	Qu’est-ce que l’injection de dépendances ? Quel est l’outil utilisé dans ce contexte et quel fichier contient l’intégralité des dépendances du projet ?

91.	Que permet le bundle Maker au sein de Symfony ? 

92.	Quel est le langage de requêtage exploité au sein d’un projet Symfony ?

93.	Quel est le composant qui garantit l’authentification et l’autorisation des utilisateurs ?

## Sécurité
94.	Qu’est-ce que l’injection SQL ? Comment s’en prémunir ?
> Une injection SQL est un type d'attaque où une personne insère du code SQL dans un champ (par exemple formulaire, url) pour lire ou modifier des informations de la base de donnée.
> Pour éviter ce genre d'attaque, on peut :
> - Sanitizer les données entrées par l'utilisateur (échapper certaines catactères, vérifier la présence de certains symboles etc)
> - Préparer les requètes SQL avec des paramètres. Par exemple en PHP on aura :
> ```php
> $req = $pdo->prepare("INSERT INTO table (username, password) VALUES (:username, :email)");
> $req->execute([
>    ":username" => $username,
>    ":email" => $email     
> ])
> ```
> Au lieu de
> ```php
> $req = $pdo->query("INSERT INTO table (username, email) VALUES ($username, $email)")
> ```


95.	Qu’est-ce que la faille XSS ? Comment s’en prémunir ?

96.	Qu’est-ce que la faille CSRF ? Comment s’en prémunir ?
> La faille CSRF signifie "Cross-Site Request Forgery". Elle force un utilisateur authentifié à exécuter des actions non désirées depuis un autre site web.
> Pour éviter ce genre d'attaque, on peut :
> - Utiliser des tokens CSRF (Permet de s'assurer que la requête est effectué depuis le même site ayant distribué le token.

97.	Définir l’attaque par force brute et l’attaque par dictionnaire

98.	Existe-t-il d’autres failles de sécurité ? Citer celles-ci et expliquer simplement leur comportement

99.	A quoi servent l’authentification et l’autorisation dans un contexte d’application web ?

100.	Définir la notion de hachage d’un mot de passe et citer des algorithmes de hachage

101.	Qu’est-ce qu’une politique de mots de passe forts ?

102.	Qu’est-ce que l’hameçonnage ?

103.	Définir la « validation des entrées »

## RGPD
104.	Qu’est-ce que le RGPD ?

105.	Quel est son objectif principal ?

106.	Quelle est la date d’entrée en vigueur du RGPD ?

107.	Quelles sont les sanctions possibles en cas de non-respect du RGPD ?

108.	En France, quel est l’autorité administrative qui s’occupe de faire appliquer le RGPD ?

109.	Quel est le consentement valide selon le RPGD ?

110.	Qu’est-ce qu’une politique de confidentialité ?

111.	Quelle est la durée de conservation maximale des données personnelles selon le RGPD ?

112.	Quels sont les droits des utilisateurs selon le RGPD ?

113.	Qu’est-ce que le principe de minimisation des données selon le RGPD ?

## SEO
114.	Qu’est-ce que le SEO ? 

115.	Quel est l’objectif principal du SEO ?

116.	Existe-t-il plusieurs types de référencement ? Lesquels ?

117.	Qu’est-ce que la densité de mots-clés en SEO ?

118.	Qu’est-ce qu’une balise « alt » ?

119.	Qu’est-ce que la balise « meta description » ?

120.	Qu’est-ce que le « nofollow » en SEO ?

121.	Quelle est l'importance du contenu de qualité pour le référencement d'un site web ?

122.	Pourquoi est-il important d'utiliser des balises de titre (h1, h2, h3, etc.) de manière structurée ?

123.	Quelle est la recommandation pour les URL d'un site web bien référencé ?

124.	Qu'est-ce que le maillage interne et pourquoi est-il important pour le référencement ?

125.	Qu'est-ce que l'optimisation des images pour le référencement ?

126.	Qu'est-ce qu'un plan de site (sitemap) et pourquoi est-il important pour le référencement ?

## Gestion de projets - DevOps
127.	Qu’est-ce que la gestion de projet ?	

128.	Qu’est-ce qu’une méthode Agile de gestion de projet ? 

129.	Expliquer la méthode MoSCoW en quelques lignes et citer ses avantages

130.	A quoi sert la méthodologie MVP ? Citer les caractéristiques clés

131.	Qu’est-ce que la planification itérative ?

132.	Citer 3 méthodes Agiles dans le cadre d’un projet informatique

133.	Qu’est-ce qu’une réunion de revue de projet ?

134.	Qu’est-ce qu’un livrable dans un projet ? 

135.	Quels sont les 3 piliers SCRUM ? Définir chacun d’entre eux

136.	Qu’est-ce que le DevOps et quel est son objectif principal ?

137.	Qu’est-ce que l’intégration continue ? 

138.	Qu’est-ce que Docker ? Et en quoi est-il utile dans le cadre du DevOps ?

139.	Qu’est-ce qu’un test unitaire ? 

140.	Quelle est l'unité de code testée lors d'un test unitaire ?

141.	Quelles sont les caractéristiques d'un bon test unitaire ?

142.	Qu'est-ce qu'une assertion dans un test unitaire ?

8)	Which of the following is a characteristic of NoSQL databases ?
a.	Strict schema enforcement
b.	Support for complex transactions
c.	Scalability and flexible data models
