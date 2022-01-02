# Configuration ansible
Ce projet contient la configuration d'installation d'un nouveau poste via ansible.

### Fichiers
- DockerFile : Un fichier docker pour tester dans un container le fonctionnement du projet afin de ne pas executer l'installation sur une configuration déjà existante
- main.yml : Le playbook a executer lors de l'installation

### Comment tester
Afin de faire évoluer le projet il est nécessaire de lancer le playbook dans un container nouvellement créer disposant des droits d'accès.

Le docker file fourni un environnement adapté à cette problèmatique:
```
# Lancer le build
docker build -t ansible-testing .

# Se connecter au container avec un terminal en disposant des droits root
docker run --rm -it -u 0 ansible-testing  bash
```
