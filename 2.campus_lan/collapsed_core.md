# Collapsed Core: LAN batiment unique
## Switching

L'objectif de cette section est de configurer et vérifier le fonctionement d'un réseau LAN d'entreprise.

Pour démarrer cette section vous configurerez un switch avec 2 hôtes et testerez le bon fonctionement.

![network-diagram](assets/collasped_core_switching.png)

[Configurez](1.env_setup/ansible_validation.md) l'IP de l'hôte Ansible avec les valeurs par défaut

[Configurez](1.env_setup/ansible_validation.md) l'IP de l'hôte 2 avec les valeurs : VLAN = 1 et HOST = 2

[Validez](1.env_setup/ansible_validation.md) la réussite de cette section avec le playbook 002

## Segmentation des domaines de diffusion: VLAN
### VLAN & Table CAM
### VLAN Switching: Tags, Trunks, 802.1q
### VLANs: VTP, DTP
## Redondance des liaisons
### Spanning-Tree
### Etherchannels
## Routage Inter-Vlan
### Router on a stick
### Layer 3 switch
## Securisation des réseaux
### ACLs
### MACLs
### VACLs
### Creation d'une DMZ