Absolument ! Voici la traduction en français du document :

```
# Notions de base sur le réseautage
> ⚠ Notions de base sur le réseautage est une introduction simple aux concepts réseau les plus importants pour le piratage éthique. C'est un vaste sujet et il est recommandé d'apprendre à partir de différentes sources telles que des cours, des livres et des certifications comme [Cisco CCNA](https://www.cisco.com/c/en/us/training-events/training-certifications/certifications/associate/ccna.html) ou [CompTIA Network+](https://www.comptia.org/certifications/network). Il existe également une tonne de **formation gratuite**, je vous recommande de [consulter cette liste](https://freetraining.dfirdiva.com/free-networking-training) plus tard.

### Objectifs
* Comprendre les concepts de base du réseau

### **Ce module suit l'ordre suivant :**
1. Introduction
2. Adresses IP et MAC
3. Sous-réseautage
4. TCP, UDP et la poignée de main en trois temps (3-Way Handshake)
5. Ports et protocoles
6. Modèle OSI

# 1. Introduction

## Alors, qu'est-ce qu'un réseau, au juste ?
Un réseau se compose de deux ordinateurs ou plus qui sont reliés afin de partager des ressources. Les réseaux informatiques sont la base de la communication en informatique. Ils sont utilisés d'une grande variété de façons et peuvent inclure de nombreux types de réseaux différents. Un réseau informatique est un ensemble d'ordinateurs connectés ensemble afin qu'ils puissent partager des informations. Les premiers exemples de réseaux informatiques datent des années 1960, mais ils ont parcouru un long chemin au cours du demi-siècle qui a suivi.

![net](https://gist.githubusercontent.com/Samsar4/62886aac358c3d484a0ec17e8eb11266/raw/5edc8fbef915a17c93fa91c95877134c8fac324c/net2.jpg)

<sub><sup>Topologie de réseau LAN - SOHO / Petit réseau domestique</sup></sub>

**Deux types de réseaux très courants incluent : le LAN (réseau local) et le WAN (réseau étendu)**

## Topologies
Il existe de nombreux types de réseaux différents, qui peuvent être utilisés à des fins différentes et par différents types de personnes et d'organisations. Voici quelques-uns des types de réseaux que vous pourriez rencontrer :

### LAN - Réseau local

* Un LAN est un réseau qui a des frontières logiques et physiques dans lesquelles un ordinateur peut diffuser

<p align="center">
<img width="70%" src="https://www.geocities.ws/alcantara97/starhttt.gif" />
</p>

### WAN - Réseau étendu

* Un WAN est un ensemble de plusieurs LAN ou de WAN supplémentaires avec une fonctionnalité de routage pour l'interconnexion.

<p align="center">
<img width="70%" src="https://gist.github.com/Samsar4/62886aac358c3d484a0ec17e8eb11266/raw/a3f9b5f3f243467208da83e0d0e543b32233c5d6/wan-topo.jpg" />
</p>

### MAN - Réseau métropolitain

<p align="center">
<img width="70%" src="https://gist.githubusercontent.com/Samsar4/62886aac358c3d484a0ec17e8eb11266/raw/f37cec4e00f726cb4be3661f20ccad77751e003a/man-topo.jpg" />
</p>

### Internet
Connecter des WAN à travers d'autres WAN jusqu'à couvrir le monde entier = Internet.

* Le protocole qui fait fonctionner Internet est TCP/IP
* Tant que vous utilisez une adresse IPv4 ou IPv6 légitime
<p align="center">
<img width="70%" src="https://gist.githubusercontent.com/Samsar4/62886aac358c3d484a0ec17e8eb11266/raw/8c176b8a798fb5749c4391c45015ee5d14d56f13/internet.png" />
</p>

### Intranet
Si vous utilisez la pile TCP/IP et créez votre propre LAN ou WAN = Intranet.

* Un Intranet est un réseau privé qui utilise toujours TCP/IP

<p align="center">
<img width="70%" src="https://gist.githubusercontent.com/Samsar4/62886aac358c3d484a0ec17e8eb11266/raw/8c176b8a798fb5749c4391c45015ee5d14d56f13/intranet.png" />
</p>

## Termes courants en réseautage
* **Adresse IP (protocole Internet)** : l'adresse réseau du système sur le réseau, également connue sous le nom d'adresse logique.

* **Adresse MAC** : l'adresse MAC ou adresse physique identifie de manière unique chaque hôte. Elle est associée à la carte d'interface réseau (NIC).

* **Système ouvert** : un système ouvert est connecté au réseau et prêt à communiquer.

* **Système fermé** : un système fermé n'est pas connecté au réseau et ne peut donc pas communiquer.

* **Port** : un port est un canal par lequel les données sont envoyées et reçues.

* **Nœuds** : nœuds est un terme utilisé pour désigner tout appareil informatique tel que les ordinateurs qui envoient et reçoivent des paquets réseau sur le réseau.

* **Paquets réseau** : les données qui sont envoyées vers et depuis les nœuds d'un réseau.

* **Routeurs** : les routeurs sont des éléments matériels qui gèrent les paquets réseau. Ils déterminent de quel nœud proviennent les informations et où les envoyer. Un routeur possède un protocole de routage qui définit comment il communique avec d'autres routeurs.

* **Traduction d'adresse réseau (NAT)** : une technique utilisée par les routeurs pour fournir un service Internet à davantage d'appareils en utilisant moins d'adresses IP publiques. Un routeur possède une adresse IP publique, mais les appareils qui y sont connectés se voient attribuer des adresses IP privées que les personnes extérieures au réseau ne peuvent pas voir.

* **Protocole de configuration dynamique des hôtes (DHCP)** : attribue des adresses IP dynamiques aux hôtes et est géré par le fournisseur de services Internet.

* **Fournisseurs de services Internet (FAI)** : entreprises qui fournissent à chacun sa connexion Internet, tant aux particuliers qu'aux entreprises et autres organisations.

# 2. Adresses IP et MAC
## Qu'est-ce qu'une adresse IP (protocole Internet) ?
![ip](https://media.fs.com/images/community/upload/wangEditor/201912/24/_1577182449_2uLs0pQcuT.jpg)

Une adresse IP est une adresse unique qui identifie un appareil sur Internet ou un réseau local. IP signifie "Internet Protocol", qui est l'ensemble des règles régissant le format des données envoyées via Internet ou un réseau local.

## Vérifier votre adresse IP locale

1. Si vous utilisez Linux ou MacOS, vous pouvez ouvrir votre terminal et taper la commande `ifconfig`
2. Pour une machine Windows, vous pouvez ouvrir l'invite de commande ou PowerShell, puis taper `ipconfig /all`

![inet](https://gist.githubusercontent.com/Samsar4/62886aac358c3d484a0ec17e8eb11266/raw/5a56240010acbc33026413ad6b5c6f66e9450413/inet.png)

- inet IPv4 : `192.168.64.3`
   - `inet` --> La famille de protocoles Internet (inet) affiche l'adresse IP locale. Il s'agit de la version 4 du protocole IP (IPv4) utilisant un nombre décimal de 32 bits.
- inet6 IPv6 : `fe80::c83b:ccff:fe0e:1069`

   - `inet6` --> Est une nouvelle version d'IP (IPv6), utilisant une valeur hexadécimale de 128 bits.
- `ether` --> Adresse MAC - identifiant unique attribué à un contrôleur d'interface réseau (NIC)

## Plus d'informations sur la valeur décimale IPv4 :

```
IPv4 = plage de 32 bits (4 octets de 8 bits, de 0 à 255 chacun (4))

11000000.10101000.01000000.00000011   [IPv4 binaire]
   192  .   168  .   64   .  3        [IPv4 décimal]
```

### L'arithmétique derrière IPv4 :

- Un octet comporte 8 bits :

0 ou 1 | 0 ou 1 | 0 ou 1 | 0 ou 1 | 0 ou 1 | 0 ou 1 | 0 ou 1 | 0 ou 1
-|-|-|-|-|-|-|-
8ème bit | 7ème bit | 6ème bit | 5ème bit | 4ème bit | 3ème bit | 2ème bit | 1er bit
128 (2^7) | 64 (2^6) | 32 (2^5) | 16 (2^4) | 8 (2^3) | 4 (2^2) | 2 (2^1) | 1 (2^0)

Voici comment les octets binaires sont convertis en décimal : le bit le plus à droite, ou bit de poids faible, d'un octet a une valeur de 2^0. Le bit juste à gauche a une valeur de 2^1. Cela continue jusqu'au bit le plus à gauche, ou bit de poids fort, qui a une valeur de 2^7. Donc, si tous les bits binaires sont à un, l'équivalent décimal serait 255 comme indiqué ici :

```
  1   1   1   1   1   1   1   1
  |   |   |   |   |   |   |   |
(128 +64 +32 +16 +8  +4  +2  +1) --> 255

Exemple de conversion d'octet :
Adresse IP : 192.168.64.3

Pour calculer le premier octet (192.), du format binaire au décimal :

128  64  32  16  8   4   2   1
 |   |   |   |   |   |   |   |
 1   1   0   0   0   0   0   0
 |   |   |   |   |   |   |   |
128+ 64+ 0+  0+  0+  0+  0+  0 = 192   ---> valeur finale (premier octet IPv4 en décimal)

```
* Prenez l'IP : `192.168.64.3`
* Le premier octet `192` en binaire 8 bits est `11000000`.
* Seuls le `8ème` et le `7ème` bit sont activés et le reste (`du 6ème au 1er bit`) est désactivé, ce qui signifie que la valeur décimale est la somme finale de ces valeurs : `128 + 64 = 192`

⚠️ **Pourquoi ? Les ordinateurs voient tout en termes binaires : marche et arrêt.**

## IPv4 et IPv6
![ipv](https://academy.avast.com/hs-fs/hubfs/New_Avast_Academy/IPv4%20vs.%20IPv6%20What%E2%80%99s%20the%20Difference/IPv4-vs-IPv6.png?width=2750&name=IPv4-vs-IPv6.png)

## Adresses IP privées et publiques
Toutes les adresses IPv4 peuvent être divisées en deux groupes principaux : **globales (ou publiques, externes)** - ce groupe peut également être appelé "adresses WAN" - celles qui sont utilisées sur Internet, et les **adresses privées (ou locales, internes)** - celles qui sont utilisées dans le réseau local (LAN).

![priv-pub](https://wiki.teltonika-networks.com/wikibase/images/thumb/a/a7/Sip.png/1100px-Sip.png)

## Plus d'informations sur les adresses **IP privées** :
Les adresses privées (internes) ne sont pas routées sur Internet et aucun trafic ne peut leur être envoyé depuis Internet, elles sont uniquement destinées à fonctionner au sein du réseau local.
Les adresses privées comprennent les adresses IP des sous-réseaux suivants :

![private-ip](https://66.media.tumblr.com/02a533c1d55ca0ba83e0176168df06ec/tumblr_inline_o4m1taQugo1u4ytoo_1280.jpg)

## NAT - Traduction d'adresse réseau
NAT signifie traduction d'adresse réseau. C'est une façon de mapper plusieurs adresses privées locales à une adresse publique avant de transférer les informations. Les organisations qui souhaitent que plusieurs appareils utilisent une seule adresse IP utilisent NAT, tout comme la plupart des routeurs domestiques.

![nat2](https://gist.githubusercontent.com/Samsar4/62886aac358c3d484a0ec17e8eb11266/raw/8275f73b57bdcb982b1d69aa8d213d2bdb384657/nat2.png)

1. **NAT statique**

   Lorsque l'adresse locale est convertie en une adresse publique, ce NAT choisit la même. Cela signifie qu'il y aura une adresse IP publique cohérente associée à ce routeur ou à cet appareil NAT.

2. **NAT dynamique**

   Au lieu de choisir la même adresse IP à chaque fois, ce NAT passe par un pool d'adresses IP publiques. Cela fait que le routeur ou l'appareil NAT obtient une adresse différente chaque fois que le routeur traduit l'adresse locale en une adresse publique.

### ⚠️ Les adresses IP fonctionnent sur la **couche 3 du modèle OSI**

*Note : Ce module couvrira le modèle OSI plus tard.*

![osi3](https://gist.githubusercontent.com/Samsar4/62886aac358c3d484a0ec17e8eb11266/raw/b9d7f33be654d299f6618feeacb97fc5fd5bd7d2/OSI_L3.png)

# 3. Sous-réseautage
### Pourquoi le sous-réseautage ?
La façon dont les adresses IP sont construites permet aux routeurs Internet de trouver relativement facilement le bon réseau dans lequel router les données. Cependant, dans un réseau de classe A (par exemple), il pourrait y avoir des millions d'appareils connectés, et il pourrait falloir un certain temps pour que les données trouvent le bon appareil. C'est pourquoi le sous-réseautage est utile : il réduit l'adresse IP à une utilisation au sein d'une plage d'appareils.

Étant donné qu'une adresse IP est limitée à l'indication du réseau et de l'adresse de l'appareil, les adresses IP ne peuvent pas être utilisées pour indiquer à quel sous-réseau un paquet IP doit être envoyé. Les routeurs au sein d'un réseau utilisent ce qu'on appelle un masque de sous-réseau pour trier les données dans les sous-réseaux.

> ⚠️ Le sous-réseautage est vraiment important pour les testeurs d'intrusion et les aspirants pirates informatiques. Vous rencontrerez inévitablement plusieurs cas impliquant des réseaux petits ou grands dans vos futurs engagements. La compréhension du type d'adresse IP, de la plage et des hôtes disponibles est cruciale pour toute analyse de réseau.

## Une feuille de triche facilite le sous-réseautage

![subnetting](https://gist.githubusercontent.com/Samsar4/62886aac358c3d484a0ec17e8eb11266/raw/5ce4b7daa9c2c10ccd44675eadaceae646e487e2/cyber-mentor-subnetting.png)

* Feuille de sous-réseautage CyberMentor : https://twitter.com/thecybermentor/status/1211335431406727169

* Autre feuille de tr
