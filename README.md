# eq_02_00_ELUERE-Titouan_GILLE-Swann_HAJO-Roudy_HEQUET-Nathan


Vous disposez d'une VM avec apache2, php 8.2,  mariaDB 10.1
La VM dispose de trois comptes root, user et sql, root et user disposent d'un accès en ssh et sql uniquement en sftp
Le SGBD dispose du compte user avec comme mot de passe pass et du compte sql avec comme mot de passe sql

Sur l'OS root et user ont le même mot de passe (ip, password) :
172.26.82.55
1D46fbjb

## Pour lancer le sîte
Cloner le dépôt, puis aller dans Botanicia-Site.
Lancer le service mariadb, installer composer avec ```composer install```. Pour créer et faire la migration de la base de données faire: ```php bin/console d:d:c```, ```php bin/console d:m:m```.
Une fois cela fait vous pouvez lancer symfony avec ```symfony server:start``` et récupérer l'addresse IP du server.
Si besoin, pour réinitialiser la base, faire successivement ```php bin/console d:d:d --force``` et refaire les 2 commandes précédentes

# Cahier de recette

### Base de données fonctionnelle

### Header

* Catégorie sur le header ✔
* Barre de recherche ✔
* Panier ✔
* Connexion ✔

### Accueil

* Carte de produit qui montre l'image, la marque, le prix, le nom du produit et change dynamiquement ✔
* Carte de produit qui montre une rupture de stock ✔
* Footer ✔
* Loader ✘

### Page de produit

* Bouton "Ajouter au panier" ✔
* Page de produit qui montre l'image, le prix, la description, ...  ✔
* Autres produits de la même catégorie sur la page d'un produit  ✔
* Catégorie qui montre seulement quelques produits de la dite catégorie, puis tous si le bouton "Afficher plus" est utilisé ✔
* Input quantité qui va jusqu'à 10, sauf s'il y a moins de 10 exemplaires ✔
* Si il reste moins de 10 exemplaires, afficher le nombre restant ✔
* Si il n'y a plus d'exemplaires, enlever le bouton "Ajouter au panier" et le remplacer par 'en rupture'✔

### Barre de recherche fonctionnelle
* Affiche les produits avec un nom ou une marque qui correspond à la recherche ✔
* Si rien ne correspond à la recherche, afficher une page spéciale ✔

### Panier

* Bouton "Supprimer le produit" ✔
* Bouton incrémenter et décrémenter la quantité d'un produit de 1 ✔
* Si il n'y a qu'un seul exemplaire et on décrémente, supprimer le produit ✔
* Si le nombre d'exemplaires est le même que le stock disponible, le bouton incrémenter disparaît ✔
* Montre le nombre d'éléments dans le panier ✔
* Si il reste plus de 10 exemplaires d'un produit, afficher "En stock" ✔
* Si il reste moins de 10 exemplaires d'un produit, afficher "Plus que X en stock !" ✔
* Si il n'y a plus d'exemplaires d'un produit, afficher "En rupture de stock" ✔
* Récapitulatif des prix ✔
* Bouton "Valider et payer" ✔

### Connexion/Inscription

* Possibilité de se connecter en tant qu'admin ✔
* Possibilité de se connecter en tant qu'utilisateur ✔
* Possibilité de s'inscrire ✔
* Mot de passe caché ✔
* Mot de passe haché ✔
* Une fois connecté, revenir à la page précédente ✘
* Une fois connecté, revenir à l'accueil ✔
* Si connexion via un "ajouter panier", revenir au panier avec l'article dedans ✘
* Mot de passe oublié avec envoie de mail ✘
* Se souvenir de moi ✘

### Administrateur

* Tableau de bord ✔
* Liste des utilisateurs ✔
* Liste des produits ✔
* Possibilité d'ajouter un utilisateur ✔
* Possibilité de modifier les informations des utilisateurs ✔
* Possibilité de supprimer des utilisateurs ✔
* Possibilité d'ajouter des produits ✔
* Possibilité de modifier des produits ✔
* Possibilité de supprimer des produits ✔
* Barre de recherche ✔
* Graphique de vente ✔

### Utilisateur

* Récapitulatif des informations personnelles ✔
* Formulaire pour modifier les informations personnelles ✔
* Liste des commandes passées avec factures téléchargeables ✔
* Support client ✘
* Changement mot de passe ✘

### Paiement

* Formulaire d'adresse ✔
* Si l'adresse n'a pas été renseignée dans les infos personnelles, le formulaire remplit les informations personnels lui-même ✔
* Si l'addresse est déjà dans les informations personnels, le formulaire est pré-rempli ✔
* Possibilité de payer en carte bancaire ou avec Paypal  ✔ (impossible de payer réellement)
* Formulaire d'information de paiement ✔
* Frais de port ✘ (incomplet)
* Code promo ✘
* Récapitulatif de commande une fois terminé ✔

### Autre
* Page 404 ✔
* Système de mail ✘
 
