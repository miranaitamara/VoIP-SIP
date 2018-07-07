#Appels VoIP basés sur SIP

Session Initiation Protocol (SIP) , un protocole client-serveur est utilisé dans ce projet. SIP est utilisé pour établir la session entre deux parties ou plus. C'est un protocole de communication, utilisé pour la signalisation d'appel et le contrôle des sessions multimédia dans l'application pour la voix, la vidéo et la messagerie sur les réseaux IP.

Il s'agit d'une application ainsi que du protocole de couche de session, selon la fonctionnalité qu'il exécute sur une instance. Il fonctionne en association avec d'autres protocoles de couche d'application tels que H.323.

Dans mon projet, j'ai utilisé 4 machines, dont une fonctionne en tant que serveur, tandis que trois autres sont des clients. La machine fonctionnant en tant que serveur a un système d'exploitation Linux; tandis que les clients sont exploités sur Windows OS.

J'ai examiné quatre conditions d'appel, qui comprend:

**Établissement d'appel** - L'appel est établi entre le client et le serveur avec différents identifiants.

**Utilisateur occupé** - Dans ce mode de fonctionnement, un utilisateur essaie d'appeler un autre utilisateur, mais l'autre utilisateur est occupé. La durée pendant laquelle l'utilisateur souhaite définir le mode occupé est envoyée en tant qu'argument dans le fichier extension.conf.

**Appel en attente** - Dans cette phase, un troisième utilisateur appelle le premier utilisateur avec l'ID 100, qui est déjà en communication avec le deuxième utilisateur. Il garde ensuite l'appel en attente et établit l'appel avec le troisième utilisateur.

**Conférence d'appel** - Dans ce scénario, le troisième utilisateur appelle le premier, alors qu'un appel est déjà en cours dans les 1er et 2ème utilisateurs. Le deuxième utilisateur met en attente et établit l'appel, puis invite à nouveau le premier utilisateur et un appel de conférence est établi.

Dans la 2ème partie du projet, j'ai développé un script Python et utilisé la bibliothèque PJSIP pour l'implémentation de SIP.

En outre, j'ai calculé la valeur MoS des appels entre les utilisateurs, en leur envoyant un ping et en surveillant la livraison réussie des paquets d'un utilisateur à l'autre. Bien que la valeur de MoS est sortie pour être grande (maximum) puisque les appels ont été faits sur une connexion LAN.
