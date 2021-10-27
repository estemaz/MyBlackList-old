# MyBlackList-old (aucun support et aucune mises a jours)

Myblacklist old est un système de Blacklist Ip qui ampère les Ip que vous avez blacklist d'accéder à votre site.

# Installation 
1. Télécharger le .zip
2. Installer le suis un serveur web
3. Ajouter ceci en haut de vos pages que vous voulez protéger : 	
```
<?php
include 'ip.php';

$b = "246154631562562364565";

if(isset($_SESSION['IP']) AND $_SERVER['REMOTE_ADDR'] == $_SESSION['IP'] or $_SESSION['Vl'] !== $b) 

{
 header( "refresh:1;url=index.php" );
}

?>
```
4. Allez dans "ip.php" et ajouter les ip blacklist
