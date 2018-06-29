glassfish.yml
=============
Voici une brève description du playbook glassfish.yml. Le code est pull depuis GitHub. 
Il a pour vocation à être joué à l'aide du plugin Ansible de Jenkins. 

Le playbook crée un container Glassfish sur les hôtes listés dans le playbook et il déploie automatiquement le .war qui aura préalablement été build par Jenkins.

Pré-requis
----------
1/ Docker doit être installé sur les machines cibles avec un volume autodeploy (volume lié au container glassfish).
2/ Les plugins Maven et Ansible doivent être installés sur Jenkins.
3/ Un script post-build permet de renommer le .war.

Script post-build
-----------------
#!/bin/bash
cd /var/jenkins_home/workspace/Mavenjeered/target
mv JEERed-1.0-SNAPSHOT.war jeered.war

Infos sur les auteurs
---------------------
Team de gauche (Damien, Sylvain, Olivier, Eric)

