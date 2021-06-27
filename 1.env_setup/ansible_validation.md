# Service d'auto-validation

Les Labs de ce TP vont tenter d'utiliser Ansible pour valider que les objectifs de chaque étapes ont été atteint, ceci est *très* experimental mais permet de manipuler Ansible ainsi que des playbook qui pourraient être utilisés comme base à des scripts de monitoring de production.

L'appliance Docker utilisé sera `craigarms/lab-ansible`

L'installation s'efféctuera:
 * Par import dans GNS3
 * Par téléchargement via la commande `docker pull craigarms/lab-ansible`
 * Par build local 
   * En clonant le repo github `git clone https://github.com/craigarms/docker-lab-ansible.git`
   * En utilisant l'utilitaire de build `docker build -t craigarms/lab-ansible` docker-lab-ansible

## Playbooks

Le dossier de travail par défaut est /playbooks.

L'execution d'un playbook se fait avec la commande "ansible-playbook NOM_DU_FICHIER_PLAYBOOK"

Ils sont numérotés afin de simplifier l'autocomplétion.

Si le playbook ne retourne pas de fail vous avez validé avec succès le fonctionement de la section.


## Configuration de l'IP

Un Playbook helper existe afin de configurer l'adresse IP ainsi que la gateway.

Dans chaque section qui le requière sera précisé la variable VLAN ainsi que HOST qui permettront de configurer les 3ème et 4ème octects de l'adresse IP de l'interface eth0.

Afin de passer ces informations au playbook il faut exporter les informations à l'environement :

```
export VLAN=10
export HOST=5

ansible-playbook 001_configure_local_ip.yml
```

en cas d'IP déjà configurée vous pouvez tout supprimer avec 

```
ip address flush dev eth0
```