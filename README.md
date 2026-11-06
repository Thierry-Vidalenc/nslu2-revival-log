# 🐚 Remise en service du Linksys NSLU2 ("Slug")

Restauration matérielle et logicielle d'un **Linksys NSLU2 (IXP4xx)** pour héberger un micro-service de presse-papier local en ligne. Projet destiné à alimenter un portfolio TSSR.

## 🛠️ Spécifications Matérielles
* **CPU** : IXP420 ARMv5 @ 266 MHz
* **RAM** : 32 Mo SDRAM
* **Firmware actuel** : Officiel Linksys (`V23R63`)
* **IP locale** : Attribuée via DHCP (`192.168.1.181`, 0% de perte au ping)

## 📌 Étapes réalisées
1. **Flash du firmware officiel** via `upslug2` sous Debian et vérification du bon fonctionnement matériel.
2. **Validation réseau** : Intégration parfaite sur le réseau local et tests de connectivité stables.
3. **Stratégie logicielle** : 
   * Éviter les piles LAMP lourdes (incompatibles avec les 32 Mo de RAM).
   * Choix d'une architecture légère : Debian `armel` sur stockage USB externe.
   * Stack visée : **LEMP-lite** (Lighttpd + SQLite) pour héberger une interface web de type presse-papier/pastebin.

## 🚀 Prochaines étapes
* Préparation d'une clé USB bootable avec un système Debian minimal.
* Configuration de la racine (`rootfs`) sur l'USB.
* Installation de Lighttpd et développement du service web.
