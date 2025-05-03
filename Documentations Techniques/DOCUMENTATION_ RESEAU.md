---
title: 'DOCUMENTATION: RESEAU'
tags: [DOC-AP4]

---

[toc]

### OpenWRT

OpenWRT source : https://images.linuxcontainers.org/images/openwrt/24.10/amd64/default/20250212_11%3A57/

**Création du conteneur**:

1.  **Commande**:
    -   Exécutez la commande suivante pour créer un nouveau conteneur.
    -   `pct create 492 /mnt/pve/iso-smb/template/cache/openWRT.tar.xz --arch amd64 --hostname RTR68COL02 --rootfs local-lvm:20 --memory 256 --cores 1 --ostype unmanaged --unprivileged 0`

    ![commande pour créer le conteneur (ci-dessus)](https://hackmd.io/_uploads/rkCjZcqKyx.png)
2.  **Ajout du réseau**:
    -   Configurez les paramètres réseau pour le conteneur.

    ![ajouter un réseau](https://hackmd.io/_uploads/H1bzGcqtkl.png)
3.  **Ajout du WAN**:
    -   Configurez l'interface WAN.

    ![ajouter un wan](https://hackmd.io/_uploads/S1vFm99Kkg.png)
4.  **Ajout du LAN**:
    -   Configurez l'interface LAN.

    ![ajouter un lan](https://hackmd.io/_uploads/SJ90Xc9Kkx.png)
5.  **Modification de la configuration réseau**:
    -   Modifiez le fichier `/etc/config/network`.

    ![démarrer le conteneur et modifier la config réseau](https://hackmd.io/_uploads/Hk_7NqcKke.png)
    -   Exemple de configuration:

    ```
    config interface 'loopback'  
            option ifname 'lo'
            option proto 'static'
            option ipaddr '127.0.0.1'              
            option netmask '255.0.0.0'

    config interface 'wan'     
            option type 'bridge'
            option ifname 'eth0' 
            option proto 'static'    
            option ipaddr '10.54.146.8'
            option netmask '255.255.255.0'
            option gateway '10.54.146.1'
                                
    config interface 'lan'      
            option type 'bridge' 
            option ifname 'eth1'        
            option proto 'static'         
            option ipaddr '172.16.0.253'
            option netmask '255.255.255.0'
    ```
6.  **Appliquer les modifications**:
    -   Commentez l'ancienne configuration et ajoutez la nouvelle.
    -   Enregistrez les modifications avec `:wq`.

    ![commenter l'ancienne config, ajouter la nouvelle (ci-dessus) puis enregistrer (:wq)](https://hackmd.io/_uploads/BJYT45qKke.png)
7.  **Redémarrer le réseau**:
    -   Redémarrez le service réseau pour appliquer les modifications.
    -   ` /etc/init.d/network restart`

    ![image](https://hackmd.io/_uploads/rkHHH9qtye.png)

### Dynfi

#### Installation

1.  **Écran d'accueil**:
    -   Écran initial pendant l'installation.

    ![bienvenue (install/shell/live CD)](https://hackmd.io/_uploads/HyFHiN9Fye.png)
2.  **Sélection du Keymap**:
    -   Sélectionnez le keymap approprié.

    ![Sélection du Keymap](https://hackmd.io/_uploads/BJhYTEqt1x.png)
3.  **Partitionnement (UFS)**:
    -   Configurez le partitionnement du disque.

    ![Partitionnement (UFS)](https://hackmd.io/_uploads/S1CsaVcF1e.png)
4.  **Partitionner le disque entier**:
    -   Choisissez de partitionner le disque entier.

    ![Partitionner le disque entier](https://hackmd.io/_uploads/S16aTEqY1l.png)
5.  **Schéma de partition MBR**:
    -   Sélectionnez le schéma de partition MBR.

    ![Schéma de partition MBR](https://hackmd.io/_uploads/rJZlR49Y1e.png)
6.  **Vérification de la partition**:
    -   Vérifiez la configuration de la partition.

    ![vérifier la partition](https://hackmd.io/_uploads/Hy0ZA4qFyg.png)
7.  **Commit (effacer le disque)**:
    -   Validez les modifications et effacez le disque.

    ![Commit (effacer le disque)](https://hackmd.io/_uploads/Skc7REcYkl.png)
8.  **Attendre l'installation**:
    -   Attendez que le système soit installé.

    ![Attendre que les paquets/système soient installés](https://hackmd.io/_uploads/r1u3dUqYkx.png)
9.  **Éteindre et retirer le disque**:
    -   Éteignez le système et retirez le disque d'installation.

    ![éteindre et retirer le disque d'installation](https://hackmd.io/_uploads/rkLXYU5Y1x.png)

#### Configuration de base (en mode tty)

Pour activer une interface LAN pour l'administration web:

1.  **Connexion**:
    -   Utilisez les identifiants suivants:
        -   Login: `root`
        -   Mot de passe par défaut: `dynfi`

    ![Après le premier démarrage, se connecter sur le routeur](https://hackmd.io/_uploads/BkoPCO2t1l.png)
2.  **Assigner les interfaces**:
    -   Allez à l'option 1 pour assigner les interfaces.

    ![Aller à l'option 1 pour assigner les interfaces](https://hackmd.io/_uploads/BJ5lJFntyl.png)
3.  **Entrez le nom de l'interface WAN**:

    ![Entrez le nom de l'interface WAN](https://hackmd.io/_uploads/Bksr1YhK1x.png)
4.  **Entrez le nom de l'interface LAN**:

    ![Entrez le nom de l'interface LAN](https://hackmd.io/_uploads/SJ4OkKhFye.png)
5.  **Confirmer les actions**:
    -   Entrez `yes` pour confirmer les actions précédentes.

    ![Entrez yes pour confirmer les actions précédentes](https://hackmd.io/_uploads/SJeAKJYnY1x.png)
6.  **Définir l'adresse IP de l'interface**:
    -   Sélectionnez l'option 2 pour définir l'adresse IP de l'interface.

    ![Sélectionnez l'option 2 pour définir l'adresse IP de l'interface](https://hackmd.io/_uploads/SyVn1YnKkg.png)
7.  **Configuration IP pour le LAN**:

    ![Configuration IP pour le LAN](https://hackmd.io/_uploads/B1MggK2tye.png)
8.  **Désactiver IPV6**:
    -   Ne configurez pas IPV6 (Non utilisé).

    ![Ne configurez pas IPV6 (Non utilisé)](https://hackmd.io/_uploads/HJ0hbt3tyl.png)

#### Config WEB (Wizard + Interfaces + HA)

1.  **Première connexion**:

    ![première connexion](https://hackmd.io/_uploads/rJH4QF2Y1x.png)
2.  **Démarrer l'assistant**:

    ![démarrer l'assistant](https://hackmd.io/_uploads/r1Xc7thF1x.png)
3.  **Informations générales**:
    -   Configurez le nom d'hôte, le domaine et les paramètres DNS.

    ![assistant : informations générales (nom d'hôte, domaine [haut-rhin.gouv], dns (routeurs avant [172.16.0.254 et .253]))](https://hackmd.io/_uploads/HkkzSt3YJe.png)
4.  **Serveurs NTP**:
    -   Pas besoin de modifier les paramètres du serveur NTP.

    ![assistant: serveurs ntp (pas besoin de toucher)](https://hackmd.io/_uploads/HJlEwSKhtJx.png)
5.  **Configurer l'interface WAN**:
    -   Définissez l'adresse IP statique et la passerelle pour l'interface WAN.

    ![assistant: configurer l'interface WAN (adresse statique et passerelle)](https://hackmd.io/_uploads/rJotTtnY1l.png)
6.  **Options de l'interface WAN**:
    -   Autorisez blogon et les réseaux privés.

    ![assistant: configurer l'interface WAN (autoriser blogon & les réseaux privés)](https://hackmd.io/_uploads/S173aKhKyl.png)
7.  **Configurer l'interface LAN**:

    ![assistant: configurer l'interface LAN](https://hackmd.io/_uploads/r11WCYnY1x.png)
8.  **Définir le mot de passe administrateur**:
    -   Définissez le mot de passe administrateur.
    -   `root@passwd : Admin`

    ![assistant: définir le mot de passe administrateur](https://hackmd.io/_uploads/HyLLCF3K1l.png)
9.  **Recharger la configuration**:
    -   Rechargez pour terminer la configuration.

    ![assistant: recharger pour terminer la configuration](https://hackmd.io/_uploads/HJwwAFntJg.png)

##### Modifier les interfaces

1.  **Assigner vnet0 à un nouveau PfSync**:

    ![Assigner vnet0 à un nouveau PfSync](https://hackmd.io/_uploads/rylpAFnKJg.png)
2.  **Définir l'adresse PfSync (SET IPV4)**:

    ![Définir l'adresse PfSync (SET IPV4)](https://hackmd.io/_uploads/SkA_yqhF1e.png)
3.  **Définir l'adresse PfSync**:
    -   Définissez l'adresse PfSync (par exemple, 10.0.0.1 pour MASTER).

    ![Définir PfSync (SET Adresse (10.0.0.1 [MASTER]))](https://hackmd.io/_uploads/B1wYychFye.png)
4.  **Recharger l'adresse PfSync**:

    ![Définir l'adresse PfSync: recharger](https://hackmd.io/_uploads/HJ7ny92Kye.png)

##### Autoriser tout le trafic sur l'interface PfSync

1.  **Règles PfSync**:

    ![Règles PfSync](https://hackmd.io/_uploads/S13N_92tke.png)
2.  **Créer une règle**:
    -   Créez une règle pour IPv4 any in any out.

    ![Créer une règle (IPV4 any in any out)](https://hackmd.io/_uploads/rJD9OchKyg.png)
3.  **Description**:
    -   Ajoutez une description pour la règle (par exemple, PfSync).

    ![Créer une règle (Description : PfSync)](https://hackmd.io/_uploads/H1bi_cnYkl.png)

---

1.  **Assigner vnet2 à un nouveau WANBackup**:

    ![Assigner vnet2 à un nouveau WANBackup](https://hackmd.io/_uploads/SkPl1c3Y1e.png)

Activez l'interface WANBackup avant les prochaines étapes.

1.  **Créer une passerelle WANBackup**:

    ![Créer une passerelle WANBackup](https://hackmd.io/_uploads/Hynmg92Fkx.png)
2.  **Configurer la passerelle WANBackup**:
    -   Configurez la passerelle WANBackup (par exemple, IPV4: 172.16.0.253).

    ![Configurer la passerelle WANBackup (IPV4 : 172.16.0.253)](https://hackmd.io/_uploads/Sy6l-93tkg.png)

Activer la surveillance pour WAN

1.  **Définir l'adresse PfSync**:

    ![Définir l'adresse PfSync (SET IPV4)](https://hackmd.io/_uploads/ryOdb92F1e.png)
2.  **Surveillance**:

    ![image](https://hackmd.io/_uploads/SkdFZ5nYke.png)

Faites de même pour le deuxième pare-feu, puis démarrez la configuration HA.

##### Configuration HA

1.  **Disponibilité HA**:
    -   Configurez l'adresse du pair et activez les états de synchronisation.

    ![Disponibilité HA : Adresse du pair (10.0.0.2) activer les états de synchronisation](https://hackmd.io/_uploads/S1vQM5hYkg.png)
2.  **Synchronisation HA**:
    -   Tout synchroniser.

    ![Disponibilité HA : Adresse du pair (10.0.0.2) tout synchroniser](https://hackmd.io/_uploads/B1PNfq2Ykx.png)

##### Configuration de CARP (LAN et WAN)

1.  **Ajouter une interface IP virtuelle**:

    ![Ajouter une interface IP virtuelle](https://hackmd.io/_uploads/H1ml9q3Fyl.png)
2.  **Configurer CARP pour LAN**:
    -   Configurez CARP pour LAN (par exemple, 172.16.1.254).

    ![Configurer CARP pour LAN (172.16.1.254)](https://hackmd.io/_uploads/S1i7qq3F1e.png)
3.  **Configurer CARP pour WAN**:
    -   Configurez CARP pour WAN (par exemple, 172.16.0.10).

    ![Configurer CARP pour WAN (172.16.0.10)](https://hackmd.io/_uploads/HkQqq92Ykg.png)
4.  **Configurer CARP pour WANBackup**:
    -   Configurez CARP pour WANBackup (par exemple, 172.16.0.20).

    ![Configurer CARP pour WANBackup (172.16.0.20)](https://hackmd.io/_uploads/HyTvsc3Fye.png)

##### Configuration des VLANs

1.  **Ajouter un VLAN**:

    ![Ajouter un VLAN](https://hackmd.io/_uploads/BJR9hcnYyx.png)
2.  **VLAN 10**:

    ![VLAN 10](https://hackmd.io/_uploads/ryHuTqhY1l.png)
3.  **VLAN 15**:

    ![VLAN 15](https://hackmd.io/_uploads/ryrhTqnYkx.png)
4.  **VLAN 30**:

    ![VLAN 30](https://hackmd.io/_uploads/ryjJ093Fkl.png)
5.  **VLAN 60**:

    ![VLAN 60](https://hackmd.io/_uploads/rkmz053KJx.png)
6.  **VLAN 90**:

    ![VLAN 90](https://hackmd.io/_uploads/rJPHRchY1g.png)
7.  **Assigner tous les VLANS à une interface**:
    -   Assigner VLAN10 à VLAN90.

    ![Assigner tous les VLANS à une interface (VLAN10 à VLAN90)](https://hackmd.io/_uploads/rkEfJjhK1g.png)
8.  **Configurer les interfaces pour tous les VLANS**:
    -   Configurez les interfaces pour tous les VLANs (par exemple, 172.16.10.253/24 -> 172.16.90.253/24 sur le pare-feu 1, et sur le 2 172.16.10.252/24 -> 172.16.90.252/24).

    ![Configurer les interfaces pour tous les VLANS (172.16.10.253/24 -> 172.16.90.253/24 sur le pare-feu 1, et sur le 2 172.16.10.252/24 -> 172.16.90.252/24)](https://hackmd.io/_uploads/HyrTlinKJg.png)

    ![Configurer les interfaces pour tous les VLANS (172.16.10.253/24 -> 172.16.90.253/24 sur le pare-feu 1, et sur le 2 172.16.10.252/24 -> 172.16.90.252/24)](https://hackmd.io/_uploads/B1BRxinYkg.png)

    ![Configurer les interfaces pour tous les VLANS (172.16.10.253/24 -> 172.16.90.253/24 sur le pare-feu 1, et sur le 2 172.16.10.252/24 -> 172.16.90.252/24)](https://hackmd.io/_uploads/rk9lbsnK1e.png)
9.  **Configurer CARP pour tous les VLANS**:
    -   Configurez CARP pour tous les VLANs (par exemple, 172.16.10.253/24 -> 172.16.90.253/24).

    ![Configurer CARP pour tous les VLANS (172.16.10.253/24 -> 172.16.90.253/24](https://hackmd.io/_uploads/Sk7c7nnKye.png)

##### Configuration du relais DHCP

1.  **Configurer le relais pour l'interface VLAN30**:
    -   Configurez le relais pour l'interface VLAN30 (Clients) avec les serveurs 172.16.10.20 et .21 (serveurs DHCP AD).

    ![Configurer le relais pour l'interface VLAN30 (Clients) avec les serveurs 172.16.10.20 et .21 (serveurs DHCP AD)](https://hackmd.io/_uploads/ByqhSgwj1g.png)

##### Configuration d'OpenVPN

###### Configuration de PKI

###### Créer une autorité de certification

1.  **Système >> Confiance >> Autorité**:

    ![Système >> Confiance >> Autorité](https://hackmd.io/_uploads/HyBwih3F1g.png)
2.  **Créer une autorité de certification (1/2)**:

    ![Créer une autorité de certification (1/2)](https://hackmd.io/_uploads/Hyj4o2hKJg.png)
3.  **Créer une autorité de certification (2/2)**:

    ![Créer une autorité de certification (2/2)](https://hackmd.io/_uploads/B1iHo23tke.png)

###### Créer un certificat serveur

1.  **Système >> Confiance >> Certificats**:

    ![Système >> Confiance >> Certificats](https://hackmd.io/_uploads/r1zEDh3FJe.png)
2.  **Créer un certificat serveur (1/2)**:

    ![Créer un certificat serveur (1/2)](https://hackmd.io/_uploads/H14U32nYkl.png)
3.  **Créer un certificat serveur (2/2)**:

    ![Créer un certificat serveur (2/2)](https://hackmd.io/_uploads/HJJD223FJl.png)

###### Configuration de TOTP

1.  **Configuration de TOTP**:

    ![image](https://hackmd.io/_uploads/BkmG62htJl.png)

###### Ajouter un serveur SSL

1.  **ACCÈS DISTANT SSL/TLS + Auth utilisateur**:

    ![ACCÈS DISTANT SSL/TLS + Auth utilisateur](https://hackmd.io/_uploads/BJIAya3Fyl.png)
2.  **Cryptographie**:

    ![Cryptographie](https://hackmd.io/_uploads/Byeyg63Ykl.png)
3.  **Paramètres du tunnel**:

    ![Paramètres du tunnel](https://hackmd.io/_uploads/Hk6ylT3Fkg.png)
4.  **Paramètres avancés**:
    -   (aucun changement)

    ![Paramètres avancés (aucun changement)](https://hackmd.io/_uploads/S10eeT2t1l.png)

###### Configuration de LDAP

1.  **Ouvrir les groupes dans les paramètres système**:

    ![Ouvrir les groupes dans les paramètres système](https://hackmd.io/_uploads/HJXSwYzRyx.png)
2.  **Sélectionner Ajouter dans les groupes**:

    ![Sélectionner Ajouter dans les groupes](https://hackmd.io/_uploads/BkHFvFz0Jg.png)
3.  **Créer un nouveau groupe OpenVPN LDAP**:

    ![Créer un nouveau groupe OpenVPN LDAP](https://hackmd.io/_uploads/HJb6PYGA1x.png)
4.  **Sélectionner Ajouter dans les serveurs**:

    ![Sélectionner Ajouter dans les serveurs](https://hackmd.io/_uploads/SkCWOFfAkl.png)
5.  **Créer un nouvel agent de compte OPENVPN sur ActiveDirectory**:

    ![Créer un nouvel agent de compte OPENVPN sur ActiveDirectory](https://hackmd.io/_uploads/HkrVbqz0ke.png)
6.  **Créer un serveur d'accès LDAP (1/2)**:

    ![Créer un serveur d'accès LDAP (1/2)](https://hackmd.io/_uploads/SyIrz9fRyl.png)
7.  **Créer un serveur d'accès LDAP (2/2)**:

    ![Créer un serveur d'accès LDAP (2/2)](https://hackmd.io/_uploads/HyAIzcMCyx.png)



















# OpenWRT

OpenWRT source : https://images.linuxcontainers.org/images/openwrt/24.10/amd64/default/20250212_11%3A57/

create container :

`pct create 492 /mnt/pve/iso-smb/template/cache/openWRT.tar.xz --arch amd64 --hostname RTR68COL02 --rootfs local-lvm:20 --memory 256 --cores 1 --ostype unmanaged --unprivileged 0`

![command to create container(above)](https://hackmd.io/_uploads/rkCjZcqKyx.png)

![add network](https://hackmd.io/_uploads/H1bzGcqtkl.png)

![add wan](https://hackmd.io/_uploads/S1vFm99Kkg.png)

![add lan](https://hackmd.io/_uploads/SJ90Xc9Kkx.png)

vi /etc/config/network

![start container and modify network config](https://hackmd.io/_uploads/Hk_7NqcKke.png)

```
config interface 'loopback'  
        option ifname 'lo'
        option proto 'static'
        option ipaddr '127.0.0.1'              
        option netmask '255.0.0.0'

config interface 'wan'     
        option type 'bridge'
        option ifname 'eth0' 
        option proto 'static'    
        option ipaddr '10.54.146.8'
        option netmask '255.255.255.0'
        option gateway '10.54.146.1'
                            
config interface 'lan'      
        option type 'bridge' 
        option ifname 'eth1'        
        option proto 'static'         
        option ipaddr '172.16.0.253'
        option netmask '255.255.255.0'
```

![comment out old config, add new one (above) then save (:wq)](https://hackmd.io/_uploads/BJYT45qKke.png)

/etc/init.d/network restart
![image](https://hackmd.io/_uploads/rkHHH9qtye.png)


# Dynfi


## Instalation

![welcome (install/shell/live CD)](https://hackmd.io/_uploads/HyFHiN9Fye.png)

![Keymap Selection](https://hackmd.io/_uploads/BJhYTEqt1x.png)

![Partiioning (UFS)](https://hackmd.io/_uploads/S1CsaVcF1e.png)

![Partition entire disk](https://hackmd.io/_uploads/S16aTEqY1l.png)

![MBR partion scheme](https://hackmd.io/_uploads/rJZlR49Y1e.png)

![review partition](https://hackmd.io/_uploads/Hy0ZA4qFyg.png)

![Commit (erase disk)](https://hackmd.io/_uploads/Skc7REcYkl.png)

![Wait for packages/system to be installed](https://hackmd.io/_uploads/r1u3dUqYkx.png)

![shutdown & remove install disk](https://hackmd.io/_uploads/rkLXYU5Y1x.png)

## Configuration de base (en mode tty)

On veut que activer une interface LAN pour administrer les pare-feu en mode WEB.

```
login : root
default password : dynfi
```

![After first boot login on ther router](https://hackmd.io/_uploads/BkoPCO2t1l.png)


![Go to the option 1 assign interfaces](https://hackmd.io/_uploads/BJ5lJFntyl.png)

![Enter the WAN interface name](https://hackmd.io/_uploads/Bksr1YhK1x.png)

![Enter the LAN interface name](https://hackmd.io/_uploads/SJ4OkKhFye.png)

![Enter yes to confirm the precedent actions](https://hackmd.io/_uploads/SJeAKJYnY1x.png)

![Select the option 2 to Set interface IP address](https://hackmd.io/_uploads/SyVn1YnKkg.png)

![IP configuration for LAN](https://hackmd.io/_uploads/B1MggK2tye.png)

![Do not configure IPV6 (Not used)](https://hackmd.io/_uploads/HJ0hbt3tyl.png)

## Config WEB (Wizard + Interfaces + HA)

![first time login](https://hackmd.io/_uploads/rJH4QF2Y1x.png)

![start wizard](https://hackmd.io/_uploads/r1Xc7thF1x.png)

![wizard : general info (hostname, domain [haut-rhin.gouv], dns (routers before [172.16.0.254 and .253]))](https://hackmd.io/_uploads/HkkzSt3YJe.png)

![wizard: ntp servers (no need to touch)](https://hackmd.io/_uploads/HJlEwSKhtJx.png)


![wizard: configure WAN interface (static addresse and gateway)](https://hackmd.io/_uploads/rJotTtnY1l.png)

![wizard: configure WAN interface (allow blogon & private networks)](https://hackmd.io/_uploads/S173aKhKyl.png)

![wizard: configure LAN interface](https://hackmd.io/_uploads/r11WCYnY1x.png)

```
root@passwd : Admin
```
![wizard: set admin password](https://hackmd.io/_uploads/HyLLCF3K1l.png)


![wizard: reload to finish setup](https://hackmd.io/_uploads/HJwwAFntJg.png)


### Modify Interfaces 

![Assign vnet0 to new PfSync](https://hackmd.io/_uploads/rylpAFnKJg.png)

![Set PfSync Address (SET IPV4)](https://hackmd.io/_uploads/SkA_yqhF1e.png)

![Set PfSync (SET Addresse (10.0.0.1 [MASTER]))](https://hackmd.io/_uploads/B1wYychFye.png)

![Set PfSync Address: reload](https://hackmd.io/_uploads/HJ7ny92Kye.png)

#### Allow any any traffic on interface PfSync

![Rules PfSync](https://hackmd.io/_uploads/S13N_92tke.png)

![Create Rule (IPV4 any in any out)](https://hackmd.io/_uploads/rJD9OchKyg.png)

![Create Rule (Description : PfSync)](https://hackmd.io/_uploads/H1bi_cnYkl.png)

---

![Assign vnet2 to new WANBackup](https://hackmd.io/_uploads/SkPl1c3Y1e.png)


Enable the WANBackup interface before the next steps.

![Create WANBackup Gateway](https://hackmd.io/_uploads/Hynmg92Fkx.png)

![Config WANBackup Gateway (IPV4 : 172.16.0.253)](https://hackmd.io/_uploads/Sy6l-93tkg.png)

Enable monitoring for WAN

![Set PfSync Address (SET IPV4)](https://hackmd.io/_uploads/ryOdb92F1e.png)

![image](https://hackmd.io/_uploads/SkdFZ5nYke.png)

Do the same for the second firewall, then start the HA config.

### HA config

![HA availibilty : Peer address (10.0.0.2) activate sync states](https://hackmd.io/_uploads/S1vQM5hYkg.png)


![HA availibilty : Peer address (10.0.0.2) sync everything](https://hackmd.io/_uploads/B1PNfq2Ykx.png)

### Setup CARP (LAN and WAN)

![Add a virtual IP interface](https://hackmd.io/_uploads/H1ml9q3Fyl.png)

![Configure CARP for LAN (172.16.1.254)](https://hackmd.io/_uploads/S1i7qq3F1e.png)

![Configure CARP for WAN (172.16.0.10)](https://hackmd.io/_uploads/HkQqq92Ykg.png)

![Configure CARP for WANBackup (172.16.0.20)](https://hackmd.io/_uploads/HyTvsc3Fye.png)

### Setup VLANs


![Add a VLAN](https://hackmd.io/_uploads/BJR9hcnYyx.png)

![VLAN 10](https://hackmd.io/_uploads/ryHuTqhY1l.png)

![VLAN 15](https://hackmd.io/_uploads/ryrhTqnYkx.png)

![VLAN 30](https://hackmd.io/_uploads/ryjJ093Fkl.png)

![VLAN 60](https://hackmd.io/_uploads/rkmz053KJx.png)

![VLAN 90](https://hackmd.io/_uploads/rJPHRchY1g.png)

![Assign all VLANS to an interface (VLAN10 to VLAN90)](https://hackmd.io/_uploads/rkEfJjhK1g.png)

![Setup interfaces for all VLANS (172.16.10.253/24 -> 172.16.90.253/24 on Firewall 1, and on 2 172.16.10.252/24 -> 172.16.90.252/24)](https://hackmd.io/_uploads/HyrTlinKJg.png)

![Setup interfaces for all VLANS (172.16.10.253/24 -> 172.16.90.253/24 on Firewall 1, and on 2 172.16.10.252/24 -> 172.16.90.252/24)](https://hackmd.io/_uploads/B1BRxinYkg.png)

![Setup interfaces for all VLANS (172.16.10.253/24 -> 172.16.90.253/24 on Firewall 1, and on 2 172.16.10.252/24 -> 172.16.90.252/24)](https://hackmd.io/_uploads/rk9lbsnK1e.png)

![Setup CARP for all VLANS (172.16.10.253/24 -> 172.16.90.253/24](https://hackmd.io/_uploads/Sk7c7nnKye.png)

### Setup DHCP relay

![Setup relay for interface VLAN30 (Clients) with servers 172.16.10.20 and .21 (AD DHCP servers)](https://hackmd.io/_uploads/ByqhSgwj1g.png)

### Setup OpenVPN

#### Setup PKI

##### Create certificate Authority

![Système >> Confiance >> Authority](https://hackmd.io/_uploads/HyBwih3F1g.png)

![Create a Certificate Authority (1/2)](https://hackmd.io/_uploads/Hyj4o2hKJg.png)

![Create a Certificate Authority (2/2)](https://hackmd.io/_uploads/B1iHo23tke.png)

##### Create certificate server

![Système >> Confiance >> Certificats](https://hackmd.io/_uploads/r1zEDh3FJe.png)

![Create a Certificate Server (1/2)](https://hackmd.io/_uploads/H14U32nYkl.png)

![Create a Certificate Server (2/2)](https://hackmd.io/_uploads/HJJD223FJl.png)

##### Setup TOTP

![image](https://hackmd.io/_uploads/BkmG62htJl.png)

##### Ajouter un serveur SSL

![REMOTE ACESS SSL/TLS + USer Auth](https://hackmd.io/_uploads/BJIAya3Fyl.png)

![Cryptography](https://hackmd.io/_uploads/Byeyg63Ykl.png)

![Tunnel settings](https://hackmd.io/_uploads/Hk6ylT3Fkg.png)

![Advanced settings (none changed)](https://hackmd.io/_uploads/S10eeT2t1l.png)

##### Setup LDAP

![Open Groups in System Settings](https://hackmd.io/_uploads/HJXSwYzRyx.png)

![Select Add in Groups](https://hackmd.io/_uploads/BkHFvFz0Jg.png)

![Create new Group OpenVPN LDAP](https://hackmd.io/_uploads/HJb6PYGA1x.png)

![Select Add in Servers](https://hackmd.io/_uploads/SkCWOFfAkl.png)

![Create a new agent OPENVPN account on ActiveDirectory](https://hackmd.io/_uploads/HkrVbqz0ke.png)

![Create LDAP Access Server (1/2)](https://hackmd.io/_uploads/SyIrz9fRyl.png)

![Create LDAP Access Server (2/2)](https://hackmd.io/_uploads/HyAIzcMCyx.png)

