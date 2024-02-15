## Projet de GL : 
## Partie 1 : Audit du projet
Sara Lyna OUYAHIA


## Contexte :

- Analyse du projet Red5-Server :

- `https://github.com/Red5/red5-server`


# 1) Présentation Globale du projet :

## 1.1) Utilité du projet

- Ce dépot contient le code source du projet Red5-Server . Il s'agit de :
Red5 est un serveur Flash gratuit et libre qui reprend les fonctionnalités de Flash Media Server de Adobe.

- Il permet de faire du streaming audio ou vidéo, partage d'objet distant (remoting), de la synchronisation de données, etc. Contrairement à Flash Media Server 2, les applications côté serveur peuvent être écrites en Java mais aussi avec d’autres langages de script comme JavaScript, Ruby, Python, …

- `english version `
Red5 is an Open Source Flash Server written in Java that supports:

	- Streaming Video (FLV, F4V, MP4, 3GP)
	- Streaming Audio (MP3, F4A, M4A, AAC)
	- Recording Client Streams (FLV and AVC+AAC in FLV container)
	- Shared Objects
	- Live Stream Publishing
	- Remoting
	- Protocols: RTMP, RTMPT, RTMPS, and RTMPE

## 1.2) Description du projet :

- Le readme est pertinent, il y a les commandes essentielles pour faire marcher le projet telle la compilation et l'exécution.
To build the red5 jars, execute the following on the command line:

- `mvn -Dmaven.test.skip=true install`
This will create the jars in the "target" directory of the workspace; this will also skip the unit tests.

- To package everything up in an assembly (tarball/zip):

`mvn -Dmaven.test.skip=true clean package -P assemble`

- To build a milestone tarball:

`mvn -Dmilestone.version=1.0.7-M1 clean package -Pmilestone`

- Create the eclipse project files, execute this within red5-server directory.
`mvn eclipse:eclipse`

- le projet est bien décrit dans le readme, on sait exactement ce qu'il fait .
- Il manque peut-etre l'UML mais rien de bien méchant.


# 2) Historique du logiciel :

## 2.1) Analyse du git :
- Nombre de contributeurs de The Red5 Project : 14
Luke Hubbard (luke@codegent.com)
Dominick Accattato (daccattato@gmail.com)
Chris Allen (mrchrisallen@gmail.com)
Joachim Bauch (jojo@struktur.de)
Mick Herres (mickherres@hotmail.com)
John Grden (johng@acmewebworks.com)
Grant Davies (grant@bluetube.com)
Steven Elliott (steven.s.elliott@gmail.com)
Jokul Tian (tianxuefeng@gmail.com)
Steven Gong (steven.gong@gmail.com)
Paul Gregoire (mondain@gmail.com)
Michael Klishin (michael.s.klishin@gmail.com)
Thijs Triemstra (info@collab.nl)
Dan Rossi (electroteque@gmail.com)
Anton Lebedevich (mabrek@gmail.com)
Art Clarke (aclarke@xuggle.com)
Tiago Daniel Jacobs (tiago@imdt.com.br)

- Sponsor du projet :  `ko-fi.com/mondain`

- Nombre de commits total : 615

- Issues : 35

- Pull-Request : 5



- on peut remarquer que `ko-fi.com/mondain` est bel et bien le contributeur principal,
un site spécial pour que tout le monde puisse corriger les bugs en open source.


- Le projet est toujours actif à l'heure d'aujourd'hui,le dernier commit date de 3 semaines, pour un porjet de cette envergure on peut dire qu'il est assez bien maintenu.



- Au total il y a six branches distinctes,
master : la branche par défaut
bug/R5SI-786
dependabot/maven/org.springframework-spring-web-6.0.0
stable-release
epic/GROGU
circleci-project-setup




# 3) Architecture logicielle :

## 3.1) Utilisation de bibliothèques extérieures :

le nombre de bibliothèques extérieures référencées : 46 bibliothéques externes et la plus part sont des bibliothèques maven-org, maven-junit, et maven-common.

la différence entre les bibliothèques référencées et celles utilisées :

les bibliothèques réellement utilisées :
 
 
## 3.2) Organisation en paquetages :

le nombre de paquetages : il y a 6 packages principaux

les liens entre les paquetages :

les noms des paquetages : client , on peut comprendre que c'est le package qui gère les clients
server : le server de sockets 
server- common : pas très évident à deviner à quoi sert ce package
io : les sockets et les controllers
service  et parent




## 3.3) Répartition des classes dans les paquetages :

 le nombre de classes par paquetage :
 
 la répartition des classes dans les différents paquetages : 
 
 le couplage et la cohésion au sein des paquetages de quelques uns en
particulier :




## 3.4) Organisation des classes :

la hiérarchie des classes :

la profondeur de l’arbre d’héritage (DIT ) :

le nombre d’enfants par classes (min, max ou moyenne) (NOC ) :
 
la stabilité des classes en général ou de quelques unes en particulier :

la cohésion des classes au sein d’un paquetage en particulier :





# 4) Analyse approfondie :

## 4.1) Tests :

le nombre de tests : il est intéressant de remarquer que  dans le projet on nous dit de skip les tests, et de ce fait on a 0 tests qui passent alors qu'ils ont bel et bien fait des tests !
Red5 ............................................... SUCCESS [  0.009 s]
[INFO] Red5 :: IO ......................................... SUCCESS [  8.696 s]
[INFO] Red5 :: Server Common .............................. SUCCESS [  5.060 s]
[INFO] Red5 :: Service .................................... SUCCESS [  0.290 s]
[INFO] Red5 :: Server ..................................... FAILURE [  1.069 s]
[INFO] Red5 :: Client ..................................... SKIPPED
 on a les tests de IO, Server Common, Service qui passent, contrairement à ceux de Server qui échouent (c'est d'ailleurs normal car dans le dossier Server il n' y a quasiment aucun test),
 et concernant le dossier Client on ils ont été skip car dans les tests ils ont mis une variable pour expressement skip les tests.

la couverture de tests : couverture de tests très faible (0-5%), il y a des tests quasiment vides et donc on optera plutot pour l'analyse du code que l'analyse des tests en profondeur ( car il n'y en a quasiment pas !! ).
sur 31k lignes de code.


le type de tests : unitaires


les tests passent : on nous a dit de skip, mais la majorité des tests passent bien oui
concernant les commentaires on avait remarqué que plein de tests ont été commentés ( probablement car ils ne passaient pas)


nombre de bugs : 230 ! c'est énorme, mais pour un projet pareil je pense que c'est cohérent,
depuis le temps c'est vrai qu'ils auraient pu corriger les bugs.

et niveau sécurité ça laisse à désirer, on a une note de E niveau sécurité.




## 4.2) Commentaires :

le nombre de lignes de commentaires : concernant les commentaires on avait remarqué que plein de tests ont été commentés ( probablement car ils ne passaient pas),


le type de commentaire: Javadoc, code commenté, licence, commentaire
pertinent :


les parties sans commentaires :




## 4.3) Dépréciation :

les bouts de code dépréciés (classes, méthodes) :

les appels à du code déprécié :



## 4.4) Duplication du code :
 
le code dupliqué : 4% de code dupliqué, plutot pas mal, on a 57k de lignes de code dupliquées. et 161 blocs dupliqués, on aurait facilement pu améliorer ça.
 
## 4.5) God Classes :

le nombre de méthodes par classe (min, max, moyenne, médiane) :

le nombre de variables d’instances par classe (min, max, moyenne, médi-
ane). Comparaison avec les résultats trouvés à la question précédente :


le nombre de lignes de code par classe (min, max, moyenne, médiane),
Comparaison avec les résultats trouvés à la question précédente :


les gods classes :


## 4.6) Analyse des méthodes :

la complexité cyclomatique des méthodes en général ou de quelques unes
en particulier (avec min, max, moyenne, médiane) :


les commentaires. Les commentaires sont-ils bien placés (les méthodes
avec une plus grande complexité cyclomatique ont elles également le plus grand
nombre de lignes de commentaire) :


le nombre de lignes de codes des méthodes (avec min, max, moyenne,
médiane) :



# 5) Nettoyage de Code et Code smells :

## 5.1) Règles de nommage :
le nom des packages est bien choisi, simple et efficace , on comprend qu'il y a un dossier Server qui gère les servers, un dossier client, un dossier IO pour les sockets, et Service pour les services que propose le logiciel.

## 5.2) Nombre magique :


## 5.3) Structure du code : 


## 5.4) Code mort :
Code Smells : 3000 !


---------------------------------------------------------
## Partie 2 : Amélioration du projet

# 6) Petites modifications :
- Coder quelques tests en plus histoire d'avoir plus de couverture.
- Décommenter les tests et essayer de les débuger.
- Faire un UML !

# 7) Moyennes modifications :


# 8) Grandes modifications :










