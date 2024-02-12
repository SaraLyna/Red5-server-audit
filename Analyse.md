## Projet de GL : 
## Partie 1 : Audit du projet
Sara Lyna OUYAHIA


## Contexte :

Analyse du projet Red5-Server :

`https://github.com/Red5/red5-server`


# Présentation Globale du projet :

## Utilité du projet

Ce dépot contient le code source du projet Red5-Server . Il s'agit de :
Red5 est un serveur Flash gratuit et libre qui reprend les fonctionnalités de Flash Media Server de Adobe.

Il permet de faire du streaming audio ou vidéo, partage d'objet distant (remoting), de la synchronisation de données, etc. Contrairement à Flash Media Server 2, les applications côté serveur peuvent être écrites en Java mais aussi avec d’autres langages de script comme JavaScript, Ruby, Python, …

`english version `
Red5 is an Open Source Flash Server written in Java that supports:

- Streaming Video (FLV, F4V, MP4, 3GP)
- Streaming Audio (MP3, F4A, M4A, AAC)
- Recording Client Streams (FLV and AVC+AAC in FLV container)
- Shared Objects
- Live Stream Publishing
- Remoting
- Protocols: RTMP, RTMPT, RTMPS, and RTMPE

## Description du projet :

Le readme est pertinent, il y a les commandes essentielles pour faire marcher le projet telle la compilation et l'exécution.
To build the red5 jars, execute the following on the command line:

`mvn -Dmaven.test.skip=true install`
This will create the jars in the "target" directory of the workspace; this will also skip the unit tests.

To package everything up in an assembly (tarball/zip):

`mvn -Dmaven.test.skip=true clean package -P assemble`

To build a milestone tarball:

`mvn -Dmilestone.version=1.0.7-M1 clean package -Pmilestone`

Create the eclipse project files, execute this within red5-server directory.
`mvn eclipse:eclipse`

le projet est bien décrit dans le readme, on sait exactement ce qu'il fait .
Il manque peut-etre l'UML mais rien de bien méchant.


# Historique du logiciel :

## Analyse du git :
Nombre de contributeurs : 14

Sponsor du projet :  `ko-fi.com/mondain`

Nombre de commits total : 615

Issues : 35

Pull-Request : 5



on peut remarquer que `ko-fi.com/mondain` est bel et bien le contributeur principal,


Le projet est toujours actif à l'heure d'aujourd'hui,le dernier commit date de 3 semaines, pour un porjet de cette envergure on peut dire qu'il est assez bien maintenu.



Au total il y a six branches distinctes,
master : la branche par défaut
bug/R5SI-786
dependabot/maven/org.springframework-spring-web-6.0.0
stable-release
epic/GROGU
circleci-project-setup




# Architecture logicielle :

## Utilisation de bibliothèques extérieures :

le nombre de bibliothèques extérieures référencées : 

la différence entre les bibliothèques référencées et celles utilisées :

les bibliothèques réellement utilisées :
 
 
## Organisation en paquetages :

le nombre de paquetages :

les liens entre les paquetages :

les noms des paquetages :




## Répartition des classes dans les paquetages :

 le nombre de classes par paquetage :
 
 la répartition des classes dans les différents paquetages : 
 
 le couplage et la cohésion au sein des paquetages de quelques uns en
particulier :




## Organisation des classes :

la hiérarchie des classes :

la profondeur de l’arbre d’héritage (DIT ) :

le nombre d’enfants par classes (min, max ou moyenne) (NOC ) :
 
la stabilité des classes en général ou de quelques unes en particulier :

la cohésion des classes au sein d’un paquetage en particulier :





# Analyse approfondie :

## Tests :

le nombre de tests : 

la couverture de tests : 


le type de tests : unitaires


les tests passent : 







## Commentaires :

le nombre de lignes de commentaires :

le type de commentaire: Javadoc, code commenté, licence, commentaire
pertinent :


les parties sans commentaires :




## Dépréciation :

les bouts de code dépréciés (classes, méthodes) :

les appels à du code déprécié :



## Duplication du code :
 
le code dupliqué : 
 
 
## God Classes :

le nombre de méthodes par classe (min, max, moyenne, médiane) :

le nombre de variables d’instances par classe (min, max, moyenne, médi-
ane). Comparaison avec les résultats trouvés à la question précédente :


le nombre de lignes de code par classe (min, max, moyenne, médiane),
Comparaison avec les résultats trouvés à la question précédente :


les gods classes :


## Analyse des méthodes :

la complexité cyclomatique des méthodes en général ou de quelques unes
en particulier (avec min, max, moyenne, médiane) :


les commentaires. Les commentaires sont-ils bien placés (les méthodes
avec une plus grande complexité cyclomatique ont elles également le plus grand
nombre de lignes de commentaire) :


le nombre de lignes de codes des méthodes (avec min, max, moyenne,
médiane) :



# Nettoyage de Code et Code smells :

## Règles de nommage :

## Nombre magique :


## Structure du code : 


## Code mort :


---------------------------------------------------------
## Partie 2 : Amélioration du projet

# Petites modifications :

# Moyennes modifications :


# Grandes modifications :










