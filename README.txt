** WARNING : if you use github, use STABLE branch (v1.1.1) ! The code on master branch (v1.2) is not working ! ** 

Version history :
- 1.1 : stable version not working (bug)
- 1.1.1 : stable version working
- 1.2 : development stopped for now (see master branch, https://moodle.org/mod/forum/discuss.php?d=259371 and https://moodle.org/plugins/local_groupautoenrol)


moodle-local-groupautoenrol
===========================
Version 1.2 (dev version) : the version is not working !


**ENGLISH**
Plugin to randomly auto enrol students in Moodle courses groups when they are enrolled into the course (whatever the enrol methods : auto-enrol by key, cohorts sync or manual enrol)

Things to know :
- The plugin use "user_enrolled" Moodle event
- If a selected group is deleted, the plugin will ignore it.

Dev version (v1.2) : 
- you can choose to enable the plugin in each course
- you can choose to auto-enrol students in all existing course or specific ones
- you can choose which role(s) the enrolment will works (in progress)
- you can choose between random, balanced or alphabetic enrolment (in progress)

Requires Moodle 2.5 (we did not test it with the previous versions but should work with all 2.x)


installation
------------
* Copy the directory 'groupautoenrol' into the `moodledir/local` directory.
* Connect to moodle as an administrator and install the plugin.
* Enable the plugin in each course you want



**FRENCH**
Plugin permettant l'inscription automatique aléatoire des étudiants dans les groupes des cours lors de leur inscription au cours (qu'elle se fasse par la synchronisation des cohortes, par clé d'inscription ou manuellement).

Précisions
- Ce plugin utilise l'évènement "user_enrolled" pour détecter l'inscription d'un utilisateur dans un cours.
- Si un groupe sélectionné pour l'inscription auto est supprimé, il sera simplement ignoré par le plugin (cela ne pose pas de blocage).
- En cas d'inscription par clé de groupe, l'utilisateur est d'abord inscrit automatiquement (selon les paramètres définis) puis il est inscrit au groupe désigné par la clé.
Selon les paramètres, il peut donc se retrouver inscrits à 1 ou 2 groupes (si le tirage aléatoire a désigné le même groupe que celui de la clé). Je n'ai pas eu de message d'erreur lorsque Moodle tente d'inscrire l'utilisateur dans le groupe de la clé même losque celui a déjà été inscrit par le plugin "inscription_auto" dans le même groupe.


Version en cours de développement (1.2) :
- plugin activable par cours
- l'inscription automatique se fait dans tous les groupes du cours ou uniquement dans des groupes sélectionnés.
- il sera possible de choisir les rôles concernés par l'inscription automatique (en developpement)
- plusieurs modes d'inscriptions seront disponibles : aléatoire, réparti ou alphabétique (en developpement)

Requiert Moodle 2.5 (Non testé avec les versions précédentes mais il doit fonctionner avec toutes les versions de Moodle 2.x)


installation
------------
* Copier le dossier 'groupautoenrol' dans le répertoire `moodledir/local`.
* Se connecter en admin et installer le plugin.
* Activer et paramétrer le plugin dans chaque cours voulu.


credits
-------
* @copyright 2014 Université Paris Ouest Nanterre - Service COMETE
pascal.maury@inalco.fr {@link http://www.service-comete.u-paris10.fr}


licence
-------
This code is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.
 
It is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.
 
You should have received a copy of the GNU General Public License
along with this software. If not, see http://www.gnu.org/licenses/.
