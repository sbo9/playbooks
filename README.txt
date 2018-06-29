glassfish.yml
=============
Voici une br�ve description du playbook glassfish.yml. Le code est pull depuis GitHub. 
Il a pour vocation � �tre jou� � l'aide du plugin Ansible de Jenkins. 

Le playbook cr�e un container Glassfish sur les h�tes list�s dans le playbook et il d�ploie automatiquement le .war qui aura pr�alablement �t� build par Jenkins.

Pr�-requis
----------
1/ Docker doit �tre install� sur les machines cibles avec un volume autodeploy (volume li� au container glassfish).
2/ Les plugins Maven et Ansible doivent �tre install�s sur Jenkins.
3/ Un script post-build permet de renommer le .war.

Script post-build
-----------------
#!/bin/bash
cd /var/jenkins_home/workspace/Mavenjeered/target
mv JEERed-1.0-SNAPSHOT.war jeered.war

Infos sur les auteurs
---------------------
Team de gauche (Damien, Sylvain, Olivier, Eric)

