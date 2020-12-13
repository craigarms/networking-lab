# Service d'auto-validation

Les Labs de ce TP vont tenter d'utiliser Ansible pour valider que les objectifs de chaque étapes ont été atteint, ceci est *très* experimental mais permet de manipuler Ansible ainsi que des playbook qui pourraient être utilisés comme base à des scripts de monitoring de production.

L'appliance Docker utilisé sera `craigarms/lab-ansible`

L'installation s'efféctuera:
 * Par import dans GNS3
 * Par téléchargement via la commande `docker pull craigarms/lab-ansible`
 * Par build local 
   * En clonant le repo github `git clone https://github.com/craigarms/docker-lab-ansible.git`
   * En utilisant l'utilitaire de build `docker build -t craigarms/lab-ansible` docker-lab-ansible