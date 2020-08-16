# Coupler une box 4G avec une Freebox
Nous allons voir comment coupler la connexion de votre box fibre, adsl, vdsl, vdsl2 !
Pour cela il vous faut une box ou routeur 4G avec une carte sim avec la 4G illimitée.
Le résultat attendu bien sur est un vrai gain de débit !!!
Pour les plus expert d'entre vous vous pouvez optimiser votre connexion en prenant un amplificateur 4G. 
Vous pouvez aussi avec votre routeur 4G le relier à une antenne 4G extérieur puis orienter celle-ci vers l'antenne relais 4G la plus proche de votre domicile.

## Préparation
Il faut accéder aux différentes interfaces d'administration.

```console
- Box 4G exemple pour un routeur 4G TPlink : http://192.168.1.1
- Toutes Freebox : http://mafreebox.freebox.fr
```

## Paramétrage
Contrôler ou modifier les paramètres IP de votre box 4G et de votre Freebox.
Depuis l'interface Freebox OS, il faut attribuer la plage d'IP par le DHCP de votre Freebox ainsi nous allons pouvoir répliquer la même configuration sur votre 4G box.

- Configuration à mettre sur votre box 4G

```console
- IP de la 4G box : 192.168.1.1
- Masque de sous réseau : 255.255.0.0
- Désactiver la fonction DHCP de votre box 4G
- Désactiver l'IPV6 sur votre box 4G et votre Freebox
- N'oubliez pas de paramétrer votre réseau Wi-Fi en lui donnant un nom et un mot de passe d'au moins 20 caractères
```

- Configuration à mettre sur votre Freebox

```console
- Dans la partie DHCP mettre cette plage d'IP : 192.168.1.10 à 192.168.1.50
- Masque de sous réseau : 255.255.0.0
- Depuis votre interface d'administration je vous conseil de changer le DNS de votre Freebox par celui-ci :
- DNS 1 : 1.1.1.1
- DNS 2 : 1.0.0.1
- Désactiver l'IPV6 sur votre box 4G et votre Freebox
- Désactiver la fonction wifi de votre Freebox
```

## Connexion des deux box
Il faut connecter un cable rj45 si possible de catégorie 6 depuis un port lan de votre freebox vers le port wan de votre box 4G

## Paramétrer vos machines (pas obligatoire)
Dans les réglages de vos machines du réseau, vous pouvez leur attribuer les paramétres suivants :

```console
- une adresse IP fixe # comprise entre 192.168.1.10 à 192.168.1.50
- un masque de sous réseau # ici le 255.255.0.0
- une passerelle # ici celle de notre Freebox 192.168.1.254
- les DNS # 1.1.1.1 et 1.0.0.1
```
